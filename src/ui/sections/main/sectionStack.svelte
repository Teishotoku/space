<script lang="ts">
	import NamingBlock from 'blocks/namingBlock.svelte';
	import Tailwind from 'img/logo/tailwind.svg';
	import Nest from 'img/logo/nest.svg';
	import Fastapi from 'img/logo/fastapi.svg';
	import Docker from 'img/logo/docker.svg';
	import Laravel from 'img/logo/laravel.svg';
	import Node from 'img/logo/nodejs.svg';
</script>

<section>
	<div class="content">
		<NamingBlock txt="stack" />
		<div class="left">
			<code lang="javascript">let a = 5</code>
		</div>
	</div>
	<div class="right">
		<div class="line">
			<img src={Tailwind} alt="" />
			<img src={Nest} alt="" />
			<img src={Fastapi} alt="" />
			<img src={Docker} alt="" />
			<img src={Laravel} alt="" />
			<img src={Node} alt="" />
		</div>
		<hr />
	</div>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		@include section;
		@include between;
		background: linear-gradient(330deg, $black 35%, $dim 100%);
	}
	.content {
		@include columnEvenly;
		width: 65%;
		height: 100%;
	}
	.left {
		width: 90%;
		height: 80%;
		margin-left: 2%;
		background: $dim;
		border: 4px solid $red;
	}
	.right {
		@include column;
		width: 30%;
		height: 100%;
		hr {
			width: 100%;
			height: 16px;
			color: $red;
			background: $red;
			border-radius: $rdLit 0 0 $rdBig;
		}
	}
	.line {
		@include columnEvenly;
		background-color: $black;
		position: relative;
		overflow: auto;
		width: 40%;
		height: 100%;
		border-inline: 2px solid $prim;
		img {
			width: 50%;
			aspect-ratio: 1 / 1;
			transition: all 0.5s;
			-webkit-filter: drop-shadow(5px 5px 5px #00000000);
			filter: drop-shadow(5px 5px 5px #00000000);
			&:hover {
				width: 80%;
				filter: drop-shadow(8px 8px 8px $orange);
			}
		}
	}
</style>
