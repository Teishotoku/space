<script lang="ts">
	import NamingBlock from 'blocks/namingBlock.svelte';
</script>

<section>
	<NamingBlock txt="Blog" />
	<h1>Coming soon.</h1>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include section;
		@include columnEvenly;
		h1 {
			color: $prim;
		}
	}
</style>
