<script lang="ts">
	let props = $props<string>();
</script>

<div>
	<h1>{props.txt}</h1>
	<hr />
</div>

<style lang="scss">
	@use 'scss' as *;
	div {
		height: 20%;
		@include column;
	}
	h1 {
		font-size: $fnDash;
		background: linear-gradient(to right, $red, $orange);
		-webkit-text-fill-color: transparent;
		-webkit-background-clip: text;
	}
	hr {
		@include brdr;
		height: 4px;
		width: 100%;
		background: linear-gradient(to right, $red, $orange);
		color: transparent;
	}
</style>
