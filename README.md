<!DOCTYPE html>
<html lang="en" class="dark scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Aben Wilson | Software Developer Portfolio & Profile</title>
    
    <!-- External CSS Libraries -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        github: {
                            bg: '#0d1117',
                            card: '#161b22',
                            border: '#30363d',
                            accent: '#58a6ff',
                            purple: '#bc8cff',
                            green: '#238636',
                            emerald: '#3fb950',
                            orange: '#d29922',
                            red: '#f85149'
                        }
                    },
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                        mono: ['Fira Code', 'monospace'],
                    }
                }
            }
        }
    </script>
    
    <style>
        body {
            background-color: #0d1117;
            color: #c9d1d9;
            font-family: 'Plus Jakarta Sans', sans-serif;
            overflow-x: hidden;
            -webkit-tap-highlight-color: transparent;
        }

        .bg-grid {
            background-size: 32px 32px;
            background-image: 
                linear-gradient(to right, rgba(255, 255, 255, 0.02) 1px, transparent 1px),
                linear-gradient(to bottom, rgba(255, 255, 255, 0.02) 1px, transparent 1px);
        }

        .glass-panel {
            background: rgba(22, 27, 34, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid #30363d;
        }

        /* Continuous Soft Glowing Red Tail Animation */
        @keyframes tailGlowPulse {
            0%, 100% {
                fill: #ff3b30;
                filter: drop-shadow(0 0 3px rgba(255, 59, 48, 0.8)) drop-shadow(0 0 8px rgba(255, 59, 48, 0.6));
            }
            50% {
                fill: #ff6b6b;
                filter: drop-shadow(0 0 10px rgba(255, 59, 48, 1)) drop-shadow(0 0 16px rgba(255, 107, 107, 0.95));
            }
        }

        .doraemon-glowing-tail {
            animation: tailGlowPulse 1.6s infinite ease-in-out;
        }

        @keyframes speechFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-3px); }
        }

        .speech-anim {
            animation: speechFloat 2.4s ease-in-out infinite;
        }

        ::-webkit-scrollbar { width: 8px; height: 8px; }
        ::-webkit-scrollbar-track { background: #0d1117; }
        ::-webkit-scrollbar-thumb { background: #30363d; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #58a6ff; }
    </style>
</head>
<body class="bg-grid min-h-screen flex flex-col justify-between antialiased selection:bg-github-accent selection:text-slate-950">

    <header class="sticky top-0 z-50 glass-panel border-b border-github-border px-4 lg:px-8 py-3">
        <div class="max-w-6xl mx-auto flex items-center justify-between">
            <a href="#" class="flex items-center space-x-3">
                <div class="w-9 h-9 rounded-xl bg-github-accent/10 border border-github-accent/30 flex items-center justify-center text-github-accent font-mono font-bold text-sm">
                    AW
                </div>
                <div class="flex flex-col">
                    <span class="text-sm font-bold text-white tracking-wide flex items-center gap-2">
                        Aben Wilson
                        <span class="px-2 py-0.5 text-[10px] font-mono rounded-full bg-github-emerald/10 text-github-emerald border border-github-emerald/30 font-semibold">
                            ● Immediate Join
                        </span>
                    </span>
                    <span class="text-[11px] font-mono text-gray-400">Software Developer • MCA</span>
                </div>
            </a>

            <!-- Navigation Links -->
            <nav class="hidden md:flex items-center space-x-6 text-xs font-mono">
                <a href="#about" class="text-gray-300 hover:text-github-accent transition-colors">About</a>
                <a href="#projects" class="text-gray-300 hover:text-github-accent transition-colors">Projects</a>
                <a href="#tech" class="text-gray-300 hover:text-github-accent transition-colors">Tech Stack</a>
                <a href="#education" class="text-gray-300 hover:text-github-accent transition-colors">Education</a>
                <button onclick="toggleMarkdownView()" id="btn-toggle-view" class="px-3.5 py-1.5 rounded-lg bg-github-accent/10 text-github-accent border border-github-accent/30 hover:bg-github-accent hover:text-slate-950 font-bold transition-all flex items-center gap-1.5">
                    <i class="fa-brands fa-markdown"></i> <span>View Markdown Source</span>
                </button>
            </nav>

            <button onclick="toggleMobileNav()" class="md:hidden p-2 rounded-lg bg-github-card border border-github-border text-gray-300">
                <i id="nav-icon" class="fa-solid fa-bars text-sm"></i>
            </button>
        </div>

        <div id="mobile-nav" class="hidden md:hidden border-t border-github-border mt-3 pt-3 space-y-2 text-xs font-mono">
            <a href="#about" onclick="toggleMobileNav()" class="block px-3 py-2 rounded-lg text-gray-300 hover:bg-github-border">About</a>
            <a href="#projects" onclick="toggleMobileNav()" class="block px-3 py-2 rounded-lg text-gray-300 hover:bg-github-border">Projects</a>
            <a href="#tech" onclick="toggleMobileNav()" class="block px-3 py-2 rounded-lg text-gray-300 hover:bg-github-border">Tech Stack</a>
            <a href="#education" onclick="toggleMobileNav()" class="block px-3 py-2 rounded-lg text-gray-300 hover:bg-github-border">Education</a>
            <button onclick="toggleMarkdownView(); toggleMobileNav();" class="w-full text-left px-3 py-2 rounded-lg text-github-accent bg-github-accent/10">Toggle View Mode</button>
        </div>
    </header>

    <main id="main-portfolio" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-12 space-y-16">

        <section id="about" class="relative text-center pt-2">
            <div class="glass-panel rounded-3xl p-6 sm:p-10 border border-github-border relative overflow-hidden shadow-2xl">
                
                <div class="absolute -top-24 left-1/2 -translate-x-1/2 w-96 h-96 bg-github-accent/10 rounded-full blur-3xl pointer-events-none"></div>

                <div class="space-y-4 relative z-10">
                    
                    <!-- Main Name Headline + Cute Resting Anime Doraemon Vector at the End of Wilson -->
                    <h1 class="text-3xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight text-white inline-flex flex-wrap items-center justify-center gap-x-3 gap-y-2">
                        <span>Hi 👋, I'm</span> 
                        <span class="text-github-accent underline decoration-github-accent/40 underline-offset-8 inline-flex items-center gap-1.5">
                            Aben Wilson
                            
                            <!-- Small Resting Doraemon Anime Vector (~48px width) -->
                            <span class="relative inline-block align-bottom ml-1">
                                <!-- Floating "Hi!" Speech Bubble -->
                                <span class="speech-anim absolute -top-7 -right-2 z-20 bg-github-accent text-slate-950 font-extrabold text-[9px] px-1.5 py-0.5 rounded-full shadow-md border border-white flex items-center gap-0.5">
                                    Hi! 👋
                                </span>

                                <!-- Proportional Anime Doraemon Vector -->
                                <svg width="48" height="36" viewBox="0 0 120 90" fill="none" xmlns="http://www.w3.org/2000/svg" class="drop-shadow-md inline-block">
                                    <!-- Tail wire & Animated Glowing Red Tail Node -->
                                    <path d="M18 68 Q10 65 8 50" stroke="#111827" stroke-width="2.5" fill="none" />
                                    <circle class="doraemon-glowing-tail" cx="7" cy="46" r="6" stroke="#111827" stroke-width="1.5" />

                                    <!-- Body (Torso resting on floor) -->
                                    <ellipse cx="45" cy="62" rx="28" ry="18" fill="#0096e6" stroke="#111827" stroke-width="3" />
                                    <ellipse cx="46" cy="62" rx="18" ry="12" fill="#ffffff" stroke="#111827" stroke-width="2" />
                                    <!-- Front Pocket -->
                                    <path d="M36 62 A10 8 0 0 0 56 62 Z" fill="#ffffff" stroke="#111827" stroke-width="2" />

                                    <!-- Feet -->
                                    <ellipse cx="25" cy="74" rx="10" ry="6" fill="#ffffff" stroke="#111827" stroke-width="2" />
                                    <ellipse cx="65" cy="74" rx="10" ry="6" fill="#ffffff" stroke="#111827" stroke-width="2" />

                                    <!-- Red Collar & Bell -->
                                    <path d="M62 48 C72 50 82 50 88 46" stroke="#e53935" stroke-width="5" stroke-linecap="round" />
                                    <circle cx="75" cy="51" r="5" fill="#ffd700" stroke="#111827" stroke-width="1.5" />

                                    <!-- Head -->
                                    <circle cx="85" cy="36" r="26" fill="#0096e6" stroke="#111827" stroke-width="3" />
                                    <ellipse cx="88" cy="39" rx="20" ry="18" fill="#ffffff" stroke="#111827" stroke-width="2" />

                                    <!-- Relaxed/Smiling Eyes -->
                                    <ellipse cx="80" cy="28" rx="5" ry="7" fill="#ffffff" stroke="#111827" stroke-width="1.5" />
                                    <ellipse cx="91" cy="28" rx="5" ry="7" fill="#ffffff" stroke="#111827" stroke-width="1.5" />
                                    <path d="M78 28 Q80 25 82 28" stroke="#111827" stroke-width="2" fill="none" />
                                    <path d="M89 28 Q91 25 93 28" stroke="#111827" stroke-width="2" fill="none" />

                                    <!-- Nose & Whiskers -->
                                    <circle cx="85" cy="33" r="3.5" fill="#e53935" stroke="#111827" stroke-width="1" />
                                    <line x1="85" y1="36.5" x2="85" y2="44" stroke="#111827" stroke-width="1.5" />
                                    <line x1="68" y1="36" x2="76" y2="37" stroke="#111827" stroke-width="1.5" />
                                    <line x1="67" y1="40" x2="76" y2="40" stroke="#111827" stroke-width="1.5" />
                                    <line x1="94" y1="37" x2="102" y2="36" stroke="#111827" stroke-width="1.5" />
                                    <line x1="94" y1="40" x2="103" y2="40" stroke="#111827" stroke-width="1.5" />

                                    <!-- Smile -->
                                    <path d="M76 43 Q85 50 94 43" stroke="#111827" stroke-width="1.5" fill="none" />
                                </svg>
                            </span>
                        </span>
                    </h1>

                    <p class="text-sm sm:text-lg font-mono text-github-purple font-medium max-w-2xl mx-auto">
                        💻 MCA Student • Full-Stack • Mobile • Cloud Developer
                    </p>

                    <p class="text-xs sm:text-sm text-gray-300 font-light max-w-xl mx-auto leading-relaxed">
                        Building practical, robust digital products from concept to deployment with full-stack and cloud technologies.
                    </p>
                </div>

                <!-- Contact & Social Badges -->
                <div class="mt-6 flex flex-wrap items-center justify-center gap-2.5 sm:gap-3 text-xs font-mono">
                    <a href="https://www.linkedin.com/in/aben-wilson-11601a348" target="_blank" 
                       class="px-4 py-2 rounded-xl bg-[#0A66C2]/20 text-[#0A66C2] border border-[#0A66C2]/40 hover:bg-[#0A66C2] hover:text-white transition-all flex items-center gap-2 font-semibold">
                        <i class="fa-brands fa-linkedin text-sm"></i>
                        <span>LinkedIn</span>
                    </a>

                    <a href="mailto:abenwilson1@gmail.com" 
                       class="px-4 py-2 rounded-xl bg-[#EA4335]/20 text-[#EA4335] border border-[#EA4335]/40 hover:bg-[#EA4335] hover:text-white transition-all flex items-center gap-2 font-semibold">
                        <i class="fa-solid fa-envelope text-sm"></i>
                        <span>Email</span>
                    </a>

                    <a href="https://github.com/Abenwilson" target="_blank" 
                       class="px-4 py-2 rounded-xl bg-github-border text-white border border-gray-600 hover:bg-gray-700 transition-all flex items-center gap-2 font-semibold">
                        <i class="fa-brands fa-github text-sm"></i>
                        <span>GitHub</span>
                    </a>
                </div>

                <!-- Development Workflow Pipeline -->
                <div class="mt-8 pt-6 border-t border-github-border/60">
                    <div class="inline-flex flex-wrap items-center justify-center gap-2 sm:gap-4 text-[11px] sm:text-xs font-mono bg-github-bg/90 px-5 py-2.5 rounded-2xl border border-github-border text-gray-300">
                        <span class="text-github-accent font-bold">💡 Think</span>
                        <span class="text-gray-600">→</span>
                        <span class="text-github-purple font-bold">🛠️ Build</span>
                        <span class="text-gray-600">→</span>
                        <span class="text-github-orange font-bold">🧪 Improve</span>
                        <span class="text-gray-600">→</span>
                        <span class="text-github-emerald font-bold">🚀 Deploy</span>
                    </div>
                </div>

            </div>
        </section>

        <section id="projects" class="space-y-6">
            <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-2 border-b border-github-border pb-3">
                <div>
                    <span class="text-xs font-mono text-github-purple">💼 FEATURED PROJECTS</span>
                    <h2 class="text-2xl sm:text-3xl font-bold text-white mt-0.5">Projects & Showcase</h2>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- KickPro -->
                <div class="glass-panel rounded-2xl p-5 border border-github-border flex flex-col justify-between space-y-4 hover:border-github-accent/50 transition-all">
                    <div class="space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="px-2.5 py-1 rounded-md bg-github-emerald/10 text-github-emerald border border-github-emerald/30 text-xs font-mono font-bold">⚽ KickPro</span>
                            <span class="text-[10px] font-mono text-gray-400">Web App</span>
                        </div>
                        <h3 class="text-lg font-bold text-white">Football Management Platform</h3>
                        <p class="text-xs text-gray-300 leading-relaxed">
                            Connects players, coaches, scouts, clubs, and tournaments in a unified scouting ecosystem.
                        </p>
                    </div>
                    <div class="flex flex-wrap gap-1.5 text-[10px] font-mono pt-2 border-t border-github-border/60">
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-accent border border-github-border">JavaScript</span>
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-accent border border-github-border">Node.js</span>
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-accent border border-github-border">Supabase</span>
                    </div>
                </div>

                <!-- CreatorBridge -->
                <div class="glass-panel rounded-2xl p-5 border border-github-border flex flex-col justify-between space-y-4 hover:border-github-accent/50 transition-all">
                    <div class="space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="px-2.5 py-1 rounded-md bg-github-accent/10 text-github-accent border border-github-accent/30 text-xs font-mono font-bold">🎬 CreatorBridge</span>
                            <span class="text-[10px] font-mono text-gray-400">Mobile App</span>
                        </div>
                        <h3 class="text-lg font-bold text-white">Creator & Editor Network</h3>
                        <p class="text-xs text-gray-300 leading-relaxed">
                            Mobile platform enabling content creators to hire, message, and collaborate with video editors.
                        </p>
                    </div>
                    <div class="flex flex-wrap gap-1.5 text-[10px] font-mono pt-2 border-t border-github-border/60">
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-purple border border-github-border">Flutter</span>
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-purple border border-github-border">Firebase</span>
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-purple border border-github-border">BLoC</span>
                    </div>
                </div>

                <!-- ShareCycle -->
                <div class="glass-panel rounded-2xl p-5 border border-github-border flex flex-col justify-between space-y-4 hover:border-github-accent/50 transition-all">
                    <div class="space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="px-2.5 py-1 rounded-md bg-github-orange/10 text-github-orange border border-github-orange/30 text-xs font-mono font-bold">♻️ ShareCycle</span>
                            <span class="text-[10px] font-mono text-gray-400">Full-Stack</span>
                        </div>
                        <h3 class="text-lg font-bold text-white">Household Item Reuse</h3>
                        <p class="text-xs text-gray-300 leading-relaxed">
                            Community platform for re-using household items with messaging and pickup tracking.
                        </p>
                    </div>
                    <div class="flex flex-wrap gap-1.5 text-[10px] font-mono pt-2 border-t border-github-border/60">
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-orange border border-github-border">PHP</span>
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-orange border border-github-border">MySQL</span>
                        <span class="px-2 py-0.5 rounded bg-github-bg text-github-orange border border-github-border">JS</span>
                    </div>
                </div>
            </div>
        </section>

        <section id="tech" class="space-y-6">
            <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-3 border-b border-github-border pb-3">
                <div>
                    <span class="text-xs font-mono text-github-emerald">🧑‍💻 TECH STACK</span>
                    <h2 class="text-2xl sm:text-3xl font-bold text-white mt-0.5">Skills & Tools</h2>
                </div>

                <div class="flex items-center space-x-1.5 overflow-x-auto text-xs font-mono pb-1">
                    <button onclick="filterTech('all')" id="btn-all" class="px-3 py-1.5 rounded-lg bg-github-accent text-slate-950 font-bold">All</button>
                    <button onclick="filterTech('mobile')" id="btn-mobile" class="px-3 py-1.5 rounded-lg bg-github-card text-gray-300 border border-github-border">Mobile</button>
                    <button onclick="filterTech('backend')" id="btn-backend" class="px-3 py-1.5 rounded-lg bg-github-card text-gray-300 border border-github-border">Backend</button>
                    <button onclick="filterTech('database')" id="btn-database" class="px-3 py-1.5 rounded-lg bg-github-card text-gray-300 border border-github-border">Databases</button>
                </div>
            </div>

            <div class="glass-panel rounded-2xl p-6 border border-github-border">
                <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 text-xs font-mono">
                    <div class="tech-card mobile p-3 rounded-xl bg-github-bg border border-github-border flex items-center gap-3">
                        <i class="fa-solid fa-mobile-screen text-sky-400 text-lg"></i>
                        <div><div class="text-white font-bold">Flutter</div><div class="text-[10px] text-gray-400">Dart</div></div>
                    </div>
                    <div class="tech-card backend p-3 rounded-xl bg-github-bg border border-github-border flex items-center gap-3">
                        <i class="fa-brands fa-python text-yellow-400 text-lg"></i>
                        <div><div class="text-white font-bold">Python</div><div class="text-[10px] text-gray-400">Backend</div></div>
                    </div>
                    <div class="tech-card backend p-3 rounded-xl bg-github-bg border border-github-border flex items-center gap-3">
                        <i class="fa-brands fa-php text-indigo-400 text-lg"></i>
                        <div><div class="text-white font-bold">PHP</div><div class="text-[10px] text-gray-400">Web Backend</div></div>
                    </div>
                    <div class="tech-card mobile backend p-3 rounded-xl bg-github-bg border border-github-border flex items-center gap-3">
                        <i class="fa-brands fa-js text-yellow-300 text-lg"></i>
                        <div><div class="text-white font-bold">JavaScript</div><div class="text-[10px] text-gray-400">Node.js</div></div>
                    </div>
                    <div class="tech-card backend p-3 rounded-xl bg-github-bg border border-github-border flex items-center gap-3">
                        <i class="fa-solid fa-fire text-amber-500 text-lg"></i>
                        <div><div class="text-white font-bold">Firebase</div><div class="text-[10px] text-gray-400">BaaS</div></div>
                    </div>
                    <div class="tech-card database backend p-3 rounded-xl bg-github-bg border border-github-border flex items-center gap-3">
                        <i class="fa-solid fa-bolt text-emerald-400 text-lg"></i>
                        <div><div class="text-white font-bold">Supabase</div><div class="text-[10px] text-gray-400">PostgreSQL</div></div>
                    </div>
                    <div class="tech-card database p-3 rounded-xl bg-github-bg border border-github-border flex items-center gap-3">
                        <i class="fa-solid fa-database text-blue-400 text-lg"></i>
                        <div><div class="text-white font-bold">MySQL</div><div class="text-[10px] text-gray-400">RDBMS</div></div>
                    </div>
                    <div class="tech-card database p-3 rounded-xl bg-github-bg border border-github-border flex items-center gap-3">
                        <i class="fa-solid fa-leaf text-emerald-500 text-lg"></i>
                        <div><div class="text-white font-bold">MongoDB</div><div class="text-[10px] text-gray-400">NoSQL</div></div>
                    </div>
                </div>
            </div>
        </section>

        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">
            <section id="education" class="lg:col-span-5 space-y-6">
                <div class="border-b border-github-border pb-3">
                    <span class="text-xs font-mono text-github-orange">🎓 ACADEMIC</span>
                    <h2 class="text-2xl font-bold text-white mt-0.5">Education</h2>
                </div>

                <div class="glass-panel rounded-2xl p-6 border border-github-border space-y-6 relative">
                    <div class="absolute left-9 top-10 bottom-10 w-0.5 bg-github-border"></div>

                    <div class="relative flex items-start space-x-4">
                        <div class="w-7 h-7 rounded-full bg-github-accent text-slate-950 font-black flex items-center justify-center text-xs z-10">1</div>
                        <div>
                            <span class="px-2 py-0.5 text-[10px] font-mono rounded bg-github-accent/10 text-github-accent border border-github-accent/30 font-semibold">Pursuing</span>
                            <h3 class="text-base font-bold text-white mt-1">MCA (Master of Computer Applications)</h3>
                            <p class="text-xs text-gray-400 font-mono">2025 - 2027</p>
                        </div>
                    </div>

                    <div class="relative flex items-start space-x-4">
                        <div class="w-7 h-7 rounded-full bg-github-card text-gray-300 border border-github-border font-bold flex items-center justify-center text-xs z-10">2</div>
                        <div>
                            <span class="px-2 py-0.5 text-[10px] font-mono rounded bg-github-emerald/10 text-github-emerald border border-github-emerald/30 font-semibold">Graduated</span>
                            <h3 class="text-base font-bold text-white mt-1">BCA (Bachelor of Computer Applications)</h3>
                            <p class="text-xs text-gray-400 font-mono">Graduated 2025</p>
                        </div>
                    </div>
                </div>
            </section>

            <section class="lg:col-span-7 space-y-6">
                <div class="border-b border-github-border pb-3">
                    <span class="text-xs font-mono text-github-purple">📊 ACTIVITY</span>
                    <h2 class="text-2xl font-bold text-white mt-0.5">GitHub Stats</h2>
                </div>

                <div class="glass-panel rounded-2xl p-6 border border-github-border space-y-4 text-center">
                    <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                        <img src="https://github-readme-stats.vercel.app/api?username=Abenwilson&show_icons=true&hide_border=true&theme=tokyonight&count_private=true" alt="Aben Wilson GitHub Stats" class="h-36 rounded-lg">
                        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Abenwilson&layout=compact&hide_border=true&theme=tokyonight" alt="Top Languages" class="h-36 rounded-lg">
                    </div>
                </div>
            </section>
        </div>

    </main>

    <main id="markdown-container" class="hidden max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-12">
        <div class="space-y-4">
            <div class="flex items-center justify-between border-b border-github-border pb-3">
                <h2 class="text-2xl font-bold text-white">Raw Markdown README Source</h2>
                <button onclick="copyMarkdownCode()" class="px-4 py-2 rounded-lg bg-github-accent text-slate-950 font-bold text-xs font-mono hover:bg-sky-400 transition-all flex items-center gap-2">
                    <i class="fa-regular fa-copy"></i>
                    <span id="copy-status">Copy Markdown</span>
                </button>
            </div>

            <div class="glass-panel rounded-2xl border border-github-border overflow-hidden">
                <pre class="p-6 bg-github-bg text-gray-300 font-mono text-xs overflow-x-auto leading-relaxed"><code id="raw-markdown-code">
&lt;div align="center"&gt;

&lt;h1&gt;Hi 👋, I'm &lt;span style="color:#58A6FF;"&gt;Aben Wilson&lt;/span&gt;&lt;/h1&gt;

&lt;h3&gt;💻 Software Developer • Full-Stack • Mobile • Cloud&lt;/h3&gt;

&lt;p&gt;Building ideas into useful digital experiences.&lt;/p&gt;

&lt;p&gt;
  &lt;a href="https://www.linkedin.com/in/aben-wilson-11601a348" target="_blank"&gt;
    &lt;img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white" /&gt;
  &lt;/a&gt;
  &lt;a href="mailto:abenwilson1@gmail.com"&gt;
    &lt;img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&amp;logo=gmail&amp;logoColor=white" /&gt;
  &lt;/a&gt;
  &lt;a href="https://github.com/Abenwilson" target="_blank"&gt;
    &lt;img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&amp;logo=github&amp;logoColor=white" /&gt;
  &lt;/a&gt;
&lt;/p&gt;

&lt;/div&gt;

---

## 🚀 About Me

I'm an **MCA student and passionate Software Developer** who enjoys turning ideas into practical, user-friendly applications.

```text
💡 Think → 🛠️ Build → 🧪 Improve → 🚀 Deploy
```
                </code></pre>
            </div>
        </div>
    </main>

    <footer class="mt-16 border-t border-github-border glass-panel py-8 text-center text-xs font-mono text-gray-400">
        <div class="max-w-6xl mx-auto px-4 space-y-2">
            <p class="text-white font-semibold">
                🟢 Available for Immediate Joining • Open to Software Development Opportunities
            </p>
            <p>
                💙 Let's Build Something Great Together • LEARN • BUILD • CREATE • GROW
            </p>
        </div>
    </footer>

    <script>
        function toggleMobileNav() {
            const nav = document.getElementById('mobile-nav');
            const icon = document.getElementById('nav-icon');
            nav.classList.toggle('hidden');
            icon.className = nav.classList.contains('hidden') ? "fa-solid fa-bars text-sm" : "fa-solid fa-xmark text-sm";
        }

        function toggleMarkdownView() {
            const mainPortfolio = document.getElementById('main-portfolio');
            const markdownContainer = document.getElementById('markdown-container');
            const btn = document.getElementById('btn-toggle-view');

            if (markdownContainer.classList.contains('hidden')) {
                mainPortfolio.classList.add('hidden');
                markdownContainer.classList.remove('hidden');
                btn.innerHTML = `<i class="fa-solid fa-desktop"></i> <span>View Live Portfolio</span>`;
            } else {
                markdownContainer.classList.add('hidden');
                mainPortfolio.classList.remove('hidden');
                btn.innerHTML = `<i class="fa-brands fa-markdown"></i> <span>View Markdown Source</span>`;
            }
        }

        function filterTech(category) {
            const cards = document.querySelectorAll('.tech-card');
            const buttons = ['all', 'mobile', 'backend', 'database'];

            buttons.forEach(btn => {
                const btnEl = document.getElementById(`btn-${btn}`);
                if (btn === category) {
                    btnEl.className = "px-3 py-1.5 rounded-lg bg-github-accent text-slate-950 font-bold";
                } else {
                    btnEl.className = "px-3 py-1.5 rounded-lg bg-github-card text-gray-300 border border-github-border";
                }
            });

            cards.forEach(card => {
                if (category === 'all' || card.classList.contains(category)) {
                    card.style.display = 'flex';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        function copyMarkdownCode() {
            const codeText = document.getElementById('raw-markdown-code').innerText;
            const tempTextArea = document.createElement('textarea');
            tempTextArea.value = codeText;
            document.body.appendChild(tempTextArea);
            tempTextArea.select();
            document.execCommand('copy');
            document.body.removeChild(tempTextArea);

            const statusEl = document.getElementById('copy-status');
            statusEl.textContent = "Copied!";
            setTimeout(() => {
                statusEl.textContent = "Copy Markdown";
            }, 2000);
        }
    </script>
</body>
</html>
