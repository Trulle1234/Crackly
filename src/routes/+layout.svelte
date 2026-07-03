<script lang="ts">
	import favicon from '$lib/assets/favicon.png';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link rel="stylesheet" href="src/app.css"/>
	<title>Crackly</title>
</svelte:head>

{@render children()}
