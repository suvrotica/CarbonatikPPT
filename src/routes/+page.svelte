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
			<h2>Tools & Resources</h2>
			<ul>
				<li>Digital Square TCO Tool</li>
				<li>Instant OpenHIE</li>
				<li>WHO DIIG</li>
				<!-- ... other items -->
			</ul>
			<aside class="notes">
				<p>Explanation of each tool and how it contributes to the OpenHIE framework.</p>
			</aside>
		</section>
		<section>
			<h2>Framework Foundation</h2>
			<p>Standards and best practices form a comprehensive HIE system foundation.</p>
			<aside class="notes">
				<p>Detailed explanation of how standards and best practices are utilized in OpenHIE.</p>
			</aside>
		</section>
		<section>
			<h2>Key Attributes</h2>
			<ul>
				<li>Standards-Based: Best practices and international standards adoption.</li>
				<li>Implementable: Provides foundational patterns for complex systems.</li>
				<li>Modular: Tailored solutions for community needs.</li>
			</ul>
			<aside class="notes">
				<p>Detailed discussion on each attribute and its significance.</p>
			</aside>
		</section>
		<section>
			<h2>The Architecture</h2>
			<p>OpenHIE architecture facilitates unified health data sharing across systems.</p>
			<aside class="notes">
				<p>Explanation of how OpenHIE architecture normalizes health information context, integrates medical supply data, and enhances decision-making.</p>
			</aside>
		</section>
	</article>



</main>

<style>

main {

-family: 'Poppins', sans-serif;
    
} 
    .reveal section h1, .reveal section h2, .reveal section h3 {
        font-size: 1.5rem;
    }

    .reveal section p, .reveal section li {

        font-size: 2rem;
        margin-bottom: 5px;
    }

    .reveal section ul {
        padding-left: 5px;
    }

    .reveal section article {
        margin-bottom: 5px;
    }

    .reveal section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        height: 100%;
        padding: 5px;
    }
</style>

