<title>KAZAMA-WEB - Soluções Digitais</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<style>
    * { 
        margin: 0; 
        padding: 0; 
        box-sizing: border-box; 
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
    }
    
    body {
        background-color: #0f172a;
        color: #f8fafc;
        display: flex;
        flex-direction: column;
        align-items: center; /* Centraliza horizontalmente o conteúdo */
        justify-content: flex-start;
        min-height: 100vh;
        padding: 20px;
        width: 100%;
    }

    /* Elemento que envelopa todo o conteúdo para garantir centralização perfeita em telas grandes */
    .wrapper {
        width: 100%;
        max-width: 1000px; /* Impede que o site se espalhe excessivamente em monitores grandes */
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    header {
        text-align: center;
        margin-bottom: 40px;
        margin-top: 20px;
        width: 100%;
    }

    header h1 {
        font-size: 2.5rem;
        color: #38bdf8;
        margin-bottom: 10px;
    }

    header p {
        color: #94a3b8;
        font-size: 1.1rem;
    }

    .section-title {
        width: 100%;
        font-size: 1.8rem;
        color: #38bdf8;
        margin: 40px 0 20px 0;
        border-bottom: 2px solid #1e293b;
        padding-bottom: 10px;
        text-align: left;
    }

    /* Container com Grid configurado para se auto-ajustar e manter centralizado */
    .container {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 25px;
        width: 100%;
        margin-bottom: 20px;
        justify-content: center;
    }

    .card {
        background-color: #1e293b;
        border: 1px solid #334155;
        border-radius: 12px;
        padding: 30px;
        width: 100%;
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        transition: transform 0.2s, border-color 0.2s;
    }

    .card:hover {
        transform: translateY(-5px);
        border-color: #38bdf8;
    }

    .card.featured {
        border: 2px solid #38bdf8;
        position: relative;
    }

    .card.featured .badge {
        position: absolute;
        top: -12px;
        left: 50%;
        transform: translateX(-50%);
        background-color: #38bdf8;
        color: #0f172a;
        padding: 3px 15px;
        border-radius: 20px;
        font-size: 0.8rem;
        font-weight: bold;
        text-transform: uppercase;
    }

    .card-icon {
        font-size: 3rem;
        color: #38bdf8;
        margin-bottom: 15px;
    }

    .card h2 {
        font-size: 1.5rem;
        margin-bottom: 15px;
        color: #f8fafc;
    }

    .price {
        font-size: 2rem;
        font-weight: bold;
        color: #38bdf8;
        margin-bottom: 20px;
    }

    .price span {
        font-size: 1rem;
        color: #94a3b8;
        font-weight: normal;
    }

    .features {
        list-style: none;
        margin-bottom: 30px;
        text-align: left;
    }

    .features li {
        margin-bottom: 10px;
        color: #cbd5e1;
        display: flex;
        align-items: center;
        font-size: 0.95rem;
    }

    .features li::before {
        content: "✓";
        color: #22c55e;
        font-weight: bold;
        margin-right: 8px;
    }

    .btn {
        background-color: #38bdf8;
        color: #0f172a;
        border: none;
        padding: 12px 20px;
        border-radius: 8px;
        font-size: 1rem;
        font-weight: bold;
        cursor: pointer;
        width: 100%;
        transition: background-color 0.2s;
    }

    .btn:hover {
        background-color: #0ea5e9;
    }

    .btn-secondary {
        background-color: #334155;
        color: #f8fafc;
    }

    .btn-secondary:hover {
        background-color: #475569;
    }

    .operator-select {
        width: 100%;
        padding: 10px;
        background-color: #0f172a;
        color: #f8fafc;
        border: 1px solid #334155;
        border-radius: 6px;
        margin-bottom: 20px;
        font-size: 1rem;
    }

    .container-recarga {
        display: flex;
        justify-content: center;
        width: 100%;
        margin-bottom: 60px;
    }

    /* Responsividade para tablets e celulares menores */
    @media (max-width: 600px) {
        .container {
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            padding: 5px;
        }
        
        .card {
            padding: 15px;
        }

        .card-icon {
            font-size: 2.2rem;
            margin-bottom: 10px;
        }

        .price {
            font-size: 1.4rem;
        }

        .card h2 {
            font-size: 1.1rem;
        }
    }
</style>

<div class="wrapper">
    <header>
        <h1>Casa na Web</h1>
        <p>Sua plataforma completa de entretenimento, inteligência artificial e soluções digitais</p>
    </header>

    <h2 class="section-title">Planos de Entretenimento (Canais & Streaming)</h2>
    <div class="container">
        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-tv"></i></div>
                <h2>Teste Grátis TV</h2>
                <div class="price">R$ 0</div>
                <ul class="features">
                    <li>Canais ao vivo, Filmes e Séries</li>
                    <li>Netflix, Disney+, GloboPlay</li>
                    <li>Paramount, Prime Video e mais</li>
                    <li>Funciona em todas as Smart TVs</li>
                </ul>
            </div>
            <button class="btn btn-secondary" onclick="enviarPedido('teste')">Solicitar Teste</button>
        </div>

        <div class="card featured">
            <div class="badge">Mais Vendido</div>
            <div>
                <div class="card-icon"><i class="fa-solid fa-circle-play"></i></div>
                <h2>Canais + Streaming Mensal</h2>
                <div class="price">R$ 35 <span>/ 30 dias</span></div>
                <ul class="features">
                    <li>Todos os canais liberados</li>
                    <li>Netflix, Disney, Doramas e Animes</li>
                    <li>Estabilidade máxima em HD/4K</li>
                    <li>Funciona em todas as Smart TVs</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('mensal')">Assinar Mensal</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-star"></i></div>
                <h2>Canais + Streaming Anual</h2>
                <div class="price">R$ 300 <span>/ 12 meses</span></div>
                <ul class="features">
                    <li>Acesso completo por 1 ano</li>
                    <li>Super desconto promocional</li>
                    <li>Suporte prioritário garantido</li>
                    <li>Todas as plataformas inclusas</li>
                </ul>
            </div>
            <button class="btn btn-secondary" onclick="enviarPedido('anual')">Assinar Anual</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-film"></i></div>
                <h2>Netflix 4K (1 Tela)</h2>
                <div class="price">R$ 20 <span>/ 30 dias</span></div>
                <ul class="features">
                    <li>Qualidade máxima Ultra HD</li>
                    <li>Acesso individual estável</li>
                    <li>Filmes e séries liberados</li>
                    <li>Sem interrupções</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('netflix')">Adquirir Netflix</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-brands fa-youtube"></i></div>
                <h2>YouTube Premium</h2>
                <div class="price">R$ 20 <span>/ 30 dias</span></div>
                <ul class="features">
                    <li>Vídeos sem propagandas</li>
                    <li>Modo offline e em segundo plano</li>
                    <li>Incluso YouTube Music Premium</li>
                    <li>Assista onde quiser</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('youtube')">Adquirir YouTube</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-music"></i></div>
                <h2>Spotify Premium</h2>
                <div class="price">R$ 20 <span>/ 3 meses</span></div>
                <ul class="features">
                    <li>Músicas sem anúncios</li>
                    <li>Modo offline ativado</li>
                    <li>PROMOÇÃO EXCLUSIVA</li>
                    <li>Alta qualidade de áudio</li>
                </ul>
            </div>
            <button class="btn btn-secondary" onclick="enviarPedido('spotify')">Adquirir Spotify</button>
        </div>
    </div>

    <h2 class="section-title">Acessos a Inteligência Artificial & Edição</h2>
    <div class="container">
        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-wand-magic-sparkles"></i></div>
                <h2>Gemini Pro</h2>
                <div class="price">R$ 49,90 <span>/ 30 dias</span></div>
                <ul class="features">
                    <li>Acesso avançado à IA</li>
                    <li>Análise de dados de ponta</li>
                    <li>Produtividade máxima</li>
                </ul>
            </div>
            <button class="btn btn-secondary" onclick="enviarPedido('gemini')">Adquirir Gemini</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-brain"></i></div>
                <h2>ChatGPT Plus</h2>
                <div class="price">R$ 49,90 <span>/ 30 dias</span></div>
                <ul class="features">
                    <li>Acesso ao GPT-4 prioritário</li>
                    <li>Respostas e criações rápidas</li>
                    <li>Ferramentas exclusivas</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('chatgpt')">Adquirir ChatGPT</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-video"></i></div>
                <h2>CapCut Pro</h2>
                <div class="price">R$ 30 <span>/ 30 dias</span></div>
                <ul class="features">
                    <li>Edição de vídeo profissional</li>
                    <li>Efeitos e transições liberados</li>
                    <li>Exportação em alta qualidade</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('capcut')">Adquirir CapCut</button>
        </div>

        <div class="card featured">
            <div class="badge">Exclusivo</div>
            <div>
                <div class="card-icon"><i class="fa-solid fa-robot"></i></div>
                <h2>Leonardo I.A. (ELIS)</h2>
                <div class="price">R$ 25 <span>/ todos os dias</span></div>
                <ul class="features">
                    <li>Sistema Inteligente Integrado</li>
                    <li>Autonomia total de decisões</li>
                    <li>Tecnologia sob medida</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('leonardo')">Contratar Sistema</button>
        </div>
    </div>

    <h2 class="section-title">Games (Assinaturas e Jogos)</h2>
    <div class="container">
        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-xbox"></i></div>
                <h2>Game Pass Ultimate</h2>
                <div class="price">Consulte</div>
                <ul class="features">
                    <li>Disponível para Console e PC</li>
                    <li>Catálogo com centenas de jogos</li>
                    <li>Acesso ao modo online EA Play</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('gamepass')">Consultar Opções</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-gamepad"></i></div>
                <h2>PlayStation Plus</h2>
                <div class="price">Consulte</div>
                <ul class="features">
                    <li>Acesso ao modo multiplayer</li>
                    <li>Jogos mensais gratuitos</li>
                    <li>Descontos exclusivos na PSN</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('psn')">Consultar Planos</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-compact-disc"></i></div>
                <h2>Jogos Digitais Retro & PC</h2>
                <div class="price">A partir de R$ 5</div>
                <ul class="features">
                    <li>PS1, PS2, PSP, Game Boy: R$ 5</li>
                    <li>Xbox 360, PS3: R$ 7</li>
                    <li>Nintendo Wii: R$ 5</li>
                    <li>Jogos de PC: R$ 10</li>
                </ul>
            </div>
            <button class="btn btn-secondary" onclick="enviarPedido('jogos')">Pedir Catálogo</button>
        </div>
    </div>

    <h2 class="section-title">Assistência Técnica & Suporte Online</h2>
    <div class="container">
        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-unlock"></i></div>
                <h2>Desbloqueios de Consoles</h2>
                <div class="price">Consulte</div>
                <ul class="features">
                    <li>Desbloqueio de PlayStation 3</li>
                    <li>Desbloqueio de Nintendo Wii</li>
                    <li>Instalação de lojas e emuladores</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('desbloqueio')">Solicitar Orçamento</button>
        </div>

        <div class="card">
            <div>
                <div class="card-icon"><i class="fa-solid fa-computer"></i></div>
                <h2>Suporte & Sistemas Online</h2>
                <div class="price">Consulte</div>
                <ul class="features">
                    <li>Instalação/Configuração de PC Online</li>
                    <li>Instalação de todos os Sistemas</li>
                    <li>Remoção de Conta Google (FRP)</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('suporte')">Chamar Técnico</button>
        </div>
    </div>

    <h2 class="section-title">Recarga de Celular Integrada</h2>
    <div class="container-recarga">
        <div class="card" style="max-width: 400px;">
            <div>
                <div class="card-icon"><i class="fa-solid fa-mobile-screen-button"></i></div>
                <h2>Recarregue Agora</h2>
                <p style="color: #94a3b8; margin-bottom: 20px; font-size: 0.95rem;">Selecione sua operadora para realizar a recarga de forma rápida e segura.</p>
                
                <select id="operadora" class="operator-select">
                    <option value="TIM">TIM</option>
                    <option value="Claro">Claro</option>
                    <option value="Vivo">Vivo</option>
                </select>

                <ul class="features">
                    <li>Créditos caem na hora</li>
                    <li>Disponível para as principais operadoras</li>
                    <li>Pagamento facilitado e seguro</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarRecarga()">Solicitar Recarga</button>
        </div>
    </div>
</div>

<script>
    function enviarPedido(type) {
        let message = "";

        switch(type) {
            case 'teste':
                message = "Olá! Gostaria de solicitar um test grats do sistema de canais e streaming para testar na minha Smart TV.";
                break;
            case 'mensal':
                message = "Olá! Gostaria de assinar o Plano Mensal de Canais + Streaming por R$ 35 (30 dias). Como faço para pagar?";
                break;
            case 'anual':
                message = "Olá! Quero aproveitar a promoção e adquirir o Plano Anual de Canais + Streaming por R$ 300 (12 meses).";
                break;
            case 'netflix':
                message = "Olá! Gostaria de adquirir uma tela da Netflix 4K por R$ 20 (30 dias). Como posso realizar o pagamento?";
                break;
            case 'youtube':
                message = "Olá! Gostaria de adquirir o acesso ao YouTube Premium sem propagandas por R$ 20 (30 dias).";
                break;
            case 'spotify':
                message = "Olá! Tenho interesse na promoção do Spotify Premium (3 meses por R$ 20).";
                break;
            case 'gemini':
                message = "Olá! Tenho interesse no acesso ao Gemini Pro por R$ 49,90 por 30 dias.";
                break;
            case 'chatgpt':
                message = "Olá! Tenho interesse no acesso ao ChatGPT Plus por R$ 49,90 por 30 dias.";
                break;
            case 'capcut':
                message = "Olá! Gostaria de adquirir o acesso ao CapCut Pro por R$ 30 por 30 dias.";
                break;
            case 'leonardo':
                message = "Olá! Quero contratar o sistema integrado com a Inteligência Artificial Leonardo I.A. (ELIS) pelo valor diário de R$ 25.";
                break;
            case 'gamepass':
                message = "Olá! Gostaria de consultar os valores e opções para o Game Pass Ultimate / Gamepass Ultimate PC.";
                break;
            case 'psn':
                message = "Olá! Gostaria de informações sobre os planos da PSN Plus.";
                break;
            case 'jogos':
                message = "Olá! Quero consultar o catálogo de jogos digitais. Tenho interesse em jogos de (PC / PS1 / PS2 / PS3 / Xbox 360 / PSP / Nintendo Wii / Game Boy).";
                break;
            case 'desbloqueio':
                message = "Olá! Gostaria de um orçamento para desbloqueio de console (PS3 / Nintendo Wii).";
                break;
            case 'suporte':
                message = "Olá! Preciso de assistência técnica (Instalação e Configurações de PC On-line / Instalação de todos os Sistemas / Remoção de Contas Google).";
                break;
            default:
                message = "Olá! Gostaria de mais informações sobre as soluções digitais da plataforma.";
        }

        dispararWhatsapp(message);
    }

    function enviarRecarga() {
        const operadoraSelecionada = document.getElementById('operadora').value;
        const message = `Olá! Gostaria de realizar uma recarga de celular para a operadora ${operadoraSelecionada} (Tim, Vivo ou Claro). Como posso proceder?`;
        dispararWhatsapp(message);
    }

    function dispararWhatsapp(message) {
        const encodedMessage = encodeURIComponent(message);
        const whatsappUrl = `https://api.whatsapp.com/send?phone=5534991926047&text=${encodedMessage}`;
        window.location.href = whatsappUrl;
    }
</script>
