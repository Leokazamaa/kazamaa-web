<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Casa na Web - Soluções Digitais</title>
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
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 40px;
            margin-top: 20px;
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
            max-width: 1200px;
            font-size: 1.8rem;
            color: #38bdf8;
            margin: 40px 0 20px 0;
            border-bottom: 2px solid #1e293b;
            padding-bottom: 10px;
            text-align: left;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 25px;
            max-width: 1200px;
            width: 100%;
        }

        .card {
            background-color: #1e293b;
            border: 1px solid #334155;
            border-radius: 12px;
            padding: 30px;
            width: 320px;
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
    </style>
</head>
<body>

    <header>
        <h1>Casa na Web</h1>
        <p>Sua plataforma completa de entretenimento, inteligência artificial e recargas</p>
    </header>

    <h2 class="section-title">Planos de Entretenimento (Canais Liberados)</h2>
    <div class="container">
        <div class="card">
            <div>
                <h2>Teste Grátis</h2>
                <div class="price">R$ 0</div>
                <ul class="features">
                    <li>Conheça a plataforma</li>
                    <li>Canais liberados</li>
                    <li>Alta estabilidade</li>
                    <li>Suporte garantido</li>
                </ul>
            </div>
            <button class="btn btn-secondary" onclick="enviarPedido('teste')">Solicitar Teste</button>
        </div>

        <div class="card featured">
            <div class="badge">Mais Vendido</div>
            <div>
                <h2>Plano Mensal</h2>
                <div class="price">R$ 35 <span>/ mês</span></div>
                <ul class="features">
                    <li>Acesso por 30 dias</li>
                    <li>Canais liberados</li>
                    <li>Estabilidade máxima</li>
                    <li>Suporte via operadoras principais</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('mensal')">Assinar Agora</button>
        </div>

        <div class="card">
            <div>
                <h2>Plano Anual</h2>
                <div class="price">R$ 300 <span>/ 12 meses</span></div>
                <ul class="features">
                    <li>Acesso por 1 ano completo</li>
                    <li>Super desconto promocional</li>
                    <li>Canais liberados em HD/4K</li>
                    <li>Suporte prioritário</li>
                </ul>
            </div>
            <button class="btn btn-secondary" onclick="enviarPedido('anual')">Aproveitar Promoção</button>
        </div>
    </div>

    <h2 class="section-title">Acessos a Inteligência Artificial</h2>
    <div class="container">
        <div class="card">
            <div>
                <h2>Grok Pro</h2>
                <div class="price">R$ 49,90 <span>/ 30 dias</span></div>
                <ul class="features">
                    <li>Acesso à tecnologia Grok</li>
                    <li>Geração de imagens de ponta</li>
                    <li>Respostas rápidas e precisas</li>
                    <li>Ideal para criadores de conteúdo</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('grok')">Adquirir Grok</button>
        </div>

        <div class="card featured">
            <div class="badge">Exclusivo</div>
            <div>
                <h2>Leonardo I.A. (ELIS)</h2>
                <div class="price">R$ 25 <span>/ todos os dias</span></div>
                <ul class="features">
                    <li>Sistema Inteligente Integrado</li>
                    <li>Autonomia total de decisões</li>
                    <li>Desenvolvimento personalizado</li>
                    <li>Tecnologia sob medida</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarPedido('leonardo')">Contratar Sistema</button>
        </div>

        <div class="card">
            <div>
                <h2>Gemini Pro</h2>
                <div class="price">R$ 49,90 <span>/ 30 dias</span></div>
                <ul class="features">
                    <li>Acesso avançado à plataforma</li>
                    <li>Análise de dados avançada</li>
                    <li>Integração total com ferramentas</li>
                    <li>Produtividade máxima</li>
                </ul>
            </div>
            <button class="btn btn-secondary" onclick="enviarPedido('gemini')">Adquirir Gemini</button>
        </div>
    </div>

    <h2 class="section-title">Recarga de Celular Integrada</h2>
    <div class="container" style="margin-bottom: 60px;">
        <div class="card" style="width: 400px;">
            <div>
                <h2>Recarregue Agora</h2>
                <p style="color: #94a3b8; margin-bottom: 20px; font-size: 0.95rem;">Selecione sua operadora para realizar a recarga de forma rápida e segura.</p>
                
                <select id="operadora" class="operator-select">
                    <option value="TIM">TIM</option>
                    <option value="Claro">Claro</option>
                    <option value="Vivo">Vivo</option>
                    <option value="Oi">Oi</option>
                    <option value="Algar">Algar Telecom</option>
                </select>

                <ul class="features">
                    <li>Créditos caem na hora</li>
                    <li>Disponível para todas as regiões</li>
                    <li>Pagamento facilitado e seguro</li>
                </ul>
            </div>
            <button class="btn" onclick="enviarRecarga()">Solicitar Recarga</button>
        </div>
    </div>

    <script>
        function enviarPedido(type) {
            let message = "";

            switch(type) {
                case 'teste':
                    message = "Olá! Gostaria de solicitar um teste grátis da plataforma para conhecer os canais e a estabilidade.";
                    break;
                case 'mensal':
                    message = "Olá! Gostaria de assinar o Plano Mensal de R$ 35 por 30 dias. Como posso realizar o pagamento?";
                    break;
                case 'anual':
                    message = "Olá! Gostaria de aproveitar a promoção e assinar o Plano Anual de R$ 300 por 12 meses. Como faço para aderir?";
                    break;
                case 'grok':
                    message = "Olá! Tenho interesse no acesso ao Grok Pro por R$ 49,90 por 30 dias. Como faço para adquirir?";
                    break;
                case 'leonardo':
                    message = "Olá! Quero contratar o sistema integrado com a Inteligência Artificial Leonardo I.A. (ELIS) pelo valor diário de R$ 25.";
                    break;
                case 'gemini':
                    message = "Olá! Tenho interesse no plano avançado do Gemini Pro por R$ 49,90 por 30 dias. Como posso assinar?";
                    break;
                default:
                    message = "Olá! Gostaria de obter mais informações sobre os serviços da plataforma.";
            }

            dispararWhatsapp(message);
        }

        function enviarRecarga() {
            const operadoraSelecionada = document.getElementById('operadora').value;
            const message = `Olá! Gostaria de realizar uma recarga de celular para a operadora ${operadoraSelecionada}. Como posso proceder com o pagamento?`;
            dispararWhatsapp(message);
        }

        function dispararWhatsapp(message) {
            const encodedMessage = encodeURIComponent(message);
            const whatsappUrl = `https://api.whatsapp.com/send?phone=5534991926047&text=${encodedMessage}`;
            window.location.href = whatsappUrl;
        }
    </script>

</body>
</html>
