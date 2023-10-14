<script lang="ts">
	import { onMount } from 'svelte';
	import Reveal from 'reveal.js';
	import Markdown from 'reveal.js/plugin/markdown/markdown';
	import Highlight from 'reveal.js/plugin/highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';

	import 'reveal.js/dist/reveal.css';
	import 'reveal.js/dist/theme/black.css';
	import 'reveal.js/plugin/highlight/monokai.css';
	let deck;
	onMount(() => {
		const deck = new Reveal({
			plugins: [Markdown, Highlight, Notes],
			autoAnimateEasing: 'ease',
			autoAnimateDuration: 1,
			hash: true,
			controls: false,
			progress: false
		});

		deck.initialize();
	});

	let today = new Date();
	let options: Intl.DateTimeFormatOptions = {
		weekday: 'long',
		month: 'short',
		day: '2-digit',
		year: 'numeric'
	};
	let dateString = today.toLocaleDateString('en-US', options);
</script>
<div class="reveal">
	<article class="slides">
		<section>
			<h1>Health Information Exchange</h1>
			<h2>An Implementation Overview</h2>
			<h3>Suvro Ghosh</h3>
			<h4>Date {dateString} </h4>
		</section>
<section>
	<h2>Introduction to HIE</h2>
	<ul>
		<li>Understanding Health Information Exchange (HIE)</li>
		<li>Significance of HIE in Healthcare</li>
	</ul>
</section>

		<!-- ...other slides... -->

	</article>
</div>

