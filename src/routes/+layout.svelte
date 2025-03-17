<script lang="ts">
	let { children } = $props();
</script>

<svelte:head>
	<title>Teishotoku</title>
</svelte:head>

<main>
	{@render children()}
</main>
