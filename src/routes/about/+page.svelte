<script lang="ts">
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';
	import { IconBrandStackoverflow, IconBrandSvelte, IconBrandMongodb, IconAlphabetLatin} from '@tabler/icons-svelte';

	let title = 'About me';
	let AboutMe =
		"I'm a Software developer with over 1 year of development experience, experienced in open-source software development. I'm based in Philippines and currently working as Web Application Developer. I'm hooked to front-end development and intents to learn and use the latest web technologies out there, just like SvelteKit, Prisma and TypeScript. ";
	let skills = {
		programming: ['Javascript', 'Python', 'Php'],
		frameworks: ['Svelte', 'Vue.js', 'FastApi', 'Django', 'Laravel', 'Yii'],
		databases: ['MongoDB', 'MySQL', 'SQLite'],
		languages: ['English', 'Filipino']
	};
</script>

<svelte:head>
	<title>Rohi — {title}</title>
</svelte:head>

<div class="container space-y-8">
	<h1>{title}</h1>
	<p class="indent-8 text-justify">{AboutMe}</p>
	<h2>Skills</h2>

	<Accordion spacing="space-y-4">
		<AccordionItem open>
			<svelte:fragment slot="lead"><IconBrandStackoverflow /></svelte:fragment>
			<svelte:fragment slot="summary">Programming</svelte:fragment>
			<svelte:fragment slot="content">
				<ul class="list-disc px-11">
					{#each skills.programming as sk}
						<li>{sk}</li>
					{/each}
				</ul>
			</svelte:fragment>
		</AccordionItem>
		<AccordionItem>
			<svelte:fragment slot="lead"><IconBrandSvelte/></svelte:fragment>
			<svelte:fragment slot="summary">Frameworks</svelte:fragment>
			<svelte:fragment slot="content">
				<ul class="list-disc px-11">
					{#each skills.frameworks as sk}
						<li>{sk}</li>
					{/each}
				</ul>
			</svelte:fragment>
		</AccordionItem>
		<AccordionItem open>
			<svelte:fragment slot="lead"><IconBrandMongodb/></svelte:fragment>
			<svelte:fragment slot="summary">Databases</svelte:fragment>
			<svelte:fragment slot="content">
				<ul class="list-disc px-11">
					{#each skills.databases as sk}
						<li>{sk}</li>
					{/each}
				</ul>
			</svelte:fragment>
		</AccordionItem>
		<AccordionItem>
			<svelte:fragment slot="lead"><IconAlphabetLatin/></svelte:fragment>
			<svelte:fragment slot="summary">Languages</svelte:fragment>
			<svelte:fragment slot="content">
				<ul class="list-disc px-11">
					{#each skills.languages as sk}
						<li>{sk}</li>
					{/each}
				</ul>
			</svelte:fragment>
		</AccordionItem>
	</Accordion>
	
</div>

<style lang="postcss">
	.container {
		@apply mx-auto p-20 max-w-5xl space-y-4;
	}
</style>
