<!DOCTYPE html>
<html lang="sw">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mim Khairoun - Ushauri Nasaha</title>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Nature & Earth Color Theme - Professional & Calming */
        :root {
            --primary: #065F46;
            --secondary: #10B981;
            --accent1: #F59E0B;
            --accent2: #34D399;
            --dark: #1F2937;
            --light: #FEFCE8;
            --cream: #F3FDEA;
            --white: #FFFFFF;
            --gradient: linear-gradient(135deg, #065F46, #10B981, #34D399);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--cream);
            overflow-x: hidden;
        }

        /* Animated Gradient Background - Subtle */
        .nature-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--gradient);
            background-size: 400% 400%;
            animation: naturePulse 20s ease infinite;
            z-index: -1;
            opacity: 0.03;
        }

        @keyframes naturePulse {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Header */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            color: var(--primary);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(0,0,0,0.08);
            border-bottom: 2px solid var(--accent2);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--primary);
            text-decoration: none;
            transition: all 0.3s;
            font-weight: 600;
            padding: 0.5rem 1rem;
            border-radius: 25px;
        }

        .nav-links a:hover {
            background: var(--secondary);
            color: white;
        }

        /* Hero Section */
        .hero {
            padding: 6rem 0;
            text-align: center;
            position: relative;
            background: var(--light);
            border-radius: 0 0 30px 30px;
            margin-bottom: 2rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
            color: var(--primary);
            font-weight: 700;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            color: var(--dark);
            animation: fadeInUp 1s ease 0.2s both;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 3rem;
            background: var(--gradient);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
            animation: fadeInUp 1s ease 0.4s both;
            box-shadow: 0 4px 15px rgba(6, 95, 70, 0.3);
            border: none;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(6, 95, 70, 0.4);
        }

        /* Emoji Animation */
        .emoji-float {
            display: inline-block;
            animation: emojiBounce 2s ease infinite;
            font-size: 2rem;
            margin: 0 0.5rem;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes emojiBounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        /* Services Section */
        .services {
            padding: 4rem 0;
            background: var(--white);
            margin: 2rem 0;
            border-radius: 25px;
            box-shadow: 0 5px 25px rgba(0,0,0,0.08);
            border: 1px solid rgba(16, 185, 129, 0.1);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--primary);
            font-weight: 700;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 18px;
            text-align: center;
            transition: all 0.4s;
            border: 2px solid transparent;
            position: relative;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--gradient);
            transform: scaleX(0);
            transition: transform 0.3s;
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 30px rgba(6, 95, 70, 0.15);
            border-color: var(--accent2);
        }

        .service-card h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            font-size: 1.4rem;
            font-weight: 600;
        }

        .service-card p {
            color: #4B5563;
            line-height: 1.7;
        }

        /* Gallery */
        .gallery {
            padding: 4rem 0;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 18px;
            height: 250px;
            background: #E5E7EB;
            cursor: pointer;
            transition: all 0.4s;
            box-shadow: 0 3px 12px rgba(0,0,0,0.08);
        }

        .gallery-item:hover {
            transform: scale(1.03);
            box-shadow: 0 8px 25px rgba(6, 95, 70, 0.2);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.4s;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(6, 95, 70, 0.9), transparent);
            color: white;
            padding: 1.5rem 1rem 1rem;
            transform: translateY(100%);
            transition: transform 0.4s;
        }

        .gallery-item:hover .gallery-overlay {
            transform: translateY(0);
        }

        /* Contact Section */
        .contact {
            padding: 4rem 0;
            background: var(--light);
            border-radius: 25px;
            margin-bottom: 2rem;
            box-shadow: 0 5px 25px rgba(0,0,0,0.08);
            border: 1px solid rgba(16, 185, 129, 0.1);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 70px;
            height: 70px;
            background: var(--gradient);
            color: white;
            border-radius: 50%;
            font-size: 1.8rem;
            text-decoration: none;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(6, 95, 70, 0.25);
        }

        .social-link:hover {
            transform: translateY(-5px) rotate(8deg);
            box-shadow: 0 10px 30px rgba(6, 95, 70, 0.4);
        }

        .social-link::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: rgba(255,255,255,0.2);
            transform: rotate(30deg);
            transition: all 0.6s;
        }

        .social-link:hover::after {
            transform: rotate(30deg) translate(20%, 20%);
        }

        .social-link i {
            z-index: 1;
        }

        .social-link span {
            position: absolute;
            bottom: -20px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 0.75rem;
            white-space: nowrap;
            opacity: 0;
            transition: all 0.3s;
            background: var(--primary);
            color: white;
            padding: 0.2rem 0.5rem;
            border-radius: 10px;
        }

        .social-link:hover span {
            bottom: -35px;
            opacity: 1;
        }

        /* Floating WhatsApp Button */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 70px;
            height: 70px;
            background: #25D366;
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: all 0.3s;
            z-index: 999;
            text-decoration: none;
            border: 4px solid white;
        }

        .whatsapp-float:hover {
            transform: scale(1.1) rotate(10deg);
        }

        /* Footer */
        footer {
            background: var(--primary);
            color: var(--cream);
            text-align: center;
            padding: 2.5rem 0;
            margin-top: 3rem;
            border-top: 5px solid var(--accent2);
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1.5rem;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .social-links {
                gap: 1.5rem;
            }
            
            .social-link {
                width: 65px;
                height: 65px;
                font-size: 1.6rem;
            }
            
            .footer-content {
                flex-direction: column;
                text-align: center;
            }
        }

        /* Loading Animation */
        .loader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--cream);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 9999;
            transition: opacity 0.5s;
        }

        .loader-content {
            text-align: center;
        }

        .loader-spinner {
            width: 60px;
            height: 60px;
            border: 4px solid rgba(6, 95, 70, 0.2);
            border-top-color: var(--primary);
            border-radius: 50%;
            animation: spin 1.2s linear infinite;
            margin: 0 auto 1rem;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <!-- Loading Screen -->
    <div class="loader" id="loader">
        <div class="loader-content">
            <div class="loader-spinner"></div>
            <p style="color: var(--primary); font-size: 1.2rem;">Inapakia...</p>
        </div>
    </div>

    <!-- Animated Background -->
    <div class="nature-bg"></div>

    <!-- Header -->
    <header>
        <nav class="container">
            <div class="logo">
                Mim Khairoun 🌿
            </div>
            <ul class="nav-links">
                <li><a href="#home">Nyumbani</a></li>
                <li><a href="#services">Huduma</a></li>
                <li><a href="#gallery">Picha</a></li>
                <li><a href="#contact">Mawasiliano</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <h1>Karibu kwenye Ushauri Nasaha <span class="emoji-float">🌱</span></h1>
            <p>Neno lako ni siri yangu. Nikuunge mkono kutoka gizani hadi kwenye mwanga wa kutulivu.</p>
            <p style="font-size: 1.4rem; margin-top: 1rem; color: var(--primary);">
                <span class="emoji-float">🤝</span>
                <span class="emoji-float">💚</span>
                <span class="emoji-float">🌿</span>
                <span class="emoji-float">✨</span>
            </p>
            <a href="#contact" class="cta-button">Nipigie Leo</a>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services container">
        <h2 class="section-title">Jinsi Ninavyosaidia <span class="emoji-float">🌿</span></h2>
        <div class="services-grid">
            <div class="service-card">
                <h3>Ushauri wa Binafsi <span class="emoji-float">🌱</span></h3>
                <p>Mazungumzo ya siri na ya kutuliza moyo. Kuja kama uliivyo, nita kupokea bila hukumu.</p>
            </div>
            <div class="service-card">
                <h3>Ushauri wa Mapenzi <span class="emoji-float">💚</span></h3>
                <p>Tunajenga mahusiano yenye afya, kuelewa hisia, na kuimarisha urafiki wa kudumu.</p>
            </div>
            <div class="service-card">
                <h3>Ushauri wa Familia <span class="emoji-float">🌳</span></h3>
                <p>Kuimarisha uhusiano wa kifamilia, kuepuka migogoro, na kueneza upendo.</p>
            </div>
            <div class="service-card">
                <h3>Motivation & Coaching <span class="emoji-float">🌻</span></h3>
                <p>Kukumbusha nguvu yako ya ndani, kutimiza malengo, na kuishi maisha yenye balansi.</p>
            </div>
            <div class="service-card">
                <h3>Ushauri wa Kijamii <span class="emoji-float">🌍</span></h3>
                <p>Kujifunza kila siku, kujenga urafiki, na kuwa na mchango chanya kwa jamii.</p>
            </div>
            <div class="service-card">
                <h3>Msaada wa Haraka <span class="emoji-float">🆘</span></h3>
                <p>Nipo hapa kwa ajili yako, siku nzima. Usijione wewe pekee kipindi cha shida.</p>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="gallery container">
        <h2 class="section-title">Picha za Tahadhari <span class="emoji-float">📸</span></h2>
        <div class="gallery-grid">
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1544027993-37dbfe43562a?w=400" alt="Ushauri">
                <div class="gallery-overlay">
                    <h4>Masaa ya Utulivu</h4>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1573497019940-1c28c88b4f3e?w=400" alt="Ngoa">
                <div class="gallery-overlay">
                    <h4>Ngoa ya Moyo</h4>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1529156069898-49953e39b3ac?w=400" alt="Kufurahi">
                <div class="gallery-overlay">
                    <h4>Kuona Mwangaza</h4>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400" alt="Amani">
                <div class="gallery-overlay">
                    <h4>Amani ya Moyo</h4>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact container">
        <h2 class="section-title">Nijulishe <span class="emoji-float">📞</span></h2>
        <p style="text-align: center; font-size: 1.3rem; margin-bottom: 2rem; color: var(--primary);">
            Nipo hapa kwa ajili yako! <span class="emoji-float">🤗</span> <br>
            Kama una swali lolote, usisite kunipigia.
        </p>
        
        <div class="social-links">
            <a href="https://instagram.com/itx_o_o.09" target="_blank" class="social-link" title="Instagram">
                <i class="fab fa-instagram"></i>
                <span>Instagram</span>
            </a>
            <a href="https://tiktok.com/@Reykhai09" target="_blank" class="social-link" title="TikTok">
                <i class="fab fa-tiktok"></i>
                <span>TikTok</span>
            </a>
            <a href="https://wa.me/212656923137" target="_blank" class="social-link" title="WhatsApp">
                <i class="fab fa-whatsapp"></i>
                <span>WhatsApp</span>
            </a>
            <a href="tel:+212656923137" class="social-link" title="Call">
                <i class="fas fa-phone"></i>
                <span>Call</span>
            </a>
        </div>

        <div style="text-align: center; margin-top: 2rem; background: white; padding: 2rem; border-radius: 20px; max-width: 600px; margin-left: auto; margin-right: auto; box-shadow: 0 5px 20px rgba(0,0,0,0.08);">
            <p style="font-size: 1.2rem; margin: 0.8rem 0; display: flex; align-items: center; justify-content: center; gap: 0.5rem;">
                <i class="fab fa-whatsapp" style="color: #25D366;"></i>
                <strong style="color: var(--primary);">WhatsApp:</strong> 0656923137 
                <span class="emoji-float" style="font-size: 1.5rem;">💚</span>
            </p>
            <p style="font-size: 1.2rem; margin: 0.8rem 0; display: flex; align-items: center; justify-content: center; gap: 0.5rem;">
                <i class="fab fa-instagram" style="color: var(--primary);"></i>
                <strong style="color: var(--primary);">Instagram:</strong> @itx_o_o.09
            </p>
            <p style="font-size: 1.2rem; margin: 0.8rem 0; display: flex; align-items: center; justify-content: center; gap: 0.5rem;">
                <i class="fab fa-tiktok" style="color: var(--dark);"></i>
                <strong style="color: var(--primary);">TikTok:</strong> @Reykhai09
            </p>
        </div>
    </section>

    <!-- Floating WhatsApp Button -->
    <a href="https://wa.me/212656923137" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <p>&copy; 2024 Mim Khairoun. Haki zote zimehifadhiwa.</p>
                <p style="display: flex; align-items: center; gap: 0.5rem;">
                    <span class="emoji-float">🌱</span>
                    Tumaini | Nguvu | Uzima
                    <span class="emoji-float">💚</span>
                </p>
            </div>
        </div>
    </footer>

    <script>
        // Remove loader after page loads
        window.addEventListener('load', function() {
            setTimeout(function() {
                document.getElementById('loader').style.opacity = '0';
                setTimeout(function() {
                    document.getElementById('loader').style.display = 'none';
                }, 500);
            }, 1000);
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all cards and sections
        document.querySelectorAll('.service-card, .gallery-item, .contact').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });

        // Add hover effect to service cards
        document.querySelectorAll('.service-card').forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-8px) scale(1.02)';
            });
            
            card.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });

        // Dynamic emoji effect
        function addEmojiEffect() {
            const emojis = document.querySelectorAll('.emoji-float');
            emojis.forEach((emoji, index) => {
                setTimeout(() => {
                    emoji.style.animation = 'none';
                    setTimeout(() => {
                        emoji.style.animation = 'emojiBounce 2s ease infinite';
                    }, 10);
                }, index * 200);
            });
        }

        // Trigger emoji effect every 5 seconds
        setInterval(addEmojiEffect, 5000);

        // Add click counter for CTA button
        document.querySelector('.cta-button').addEventListener('click', function() {
            this.style.transform = 'scale(0.95)';
            setTimeout(() => {
                this.style.transform = 'translateY(-3px)';
            }, 100);
        });

        // Add parallax effect to nature background
        window.addEventListener('scroll', function() {
            const scrolled = window.pageYOffset;
            const natureBg = document.querySelector('.nature-bg');
            natureBg.style.transform = `translateY(${scrolled * 0.3}px)`;
        });

        // Welcome message
        setTimeout(() => {
            const welcomeMsg = document.createElement('div');
            welcomeMsg.innerHTML = `
                <div style="position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%); 
                     background: white; padding: 2.5rem; border-radius: 20px; box-shadow: 0 15px 50px rgba(0,0,0,0.2); 
                     z-index: 2000; text-align: center; max-width: 90%; border: 3px solid var(--accent2);">
                    <h3 style="color: var(--primary); margin-bottom: 1rem;">Karibu sana! 🌿</h3>
                    <p style="color: var(--dark); font-size: 1.1rem;">Nimefurahi sana ukuje kwenye tovuti yangu!</p>
                    <p style="color: var(--dark); font-size: 1.1rem;">Tafadhali usisite kunipigia kama unahitaji ushauri wowote.</p>
                    <button onclick="this.parentElement.remove()" style="margin-top: 1.5rem; padding: 0.7rem 2.5rem; 
                            background: var(--primary); color: white; border: none; border-radius: 25px; cursor: pointer;
                            font-weight: bold; transition: all 0.3s;">
                        Asante! ✨
                    </button>
                </div>
            `;
            document.body.appendChild(welcomeMsg);
            
            setTimeout(() => {
                if (welcomeMsg.parentElement) {
                    welcomeMsg.style.opacity = '0';
                    setTimeout(() => welcomeMsg.remove(), 300);
                }
            }, 5000);
        }, 2000);
    </script>
</body>
</html>
