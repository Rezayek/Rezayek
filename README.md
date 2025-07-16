<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abderrazek Ben Cheikh Souguir - Terminal README</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Fira Code', monospace;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
            color: #00ff00;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .terminal-window {
            background: #000000;
            border: 2px solid #00ff00;
            border-radius: 10px;
            margin: 20px 0;
            box-shadow: 0 0 20px rgba(0, 255, 0, 0.3);
            animation: borderGlow 2s ease-in-out infinite alternate;
        }

        @keyframes borderGlow {
            0% { box-shadow: 0 0 20px rgba(0, 255, 0, 0.3); }
            100% { box-shadow: 0 0 40px rgba(0, 255, 0, 0.6); }
        }

        .terminal-header {
            background: #00ff00;
            color: #000000;
            padding: 10px;
            border-radius: 8px 8px 0 0;
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 600;
        }

        .terminal-dots {
            display: flex;
            gap: 5px;
        }

        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #000000;
            animation: pulse 1.5s ease-in-out infinite;
        }

        .dot:nth-child(2) { animation-delay: 0.3s; }
        .dot:nth-child(3) { animation-delay: 0.6s; }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }

        .terminal-content {
            padding: 20px;
        }

        .header-section {
            text-align: center;
            margin-bottom: 30px;
        }

        .name {
            font-size: 2.5em;
            font-weight: 700;
            margin-bottom: 20px;
            animation: typeWriter 3s ease-in-out;
            text-shadow: 0 0 10px rgba(0, 255, 0, 0.8);
        }

        @keyframes typeWriter {
            0% { width: 0; }
            100% { width: 100%; }
        }

        .typing-animation {
            font-size: 1.2em;
            margin: 20px 0;
            border-right: 2px solid #00ff00;
            animation: blink 1s step-start infinite;
        }

        @keyframes blink {
            0%, 50% { border-color: #00ff00; }
            51%, 100% { border-color: transparent; }
        }

        .section {
            margin: 30px 0;
            padding: 20px;
            background: rgba(0, 255, 0, 0.05);
            border-left: 4px solid #00ff00;
            border-radius: 5px;
            animation: slideIn 0.6s ease-out;
        }

        @keyframes slideIn {
            0% { transform: translateX(-100%); opacity: 0; }
            100% { transform: translateX(0); opacity: 1; }
        }

        .section-title {
            font-size: 1.8em;
            font-weight: 600;
            margin-bottom: 15px;
            color: #00ff00;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title::before {
            content: '>';
            color: #00ff00;
            animation: blink 1s step-start infinite;
        }

        .skill-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .skill-category {
            background: rgba(0, 0, 0, 0.8);
            border: 1px solid #00ff00;
            border-radius: 8px;
            padding: 15px;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .skill-category:hover {
            background: rgba(0, 255, 0, 0.1);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 255, 0, 0.2);
        }

        .skill-category h3 {
            color: #00ff00;
            margin-bottom: 10px;
            font-size: 1.1em;
        }

        .skill-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .badge {
            background: #000000;
            color: #00ff00;
            padding: 4px 8px;
            border: 1px solid #00ff00;
            border-radius: 4px;
            font-size: 0.8em;
            transition: all 0.3s ease;
            animation: fadeIn 0.5s ease-out;
        }

        .badge:hover {
            background: #00ff00;
            color: #000000;
            transform: scale(1.05);
        }

        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .stat-card {
            background: rgba(0, 0, 0, 0.8);
            border: 1px solid #00ff00;
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
            animation: float 3s ease-in-out infinite;
        }

        .stat-card:nth-child(2) { animation-delay: 1s; }
        .stat-card:nth-child(3) { animation-delay: 2s; }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .stat-card:hover {
            background: rgba(0, 255, 0, 0.1);
            transform: translateY(-5px);
        }

        .command-line {
            background: #000000;
            color: #00ff00;
            padding: 10px;
            border-radius: 5px;
            margin: 10px 0;
            font-family: 'Fira Code', monospace;
            border: 1px solid #00ff00;
            position: relative;
            overflow: hidden;
        }

        .command-line::before {
            content: '$ ';
            color: #00ff00;
            font-weight: bold;
        }

        .matrix-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
        }

        .matrix-char {
            position: absolute;
            color: #00ff00;
            font-family: 'Fira Code', monospace;
            font-size: 14px;
            animation: matrixFall 10s linear infinite;
        }

        @keyframes matrixFall {
            0% { transform: translateY(-100vh); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0; }
        }

        .contact-section {
            text-align: center;
            margin: 40px 0;
        }

        .contact-link {
            display: inline-block;
            background: #000000;
            color: #00ff00;
            padding: 12px 24px;
            border: 2px solid #00ff00;
            border-radius: 8px;
            text-decoration: none;
            margin: 10px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .contact-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 0, 0.2), transparent);
            transition: left 0.5s ease;
        }

        .contact-link:hover {
            background: #00ff00;
            color: #000000;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 255, 0, 0.3);
        }

        .contact-link:hover::before {
            left: 100%;
        }

        .project-card {
            background: rgba(0, 0, 0, 0.8);
            border: 1px solid #00ff00;
            border-radius: 8px;
            padding: 20px;
            margin: 15px 0;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, #00ff00, transparent);
            animation: loadingBar 3s ease-in-out infinite;
        }

        @keyframes loadingBar {
            0% { width: 0%; }
            50% { width: 100%; }
            100% { width: 0%; }
        }

        .project-card:hover {
            background: rgba(0, 255, 0, 0.1);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 255, 0, 0.2);
        }

        .about-list {
            list-style: none;
            padding: 0;
        }

        .about-list li {
            margin: 10px 0;
            padding-left: 20px;
            position: relative;
        }

        .about-list li::before {
            content: '►';
            position: absolute;
            left: 0;
            color: #00ff00;
            animation: pulse 2s ease-in-out infinite;
        }

        .glitch {
            animation: glitch 0.3s ease-in-out infinite;
        }

        @keyframes glitch {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-2px); }
            50% { transform: translateX(2px); }
            75% { transform: translateX(-1px); }
        }
    </style>
</head>
<body>
    <div class="matrix-bg" id="matrix"></div>
    
    <div class="container">
        <div class="terminal-window">
            <div class="terminal-header">
                <div class="terminal-dots">
                    <div class="dot"></div>
                    <div class="dot"></div>
                    <div class="dot"></div>
                </div>
                <span>abderrazek@github:~/profile$</span>
            </div>
            
            <div class="terminal-content">
                <div class="header-section">
                    <div class="name">👋 Hi, I'm Abderrazek Ben Cheikh Souguir</div>
                    <div class="typing-animation" id="typing"></div>
                    <div class="command-line">whoami | grep -E "(Software Engineer|Game Developer|Flutter Developer|AI Enthusiast)"</div>
                </div>

                <div class="section">
                    <h2 class="section-title">👨‍💻 About Me</h2>
                    <ul class="about-list">
                        <li>💼 Currently working as a <strong>Software Engineer</strong> at <strong>Kosmos Technologies</strong></li>
                        <li>🧠 Currently expanding my knowledge in <strong>Agents</strong> and <strong>MCPs implementations</strong></li>
                        <li>💻 Passionate about <strong>Game Development</strong></li>
                        <li>📱 Ask me about <strong>Flutter</strong>, <strong>Unity Game Development</strong>, <strong>AI Agents</strong></li>
                    </ul>
                </div>

                <div class="section">
                    <h2 class="section-title">🏆 GitHub Stats</h2>
                    <div class="stats-grid">
                        <div class="stat-card">
                            <h3>Profile Views</h3>
                            <div class="command-line">curl -s https://api.github.com/users/rezayek | jq '.public_repos'</div>
                        </div>
                        <div class="stat-card">
                            <h3>Contributions</h3>
                            <div class="command-line">git log --oneline | wc -l</div>
                        </div>
                        <div class="stat-card">
                            <h3>Streak</h3>
                            <div class="command-line">git log --since="1 month ago" --oneline | wc -l</div>
                        </div>
                    </div>
                </div>

                <div class="section">
                    <h2 class="section-title">🔭 Featured Project</h2>
                    <div class="project-card">
                        <h3>Enigma's Echo</h3>
                        <p>A mystery adventure game built with Unity that challenges players with puzzles and immersive storytelling.</p>
                        <div class="command-line">cd ~/projects/enigmas-echo && unity -batchmode -executeMethod BuildScript.BuildGame</div>
                    </div>
                </div>

                <div class="section">
                    <h2 class="section-title">🛠️ Technical Skills</h2>
                    <div class="skill-grid">
                        <div class="skill-category">
                            <h3>Programming Languages</h3>
                            <div class="skill-badges">
                                <span class="badge">C</span>
                                <span class="badge">C++</span>
                                <span class="badge">C#</span>
                                <span class="badge">Dart</span>
                                <span class="badge">JavaScript</span>
                                <span class="badge">Python</span>
                                <span class="badge">Java</span>
                            </div>
                        </div>
                        
                        <div class="skill-category">
                            <h3>Frameworks & Technologies</h3>
                            <div class="skill-badges">
                                <span class="badge">Flutter</span>
                                <span class="badge">Unity</span>
                                <span class="badge">FastAPI</span>
                                <span class="badge">TensorFlow</span>
                                <span class="badge">Firebase</span>
                                <span class="badge">Supabase</span>
                                <span class="badge">Docker</span>
                            </div>
                        </div>
                        
                        <div class="skill-category">
                            <h3>AI & Automation</h3>
                            <div class="skill-badges">
                                <span class="badge">crewAI</span>
                                <span class="badge">AI Agents</span>
                                <span class="badge">Prompt Engineering</span>
                                <span class="badge">n8n</span>
                                <span class="badge">Make.com</span>
                                <span class="badge">TensorFlow</span>
                            </div>
                        </div>
                        
                        <div class="skill-category">
                            <h3>Databases</h3>
                            <div class="skill-badges">
                                <span class="badge">PostgreSQL</span>
                                <span class="badge">MySQL</span>
                                <span class="badge">SQLite</span>
                            </div>
                        </div>
                        
                        <div class="skill-category">
                            <h3>Tools & Other</h3>
                            <div class="skill-badges">
                                <span class="badge">Git</span>
                                <span class="badge">Figma</span>
                                <span class="badge">Blender</span>
                                <span class="badge">Postman</span>
                                <span class="badge">Linux</span>
                                <span class="badge">RabbitMQ</span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="section">
                    <h2 class="section-title">📫 Connect With Me</h2>
                    <div class="contact-section">
                        <a href="https://www.linkedin.com/in/abderrazek-ben-cheikh-souguir-803743233/" class="contact-link" target="_blank">
                            LinkedIn Profile
                        </a>
                        <div class="command-line">ssh abderrazek@linkedin.com</div>
                    </div>
                </div>

                <div class="section">
                    <div class="command-line">echo "Built with ❤️ and lots of ☕" | figlet</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Matrix rain effect
        function createMatrix() {
            const matrix = document.getElementById('matrix');
            const chars = '01アイウエオカキクケコサシスセソタチツテトナニヌネノハヒフヘホマミムメモヤユヨラリルレロワヲン';
            
            for (let i = 0; i < 50; i++) {
                const char = document.createElement('div');
                char.className = 'matrix-char';
                char.textContent = chars[Math.floor(Math.random() * chars.length)];
                char.style.left = Math.random() * 100 + '%';
                char.style.animationDelay = Math.random() * 10 + 's';
                char.style.animationDuration = (Math.random() * 5 + 5) + 's';
                matrix.appendChild(char);
            }
        }

        // Typing animation
        function typeWriter() {
            const texts = [
                'Software Engineer',
                'Game Developer', 
                'Flutter Developer',
                'AI Enthusiast'
            ];
            let textIndex = 0;
            let charIndex = 0;
            const typingElement = document.getElementById('typing');
            
            function type() {
                if (charIndex < texts[textIndex].length) {
                    typingElement.textContent += texts[textIndex].charAt(charIndex);
                    charIndex++;
                    setTimeout(type, 100);
                } else {
                    setTimeout(() => {
                        typingElement.textContent = '';
                        charIndex = 0;
                        textIndex = (textIndex + 1) % texts.length;
                        setTimeout(type, 500);
                    }, 2000);
                }
            }
            
            type();
        }

        // Glitch effect on hover
        function addGlitchEffect() {
            const badges = document.querySelectorAll('.badge');
            badges.forEach(badge => {
                badge.addEventListener('mouseenter', () => {
                    badge.classList.add('glitch');
                    setTimeout(() => {
                        badge.classList.remove('glitch');
                    }, 300);
                });
            });
        }

        // Random command line updates
        function updateCommandLines() {
            const commands = [
                'npm install success',
                'git push origin main',
                'docker build -t app .',
                'python train_model.py',
                'flutter build apk',
                'unity -batchmode -quit'
            ];
            
            const commandLines = document.querySelectorAll('.command-line');
            
            setInterval(() => {
                const randomCmd = commandLines[Math.floor(Math.random() * commandLines.length)];
                const randomCommand = commands[Math.floor(Math.random() * commands.length)];
                
                const originalText = randomCmd.textContent;
                randomCmd.textContent = '$ ' + randomCommand;
                
                setTimeout(() => {
                    randomCmd.textContent = originalText;
                }, 2000);
            }, 10000);
        }

        // Initialize animations
        document.addEventListener('DOMContentLoaded', () => {
            createMatrix();
            typeWriter();
            addGlitchEffect();
            updateCommandLines();
        });
    </script>
</body>
</html>
