<script lang="ts">
	import NamingBlock from 'blocks/namingBlock.svelte';
</script>

<section>
	<NamingBlock txt="System" />
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include section;
		@include columnEvenly;
	}
</style>
