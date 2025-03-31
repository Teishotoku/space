<script lang="ts">
	import Video from 'video/vaporeimu.mp4';
	import Profile from 'img/alice.jpg';
	import PrimaryButton from '../../elements/buttons/primaryButton.svelte';
</script>

<section>
	<div class="text">
		<img src={Profile} alt="" />
		<div class="head">
			<h1>Welcome to</h1>
			<h1>Teishotoku.info</h1>
		</div>
		<PrimaryButton cls="dashBtn" txt="my projects" />
	</div>
	<div class="video">
		<div class="layer"></div>
		<video src={Video} loop autoplay> </video>
	</div>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		width: 100vw;
		height: 90vh;
		@include between;
	}
	.text {
		@include columnStart;
		width: 30%;
		height: 100%;
		padding-left: 5%;
		img {
			height: 25%;
			border-radius: 100%;
		}
	}
	.head {
		@include columnStart;
		h1 {
			font-size: $fnDash;
			background: linear-gradient(to right, $red, $orange);
			-webkit-text-fill-color: transparent;
			-webkit-background-clip: text;
		}
	}
	.video {
		overflow: hidden;
		width: 70%;
		height: 100%;
		video {
			height: 100%;
			width: 110%;
		}
	}
	.layer {
		width: 50%;
		height: 100%;
		position: absolute;
		background: linear-gradient(to right, $black 10%, transparent);
	}
	:global(.dashBtn) {
		width: 70%;
		height: 10%;
		font-size: $fnBig;
	}
</style>
