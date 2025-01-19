<script lang="ts">
	import 'css/index.scss';
</script>

<main>
	<h1>hello from about</h1>
	<a href="/">home</a>
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
