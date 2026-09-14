<!-- src/routes/+layout.svelte -->
<script>
	let { childen } = $props()
</script>

<svelte:head>
	<title>Ajou Mini Portfolio</title>
	<meta name="description" content="SvelteKit + Vercel mini portfolio" />
</svelte:heade>

<nav>
	<a href="/">Home</a>
	<a href="/about"About</a>
	<a hreg="/projects">Projects</a>
</nav>

<main>
	{@render children()}
</main>

<style>
	@import '../app.css';
</style>