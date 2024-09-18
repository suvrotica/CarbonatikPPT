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

<main class="reveal">
    <article class="slides">
        <section>
            <header>
                <h1>Non-Response in Indian Surveys: Challenges and Solutions</h1>
            </header>
            <h2>Focusing on Affluent Demographics</h2>
            <p>Date: {dateString}</p>
        </section>

        <section>
            <header>
                <h2>1. Introduction</h2>
            </header>
            <ul>
                <li><strong>National Sample Surveys in India</strong>
                    <ul>
                        <li>Conducted by organizations like <strong>NSSO</strong></li>
                        <li><em>Crucial for socio-economic data collection</em></li>
                    </ul>
                </li>
                <li><strong>Importance for Policy Making</strong>
                    <ul>
                        <li>Informs government policies on <strong>poverty alleviation</strong>, <strong>employment</strong>, <strong>healthcare</strong></li>
                        <li>Guides <strong>resource allocation</strong> and program evaluation</li>
                    </ul>
                </li>
            </ul>
        </section>

        <section>
            <section>
                <header>
                    <h2>2. The Non-Response Problem</h2>
                </header>
<img src="napkin-selection (4).png"/>
                <ul>
                    <li><strong>Definition</strong>: <em>Non-response</em> occurs when selected participants do not provide information.</li>
                    <li><strong>Significance</strong>:
                        <ul>
                            <li>Leads to <strong>bias</strong> in data</li>
                            <li>Affects <strong>accuracy</strong> and <strong>reliability</strong></li>
                        </ul>
                    </li>
                    <li><strong>Current Trends</strong>:
                        <ul>
                            <li><strong>Increasing non-response rates</strong> over the past decade</li>
                            <li>Particularly in <strong>urban areas</strong> and among <strong>high-income groups</strong></li>
                        </ul>
                    </li>
                    <li><strong>Impact on Data</strong>:
                        <ul>
                            <li>Underrepresentation of affluent groups</li>
                            <li>Skewed socio-economic indicators</li>
                        </ul>
                    </li>
                </ul>
                <aside class="notes">Insert a line graph showing the trend of non-response rates over the past decade, highlighting the increase in urban and affluent areas.</aside>
            </section>
        </section>

        <section>
            <header>
                <h2>3. Focus on Affluent Groups</h2>
            </header>
            <ul>
                <li><strong>Specific Challenges</strong>:
                    <ul>
                        <li><strong>Restricted Access</strong> to gated communities</li>
                        <li><strong>Gatekeepers</strong> preventing surveyors' entry</li>
                        <li><strong>Lower Visibility</strong> of residents in high-rise apartments</li>
                    </ul>
                </li>
                <li><strong>Data on Non-Response Rates</strong>:
                    <ul>
                        <li>Non-response rates up to <strong>20% higher</strong> in high-income neighborhoods</li>
                        <li><strong>Case Study</strong>: Bengaluru survey showed <strong>15% lower</strong> response in gated communities</li>
                    </ul>
                </li>
                <li><strong>Comparison with Other Groups</strong>:
                    <ul>
                        <li><strong>Urban affluent vs. rural populations</strong>: Higher non-response in urban affluent areas</li>
                        <li>Despite higher education levels, response rates are <strong>lower</strong> among the affluent</li>
                    </ul>
                </li>
            </ul>
            <aside class="notes">Include a bar chart comparing non-response rates across different socio-economic strata.</aside>
        </section>

        <section>
            <header>
                <h2>4. Causes of Non-Response</h2>
            </header>
            <ul>
                <li><strong>Privacy Concerns</strong>:
                    <ul>
                        <li>Fear of <strong>data misuse</strong> or breaches</li>
                    </ul>
                </li>
                <li><strong>Time Constraints</strong>:
                    <ul>
                        <li>Busy lifestyles with <strong>limited availability</strong></li>
                    </ul>
                </li>
                <li><strong>Lack of Perceived Benefit</strong>:
                    <ul>
                        <li>Belief that surveys do not <strong>directly benefit</strong> them</li>
                    </ul>
                </li>
                <li><strong>Other Factors</strong>:
                    <ul>
                        <li><strong>Distrust in Institutions</strong></li>
                        <li>Increasing <strong>individualism</strong> and focus on personal privacy</li>
                    </ul>
                </li>
            </ul>
            <p><strong>Expert Opinion</strong>:</p>
            <ul>
                <li>Sociologists attribute non-response to <strong>increased individualism</strong></li>
            </ul>
        </section>

        <section>
            <header>
                <h2>5. Implications</h2>
            </header>
            <ul>
                <li><strong>Effect on Survey Results</strong>:
                    <ul>
                        <li><strong>Bias</strong> due to underrepresentation of affluent groups</li>
                        <li>Inaccurate estimates of <strong>income distribution</strong> and <strong>consumption patterns</strong></li>
                    </ul>
                </li>
                <li><strong>Potential Policy Distortions</strong>:
                    <ul>
                        <li>Policies may not address the needs of <strong>non-responding groups</strong></li>
                    </ul>
                </li>
                <li><strong>Economic and Social Impact</strong>:
                    <ul>
                        <li><strong>Misallocation of resources</strong></li>
                        <li>Ineffective <strong>development programs</strong></li>
                    </ul>
                </li>
            </ul>
            <blockquote>
                <p>"Non-response bias can significantly distort our understanding of socio-economic conditions, leading to policies that fail to address actual needs."</p>
                <footer>Expert in Survey Methodology</footer>
            </blockquote>
        </section>

        <section>
            <header>
                <h2>6. International Perspective</h2>
            </header>
            <ul>
                <li><strong>Best Practices from Other Countries</strong>:
                    <ul>
                        <li><strong>Advance Letters</strong> to inform residents about upcoming surveys</li>
                        <li>Providing <strong>incentives</strong> for participation</li>
                        <li><strong>Multiple Contact Methods</strong>: Mail, phone, online</li>
                        <li><strong>Cultural Sensitivity Training</strong> for surveyors</li>
                    </ul>
                </li>
                <li><strong>Comparative Analysis</strong>:
                    <ul>
                        <li>Similar challenges in countries like the <strong>USA</strong> and <strong>UK</strong></li>
                        <li>Successful strategies implemented to improve response rates</li>
                    </ul>
                </li>
            </ul>
            <p><strong>Case Study</strong>: The <strong>US Census Bureau</strong> improved response rates through online surveys and targeted communication.</p>
        </section>

        <section>
            <header>
                <h2>7. Proposed Strategies</h2>
            </header>
            <ul>
                <li><strong>Building Trust Through Education</strong>:
                    <ul>
                        <li><strong>Transparency</strong> about survey purpose and benefits</li>
                        <li>Emphasize <strong>privacy protection</strong> measures</li>
                    </ul>
                </li>
                <li><strong>Technological Solutions for Convenience</strong>:
                    <ul>
                        <li><strong>Online Surveys</strong> accessible via secure links</li>
                        <li><strong>Mobile Apps</strong> for easy participation</li>
                    </ul>
                </li>
                <li><strong>Tailored Approaches for Affluent Respondents</strong>:
                    <ul>
                        <li><strong>Flexible Scheduling</strong> options</li>
                        <li><strong>Customized Communication</strong> with personalized messages</li>
                    </ul>
                </li>
                <li><strong>Ethical Considerations</strong>:
                    <ul>
                        <li>Ensure <strong>voluntary participation</strong> and <strong>consent</strong></li>
                        <li>Maintain <strong>confidentiality</strong> and respect for <strong>autonomy</strong></li>
                    </ul>
                </li>
            </ul>
        </section>

        <section>
            <header>
                <h2>8. Methodological Adjustments</h2>
            </header>
            <ul>
                <li><strong>Statistical Techniques</strong>:
                    <ul>
                        <li><strong>Weighting Adjustments</strong> to account for underrepresented groups</li>
                        <li><strong>Imputation Methods</strong> for estimating missing data</li>
                    </ul>
                </li>
                <li><strong>Innovative Sampling Methods</strong>:
                    <ul>
                        <li><strong>Mixed-Mode Surveys</strong> combining online, phone, and face-to-face methods</li>
                        <li><strong>Follow-Up Surveys</strong> targeting initial non-respondents</li>
                    </ul>
                </li>
            </ul>
        </section>

        <section>
            <header>
                <h2>9. Recommendations</h2>
            </header>
            <ul>
                <li><strong>For Policy Makers</strong>:
                    <ul>
                        <li><strong>Enhance Engagement Efforts</strong> with affluent communities</li>
                        <li>Launch <strong>public awareness campaigns</strong> on survey importance</li>
                    </ul>
                </li>
                <li><strong>For Survey Organizations</strong>:
                    <ul>
                        <li><strong>Improve Accessibility</strong> via technological platforms</li>
                        <li><strong>Invest in Training</strong> for staff on communication skills</li>
                    </ul>
                </li>
                <li><strong>For Future Research</strong>:
                    <ul>
                        <li><strong>Monitor and Evaluate</strong> the effectiveness of strategies</li>
                        <li>Establish <strong>feedback mechanisms</strong> for continuous improvement</li>
                    </ul>
                </li>
            </ul>
        </section>

        <section>
            <header>
                <h2>10. Conclusion</h2>
            </header>
            <ul>
                <li><strong>Summary of Key Points</strong>:
                    <ul>
                        <li>Non-response among affluent groups is a significant issue impacting data quality</li>
                        <li>A <strong>multifaceted approach</strong> is required to address this challenge</li>
                    </ul>
                </li>
                <li><strong>Call to Action</strong>:
                    <ul>
                        <li><strong>Implement proposed strategies</strong> to improve participation</li>
                        <li>Ensure <strong>representative data</strong> for effective policy making</li>
                    </ul>
                </li>
            </ul>
        </section>

        <section>
            <p><em>This presentation highlights the challenges of non-response in Indian surveys, particularly among affluent demographics, and proposes comprehensive strategies to address the issue.</em></p>
            <p><em>Prepared for stakeholders in survey and policy-making fields to foster understanding and prompt action on improving survey participation among affluent groups in India.</em></p>
        </section>
    </article>
</main>


<style>
main, header {
    overflow: hidden;
  
    padding: 20px;
  
font-family: 'Poppins', sans-serif;
margin :10px;
    
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

