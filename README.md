<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wasif Bin Nasir - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 50%, #16213e 100%);
            color: #ffffff;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        /* Animated background particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: #64ffda;
            border-radius: 50%;
            opacity: 0.6;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 0.6; }
            50% { transform: translateY(-20px) rotate(180deg); opacity: 1; }
        }

        /* Header section */
        .header {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(100, 255, 218, 0.1) 0%, transparent 70%);
            border-radius: 50%;
            z-index: -1;
        }

        .header h1 {
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, #64ffda 0%, #a8edea 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
            animation: slideInDown 1s ease-out;
        }

        .header h3 {
            font-size: 1.4rem;
            font-weight: 400;
            color: #8892b0;
            margin-bottom: 2rem;
            animation: slideInUp 1s ease-out 0.2s both;
        }

        .wave {
            display: inline-block;
            animation: wave 2s ease-in-out infinite;
            transform-origin: 70% 70%;
            font-size: 2rem;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            10%, 30%, 50%, 70%, 90% { transform: rotate(-10deg) scale(1.1); }
            20%, 40%, 60%, 80% { transform: rotate(10deg) scale(1.1); }
        }

        /* Profile views counter */
        .profile-stats {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(100, 255, 218, 0.2);
            border-radius: 15px;
            padding: 1rem 2rem;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(100, 255, 218, 0.1), transparent);
            transition: left 0.5s;
        }

        .stat-card:hover::before {
            left: 100%;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            border-color: #64ffda;
            box-shadow: 0 10px 30px rgba(100, 255, 218, 0.3);
        }

        /* About section */
        .about {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(100, 255, 218, 0.1);
            border-radius: 20px;
            padding: 2.5rem;
            margin: 3rem 0;
            position: relative;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        .section-title {
            font-size: 2rem;
            font-weight: 700;
            color: #64ffda;
            margin-bottom: 2rem;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 3px;
            background: linear-gradient(90deg, #64ffda, #a8edea);
            animation: expandWidth 1s ease-out 1.2s both;
        }

        @keyframes expandWidth {
            to { width: 100%; }
        }

        .about-list {
            list-style: none;
            padding: 0;
        }

        .about-item {
            margin: 1rem 0;
            padding: 0.5rem 0;
            border-left: 3px solid transparent;
            padding-left: 1rem;
            transition: all 0.3s ease;
            opacity: 0;
            transform: translateX(-20px);
            animation: slideInRight 0.8s ease-out forwards;
        }

        .about-item:nth-child(1) { animation-delay: 0.8s; }
        .about-item:nth-child(2) { animation-delay: 1s; }
        .about-item:nth-child(3) { animation-delay: 1.2s; }
        .about-item:nth-child(4) { animation-delay: 1.4s; }
        .about-item:nth-child(5) { animation-delay: 1.6s; }
        .about-item:nth-child(6) { animation-delay: 1.8s; }
        .about-item:nth-child(7) { animation-delay: 2s; }
        .about-item:nth-child(8) { animation-delay: 2.2s; }

        @keyframes slideInRight {
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .about-item:hover {
            border-left-color: #64ffda;
            background: rgba(100, 255, 218, 0.05);
            transform: translateX(10px);
        }

        .about-item strong {
            color: #64ffda;
        }

        /* Social links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 3rem 0;
            animation: fadeInUp 1s ease-out 0.8s both;
        }

        .social-link {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(100, 255, 218, 0.2);
            border-radius: 50px;
            text-decoration: none;
            color: #ffffff;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .social-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, #64ffda, transparent);
            transition: left 0.5s;
        }

        .social-link:hover::before {
            left: 100%;
        }

        .social-link:hover {
            transform: translateY(-5px) scale(1.05);
            border-color: #64ffda;
            box-shadow: 0 15px 40px rgba(100, 255, 218, 0.4);
            background: rgba(100, 255, 218, 0.1);
        }

        /* Tech stack */
        .tech-stack {
            text-align: center;
            margin: 4rem 0;
            animation: fadeInUp 1s ease-out 1s both;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
            gap: 1.5rem;
            max-width: 800px;
            margin: 2rem auto;
        }

        .tech-item {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(100, 255, 218, 0.1);
            border-radius: 15px;
            padding: 1.5rem;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .tech-item::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: radial-gradient(circle, rgba(100, 255, 218, 0.2) 0%, transparent 70%);
            transition: all 0.4s ease;
            border-radius: 50%;
            transform: translate(-50%, -50%);
        }

        .tech-item:hover::before {
            width: 200px;
            height: 200px;
        }

        .tech-item:hover {
            transform: translateY(-10px) rotateY(10deg);
            border-color: #64ffda;
            box-shadow: 0 20px 50px rgba(100, 255, 218, 0.3);
        }

        .tech-icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            transition: transform 0.4s ease;
        }

        .tech-item:hover .tech-icon {
            transform: scale(1.2) rotateY(-10deg);
        }

        /* GitHub stats */
        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin: 4rem 0;
            animation: fadeInUp 1s ease-out 1.2s both;
        }

        .stat-image {
            border-radius: 15px;
            transition: all 0.4s ease;
            border: 1px solid rgba(100, 255, 218, 0.2);
            overflow: hidden;
        }

        .stat-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.4s ease;
        }

        .stat-image:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(100, 255, 218, 0.3);
            border-color: #64ffda;
        }

        .stat-image:hover img {
            transform: scale(1.05);
        }

        /* Fun badges */
        .badges {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            margin: 3rem 0;
            animation: fadeInUp 1s ease-out 1.4s both;
        }

        .badge {
            background: linear-gradient(135deg, rgba(100, 255, 218, 0.2) 0%, rgba(168, 237, 234, 0.2) 100%);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(100, 255, 218, 0.3);
            border-radius: 25px;
            padding: 0.8rem 1.5rem;
            font-weight: 500;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .badge::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.6s;
        }

        .badge:hover::before {
            left: 100%;
        }

        .badge:hover {
            transform: translateY(-3px) scale(1.05);
            background: linear-gradient(135deg, rgba(100, 255, 218, 0.3) 0%, rgba(168, 237, 234, 0.3) 100%);
            box-shadow: 0 10px 30px rgba(100, 255, 218, 0.4);
        }

        /* Animations */
        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
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

        /* Responsive design */
        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }

            .header h1 {
                font-size: 2.5rem;
            }

            .profile-stats {
                flex-direction: column;
                align-items: center;
            }

            .social-links {
                flex-wrap: wrap;
            }

            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(50px, 1fr));
            }
        }
    </style>
</head>
<body>
    <!-- Animated background particles -->
    <div class="particles" id="particles"></div>

    <div class="container">
        <!-- Header -->
        <header class="header">
            <h1>Hi <span class="wave">👋</span>, I'm Wasif Bin Nasir</h1>
            <h3>🚀 Full Stack Developer | 💡 Lifelong Learner | 🌍 From Pakistan</h3>
            
            <div class="profile-stats">
                <div class="stat-card">
                    <h4>Profile Views</h4>
                    <p>10,847</p>
                </div>
                <div class="stat-card">
                    <h4>GitHub Stars</h4>
                    <p>256</p>
                </div>
                <div class="stat-card">
                    <h4>Projects</h4>
                    <p>42+</p>
                </div>
            </div>
        </header>

        <!-- About Me -->
        <section class="about">
            <h2 class="section-title">🌟 About Me</h2>
            <ul class="about-list">
                <li class="about-item">🔭 Currently building: <strong><a href="https://research-assistant-gui.vercel.app/" target="_blank" style="color: #64ffda; text-decoration: none;">Mini Research Assistant</a></strong></li>
                <li class="about-item">🌱 Learning: <strong>LangChain & LangGraph</strong></li>
                <li class="about-item">🤝 Open to collaboration on: <strong><a href="https://career-craft-client-beta.vercel.app/" target="_blank" style="color: #64ffda; text-decoration: none;">CareerCraft</a></strong></li>
                <li class="about-item">👨‍💻 Portfolio: <strong><a href="https://wasiiff.github.io/Portfolio/" target="_blank" style="color: #64ffda; text-decoration: none;">wasiiff.github.io/Portfolio/</a></strong></li>
                <li class="about-item">💬 Ask me about: <strong>React, Next.js, NestJS, Express</strong></li>
                <li class="about-item">📫 Reach me at: <strong>wasifbinnasir@gmail.com</strong></li>
                <li class="about-item">📄 Experience details: <strong><a href="https://muhammad-wasif-bin-nasir.tiiny.site/" target="_blank" style="color: #64ffda; text-decoration: none;">Resume</a></strong></li>
                <li class="about-item">⚡ Fun fact: <strong>I love tinkering with side-projects, reading tech blogs, and solving coding challenges!</strong></li>
            </ul>
        </section>

        <!-- Social Links -->
        <section class="social-links">
            <a href="https://twitter.com/wasiff__" target="_blank" class="social-link">🐦 Twitter</a>
            <a href="https://linkedin.com/in/wasif-bin-nasir" target="_blank" class="social-link">💼 LinkedIn</a>
            <a href="https://instagram.com/whoiswasiff._" target="_blank" class="social-link">📷 Instagram</a>
            <a href="https://leetcode.com/wasiiff" target="_blank" class="social-link">💻 LeetCode</a>
        </section>

        <!-- Tech Stack -->
        <section class="tech-stack">
            <h2 class="section-title">⚒️ Languages & Tools</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-icon">⚛️</div>
                    <p>React</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🔺</div>
                    <p>Next.js</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🔄</div>
                    <p>Redux</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🎨</div>
                    <p>Tailwind</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">📘</div>
                    <p>TypeScript</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">📜</div>
                    <p>JavaScript</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🌐</div>
                    <p>HTML</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🎯</div>
                    <p>CSS</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">⚙️</div>
                    <p>C++</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">💚</div>
                    <p>Node.js</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🚀</div>
                    <p>Express</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🏰</div>
                    <p>NestJS</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🍃</div>
                    <p>MongoDB</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🐬</div>
                    <p>MySQL</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🔥</div>
                    <p>Firebase</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🌿</div>
                    <p>Git</p>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">📮</div>
                    <p>Postman</p>
                </div>
            </div>
        </section>

        <!-- GitHub Stats -->
        <section class="github-stats">
            <div class="stat-image">
                <img src="https://github-readme-stats.vercel.app/api?username=wasiiff&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="GitHub stats" />
            </div>
            <div class="stat-image">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=wasiiff&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="GitHub streak" />
            </div>
            <div class="stat-image">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=wasiiff&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="Top Languages" />
            </div>
            <div class="stat-image">
                <img src="https://github-readme-activity-graph.vercel.app/graph?username=wasiiff&theme=tokyo-night&hide_border=true&bg_color=0d1117" alt="Activity Graph" />
            </div>
        </section>

        <!-- Fun Badges -->
        <section class="badges">
            <div class="badge">💻 Full Stack Developer</div>
            <div class="badge">☕ Coffee Lover</div>
            <div class="badge">📚 Tech Blogger</div>
            <div class="badge">⚡ Always Learning</div>
            <div class="badge">🚀 Problem Solver</div>
            <div class="badge">🎯 Goal Oriented</div>
        </section>
    </div>

    <script>
        // Create animated particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;

            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                // Random position
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                
                // Random animation delay
                particle.style.animationDelay = Math.random() * 6 + 's';
                
                // Random size variation
                const size = Math.random() * 3 + 1;
                particle.style.width = size + 'px';
                particle.style.height = size + 'px';
                
                particlesContainer.appendChild(particle);
            }
        }

        // Initialize particles when page loads
        window.addEventListener('load', createParticles);

        // Add scroll-triggered animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationDelay = '0s';
                    entry.target.style.animationFillMode = 'both';
                }
            });
        }, observerOptions);

        // Observe all animated elements
        document.addEventListener('DOMContentLoaded', () => {
            const animatedElements = document.querySelectorAll('.about, .tech-stack, .github-stats, .badges');
            animatedElements.forEach(el => observer.observe(el));
        });

        // Add interactive hover effects
        document.querySelectorAll('.tech-item').forEach(item => {
            item.addEventListener('mousemove', (e) => {
                const rect = item.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                item.style.setProperty('--mouse-x', x + 'px');
                item.style.setProperty('--mouse-y', y + 'px');
            });
        });

        // Dynamic typing effect for header
        function typeWriter(element, text, speed = 100) {
            let i = 0;
            element.innerHTML = '';
            
            function type() {
                if (i < text.length) {
                    element.innerHTML += text.charAt(i);
                    i++;
                    setTimeout(type, speed);
                }
            }
            type();
        }

        // Add smooth scrolling for links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            });
        });
    </script>
</body>
</html>
