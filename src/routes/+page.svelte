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
            plugins: [RevealMarkdown, Highlight, Notes],
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
    <div class="slides">
        <section data-markdown>
        ```
        # Achieving Health Information Exchange (HIE) with Open Source Solutions
        ### An In-depth Analysis
        **Presenter’s Name**  
        **Date**
        ```
        </section>

        <section data-markdown>
        ```
        ## Understanding Health Information Exchange (HIE)
        - Definition of Health Information Exchange (HIE)
        - Significance of HIE in modern healthcare
        ```
        </section>

        <section data-markdown>
        ```
        ## Open Source Solutions: Introduction to OpenHIE
        - Unveiling OpenHIE as an open-source platform for HIE
        - Advantages of utilizing open source solutions in HIE
        ```
        </section>
    </div>
</div>
