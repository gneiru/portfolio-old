<script>
	export const Text = "Powered by"
	export const a = {
		href: "https://kit.svelte.dev/",
		innerText: "SvelteKit"
	}
</script>
<footer>
    <p>{Text} <a href={a.href}>{a.innerText}</a></p>
</footer>

<style>
    footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}
    @media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>