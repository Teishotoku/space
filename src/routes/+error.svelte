<script lang="ts">
</script>

<section>
	<div class="errorBlock">
		<div class="text">
			<h1>Page</h1>
			<h1>not found</h1>
		</div>
		<h1 class="textPrim">404</h1>
	</div>
	<div class="hidden">
		<div class="layer"></div>
		<div class="img"></div>
	</div>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include center;
		width: 100vw;
		height: 90vh;
	}
	.errorBlock {
		@include columnStart;
		width: 30%;
		height: 60%;
		color: $white;
		h1 {
			padding-left: 10%;
		}
	}
	.img {
		@include imgback('img/404.jpg');
		width: 100%;
		height: 100%;
	}
	.text {
		width: 100%;
		height: 100%;
	}
	.textPrim {
		font-size: 10vw;
		background: linear-gradient(to right, $red, $orange);
		-webkit-text-fill-color: transparent;
		-webkit-background-clip: text;
	}
	.hidden {
		width: 70%;
		height: 100%;
		overflow: hidden;
	}
	.layer {
		width: 50%;
		height: 90%;
		position: absolute;
		background: linear-gradient(to right, $black 10%, transparent);
	}
</style>
