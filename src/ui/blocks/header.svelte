<script lang="ts">
	import { page } from '$app/state';
	import Fumo from 'icon/fumo.png';
	let props = $props<string>();
</script>

<header>
	<div class="left">
		<img src={Fumo} alt="" />
		<h1>Teishotoku</h1>
	</div>
	<div class="right">
		<a href="/" class={page.url.pathname === '/' ? 'active' : 'static'}>main</a>
		<a href="/projects" class={page.url.pathname === '/projects' ? 'active' : 'static'}>projects</a>
		<a href="/system" class={page.url.pathname === '/system' ? 'active' : 'static'}>system</a>
		<a href="/blog " class={page.url.pathname === '/blog' ? 'active' : 'static'}>blog</a>
	</div>
</header>

<style lang="scss">
	@use 'scss' as *;
	header {
		background-color: $blackLight;
		width: 100vw;
		height: 10vh;
		border-radius: 0 0 $rdMed $rdMed;
		@include between;
		z-index: 30;
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
	}
	.active {
		color: $red;
		text-decoration: underline;
	}
</style>
