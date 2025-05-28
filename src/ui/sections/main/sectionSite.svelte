<script lang="ts">
	import NamingBlock from 'blocks/namingBlock.svelte';
	import Svelte from 'img/logo/svelte.svg';
	import Ts from 'img/logo/typescript.svg';
	import Sass from 'img/logo/sass.svg';
</script>

<section>
	<NamingBlock txt="this site" />
	<div class="content">
		<div class="left">
			<hr />
			<div class="line">
				<img src={Svelte} alt="" />
				<h2>svelteKit</h2>
			</div>
			<div class="line">
				<img src={Ts} alt="" />
				<h2>typescript</h2>
			</div>
			<div class="line">
				<img src={Sass} alt="" />
				<h2>sass</h2>
			</div>
			<hr />
		</div>
		<div class="right">
			<div class="font">
				<h2>fonts</h2>
				<h2 class="victor">Victor Mono</h2>
				<h2 class="jet">JetBrains Mono</h2>
			</div>
			<div class="theme">
				<h2>colortheme: rose-pine</h2>
				<div class="colors">
					<div></div>
					<div></div>
					<div></div>
					<div></div>
					<div></div>
					<div></div>
					<div></div>
					<div></div>
				</div>
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include section;
		@include columnEvenly;
		background: linear-gradient(to bottom, $black, $dim);
	}
	.content {
		@include evenly;
		width: 90%;
		height: 90%;
	}
	.left {
		@include columnStart;
		width: 40%;
		height: 60%;
		hr {
			width: 90%;
			height: 8px;
			color: $red;
			background: $red;
			&:nth-child(1) {
				border-radius: 0 0 $rdBig 0;
			}
			&:nth-last-child(1) {
				border-radius: 0 $rdBig 0 0;
			}
		}
	}
	.right {
		@include columnStart;
		width: 40%;
		height: 60%;
	}
	.font {
		h2:nth-child(1) {
			color: $prim;
		}
	}
	.victor {
		font-family: 'italic';
	}
	.line {
		@include start;
		column-gap: 15%;
	}
	.theme {
		@include columnStart;
		height: 80%;
		width: 100%;
	}
	.colors {
		height: 70%;
		width: 100%;
		display: grid;
		grid-template-rows: repeat(2, 1fr);
		grid-template-columns: repeat(4, 1fr);
		div {
			@include brdr;
			height: 45%;
			aspect-ratio: 1 / 1;
			background-color: $dim;
			transition: all 0.4s;
			box-shadow: 4px 4px 8px #000000;
			&:hover {
				box-shadow: 4px 4px 8px $white;
				aspect-ratio: 1.7 / 1;
			}
			&:nth-child(1) {
				background-color: $red;
			}
			&:nth-child(2) {
				background-color: $yellow;
			}
			&:nth-child(3) {
				background-color: $orange;
			}
			&:nth-child(4) {
				background-color: $green;
			}
			&:nth-child(5) {
				background-color: $cyan;
			}
			&:nth-child(6) {
				background-color: $blue;
			}
			&:nth-child(7) {
				background-color: $purple;
			}
			&:nth-child(8) {
				background-color: $pink;
			}
		}
	}
	@media only screen and (max-width: 1024px) {
		.content {
			@include columnEvenly;
		}
		.left {
			@include evenly;
			flex-direction: row;
			height: 40%;
			width: 100%;
			hr {
				width: 4px;
				height: 80%;
			}
		}
		.line {
			height: 80%;
			@include columnEvenly;
		}
		.right {
			@include columnEvenly;
			height: 50%;
			width: 100%;
		}
		.font {
			@include evenly;
			height: 30%;
			width: 80%;
			h2 {
				font-size: $fnBig;
			}
		}
		.theme {
			@include columnEvenly;
			width: 100%;
		}
		.colors {
			width: 70%;
		}
	}
</style>
