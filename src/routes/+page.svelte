<script lang="ts">
	import 'css/index.scss';
	import { store } from '../store/global.svelte';
</script>

<main>
	<h1>Welcome to SveltePattern</h1>
	<h2>{store.value}</h2>
	<a href="/about">about</a>
</main>

<style lang="scss">
	@use 'css' as *;
	main {
		width: 100vw;
		height: 100vh;
		background-color: $prim;
		@include column;
	}
	h1 {
		color: $black;
	}
</style>
