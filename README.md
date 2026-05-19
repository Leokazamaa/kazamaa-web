<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Premium Service - Alta Performance</title>
    <!-- Tailwind CSS para design ágil e responsivo -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Lucide Icons para vetores limpos -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        .glass-card {
            background: rgba(30, 41, 59, 0.7);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .glow-effect {
            box-shadow: 0 0 25px -5px rgba(59, 130, 246, 0.5);
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 font-sans antialiased selection:bg-blue-600 selection:text-white">

    <!-- Background Glows -->
    <div class="absolute top-0 left-1/2 -translate-x-1/2 w-full max-w-7xl h-[500px] bg-blue-600/10 blur-[120px] rounded-full pointer-events-none"></div>

    <!-- Navigation -->
    <nav class="border-b border-slate-800/60 bg-slate-950/80 backdrop-blur-md sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <i data-lucide="zap" class="text-blue-500 w-6 h-6 fill-blue-500/20"></i>
                <span class="text-xl font-bold tracking-tight bg-gradient-to-r from-white to-slate-400 bg-clip-text text-transparent">PLATAFORMA</span>
            </div>
            <div class="hidden md:flex items-center gap-8 text-sm font-medium text-slate-400">
                <a href="#features" class="hover:text-white transition">Benefícios</a>
                <a href="#pricing" class="hover:text-white transition">Planos</a>
                <a href="#faq" class="hover:text-white transition">Suporte</a>
            </div>
            <div class="flex items-center gap-4">
                <button onclick="openModal('loginModal')" class="text-sm font-medium text-slate-300 hover:text-white transition">Entrar</button>
                <button onclick="openModal('registerModal')" class="bg-blue-600 hover:bg-blue-500 text-white px-4 py-2 rounded-lg text-sm font-medium transition glow-effect">Cadastrar</button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-24 pb-20 text-center">
        <span class="inline-flex items-center gap-1.5 px-3 py-1 text-xs font-medium text-blue-400 bg-blue-500/10 rounded-full border border-blue-500/20 mb-6">
            <span class="w-1.5 h-1.5 rounded-full bg-blue-400 animate-pulse"></span> Servidor Ultra Estável
        </span>
        <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight max-w-4xl mx-auto leading-none mb-6">
            Acesso instantâneo ao melhor conteúdo em <span class="bg-gradient-to-r from-blue-400 to-indigo-500 bg-clip-text text-transparent">Ultra HD</span>
        </h1>
        <p class="text-lg text-slate-400 max-w-2xl mx-auto mb-10">
            Estabilidade absoluta sem travamentos. Conecte todos os seus dispositivos na plataforma mais rápida do mercado com suporte ativo 24 horas.
        </p>
        <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
            <a href="#pricing" class="w-full sm:w-auto bg-blue-600 hover:bg-blue-500 text-white px-8 py-4 rounded-xl font-semibold transition text-lg shadow-lg shadow-blue-600/20">Escolher Plano</a>
            <button onclick="redirectToWhatsApp('teste')" class="w-full sm:w-auto bg-slate-900 hover:bg-slate-800 border border-slate-800 text-white px-8 py-4 rounded-xl font-semibold transition text-lg flex items-center justify-center gap-2">
                <i data-lucide="message-circle" class="w-5 h-5 text-green-400"></i> Teste Grátis no WhatsApp
            </button>
        </div>
    </section>

    <!-- Features Grid -->
    <section id="features" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 border-t border-slate-900">
        <div class="text-center mb-16">
            <h2 class="text-3xl font-bold tracking-tight">Por que escolher nossa infraestrutura?</h2>
            <p class="text-slate-400 mt-2">Tecnologia de ponta para garantir sua melhor experiência.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="glass-card p-8 rounded-2xl">
                <div class="w-12 h-12 bg-blue-500/10 rounded-xl flex items-center justify-center mb-6 border border-blue-500/20">
                    <i data-lucide="tv" class="text-blue-400 w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-semibold mb-2">Máxima Qualidade</h3>
                <p class="text-slate-400 text-sm leading-relaxed">Transmissões puras em 4K e Full HD com taxa de quadros otimizada para eventos esportivos e ação fluida.</p>
            </div>
            <div class="glass-card p-8 rounded-2xl">
                <div class="w-12 h-12 bg-purple-500/10 rounded-xl flex items-center justify-center mb-6 border border-purple-500/20">
                    <i data-lucide="shield-check" class="text-purple-400 w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-semibold mb-2">99.9% de Uptime</h3>
                <p class="text-slate-400 text-sm leading-relaxed">Servidores redundantes de última geração que evitam quedas e congelamentos nos horários de pico.</p>
            </div>
            <div class="glass-card p-8 rounded-2xl">
                <div class="w-12 h-12 bg-emerald-500/10 rounded-xl flex items-center justify-center mb-6 border border-emerald-500/20">
                    <i data-lucide="smartphone" class="text-emerald-400 w-6 h-6"></i>
                </div>
                <h3 class="text-xl font-semibold mb-2">Multiplataforma</h3>
                <p class="text-slate-400 text-sm leading-relaxed">Compatibilidade nativa com Smart TVs, smartphones, TV Box, notebooks e sistemas operacionais modernos.</p>
            </div>
        </div>
    </section>

    <!-- Pricing Cards -->
    <section id="pricing" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 border-t border-slate-900 relative">
        <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[400px] h-[400px] bg-indigo-600/5 blur-[100px] rounded-full pointer-events-none"></div>
        <div class="text-center mb-16">
            <h2 class="text-3xl font-bold tracking-tight">Planos Diretos & Transparentes</h2>
            <p class="text-slate-400 mt-2">Escolha o período ideal para o seu perfil e economize.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto items-center">
            <!-- Mensal -->
            <div class="glass-card p-8 rounded-2xl relative border-slate-800">
                <h3 class="text-xl font-bold">Acesso Mensal</h3>
                <p class="text-slate-400 text-sm mt-1">Ideal para testar a estabilidade</p>
                <div class="my-6">
                    <span class="text-4xl font-extrabold text-white">R$ 35</span>
                    <span class="text-slate-400 text-sm">/ 30 dias</span>
                </div>
                <ul class="space-y-4 text-sm text-slate-300 mb-8">
                    <li class="flex items-center gap-3.5"><i data-lucide="check" class="text-blue-500 w-4 h-4"></i> Canais, Filmes e Séries inclusos</li>
                    <li class="flex items-center gap-3.5"><i data-lucide="check" class="text-blue-500 w-4 h-4"></i> Qualidade SD, HD e 4K</li>
                    <li class="flex items-center gap-3.5"><i data-lucide="check" class="text-blue-500 w-4 h-4"></i> Atualizações automáticas de catálogo</li>
                    <li class="flex items-center gap-3.5"><i data-lucide="check" class="text-blue-500 w-4 h-4"></i> Suporte via WhatsApp</li>
                </ul>
                <button onclick="redirectToWhatsApp('mensal')" class="block w-full text-center bg-slate-900 hover:bg-slate-800 border border-slate-800 text-white font-medium py-3 rounded-xl transition">Contratar Mensal</button>
            </div>
            <!-- Anual -->
            <div class="glass-card p-8 rounded-2xl relative border-blue-500/30 ring-1 ring-blue-500/30 overflow-hidden shadow-xl">
                <div class="absolute top-0 right-0 bg-blue-600 text-white text-[10px] uppercase font-extrabold px-3 py-1 rounded-bl-xl tracking-wider">Melhor Valor</div>
                <h3 class="text-xl font-bold">Acesso Anual</h3>
                <p class="text-blue-400 text-sm mt-1">Economia massiva de longo prazo</p>
                <div class="my-6">
                    <span class="text-4xl font-extrabold text-white">R$ 300</span>
                    <span class="text-slate-400 text-sm">/ 12 meses</span>
                </div>
                <ul class="space-y-4 text-sm text-slate-300 mb-8">
                    <li class="flex items-center gap-3.5"><i data-lucide="check" class="text-blue-500 w-4 h-4"></i> Todos os benefícios do Mensal</li>
                    <li class="flex items-center gap-3.5"><i data-lucide="check" class="text-blue-500 w-4 h-4"></i> Economia superior a 25% anual</li>
                    <li class="flex items-center gap-3.5"><i data-lucide="check" class="text-blue-500 w-4 h-4"></i> Ativação imediata prioritária</li>
                    <li class="flex items-center gap-3.5"><i data-lucide="check" class="text-blue-500 w-4 h-4"></i> Suporte VIP dedicado</li>
                </ul>
                <button onclick="redirectToWhatsApp('anual')" class="block w-full text-center bg-blue-600 hover:bg-blue-500 text-white font-semibold py-3 rounded-xl transition glow-effect">Contratar Anual</button>
            </div>
        </div>
    </section>

    <!-- MODAL: LOGIN -->
    <div id="loginModal" class="fixed inset-0 bg-slate-950/60 backdrop-blur-md hidden items-center justify-center z-50 p-4 transition-all duration-300">
        <div class="bg-slate-900 border border-slate-800 w-full max-w-md p-8 rounded-2xl shadow-2xl relative">
            <button onclick="closeModal('loginModal')" class="absolute top-4 right-4 text-slate-400 hover:text-white transition">
                <i data-lucide="x" class="w-5 h-5"></i>
            </button>
            <h3 class="text-2xl font-bold mb-2">Acessar Painel</h3>
            <p class="text-sm text-slate-400 mb-6">Insira suas credenciais para entrar na plataforma.</p>
            <form class="space-y-4" onsubmit="event.preventDefault();">
                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2">Usuário ou E-mail</label>
                    <input type="text" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-slate-100 focus:outline-none focus:border-blue-500 transition text-sm" placeholder="seu_usuario">
                </div>
                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2">Senha</label>
                    <input type="password" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-slate-100 focus:outline-none focus:border-blue-500 transition text-sm" placeholder="••••••••">
                </div>
                <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 text-white font-medium py-3 rounded-xl transition mt-2 glow-effect">Entrar</button>
            </form>
            <p class="text-center text-sm text-slate-400 mt-6">
                Não tem uma conta? <button onclick="switchModal('loginModal', 'registerModal')" class="text-blue-400 hover:underline font-medium">Cadastre-se</button>
            </p>
        </div>
    </div>

    <!-- MODAL: CADASTRO -->
    <div id="registerModal" class="fixed inset-0 bg-slate-950/60 backdrop-blur-md hidden items-center justify-center z-50 p-4 transition-all duration-300">
        <div class="bg-slate-900 border border-slate-800 w-full max-w-md p-8 rounded-2xl shadow-2xl relative">
            <button onclick="closeModal('registerModal')" class="absolute top-4 right-4 text-slate-400 hover:text-white transition">
                <i data-lucide="x" class="w-5 h-5"></i>
            </button>
            <h3 class="text-2xl font-bold mb-2">Criar Nova Conta</h3>
            <p class="text-sm text-slate-400 mb-6">Preencha os dados abaixo para se registrar.</p>
            <form class="space-y-4" onsubmit="event.preventDefault();">
                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2">Nome Completo</label>
                    <input type="text" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-slate-100 focus:outline-none focus:border-blue-500 transition text-sm" placeholder="Seu Nome">
                </div>
                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2">E-mail</label>
                    <input type="email" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-slate-100 focus:outline-none focus:border-blue-500 transition text-sm" placeholder="nome@provedor.com">
                </div>
                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-400 mb-2">Senha</label>
                    <input type="password" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-slate-100 focus:outline-none focus:border-blue-500 transition text-sm" placeholder="Mínimo 6 caracteres">
                </div>
                <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 text-white font-medium py-3 rounded-xl transition mt-2 glow-effect">Finalizar Cadastro</button>
            </form>
            <p class="text-center text-sm text-slate-400 mt-6">
                Já possui uma conta? <button onclick="switchModal('registerModal', 'loginModal')" class="text-blue-400 hover:underline font-medium">Fazer Login</button>
            </p>
        </div>
    </div>

    <!-- Footer -->
    <footer class="border-t border-slate-900 bg-slate-950 py-8 text-center text-xs text-slate-500">
        <p>&copy; 2026 Plataforma Premium. Todos os direitos reservados.</p>
    </footer>

    <!-- Lógica de Controle dos Modais e Redirecionamento de Vendas -->
    <script>
        // Inicialização dos Ícones Vetoriais
        lucide.createIcons();

        // Configuração Centralizada do WhatsApp de Vendas
        // IMPORTANTE: Insira aqui o formato 55 + DDD + SEU NÚMERO (apenas números, sem espaços ou traços)
        const WHATSAPP_NUMBER = "5534991926047"; 

        function redirectToWhatsApp(type) {
            let message = "";
            
            switch(type) {
                case 'teste':
                    message = "Olá! Gostaria de solicitar um teste grátis da plataforma para conhecer os canais e a estabilidade.";
                    break;
                case 'mensal':
                    message = "Olá! Gostaria de assinar o Plano Mensal de R$ 35 por 30 dias. Como posso realizar o pagamento?";
                    break;
                case 'anual':
                    message = "Olá! Gostaria de aproveitar a promoção e assinar o Plano Anual de R$ 300 por 12 meses. Como faço para ativar?";
                    break;
                default:
                    message = "Olá! Gostaria de obter mais informações sobre os planos da plataforma.";
            }
            
            const encodedMessage = encodeURIComponent(message);
            const whatsappUrl = `https://api.whatsapp.com/send?phone=${WHATSAPP_+5534991926047}&text=${encodedMessage}`;
            
            // Redireciona na mesma janela para garantir que navegadores locais não bloqueiem como pop-up
            window.location.href = whatsappUrl;
        }

        // Funções de Interface dos Modais
        function openModal(modalId) {
            const modal = document.getElementById(modalId);
            modal.style.display = 'flex';
        }

        function closeModal(modalId) {
            const modal = document.getElementById(modalId);
            modal.style.display = 'none';
        }

        function switchModal(currentModalId, targetModalId) {
            closeModal(currentModalId);
            openModal(targetModalId);
        }

        // Fecha o modal se o usuário clicar na área escura de fundo
        window.onclick = function(event) {
            if (event.target.id === 'loginModal' || event.target.id === 'registerModal') {
                event.target.style.display = 'none';
            }
        }
    </script>
</body>
</html>
