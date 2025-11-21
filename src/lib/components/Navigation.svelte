<script lang="ts">
	import { slide } from 'svelte/transition';

	let { currentPath = $bindable('/') } = $props();
	let mobileMenuOpen = $state(false);
</script>

<nav class="fixed top-0 left-0 right-0 z-50 bg-black border-b border-white/10">
	<div class="max-w-7xl mx-auto px-6">
		<div class="flex items-center justify-between py-4">
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

			<!-- Mobile Menu Button (44px touch target) -->
			<button
				class="md:hidden w-11 h-11 flex items-center justify-center text-white/60 hover:text-white transition-colors duration-150"
				onclick={() => (mobileMenuOpen = !mobileMenuOpen)}
				aria-label={mobileMenuOpen ? 'Close menu' : 'Open menu'}
			>
				{#if mobileMenuOpen}
					<svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
					</svg>
				{:else}
					<svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
					</svg>
				{/if}
			</button>
		</div>

		<!-- Mobile Navigation Menu -->
		{#if mobileMenuOpen}
			<div transition:slide={{ duration: 200 }} class="md:hidden py-4 border-t border-white/10">
				<div class="flex flex-col gap-4">
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
			</div>
		{/if}
	</div>
</nav>
