<script lang="ts">
	import NamingBlock from 'blocks/namingBlock.svelte';
	import SectionPets from 'sections/projects/sectionPets.svelte';
	import Fastapi from 'img/logo/fastapi.svg';
	import Mongo from 'img/logo/mongodb.png';
	import Solidjs from 'img/logo/solidjs.png';
	import Tailwind from 'img/logo/tailwind.svg';
	import Typescript from 'img/logo/typescript.svg';
	import Express from 'img/logo/nodejs.svg';
	import Postgres from 'img/logo/postgres.png';
	import React from 'img/logo/react.png';
	import Docker from 'img/logo/docker.svg';
	import Laravel from 'img/logo/laravel.svg';
	import Mysql from 'img/logo/mysql.png';
	import Svelte from 'img/logo/svelte.svg';
	import Sass from 'img/logo/sass.svg';
</script>

<svelte:head>
	<title>Projects</title>
</svelte:head>

<div class="head">
	<div>
		<NamingBlock txt="Projects Page" />
	</div>
</div>
<SectionPets
	head="Best Shop"
	domain="pet1.teisho.space"
	img="1pet.png"
	back={Fastapi}
	base={Mongo}
	front={Solidjs}
	style={Tailwind}
	other={Typescript}
/>
<SectionPets
	head="FindTrend"
	domain="pet2.teisho.space"
	img="2pet.png"
	back={Express}
	base={Postgres}
	front={React}
	style={Tailwind}
	other={Docker}
/>
<SectionPets
	head="Kugoo"
	domain="pet3.teisho.space"
	img="3pet.png"
	back={Laravel}
	base={Mysql}
	front={Svelte}
	style={Sass}
	other={Typescript}
/>

<style lang="scss">
	@use 'scss' as *;
	.head {
		@include center;
		width: 100%;
		height: 20vh;
	}
</style>
