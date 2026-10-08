```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EcoWash - TCC Sabão em Pó</title>
    
    <style>
        /* Reset básico */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        /* Variáveis de Cores */
        :root {
            --azul-primario: #0056b3;
            --verde-eco: #28a745;
            --fundo-claro: #f4f7f6;
            --texto-escuro: #333;
        }

        /* Cabeçalho */
        header {
            background-color: var(--azul-primario);
            color: white;
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        header .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 1.5rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
        }

        nav a:hover {
            color: var(--verde-eco);
        }

        /* Seções Gerais */
        .secao {
            padding: 4rem 5%;
            text-align: center;
        }

        .bg-claro {
            background-color: var(--fundo-claro);
        }

        h2 {
            color: var(--azul-primario);
            margin-bottom: 2rem;
            font-size: 2rem;
        }

        /* Botões */
        .btn {
            background-color: var(--verde-eco);
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            border: none;
            cursor: pointer;
            display: inline-block;
            margin-top: 1rem;
        }

        .btn:hover {
            background-color: #218838;
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--azul-primario);
            color: var(--azul-primario);
        }

        .btn-outline:hover {
            background-color: var(--azul-primario);
            color: white;
        }

        /* Banner Principal (Hero) */
        .hero {
            background: linear-gradient(rgba(0, 86, 179, 0.8), rgba(40, 167, 69, 0.8)), url('https://images.unsplash.com/photo-1582735689369-4fe89db7114c?auto=format&fit=crop&q=80') center/cover;
            height: 70vh;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        /* Cards de Produto */
        .cards {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }

        .card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            width: 300px;
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h3 {
            color: var(--verde-eco);
            margin-bottom: 1rem;
        }

        /* Layout do TCC */
        .tcc-content {
            display: flex;
            justify-content: space-around;
            gap: 2rem;
            text-align: left;
            max-width: 900px;
            margin: 0 auto 2rem auto;
        }

        .tcc-content ul {
            margin-left: 20px;
            margin-top: 10px;
        }

        /* Calculadora */
        .calc-box {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            max-width: 500px;
            margin: 0 auto;
        }

        .calc-box input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1rem;
        }

        .resultado-escondido {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background-color: #e9f7ef;
            border-left: 5px solid var(--verde-eco);
            text-align: left;
        }

        /* Rodapé */
        footer {
            background-color: var(--texto-escuro);
            color: white;
            text-align: center;
            padding: 2rem;
        }

        footer p {
            margin-bottom: 0.5rem;
        }
    </style>
</head>
<body>

    <!-- Cabeçalho -->
    <header>
        <div class="logo">EcoWash TCC</div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#produto">O Produto</a></li>
                <li><a href="#tcc">O Projeto (TCC)</a></li>
                <li><a href="#calculadora">Calculadora</a></li>
            </ul>
        </nav>
    </header>

    <!-- Seção Home -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>A Revolução da Limpeza Sustentável</h1>
            <p>Fórmula 100% biodegradável, máximo rendimento e respeito ao meio ambiente.</p>
            <a href="#produto" class="btn">Conheça a Inovação</a>
        </div>
    </section>

    <!-- Seção O Produto -->
    <section id="produto" class="secao">
        <h2>O Produto & Diferenciais Técnicos</h2>
        <div class="cards">
            <div class="card">
                <h3>🌿 Sustentabilidade</h3>
                <p>Tensoativos ecológicos e ausência total de fosfatos que poluem os rios.</p>
            </div>
            <div class="card">
                <h3>💧 Economia de Água</h3>
                <p>Fórmula de fácil enxágue, reduzindo o uso de água na máquina.</p>
            </div>
            <div class="card">
                <h3>🔬 Poder Enzimático</h3>
                <p>Remove manchas difíceis mesmo em lavagens com água fria.</p>
            </div>
        </div>
    </section>

    <!-- Seção O Projeto (TCC) -->
    <section id="tcc" class="secao bg-claro">
        <h2>O Projeto Acadêmico</h2>
        <div class="tcc-content">
            <div>
                <h3>Justificativa</h3>
                <p>Este TCC nasceu da necessidade de criar uma alternativa aos detergentes tradicionais que causam eutrofização das águas. Desenvolvemos uma fórmula eficiente e de baixo impacto.</p>
            </div>
            <div>
                <h3>Resultados de Laboratório</h3>
                <ul>
                    <li><strong>pH:</strong> 9.5 (Ideal para limpeza sem agredir tecidos)</li>
                    <li><strong>Biodegradabilidade:</strong> 98% em 21 dias</li>
                    <li><strong>Solubilidade:</strong> Total a 20°C</li>
                </ul>
            </div>
        </div>
        <div class="download-box">
            <p>Quer ler a pesquisa completa?</p>
            <a href="#" class="btn btn-outline">Baixar Monografia (PDF)</a>
        </div>
    </section>

    <!-- Seção Calculadora -->
    <section id="calculadora" class="secao">
        <h2>Calculadora de Economia</h2>
        <p>Descubra o quanto você economiza usando o nosso sabão em comparação aos tradicionais.</p>
        
        <div class="calc-box">
            <label for="lavagens">Quantas vezes você lava roupa por semana?</label>
            <input type="number" id="lavagens" placeholder="Ex: 3" min="1">
            <button onclick="calcularEconomia()" class="btn">Calcular</button>
            
            <div id="resultado" class="resultado-escondido">
                <!-- O resultado vai aparecer aqui via JavaScript -->
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer>
        <p>Projeto de TCC - Curso de [Seu Curso] | Instituição [Sua Faculdade]</p>
        <p>Equipe: [Seu Nome e do Grupo] | Orientador(a): [Nome do Orientador]</p>
        <p><small>*Este é um projeto acadêmico sem fins comerciais.</small></p>
    </footer>

    <!-- Script da Calculadora -->
    <script>
        function calcularEconomia() {
            const inputLavagens = document.getElementById('lavagens').value;
            const divResultado = document.getElementById('resultado');

            if (inputLavagens === '' || inputLavagens <= 0) {
                alert("Por favor, insira um número válido de lavagens.");
                return;
            }

            const lavagensPorSemana = parseInt(inputLavagens);
            const lavagensPorMes = lavagensPorSemana * 4;

            // Lógica fictícia baseada no seu produto (Ajuste os valores reais do seu TCC)
            // Supondo que o seu sabão usa 50g por lavagem e o tradicional 100g
            const sabaoTradicionalKg = (lavagensPorMes * 100) / 1000;
            const sabaoTCCKg = (lavagensPorMes * 50) / 1000;
            const economiaKg = sabaoTradicionalKg - sabaoTCCKg;

            // Exibindo o resultado
            divResultado.style.display = 'block';
            divResultado.innerHTML = `
                <h3 style="color: #28a745; margin-bottom: 10px;">Seus Resultados Mensais:</h3>
                <p>🧼 <strong>Sabão Tradicional gasto:</strong> ${sabaoTradicionalKg} kg</p>
                <p>🌿 <strong>Nosso Sabão gasto:</strong> ${sabaoTCCKg} kg</p>
                <br>
                <p>✨ <strong>Impacto:</strong> Você deixa de jogar <strong>${economiaKg} kg</strong> de produtos químicos agressivos na natureza por mês, com a mesma eficiência de limpeza!</p>
            `;
        }
    </script>
</body>
</html>

```
