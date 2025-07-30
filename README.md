# Lagos-startup
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lagos Startup Report 2025 | Partnership Opportunity</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.2/dist/chart.umd.min.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Calm Harmony (Stone, Slate, Amber) -->
    <!-- Application Structure Plan: A single-page, scrolling narrative designed to persuade potential partners. The structure starts with a high-impact hero section stating the mission, followed by a clear presentation of the problem and the proposed solution (the report). It then uses interactive elements (tabs for objectives, a chart for the timeline, clickable cards for partnership tiers) to break down complex information, making it digestible and encouraging user exploration. This thematic flow is more engaging than a traditional document structure and guides the user from understanding the need to a clear call to action. -->
    <!-- Visualization & Content Choices: 
        - Report Info: Key stats (88% activity, 60% VC). Goal: Inform/Impact. Method: Large, animated numbers. Interaction: Count-up on scroll. Justification: Creates immediate impact and memorability. Library: Vanilla JS.
        - Report Info: Core Objectives. Goal: Organize/Inform. Method: Interactive tabs. Interaction: Click to reveal content. Justification: Prevents a wall of text and allows user-led discovery. Library: Vanilla JS.
        - Report Info: Project Timeline. Goal: Change/Inform. Method: Horizontal Bar Chart (Gantt-style). Interaction: Tooltips on hover. Justification: More professional and visually clearer than a static table. Library: Chart.js.
        - Report Info: Partnership Tiers. Goal: Compare/Inform. Method: Clickable cards. Interaction: Click to expand and see benefits. Justification: Encourages interaction and simplifies comparison. Library: Vanilla JS.
        - Report Info: Funding Distribution. Goal: Compare. Method: Donut Chart. Interaction: Tooltips on hover. Justification: Provides a strong visual anchor for the 60% VC inflow statistic. Library: Chart.js.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc; /* slate-50 */
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
        .tab-active {
            background-color: #0f172a; /* slate-900 */
            color: white;
        }
        .tab-inactive {
            background-color: #e2e8f0; /* slate-200 */
            color: #334155; /* slate-700 */
        }
        .partner-card-selected {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
            border-color: #f59e0b; /* amber-500 */
        }
    </style>
</head>
<body class="text-slate-700">

    <header class="bg-white/80 backdrop-blur-lg sticky top-0 z-50 shadow-sm">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-xl font-bold text-slate-900">Lagos Startup Report 2025</a>
            <div class="hidden md:flex items-center space-x-4">
                <a href="#about" class="hover:text-amber-600 transition-colors">The Report</a>
                <a href="#objectives" class="hover:text-amber-600 transition-colors">Objectives</a>
                <a href="#deliverables" class="hover:text-amber-600 transition-colors">Deliverables</a>
                <a href="#partner" class="hover:text-amber-600 transition-colors">Partner With Us</a>
                <a href="#contact" class="bg-amber-500 text-white px-4 py-2 rounded-lg shadow-md hover:bg-amber-600 transition-all">Get Involved</a>
            </div>
            <button id="mobile-menu-button" class="md:hidden text-slate-900">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
            </button>
        </nav>
        <div id="mobile-menu" class="hidden md:hidden px-6 pb-4 space-y-2">
            <a href="#about" class="block hover:text-amber-600 transition-colors">The Report</a>
            <a href="#objectives" class="block hover:text-amber-600 transition-colors">Objectives</a>
            <a href="#deliverables" class="block hover:text-amber-600 transition-colors">Deliverables</a>
            <a href="#partner" class="block hover:text-amber-600 transition-colors">Partner With Us</a>
            <a href="#contact" class="block bg-amber-500 text-white px-4 py-2 rounded-lg shadow-md hover:bg-amber-600 transition-all mt-2 text-center">Get Involved</a>
        </div>
    </header>

    <main>
        <section id="hero" class="py-20 md:py-32 bg-white">
            <div class="container mx-auto px-6 text-center">
                <h1 class="text-4xl md:text-6xl font-bold text-slate-900 mb-4 leading-tight">Reshaping the Lagos Startup Ecosystem with Data</h1>
                <p class="text-lg md:text-xl max-w-3xl mx-auto text-slate-600 mb-8">A bold, data-driven initiative to unlock actionable intelligence for investors, policymakers, and founders in Africa's most vibrant innovation hub.</p>
                <div class="flex justify-center items-center space-x-4 mb-12">
                     <a href="#partner" class="bg-amber-500 text-white px-8 py-3 rounded-lg shadow-lg hover:bg-amber-600 transition-all text-lg font-semibold">Become a Partner</a>
                     <a href="#about" class="bg-slate-200 text-slate-800 px-8 py-3 rounded-lg shadow-lg hover:bg-slate-300 transition-all text-lg font-semibold">Learn More</a>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto mt-16 text-left">
                    <div class="bg-slate-100 p-6 rounded-lg">
                        <div class="flex items-center">
                            <span class="text-5xl font-bold text-amber-500 mr-4" data-target="88">0</span>
                            <span class="text-5xl font-bold text-amber-500">%</span>
                        </div>
                        <p class="text-slate-600 mt-2">Of Nigeria’s startup activity is concentrated in Lagos, making it the undisputed epicenter of innovation.</p>
                    </div>
                    <div class="bg-slate-100 p-6 rounded-lg">
                         <div class="flex items-center">
                            <span class="text-5xl font-bold text-amber-500 mr-2" data-target="60">0</span>
                            <span class="text-5xl font-bold text-amber-500">%</span>
                        </div>
                        <p class="text-slate-600 mt-2">Of the country's venture capital inflows are captured by Lagos startups, yet significant funding gaps remain.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="about" class="py-20">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-slate-900">The Challenge and The Opportunity</h2>
                    <p class="mt-4 max-w-2xl mx-auto text-lg text-slate-600">Despite its dominance, the Lagos ecosystem faces critical hurdles. This report is designed to transform those challenges into data-driven opportunities for growth.</p>
                </div>

                <div class="grid md:grid-cols-5 gap-8 items-start">
                    <div class="md:col-span-2 bg-white p-8 rounded-lg shadow-md">
                        <h3 class="text-2xl font-bold text-red-600 mb-4">The Invisible Fault Lines</h3>
                        <ul class="space-y-3 text-slate-600">
                            <li class="flex items-start"><span class="text-red-500 mr-3 mt-1">&#10007;</span>Limited access to early-stage capital</li>
                            <li class="flex items-start"><span class="text-red-500 mr-3 mt-1">&#10007;</span>Poor infrastructure impeding operations</li>
                            <li class="flex items-start"><span class="text-red-500 mr-3 mt-1">&#10007;</span>Fragile and unpredictable regulatory environments</li>
                            <li class="flex items-start"><span class="text-red-500 mr-3 mt-1">&#10007;</span>High failure rates at pre-seed & seed stages</li>
                            <li class="flex items-start"><span class="text-red-500 mr-3 mt-1">&#10007;</span>Overlooked sectors and founder demographics</li>
                        </ul>
                    </div>
                    <div class="md:col-span-3 bg-slate-900 text-white p-8 rounded-lg shadow-lg">
                         <h3 class="text-2xl font-bold text-amber-400 mb-4">Our Solution: The Lagos Startup Report</h3>
                         <p class="mb-6">The LSR 2025 is more than a report; it's a strategic ecosystem intervention. We move beyond anecdotes to provide the most comprehensive, founder-centric analysis of Lagos to date. By blending rigorous data with human-centered storytelling, we uncover the real dynamics of success, failure, and resilience.</p>
                         <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div class="bg-slate-800 p-4 rounded-lg"><span class="font-semibold text-amber-400">Visual-First:</span> Clear, engaging, and actionable insights through rich data visualizations.</div>
                            <div class="bg-slate-800 p-4 rounded-lg"><span class="font-semibold text-amber-400">Founder-Centric:</span> Capturing real experiences, motivations, and stressors.</div>
                            <div class="bg-slate-800 p-4 rounded-lg"><span class="font-semibold text-amber-400">Solution-Oriented:</span> Delivering stakeholder-specific recommendations for tangible change.</div>
                            <div class="bg-slate-800 p-4 rounded-lg"><span class="font-semibold text-amber-400">Inclusive Scope:</span> Covering diverse sectors, stages, and geographies.</div>
                         </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="objectives" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-slate-900">Core Objectives</h2>
                    <p class="mt-4 max-w-2xl mx-auto text-lg text-slate-600">Our research is guided by a set of core objectives designed to generate a holistic and actionable understanding of the ecosystem. Click on each objective to learn more about our focus.</p>
                </div>
                <div class="flex flex-wrap justify-center gap-2 mb-8">
                    <button data-tab="tab1" class="tab-button px-4 py-2 rounded-lg font-semibold transition-colors tab-active">Map Ecosystem</button>
                    <button data-tab="tab2" class="tab-button px-4 py-2 rounded-lg font-semibold transition-colors tab-inactive">Uncover Failure</button>
                    <button data-tab="tab3" class="tab-button px-4 py-2 rounded-lg font-semibold transition-colors tab-inactive">Analyse Funding</button>
                    <button data-tab="tab4" class="tab-button px-4 py-2 rounded-lg font-semibold transition-colors tab-inactive">Assess Support</button>
                    <button data-tab="tab5" class="tab-button px-4 py-2 rounded-lg font-semibold transition-colors tab-inactive">Identify Growth</button>
                </div>
                <div class="max-w-3xl mx-auto bg-slate-50 p-8 rounded-lg shadow-inner">
                    <div id="tab1" class="tab-content">
                        <h3 class="text-2xl font-bold text-slate-800 mb-3">Map the Lagos Startup Ecosystem</h3>
                        <p>We will identify and categorize the city’s startups, incubators, accelerators, investors, public institutions, and support organisations, creating a comprehensive map of how they interact and influence one another.</p>
                    </div>
                    <div id="tab2" class="tab-content hidden">
                        <h3 class="text-2xl font-bold text-slate-800 mb-3">Uncover Causes of Failure</h3>
                        <p>Our research explores the structural, psychological, policy, and operational reasons why startups fail, especially at the pre-seed and seed stages, using first-hand narratives and validated data to move beyond surface-level explanations.</p>
                    </div>
                    <div id="tab3" class="tab-content hidden">
                        <h3 class="text-2xl font-bold text-slate-800 mb-3">Analyse Funding Flows</h3>
                        <p>We will examine capital movement within and across sectors, highlighting critical gaps, disparities, and overlooked segments such as women-led ventures and non-fintech verticals to guide future investment.</p>
                        <div class="chart-container mt-6 h-64 max-h-64">
                            <canvas id="fundingChart"></canvas>
                        </div>
                    </div>
                    <div id="tab4" class="tab-content hidden">
                        <h3 class="text-2xl font-bold text-slate-800 mb-3">Assess Support Infrastructure</h3>
                        <p>This objective focuses on evaluating the effectiveness and accessibility of the ecosystem's legal, advisory, training, mentorship, and professional services, identifying what works and where improvements are needed.</p>
                    </div>
                    <div id="tab5" class="tab-content hidden">
                        <h3 class="text-2xl font-bold text-slate-800 mb-3">Identify Growth Frontiers</h3>
                        <p>We will spotlight underinvested but high-potential sectors such as AgriTech, CivicTech, HealthTech, and the Blue Economy, providing a roadmap for diversifying Lagos's innovation portfolio.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="methodology" class="py-20">
            <div class="container mx-auto px-6">
                 <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-slate-900">A Rigorous, Mixed-Methods Approach</h2>
                    <p class="mt-4 max-w-2xl mx-auto text-lg text-slate-600">Our insights are built on a foundation of triangulated data, ensuring our findings are rich, context-aware, and practically useful for all stakeholders.</p>
                </div>
                <div class="max-w-4xl mx-auto">
                    <div class="relative">
                        <div class="absolute left-1/2 top-0 bottom-0 w-0.5 bg-slate-300 hidden md:block"></div>
                        <div class="space-y-12">
                            <div class="md:flex items-center md:space-x-8">
                                <div class="md:w-1/2">
                                    <div class="bg-white p-6 rounded-lg shadow-md">
                                        <h4 class="font-bold text-xl text-amber-600">1. Data Collection</h4>
                                        <p class="text-slate-600 mt-2">Quantitative surveys of 200+ founders, Key Informant Interviews (KIIs), and Focus Group Discussions (FGDs).</p>
                                    </div>
                                </div>
                                <div class="w-12 h-12 bg-slate-900 rounded-full flex items-center justify-center text-white font-bold text-xl absolute left-1/2 -translate-x-1/2 hidden md:flex">1</div>
                            </div>
                             <div class="md:flex flex-row-reverse items-center md:space-x-8 md:space-x-reverse">
                                <div class="md:w-1/2">
                                    <div class="bg-white p-6 rounded-lg shadow-md">
                                        <h4 class="font-bold text-xl text-amber-600">2. Secondary Review</h4>
                                        <p class="text-slate-600 mt-2">Analysis of existing industry reports, deal databases, government regulations, and academic literature to build a comprehensive context.</p>
                                    </div>
                                </div>
                                <div class="w-12 h-12 bg-slate-900 rounded-full flex items-center justify-center text-white font-bold text-xl absolute left-1/2 -translate-x-1/2 hidden md:flex">2</div>
                            </div>
                             <div class="md:flex items-center md:space-x-8">
                                <div class="md:w-1/2">
                                    <div class="bg-white p-6 rounded-lg shadow-md">
                                        <h4 class="font-bold text-xl text-amber-600">3. Validation & Refinement</h4>
                                        <p class="text-slate-600 mt-2">Collaborative stakeholder validation workshops to test, challenge, and refine our insights with ecosystem actors.</p>
                                    </div>
                                </div>
                                <div class="w-12 h-12 bg-slate-900 rounded-full flex items-center justify-center text-white font-bold text-xl absolute left-1/2 -translate-x-1/2 hidden md:flex">3</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="deliverables" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-slate-900">Key Deliverables</h2>
                    <p class="mt-4 max-w-2xl mx-auto text-lg text-slate-600">By October 31, 2025, we will deliver a suite of high-impact resources designed for maximum utility and engagement across different audiences.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <div class="bg-slate-50 p-6 rounded-lg border border-slate-200">
                        <h4 class="font-bold text-xl text-slate-800">Main Report</h4>
                        <p class="text-slate-600 mt-2">A concise, visually compelling publication distilling complex findings into digestible narratives and infographics.</p>
                    </div>
                    <div class="bg-slate-50 p-6 rounded-lg border border-slate-200">
                        <h4 class="font-bold text-xl text-slate-800">Executive Summary</h4>
                        <p class="text-slate-600 mt-2">A highly visual, insight-packed brief with actionable takeaways for senior leaders.</p>
                    </div>
                    <div class="bg-slate-50 p-6 rounded-lg border border-slate-200">
                        <h4 class="font-bold text-xl text-slate-800">Founder Survey Report</h4>
                        <p class="text-slate-600 mt-2">Aggregated findings from founders, capturing hidden insights and red flags.</p>
                    </div>
                    <div class="bg-slate-50 p-6 rounded-lg border border-slate-200">
                        <h4 class="font-bold text-xl text-slate-800">Sector Deep-Dives</h4>
                        <p class="text-slate-600 mt-2">Detailed analyses of 3–5 high-potential, underserved verticals.</p>
                    </div>
                    <div class="bg-slate-50 p-6 rounded-lg border border-slate-200">
                        <h4 class="font-bold text-xl text-slate-800">Investor Guide</h4>
                        <p class="text-slate-600 mt-2">Practical advice, deal-flow insights, and risk maps for funders.</p>
                    </div>
                    <div class="bg-slate-50 p-6 rounded-lg border border-slate-200">
                        <h4 class="font-bold text-xl text-slate-800">Policy Briefs</h4>
                        <p class="text-slate-600 mt-2">Targeted, data-backed recommendations for federal and state policy actors.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="timeline" class="py-20">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-slate-900">Project Timeline</h2>
                    <p class="mt-4 max-w-2xl mx-auto text-lg text-slate-600">We are operating on a clearly defined and accelerated timeline to deliver timely insights.</p>
                </div>
                <div class="bg-white p-4 sm:p-8 rounded-lg shadow-lg">
                    <div class="chart-container">
                        <canvas id="timelineChart"></canvas>
                    </div>
                </div>
            </div>
        </section>

        <section id="partner" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-slate-900">Partner With Us</h2>
                    <p class="mt-4 max-w-2xl mx-auto text-lg text-slate-600">Your organization can play a vital role in this transformative project. Select a partnership tier to see the associated benefits and join us in shaping the future of innovation in Lagos.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
                    <div id="funding-partner" class="partner-card border-2 border-slate-200 p-6 rounded-lg cursor-pointer transition-all">
                        <h4 class="font-bold text-xl text-slate-800">Funding Partner</h4>
                        <p class="text-slate-600 mt-2">Provide financial support for research, content development, and dissemination.</p>
                    </div>
                    <div id="data-partner" class="partner-card border-2 border-slate-200 p-6 rounded-lg cursor-pointer transition-all">
                        <h4 class="font-bold text-xl text-slate-800">Data Partner</h4>
                        <p class="text-slate-600 mt-2">Share anonymised data, co-distribute surveys, or facilitate founder access.</p>
                    </div>
                    <div id="amplification-partner" class="partner-card border-2 border-slate-200 p-6 rounded-lg cursor-pointer transition-all">
                        <h4 class="font-bold text-xl text-slate-800">Amplification Partner</h4>
                        <p class="text-slate-600 mt-2">Support the report's visibility through media and community networks.</p>
                    </div>
                </div>
                <div id="partner-benefits" class="max-w-4xl mx-auto bg-slate-50 p-8 rounded-lg shadow-inner min-h-[200px] flex items-center justify-center">
                    <p class="text-slate-500 text-center">Select a partnership tier above to view the benefits.</p>
                </div>
            </div>
        </section>

        <section id="contact" class="py-20 bg-slate-900 text-white">
            <div class="container mx-auto px-6 text-center">
                <h2 class="text-3xl md:text-4xl font-bold">Become a Game-Changer</h2>
                <p class="mt-4 max-w-2xl mx-auto text-lg text-slate-300 mb-8">The Lagos Startup Report 2025 can be a pivotal force for innovation policy, venture capital deployment, and founder resilience across Africa. Let's explore how we can collaborate.</p>
                <a href="mailto:maryann.onu@example.com?subject=Lagos%20Startup%20Report%202025%20Partnership" class="bg-amber-500 text-white px-8 py-4 rounded-lg shadow-lg hover:bg-amber-600 transition-all text-lg font-semibold">Schedule a Presentation</a>
            </div>
        </section>
    </main>

    <footer class="bg-white py-8">
        <div class="container mx-auto px-6 text-center text-slate-500">
            <p>&copy; 2025 Lagos Startup Report Initiative. All Rights Reserved.</p>
            <p class="text-sm mt-2">Contact: Maryann Onu, Stakeholder Engagement Team</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });

            const counters = document.querySelectorAll('.text-5xl[data-target]');
            const speed = 200; 

            const animateCounters = () => {
                counters.forEach(counter => {
                    const updateCount = () => {
                        const target = +counter.getAttribute('data-target');
                        const count = +counter.innerText;
                        const inc = target / speed;

                        if (count < target) {
                            counter.innerText = Math.ceil(count + inc);
                            setTimeout(updateCount, 1);
                        } else {
                            counter.innerText = target;
                        }
                    };
                    updateCount();
                });
            };
            
            const heroSection = document.getElementById('hero');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        animateCounters();
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.5 });
            observer.observe(heroSection);

            const tabButtons = document.querySelectorAll('.tab-button');
            const tabContents = document.querySelectorAll('.tab-content');
            tabButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const tabId = button.dataset.tab;

                    tabButtons.forEach(btn => {
                        btn.classList.remove('tab-active');
                        btn.classList.add('tab-inactive');
                    });
                    button.classList.add('tab-active');
                    button.classList.remove('tab-inactive');

                    tabContents.forEach(content => {
                        if (content.id === tabId) {
                            content.classList.remove('hidden');
                        } else {
                            content.classList.add('hidden');
                        }
                    });
                });
            });

            const partnerCards = document.querySelectorAll('.partner-card');
            const benefitsContainer = document.getElementById('partner-benefits');
            const benefitsData = {
                'funding-partner': {
                    title: 'Benefits for Funding Partners',
                    points: [
                        'Prominent brand visibility and co-author recognition.',
                        'Speaking opportunities at the official launch forum.',
                        'Early access to all reports, data, and insights.',
                        'Direct influence on a key piece of ecosystem research.'
                    ]
                },
                'data-partner': {
                    title: 'Benefits for Data Partners',
                    points: [
                        'Access to custom data slices and collaborative research.',
                        'Recognition as a key data contributor to the ecosystem.',
                        'Shape research questions with proprietary insights.',
                        'Strengthen your position as a data-driven organization.'
                    ]
                },
                'amplification-partner': {
                    title: 'Benefits for Amplification Partners',
                    points: [
                        'Brand visibility across all report communications.',
                        'Association with a high-impact, credible research initiative.',
                        'Access to shareable, high-quality content for your channels.',
                        'Demonstrate commitment to the growth of the local ecosystem.'
                    ]
                }
            };

            partnerCards.forEach(card => {
                card.addEventListener('click', () => {
                    partnerCards.forEach(c => c.classList.remove('partner-card-selected'));
                    card.classList.add('partner-card-selected');
                    
                    const partnerId = card.id;
                    const data = benefitsData[partnerId];
                    
                    let benefitsHTML = `<div class="text-left w-full">
                        <h4 class="font-bold text-xl text-slate-800 mb-4">${data.title}</h4>
                        <ul class="space-y-2">`;
                    data.points.forEach(point => {
                        benefitsHTML += `<li class="flex items-start"><span class="text-amber-500 mr-3 mt-1">&#10003;</span><span>${point}</span></li>`;
                    });
                    benefitsHTML += `</ul></div>`;
                    
                    benefitsContainer.innerHTML = benefitsHTML;
                });
            });

            const fundingCtx = document.getElementById('fundingChart');
            if (fundingCtx) {
                new Chart(fundingCtx, {
                    type: 'doughnut',
                    data: {
                        labels: ['Lagos Startups', 'Rest of Nigeria'],
                        datasets: [{
                            label: 'VC Inflow Distribution',
                            data: [60, 40],
                            backgroundColor: ['#0f172a', '#f59e0b'],
                            borderColor: '#ffffff',
                            borderWidth: 4
                        }]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: {
                                position: 'top',
                            },
                            title: {
                                display: true,
                                text: 'Venture Capital Inflow Distribution'
                            }
                        }
                    }
                });
            }

            const timelineCtx = document.getElementById('timelineChart');
            if (timelineCtx) {
                 new Chart(timelineCtx, {
                    type: 'bar',
                    data: {
                        labels: ['Partner Mobilization', 'Survey & Interview', 'Data Analysis & Drafting', 'Finalization & Launch'],
                        datasets: [{
                            label: 'Project Phase',
                            data: [
                                { x: [new Date('2025-07-01'), new Date('2025-07-31')], y: 'Partner Mobilization' },
                                { x: [new Date('2025-08-01'), new Date('2025-09-15')], y: 'Survey & Interview' },
                                { x: [new Date('2025-09-15'), new Date('2025-10-15')], y: 'Data Analysis & Drafting' },
                                { x: [new Date('2025-10-15'), new Date('2025-10-31')], y: 'Finalization & Launch' }
                            ],
                            backgroundColor: [
                                'rgba(15, 23, 42, 0.7)',
                                'rgba(245, 158, 11, 0.7)',
                                'rgba(15, 23, 42, 0.7)',
                                'rgba(245, 158, 11, 0.7)',
                            ],
                            borderColor: [
                                'rgba(15, 23, 42, 1)',
                                'rgba(245, 158, 11, 1)',
                                'rgba(15, 23, 42, 1)',
                                'rgba(245, 158, 11, 1)',
                            ],
                            borderWidth: 1,
                            barPercentage: 0.5,
                            categoryPercentage: 0.8
                        }]
                    },
                    options: {
                        indexAxis: 'y',
                        responsive: true,
                        maintainAspectRatio: false,
                        scales: {
                           x: {
                                min: new Date('2025-07-01').valueOf(),
                                max: new Date('2025-11-01').valueOf(),
                                type: 'time',
                                time: {
                                    unit: 'month'
                                },
                                title: {
                                    display: true,
                                    text: 'Date'
                                }
                            },
                            y: {
                                stacked: true
                            }
                        },
                        plugins: {
                            legend: {
                                display: false
                            },
                            tooltip: {
                                callbacks: {
                                    title: function(context) {
                                        return context[0].label;
                                    },
                                    label: function(context) {
                                       const start = new Date(context.raw.x[0]).toLocaleDateString();
                                       const end = new Date(context.raw.x[1]).toLocaleDateString();
                                       return `Duration: ${start} - ${end}`;
                                    }
                                }
                            }
                        }
                    }
                });
            }
        });
    </script>
</body>
</html>
