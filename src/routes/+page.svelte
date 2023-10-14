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

<style>
    
    p {
        font-family: 'Poppins', sans-serif;
    }
    h1, h2 {
        font-family: 'Poppins', sans-serif;
    }
</style>

<div class="reveal">
    <div class="slides">
        <section data-markdown>
<script type="text/template">
  
                
                ## Achieving Health Information Exchange (HIE) with Open Source Solutions
                ### An In-depth Analysis
                **Presenter’s Name**  
                **Date** {dateString} 
                ---
                ## Understanding Health Information Exchange (HIE)
                - Definition of Health Information Exchange (HIE)
                - Significance of HIE in modern healthcare
                ---
                ## Open Source Solutions: Introduction to OpenHIE
                - Unveiling OpenHIE as an open-source platform for HIE
                - Advantages of utilizing open source solutions in HIE
                </script>
  </textarea>
        </section>


    </div>
</div>
