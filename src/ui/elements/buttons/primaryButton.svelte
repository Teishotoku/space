<script lang="ts">
	let props = $props<string>();
</script>

<button class={props.cls}><a href={props.href}>{props.txt}</a></button>

<style lang="scss">
	@use 'scss' as *;
	@property --myColor1 {
		syntax: '<color>';
		initial-value: $red;
		inherits: false;
	}

	@property --myColor2 {
		syntax: '<color>';
		initial-value: $orange;
		inherits: false;
	}
	button {
		background: linear-gradient(to right, var(--myColor1), var(--myColor2));
		transition:
			--myColor1 1s,
			--myColor2 1s,
			all 0.4s;
		color: $black;
		border-radius: $rdBig $rdLit $rdBig $rdLit;
		border: none;
		font-family: bold;
		box-shadow: 8px 8px 8px #000;
		&:hover {
			transform: translateY(-10%);
			--myColor1: #9ccfd8;
			--myColor2: #c4a7e7;
		}
		a {
			color: $black;
			font-size: $fnBig;
		}
	}
</style>
