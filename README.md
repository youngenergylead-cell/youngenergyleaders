<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Young Energy Leaders - Réseau YEL</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #000000 0%, #1a1a1a 50%, #DC143C 100%);
            color: #333;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            color: white;
            padding: 40px 20px 60px;
            animation: fadeIn 1.5s ease-in;
        }

        .logo-container {
            margin-bottom: 30px;
            animation: fadeInDown 1.5s ease-out;
        }

        .logo-container img {
            max-width: 600px;
            width: 90%;
            height: auto;
            background: white;
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(220, 20, 60, 0.4);
        }

        header p {
            font-size: 1.5em;
            margin-top: 20px;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .card {
            background: white;
            border-radius: 20px;
            padding: 40px;
            margin: 30px 0;
            box-shadow: 0 10px 40px rgba(0,0,0,0.3);
            animation: slideUp 0.8s ease-out;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(220, 20, 60, 0.4);
        }

        .section-title {
            color: #DC143C;
            font-size: 2.2em;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 15px;
            border-bottom: 3px solid #DC143C;
            padding-bottom: 15px;
        }

        .icon {
            font-size: 1.2em;
        }

        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .benefit-item {
            padding: 30px;
            background: linear-gradient(135deg, #f5f7fa 0%, #e8e8e8 100%);
            border-radius: 15px;
            transition: all 0.4s ease;
            cursor: pointer;
            border: 3px solid transparent;
        }

        .benefit-item:hover {
            transform: scale(1.08) rotate(2deg);
            background: linear-gradient(135deg, #DC143C 0%, #000000 100%);
            color: white;
            border-color: #DC143C;
            box-shadow: 0 15px 40px rgba(220, 20, 60, 0.5);
        }

        .benefit-item h3 {
            margin-bottom: 15px;
            font-size: 1.3em;
        }

        .values-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }

        .value-badge {
            flex: 1;
            min-width: 220px;
            padding: 30px;
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            border-radius: 15px;
            text-align: center;
            font-weight: bold;
            transition: all 0.4s ease;
            cursor: pointer;
            border: 3px solid transparent;
        }

        .value-badge:hover {
            transform: rotate(-5deg) scale(1.1);
            background: linear-gradient(135deg, #DC143C 0%, #ff6b6b 100%);
            color: white;
            border-color: white;
            box-shadow: 0 10px 30px rgba(220, 20, 60, 0.5);
        }

        .onboarding-steps {
            position: relative;
            margin-top: 30px;
        }

        .step {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin: 25px 0;
            padding: 25px;
            background: #f8f9fa;
            border-radius: 12px;
            border-left: 6px solid #DC143C;
            transition: all 0.4s ease;
            cursor: pointer;
        }

        .step:hover {
            background: #fff5f5;
            transform: translateX(15px);
            box-shadow: 0 8px 25px rgba(220, 20, 60, 0.3);
        }

        .step-number {
            background: #DC143C;
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.3em;
            flex-shrink: 0;
            box-shadow: 0 4px 15px rgba(220, 20, 60, 0.4);
        }

        .cta-section {
            text-align: center;
            padding: 60px 40px;
            background: linear-gradient(135deg, #DC143C 0%, #8B0000 100%);
            color: white;
            border-radius: 20px;
            margin: 40px 0;
            box-shadow: 0 15px 50px rgba(220, 20, 60, 0.5);
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.02); }
        }

        .cta-button {
            display: inline-block;
            padding: 20px 50px;
            background: white;
            color: #DC143C;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.4em;
            margin-top: 30px;
            transition: all 0.4s ease;
            box-shadow: 0 8px 30px rgba(0,0,0,0.3);
            border: 4px solid white;
        }

        .cta-button:hover {
            transform: scale(1.15) rotate(-2deg);
            box-shadow: 0 12px 40px rgba(0,0,0,0.5);
            background: #000000;
            color: white;
            border-color: #DC143C;
        }

        .rewards {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 25px;
            margin-top: 30px;
        }

        .reward-item {
            text-align: center;
            padding: 30px;
            background: linear-gradient(135deg, #fff5b7 0%, #ffd89b 100%);
            border-radius: 15px;
            flex: 1;
            min-width: 220px;
            transition: all 0.4s ease;
            cursor: pointer;
            border: 3px solid transparent;
        }

        .reward-item:hover {
            transform: translateY(-10px) scale(1.05);
            background: linear-gradient(135deg, #FFD700 0%, #FFA500 100%);
            border-color: #DC143C;
            box-shadow: 0 15px 40px rgba(255, 215, 0, 0.5);
        }

        .reward-icon {
            font-size: 3.5em;
            margin-bottom: 15px;
        }

        .social-section {
            background: linear-gradient(135deg, #000000 0%, #DC143C 100%);
            color: white;
            padding: 50px;
            border-radius: 20px;
            margin: 40px 0;
            box-shadow: 0 15px 50px rgba(220, 20, 60, 0.5);
        }

        .social-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            padding: 25px;
            background: white;
            color: #DC143C;
            text-decoration: none;
            border-radius: 15px;
            font-weight: bold;
            font-size: 1.2em;
            transition: all 0.4s ease;
            box-shadow: 0 6px 20px rgba(0,0,0,0.3);
            border: 3px solid transparent;
        }

        .social-link:hover {
            transform: translateY(-8px) scale(1.05);
            box-shadow: 0 12px 35px rgba(255, 255, 255, 0.4);
            background: #DC143C;
            color: white;
            border-color: white;
        }

        .social-icon {
            font-size: 2em;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin-top: 30px;
            font-size: 1.2em;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 20px;
            background: rgba(255,255,255,0.1);
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            background: rgba(255,255,255,0.2);
            transform: translateX(10px);
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        footer {
            text-align: center;
            color: white;
            padding: 50px;
            font-size: 1.1em;
            background: rgba(0,0,0,0.3);
            border-radius: 20px;
            margin-top: 40px;
        }

        footer a {
            color: #FFD700;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        footer a:hover {
            color: white;
            text-decoration: underline;
        }

        @media (max-width: 768px) {
            header p {
                font-size: 1.2em;
            }

            .section-title {
                font-size: 1.6em;
            }

            .benefits-grid {
                grid-template-columns: 1fr;
            }

            .social-links {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo-container">
                <img src="https://www.dropbox.com/scl/fi/spwtisnoifd5l2m3ffqlb/Logo-Yel-fond-blanc-1.jpg?rlkey=6pqd32fxdfmem16hrtxlh85zt&raw=1" alt="Young Energy Leaders Logo" onerror="this.onerror=null; this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 width=%22600%22 height=%22200%22%3E%3Crect fill=%22%23DC143C%22 width=%22600%22 height=%22200%22/%3E%3Ctext x=%2250%25%22 y=%2250%25%22 dominant-baseline=%22middle%22 text-anchor=%22middle%22 font-family=%22Arial%22 font-size=%2240%22 fill=%22white%22 font-weight=%22bold%22%3EYoung Energy Leaders%3C/text%3E%3C/svg%3E';">
            </div>
            <p>⚡ La jeunesse prend le lead énergétique 🌍</p>
        </header>

        <div class="card">
            <h2 class="section-title"><span class="icon">🚀</span> Pourquoi rejoindre YEL ?</h2>
            <p style="font-size: 1.2em; line-height: 1.8; margin-bottom: 20px;">
                Le <strong>Young Energy Leaders (YEL)</strong> est plus qu'un simple réseau : c'est une <strong>communauté de jeunes visionnaires</strong> qui veulent transformer l'avenir énergétique en Afrique et au-delà. Ici, chaque membre a une voix, une place et une mission. 🌍⚡
            </p>

            <div class="benefits-grid">
                <div class="benefit-item">
                    <h3>🤝 Un réseau puissant</h3>
                    <p>Connecte-toi avec des étudiants, des experts et des jeunes leaders passionnés d'énergie.</p>
                </div>
                <div class="benefit-item">
                    <h3>🎓 Formations continues</h3>
                    <p>Ateliers, webinaires et sessions pratiques pour renforcer tes compétences.</p>
                </div>
                <div class="benefit-item">
                    <h3>🔥 Un espace pour briller</h3>
                    <p>Participe à des projets innovants et développe ton leadership.</p>
                </div>
                <div class="benefit-item">
                    <h3>🌱 Un impact concret</h3>
                    <p>Contribue à des initiatives en énergies renouvelables et développement durable.</p>
                </div>
            </div>
        </div>

        <div class="card">
            <h2 class="section-title"><span class="icon">🌍</span> Notre Vision</h2>
            <p style="font-size: 1.3em; text-align: center; padding: 30px; background: linear-gradient(135deg, #ffe0e0 0%, #ffcccc 100%); border-radius: 15px; color: #333; font-weight: 500; line-height: 1.8;">
                <strong style="font-size: 1.3em; color: #DC143C;">✨ La jeunesse prend le lead énergétique ✨</strong><br><br>
                Nous croyons que les jeunes ne sont pas seulement les bénéficiaires de la transition énergétique, mais ses <strong>acteurs principaux</strong>. Ensemble, nous bâtissons un avenir durable, inclusif et innovant.
            </p>
        </div>

        <div class="card">
            <h2 class="section-title"><span class="icon">🔑</span> Nos Valeurs</h2>
            <div class="values-container">
                <div class="value-badge">
                    <div style="font-size: 2.5em; margin-bottom: 15px;">💪</div>
                    <strong style="font-size: 1.2em;">Leadership</strong><br><br>
                    Chaque jeune peut être une force de transformation
                </div>
                <div class="value-badge">
                    <div style="font-size: 2.5em; margin-bottom: 15px;">💡</div>
                    <strong style="font-size: 1.2em;">Innovation</strong><br><br>
                    Trouver des solutions créatives aux défis énergétiques
                </div>
                <div class="value-badge">
                    <div style="font-size: 2.5em; margin-bottom: 15px;">🤝</div>
                    <strong style="font-size: 1.2em;">Solidarité</strong><br><br>
                    Avancer ensemble, main dans la main
                </div>
                <div class="value-badge">
                    <div style="font-size: 2.5em; margin-bottom: 15px;">🌱</div>
                    <strong style="font-size: 1.2em;">Durabilité</strong><br><br>
                    Protéger la planète en agissant maintenant
                </div>
            </div>
        </div>

        <div class="card">
            <h2 class="section-title"><span class="icon">🎯</span> Ton Parcours d'Intégration</h2>
            <div class="onboarding-steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <div>
                        <h3 style="font-size: 1.3em; margin-bottom: 10px;">Accueil chaleureux</h3>
                        <p style="font-size: 1.1em;">Message personnalisé et kit de bienvenue digital</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <div>
                        <h3 style="font-size: 1.3em; margin-bottom: 10px;">Découverte</h3>
                        <p style="font-size: 1.1em;">Présentation de la mission, des projets et des valeurs YEL</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <div>
                        <h3 style="font-size: 1.3em; margin-bottom: 10px;">Action immédiate</h3>
                        <p style="font-size: 1.1em;">Une première tâche simple pour t'impliquer dès le départ</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">4</div>
                    <div>
                        <h3 style="font-size: 1.3em; margin-bottom: 10px;">Accompagnement</h3>
                        <p style="font-size: 1.1em;">Un mentor (buddy) pour t'aider à trouver ta place</p>
                    </div>
                </div>
                <div class="step">
                    <div class="step-number">5</div>
                    <div>
                        <h3 style="font-size: 1.3em; margin-bottom: 10px;">Engagement</h3>
                        <p style="font-size: 1.1em;">Participation à des projets, événements et initiatives concrètes</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="card">
            <h2 class="section-title"><span class="icon">🎖️</span> Et Après ?</h2>
            <p style="font-size: 1.2em; margin-bottom: 30px; font-weight: 500;">À la fin de ton onboarding, tu recevras :</p>
            <div class="rewards">
                <div class="reward-item">
                    <div class="reward-icon">🎖️</div>
                    <strong style="font-size: 1.2em;">Badge Digital YEL</strong><br><br>
                    Confirmation de ton appartenance à la communauté
                </div>
                <div class="reward-item">
                    <div class="reward-icon">🚀</div>
                    <strong style="font-size: 1.2em;">Projet Actif</strong><br><br>
                    Invitation à rejoindre un projet ou comité
                </div>
                <div class="reward-item">
                    <div class="reward-icon">🌟</div>
                    <strong style="font-size: 1.2em;">Ambassadeur YEL</strong><br><br>
                    Possibilité de représenter YEL dans ton campus
                </div>
            </div>
        </div>

        <div class="cta-section">
            <h2 style="font-size: 2.8em; margin-bottom: 25px;">✨ Prêt à transformer l'avenir énergétique ?</h2>
            <p style="font-size: 1.4em; margin-bottom: 20px; line-height: 1.6;">
                Chez YEL, tu ne rejoins pas seulement un réseau…<br>
                <strong style="font-size: 1.2em;">TU DEVIENS UN LEADER DE L'ÉNERGIE</strong>
            </p>
            <a href="https://forms.gle/nEKpbd2bMvRG8N2w5" class="cta-button" target="_blank">
                📝 Rejoindre YEL Maintenant 🚀
            </a>
        </div>

        <div class="social-section">
            <h2 style="font-size: 2.5em; margin-bottom: 20px; text-align: center;">📱 Rejoins Notre Communauté</h2>
            <p style="text-align: center; font-size: 1.3em; margin-bottom: 30px;">Connecte-toi avec nous sur toutes nos plateformes !</p>
            
            <div class="social-links">
                <a href="https://forms.gle/nEKpbd2bMvRG8N2w5" class="social-link" target="_blank">
                    <span class="social-icon">📝</span>
                    <span>Formulaire d'inscription</span>
                </a>
                <a href="https://chat.whatsapp.com/Dy1KBqDsUc47yafnjL5hPG" class="social-link" target="_blank">
                    <span class="social-icon">💬</span>
                    <span>Groupe WhatsApp</span>
                </a>
                <a href="https://www.linkedin.com/company/youngenergyleaders" class="social-link" target="_blank">
                    <span class="social-icon">💼</span>
                    <span>LinkedIn</span>
                </a>
                <a href="https://web.facebook.com/youngenergyleaders" class="social-link" target="_blank">
                    <span class="social-icon">📘</span>
                    <span>Facebook</span>
                </a>
                <a href="mailto:youngenergylead@gmail.com" class="social-link">
                    <span class="social-icon">📧</span>
                    <span>Email</span>
                </a>
            </div>

            <div class="contact-info">
                <div class="contact-item">
                    <span style="font-size: 1.5em;">📧</span>
                    <strong>Email:</strong> youngenergylead@gmail.com
                </div>
                <div class="contact-item">
                    <span style="font-size: 1.5em;">💬</span>
                    <strong>WhatsApp:</strong> Rejoins notre communauté active
                </div>
                <div class="contact-item">
                    <span style="font-size: 1.5em;">🌍</span>
                    <strong>Localisation:</strong> Afrique - Réseau Panafricain
                </div>
            </div>
        </div>

        <footer>
            <p style="font-size: 1.8em; margin-bottom: 20px; font-weight: bold;">🌍⚡ Ensemble, nous écrivons l'avenir 🔋🌍</p>
            <p style="margin-bottom: 30px; font-size: 1.2em;">Young Energy Leaders - La communauté qui transforme l'énergie en Afrique</p>
            <div style="margin-top: 30px; padding-top: 30px; border-top: 3px solid rgba(220, 20, 60, 0.5);">
                <p style="font-size: 1.2em; margin-bottom: 15px;">
                    📝 <a href="https://forms.gle/nEKpbd2bMvRG8N2w5" target="_blank">Inscris-toi dès maintenant</a>
                </p>
                <p style="font-size: 1.2em; margin-bottom: 15px;">
                    💬 <a href="https://chat.whatsapp.com/Dy1KBqDsUc47yafnjL5hPG" target="_blank">Rejoins-nous sur WhatsApp</a>
                </p>
                <p style="font-size: 1.1em;">📧 youngenergylead@gmail.com</p>
            </div>
        </footer>
    </div>
</body>
</html>
