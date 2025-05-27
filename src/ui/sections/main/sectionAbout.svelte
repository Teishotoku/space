<script lang="ts">
	import NamingBlock from 'blocks/namingBlock.svelte';
	import Rust from 'icon/rust.png';
	import Haskell from 'icon/haskell.png';
</script>

<section>
	<NamingBlock txt="about me" />
	<div class="content">
		<article>
			<span><p>Hi.</p></span>
			<p>
				I can be called a mix of web <span>developer</span> and <span>devops.</span> I try to develop
				in both directions, although in fact it comes out spontaneously, just out of interest in different
				technologies in these areas.
			</p>
			<p>
				My journey began with the introduction of <span>unix-like systems</span>, which served as a
				funnel into the it sphere. Starting from the canonical, red hat, and gentoo distributions, I
				learned how to interact and manage my operating system.
			</p>
			<p>
				I find it interesting to automate all kinds of things, and I enjoy system administration. I
				try to spend my free time watching works of art like movies, paintings, and music.
			</p>
		</article>
		<div class="bright">
			<h1>my interest</h1>
			<img src={Rust} alt="" />
			<img src={Haskell} alt="" />
		</div>
	</div>
</section>

<style lang="scss">
	@use 'scss' as *;
	section {
		background: linear-gradient(150deg, $black 20%, $dim 100%);
		@include columnEvenly;
		@include section;
	}
	.content {
		@include between;
		width: 100%;
		height: 100%;
	}
	span {
		color: $red;
	}
	.bright {
		color: $black;
		@include columnEvenly;
		width: 30%;
		height: 100%;
		background: linear-gradient(to right, $red, $orange);
		border-radius: $rdBig 0 0 $rdBig;
		box-shadow: -4px 2px 8px #000;
		img {
			height: 20%;
			transition: all 0.5s;
			-webkit-filter: drop-shadow(5px 5px 5px $black);
			filter: drop-shadow(5px 5px 5px $black);
			&:hover {
				height: 35%;
				filter: drop-shadow(8px 8px 8px $black);
			}
		}
	}
	article {
		@include columnStart;
		margin-left: 5%;
		width: 60%;
		height: 80%;
		p {
			font-size: $fnReg;
		}
	}
</style>
