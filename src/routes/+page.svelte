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
			<p>Suvro Ghosh</p>
			<p>Date {dateString} </p>
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
<style>
  .reveal {
    font-family: 'Arial', sans-serif;
  }

  .slides section {
    padding: 20px;
    background-color: #2e2e2e;
    color: #ffffff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
  }

  .slides section h1,
  .slides section h2,
  .slides section h3 {
    color: #ecf0f1;
    margin-bottom: 20px;
  }

  .slides section p {
    margin-bottom: 10px;
    line-height: 1.6;
    font-size: 1.5em; /* Increased font size */
  }

  .slides section ul {
    margin-bottom: 20px;
  }

  .slides section ul li {
    margin-bottom: 10px;
    list-style-type: disc;
    margin-left: 20px;
  }

  .capitalize {
    text-transform: capitalize;
  }
</style>
