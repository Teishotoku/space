<script lang="ts">
	import NamingBlock from 'blocks/namingBlock.svelte';
</script>

<section>
	<NamingBlock txt="Blog" />
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include section;
		@include columnEvenly;
	}
</style>
