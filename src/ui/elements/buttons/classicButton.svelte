<script lang="ts">
	let props = $props();
</script>

<button>{props.txt}</button>

<style lang="scss">
	@use 'scss' as *;
	button {
		background-color: $black;
		color: $orange;
		border-radius: $rdMed;
		font-size: $fnBut;
		padding: 1% 3%;
		border: none;
		@include transit;
		&:hover {
			background-color: $white;
			color: $black;
		}
	}
</style>
