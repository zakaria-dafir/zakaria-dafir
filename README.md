<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zakaria Dafir - Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #0d1117;
            color: #c9d1d9;
            line-height: 1.6;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        
        header {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 30px 20px;
            background: linear-gradient(135deg, #161b22 0%, #0d1117 100%);
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            margin-bottom: 20px;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid #58a6ff;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #58a6ff, #2ea043);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 50px;
            color: white;
        }
        
        h1 {
            font-size: 2.5rem;
            color: #58a6ff;
            margin-bottom: 10px;
        }
        
        h2 {
            font-size: 1.8rem;
            color: #c9d1d9;
            margin-bottom: 20px;
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
            margin-top: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            background-color: #161b22;
            padding: 10px 20px;
            border-radius: 30px;
            transition: transform 0.3s ease;
        }
        
        .contact-item:hover {
            transform: translateY(-5px);
            background-color: #1f6feb;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-block;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: #21262d;
            color: #c9d1d9;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            font-size: 20px;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: #58a6ff;
            color: white;
            transform: translateY(-5px);
        }
        
        section {
            background-color: #161b22;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
        }
        
        .section-title {
            color: #58a6ff;
            font-size: 1.8rem;
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 2px solid #30363d;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .card {
            background-color: #21262d;
            padding: 20px;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .card h3 {
            color: #58a6ff;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .card p {
            color: #8b949e;
            margin-bottom: 10px;
        }
        
        .date {
            color: #3fb950;
            font-weight: 500;
            margin-bottom: 10px;
            display: block;
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
        }
        
        .skill {
            background-color: #1f6feb;
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .languages {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .language {
            background-color: #3fb950;
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .project-card {
            background-color: #21262d;
            padding: 20px;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .project-card h3 {
            color: #58a6ff;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 15px 0;
        }
        
        .tech {
            background-color: #1f6feb;
            color: white;
            padding: 5px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
        }
        
        footer {
            text-align: center;
            padding: 30px;
            margin-top: 30px;
            color: #8b949e;
            border-top: 1px solid #30363d;
        }
        
        @media (max-width: 768px) {
            .contact-info {
                flex-direction: column;
                align-items: center;
            }
            
            .grid {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-img">ZD</div>
            <h1>Zakaria Dafir</h1>
            <h2>Full Stack Web Developer</h2>
            
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>zakariadafir209@gmail.com</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span>07 03 22 41 20</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>Khouribga, Maroc</span>
                </div>
            </div>
            
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fas fa-globe"></i></a>
            </div>
        </header>
        
        <section>
            <h2 class="section-title"><i class="fas fa-user-graduate"></i> Education</h2>
            <div class="grid">
                <div class="card">
                    <span class="date">2021 - 2024</span>
                    <h3>ISTA Tiznit</h3>
                    <p>DTS Développement Digital (Web Full Stack)</p>
                    <p>Courses: HTML/CSS, JavaScript, React, Laravel, MySQL</p>
                </div>
                <div class="card">
                    <span class="date">2020</span>
                    <h3>Université Ibn Zohr, Ait Melloul</h3>
                    <p>DEUG Biologie</p>
                </div>
                <div class="card">
                    <span class="date">2018</span>
                    <h3>Lycée Ibn Zohr</h3>
                    <p>Baccalauréat Sciences Physiques</p>
                </div>
            </div>
        </section>
        
        <section>
            <h2 class="section-title"><i class="fas fa-briefcase"></i> Experience</h2>
            <div class="grid">
                <div class="card">
                    <span class="date">Juin - Août 2025</span>
                    <h3>Participant - Piscine 1337 Coding School</h3>
                    <p>Intensive learning of C language and Unix tools</p>
                    <p>Algorithmic project resolution (Libft, Get Next Line, Printf)</p>
                    <p>Development of teamwork and autonomy skills</p>
                </div>
                <div class="card">
                    <span class="date">Juin - Mai 2025</span>
                    <h3>Stagiaire en Bureautique - Commune de Belfaa</h3>
                    <p>Writing and formatting administrative documents</p>
                    <p>Filing and organization of paper and digital files</p>
                    <p>Use of office tools (Word, Excel, PowerPoint)</p>
                </div>
            </div>
        </section>
        
        <section>
            <h2 class="section-title"><i class="fas fa-code"></i> Projects</h2>
            <div class="project-grid">
                <div class="project-card">
                    <h3>E-commerce Application</h3>
                    <p>Full-stack JavaScript e-commerce site with product management, cart, and simulated payment system</p>
                    <div class="project-tech">
                        <span class="tech">JavaScript</span>
                        <span class="tech">HTML/CSS</span>
                        <span class="tech">API</span>
                    </div>
                </div>
                <div class="project-card">
                    <h3>Car Rental Platform</h3>
                    <p>Car reservation platform with admin dashboard using Laravel and React</p>
                    <div class="project-tech">
                        <span class="tech">Laravel</span>
                        <span class="tech">React</span>
                        <span class="tech">MySQL</span>
                    </div>
                </div>
                <div class="project-card">
                    <h3>Hotel Management System</h3>
                    <p>Software to manage reservations, rooms and clients with Python</p>
                    <div class="project-tech">
                        <span class="tech">Python</span>
                        <span class="tech">SQLite</span>
                        <span class="tech">Tkinter</span>
                    </div>
                </div>
            </div>
        </section>
        
        <section>
            <h2 class="section-title"><i class="fas fa-tools"></i> Skills</h2>
            <div class="grid">
                <div class="card">
                    <h3>Languages</h3>
                    <div class="skills">
                        <span class="skill">HTML</span>
                        <span class="skill">CSS</span>
                        <span class="skill">JavaScript</span>
                        <span class="skill">PHP</span>
                        <span class="skill">SQL</span>
                        <span class="skill">Python</span>
                        <span class="skill">C</span>
                    </div>
                </div>
                <div class="card">
                    <h3>Frameworks & Technologies</h3>
                    <div class="skills">
                        <span class="skill">Laravel</span>
                        <span class="skill">React</span>
                        <span class="skill">Bootstrap</span>
                        <span class="skill">Node.js</span>
                        <span class="skill">Git</span>
                        <span class="skill">MySQL</span>
                    </div>
                </div>
                <div class="card">
                    <h3>Tools & Environments</h3>
                    <div class="skills">
                        <span class="skill">VS Code</span>
                        <span class="skill">GitHub</span>
                        <span class="skill">Linux</span>
                        <span class="skill">Docker</span>
                        <span class="skill">Figma</span>
                    </div>
                </div>
                <div class="card">
                    <h3>Languages</h3>
                    <div class="languages">
                        <span class="language">Arabic (Native)</span>
                        <span class="language">English (Fluent)</span>
                        <span class="language">French (B2)</span>
                    </div>
                </div>
            </div>
        </section>
        
        <section>
            <h2 class="section-title"><i class="fas fa-star"></i> Personal Skills</h2>
            <div class="grid">
                <div class="card">
                    <p>Problem Solving, Attention to Detail, Adaptability, Communication</p>
                </div>
                <div class="card">
                    <p>Time Management, Teamwork, Continuous Learning, Autonomy</p>
                </div>
            </div>
        </section>
        
        <footer>
            <p>© 2023 Zakaria Dafir. All rights reserved.</p>
            <p>Designed with ❤️ for GitHub</p>
        </footer>
    </div>

    <script>
        // Simple animation for page elements
        document.addEventListener('DOMContentLoaded', function() {
            const elements = document.querySelectorAll('.card, .contact-item, .project-card');
            
            elements.forEach((element, index) => {
                setTimeout(() => {
                    element.style.opacity = 1;
                    element.style.transform = 'translateY(0)';
                }, 100 + (index * 100));
            });
        });
    </script>
</body>
</html>
