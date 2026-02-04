<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DepEd Career Pathways Interactive Guide</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Merriweather:ital,wght@0,300;0,700;1,300&display=swap" rel="stylesheet">

    <!-- Placeholder Comments Required -->
    <!-- Chosen Palette: Warm Neutrals & Earth Tones (Cream #FDFBF7, Stone #F5F5F4, Deep Brown #433422, Muted Gold #D97706) -->
    <!-- Application Structure Plan: The app is designed as a vertical scrollytelling experience. It begins with the 'Whole Person' concept to ground the user, then moves to practical 'Pathways' exploration, followed by 'Influences' analysis, and concludes with 'Middle-Level Skills'. This structure moves from abstract philosophy to concrete options to actionable skills. Key interactions include tabbed filtering for pathways and dynamic charts for comparing durations and influence weights. -->
    <!-- Visualization & Content Choices: 
         1. Degree Duration Chart (Bar Chart): Transforms text data (2 years, 4 years) into a visual timeline to compare commitment. 
         2. Influence Factors (Radar/Bar Chart): Visualizes the qualitative 'weight' of influences (Parents = High) to show relative impact. 
         3. Pathways Grid: Uses interactive cards to organize dense text into digestible chunks. 
         4. Interaction: JS-based filtering and modal-like expansions. 
         5. CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. Standard HTML/CSS/Canvas only. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'deped-cream': '#FDFBF7',
                        'deped-stone': '#E7E5E4',
                        'deped-brown': '#433422',
                        'deped-gold': '#D97706',
                        'deped-accent': '#A16207',
                        'deped-text': '#292524',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Merriweather', 'serif'],
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Chart Container Styles - MANDATORY */
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            height: 400px;
            margin-left: auto;
            margin-right: auto;
            background-color: white;
            border-radius: 0.5rem;
            padding: 1rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        @media (max-width: 640px) {
            .chart-container {
                height: 300px;
            }
        }

        .pathway-card {
            transition: all 0.3s ease;
            cursor: pointer;
        }
        .pathway-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
            border-color: #D97706;
        }
        .pathway-card.active {
            background-color: #FEF3C7;
            border-color: #D97706;
        }

        html {
            scroll-behavior: smooth;
        }
        
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
        
        /* Copy Notification Style */
        #copy-notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            padding: 10px 20px;
            background: #433422;
            color: white;
            border-radius: 8px;
            z-index: 1000;
            display: none;
        }
    </style>
</head>
<body class="bg-deped-cream text-deped-text font-sans antialiased selection:bg-deped-gold selection:text-white">

    <!-- Copy Code Tool (Fix for user request) -->
    <div id="copy-notification">Code copied to clipboard!</div>
    <div class="bg-deped-brown text-white py-2 text-center text-xs flex justify-center items-center gap-4">
        <span>Need the raw code?</span>
        <button id="copy-btn" class="bg-deped-gold px-3 py-1 rounded hover:bg-deped-accent font-bold transition">Copy Whole File Code</button>
    </div>

    <!-- Navigation -->
    <nav class="sticky top-0 z-50 bg-white/90 backdrop-blur-md border-b border-stone-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16 items-center">
                <div class="flex items-center space-x-2">
                    <span class="text-2xl text-deped-gold">✦</span>
                    <span class="font-serif font-bold text-lg text-deped-brown tracking-tight">DepEd Pathways</span>
                </div>
                <div class="hidden md:flex space-x-8">
                    <button onclick="scrollToSection('holistic')" class="text-sm font-medium text-stone-600 hover:text-deped-gold transition">Holistic View</button>
                    <button onclick="scrollToSection('pathways')" class="text-sm font-medium text-stone-600 hover:text-deped-gold transition">7 Pathways</button>
                    <button onclick="scrollToSection('influences')" class="text-sm font-medium text-stone-600 hover:text-deped-gold transition">Influences</button>
                    <button onclick="scrollToSection('middle-skills')" class="text-sm font-medium text-stone-600 hover:text-deped-gold transition">Middle-Level Skills</button>
                </div>
                <button onclick="toggleMobileMenu()" class="md:hidden text-stone-600 hover:text-deped-gold focus:outline-none">
                    <span class="text-2xl">☰</span>
                </button>
            </div>
        </div>
        <div id="mobile-menu" class="hidden md:hidden bg-white border-b border-stone-200">
            <div class="px-2 pt-2 pb-3 space-y-1">
                <button onclick="scrollToSection('holistic'); toggleMobileMenu()" class="block w-full text-left px-3 py-2 text-base font-medium text-stone-600 hover:bg-stone-50 hover:text-deped-gold rounded-md">Holistic View</button>
                <button onclick="scrollToSection('pathways'); toggleMobileMenu()" class="block w-full text-left px-3 py-2 text-base font-medium text-stone-600 hover:bg-stone-50 hover:text-deped-gold rounded-md">7 Pathways</button>
                <button onclick="scrollToSection('influences'); toggleMobileMenu()" class="block w-full text-left px-3 py-2 text-base font-medium text-stone-600 hover:bg-stone-50 hover:text-deped-gold rounded-md">Influences</button>
                <button onclick="scrollToSection('middle-skills'); toggleMobileMenu()" class="block w-full text-left px-3 py-2 text-base font-medium text-stone-600 hover:bg-stone-50 hover:text-deped-gold rounded-md">Middle-Level Skills</button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative bg-white overflow-hidden">
        <div class="max-w-7xl mx-auto">
            <div class="relative z-10 pb-8 bg-white sm:pb-16 md:pb-20 lg:max-w-2xl lg:w-full lg:pb-28 xl:pb-32">
                <main class="mt-10 mx-auto max-w-7xl px-4 sm:mt-12 sm:px-6 md:mt-16 lg:mt-20 lg:px-8 xl:mt-28">
                    <div class="sm:text-center lg:text-left">
                        <h1 class="text-4xl tracking-tight font-extrabold text-deped-brown sm:text-5xl md:text-6xl font-serif">
                            <span class="block xl:inline">Navigating Your</span>
                            <span class="block text-deped-gold xl:inline">Career Pathway</span>
                        </h1>
                        <p class="mt-3 text-base text-stone-500 sm:mt-5 sm:text-lg sm:max-w-xl sm:mx-auto md:mt-5 md:text-xl lg:mx-0">
                            Based on the DepEd Bureau of Learning Delivery guidelines. Explore academic routes, technical skills, and the "Whole Person" approach to future readiness.
                        </p>
                        <div class="mt-5 sm:mt-8 sm:flex sm:justify-center lg:justify-start">
                            <div class="rounded-md shadow">
                                <button onclick="scrollToSection('pathways')" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-deped-gold hover:bg-deped-accent md:py-4 md:text-lg transition">
                                    Explore Pathways
                                </button>
                            </div>
                        </div>
                    </div>
                </main>
            </div>
        </div>
        <div class="lg:absolute lg:inset-y-0 lg:right-0 lg:w-1/2 bg-stone-100 flex items-center justify-center">
            <div class="p-8 text-center text-stone-400">
                <div class="text-9xl mb-4">🎓</div>
                <p class="font-serif italic">"Career pathways are not linear."</p>
                <p class="text-sm">— Zunker, 2016</p>
            </div>
        </div>
    </header>

    <!-- Section 1: Holistic View -->
    <section id="holistic" class="py-16 bg-deped-cream border-t border-stone-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-base text-deped-gold font-semibold tracking-wide uppercase">Foundation</h2>
                <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-deped-brown sm:text-4xl font-serif">
                    The "Whole Person" Lens
                </p>
                <p class="mt-4 max-w-2xl text-xl text-stone-500 mx-auto">
                    Career development considers values, personality, life circumstances, and cultural background.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                <div class="bg-white p-6 rounded-lg shadow-sm border border-stone-100 h-full">
                    <h3 class="text-lg font-bold text-deped-brown mb-4">A Dynamic Interplay</h3>
                    <p class="text-stone-600 mb-4 text-sm">
                        Pathways are shaped by internal and external factors. This approach is especially relevant for students in:
                    </p>
                    <ul class="space-y-3">
                        <li class="flex items-start text-sm">
                            <span class="flex-shrink-0 h-5 w-5 rounded-full bg-green-100 flex items-center justify-center text-green-600 text-xs font-bold mr-3">✓</span>
                            <span class="text-stone-700 font-medium">Healthcare & Support</span>
                        </li>
                        <li class="flex items-start text-sm">
                            <span class="flex-shrink-0 h-5 w-5 rounded-full bg-green-100 flex items-center justify-center text-green-600 text-xs font-bold mr-3">✓</span>
                            <span class="text-stone-700 font-medium">Skilled Trades & Logistics</span>
                        </li>
                        <li class="flex items-start text-sm">
                            <span class="flex-shrink-0 h-5 w-5 rounded-full bg-green-100 flex items-center justify-center text-green-600 text-xs font-bold mr-3">✓</span>
                            <span class="text-stone-700 font-medium">IT & Advanced Tech</span>
                        </li>
                    </ul>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-sm border border-stone-100 flex flex-col items-center justify-center h-full min-h-[300px]">
                    <div class="relative w-48 h-48">
                        <div class="absolute inset-0 rounded-full border-2 border-dashed border-deped-gold"></div>
                        <div class="absolute inset-4 rounded-full bg-stone-50 flex items-center justify-center text-center p-4">
                            <div class="text-sm font-bold text-deped-brown">THE STUDENT</div>
                        </div>
                    </div>
                    <p class="text-center text-xs text-stone-400 mt-6 italic">Visualizing Zunker's Model</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 2: 7 Pathways Explorer -->
    <section id="pathways" class="py-16 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="mb-10">
                <h2 class="text-3xl font-serif font-bold text-deped-brown">7 Types of Higher Education Pathways</h2>
                <p class="mt-4 text-stone-600 max-w-3xl">
                    Select a pathway below to reveal specific details and commitment levels.
                </p>
            </div>

            <div class="flex flex-col lg:flex-row gap-8">
                <div class="lg:w-1/3 space-y-2 overflow-y-auto max-h-[500px] pr-2 no-scrollbar">
                    <div onclick="showPathway(0)" id="p-btn-0" class="pathway-card active p-4 border-l-4 border-deped-gold bg-stone-50 rounded-r-lg">
                        <h3 class="font-bold text-deped-brown">1. Academic Pathways</h3>
                    </div>
                    <div onclick="showPathway(1)" id="p-btn-1" class="pathway-card p-4 border-l-4 border-transparent bg-white hover:bg-stone-50 rounded-r-lg">
                        <h3 class="font-bold text-deped-brown">2. Vocational / Technical</h3>
                    </div>
                    <div onclick="showPathway(2)" id="p-btn-2" class="pathway-card p-4 border-l-4 border-transparent bg-white hover:bg-stone-50 rounded-r-lg">
                        <h3 class="font-bold text-deped-brown">3. Pathway / Foundation</h3>
                    </div>
                    <div onclick="showPathway(3)" id="p-btn-3" class="pathway-card p-4 border-l-4 border-transparent bg-white hover:bg-stone-50 rounded-r-lg">
                        <h3 class="font-bold text-deped-brown">4. Transfer Pathways</h3>
                    </div>
                    <div onclick="showPathway(4)" id="p-btn-4" class="pathway-card p-4 border-l-4 border-transparent bg-white hover:bg-stone-50 rounded-r-lg">
                        <h3 class="font-bold text-deped-brown">5. Online / Distance</h3>
                    </div>
                    <div onclick="showPathway(5)" id="p-btn-5" class="pathway-card p-4 border-l-4 border-transparent bg-white hover:bg-stone-50 rounded-r-lg">
                        <h3 class="font-bold text-deped-brown">6. Alternative (RPL)</h3>
                    </div>
                    <div onclick="showPathway(6)" id="p-btn-6" class="pathway-card p-4 border-l-4 border-transparent bg-white hover:bg-stone-50 rounded-r-lg">
                        <h3 class="font-bold text-deped-brown">7. Specialized Pathways</h3>
                    </div>
                </div>

                <div class="lg:w-2/3 bg-stone-50 rounded-xl p-8 border border-stone-200 shadow-inner min-h-[400px]">
                    <div id="pathway-content" class="h-full flex flex-col justify-center transition-opacity duration-300"></div>
                </div>
            </div>

            <div class="mt-16">
                 <h3 class="text-xl font-bold text-deped-brown mb-6 text-center">Comparing Time Commitment</h3>
                 <div class="chart-container">
                    <canvas id="durationChart"></canvas>
                 </div>
            </div>
        </div>
    </section>

    <!-- Section 3: Influences Dashboard -->
    <section id="influences" class="py-16 bg-deped-brown text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl font-serif font-bold text-deped-gold mb-8">What drives career choices?</h2>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div>
                    <div class="bg-white rounded-lg p-2 chart-container">
                        <canvas id="influencesChart"></canvas>
                    </div>
                </div>

                <div class="space-y-4">
                    <div class="bg-white/10 p-4 rounded-lg">
                        <h3 class="font-bold text-deped-gold">Parental Influence</h3>
                        <p class="text-stone-200 text-sm">Most significant factor. Parents' professions and expectations heavily shape aspirations.</p>
                    </div>
                    <div class="bg-white/10 p-4 rounded-lg">
                        <h3 class="font-bold text-deped-gold">Financial Constraints</h3>
                        <p class="text-stone-200 text-sm">Often leads to choosing paths with quicker ROI or earlier workforce entry.</p>
                    </div>
                    <div class="bg-white/10 p-4 rounded-lg">
                        <h3 class="font-bold text-deped-gold">Market Demand</h3>
                        <p class="text-stone-200 text-sm">Especially in IT, students look at job stability and salary prospects.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Middle-Level Skills -->
    <section id="middle-skills" class="py-16 bg-deped-cream">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-serif font-bold text-deped-brown">Middle-Level Skills</h2>
                <p class="mt-4 text-stone-600 max-w-2xl mx-auto">Beyond basic education but specialized. Key learning modalities include:</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <div class="bg-white rounded-xl shadow-sm p-6 border-t-4 border-blue-500 text-center">
                    <h4 class="font-bold text-gray-800 mb-2">Flexible</h4>
                    <p class="text-xs text-gray-600">Modular learning units.</p>
                </div>
                <div class="bg-white rounded-xl shadow-sm p-6 border-t-4 border-green-500 text-center">
                    <h4 class="font-bold text-gray-800 mb-2">Competency</h4>
                    <p class="text-xs text-gray-600">Based on mastery.</p>
                </div>
                <div class="bg-white rounded-xl shadow-sm p-6 border-t-4 border-purple-500 text-center">
                    <h4 class="font-bold text-gray-800 mb-2">Blended</h4>
                    <p class="text-xs text-gray-600">Online + Hands-on.</p>
                </div>
                <div class="bg-white rounded-xl shadow-sm p-6 border-t-4 border-orange-500 text-center">
                    <h4 class="font-bold text-gray-800 mb-2">Integrated</h4>
                    <p class="text-xs text-gray-600">Work-site learning.</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-stone-900 text-stone-500 py-8 text-center text-xs">
        <p>Based on DepEd Bureau of Learning Delivery documents.</p>
    </footer>

    <script>
        const pathwaysData = [
            { title: "Academic Pathways", icon: "📚", desc: "Theoretical disciplines.", details: ["Associate: 2y", "Bachelor: 3-4y", "Master: +1-2y", "Doctoral: +3-7y"] },
            { title: "Vocational / Technical", icon: "🔧", desc: "Practical skills.", details: ["Certificates: 6-12m", "Apprenticeships: Work-based", "TESDA NC II: Job-ready"] },
            { title: "Pathway / Foundation", icon: "🌉", desc: "Bridging gaps.", details: ["Foundation Year", "English Language Pathways", "Pre-requisite courses"] },
            { title: "Transfer Pathways", icon: "🔄", desc: "Institutional hopping.", details: ["2+2 Programs", "Articulation Agreements", "Credit recognition"] },
            { title: "Online / Distance", icon: "💻", desc: "Flexible remote.", details: ["MOOCs", "Microcredentials", "Digital degrees"] },
            { title: "Alternative (RPL)", icon: "⭐", desc: "Experience counts.", details: ["Portfolio Assessment", "Work-experience credits", "Non-traditional entry"] },
            { title: "Specialized Pathways", icon: "🚀", desc: "High performance.", details: ["Honors Programs", "Dual Degrees", "Accelerated 3yr Bachelor's"] }
        ];

        function showPathway(index) {
            document.querySelectorAll('.pathway-card').forEach((el, i) => {
                el.classList.toggle('active', i === index);
                el.classList.toggle('border-deped-gold', i === index);
                el.classList.toggle('bg-stone-50', i === index);
                el.classList.toggle('border-transparent', i !== index);
                el.classList.toggle('bg-white', i !== index);
            });

            const p = pathwaysData[index];
            const contentDiv = document.getElementById('pathway-content');
            contentDiv.style.opacity = '0';
            setTimeout(() => {
                contentDiv.innerHTML = `
                    <div class="text-5xl mb-4">${p.icon}</div>
                    <h3 class="text-2xl font-serif font-bold text-deped-brown mb-2">${p.title}</h3>
                    <p class="text-deped-gold font-medium mb-4">${p.desc}</p>
                    <div class="bg-white p-4 rounded-lg border border-stone-100">
                        <ul class="space-y-2 text-sm text-stone-600">
                            ${p.details.map(d => `<li>• ${d}</li>`).join('')}
                        </ul>
                    </div>
                `;
                contentDiv.style.opacity = '1';
            }, 200);
        }

        function scrollToSection(id) {
            document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
        }

        function toggleMobileMenu() {
            document.getElementById('mobile-menu').classList.toggle('hidden');
        }

        document.getElementById('copy-btn').addEventListener('click', function() {
            const htmlContent = document.documentElement.outerHTML;
            const tempTextArea = document.createElement("textarea");
            tempTextArea.value = htmlContent;
            document.body.appendChild(tempTextArea);
            tempTextArea.select();
            document.execCommand("copy");
            document.body.removeChild(tempTextArea);
            
            const notify = document.getElementById('copy-notification');
            notify.style.display = 'block';
            setTimeout(() => { notify.style.display = 'none'; }, 2000);
        });

        document.addEventListener('DOMContentLoaded', () => {
            showPathway(0);
            new Chart(document.getElementById('durationChart'), {
                type: 'bar',
                data: {
                    labels: ['Associate', 'Bachelor', 'Master', 'Doctoral'],
                    datasets: [{ label: 'Years', data: [2, 4, 6, 9], backgroundColor: '#D97706' }]
                },
                options: { responsive: true, maintainAspectRatio: false }
            });

            new Chart(document.getElementById('influencesChart'), {
                type: 'doughnut',
                data: {
                    labels: ['Parents', 'Finance', 'Market', 'Peers'],
                    datasets: [{ data: [40, 30, 20, 10], backgroundColor: ['#433422', '#D97706', '#A16207', '#E7E5E4'] }]
                },
                options: { responsive: true, maintainAspectRatio: false }
            });
        });
    </script>
</body>
</html>
