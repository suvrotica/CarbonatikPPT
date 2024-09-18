<script lang="ts">
	import { onMount } from 'svelte';
	import Reveal from 'reveal.js';
	import Markdown from 'reveal.js/plugin/markdown/markdown';
	import Highlight from 'reveal.js/plugin/highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';

	import 'reveal.js/dist/reveal.css';
	import 'reveal.js/dist/theme/league.css'; 
	import 'reveal.js/plugin/highlight/monokai.css';

	let deck;
	onMount(() => {
		deck = new Reveal({
			plugins: [Markdown, Highlight, Notes],
			autoAnimateEasing: 'ease',
			autoAnimateDuration: 1,
			slideNumber: 'c/t',
			disableLayout: true,
			hash: true,
			controls: true,
			progress: true,
			transition: 'slide', // Changed transition to 'slide' for smoother effect
			controlsLayout: 'bottom-right',
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
		
            <!-- Slide 1: Title -->
            <section>
                <header>
                    <h1>Non-Response in Indian Surveys</h1>
                    <h2>Challenges, Solutions, and a Quadrant Analysis</h2>
                    <img src="Images/napkin-selection (7).png" alt="Survey Illustration" width="50%"/>
                    <p>Date: September 18, 2024</p>
                </header>
            </section>

            <!-- Slide 2: Introduction -->
            <section>
                <header>
                    <h2>1. Introduction</h2>
                </header>
                <ul>
                    <li>
                        <strong>National Sample Surveys in India</strong>:
                        <ul>
                            <li>Conducted by organizations like <strong>NSSO</strong></li>
                            <li><em>Crucial for socio-economic data collection</em></li>
                        </ul>
                    </li>
                    <li>
                        <strong>Importance for Policy Making</strong>:
                        <ul>
                            <li>Informs government policies on <strong>poverty alleviation</strong>, <strong>employment</strong>, <strong>healthcare</strong></li>
                            <li>Guides <strong>resource allocation</strong> and program evaluation</li>
                        </ul>
                    </li>
                </ul>
            </section>
            
            <!-- Slide 3: Understanding Non-Response -->
            <section>
                <header>
                    <h2>2. Understanding Non-Response</h2>
                </header>
                <img src="Images/napkin-selection (5a).png" alt="Survey Illustration" width="60%"/>
                <ul>
                    <li>
                        <strong>Definition</strong>: <em>Non-response</em> occurs when selected participants do not provide information.
                    </li>
                    <li>
                        <strong>Why It Matters</strong>:
                        <ul>
                            <li>Leads to <strong>bias</strong> in data</li>
                            <li>Affects <strong>accuracy</strong> and <strong>reliability</strong></li>
                        </ul>
                    </li>
                </ul>
                <aside class="notes">
                    Explain that non-response can skew the data, making the survey results less reliable.
                </aside>
            </section>

            <!-- Slide 4: The Non-Response Problem -->
            <section>
                <header>
                    <h2>3. The Non-Response Problem</h2>
                </header>
                <img src="Images/napkin-selection (28).png" alt="The Non-Response Problem"width="50%"/>
                <ul>
                    <li>
                        <strong>Current Trends</strong>:
                        <ul>
                            <li><strong>Increasing non-response rates</strong> over the past decade</li>
                            <li>
                                Particularly in <strong>urban areas</strong> and among <strong>high-income groups</strong>
                            </li>
                        </ul>
                    </li>
                    <li>
                        <strong>Impact on Data</strong>:
                        <ul>
                            <li>Underrepresentation of affluent groups</li>
                            <li>Skewed socio-economic indicators</li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Non-response bias can significantly distort our understanding of socio-economic conditions."
                    </p>
                    <footer>Expert in Survey Methodology</footer>
                </blockquote>
            </section>

            <!-- Slide 5: 4 Quadrant Analysis of Non-Response Factors -->
            <section>
                <header>
                    <h2>4. 4 Quadrant Analysis of Non-Response Factors</h2>
                </header>
                <img src="Images/napkin-selection (3).png" alt="4 Quadrant Analysis" width="60%"/>
                <ul>
                    <li>
                        <strong>Privacy Concerns</strong>:
                        <ul>
                            <li>Fear of <strong>data misuse</strong> or breaches</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Time Constraints</strong>:
                        <ul>
                            <li>Busy lifestyles with <strong>limited availability</strong></li>
                        </ul>
                    </li>
                    <li>
                        <strong>Lack of Perceived Benefit</strong>:
                        <ul>
                            <li>Belief that surveys do not <strong>directly benefit</strong> them</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Distrust in Institutions</strong>:
                        <ul>
                            <li>Growing <strong>individualism</strong> and focus on personal privacy</li>
                        </ul>
                    </li>
                </ul>
                <aside class="notes">
                    Discuss how each quadrant represents different reasons for non-response and their interplay.
                </aside>
            </section>

            <!-- Slide 6: Focus on Affluent Demographics -->
            <section>
                <header>
                    <h2>5. Focus on Affluent Demographics</h2>
                </header>
                <img src="Images/napkin-selection (19).png" alt="4 Quadrant Analysis" width="40%"/>
                <ul>
                    <li>
                        <strong>Specific Challenges</strong>:
                        <ul>
                            <li><strong>Restricted Access</strong> to gated communities</li>
                            <li><strong>Gatekeepers</strong> preventing surveyors' entry</li>
                            <li><strong>Lower Visibility</strong> of residents in high-rise apartments</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Data on Non-Response Rates</strong>:
                        <ul>
                            <li>Non-response rates up to <strong>20% higher</strong> in high-income neighborhoods</li>
                            <li>
                                <strong>Case Study</strong>: Bengaluru survey showed <strong>15% lower</strong> response in gated communities
                            </li>
                        </ul>
                    </li>
                    <li>
                        <strong>Comparison with Other Groups</strong>:
                        <ul>
                            <li><strong>Urban affluent vs. rural populations</strong>: Higher non-response in urban affluent areas</li>
                            <li>
                                Despite higher education levels, response rates are <strong>lower</strong> among the affluent
                            </li>
                        </ul>
                    </li>
                </ul>
                <aside class="notes">
                    Highlight how affluent groups are less likely to respond and why this is a problem.
                </aside>
            </section>

            <!-- Slide 7: Causes of Non-Response -->
            <section>
                <header>
                    <h2>6. Causes of Non-Response</h2>
                </header>
                <img src="Images/napkin-selection (26).png" alt="4 Quadrant Analysis" width="50%"/>
                <ul>
                    <li>
                        <strong>Privacy Concerns</strong>:
                        <ul>
                            <li>Fear of <strong>data misuse</strong> or breaches</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Time Constraints</strong>:
                        <ul>
                            <li>Busy lifestyles with <strong>limited availability</strong></li>
                        </ul>
                    </li>
                    <li>
                        <strong>Lack of Perceived Benefit</strong>:
                        <ul>
                            <li>Belief that surveys do not <strong>directly benefit</strong> them</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Other Factors</strong>:
                        <ul>
                            <li><strong>Distrust in Institutions</strong></li>
                            <li>Increasing <strong>individualism</strong> and focus on personal privacy</li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Building trust is essential to increasing survey participation."
                    </p>
                    <footer>Survey Strategist</footer>
                </blockquote>
            </section>

            <!-- Slide 8: Implications of Non-Response -->
            <section>
                <header>
                    <h2>7. The Funnel of Implications</h2>
                </header>
                <img src="Images/napkin-selection (31).png" alt="4 Quadrant Analysis"/>
                <ul>
                    <li>
                        <strong>Effect on Survey Results</strong>:
                        <ul>
                            <li><strong>Bias</strong> due to underrepresentation of affluent groups</li>
                            <li>
                                Inaccurate estimates of <strong>income distribution</strong> and <strong>consumption patterns</strong>
                            </li>
                        </ul>
                    </li>
                    <li>
                        <strong>Potential Policy Distortions</strong>:
                        <ul>
                            <li>Policies may not address the needs of <strong>non-responding groups</strong></li>
                        </ul>
                    </li>
                    <li>
                        <strong>Economic and Social Impact</strong>:
                        <ul>
                            <li><strong>Misallocation of resources</strong></li>
                            <li>Ineffective <strong>development programs</strong></li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Accurate surveys lead to better policies and improved lives."
                    </p>
                    <footer>Survey Expert</footer>
                </blockquote>
            </section>

            <!-- Slide 9: International Perspectives -->
            <section>
                <header>
                    <h2>8. International Perspectives</h2>
                </header>
                <img src="Images/napkin-selection (62).png" alt="4 Quadrant Analysis" width="50%"/>
                <ul>
                    <li>
                        <strong>Best Practices from Other Countries</strong>:
                        <ul>
                            <li><strong>Advance Letters</strong> to inform residents about upcoming surveys</li>
                            <li>Providing <strong>incentives</strong> for participation</li>
                            <li><strong>Multiple Contact Methods</strong>: Mail, phone, online</li>
                            <li><strong>Cultural Sensitivity Training</strong> for surveyors</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Comparative Analysis</strong>:
                        <ul>
                            <li>Similar challenges in countries like the <strong>USA</strong> and <strong>UK</strong></li>
                            <li>Successful strategies implemented to improve response rates</li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Learning from global best practices can enhance our survey methodologies."
                    </p>
                    <footer>International Researcher</footer>
                </blockquote>
            </section>

            <!-- Slide 10: Proposed Strategies -->
            <section>
                <header>
                    <h2>9. Proposed Strategies</h2>
                </header>
                <img src="Images/napkin-selection (39).png" alt="4 Quadrant Analysis"/>
                <ul>
                    <li>
                        <strong>Building Trust Through Education</strong>:
                        <ul>
                            <li><strong>Transparency</strong> about survey purpose and benefits</li>
                            <li>Emphasize <strong>privacy protection</strong> measures</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Technological Solutions for Convenience</strong>:
                        <ul>
                            <li><strong>Online Surveys</strong> accessible via secure links</li>
                            <li><strong>Mobile Apps</strong> for easy participation</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Tailored Approaches for Affluent Respondents</strong>:
                        <ul>
                            <li><strong>Flexible Scheduling</strong> options</li>
                            <li><strong>Customized Communication</strong> with personalized messages</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Ethical Considerations</strong>:
                        <ul>
                            <li>Ensure <strong>voluntary participation</strong> and <strong>consent</strong></li>
                            <li>Maintain <strong>confidentiality</strong> and respect for <strong>autonomy</strong></li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Ethical practices foster trust and enhance participation rates."
                    </p>
                    <footer>Ethics Advisor</footer>
                </blockquote>
            </section>

            <!-- Slide 11: Methodological Adjustments -->
            <section>
                <header>
                    <h2>10. Methodological Adjustments</h2>
                </header>
                <img src="Images/napkin-selection (43).png" alt="4 Quadrant Analysis"/>
                <ul>
                    <li>
                        <strong>Statistical Techniques</strong>:
                        <ul>
                            <li><strong>Weighting Adjustments</strong> to account for underrepresented groups</li>
                            <li><strong>Imputation Methods</strong> for estimating missing data</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Innovative Sampling Methods</strong>:
                        <ul>
                            <li><strong>Mixed-Mode Surveys</strong> combining online, phone, and face-to-face methods</li>
                            <li><strong>Follow-Up Surveys</strong> targeting initial non-respondents</li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Innovative methodologies can bridge the gap caused by non-response."
                    </p>
                    <footer>Data Scientist</footer>
                </blockquote>
            </section>

            <!-- Slide 12: Recommendations -->
            <section>
                <header>
                    <h2>11. Recommendations</h2>
                </header>
                <ul>
                    <li>
                        <strong>For Policy Makers</strong>:
                        <ul>
                            <li><strong>Enhance Engagement Efforts</strong> with affluent communities</li>
                            <li>Launch <strong>public awareness campaigns</strong> on survey importance</li>
                        </ul>
                    </li>
                    <li>
                        <strong>For Survey Organizations</strong>:
                        <ul>
                            <li><strong>Improve Accessibility</strong> via technological platforms</li>
                            <li><strong>Invest in Training</strong> for staff on communication skills</li>
                        </ul>
                    </li>
                    <li>
                        <strong>For Future Research</strong>:
                        <ul>
                            <li><strong>Monitor and Evaluate</strong> the effectiveness of strategies</li>
                            <li>Establish <strong>feedback mechanisms</strong> for continuous improvement</li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Continuous improvement and adaptation are key to overcoming non-response challenges."
                    </p>
                    <footer>Research Director</footer>
                </blockquote>
            </section>

            <!-- Slide 13: Conclusion -->
            <section>
                <header>
                    <h2>12. Conclusion</h2>
                </header>
                <ul>
                    <li>
                        <strong>Summary of Key Points</strong>:
                        <ul>
                            <li>Non-response among affluent groups is a significant issue impacting data quality</li>
                            <li>A <strong>multifaceted approach</strong> is required to address this challenge</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Call to Action</strong>:
                        <ul>
                            <li><strong>Implement proposed strategies</strong> to improve participation</li>
                            <li>Ensure <strong>representative data</strong> for effective policy making</li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Accurate and representative data is essential for creating effective and equitable policies."
                    </p>
                    <footer>Policy Maker</footer>
                </blockquote>
            </section>

            <!-- Slide 14: Summary and Call to Action -->
            <section>
                <header>
                    <h2>13. Summary and Call to Action</h2>
                </header>
                <ul>
                    <li>
                        <strong>Key Takeaways</strong>:
                        <ul>
                            <li>Non-response can distort survey data and policy outcomes.</li>
                            <li>Affluent demographics present unique challenges in survey participation.</li>
                            <li>Implementing targeted strategies can enhance response rates.</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Next Steps</strong>:
                        <ul>
                            <li>Adopt recommended strategies to improve survey participation.</li>
                            <li>Continuously monitor and refine survey methodologies.</li>
                            <li>Foster collaboration between policymakers and survey organizations.</li>
                        </ul>
                    </li>
                </ul>
                <blockquote>
                    <p>
                        "Taking proactive steps today ensures accurate data and effective policies tomorrow."
                    </p>
                    <footer>Community Leader</footer>
                </blockquote>
            </section>

            <!-- Slide 15: Thank You / Q&A -->
            <section>
                <header>
                    <h2>Thank You!</h2>
                </header>
                <p>Questions & Answers</p>
                
            </section>
        
	</article>
</main>

<style>
/* Global Box Sizing */
*, *::before, *::after {
    box-sizing: border-box;
}

/* General Styles */
main,
header {
    overflow: hidden;
    padding: 30px;
    font-family: 'Poppins', sans-serif;
    margin: 0 auto; /* Center the main content */
    max-width: 1200px; /* Optional: constrain the main content width */
}

/* Header Styles */
.reveal section h1 {
    font-size: 2.5rem;
    text-align: center;
    margin-bottom: 0.5em;
}

.reveal section h2 {
    font-size: 2rem;
    text-align: center;
    margin-bottom: 0.5em;
}


/* Text and List Styles */
.reveal section p,
.reveal section li {
    font-size: 1.125rem; /* Increased font size for better readability */
    line-height: 1.6;
    margin: 10px 0;
}

.reveal section ul {
    padding-left: 20px;
}

.reveal section article {
    font-size: 1.125rem;
    margin: 10px 0;
}

/* Slide Layout */
.reveal section {
 
    background-color: transparent;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center; /* Center children horizontally */
    height: 100%;
    padding: 20px;
}

/* Image Styles */
.reveal img {
    display: block;
    
    margin: 20px auto; /* Centered image with vertical spacing */
    border-radius: 18px; /* Added slight rounding for aesthetics */
    border-color: azure;
    box-shadow: 0 4px 8px rgba(109, 107, 107, 0.7); /* Added subtle shadow */
}

/* Blockquote Styles */
.reveal blockquote {
    max-width: 60%;
    margin: 20px auto;
    padding: 15px 20px;
    background-color: transparent;
    border: none;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    text-align: center;
    font-style: italic;
    color: #191b1c;
}

/* Responsive Adjustments */
@media (max-width: 768px) {
    .reveal blockquote {
        max-width: 90%;
        padding: 10px 15px;
        font-size: 1rem;
    }
    
    .reveal section h1 {
        font-size: 2rem;
    }

    .reveal section h2 {
        font-size: 1.75rem;
    }

    .reveal section p,
    .reveal section li {
        font-size: 1rem;
    }

    .reveal img {
        max-width: 90%;
        max-height: 50vh;
    }
}


/* Blockquote Footer */
.reveal blockquote footer {
    text-align: right;
    font-size: 0.9rem;
    color: #657b83;
    margin-top: 5px;
}

    
</style>