<!DOCTYPE html>
<html lang="en" class="scroll-smooth dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saicharan K. | Portfolio</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        darkBg: '#090d16',
                        cardBg: '#111827',
                        accentBlue: '#3b82f6',
                        accentCyan: '#06b6d4',
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #090d16;
            color: #f3f4f6;
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #090d16;
        }
        ::-webkit-scrollbar-thumb {
            background: #1f2937;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #374151;
        }
    </style>
</head>
<body class="bg-[#090d16] text-gray-100 selection:bg-blue-500 selection:text-white">

    <!-- Sticky Navbar -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-[#090d16]/80 backdrop-blur-md border-b border-gray-800/60 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <a href="#hero" class="text-xl font-extrabold tracking-tight bg-gradient-to-r from-blue-400 via-cyan-400 to-indigo-500 bg-clip-text text-transparent flex items-center gap-2">
                <i class="fa-solid fa-code text-blue-400"></i> Saicharan K.
            </a>
            
            <!-- Desktop Menu -->
            <nav class="hidden md:flex items-center space-x-8 text-sm font-medium text-gray-300">
                <a href="#about" class="hover:text-blue-400 transition-colors">About</a>
                <a href="#skills" class="hover:text-blue-400 transition-colors">Skills</a>
                <a href="#projects" class="hover:text-blue-400 transition-colors">Projects</a>
                <a href="#certifications" class="hover:text-blue-400 transition-colors">Certifications</a>
                <a href="#contact" class="hover:text-blue-400 transition-colors">Contact</a>
            </nav>

            <div class="hidden md:flex items-center space-x-4">
                <a href="#contact" class="px-5 py-2.5 rounded-full text-sm font-semibold text-white bg-gradient-to-r from-blue-600 to-cyan-500 hover:from-blue-500 hover:to-cyan-400 shadow-lg shadow-blue-500/25 transition-all duration-300 transform hover:-translate-y-0.5">
                    Let's Talk
                </a>
            </div>

            <!-- Mobile Menu Button -->
            <button id="mobile-menu-btn" aria-label="Toggle Navigation" class="md:hidden text-gray-300 hover:text-white focus:outline-none p-2 rounded-lg bg-gray-900 border border-gray-800">
                <i class="fa-solid fa-bars text-xl"></i>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden bg-[#0b101d] border-b border-gray-800 px-6 pt-4 pb-6 space-y-3 shadow-xl">
            <a href="#about" class="block text-gray-300 hover:text-blue-400 font-medium py-2 mobile-link">About</a>
            <a href="#skills" class="block text-gray-300 hover:text-blue-400 font-medium py-2 mobile-link">Skills</a>
            <a href="#projects" class="block text-gray-300 hover:text-blue-400 font-medium py-2 mobile-link">Projects</a>
            <a href="#certifications" class="block text-gray-300 hover:text-blue-400 font-medium py-2 mobile-link">Certifications</a>
            <a href="#contact" class="block text-gray-300 hover:text-blue-400 font-medium py-2 mobile-link">Contact</a>
            <div class="pt-2">
                <a href="#contact" class="block text-center w-full px-5 py-2.5 rounded-xl text-sm font-semibold text-white bg-gradient-to-r from-blue-600 to-cyan-500 shadow-md">
                    Let's Talk
                </a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="hero" class="relative min-h-screen flex items-center justify-center pt-28 pb-16 px-4 sm:px-6 lg:px-8 overflow-hidden">
        <!-- Background Glow Orbs -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[350px] sm:w-[500px] h-[350px] sm:h-[500px] bg-blue-600/20 rounded-full blur-[120px] pointer-events-none"></div>
        <div class="absolute bottom-10 right-10 w-[300px] h-[300px] bg-cyan-600/15 rounded-full blur-[100px] pointer-events-none"></div>

        <div class="max-w-4xl mx-auto text-center relative z-10">
            <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-blue-950/60 border border-blue-800/50 text-blue-400 text-xs sm:text-sm font-medium mb-8 backdrop-blur-sm animate-pulse">
                <span class="w-2 h-2 rounded-full bg-blue-400"></span>
                J.N.N Institute of Engineering • CSE Undergraduate
            </div>
            
            <h1 class="text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight text-white mb-6">
                Hi, I'm <span class="bg-gradient-to-r from-blue-400 via-cyan-400 to-indigo-400 bg-clip-text text-transparent">Saicharan K.</span>
            </h1>
            
            <p class="text-lg sm:text-xl text-gray-300 font-medium max-w-2xl mx-auto mb-10 leading-relaxed">
                Undergraduate Computer Science & Engineering Student | Full-Stack Developer & AI Integrator bridging modern frontend interfaces with robust backend systems.
            </p>
            
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                <a href="#projects" class="w-full sm:w-auto px-8 py-4 rounded-xl text-base font-semibold text-white bg-blue-600 hover:bg-blue-500 shadow-lg shadow-blue-600/30 transition-all duration-300 flex items-center justify-center gap-2 transform hover:-translate-y-0.5">
                    <span>View Projects</span>
                    <i class="fa-solid fa-arrow-down text-sm"></i>
                </a>
                <a href="#contact" class="w-full sm:w-auto px-8 py-4 rounded-xl text-base font-semibold text-gray-300 bg-gray-900/80 hover:bg-gray-800 border border-gray-800 hover:border-gray-700 transition-all duration-300 flex items-center justify-center gap-2">
                    <span>Contact Me</span>
                    <i class="fa-regular fa-envelope text-sm"></i>
                </a>
            </div>

            <!-- Quick Social Bar -->
            <div class="mt-14 flex items-center justify-center gap-6 text-gray-400">
                <a href="https://github.com" target="_blank" rel="noopener noreferrer" aria-label="GitHub Profile" class="w-11 h-11 rounded-xl bg-gray-900/90 border border-gray-800 flex items-center justify-center hover:text-white hover:border-blue-500/50 hover:bg-gray-800 transition-all">
                    <i class="fa-brands fa-github text-lg"></i>
                </a>
                <a href="https://linkedin.com" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn Profile" class="w-11 h-11 rounded-xl bg-gray-900/90 border border-gray-800 flex items-center justify-center hover:text-white hover:border-blue-500/50 hover:bg-gray-800 transition-all">
                    <i class="fa-brands fa-linkedin-in text-lg"></i>
                </a>
                <a href="mailto:contact@saicharan.dev" aria-label="Email Me" class="w-11 h-11 rounded-xl bg-gray-900/90 border border-gray-800 flex items-center justify-center hover:text-white hover:border-blue-500/50 hover:bg-gray-800 transition-all">
                    <i class="fa-solid fa-envelope text-lg"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-24 px-4 sm:px-6 lg:px-8 bg-[#0b101d]/60 border-t border-gray-900">
        <div class="max-w-5xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-blue-400 mb-3">About Me</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Engineering Intelligent Digital Solutions</h3>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-center">
                <div class="md:col-span-1 bg-gray-900/80 border border-gray-800 p-8 rounded-2xl text-center relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-32 h-32 bg-blue-500/10 rounded-full blur-2xl group-hover:bg-blue-500/20 transition-all"></div>
                    <div class="w-24 h-24 mx-auto mb-6 rounded-2xl bg-gradient-to-tr from-blue-600 to-cyan-500 flex items-center justify-center text-white text-3xl font-extrabold shadow-lg shadow-blue-500/30">
                        SK
                    </div>
                    <h4 class="text-xl font-bold text-white mb-1">Saicharan K.</h4>
                    <p class="text-sm text-blue-400 font-medium mb-3">CSE Undergraduate</p>
                    <p class="text-xs text-gray-400">J.N.N Institute of Engineering, Tamil Nadu</p>
                </div>

                <div class="md:col-span-2 bg-gray-900/60 border border-gray-800/80 p-8 sm:p-10 rounded-2xl leading-relaxed text-gray-300">
                    <p class="text-base sm:text-lg mb-6">
                        Motivated and detail-oriented Computer Science undergraduate with hands-on experience building full-stack web applications, integrating multimodal artificial intelligence pipelines, and developing automated workflow solutions.
                    </p>
                    <p class="text-base sm:text-lg text-gray-400 mb-6">
                        Adept at bridging modern frontend interfaces with robust backend architectures, focusing on practical, user-centric deployments across health-tech, travel, and communication domains.
                    </p>
                    <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 pt-4 border-t border-gray-800">
                        <div>
                            <span class="block text-2xl font-extrabold text-white">3+</span>
                            <span class="text-xs text-gray-400">Core Projects</span>
                        </div>
                        <div>
                            <span class="block text-2xl font-extrabold text-white">SIH</span>
                            <span class="text-xs text-gray-400">National Finalist Experience</span>
                        </div>
                        <div>
                            <span class="block text-2xl font-extrabold text-white">AI/Full-Stack</span>
                            <span class="text-xs text-gray-400">Specialization Focus</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills & Expertise Section -->
    <section id="skills" class="py-24 px-4 sm:px-6 lg:px-8 border-t border-gray-900">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-blue-400 mb-3">Expertise</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Skills & Technical Stack</h3>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Card 1: Languages -->
                <div class="bg-gray-900/60 border border-gray-800 hover:border-gray-700 p-6 rounded-2xl transition-all duration-300 group hover:-translate-y-1">
                    <div class="w-12 h-12 rounded-xl bg-blue-500/10 border border-blue-500/20 flex items-center justify-center text-blue-400 mb-5 group-hover:bg-blue-500 group-hover:text-white transition-all">
                        <i class="fa-solid fa-code text-lg"></i>
                    </div>
                    <h4 class="text-lg font-bold text-white mb-3">Languages</h4>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Python</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">JavaScript</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">TypeScript</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Java</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">C</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">8086 Assembly</span>
                    </div>
                </div>

                <!-- Card 2: Frontend & Styling -->
                <div class="bg-gray-900/60 border border-gray-800 hover:border-gray-700 p-6 rounded-2xl transition-all duration-300 group hover:-translate-y-1">
                    <div class="w-12 h-12 rounded-xl bg-cyan-500/10 border border-cyan-500/20 flex items-center justify-center text-cyan-400 mb-5 group-hover:bg-cyan-500 group-hover:text-white transition-all">
                        <i class="fa-solid fa-laptop-code text-lg"></i>
                    </div>
                    <h4 class="text-lg font-bold text-white mb-3">Frontend & Styling</h4>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">React</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Next.js</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Tailwind CSS</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Bootstrap</span>
                    </div>
                </div>

                <!-- Card 3: Backend & APIs -->
                <div class="bg-gray-900/60 border border-gray-800 hover:border-gray-700 p-6 rounded-2xl transition-all duration-300 group hover:-translate-y-1">
                    <div class="w-12 h-12 rounded-xl bg-indigo-500/10 border border-indigo-500/20 flex items-center justify-center text-indigo-400 mb-5 group-hover:bg-indigo-500 group-hover:text-white transition-all">
                        <i class="fa-solid fa-server text-lg"></i>
                    </div>
                    <h4 class="text-lg font-bold text-white mb-3">Backend & APIs</h4>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Node.js</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Express</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">FastAPI</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">WhatsApp Cloud API</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Twilio</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">n8n Webhooks</span>
                    </div>
                </div>

                <!-- Card 4: Databases -->
                <div class="bg-gray-900/60 border border-gray-800 hover:border-gray-700 p-6 rounded-2xl transition-all duration-300 group hover:-translate-y-1">
                    <div class="w-12 h-12 rounded-xl bg-emerald-500/10 border border-emerald-500/20 flex items-center justify-center text-emerald-400 mb-5 group-hover:bg-emerald-500 group-hover:text-white transition-all">
                        <i class="fa-solid fa-database text-lg"></i>
                    </div>
                    <h4 class="text-lg font-bold text-white mb-3">Databases</h4>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">MongoDB</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">PostgreSQL</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">SQLite</span>
                    </div>
                </div>

                <!-- Card 5: AI & Tooling -->
                <div class="bg-gray-900/60 border border-gray-800 hover:border-gray-700 p-6 rounded-2xl transition-all duration-300 group hover:-translate-y-1 md:col-span-2 lg:col-span-2">
                    <div class="w-12 h-12 rounded-xl bg-amber-500/10 border border-amber-500/20 flex items-center justify-center text-amber-400 mb-5 group-hover:bg-amber-500 group-hover:text-white transition-all">
                        <i class="fa-solid fa-brain text-lg"></i>
                    </div>
                    <h4 class="text-lg font-bold text-white mb-3">AI & Tooling</h4>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Google Gemini API</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Bhashini ULCA APIs</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Ollama (Qwen2.5-Coder)</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Git & GitHub</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">GitHub Copilot</span>
                        <span class="px-3 py-1 rounded-lg bg-gray-800/80 text-gray-300 text-xs font-medium border border-gray-700/60">Continue / VS Code</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-24 px-4 sm:px-6 lg:px-8 bg-[#0b101d]/60 border-t border-gray-900">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-blue-400 mb-3">Portfolio</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Featured Key Projects</h3>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <!-- Project 1: CareIntake -->
                <div class="bg-gray-900/80 border border-gray-800 rounded-2xl overflow-hidden flex flex-col justify-between hover:border-blue-500/50 transition-all duration-300 group">
                    <div class="p-8">
                        <div class="flex items-center justify-between mb-6">
                            <span class="px-3 py-1 rounded-full bg-blue-950 border border-blue-800 text-blue-400 text-xs font-semibold">SIH 2026</span>
                            <i class="fa-solid fa-hospital-user text-2xl text-blue-400 group-hover:scale-110 transition-transform"></i>
                        </div>
                        <h4 class="text-xl font-bold text-white mb-3">CareIntake Platform</h4>
                        <p class="text-gray-300 text-sm leading-relaxed mb-6">
                            An AI-powered pre-consultation medical history platform featuring voice and touch interfaces, OCR document parsing, AYUSH diagnostic mode, and an offline decision tree inference engine.
                        </p>
                        <div class="flex flex-wrap gap-2 mb-6">
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">React</span>
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">FastAPI</span>
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">Gemini API</span>
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">OCR</span>
                        </div>
                    </div>
                    <div class="px-8 py-4 bg-gray-950/60 border-t border-gray-800/80 flex items-center justify-between">
                        <span class="text-xs text-gray-400 font-medium">Health-Tech Innovation</span>
                        <a href="#contact" class="text-xs font-semibold text-blue-400 hover:text-blue-300 flex items-center gap-1">
                            <span>Inquire</span>
                            <i class="fa-solid fa-arrow-right text-[10px]"></i>
                        </a>
                    </div>
                </div>

                <!-- Project 2: Travel Website -->
                <div class="bg-gray-900/80 border border-gray-800 rounded-2xl overflow-hidden flex flex-col justify-between hover:border-cyan-500/50 transition-all duration-300 group">
                    <div class="p-8">
                        <div class="flex items-center justify-between mb-6">
                            <span class="px-3 py-1 rounded-full bg-cyan-950 border border-cyan-800 text-cyan-400 text-xs font-semibold">Internship Project</span>
                            <i class="fa-solid fa-plane-departure text-2xl text-cyan-400 group-hover:scale-110 transition-transform"></i>
                        </div>
                        <h4 class="text-xl font-bold text-white mb-3">Travel Booking Platform</h4>
                        <p class="text-gray-300 text-sm leading-relaxed mb-6">
                            Designed and engineered a full-stack travel booking platform leveraging React for dynamic user interactions and Node.js for backend server handling and booking data management.
                        </p>
                        <div class="flex flex-wrap gap-2 mb-6">
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">React</span>
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">Node.js</span>
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">Express</span>
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">MongoDB</span>
                        </div>
                    </div>
                    <div class="px-8 py-4 bg-gray-950/60 border-t border-gray-800/80 flex items-center justify-between">
                        <span class="text-xs text-gray-400 font-medium">J.N.N Internship</span>
                        <a href="#contact" class="text-xs font-semibold text-cyan-400 hover:text-cyan-300 flex items-center gap-1">
                            <span>Inquire</span>
                            <i class="fa-solid fa-arrow-right text-[10px]"></i>
                        </a>
                    </div>
                </div>

                <!-- Project 3: WhatsApp Prescription Dispatcher -->
                <div class="bg-gray-900/80 border border-gray-800 rounded-2xl overflow-hidden flex flex-col justify-between hover:border-indigo-500/50 transition-all duration-300 group">
                    <div class="p-8">
                        <div class="flex items-center justify-between mb-6">
                            <span class="px-3 py-1 rounded-full bg-indigo-950 border border-indigo-800 text-indigo-400 text-xs font-semibold">Automation</span>
                            <i class="fa-brands fa-whatsapp text-2xl text-indigo-400 group-hover:scale-110 transition-transform"></i>
                        </div>
                        <h4 class="text-xl font-bold text-white mb-3">Prescription Dispatcher</h4>
                        <p class="text-gray-300 text-sm leading-relaxed mb-6">
                            Built an automated backend workflow using Express and the WhatsApp Cloud API to securely dispatch digital prescriptions and PDF medical attachments directly to patients.
                        </p>
                        <div class="flex flex-wrap gap-2 mb-6">
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">Express</span>
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">WhatsApp Cloud API</span>
                            <span class="px-2.5 py-1 rounded-md bg-gray-800 text-gray-300 text-xs font-medium">n8n</span>
                        </div>
                    </div>
                    <div class="px-8 py-4 bg-gray-950/60 border-t border-gray-800/80 flex items-center justify-between">
                        <span class="text-xs text-gray-400 font-medium">Automated Workflow</span>
                        <a href="#contact" class="text-xs font-semibold text-indigo-400 hover:text-indigo-300 flex items-center gap-1">
                            <span>Inquire</span>
                            <i class="fa-solid fa-arrow-right text-[10px]"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section id="certifications" class="py-24 px-4 sm:px-6 lg:px-8 border-t border-gray-900">
        <div class="max-w-4xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-blue-400 mb-3">Credentials</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Certifications & Training</h3>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                <!-- Cert 1 -->
                <div class="bg-gray-900/60 border border-gray-800 p-6 rounded-2xl flex items-start gap-4 hover:border-gray-700 transition-all">
                    <div class="w-12 h-12 rounded-xl bg-blue-500/10 border border-blue-500/20 flex-shrink-0 flex items-center justify-center text-blue-400 font-bold">
                        <i class="fa-solid fa-award text-lg"></i>
                    </div>
                    <div>
                        <span class="inline-block px-2.5 py-0.5 rounded text-[10px] font-semibold bg-blue-950 text-blue-400 border border-blue-800/60 mb-2">Infosys Springboard</span>
                        <h4 class="text-base font-bold text-white mb-1">Artificial Intelligence & Python</h4>
                        <p class="text-xs text-gray-400">Comprehensive coursework covering core Python programming and foundational AI concepts.</p>
                    </div>
                </div>

                <!-- Cert 2 -->
                <div class="bg-gray-900/60 border border-gray-800 p-6 rounded-2xl flex items-start gap-4 hover:border-gray-700 transition-all">
                    <div class="w-12 h-12 rounded-xl bg-cyan-500/10 border border-cyan-500/20 flex-shrink-0 flex items-center justify-center text-cyan-400 font-bold">
                        <i class="fa-solid fa-robot text-lg"></i>
                    </div>
                    <div>
                        <span class="inline-block px-2.5 py-0.5 rounded text-[10px] font-semibold bg-cyan-950 text-cyan-400 border border-cyan-800/60 mb-2">GitHub</span>
                        <h4 class="text-base font-bold text-white mb-1">GitHub Copilot Developer</h4>
                        <p class="text-xs text-gray-400">Developer Productivity & AI-Assisted Coding Certification for accelerated software engineering.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-24 px-4 sm:px-6 lg:px-8 bg-[#0b101d]/60 border-t border-gray-900">
        <div class="max-w-3xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-blue-400 mb-3">Get In Touch</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Let's Build Something Great</h3>
            </div>

            <!-- Notification Box (Replaces alert) -->
            <div id="form-alert" class="hidden mb-6 p-4 rounded-xl border text-sm font-medium transition-all"></div>

            <form id="contact-form" class="bg-gray-900/80 border border-gray-800 p-8 sm:p-10 rounded-2xl shadow-xl space-y-6">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                    <div>
                        <label for="name" class="block text-xs font-semibold text-gray-300 uppercase tracking-wider mb-2">Your Name</label>
                        <input type="text" id="name" required class="w-full bg-gray-950 border border-gray-800 rounded-xl px-4 py-3 text-white placeholder-gray-600 focus:outline-none focus:border-blue-500 transition-all text-sm" placeholder="John Doe">
                    </div>
                    <div>
                        <label for="email" class="block text-xs font-semibold text-gray-300 uppercase tracking-wider mb-2">Your Email</label>
                        <input type="email" id="email" required class="w-full bg-gray-950 border border-gray-800 rounded-xl px-4 py-3 text-white placeholder-gray-600 focus:outline-none focus:border-blue-500 transition-all text-sm" placeholder="john@example.com">
                    </div>
                </div>
                <div>
                    <label for="subject" class="block text-xs font-semibold text-gray-300 uppercase tracking-wider mb-2">Subject</label>
                    <input type="text" id="subject" required class="w-full bg-gray-950 border border-gray-800 rounded-xl px-4 py-3 text-white placeholder-gray-600 focus:outline-none focus:border-blue-500 transition-all text-sm" placeholder="Project Inquiry / Collaboration">
                </div>
                <div>
                    <label for="message" class="block text-xs font-semibold text-gray-300 uppercase tracking-wider mb-2">Message</label>
                    <textarea id="message" rows="5" required class="w-full bg-gray-950 border border-gray-800 rounded-xl px-4 py-3 text-white placeholder-gray-600 focus:outline-none focus:border-blue-500 transition-all text-sm resize-none" placeholder="Write your message here..."></textarea>
                </div>
                <button type="submit" class="w-full py-4 rounded-xl text-base font-semibold text-white bg-gradient-to-r from-blue-600 to-cyan-500 hover:from-blue-500 hover:to-cyan-400 shadow-lg shadow-blue-500/25 transition-all duration-300 flex items-center justify-center gap-2">
                    <span>Send Message</span>
                    <i class="fa-solid fa-paper-plane text-xs"></i>
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-10 px-4 sm:px-6 lg:px-8 border-t border-gray-900 bg-[#090d16] text-center text-gray-500 text-sm">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-4">
            <p>&copy; 2026 Saicharan K. All rights reserved.</p>
            <div class="flex items-center space-x-6 text-gray-400">
                <a href="https://github.com" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors"><i class="fa-brands fa-github text-base"></i></a>
                <a href="https://linkedin.com" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors"><i class="fa-brands fa-linkedin-in text-base"></i></a>
                <a href="mailto:contact@saicharan.dev" class="hover:text-white transition-colors"><i class="fa-solid fa-envelope text-base"></i></a>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Navbar Shadow on Scroll
        const header = document.querySelector('header');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 20) {
                header.classList.add('bg-[#090d16]/95', 'shadow-lg', 'border-gray-800');
            } else {
                header.classList.remove('shadow-lg');
            }
        });

        // Contact Form Submission with Custom MessageBox (No alert())
        const contactForm = document.getElementById('contact-form');
        const formAlert = document.getElementById('form-alert');

        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const subject = document.getElementById('subject').value.trim();
            const message = document.getElementById('message').value.trim();

            if (!name || !email || !subject || !message) {
                showAlert('Please fill in all required fields.', 'error');
                return;
            }

            // Simulate successful message dispatch
            showAlert(`Thank you, ${name}! Your message has been successfully sent. I will get back to you soon.`, 'success');
            contactForm.reset();
        });

        function showAlert(message, type) {
            formAlert.textContent = message;
            formAlert.classList.remove('hidden', 'bg-emerald-950', 'border-emerald-800', 'text-emerald-400', 'bg-rose-950', 'border-rose-800', 'text-rose-400');
            
            if (type === 'success') {
                formAlert.classList.add('bg-emerald-950/80', 'border-emerald-800', 'text-emerald-400');
            } else {
                formAlert.classList.add('bg-rose-950/80', 'border-rose-800', 'text-rose-400');
            }

            // Scroll alert into view
            formAlert.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
    </script>
</body>
</html>
