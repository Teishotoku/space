<script lang="ts">
	import { page } from '$app/state';
</script>

<div class="links">
	<a href="/" class={page.url.pathname === '/' ? 'active' : 'static'}
		>main
		<hr />
	</a>
	<a href="/projects" class={page.url.pathname === '/projects' ? 'active' : 'static'}
		>projects
		<hr />
	</a>
	<a href="/system" class={page.url.pathname === '/system' ? 'active' : 'static'}
		>system
		<hr />
	</a>
	<a href="/blog " class={page.url.pathname === '/blog' ? 'active' : 'static'}
		>blog
		<hr />
	</a>
</div>

<style lang="scss">
	@use 'scss' as *;
	.links {
		@include between;
		margin: 0% 5%;
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
