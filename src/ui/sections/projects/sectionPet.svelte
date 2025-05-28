<script lang="ts">
	import PrimaryButton from 'buttons/primaryButton.svelte';
	import Fastapi from 'img/logo/fastapi.svg';
	import Mongo from 'img/logo/mongodb.png';
	import Solidjs from 'img/logo/solidjs.png';
	import Tailwind from 'img/logo/tailwind.svg';
	import Typescript from 'img/logo/typescript.svg';
</script>

<section>
	<h1>projects page</h1>
	<div class="pet">
		<div class="dark">
			<div class="left">
				<h1>Best Shop</h1>
				<PrimaryButton txt="on site" cls="btnPet1" href="https://pet1.teisho.space" />
			</div>
			<div class="right">
				<div class="stack">
					<h2>stack</h2>
					<div class="logos">
						<img src={Fastapi} alt="" />
						<img src={Mongo} alt="" />
						<img src={Solidjs} alt="" />
						<img src={Tailwind} alt="" />
						<img src={Typescript} alt="" />
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include columnEvenly;
		width: 100vw;
		height: 120vh;
	}
	.pet {
		@include imgback('img/1pet.png');
		background-size: cover;
		width: 90%;
		height: 80%;
		border-radius: $rdMed;
		border-bottom: 4px solid $orange;
	}
	.dark {
		@include full;
		@include evenly;
		background: linear-gradient(to bottom, #00000000 10%, $black 100%);
		overflow: hidden;
	}
	.left {
		@include columnStart;
		padding-left: 5%;
		height: 70%;
		width: 30%;
		color: $orange;
		text-shadow: 2px 2px 4px $black;
	}
	.right {
		@include evenly;
		align-items: flex-end;
		width: 70%;
		height: 100%;
	}
	.stack {
		@include evenly;
		width: 100%;
		height: 20%;
		font-size: $fnBig;
		color: $orange;
	}
	.logos {
		@include evenly;
		width: 70%;
		height: 80%;
		img {
			height: 50%;
		}
	}
	:global(.btnPet1) {
		padding: 5% 10%;
	}
	@media only screen and (max-width: 1375px) {
		.dark {
			@include columnEvenly;
		}
		.left {
			@include columnEvenly;
			height: 40%;
			width: 50%;
			padding-left: 0;
		}
		.right {
			height: 40%;
			width: 90%;
		}
		.stack {
			@include columnEvenly;
			height: 80%;
			h2 {
				font-size: $fnDash;
			}
		}
		.logos {
			width: 100%;
			height: 70%;
		}
	}
	@media only screen and (max-width: 1000px) {
		.left {
			width: 100%;
		}
		.logos {
			img {
				height: 70%;
			}
			display: grid;
			grid-template-rows: repeat(2, 1fr);
			grid-template-columns: repeat(3, 20%);
			grid-row: 2 2 / 6;
		}
	}
</style>
