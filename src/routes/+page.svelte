<!-- YOU CAN DELETE EVERYTHING IN THIS PAGE -->
<script>
	import { IconBrandGithub, IconBrandLinkedin, IconBrandYoutube } from '@tabler/icons-svelte';

	let title = 'Rohi';
	let imgSRC = 'https://avatars.githubusercontent.com/u/105811202';
	let texts = {
		h1: "Hi, I'm Rohi",
		h4: 'A Web Developer based in Philippines'
	};
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<div class="container h-full mx-auto flex justify-center items-center">
	<div class="space-y-10 text-center justify-center">
		<h1 class="font-bold">{texts.h1}</h1>
		<!-- Animated Logo -->
		<section class="img-bg ml-5" />
		<img src={imgSRC} alt="shidou" class="rounded-full m-auto display-block" />
		<!-- / -->
		<div class="flex justify-center space-x-2">
			<h4 class="font-bold">{texts.h4}</h4>
		</div>

		<div class="flex justify-center">
			<a href="https://github.com/gneiru"><IconBrandGithub size={48} /></a>
			<a href="https://www.linkedin.com/in/gneiru/"><IconBrandLinkedin size={48} /></a>
			<a href="https://youtube.com/@shidou111"><IconBrandYoutube size={48} /></a>
		</div>
	</div>
</div>

<style lang="postcss">
	.img-bg {
		@apply w-60 h-60 md:w-80 md:h-80;
	}
	.img-bg {
		@apply absolute z-[-1] rounded-full blur-[50px] transition-all;
		animation: pulse 5s cubic-bezier(0, 0, 0, 0.5) infinite, glow 5s linear infinite;
	}
	@keyframes glow {
		0% {
			@apply bg-primary-400/50;
		}
		33% {
			@apply bg-secondary-400/50;
		}
		66% {
			@apply bg-tertiary-400/50;
		}
		100% {
			@apply bg-primary-400/50;
		}
	}
	@keyframes pulse {
		50% {
			transform: scale(1.5);
		}
	}
</style>
