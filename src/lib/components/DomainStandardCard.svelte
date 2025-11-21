<script lang="ts">
	type DomainStandard = {
		domain: string;
		title: string;
		standards: string[];
	};

	let { domainStandard }: { domainStandard: DomainStandard } = $props();
</script>

<div class="border border-white/10 rounded-xl p-8">
	<div class="mb-6">
		<span class="text-xs font-mono opacity-40">{domainStandard.domain}</span>
		<h3 class="text-2xl font-semibold mt-2">{domainStandard.title}</h3>
	</div>

	<ul class="space-y-4 text-base opacity-70">
		{#each domainStandard.standards as standard}
			<li class="flex items-start gap-3">
				<span class="opacity-40 mt-1">—</span>
				<span>{@html standard}</span>
			</li>
		{/each}
	</ul>
</div>
