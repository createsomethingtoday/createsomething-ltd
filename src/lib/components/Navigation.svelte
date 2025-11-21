<script lang="ts">
	let { currentPath = $bindable('/') } = $props();
	let mobileMenuOpen = $state(false);
</script>

<nav class="border-b border-white/10">
	<div class="max-w-7xl mx-auto px-6 py-6">
		<div class="flex items-center justify-between">
			<!-- Logo / Home -->
			<a href="/" class="text-xl font-bold tracking-tight">
				CREATE SOMETHING
				<span class="font-normal opacity-60">.ltd</span>
			</a>

			<!-- Desktop Navigation Links -->
			<div class="hidden md:flex items-center gap-8">
				<a
					href="/masters"
					class="text-sm font-medium {currentPath.startsWith('/masters')
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
				>
					Masters
				</a>
				<a
					href="/patterns"
					class="text-sm font-medium {currentPath.startsWith('/patterns')
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
				>
					Patterns
				</a>
				<a
					href="/principles"
					class="text-sm font-medium {currentPath.startsWith('/principles')
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
				>
					Principles
				</a>
				<a
					href="/standards"
					class="text-sm font-medium {currentPath.startsWith('/standards')
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
				>
					Standards
				</a>
				<a
					href="/ethos"
					class="text-sm font-medium {currentPath === '/ethos'
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
				>
					Ethos
				</a>
			</div>

			<!-- Mobile Menu Button -->
			<button
				class="md:hidden text-sm font-medium opacity-60 hover:opacity-100"
				onclick={() => (mobileMenuOpen = !mobileMenuOpen)}
				aria-label="Toggle menu"
			>
				{mobileMenuOpen ? '✕' : '☰'}
			</button>
		</div>

		<!-- Mobile Navigation Menu -->
		{#if mobileMenuOpen}
			<div class="md:hidden pt-6 flex flex-col gap-4">
				<a
					href="/masters"
					class="text-sm font-medium {currentPath.startsWith('/masters')
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
					onclick={() => (mobileMenuOpen = false)}
				>
					Masters
				</a>
				<a
					href="/patterns"
					class="text-sm font-medium {currentPath.startsWith('/patterns')
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
					onclick={() => (mobileMenuOpen = false)}
				>
					Patterns
				</a>
				<a
					href="/principles"
					class="text-sm font-medium {currentPath.startsWith('/principles')
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
					onclick={() => (mobileMenuOpen = false)}
				>
					Principles
				</a>
				<a
					href="/standards"
					class="text-sm font-medium {currentPath.startsWith('/standards')
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
					onclick={() => (mobileMenuOpen = false)}
				>
					Standards
				</a>
				<a
					href="/ethos"
					class="text-sm font-medium {currentPath === '/ethos'
						? 'opacity-100'
						: 'opacity-60 hover:opacity-100'}"
					onclick={() => (mobileMenuOpen = false)}
				>
					Ethos
				</a>
			</div>
		{/if}
	</div>
</nav>
