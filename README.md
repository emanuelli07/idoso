<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cidadania Digital & Direitos na Redes</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f0f9ff',
                            100: '#e0f2fe',
                            500: '#0284c7',
                            600: '#0284c7',
                            700: '#0369a1',
                            800: '#075985',
                            900: '#0c4a6e',
                        }
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .gradient-banner {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #0369a1 100%);
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
        }
        .dark .glass-card {
            background: rgba(30, 41, 59, 0.85);
            backdrop-filter: blur(12px);
        }
    </style>
</head>
<body class="bg-slate-50 dark:bg-slate-900 text-slate-800 dark:text-slate-100 font-sans transition-colors duration-300 min-h-screen flex flex-col">

    <!-- Header & Navegação -->
    <header class="sticky top-0 z-50 bg-white/90 dark:bg-slate-900/90 backdrop-blur-md border-b border-slate-200 dark:border-slate-800 transition-colors">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <!-- Logo -->
                <div class="flex items-center space-x-3 cursor-pointer" onclick="scrollToSection('hero')">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-sky-500 to-indigo-600 flex items-center justify-center text-white shadow-md">
                        <i class="fa-solid fa-shield-halved text-xl"></i>
                    </div>
                    <div>
                        <span class="font-bold text-lg tracking-tight bg-gradient-to-r from-sky-600 to-indigo-600 dark:from-sky-400 dark:to-indigo-400 bg-clip-text text-transparent">CidadaniaDigital</span>
                        <span class="block text-[10px] uppercase font-semibold tracking-wider text-slate-400 dark:text-slate-500">Guia & Direitos</span>
                    </div>
                </div>

                <!-- Menu Desktop -->
                <nav class="hidden md:flex items-center space-x-8 text-sm font-medium">
                    <button onclick="scrollToSection('hero')" class="hover:text-sky-500 transition">Início</button>
                    <button onclick="scrollToSection('seguranca')" class="hover:text-sky-500 transition">Segurança & Dicas</button>
                    <button onclick="scrollToSection('leis')" class="hover:text-sky-500 transition">Leis e Direitos</button>
                    <button onclick="scrollToSection('dia-a-dia')" class="hover:text-sky-500 transition">Práticas Diárias</button>
                    <button onclick="scrollToSection('recursos')" class="hover:text-sky-500 transition">Quiz & Ferramentas</button>
                </nav>

                <!-- Botões Auxiliares -->
                <div class="flex items-center space-x-3">
                    <button id="themeToggleBtn" onclick="toggleDarkMode()" class="p-2 rounded-lg text-slate-500 dark:text-slate-400 hover:bg-slate-100 dark:hover:bg-slate-800 transition" title="Alternar Tema">
                        <i id="themeIcon" class="fa-solid fa-moon text-lg"></i>
                    </button>
                    <!-- Mobile Hamburger -->
                    <button onclick="toggleMobileMenu()" class="md:hidden p-2 rounded-lg text-slate-600 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800">
                        <i class="fa-solid fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Menu Mobile -->
        <div id="mobileMenu" class="hidden md:hidden border-b border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 px-4 pt-2 pb-4 space-y-2">
            <button onclick="scrollToSection('hero'); toggleMobileMenu()" class="block w-full text-left py-2 px-3 rounded-md hover:bg-slate-100 dark:hover:bg-slate-800">Início</button>
            <button onclick="scrollToSection('seguranca'); toggleMobileMenu()" class="block w-full text-left py-2 px-3 rounded-md hover:bg-slate-100 dark:hover:bg-slate-800">Segurança & Dicas</button>
            <button onclick="scrollToSection('leis'); toggleMobileMenu()" class="block w-full text-left py-2 px-3 rounded-md hover:bg-slate-100 dark:hover:bg-slate-800">Leis e Direitos</button>
            <button onclick="scrollToSection('dia-a-dia'); toggleMobileMenu()" class="block w-full text-left py-2 px-3 rounded-md hover:bg-slate-100 dark:hover:bg-slate-800">Práticas Diárias</button>
            <button onclick="scrollToSection('recursos'); toggleMobileMenu()" class="block w-full text-left py-2 px-3 rounded-md hover:bg-slate-100 dark:hover:bg-slate-800">Quiz & Ferramentas</button>
        </div>
    </header>

    <!-- BANNER INICIAL / HERO SECTION -->
    <section id="hero" class="relative gradient-banner text-white py-20 px-4 sm:px-6 lg:px-8 overflow-hidden">
        <div class="absolute inset-0 opacity-10 bg-[radial-gradient(#fff_1px,transparent_1px)] [background-size:16px_16px]"></div>
        
        <div class="max-w-7xl mx-auto relative z-10 grid md:grid-cols-2 gap-12 items-center">
            <div class="space-y-6 text-center md:text-left">
                <span class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full text-xs font-semibold bg-sky-500/20 text-sky-300 border border-sky-400/30">
                    <i class="fa-solid fa-user-lock"></i> Navegue com Responsabilidade e Segurança
                </span>
                <h1 class="text-4xl sm:text-5xl font-extrabold tracking-tight leading-tight">
                    Sua jornada para uma <span class="bg-clip-text text-transparent bg-gradient-to-r from-sky-300 to-emerald-300">Cidadania Digital</span> consciente.
                </h1>
                <p class="text-slate-300 text-lg leading-relaxed max-w-xl">
                    Compreenda seus direitos na internet, aprenda a proteger seus dados pessoais, previna-se contra golpes digitais e adote hábitos seguros no ecossistema online.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start pt-2">
                    <button onclick="scrollToSection('seguranca')" class="px-6 py-3.5 rounded-xl bg-sky-500 hover:bg-sky-400 text-white font-semibold transition shadow-lg shadow-sky-500/30 flex items-center justify-center gap-2">
                        <i class="fa-solid fa-shield-virus"></i> Ver Dicas de Segurança
                    </button>
                    <button onclick="scrollToSection('leis')" class="px-6 py-3.5 rounded-xl bg-slate-800/80 hover:bg-slate-700/80 text-black font-semibold transition border border-slate-700 flex items-center justify-center gap-2">
                        <i class="fa-solid fa-scale-balanced"></i> Conhecer Seus Direitos
                    </button>
                </div>
            </div>

            <!-- Card Destaque Interativo no Banner -->
            <div class="glass-card p-6 rounded-2xl border border-white/20 text-slate-800 dark:text-slate-100 shadow-2xl space-y-4">
                <div class="flex items-center justify-between pb-3 border-b border-slate-200 dark:border-slate-700">
                    <h2 class="font-bold text-lg flex items-center gap-2">
                        <i class="fa-solid fa-bullhorn text-sky-500"></i> Destaques da Cidadania
                    </h2>
                    <span class="text-xs bg-emerald-100 dark:bg-emerald-900/50 text-emerald-700 dark:text-emerald-300 px-2.5 py-1 rounded-full font-semibold">Atualizado</span>
                </div>
                <div class="space-y-3 text-sm">
                    <div class="p-3 rounded-lg bg-slate-100/80 dark:bg-slate-800/80 flex items-start gap-3">
                        <i class="fa-solid fa-lock text-sky-500 mt-1"></i>
                        <div>
                            <strong class="block font-semibold">Proteção de Dados (LGPD)</strong>
                            <p class="text-xs text-slate-600 dark:text-slate-400">Você tem o direito de saber quais dados as empresas coletam e de pedir a exclusão deles.</p>
                        </div>
                    </div>
                    <div class="p-3 rounded-lg bg-slate-100/80 dark:bg-slate-800/80 flex items-start gap-3">
                        <i class="fa-solid fa-fingerprint text-emerald-500 mt-1"></i>
                        <div>
                            <strong class="block font-semibold">Autenticação em Dois Fatores (2FA)</strong>
                            <p class="text-xs text-slate-600 dark:text-slate-400">Ative o 2FA em WhatsApp, e-mails e redes sociais para bloquear acessos não autorizados.</p>
                        </div>
                    </div>
                    <div class="p-3 rounded-lg bg-slate-100/80 dark:bg-slate-800/80 flex items-start gap-3">
                        <i class="fa-solid fa-gavel text-amber-500 mt-1"></i>
                        <div>
                            <strong class="block font-semibold">Marco Civil da Internet</strong>
                            <p class="text-xs text-slate-600 dark:text-slate-400">Garante a neutralidade da rede e a privacidade de suas comunicações digitais.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SEÇÃO 1: DICAS DE SEGURANÇA E PRIVACIDADE -->
    <section id="seguranca" class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto w-full">
        <div class="text-center max-w-3xl mx-auto mb-12">
            <h2 class="text-3xl font-extrabold text-slate-900 dark:text-white tracking-tight">
                Dicas de Segurança e Privacidade
            </h2>
            <p class="mt-3 text-slate-600 dark:text-slate-400">
                Aprenda a criar defesas sólidas para proteger sua identidade, suas senhas e suas finanças no ambiente online.
            </p>
        </div>

        <!-- Filtro/Busca Rápida de Dicas -->
        <div class="max-w-md mx-auto mb-8 relative">
            <input type="text" id="searchTips" onkeyup="filterTips()" placeholder="Buscar dica (ex: senhas, golpes, Wi-Fi)..." 
                class="w-full pl-10 pr-4 py-3 rounded-xl border border-slate-300 dark:border-slate-700 bg-white dark:bg-slate-800 text-slate-900 dark:text-slate-100 focus:outline-none focus:ring-2 focus:ring-sky-500 shadow-sm transition">
            <i class="fa-solid fa-magnifying-glass absolute left-3.5 top-4 text-slate-400"></i>
        </div>

        <div id="tipsGrid" class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Card 1 -->
            <div class="tip-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition">
                <div class="w-12 h-12 rounded-xl bg-sky-100 dark:bg-sky-900/40 text-sky-600 dark:text-sky-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-key"></i>
                </div>
                <h3 class="font-bold text-lg mb-2 text-slate-900 dark:text-white">Gerenciamento de Senhas Forte</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed">
                    Evite usar datas de nascimento ou sequências fáceis. Use frases longas misturando letras, números e símbolos, ou utilize um gerenciador de senhas confiável.
                </p>
            </div>

            <!-- Card 2 -->
            <div class="tip-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition">
                <div class="w-12 h-12 rounded-xl bg-amber-100 dark:bg-amber-900/40 text-amber-600 dark:text-amber-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-fish-fins"></i>
                </div>
                <h3 class="font-bold text-lg mb-2 text-slate-900 dark:text-white">Atenção ao Phishing (Golpes)</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed">
                    Desconfie de e-mails, SMS e mensagens com Links urgentes, prêmios inesperados ou solicitações de confirmação de dados bancários.
                </p>
            </div>

            <!-- Card 3 -->
            <div class="tip-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition">
                <div class="w-12 h-12 rounded-xl bg-emerald-100 dark:bg-emerald-900/40 text-emerald-600 dark:text-emerald-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-mobile-screen-button"></i>
                </div>
                <h3 class="font-bold text-lg mb-2 text-slate-900 dark:text-white">Verificação em Duas Etapas</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed">
                    Mesmo que descubram sua senha, o código adicional enviado ao seu aplicativo autenticador impedirá a invasão de suas contas.
                </p>
            </div>

            <!-- Card 4 -->
            <div class="tip-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition">
                <div class="w-12 h-12 rounded-xl bg-purple-100 dark:bg-purple-900/40 text-purple-600 dark:text-purple-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-wifi"></i>
                </div>
                <h3 class="font-bold text-lg mb-2 text-slate-900 dark:text-white">Cuidado com Wi-Fi Público</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed">
                    Evite acessar aplicativos bancários ou digitar senhas confidenciais enquanto estiver conectado a redes Wi-Fi abertas ou públicas sem VPN.
                </p>
            </div>

            <!-- Card 5 -->
            <div class="tip-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition">
                <div class="w-12 h-12 rounded-xl bg-rose-100 dark:bg-rose-900/40 text-rose-600 dark:text-rose-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-rotate"></i>
                </div>
                <h3 class="font-bold text-lg mb-2 text-slate-900 dark:text-white">Atualizações de Sistema</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed">
                    Mantenha o sistema operacional do seu celular/PC e seus aplicativos sempre atualizados. As atualizações corrigem brechas críticas de segurança.
                </p>
            </div>

            <!-- Card 6 -->
            <div class="tip-card bg-white dark:bg-slate-800 p-6 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm hover:shadow-md transition">
                <div class="w-12 h-12 rounded-xl bg-indigo-100 dark:bg-indigo-900/40 text-indigo-600 dark:text-indigo-400 flex items-center justify-center text-xl mb-4">
                    <i class="fa-solid fa-eye-slash"></i>
                </div>
                <h3 class="font-bold text-lg mb-2 text-slate-900 dark:text-white">Configuração de Privacidade</h3>
                <p class="text-sm text-slate-600 dark:text-slate-300 leading-relaxed">
                    Revise periodicamente quem pode ver suas fotos, localização e publicações nas redes sociais. Limite o acesso do público em geral.
                </p>
            </div>
        </div>
    </section>

    <!-- SEÇÃO 2: DIREITOS LEGAIS E GARANTIAS DIGITAIS -->
    <section id="leis" class="py-16 bg-slate-100/70 dark:bg-slate-800/50 border-y border-slate-200 dark:border-slate-800 transition-colors">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <span class="text-sky-600 dark:text-sky-400 font-semibold text-sm uppercase tracking-wider">Legislação & Proteção</span>
                <h2 class="text-3xl font-extrabold text-slate-900 dark:text-white tracking-tight mt-1">
                    Leis e Garantias no Ambiente Digital
                </h2>
                <p class="mt-3 text-slate-600 dark:text-slate-400">
                    Na internet, você possui direitos fundamentais resguardados pela legislação brasileira.
                </p>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Marco Civil -->
                <div class="bg-white dark:bg-slate-900 p-6 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-sm flex flex-col justify-between">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="px-3 py-1 bg-sky-100 dark:bg-sky-900/50 text-sky-700 dark:text-sky-300 rounded-full text-xs font-bold">Lei 12.965/2014</span>
                            <i class="fa-solid fa-globe text-2xl text-sky-500"></i>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">Marco Civil da Internet</h3>
                        <p class="text-sm text-slate-600 dark:text-slate-400 mb-4 leading-relaxed">
                            Estabelece princípios, garantias, direitos e deveres para o uso da internet no Brasil.
                        </p>
                        <ul class="text-sm text-slate-600 dark:text-slate-300 space-y-2">
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Neutralidade da rede.</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Inviolabilidade do fluxo de comunicações.</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Guarda sigilosa de registros de acesso.</li>
                        </ul>
                    </div>
                </div>

                <!-- LGPD -->
                <div class="bg-white dark:bg-slate-900 p-6 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-sm flex flex-col justify-between">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="px-3 py-1 bg-indigo-100 dark:bg-indigo-900/50 text-indigo-700 dark:text-indigo-300 rounded-full text-xs font-bold">Lei 13.709/2018</span>
                            <i class="fa-solid fa-user-shield text-2xl text-indigo-500"></i>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">LGPD (Lei Geral de Proteção de Dados)</h3>
                        <p class="text-sm text-slate-600 dark:text-slate-400 mb-4 leading-relaxed">
                            Regulamenta o tratamento de dados pessoais por empresas públicas e privadas.
                        </p>
                        <ul class="text-sm text-slate-600 dark:text-slate-300 space-y-2">
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Direito de acessar e corrigir seus dados.</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Exigência de consentimento claro.</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Revogação de autorizações e exclusão de cadastros.</li>
                        </ul>
                    </div>
                </div>

                <!-- CDC no E-commerce -->
                <div class="bg-white dark:bg-slate-900 p-6 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-sm flex flex-col justify-between">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <span class="px-3 py-1 bg-emerald-100 dark:bg-emerald-900/50 text-emerald-700 dark:text-emerald-300 rounded-full text-xs font-bold">Decreto 7.962/2013</span>
                            <i class="fa-solid fa-cart-shopping text-2xl text-emerald-500"></i>
                        </div>
                        <h3 class="text-xl font-bold text-slate-900 dark:text-white mb-2">CDC & Comércio Eletrônico</h3>
                        <p class="text-sm text-slate-600 dark:text-slate-400 mb-4 leading-relaxed">
                            Aplica as garantias do consumidor às compras efetuadas pela internet.
                        </p>
                        <ul class="text-sm text-slate-600 dark:text-slate-300 space-y-2">
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Direito de Arrependimento em até 7 dias.</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Informações claras sobre CNPJ e atendimento.</li>
                            <li class="flex items-start gap-2"><i class="fa-solid fa-check text-emerald-500 mt-1"></i> Reembolso integral de devoluções.</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Como agir em caso de violação de direitos -->
            <div class="mt-12 bg-white dark:bg-slate-900 p-8 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-sm">
                <h3 class="text-2xl font-bold text-slate-900 dark:text-white mb-4 flex items-center gap-3">
                    <i class="fa-solid fa-triangle-exclamation text-amber-500"></i>
                    O que fazer se seus direitos forem violados online?
                </h3>
                <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6 text-sm">
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-slate-800/50 border border-slate-200 dark:border-slate-700">
                        <span class="font-bold text-sky-600 dark:text-sky-400 block text-lg mb-1">1. Registre Provas</span>
                        <p class="text-slate-600 dark:text-slate-400">Faça capturas de tela (screenshots), guarde URLs, e-mails, horários e mensagens trocadas.</p>
                    </div>
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-slate-800/50 border border-slate-200 dark:border-slate-700">
                        <span class="font-bold text-sky-600 dark:text-sky-400 block text-lg mb-1">2. Faça Boletim de Ocorrência</span>
                        <p class="text-slate-600 dark:text-slate-400">Em caso de crimes cibernéticos (fraudes, ofensas, vazamento de fotos), registre B.O. na delegacia eletrônica.</p>
                    </div>
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-slate-800/50 border border-slate-200 dark:border-slate-700">
                        <span class="font-bold text-sky-600 dark:text-sky-400 block text-lg mb-1">3. Denuncie na Plataforma</span>
                        <p class="text-slate-600 dark:text-slate-400">Utilize os canais de denúncia da própria rede social ou site para solicitar a remoção do conteúdo ilícito.</p>
                    </div>
                    <div class="p-4 rounded-xl bg-slate-50 dark:bg-slate-800/50 border border-slate-200 dark:border-slate-700">
                        <span class="font-bold text-sky-600 dark:text-sky-400 block text-lg mb-1">4. Órgãos de Proteção</span>
                        <p class="text-slate-600 dark:text-slate-400">Recorra ao Procon, Consumidor.gov.br ou ANPD (Autoridade Nacional de Proteção de Dados).</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SEÇÃO 3: CIDADANIA DIGITAL NO DIA A DIA -->
    <section id="dia-a-dia" class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto w-full">
        <div class="text-center max-w-3xl mx-auto mb-12">
            <span class="text-sky-600 dark:text-sky-400 font-semibold text-sm uppercase tracking-wider">Hábitos Conscientes</span>
            <h2 class="text-3xl font-extrabold text-slate-900 dark:text-white tracking-tight mt-1">
                Praticando a Cidadania Digital no Dia a Dia
            </h2>
            <p class="mt-3 text-slate-600 dark:text-slate-400">
                A cidadania digital vai além da tecnologia: envolve ética, respeito, empatia e senso crítico no cotidiano online.
            </p>
        </div>

        <div class="grid md:grid-cols-2 gap-8 items-stretch">
            <!-- Boas Práticas -->
            <div class="bg-white dark:bg-slate-800 p-6 sm:p-8 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-sm space-y-6">
                <h3 class="text-xl font-bold text-slate-900 dark:text-white flex items-center gap-2">
                    <i class="fa-solid fa-heart text-rose-500"></i> Etiqueta Digital & Empatia (Netiqueta)
                </h3>
                
                <div class="space-y-4 text-sm">
                    <div class="flex gap-4 items-start">
                        <div class="w-8 h-8 rounded-full bg-emerald-100 dark:bg-emerald-900/50 text-emerald-600 dark:text-emerald-300 flex items-center justify-center shrink-0 font-bold">1</div>
                        <div>
                            <strong class="text-slate-900 dark:text-white block">Verifique antes de compartilhar</strong>
                            <p class="text-slate-600 dark:text-slate-400">Combata a desinformação. Cheque fontes antes de repassar notícias ou áudios em grupos.</p>
                        </div>
                    </div>

                    <div class="flex gap-4 items-start">
                        <div class="w-8 h-8 rounded-full bg-emerald-100 dark:bg-emerald-900/50 text-emerald-600 dark:text-emerald-300 flex items-center justify-center shrink-0 font-bold">2</div>
                        <div>
                            <strong class="text-slate-900 dark:text-white block">Respeite a diversidade de opiniões</strong>
                            <p class="text-slate-600 dark:text-slate-400">Evite discursos de ódio ou comentários agressivos (cyberbullying). Lembre-se: há pessoas reais do outro lado da tela.</p>
                        </div>
                    </div>

                    <div class="flex gap-4 items-start">
                        <div class="w-8 h-8 rounded-full bg-emerald-100 dark:bg-emerald-900/50 text-emerald-600 dark:text-emerald-300 flex items-center justify-center shrink-0 font-bold">3</div>
                        <div>
                            <strong class="text-slate-900 dark:text-white block">Preserve a imagem alheia</strong>
                            <p class="text-slate-600 dark:text-slate-400">Peça autorização antes de publicar fotos ou vídeos onde terceiros ou crianças aparecem.</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Interativo: Checklist Diário de Privacidade -->
            <div class="bg-gradient-to-br from-sky-900 to-slate-900 text-white p-6 sm:p-8 rounded-2xl shadow-xl flex flex-col justify-between">
                <div>
                    <h3 class="text-xl font-bold mb-2 flex items-center gap-2">
                        <i class="fa-solid fa-list-check text-sky-400"></i> Checklist Diário de Segurança
                    </h3>
                    <p class="text-xs text-sky-200 mb-6">Marque os itens que você já praticou hoje:</p>

                    <div class="space-y-3 text-sm">
                        <label class="flex items-center gap-3 p-3 rounded-lg bg-white/10 hover:bg-white/15 cursor-pointer transition">
                            <input type="checkbox" class="daily-check w-5 h-5 rounded text-sky-500 focus:ring-0 cursor-pointer" onchange="updateChecklistProgress()">
                            <span>Bloqueei a tela do meu celular com PIN/Biometria.</span>
                        </label>
                        <label class="flex items-center gap-3 p-3 rounded-lg bg-white/10 hover:bg-white/15 cursor-pointer transition">
                            <input type="checkbox" class="daily-check w-5 h-5 rounded text-sky-500 focus:ring-0 cursor-pointer" onchange="updateChecklistProgress()">
                            <span>Não cliquei em links suspeitos recebidos por mensagem.</span>
                        </label>
                        <label class="flex items-center gap-3 p-3 rounded-lg bg-white/10 hover:bg-white/15 cursor-pointer transition">
                            <input type="checkbox" class="daily-check w-5 h-5 rounded text-sky-500 focus:ring-0 cursor-pointer" onchange="updateChecklistProgress()">
                            <span>Não divulguei dados sensíveis em redes sociais públicas.</span>
                        </label>
                        <label class="flex items-center gap-3 p-3 rounded-lg bg-white/10 hover:bg-white/15 cursor-pointer transition">
                            <input type="checkbox" class="daily-check w-5 h-5 rounded text-sky-500 focus:ring-0 cursor-pointer" onchange="updateChecklistProgress()">
                            <span>Conferi a presença do cadeado HTTPS nos sites acessados.</span>
                        </label>
                    </div>
                </div>

                <div class="mt-6 pt-4 border-t border-white/10">
                    <div class="flex justify-between text-xs font-semibold mb-1">
                        <span>Progresso de Proteção:</span>
                        <span id="checklistScore">0%</span>
                    </div>
                    <div class="w-full bg-slate-700 h-2.5 rounded-full overflow-hidden">
                        <div id="checklistBar" class="bg-sky-400 h-full w-0 transition-all duration-300"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SEÇÃO 4: QUIZ INTERATIVO & RECURSOS ÚTEIS -->
    <section id="recursos" class="py-16 bg-slate-100/70 dark:bg-slate-800/50 border-t border-slate-200 dark:border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-2 gap-12 items-start">
                
                <!-- QUIZ DE CIDADANIA DIGITAL -->
                <div class="bg-white dark:bg-slate-900 p-6 sm:p-8 rounded-2xl border border-slate-200 dark:border-slate-800 shadow-sm">
                    <div class="flex items-center justify-between mb-6">
                        <h3 class="text-2xl font-bold text-slate-900 dark:text-white flex items-center gap-2">
                            <i class="fa-solid fa-graduation-cap text-sky-500"></i> Teste Seus Conhecimentos
                        </h3>
                        <span id="quizStep" class="text-xs bg-sky-100 dark:bg-sky-900/50 text-sky-700 dark:text-sky-300 font-bold px-2.5 py-1 rounded-full">Pergunta 1/3</span>
                    </div>

                    <div id="quizContainer">
                        <p id="quizQuestion" class="font-semibold text-slate-800 dark:text-slate-200 mb-4 text-base">
                            Carregando pergunta...
                        </p>
                        <div id="quizOptions" class="space-y-3">
                            <!-- Opções geradas via JS -->
                        </div>
                        <div id="quizFeedback" class="mt-4 p-3 rounded-lg text-sm hidden font-medium"></div>
                        <button id="nextBtn" onclick="nextQuestion()" class="mt-6 w-full py-3 bg-sky-600 hover:bg-sky-500 text-white font-semibold rounded-xl transition hidden">
                            Próxima Pergunta
                        </button>
                    </div>

                    <div id="quizResult" class="hidden text-center py-6 space-y-4">
                        <i class="fa-solid fa-award text-5xl text-amber-400"></i>
                        <h4 class="text-xl font-bold text-slate-900 dark:text-white">Quiz Concluído!</h4>
                        <p id="resultText" class="text-slate-600 dark:text-slate-300 text-sm"></p>
                        <button onclick="resetQuiz()" class="px-6 py-2.5 bg-slate-800 dark:bg-slate-700 text-white rounded-xl text-sm font-semibold hover:bg-slate-700 transition">
                            Refazer Quiz
                        </button>
                    </div>
                </div>

                <!-- CANAIS DE DENÚNCIA E CONTATOS ÚTEIS -->
                <div class="space-y-6">
                    <div>
                        <h3 class="text-2xl font-bold text-slate-900 dark:text-white mb-2 flex items-center gap-2">
                            <i class="fa-solid fa-phone-volume text-emerald-500"></i> Canas de Ajuda e Denúncia
                        </h3>
                        <p class="text-sm text-slate-600 dark:text-slate-400">
                            Acesse órgãos oficiais e entidades especializadas para orientação ou denúncia de crimes na internet.
                        </p>
                    </div>

                    <div class="space-y-3">
                        <a href="https://safernet.org.br" target="_blank" class="block p-4 bg-white dark:bg-slate-900 rounded-xl border border-slate-200 dark:border-slate-800 hover:border-sky-500 dark:hover:border-sky-500 transition shadow-sm group">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center gap-3">
                                    <div class="w-10 h-10 rounded-lg bg-sky-100 dark:bg-sky-900/40 text-sky-600 flex items-center justify-center font-bold">
                                        <i class="fa-solid fa-shield-cat text-lg"></i>
                                    </div>
                                    <div>
                                        <strong class="text-slate-900 dark:text-white group-hover:text-sky-500 transition">SaferNet Brasil</strong>
                                        <span class="block text-xs text-slate-500">Denúncias anônimas de violações de direitos humanos na web.</span>
                                    </div>
                                </div>
                                <i class="fa-solid fa-arrow-up-right-from-square text-xs text-slate-400 group-hover:text-sky-500"></i>
                            </div>
                        </a>

                        <a href="https://www.consumidor.gov.br" target="_blank" class="block p-4 bg-white dark:bg-slate-900 rounded-xl border border-slate-200 dark:border-slate-800 hover:border-sky-500 dark:hover:border-sky-500 transition shadow-sm group">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center gap-3">
                                    <div class="w-10 h-10 rounded-lg bg-emerald-100 dark:bg-emerald-900/40 text-emerald-600 flex items-center justify-center font-bold">
                                        <i class="fa-solid fa-handshake text-lg"></i>
                                    </div>
                                    <div>
                                        <strong class="text-slate-900 dark:text-white group-hover:text-emerald-500 transition">Consumidor.gov.br</strong>
                                        <span class="block text-xs text-slate-500">Plataforma pública para solução de conflitos de consumo online.</span>
                                    </div>
                                </div>
                                <i class="fa-solid fa-arrow-up-right-from-square text-xs text-slate-400 group-hover:text-emerald-500"></i>
                            </div>
                        </a>

                        <a href="https://www.gov.br/anpd/pt-br" target="_blank" class="block p-4 bg-white dark:bg-slate-900 rounded-xl border border-slate-200 dark:border-slate-800 hover:border-sky-500 dark:hover:border-sky-500 transition shadow-sm group">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center gap-3">
                                    <div class="w-10 h-10 rounded-lg bg-indigo-100 dark:bg-indigo-900/40 text-indigo-600 flex items-center justify-center font-bold">
                                        <i class="fa-solid fa-building-columns text-lg"></i>
                                    </div>
                                    <div>
                                        <strong class="text-slate-900 dark:text-white group-hover:text-indigo-500 transition">ANPD (Autoridade de Proteção de Dados)</strong>
                                        <span class="block text-xs text-slate-500">Órgão regulador responsável por fiscalizar o cumprimento da LGPD.</span>
                                    </div>
                                </div>
                                <i class="fa-solid fa-arrow-up-right-from-square text-xs text-slate-400 group-hover:text-indigo-500"></i>
                            </div>
                        </a>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- FOOTER / RODAPÉ -->
    <footer class="bg-slate-900 text-slate-400 py-10 border-t border-slate-800 mt-auto">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center justify-between gap-6">
            <div class="flex items-center space-x-3">
                <div class="w-8 h-8 rounded-lg bg-sky-500 flex items-center justify-center text-white">
                    <i class="fa-solid fa-shield-halved text-sm"></i>
                </div>
                <span class="text-white font-bold tracking-tight">CidadaniaDigital</span>
            </div>
            <p class="text-xs text-center md:text-left">
                Guia educacional sobre Segurança, Proteção de Dados e Direitos na Internet. Desenvolvido para fins informativos.
            </p>
            <div class="flex space-x-4 text-slate-400 text-sm">
                <a href="#hero" class="hover:text-white transition">Início</a>
                <a href="#seguranca" class="hover:text-white transition">Dicas</a>
                <a href="#leis" class="hover:text-white transition">Direitos</a>
            </div>
        </div>
    </footer>

    <!-- JAVASCRIPT DE INTERATIVIDADE -->
    <script>
        // Alternar Tema Claro/Escuro
        function toggleDarkMode() {
            const html = document.documentElement;
            const icon = document.getElementById('themeIcon');
            if (html.classList.contains('dark')) {
                html.classList.remove('dark');
                icon.className = 'fa-solid fa-moon text-lg';
            } else {
                html.classList.add('dark');
                icon.className = 'fa-solid fa-sun text-lg';
            }
        }

        // Alternar Menu Mobile
        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        // Rolagem Suave para Seção
        function scrollToSection(id) {
            const element = document.getElementById(id);
            if (element) {
                element.scrollIntoView({ behavior: 'smooth' });
            }
        }

        // Filtro Dinâmico de Dicas de Segurança
        function filterTips() {
            const input = document.getElementById('searchTips').value.toLowerCase();
            const cards = document.querySelectorAll('.tip-card');

            cards.forEach(card => {
                const text = card.innerText.toLowerCase();
                if (text.includes(input)) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        // Atualizar Progresso do Checklist
        function updateChecklistProgress() {
            const checkboxes = document.querySelectorAll('.daily-check');
            const total = checkboxes.length;
            let checkedCount = 0;

            checkboxes.forEach(cb => {
                if (cb.checked) checkedCount++;
            });

            const percentage = Math.round((checkedCount / total) * 100);
            document.getElementById('checklistScore').innerText = percentage + '%';
            document.getElementById('checklistBar').style.width = percentage + '%';
        }

        // LÓGICA DO QUIZ INTERATIVO
        const quizData = [
            {
                question: "Qual das opções é uma prática segura ao receber um e-mail solicitando atualização bancária?",
                options: [
                    "Clicar imediatamente no link recebido para evitar o bloqueio.",
                    "Ignorar o link e entrar em contato direto com o banco por canais oficiais.",
                    "Responder ao e-mail informando sua senha atual para confirmação."
                ],
                correct: 1,
                explanation: "Bancos não solicitam atualização de senhas por links de e-mail. Sempre use o app ou site oficial do banco."
            },
            {
                question: "De acordo com a LGPD, qual é um direito do titular dos dados pessoais?",
                options: [
                    "Solicitar a confirmação da existência de tratamento e o acesso aos seus dados.",
                    "Ser obrigado a aceitar o compartilhamento ilimitado de seus dados.",
                    "Não poder cancelar o cadastro em nenhuma empresa."
                ],
                correct: 0,
                explanation: "A LGPD garante ao cidadão o direito de saber como seus dados são usados e de solicitar sua exclusão."
            },
            {
                question: "O que garante o Direito de Arrependimento nas compras online?",
                options: [
                    "Possibilidade de desistir da compra em até 7 dias após o recebimento, com reembolso total.",
                    "Troca garantida apenas se o produto estiver com defeito de fábrica.",
                    "O direito de cancelar a compra somente no primeiro minuto após o pagamento."
                ],
                correct: 0,
                explanation: "O Código de Defesa do Consumidor garante 7 dias corridos para devolução sem necessidade de justificativa."
            }
        ];

        let currentQuizIndex = 0;
        let quizScore = 0;

        function loadQuestion() {
            const q = quizData[currentQuizIndex];
            document.getElementById('quizStep').innerText = `Pergunta ${currentQuizIndex + 1}/${quizData.length}`;
            document.getElementById('quizQuestion').innerText = q.question;

            const optionsContainer = document.getElementById('quizOptions');
            optionsContainer.innerHTML = '';

            const feedback = document.getElementById('quizFeedback');
            feedback.classList.add('hidden');
            document.getElementById('nextBtn').classList.add('hidden');

            q.options.forEach((opt, idx) => {
                const btn = document.createElement('button');
                btn.className = 'w-full text-left p-3.5 rounded-xl border border-slate-200 dark:border-slate-700 hover:border-sky-500 dark:hover:border-sky-500 text-sm font-medium transition bg-slate-50 dark:bg-slate-800 text-slate-800 dark:text-slate-200';
                btn.innerText = opt;
                btn.onclick = () => selectOption(idx);
                optionsContainer.appendChild(btn);
            });
        }

        function selectOption(index) {
            const q = quizData[currentQuizIndex];
            const feedback = document.getElementById('quizFeedback');
            const optionsBtns = document.getElementById('quizOptions').children;

            // Desabilitar botões após resposta
            for (let btn of optionsBtns) {
                btn.disabled = true;
                btn.classList.add('opacity-70', 'cursor-not-allowed');
            }

            if (index === q.correct) {
                quizScore++;
                optionsBtns[index].classList.add('bg-emerald-100', 'dark:bg-emerald-900/60', 'border-emerald-500', 'text-emerald-800', 'dark:text-emerald-200');
                feedback.className = 'mt-4 p-3 rounded-lg text-sm bg-emerald-100 dark:bg-emerald-900/50 text-emerald-800 dark:text-emerald-200 font-medium block';
                feedback.innerText = 'Resposta Correta! ' + q.explanation;
            } else {
                optionsBtns[index].classList.add('bg-rose-100', 'dark:bg-rose-900/60', 'border-rose-500', 'text-rose-800', 'dark:text-rose-200');
                optionsBtns[q.correct].classList.add('bg-emerald-100', 'dark:bg-emerald-900/60', 'border-emerald-500');
                feedback.className = 'mt-4 p-3 rounded-lg text-sm bg-rose-100 dark:bg-rose-900/50 text-rose-800 dark:text-rose-200 font-medium block';
                feedback.innerText = 'Ops, incorreto. ' + q.explanation;
            }

            document.getElementById('nextBtn').classList.remove('hidden');
        }

        function nextQuestion() {
            currentQuizIndex++;
            if (currentQuizIndex < quizData.length) {
                loadQuestion();
            } else {
                showQuizResult();
            }
        }

        function showQuizResult() {
            document.getElementById('quizContainer').classList.add('hidden');
            const resultDiv = document.getElementById('quizResult');
            resultDiv.classList.remove('hidden');
            document.getElementById('resultText').innerText = `Você acertou ${quizScore} de ${quizData.length} perguntas! Continue praticando a Cidadania Digital no seu dia a dia.`;
        }

        function resetQuiz() {
            currentQuizIndex = 0;
            quizScore = 0;
            document.getElementById('quizResult').classList.add('hidden');
            document.getElementById('quizContainer').classList.remove('hidden');
            loadQuestion();
        }

        // Inicializar quiz
        window.onload = function() {
            loadQuestion();
        };
    </script>
</body>
</html>
