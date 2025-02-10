<script lang="ts">
	let props = $props();
</script>

<div>
	<h2>{props.txt}</h2>
	<a href={props.link}>{props.where}</a>
</div>

<style lang="scss">
	@use 'scss' as *;
	div {
		@include column;
	}
	h1,
	h2 {
		color: $black;
	}
</style>
