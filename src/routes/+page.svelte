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
slideNumber: "c/t",
disableLayout: true,
            hash: true,
            controls: true,
            progress: true,
transition: 'fade', 
controlsLayout: 'center',
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


<div class="reveal">
	
	<article class="slides">
		<section>
            <h1>Achieving Health Information Exchange (HIE) with Open Source Solutions</h1>
            <h2>An In-depth Analysis</h2>
            <p>Suvro Ghosh</p>
            <p>Date: {dateString}</p>
        </section>

        <section>
            <h2>Introduction to HIE</h2>
            <ul>
                <li>Understanding Health Information Exchange (HIE)</li>
                <li>Significance of HIE in Healthcare</li>
            </ul>
        </section>
		
		
<section>
<section>
<header>
                <h2>Open Source Solutions</h2>
            </header>
            <article>
                <h3>Introduction to OpenHIE</h3>
                <p>OpenHIE, or Open Health Information Exchange, is an initiative that helps guide countries in developing HIEs to improve healthcare delivery. It’s essentially a framework rather than a software, which countries can use to create a suitable HIE based on their unique needs.</p>
            </article>
</section>
<section>
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
            
            
        </section>
	</article>



</div>

<style>

main {

-family: 'Poppins', sans-serif;
    
} 
    .reveal section h1, .reveal section h2, .reveal section h3 {
        font-size:1rem;
    }

    .reveal section p, .reveal section li {
font-size:1rem;
        
        margin: 5px;
    }

    .reveal section ul {
        padding-left: 5px;
    }

    .reveal section article {
font-size:1rem;
        margin: 5px;
    }

    .reveal section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        height: 100%;
        padding: 5px;
    }
.reveal .controls {
    right: 30%;}
</style>

