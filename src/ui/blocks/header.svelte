<script lang="ts">
	import { page } from '$app/state';
	import Fumo from 'icon/fumo.png';
	import LinksBlock from './linksBlock.svelte';
	let props = $props<string>();
</script>

<header>
	<div class="left">
		<img src={Fumo} alt="" />
		<h1>Teishotoku</h1>
	</div>
	<LinksBlock />
</header>

<style lang="scss">
	@use 'scss' as *;
	header {
		background-color: $blackLight;
		width: 100vw;
		height: 10vh;
		border-radius: 0 0 $rdMed $rdMed;
		@include between;
		z-index: 50;
	}
	.left {
		@include start;
		margin-left: 5%;
		width: 20%;
		height: 100%;
		font-family: 'italic';
		h1 {
			font-size: $fnDash;
			background: linear-gradient(to right, $red, $orange);
			-webkit-text-fill-color: transparent;
			-webkit-background-clip: text;
		}
		img {
			height: 60%;
			margin-right: 5%;
		}
	}
	.right {
		@include between;
		margin-right: 5%;
		width: 25%;
		a {
			font-size: $fnMed;
		}
		a {
			display: block;
			text-shadow: 1px 1px 4px $red;
			font-size: $fnReg;
			margin-right: 5%;
			transition: all 0.4s;
			&:hover {
				transform: translateY(-10%);
				hr {
					width: 100%;
					background: $red;
				}
			}
			hr {
				@include brdr;
				transition: all ease 0.4s;
				width: 0px;
				height: 4px;
				background: transparent;
				color: transparent;
			}
		}
		.active {
			color: $purple;
			hr {
				width: 100%;
				background: $purple;
			}
		}
	}
</style>
