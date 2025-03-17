<script lang="ts">
	import PresentBlock from 'blocks/presentBlock.svelte';
	import { store } from 'store/global.svelte';
	import ClassicButton from 'buttons/classicButton.svelte';
</script>

<section>
	<h1>Welcome to SvelteEtude</h1>
	<PresentBlock txt={store.value} link="/about" where="about" />
	<ClassicButton txt="yep" />
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		width: 50%;
		height: 50%;
		@include columnAround;
	}
</style>
