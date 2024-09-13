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
            justify-content: flex-start;
            align-items: center;
        }

        .main-section {
            position: relative;
            width: 100%;
            height: 150vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            z-index: 1;
        }

        .matrix {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .connect-tech {
            font-size: 20px;
            opacity: 1;
            text-align: center;
            z-index: 1;
            position: absolute;
            top: 10%;
            transform: translateY(-10%);
        }

        .matrix-code {
            display: block;
            font-size: 24px;
            opacity: 0;
            position: absolute;
            animation: animate 5s linear infinite;
            white-space: nowrap;
        }

        @keyframes animate {
            0%, 100% {
                transform: translateY(0);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                transform: translateY(150vh);
            }
        }

        @keyframes beta-gradient {
            0% {
                background-position: 0 0;
            }
            100% {
                background-position: 100% 0;
            }
        }

        .colorbar {
            width: 100%;
            height: 200px;
            background: linear-gradient(to right, #B294FF, #57E6E6, #FEFFB8, #57E6E6, #B294FF, #57E6E6);
            background-size: 500% auto;
            animation: beta-gradient 3s linear infinite;
            position: relative;
            overflow: hidden;
        }

        .colorbar::after {
            content: "";
            width: 100%;
            height: 200px;
            position: absolute;
            top: 0;
            left: 0;
            background-image: linear-gradient(135deg, #ffffff00, #ffffff2e 50%, #ffffff00 95%), url(https://i.imgur.com/rRPChfA.png);
            animation: beta-gradient 40s linear infinite;
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
            border-bottom: 1px solid #444;
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
        <div class="connect-tech"><h4>Bit_nit______Soluções em Tecnologia, Informação e Comunicação!</h4>h4></div>
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
        const matrix = document.querySelector('.matrix');
        const scrollIndicator = document.getElementById('scrollIndicator');

        function createMatrixCode() {
            const code = document.createElement('span');
            code.className = 'matrix-code';
            code.innerHTML = Math.random() < 0.5 ? '0' : '1';
            code.style.left = `${Math.random() * 100}%`;
            code.style.top = `${Math.random() * -100}px`;
            code.style.animationDuration = `${Math.random() * 4 + 4}s`;
            code.style.fontSize = `${Math.random() * 10 + 5}px`;

            matrix.appendChild(code);
            code.addEventListener('animationend', () => {
                code.remove();
            });
        }

        setInterval(createMatrixCode, 300);

        function handleScroll() {
            if (window.scrollY > 100) {
                scrollIndicator.style.opacity = '0';
            } else {
                scrollIndicator.style.opacity = '1';
            }
        }

        window.addEventListener('scroll', handleScroll);
    </script>

    <!-- Carregar Firebase após o carregamento da página -->
    <script type="module" defer>
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.6.0/firebase-app.js";
        import { getAnalytics } from "https://www.gstatic.com/firebasejs/10.6.0/firebase-analytics.js";

        const firebaseConfig = {
            apiKey: "AIzaSyAnufuTXRKhtOpYP5AipXd2hf8AqwrHIpw",
            authDomain: "connect-3e9c9.firebaseapp.com",
            projectId: "connect-3e9c9",
            storageBucket: "connect-3e9c9.appspot.com",
            messagingSenderId: "150149446118",
            appId: "1:150149446118:web:27524a7e3d19275761fe27",
            measurementId: "G-T55280126P"
        };

        const app = initializeApp(firebaseConfig);
        const analytics = getAnalytics(app);
    </script>
</body>
</html>
