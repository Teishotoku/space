<script lang="ts">
	import NamingBlock from 'blocks/namingBlock.svelte';
	import Nixos from 'img/logo/nixos.png';
</script>

<section>
	<NamingBlock txt="System" />
	<div class="content">
		<div class="bg">
			<div class="into">
				<h1>Desktop img</h1>
			</div>
		</div>
		<div class="about">
			<img src={Nixos} alt="" class="logo" />
			<div class="txt">
				<p>
					I prefer nixos. Is imutable, declarative linux distributive. with him i can deployment
					machines with a couples command.
				</p>
			</div>
			<div class="conf">
				<h2>config and more info - coming soon.</h2>
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include section;
		@include columnEvenly;
	}
	.content {
		@include full;
		@include evenly;
	}
	.bg {
		width: 60%;
		height: 80%;
		@include imgback('img/mysystem.png');
		background-size: cover;
		background-position: center;
	}
	.into {
		@include full;
		background: linear-gradient(to bottom, #00000000, $black);
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		align-items: flex-start;
		color: $prim;
		border: 2px solid $prim;
		border-radius: 16px;
		h1 {
			padding-left: 5%;
			padding-bottom: 5%;
		}
	}
	.about {
		width: 30%;
		height: 80%;
		@include columnStart;
		p {
			font-size: $fnMed;
		}
		h2 {
			color: $prim;
		}
	}
	.logo {
		height: 30%;
		aspect-ratio: 1 / 1;
	}
	@media only screen and (max-width: 1024px) {
		.content {
			@include columnEvenly;
		}
		.bg {
			width: 90%;
		}
		.about {
			flex-direction: row;
			@include between;
			width: 90%;
		}
		.logo {
			height: 30%;
		}
		.txt {
			text-align: center;
			width: 40%;
		}
		.conf {
			text-align: center;
			width: 30%;
		}
	}
	@media only screen and (max-width: 600px) {
		.about {
			@include columnEvenly;
			overflow: hidden;
			z-index: 0;
		}
		.logo {
			display: none;
		}
	}
</style>
