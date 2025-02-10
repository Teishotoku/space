<script lang="ts">
	import SectionMain from 'sections/sectionMain.svelte';
</script>

<main>
	<SectionMain />
</main>

<style lang="scss">
	@use 'scss' as *;
	main {
		width: 100vw;
		height: 100vh;
		background-color: $prim;
		@include columnAround;
	}
</style>
