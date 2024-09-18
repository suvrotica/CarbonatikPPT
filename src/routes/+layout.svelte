<script lang="ts">
	import { onMount } from 'svelte';
	// Import Reveal.js CSS
	import 'reveal.js/dist/reveal.css';
	import 'reveal.js/dist/theme/league.css';
	import 'reveal.js/plugin/highlight/monokai.css';

	import '@picocss/pico';
	let fontLoaded = false;

	let fontLink;

	// Import Reveal.js and its plugins
	import Reveal from 'reveal.js';
	import Highlight from 'reveal.js/plugin/highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';
	import Markdown from 'reveal.js/plugin/markdown/markdown';

	// Initialize Reveal.js on component mount
	onMount(() => {
		fontLink = document.createElement('link');
		fontLink.href =
			'https://fonts.googleapis.com/css2?family=Gaegu:wght@300;400;700&family=Poppins:ital,wght@0,100;1,100&family=Montserrat:wght@300&family=Amatic+SC:wght@400;700&display=swap';
		fontLink.rel = 'stylesheet';
		fontLoaded = true;
		document.head.appendChild(fontLink);
		Reveal.initialize({
			plugins: [Highlight, Notes, Markdown],
			transition: 'slide', // Transition style
			slideNumber: 'c/t', // Show current slide number
			controls: true, // Show navigation controls
			progress: true, // Show progress bar
			hash: true, // Enable URL hash
			overview: true, // Enable overview mode
			center: true, // Center slides vertically
			// disableLayout: true,
			//width: '100%',
			//height: '100%',
			margin: 0.5,
			minScale: 0.5,
			maxScale: 1.5
		});
	});
</script>

<svelte:head>
	<!-- <link rel="stylesheet" href="/node_modules/reveal.js/dist/reveal.css" /> -->
	<!-- <link rel="stylesheet" href="/node_modules/reveal.js/dist/theme/league.css" /> -->
</svelte:head>

<slot />

<slot />

<style>
	/* Your custom CSS will go here */
</style>
