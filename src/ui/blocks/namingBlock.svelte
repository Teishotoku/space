<script lang="ts">
	let props = $props<string>();
</script>

<div>
	<h1>{props.txt}</h1>
	<hr />
</div>

<style lang="scss">
	@use 'scss' as *;
	h1 {
		font-size: $fnDash;
		background: linear-gradient(to right, $red, $orange);
		-webkit-text-fill-color: transparent;
		-webkit-background-clip: text;
	}
	hr {
		@include brdr;
		height: 4px;
		background: linear-gradient(to right, $red, $orange);
		color: transparent;
	}
</style>
