<script lang="ts">
	import '@skeletonlabs/skeleton/themes/theme-crimson.css';
	import '@skeletonlabs/skeleton/styles/all.css';
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import { IconUserCircle } from '@tabler/icons-svelte';
	import Footer from '$lib/components/Footer.svelte';
	import { LightSwitch } from '@skeletonlabs/skeleton';

	let navTrails = [
		{
			href: '/',
			str: 'Home'
		},
		{
			href: '/projects',
			str: 'Projects'
		},
		{
			href: '/about',
			str: 'About'
		}
	];
</script>

<AppShell slotPageHeader="">
	<svelte:fragment slot="header">
		<AppBar>
			<svelte:fragment slot="lead">
				<a href="/">
					<IconUserCircle />
				</a>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<ul class="flex flex-row gap-4">
					{#each navTrails as {href, str}}
						<li>
							<a href={href}>{str}</a>
						</li>
					{/each}
					<li>
						<LightSwitch />
					</li>
				</ul>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<slot />
	<svelte:fragment slot="pageFooter">
		<Footer />
	</svelte:fragment>
</AppShell>
