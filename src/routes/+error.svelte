<script lang="ts">
</script>

<section>
	<div class="errorBlock">
		<h1>Страница</h1>
		<h1>не найдена</h1>
	</div>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include center;
		width: 100vw;
		height: 60vh;
	}
	.errorBlock {
		@include start;
		@include imgback('img/404.png');
		width: 90%;
		height: 90%;
		color: $white;
	}
</style>
