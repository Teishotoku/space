<script lang="ts">
	let { children } = $props();
	import Header from 'blocks/header.svelte';
	import Footer from 'blocks/footer.svelte';
</script>

<svelte:head>
	<title>Teishotoku</title>
</svelte:head>

<main>
	<Header />
	{@render children()}
	<Footer />
</main>
