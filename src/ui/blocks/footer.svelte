<script lang="ts">
	import LinksBlock from './linksBlock.svelte';
	import Gitlab from 'icon/git/gitlab.svg';
	import Github from 'icon/git/github.svg';
	import Forgejo from 'icon/git/forgejo.svg';
	import Codeberg from 'icon/git/codeberg.svg';
	let props = $props<string>();
</script>

<footer>
	<LinksBlock />
	<div class="right">
		<a href="https://codeberg.org/Teishotoku"><img src={Codeberg} alt="" /></a>
		<a href="https://gitlab.com/Teishotoku"><img src={Gitlab} alt="" /></a>
		<a href="https://github.com/Teishotoku"><img src={Github} alt="" /></a>
		<a href="https://git.teisho.space/Teishotoku"><img src={Forgejo} alt="" class="svg" /></a>
	</div>
</footer>

<style lang="scss">
	@use 'scss' as *;
	footer {
		width: 100vw;
		height: 20vh;
		@include between;
		z-index: 20;
	}
	.right {
		margin-right: 5%;
		width: 30%;
		height: 80%;
		@include between;
		a {
			@include center;
			height: 100%;
			img {
				height: 30%;
				transition: all 0.4s;
				&:hover {
					filter: invert(54%) sepia(27%) saturate(1088%) hue-rotate(294deg) brightness(100%)
						contrast(85%);
				}
			}
		}
	}
	.svg {
		filter: invert(1);
	}
</style>
