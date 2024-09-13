<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta name="google-site-verification" content="7UtqHJKb0TIKJU7yIO2bSxdwW1MyHX-mW5EcQclj6H4" />
    <title>Bit_nit-Serviços de Tecnologia</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Courier New', monospace;
            background: black;
            color: green;
            overflow-x: hidden;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .main-section {
            position: relative;
            width: 100%;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            z-index: 1;
        }

        .matrix {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
            overflow: hidden;
            background: black;
        }

        .matrix-code {
            position: absolute;
            color: green;
            font-size: 20px;
            white-space: nowrap;
            opacity: 0;
            animation: animate 5s linear infinite;
        }

        @keyframes animate {
            0% {
                transform: translateY(-100%);
                opacity: 1;
            }
            100% {
                transform: translateY(100%);
                opacity: 0;
            }
        }

        .scroll-content {
            width: 100%;
            padding: 20px;
            background: #111;
            color: #eee;
            z-index: 2;
        }

        section {
            padding: 20px;
            background: #222;
            color: #eee;
            margin: 20px 0;
            border-radius: 10px;
        }

        footer {
            background: transparent;
            color: #fff;
            text-align: center;
            padding: 10px;
        }

        .whatsapp-link {
            color: #fff;
            background-color: #21AB72;
            text-decoration: none;
            font-size: 18px;
            font-weight: bold;
            display: inline-block;
            padding: 10px 20px;
            border-radius: 15px;
            margin-top: 10px;
            transition: background-color 0.3s, color 0.3s;
        }

        .whatsapp-link:hover {
            background-color: #128C7E;
            color: #fff;
        }

        .scroll-indicator {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            text-align: center;
            cursor: pointer;
            z-index: 1000;
            opacity: 1;
            transition: opacity 0.5s ease-in-out;
        }

        .arrow {
            width: 0;
            height: 0;
            border-left: 10px solid transparent;
            border-right: 10px solid transparent;
            border-top: 15px solid green;
            animation: blink 1.5s infinite;
        }

        @keyframes blink {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.5;
            }
        }

        .scroll-indicator:hover .arrow {
            border-top-color: #aaa;
        }
    </style>
</head>
<body>
    <div class="main-section">
        <div class="matrix"></div>
        <div class="connect-tech"><h4>Bit_nit______Soluções em Tecnologia, Informação e Comunicação!</h4></div>
    </div>

    <div class="scroll-content">
        <section>
            <div class="content">
                <h2>*___*___*</h2>
                <p style="color: green;">
                    Para você ou sua empresa que busca manutenção ou implementação de sistemas informatizados.<br>
                   · Instalação e manutenção de Sistemas operacionais.<br>
                   · Atualizações e correções de sistemas Linux e Windows.<br>
                   · Transferência de arquivos.
                </p>
            </div>
        </section>

        <section>
            <div class="content">
                <h2>*___*___*</h2>
                <p style="color: green;">
                    Melhore a forma que você se relaciona com a internet.<br>
                   · Backup e restauração de dados.<br>
                   · Recuperação de senhas.<br>
                   · Configuração de redes.
                </p>
            </div>
        </section>

        <section>
            <div class="content">
                <h2>*___*___*</h2>
                <p style="color: green;">
                    Solução em consultoria em TI.<br>
                   · Desinfecção de vírus e malware.<br>
                   · Consultoria em Tecnologia da Informação e Comunicação.
                </p>
            </div>
        </section>

        <section>
            <div class="content">
                <h2>*___*___*</h2>
                <p style="color: green;">
                    Serviços especializados para smartphones Android:<br>
                   · Reparos e manutenção de softwares Android.<br>
                   · Suporte técnico para aplicativos e sistemas.
                </p>
            </div>
        </section>
    </div>

    <footer>
        <p><a href="https://wa.me/48999830912" class="whatsapp-link">Clique aqui para falar conosco!</a></p>
    </footer>

    <div class="scroll-indicator" id="scrollIndicator">
        <div class="arrow"></div>
    </div>

    <script>
        // Função para criar os elementos de código Matrix
        function createMatrixCode() {
            const matrix = document.querySelector('.matrix');
            const code = document.createElement('span');
            code.className = 'matrix-code';
            code.innerHTML = Math.random() < 0.5 ? '0' : '1';
            code.style.left = `${Math.random() * 100}%`;
            code.style.fontSize = `${Math.random() * 20 + 10}px`;

            // Alterar o tempo de animação para melhorar o efeito
            code.style.animationDuration = `${Math.random() * 5 + 5}s`;

            matrix.appendChild(code);
            code.addEventListener('animationend', () => {
                code.remove();
            });
        }

        setInterval(createMatrixCode, 100);  // Intervalo ajustado para criar mais elementos

        // Função para controlar a visibilidade do indicador de rolagem
        function handleScroll() {
            const scrollIndicator = document.getElementById('scrollIndicator');
            scrollIndicator.style.opacity = window.scrollY > 100 ? '0' : '1';
        }

        window.addEventListener('scroll', handleScroll);
    </script>
</body>
</html>
