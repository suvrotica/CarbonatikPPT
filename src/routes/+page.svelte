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
        deck = new Reveal({
            plugins: [Markdown, Highlight, Notes],
            autoAnimateEasing: 'ease',
            autoAnimateDuration: 1,
            hash: true,
            controls: true,
            progress: false,
        markdown: {
            smartypants: true
        }
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


<main class="reveal">
	<article class="slides">
		<section>
<header>
			<h1>Achieving Health Information Exchange (HIE) with Open Source Solutions</h1>
			<h2>An In-depth Analysis</h2>
</header>
			<p>Suvro Ghosh</p>
			<p>Date: </p>{dateString} 
		</section>

	<section>
<header>
	<h2>Introduction to HIE</h2>
</header>
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
</main>
