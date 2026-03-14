# 💼 Divino José | Especialista em Soluções e Gestão

Bem-vindo ao repositório da minha landing page profissional. Este projeto foi desenvolvido para centralizar meus serviços de consultoria e facilitar o contato direto com clientes.

## 🚀 Sobre o Projeto
O site apresenta soluções práticas para problemas reais, focado em:
* **Administração & Logística:** Organização de estoque e melhoria de processos.
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Divino José - Consultoria em Administração, RH, Planilhas e Trabalhos Acadêmicos. Soluções rápidas e eficientes.">
    <title>Divino José | Especialista em Soluções e Gestão</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@500;700;800&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary: #0A2540;     
            --primary-light: #1A3C60;
            --accent: #C5A880;      
            --accent-hover: #b0926a;
            --bg-color: #F8F9FA;    
            --text-main: #2D3748;
            --text-muted: #718096;
            --success: #25D366;     
            --white: #FFFFFF;
        }

        html { scroll-behavior: smooth; }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: 'Open Sans', sans-serif; background-color: var(--bg-color); color: var(--text-main); line-height: 1.7; overflow-x: hidden; }
        h1, h2, h3, h4 { font-family: 'Montserrat', sans-serif; font-weight: 700; }

        header {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            color: var(--white); padding: 100px 20px 120px; text-align: center; position: relative;
        }

        .logo-css {
            width: 140px; height: 140px; margin: 0 auto 30px; 
            background-color: var(--white); border-radius: 50%; 
            display: flex; align-items: center; justify-content: center;
            box-shadow: 0 15px 35px rgba(0,0,0,0.3); 
            border: 5px solid var(--accent); position: relative;
            transition: transform 0.3s ease;
        }

        .logo-css:hover { transform: scale(1.05); }

        .logo-initials {
            display: flex; position: relative;
            font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 64px;
            letter-spacing: -6px;
            margin-right: -6px;
        }

        .char-d { color: var(--primary); z-index: 2; position: relative; }
        .char-j { color: var(--accent); position: relative; left: -2px; z-index: 1; }

        .logo-tagline {
            position: absolute; bottom: 18px; left: 50%; transform: translateX(-50%);
            font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 11px;
            color: var(--primary); text-transform: uppercase; letter-spacing: 2px;
            white-space: nowrap;
        }

        header h1 { font-size: 42px; letter-spacing: 1px; margin-bottom: 15px; font-weight: 800; text-transform: uppercase;}
        header p { font-size: 20px; font-weight: 400; color: rgba(255, 255, 255, 0.9); max-width: 600px; margin: 0 auto; }

        .container { max-width: 1050px; margin: -70px auto 40px; padding: 0 20px; position: relative; z-index: 10; }

        .card {
            background: var(--white); border-radius: 24px; padding: 50px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.04); margin-bottom: 40px;
            transition: transform 0.4s ease, box-shadow 0.4s ease; border: 1px solid rgba(0,0,0,0.02);
            opacity: 0; transform: translateY(30px); animation: fadeInUp 0.8s forwards;
        }

        @keyframes fadeInUp { to { opacity: 1; transform: translateY(0); } }
        
        .card:nth-child(1) { animation-delay: 0.1s; }
        .card:nth-child(2) { animation-delay: 0.3s; }
        .card:nth-child(3) { animation-delay: 0.5s; }
        .card:nth-child(4) { animation-delay: 0.7s; }

        .card-title { color: var(--primary); font-size: 28px; margin-bottom: 30px; display: flex; align-items: center; gap: 12px; }
        .card-title i { color: var(--accent); }

        .about-text p { margin-bottom: 15px; font-size: 16px; color: var(--text-main); }
        .about-text strong { color: var(--primary); font-weight: 700;}

        .service-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .service-item {
            border: 1px solid #edf2f7; border-radius: 20px; padding: 35px 25px; background: var(--white);
            display: flex; flex-direction: column; justify-content: space-between; transition: all 0.3s ease;
            position: relative; overflow: hidden;
        }

        .service-item::before {
            content: ''; position: absolute; top: 0; left: 0; width: 100%; height: 5px; background: var(--accent);
            transform: scaleX(0); transition: transform 0.4s ease; transform-origin: left;
        }

        .service-item:hover { border-color: transparent; box-shadow: 0 25px 50px rgba(10,37,64,0.08); transform: translateY(-5px); }
        .service-item:hover::before { transform: scaleX(1); }
        .service-icon { font-size: 38px; color: var(--primary); margin-bottom: 20px; }
        .service-item h3 { font-size: 22px; color: var(--primary); margin-bottom: 12px; }
        .service-item p { color: var(--text-muted); font-size: 15px; margin-bottom: 25px; flex-grow: 1; }
        .price { font-weight: 800; color: var(--accent); font-size: 18px; margin-bottom: 25px; font-family: 'Montserrat', sans-serif; display: block; }

        .btn {
            background: var(--primary); color: var(--white); border: none; padding: 14px 24px; border-radius: 50px;
            cursor: pointer; font-size: 14px; font-weight: 700; font-family: 'Montserrat', sans-serif; text-transform: uppercase;
            letter-spacing: 1px; transition: all 0.3s ease; width: 100%;
        }
        .btn:hover { background: var(--accent); color: var(--white); box-shadow: 0 10px 20px rgba(197,168,128,0.3); }

        .steps-container { display: flex; justify-content: space-between; gap: 20px; text-align: center; margin-top: 20px; flex-wrap: wrap; }
        .step { flex: 1; min-width: 200px; padding: 20px; }
        .step-icon { width: 60px; height: 60px; background: rgba(197,168,128,0.1); color: var(--accent); border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 24px; margin: 0 auto 15px; }
        .step h4 { color: var(--primary); margin-bottom: 10px; }
        .step p { font-size: 14px; color: var(--text-muted); }

        .pix-container { display: flex; align-items: center; justify-content: center; gap: 15px; margin: 25px 0; flex-wrap: wrap; }
        .pix-key {
            font-family: monospace; background: #F7FAFC; padding: 15px 25px; border-radius: 12px;
            font-weight: 800; font-size: 24px; color: var(--primary); border: 2px dashed #CBD5E0; letter-spacing: 1px;
        }
        .btn-copy {
            background-color: var(--primary); color: white; border: none; padding: 15px 25px;
            border-radius: 12px; cursor: pointer; font-weight: bold; font-family: 'Montserrat', sans-serif;
            transition: 0.3s; display: flex; align-items: center; gap: 8px; font-size: 15px;
        }
        .btn-copy:hover { background-color: var(--accent); }
        .btn-copy.copied { background-color: var(--success); }

        .btn-whatsapp-cta {
            display: flex; align-items: center; justify-content: center; gap: 12px; background-color: var(--success);
            color: var(--white); padding: 20px 35px; text-decoration: none; border-radius: 50px; font-weight: 800;
            font-size: 18px; margin-top: 30px; font-family: 'Montserrat', sans-serif; transition: all 0.3s ease;
            box-shadow: 0 10px 25px rgba(37, 211, 102, 0.3); width: 100%; text-transform: uppercase; letter-spacing: 1px;
        }
        .btn-whatsapp-cta:hover { transform: translateY(-3px); box-shadow: 0 15px 30px rgba(37, 211, 102, 0.4); }

        .modal {
            display: none; position: fixed; z-index: 9999; left: 0; top: 0; width: 100%; height: 100%;
            background-color: rgba(10, 37, 64, 0.85); backdrop-filter: blur(8px); opacity: 0; transition: opacity 0.3s ease;
        }
        .modal.show { display: flex; align-items: center; justify-content: center; opacity: 1; }
        .modal-content {
            background-color: var(--white); padding: 50px 40px; border-radius: 24px; width: 90%; max-width: 600px;
            position: relative; transform: scale(0.9); transition: transform 0.3s ease; box-shadow: 0 25px 50px rgba(0,0,0,0.2);
        }
        .modal.show .modal-content { transform: scale(1); }
        .close { position: absolute; right: 25px; top: 20px; font-size: 32px; cursor: pointer; color: #A0AEC0; transition: color 0.3s; }
        .close:hover { color: var(--primary); }
        .modal p { color: var(--text-main); font-size: 16px; margin-bottom: 15px;}
        .modal p strong { color: var(--primary); }

        .whatsapp-float {
            position: fixed; width: 65px; height: 65px; bottom: 30px; right: 30px; background-color: var(--success);
            color: var(--white); border-radius: 50%; display: flex; align-items: center; justify-content: center;
            font-size: 35px; z-index: 8000; box-shadow: 0 10px 20px rgba(37, 211, 102, 0.4); transition: all 0.3s ease; text-decoration: none;
        }
        .whatsapp-float:hover { transform: scale(1.1) rotate(-10deg); }

        footer { text-align: center; font-size: 15px; color: var(--text-muted); padding: 40px 20px 60px; border-top: 1px solid rgba(0,0,0,0.05);}
        footer strong { color: var(--primary); }

        @media (max-width: 768px) {
            .card { padding: 30px 20px; }
            header { padding: 70px 20px 90px; }
            .pix-container { flex-direction: column; }
            .steps-container { flex-direction: column; gap: 10px;}
            header h1 { font-size: 32px; }
            .logo-css { width: 120px; height: 120px; }
            .logo-initials { font-size: 56px; }
            .logo-tagline { font-size: 10px; bottom: 15px;}
        }
    </style>
</head>
<body>

    <a href="https://wa.me/5561995807599?text=Ol%C3%A1%2C%20Divino!%20Vim%20pelo%20seu%20site%20e%20gostaria%20de%20tirar%20uma%20d%C3%BAvida." class="whatsapp-float" target="_blank" title="Falar Agora">
        <i class="fab fa-whatsapp"></i>
    </a>

    <header>
        <div class="logo-css">
            <div class="logo-initials">
                <span class="char-d">D</span>
                <span class="char-j">J</span>
            </div>
            <div class="logo-tagline">Consultoria</div>
        </div>
        <h1>DIVINO JOSÉ</h1>
        <p>A Força da Execução em Administração, Trabalhos e Tecnologia</p>
    </header>

    <div class="container">
        <div class="card">
            <h2 class="card-title"><i class="fas fa-user-shield"></i> Quem executa o seu projeto?</h2>
            <div class="about-text">
                <p>Olá, sou o <strong>Divino José</strong>. Sou estudante de graduação em <strong>Administração e Recursos Humanos</strong>. Não sou uma agência que terceiriza serviços; eu coloco a mão na massa.</p>
                <p>Com resiliência forjada no atendimento de alto fluxo e experiência prática em rigorosos controles de processos logísticos, eu aplico visão técnica e disciplina impecável em tudo o que crio.</p>
                <p>Seja formatando o seu TCC de madrugada ou organizando a planilha do seu negócio, a minha meta é uma só: <strong>resolver o seu problema com excelência e entregar resultados.</strong></p>
            </div>
        </div>

        <div class="card">
            <h2 class="card-title"><i class="fas fa-briefcase"></i> Soluções de Execução Direta</h2>
            <div class="service-grid">
                <div class="service-item">
                    <i class="fas fa-graduation-cap service-icon"></i>
                    <div>
                        <h3>Trabalhos Acadêmicos & ABNT</h3>
                        <p>Eu crio, estruturo e formato. Do zero à adequação rigorosa às normas da ABNT para garantir a sua aprovação.</p>
                        <span class="price">A partir de R$ 50</span>
                    </div>
                    <button class="btn" onclick="openModal('modalAbnt')">Ver Detalhes</button>
                </div>

                <div class="service-item">
                    <i class="fas fa-file-excel service-icon"></i>
                    <div>
                        <h3>Planilhas Inteligentes</h3>
                        <p>Eu construo sistemas automatizados e formulários sob medida para organizar os dados da sua empresa ou rotina.</p>
                        <span class="price">A partir de R$ 80</span>
                    </div>
                    <button class="btn" onclick="openModal('modalPlanilha')">Ver Detalhes</button>
                </div>

                <div class="service-item">
                    <i class="fas fa-boxes service-icon"></i>
                    <div>
                        <h3>Organização de Estoque</h3>
                        <p>Mapeio os seus processos e crio o controle definitivo de entradas e saídas. Fim da perda de mercadoria.</p>
                        <span class="price">Sob consulta</span>
                    </div>
                    <button class="btn" onclick="openModal('modalGestao')">Ver Detalhes</button>
                </div>

                <div class="service-item">
                    <i class="fas fa-user-tie service-icon"></i>
                    <div>
                        <h3>Currículo de Alto Impacto</h3>
                        <p>Analiso e reescrevo a sua trajetória com o olhar técnico de RH para furar o bloqueio dos softwares de seleção.</p>
                        <span class="price">Consultar valor</span>
                    </div>
                    <button class="btn" onclick="openModal('modalCurriculo')">Ver Detalhes</button>
                </div>
            </div>
        </div>

        <div class="card">
            <h2 class="card-title"><i class="fas fa-bolt"></i> Início Imediato via PIX</h2>
            <div class="pix-container">
                <span class="pix-key">715.511.371-94</span>
                <button class="btn-copy" id="btnCopyPix" onclick="copyPix()">
                    <i class="far fa-copy"></i> Copiar Chave
                </button>
            </div>
            <p style="text-align: center; margin-bottom: 20px; color: var(--text-muted);">Favorecido: <strong>Divino José Silva Mota</strong></p>
            <a href="https://wa.me/5561995807599?text=Ol%C3%A1%2C%20Divino!%20Gostaria%20de%20iniciar%20um%20projeto%20com%20voc%C3%AA." class="btn-whatsapp-cta" target="_blank">
                <i class="fab fa-whatsapp"></i> FALAR DIRETAMENTE COMIGO
            </a>
        </div>

        <footer>
            <strong>Divino José Silva Mota</strong><br>
            © 2026 - Onde a Estratégia encontra a Execução.
        </footer>
    </div>

    <div id="modalAbnt" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('modalAbnt')">&times;</span>
            <h3>Trabalhos e Formatação ABNT</h3>
            <p>Eu pesquiso, redijo e estruturo o seu TCC ou artigo de ponta a ponta.</p>
            <a href="https://wa.me/5561995807599" class="btn-whatsapp-cta">Enviar Detalhes</a>
        </div>
    </div>
    <script>
        function copyPix() {
            const pixKeyRaw = "71551137194";
            navigator.clipboard.writeText(pixKeyRaw).then(function() {
                const btn = document.getElementById("btnCopyPix");
                btn.innerHTML = '<i class="fas fa-check"></i> Copiada!';
                setTimeout(() => btn.innerHTML = '<i class="far fa-copy"></i> Copiar Chave', 3000);
            });
        }
        function openModal(id) { 
            const m = document.getElementById(id); m.style.display = "flex"; 
            setTimeout(() => m.classList.add('show'), 10);
        }
        function closeModal(id) { 
            const m = document.getElementById(id); m.classList.remove('show'); 
            setTimeout(() => m.style.display = "none", 300);
        }
    </script>
</body>
</html>* **Recursos Humanos:** Elaboração de currículos estratégicos para o mercado atual.
* **Trabalhos Acadêmicos:** Consultoria e formatação completa nas normas ABNT.
* **Tecnologia:** Criação de planilhas inteligentes e automações.

## 🛠️ Tecnologias
- HTML5 / CSS3 (Design responsivo e Logo em CSS)
- JavaScript (Funcionalidades de Modal e Clipboard)
- Font Awesome & Google Fonts

## 📬 Contato
Estou localizado em Santo Antônio do Descoberto - GO e atendo toda a região e online.
- **WhatsApp:** (https://wa.me/5561995807599)


---
*Este projeto está hospedado via GitHub Pages.*
