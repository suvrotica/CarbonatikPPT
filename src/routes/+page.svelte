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
<section>
    <header>
        <h2>Open Source Solutions</h2>
    </header>
    <article>
        <h3>Introduction to OpenHIE</h3>
        <p>OpenHIE, or Open Health Information Exchange, is an initiative that helps guide countries in developing HIEs to improve healthcare delivery. It’s essentially a framework rather than a software, which countries can use to create a suitable HIE based on their unique needs.</p>
    </article>
    <article>
        <h3>Advantages of Open Source in HIE</h3>
        <ul>
            <li>Cost-Effectiveness: Lower upfront costs compared to proprietary solutions.</li>
            <li>Flexibility and Customizability: Can be tailored to meet specific needs and requirements.</li>
            <li>Community Support: Backed by a community of developers for support and continuous improvement.</li>
            <li>Transparency: Open standards and codes ensure transparency and interoperability.</li>
        </ul>
    </article>
</section>

		

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
    font-size:20px; 
  }

  .slides section ul {
    margin-bottom: 20px;
  }

  .slides section ul li {
font-size: 1.5em; 
    margin-bottom: 10px;
    list-style-type: disc;
    margin-left: 20px;
  }

  .capitalize {
    text-transform: capitalize;
  }
</style>
