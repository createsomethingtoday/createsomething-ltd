<script lang="ts">
	import Navigation from '$lib/components/Navigation.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import '../app.css';

	let { children, data } = $props();
</script>

<svelte:head>
	<meta name="theme-color" content="#FFFFFF" />
</svelte:head>

<div class="min-h-screen flex flex-col">
	<Navigation currentPath={data?.pathname || '/'} />

	<main class="flex-1">
		{@render children()}
	</main>

	<Footer />
</div>
