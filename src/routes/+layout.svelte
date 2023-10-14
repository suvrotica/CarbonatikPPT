<script lang="ts">
	import { onMount } from 'svelte';

	import '@picocss/pico';
	let fontLoaded = false;

	let fontLink;

	onMount(() => {
		fontLink = document.createElement('link');
		fontLink.href =
			'https://fonts.googleapis.com/css2?family=Gaegu:wght@300;400;700&family=Poppins:ital,wght@0,100;1,100&family=Montserrat:wght@300&family=Amatic+SC:wght@400;700&display=swap';
		fontLink.rel = 'stylesheet';
		fontLoaded = true;
		document.head.appendChild(fontLink);
	});
</script>

<svelte:head>
	<link rel="stylesheet" href="/node_modules/reveal.js/dist/reveal.css" />
	<link rel="stylesheet" href="/node_modules/reveal.js/dist/theme/black.css" />

</svelte:head>


<slot />

