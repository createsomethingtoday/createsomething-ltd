<script lang="ts">
	import DomainStandardCard from '$lib/components/DomainStandardCard.svelte';

	const domainStandards = [
		{
			domain: '.io',
			title: 'Research Standards',
			standards: [
				'Every paper must answer: <strong>Is this useful?</strong> Not interesting, not novel—useful.',
				'Findings must be <strong>reproducible</strong>. Methodology transparent. Metrics honest.',
				'Writing serves the reader. <strong>Clarity over cleverness.</strong> Simple language over jargon.',
				'If a principle from .ltd applies, cite it. <strong>Connect theory to the lineage.</strong>'
			]
		},
		{
			domain: '.space',
			title: 'Practice Standards',
			standards: [
				'Every experiment must <strong>teach a principle</strong>, not just a technique.',
				'Interfaces are minimal. <strong>Zero decoration.</strong> Only essential feedback.',
				'Success is completion, not clicks. <strong>Measure learning, not engagement.</strong>',
				'Link to .io for depth, to .ltd for philosophy. <strong>Practice without context is shallow.</strong>'
			]
		},
		{
			domain: '.agency',
			title: 'Service Standards',
			standards: [
				'Delivered work must meet canonical standards. <strong>No shortcuts, no compromises.</strong>',
				'Solutions solve problems. <strong>Not features for features\' sake.</strong>',
				'Documentation is complete. Code is readable. <strong>Future maintainers are users too.</strong>',
				'Case studies cite which .ltd principles were applied. <strong>Proof, not just claims.</strong>'
			]
		}
	];
</script>

<svelte:head>
	<title>Ethos — CREATE SOMETHING.ltd</title>
	<meta
		name="description"
		content="How Create Something applies the canon of 'less, but better' across research, practice, and services."
	/>
</svelte:head>

<!-- Header -->
<section class="pt-24 pb-16 px-6 border-b border-white/10">
	<div class="max-w-4xl mx-auto text-center">
		<p class="text-sm tracking-widest uppercase opacity-60 mb-4">Our Philosophy</p>
		<h1 class="mb-6">Ethos</h1>
		<p class="text-xl opacity-70 leading-relaxed">
			How we apply the canon of "less, but better" across the Create Something ecosystem.
		</p>
	</div>
</section>

<!-- Core Philosophy -->
<section class="py-16 px-6">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">Less, But Better</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p>
				<strong>This isn't minimalism for aesthetics.</strong> It's discipline for clarity. It's constraint
				for excellence.
			</p>

			<p>
				Dieter Rams asked: "Is my design good design?" We ask the same of every experiment, every
				paper, every line of code. The answer requires ruthless honesty.
			</p>

			<p>
				Mies van der Rohe proved that "less is more" in architecture. We prove it in software. Not
				by removing features—by ensuring every element justifies its existence.
			</p>

			<p>
				The Eameses showed us "the best for the most for the least." We build tools that serve
				developers without waste, without bloat, without compromise.
			</p>
		</div>
	</div>
</section>

<!-- Standards for Each Domain -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-5xl mx-auto">
		<h2 class="mb-12 text-center">Standards Across the Ecosystem</h2>

		<div class="space-y-12">
			{#each domainStandards as standard}
				<DomainStandardCard domainStandard={standard} />
			{/each}
		</div>
	</div>
</section>

<!-- The Hermeneutic Circle -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">The Hermeneutic Circle</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p>
				.ltd provides the <strong>horizon of understanding</strong> for everything else. You can't
				evaluate research (.io) without standards. You can't design practice (.space) without
				principles. You can't deliver services (.agency) without a philosophical ground.
			</p>

			<p>
				But the circle feeds back: real-world outcomes test the canon. If a principle doesn't hold
				in production, it doesn't belong in .ltd. The canon evolves—slowly, carefully—through
				validation.
			</p>

			<div class="mt-12 p-8 border border-white/10 rounded-xl">
				<pre class="text-sm opacity-60 font-mono leading-relaxed overflow-x-auto">
.ltd (STANDARDS)
    ↓ provides criteria
.io (RESEARCH)
    ↓ validated through
.space (PRACTICE)
    ↓ applied to clients
.agency (SERVICES)
    ↓ feeds back to
.ltd (ethos evolves)
				</pre>
			</div>
		</div>
	</div>
</section>

