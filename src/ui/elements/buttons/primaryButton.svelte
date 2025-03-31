<script lang="ts">
	let props = $props<string>();
</script>

<button class={props.cls}>{props.txt}</button>

<style lang="scss">
	@use 'scss' as *;
	button {
		background: linear-gradient(to right, $red, $orange);
		color: $black;
		border-radius: $rdBig $rdLit $rdBig $rdLit;
		border: none;
		font-family: bold;
		transition: 0.4s all;
		&:hover {
			background: linear-gradient(to right, $red, $blue);
		}
	}
</style>
