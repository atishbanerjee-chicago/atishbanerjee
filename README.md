<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Atish Banerjee | Product Strategy Portfolio</title>
    <meta name="description" content="Strategic Product Executive Portfolio for Atish Banerjee. AI Innovation, RWD Strategy, and Digital Transformation.">
    
    <!-- Open Graph for Social Sharing (LinkedIn) -->
    <meta property="og:title" content="Atish Banerjee - Strategic Product Executive">
    <meta property="og:description" content="View my interactive portfolio covering AI Innovation, Market Strategy ($250M SOM), and Healthcare Transformation.">
    <meta property="og:image" content="https://ui-avatars.com/api/?name=Atish+Banerjee&background=0f172a&color=fff&size=512&font-size=0.33">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Plotly.js -->
    <script src="https://cdn.plot.ly/plotly-2.27.0.min.js"></script>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

    <style>
        body { font-family: 'Inter', sans-serif; background-color: #f8fafc; color: #334155; }
        
        /* Chart Styling */
        .chart-container { position: relative; width: 100%; max-width: 600px; margin: 0 auto; height: 300px; max-height: 400px; }
        @media (min-width: 768px) { .chart-container { height: 350px; } }
        .plotly-container { width: 100%; height: 400px; }

        /* Navigation */
        .nav-item.active { background-color: #eff6ff; color: #2563eb; border-right: 3px solid #2563eb; }

        /* Animations */
        .fade-in { animation: fadeIn 0.5s ease-out; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        /* Print Specifics */
        @media print {
            aside, .no-print { display: none !important; }
            body { background-color: white; height: auto; overflow: visible; }
            #content-area { padding: 0; margin: 0; overflow: visible; }
            .print-break { page-break-inside: avoid; }
        }
    </style>
</head>
<body class="flex h-screen overflow-hidden bg-slate-50">

    <!-- Sidebar (Desktop) -->
    <aside class="hidden md:flex flex-col w-72 bg-white border-r border-slate-200 shadow-sm z-20">
        <div class="p-8 border-b border-slate-100">
            <div class="w-12 h-12 bg-slate-900 text-white rounded-lg flex items-center justify-center text-xl font-bold mb-4 shadow-md">AB</div>
            <h1 class="text-xl font-bold text-slate-800 tracking-tight">Atish Banerjee</h1>
            <p class="text-xs text-blue-600 font-bold uppercase mt-1 tracking-wider">Product Executive</p>
        </div>
        
        <nav class="flex-1 overflow-y-auto py-6 space-y-1">
            <button onclick="router('dashboard')" id="nav-dashboard" class="nav-item w-full text-left px-8 py-4 text-slate-600 hover:bg-slate-50 font-medium flex items-center gap-3 active">
                <i class="fas fa-chart-line w-5 text-center"></i> Dashboard
            </button>
            <button onclick="router('strategy')" id="nav-strategy" class="nav-item w-full text-left px-8 py-4 text-slate-600 hover:bg-slate-50 font-medium flex items-center gap-3">
                <i class="fas fa-chess w-5 text-center"></i> Strategy Lab
            </button>
            <button onclick="router('experience')" id="nav-experience" class="nav-item w-full text-left px-8 py-4 text-slate-600 hover:bg-slate-50 font-medium flex items-center gap-3">
                <i class="fas fa-briefcase w-5 text-center"></i> Impact Timeline
            </button>
            <button onclick="router('print')" id="nav-print" class="nav-item w-full text-left px-8 py-4 text-slate-600 hover:bg-slate-50 font-medium flex items-center gap-3 text-emerald-600">
                <i class="fas fa-file-pdf w-5 text-center"></i> Print / PDF Mode
            </button>
        </nav>

        <div class="p-6 bg-slate-50 border-t border-slate-100">
            <a href="mailto:ban_atish@yahoo.com" class="text-sm text-slate-600 hover:text-blue-600 flex items-center gap-2 mb-2 transition-colors">
                <i class="fas fa-envelope"></i> Contact Me
            </a>
            <div class="text-sm text-slate-600 flex items-center gap-2">
                <i class="fas fa-phone"></i> (847) 826-2578
            </div>
        </div>
    </aside>

    <!-- Mobile Header -->
    <div class="md:hidden fixed w-full bg-white border-b border-slate-200 z-50 flex justify-between items-center p-4 shadow-sm">
        <div class="font-bold text-slate-800">Atish Banerjee</div>
        <button onclick="toggleMobileMenu()" class="text-slate-600 p-2">
            <i class="fas fa-bars text-xl"></i>
        </button>
    </div>

    <!-- Mobile Menu -->
    <div id="mobile-menu" class="fixed inset-0 bg-white z-40 transform translate-x-full transition-transform duration-300 md:hidden flex flex-col pt-20">
        <nav class="flex-1 px-6 space-y-4">
            <button onclick="router('dashboard'); toggleMobileMenu()" class="w-full text-left py-3 text-lg border-b border-slate-100 font-medium text-slate-800">Dashboard</button>
            <button onclick="router('strategy'); toggleMobileMenu()" class="w-full text-left py-3 text-lg border-b border-slate-100 font-medium text-slate-800">Strategy Lab</button>
            <button onclick="router('experience'); toggleMobileMenu()" class="w-full text-left py-3 text-lg border-b border-slate-100 font-medium text-slate-800">Experience</button>
            <button onclick="router('print'); toggleMobileMenu()" class="w-full text-left py-3 text-lg border-b border-slate-100 font-medium text-emerald-600">Print / PDF Resume</button>
        </nav>
    </div>

    <!-- Main Content -->
    <main id="content-area" class="flex-1 overflow-y-auto pt-16 md:pt-0 bg-slate-50/50">
        <!-- JS Injected Content -->
    </main>

    <script>
        // --- Data ---
        const data = {
            summary: "Visionary Product Executive with 20+ years of experience bridging the gap between clinical data, commercial strategy, and digital transformation. Expert in crafting AI-First product roadmaps that displace incumbents and capture market share. Proven track record of managing $20M+ P&Ls and leading organizations of 75+ professionals.",
            kpis: [
                { label: "P&L Managed", value: "$20M+", icon: "fa-sack-dollar", color: "text-emerald-600", bg: "bg-emerald-100" },
                { label: "Team Size", value: "75+", icon: "fa-users", color: "text-blue-600", bg: "bg-blue-100" },
                { label: "Market Opp ID", value: "$250M", icon: "fa-bullseye", color: "text-purple-600", bg: "bg-purple-100" },
                { label: "Experience", value: "20+ Yrs", icon: "fa-clock", color: "text-amber-600", bg: "bg-amber-100" }
            ],
            strategy: {
                title: "The 'Patient Ready' Initiative",
                problem: "Pharma Commercial Ops teams spent 60% of time cleaning data. Claims data was 6 weeks old (lagging).",
                solution: "Shifted value prop to 'Time-to-Insight'. Used Probabilistic AI Models to pre-link Claims, EHR, and SDOH.",
                impact: "Identified a $250M SOM by offering predictive biomarker alerts (e.g., PD-L1) 6 weeks faster than competitors."
            },
            history: [
                {
                    role: "Senior Product Manager – RWD & Analytics",
                    company: "McKesson",
                    period: "Nov 2024 – Present",
                    desc: "Leading strategic transformation of data portfolio from retrospective reporting to predictive AI intelligence.",
                    bullets: ["Architected 'Patient Ready' product vision.", "Developed 'Disruption Pricing' model (Value Trap).", "Partnered to build global COE."]
                },
                {
                    role: "Senior Product Leader",
                    company: "Optum (UHG)",
                    period: "Nov 2011 – Sept 2024",
                    desc: "Directed enterprise product strategies for consumer engagement, Star Ratings, and Specialty Pharmacy.",
                    bullets: ["Led 'Advocate4Me' AI strategy: +15 NPS increase.", "Moved 80% of membership to 4-Star+ plans.", "Scaled outreach by 428% via AI."]
                },
                {
                    role: "Consulting Partner",
                    company: "Saven Technologies",
                    period: "Feb 2006 – Oct 2011",
                    desc: "Executive leader for Healthcare & Retail practice responsible for P&L and growth.",
                    bullets: ["Managed $20M P&L with $5M annual growth.", "Built team of 75+ professionals.", "Reduced operating costs by 15%."]
                }
            ],
            competencies: [95, 90, 90, 95, 85, 85]
        };

        // --- Renderers ---
        function renderDashboard() {
            document.getElementById('content-area').innerHTML = `
                <div class="fade-in max-w-7xl mx-auto p-6 md:p-12">
                    <div class="mb-12">
                        <h2 class="text-3xl font-bold text-slate-800 mb-4">Executive Command Center</h2>
                        <div class="bg-white p-6 rounded-xl border-l-4 border-blue-600 shadow-sm"><p class="text-lg text-slate-600">${data.summary}</p></div>
                    </div>
                    <div class="grid grid-cols-2 lg:grid-cols-4 gap-6 mb-12">
                        ${data.kpis.map(k => `
                            <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100 flex flex-col items-center text-center">
                                <div class="w-14 h-14 ${k.bg} ${k.color} rounded-full flex items-center justify-center text-2xl mb-4"><i class="fas ${k.icon}"></i></div>
                                <div class="text-3xl font-bold text-slate-800">${k.value}</div>
                                <div class="text-xs font-bold text-slate-400 uppercase tracking-wider">${k.label}</div>
                            </div>
                        `).join('')}
                    </div>
                    <div class="grid lg:grid-cols-2 gap-8">
                        <div class="bg-white p-8 rounded-xl shadow-sm border border-slate-100">
                            <h3 class="text-xl font-bold text-slate-800 mb-2">Competency Profile</h3>
                            <div class="chart-container"><canvas id="radarChart"></canvas></div>
                        </div>
                        <div class="bg-slate-900 text-white p-8 rounded-xl shadow-lg relative overflow-hidden flex flex-col justify-center">
                            <div class="relative z-10">
                                <div class="inline-block px-3 py-1 bg-blue-600 text-xs font-bold rounded-full mb-4">FEATURED CASE STUDY</div>
                                <h3 class="text-3xl font-bold mb-4">The "Patient Ready" Lab</h3>
                                <p class="text-slate-300 mb-8">How we unlocked a $250M market opportunity by solving the "Data Janitor" problem.</p>
                                <button onclick="router('strategy')" class="bg-white text-slate-900 px-6 py-3 rounded-lg font-bold hover:bg-blue-50 transition-colors inline-flex items-center gap-2">View Strategy <i class="fas fa-arrow-right"></i></button>
                            </div>
                        </div>
                    </div>
                </div>`;
            initRadarChart();
        }

        function renderStrategy() {
            document.getElementById('content-area').innerHTML = `
                <div class="fade-in max-w-7xl mx-auto p-6 md:p-12">
                    <button onclick="router('dashboard')" class="text-slate-400 hover:text-blue-600 mb-6 flex items-center gap-2"><i class="fas fa-arrow-left"></i> Back</button>
                    <h2 class="text-3xl font-bold text-slate-800 mb-2">Strategy Lab</h2>
                    <p class="text-slate-500 mb-8">Case Study: McKesson RWD Transformation</p>
                    <div class="grid md:grid-cols-2 gap-8 mb-12">
                        <div class="bg-red-50 p-8 rounded-xl border border-red-100"><h3 class="font-bold text-red-800 mb-2">The Problem</h3><p class="text-red-700">${data.strategy.problem}</p></div>
                        <div class="bg-emerald-50 p-8 rounded-xl border border-emerald-100"><h3 class="font-bold text-emerald-800 mb-2">The Solution</h3><p class="text-emerald-700">${data.strategy.solution}</p></div>
                    </div>
                    <div class="bg-white p-8 rounded-xl shadow-sm border border-slate-100">
                        <h3 class="text-xl font-bold text-slate-800 mb-4">Market Penetration (SOM Analysis)</h3>
                        <div class="plotly-container" id="funnelChart"></div>
                    </div>
                </div>`;
            initFunnelChart();
        }

        function renderExperience() {
            document.getElementById('content-area').innerHTML = `
                <div class="fade-in max-w-5xl mx-auto p-6 md:p-12">
                    <h2 class="text-3xl font-bold text-slate-800 mb-10">Impact Timeline</h2>
                    <div class="space-y-8 border-l-2 border-slate-200 ml-4 pl-8 relative">
                        ${data.history.map((job, idx) => `
                            <div class="bg-white p-8 rounded-xl shadow-sm border border-slate-100 relative">
                                <div class="absolute -left-[41px] top-8 w-4 h-4 bg-white border-4 border-blue-500 rounded-full"></div>
                                <h3 class="text-xl font-bold text-slate-800">${job.role}</h3>
                                <div class="text-slate-500 font-medium mb-4">${job.company} | ${job.period}</div>
                                <p class="text-slate-600 italic mb-4">"${job.desc}"</p>
                                <ul class="space-y-2">${job.bullets.map(b => `<li class="flex gap-2 text-sm text-slate-700"><i class="fas fa-check text-blue-500 mt-1"></i> ${b}</li>`).join('')}</ul>
                            </div>
                        `).join('')}
                    </div>
                </div>`;
        }

        function renderPrintView() {
            document.getElementById('content-area').innerHTML = `
                <div class="max-w-4xl mx-auto p-8 bg-white print-container">
                    <div class="text-center border-b pb-6 mb-8">
                        <h1 class="text-4xl font-bold text-slate-900 mb-2">Atish Banerjee</h1>
                        <p class="text-xl text-blue-600 font-medium">Strategic Product Executive | AI Innovation | Healthcare Transformation</p>
                        <div class="text-slate-500 mt-2">Chicago, IL | ban_atish@yahoo.com | (847) 826-2578</div>
                    </div>
                    <section class="mb-8">
                        <h2 class="text-lg font-bold uppercase tracking-wide text-slate-400 mb-4 border-b pb-1">Professional Summary</h2>
                        <p class="text-slate-800 leading-relaxed">${data.summary}</p>
                    </section>
                    <section class="mb-8">
                        <h2 class="text-lg font-bold uppercase tracking-wide text-slate-400 mb-4 border-b pb-1">Core Competencies</h2>
                        <div class="flex flex-wrap gap-2">
                            ${['Product Strategy', 'P&L Management ($20M)', 'AI/ML Integration', 'Market Penetration', 'RWD Analytics', 'Digital Transformation'].map(s => `<span class="bg-slate-100 px-3 py-1 rounded text-sm font-bold text-slate-700">${s}</span>`).join('')}
                        </div>
                    </section>
                    <section class="mb-8">
                        <h2 class="text-lg font-bold uppercase tracking-wide text-slate-400 mb-4 border-b pb-1">Professional Experience</h2>
                        <div class="space-y-6">
                            ${data.history.map(job => `
                                <div class="print-break">
                                    <div class="flex justify-between items-baseline mb-2">
                                        <h3 class="text-xl font-bold text-slate-900">${job.role}</h3>
                                        <span class="text-slate-600 font-medium">${job.period}</span>
                                    </div>
                                    <div class="text-blue-600 font-medium mb-2">${job.company}</div>
                                    <p class="text-slate-700 mb-2 italic">${job.desc}</p>
                                    <ul class="list-disc list-inside text-slate-700 space-y-1 ml-2">
                                        ${job.bullets.map(b => `<li>${b}</li>`).join('')}
                                    </ul>
                                </div>
                            `).join('')}
                        </div>
                    </section>
                    <div class="no-print mt-8 text-center">
                        <button onclick="window.print()" class="bg-blue-600 text-white px-8 py-3 rounded-lg font-bold hover:bg-blue-700">Print / Save as PDF</button>
                    </div>
                </div>
            `;
        }

        // --- Init & Helpers ---
        function initRadarChart() {
            const ctx = document.getElementById('radarChart');
            if(ctx) new Chart(ctx, { type: 'radar', data: { labels: ["Strategy", "AI/Tech", "Leadership", "Healthcare", "Digital", "GTM"], datasets: [{ label: 'Proficiency', data: data.competencies, backgroundColor: 'rgba(37, 99, 235, 0.2)', borderColor: '#2563eb' }] }, options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { r: { ticks: { display: false } } } } });
        }
        function initFunnelChart() {
            const el = document.getElementById('funnelChart');
            if(el) Plotly.newPlot(el, [{ type: 'funnel', y: ["TAM ($25B)", "SAM ($5B)", "SOM ($250M)"], x: [25000, 5000, 250], textinfo: "value+label" }], { margin: { l: 150, r: 20, t: 20, b: 20 }, showlegend: false }, {displayModeBar: false});
        }
        function router(view) {
            document.querySelectorAll('.nav-item').forEach(el => el.classList.remove('active'));
            const btn = document.getElementById(`nav-${view}`);
            if(btn) btn.classList.add('active');
            
            if(view === 'print') { renderPrintView(); }
            else if(view === 'dashboard') { renderDashboard(); }
            else if(view === 'strategy') { renderStrategy(); }
            else if(view === 'experience') { renderExperience(); }
            
            const menu = document.getElementById('mobile-menu');
            if(menu) menu.classList.add('translate-x-full');
        }
        function toggleMobileMenu() { document.getElementById('mobile-menu').classList.toggle('translate-x-full'); }
        
        // Start
        document.addEventListener('DOMContentLoaded', () => router('dashboard'));
    </script>
</body>
</html>
