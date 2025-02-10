<script lang="ts">
	import PresentBlock from 'blocks/presentBlock.svelte';
</script>

<main>
	<PresentBlock txt="welcome from about" link="/" where="home" />
</main>

<style lang="scss">
	@use 'scss' as *;
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
