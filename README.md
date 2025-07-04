<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ABCD SAMPLE WEB - Home</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
 body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            min-height: 100vh;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
 /* Header */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
        }
 nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }
.logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #2c3e50;
        }
 .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
.nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
            cursor: pointer;
        }
.nav-links a:hover,
        .nav-links a.active {
            color: #3498db;
        }
/* Main Content */
        main {
            margin-top: 80px;
            padding: 2rem 0;
        }
.page {
            display: none;
            background: white;
            margin: 20px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            padding: 3rem;
            min-height: 80vh;
        }
.page.active {
            display: block;
        }
.page h1 {
            color: #2c3e50;
            margin-bottom: 2rem;
            font-size: 2.5rem;
            text-align: center;
        }
.page h2 {
            color: #3498db;
            margin-bottom: 1.5rem;
            font-size: 2rem;
        }
.page p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            text-align: justify;
        }
/* Home Page Specific */
        .hero {
            text-align: center;
            padding: 2rem 0;
        }
.hero h1 {
            font-size: 3rem;
            color: #2c3e50;
            margin-bottom: 1rem;
        }
.hero p {
            font-size: 1.3rem;
            color: #555;
            text-align: center;
        }
.welcome-card {
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            padding: 2rem;
            border-radius: 15px;
            margin: 2rem 0;
            text-align: center;
        }
.features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
.feature-card {
            background: #f8f9fa;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s ease;
        }
.feature-card:hover {
            transform: translateY(-5px);
        }
.feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
      /* About Page Specific */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 3rem;
            align-items: center;
            margin-top: 2rem;
        }
      .profile-section {
            text-align: center;
        }
      .profile-image {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background: linear-gradient(135deg, #3498db, #2c3e50);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: white;
            margin: 0 auto 2rem;
        }
      .skills-section {
            margin-top: 3rem;
        }
      .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        } 
      .skill-item {
            background: #f8f9fa;
            padding: 1rem;
            border-radius: 8px;
            text-align: center;
        }
/* Contact Page Specific */
        .contact-content {
            max-width: 800px;
            margin: 0 auto;
        }
.contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
.contact-card {
            background: #f8f9fa;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
        }
.contact-card h3 {
            color: #3498db;
            margin-bottom: 1rem;
        }
.contact-form {
            background: #f8f9fa;
            padding: 2rem;
            border-radius: 10px;
        }
.form-group {
            margin-bottom: 1.5rem;
        }
.form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #333;
            font-weight: 500;
        }
.form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }
.form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #3498db;
        }
.submit-btn {
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            transition: transform 0.3s ease;
        }
.submit-btn:hover {
            transform: translateY(-2px);
        }
      /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
        }
 /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                gap: 1rem;
            }
             .hero h1 {
                font-size: 2rem;
            }
            .about-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            .page {
                margin: 10px;
                padding: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">ABCD SAMPLE WEB</div>
            <ul class="nav-links">
                <li><a href="#" onclick="showPage('home')" class="active">Home</a></li>
                <li><a href="#" onclick="showPage('about')">About</a></li>
                <li><a href="#" onclick="showPage('contact')">Contact</a></li>
            </ul>
        </nav>
    </header>
<main>
        <!-- HOME PAGE -->
        <div id="home" class="page active">
            <div class="container">
                <div class="hero">
                    <h1>Welcome to ABCD Sample Web</h1>
                    <p>Your Personal Digital Space</p>
                </div>
                <div class="welcome-card">
                    <h2>Hello & Welcome!</h2>
                    <p>This is your personal website showcasing who you are and what you do. Navigate through the pages to learn more about me and get in touch!</p>
                </div>

 <div class="features">
                    <div class="feature-card">
                        <div class="feature-icon">🏠</div>
                        <h3>Personal Space</h3>
                        <p>This is my digital home where I share my thoughts, experiences, and connect with others.</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">👨‍💻</div>
                        <h3>Professional</h3>
                        <p>Learn about my skills, experience, and professional background in the About section.</p>
                    </div>
                    <div class="feature-card">
                        <div class="feature-icon">📞</div>
                        <h3>Get In Touch</h3>
                        <p>Ready to connect? Visit the Contact page to reach out and start a conversation.</p>
                    </div>
                </div>
            </div>
        </div>
<!-- ABOUT PAGE -->
        <div id="about" class="page">
            <div class="container">
                <h1>About Me</h1>
                
<div class="about-content">
                    <div class="profile-section">
                        <div class="profile-image">👤</div>
                        <h2>ABCD Sample</h2>
                        <p><strong>Professional Title</strong></p>
                    </div>
                    <div class="bio-section">
                        <h2>My Story</h2>
                        <p>Welcome to my personal website! I'm passionate about creating meaningful connections and sharing knowledge with others. This space represents my journey, experiences, and the things that matter most to me.</p>
                        
                    <p>I believe in continuous learning and growth. Whether it's through professional development, personal projects, or connecting with like-minded individuals, I'm always looking for new opportunities to expand my horizons.</p>
                        
                        <p>When I'm not working, you can find me exploring new technologies, reading books, or enjoying time with family and friends. I believe that balance is key to a fulfilling life.</p>
                    </div>
                </div>

 <div class="skills-section">
                    <h2>My Skills & Interests</h2>
                    <div class="skills-grid">
                        <div class="skill-item">
                            <h3>Communication</h3>
                            <p>Strong verbal and written communication skills</p>
                        </div>
                        <div class="skill-item">
                            <h3>Problem Solving</h3>
                            <p>Creative approach to finding solutions</p>
                        </div>
                        <div class="skill-item">
                            <h3>Technology</h3>
                            <p>Comfortable with modern digital tools</p>
                        </div>
                        <div class="skill-item">
                            <h3>Leadership</h3>
                            <p>Experience in guiding teams and projects</p>
                        </div>
                        <div class="skill-item">
                            <h3>Creativity</h3>
                            <p>Innovative thinking and artistic expression</p>
                        </div>
                        <div class="skill-item">
                            <h3>Learning</h3>
                            <p>Passionate about continuous education</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
<!-- CONTACT PAGE -->
        <div id="contact" class="page">
            <div class="container">
                <div class="contact-content">
                    <h1>Get In Touch</h1>
                    <p style="text-align: center; font-size: 1.2rem; margin-bottom: 3rem;">
                        I'd love to hear from you! Whether you have a question, want to collaborate, or just want to say hello, feel free to reach out.
                    </p>

<div class="contact-info">
                        <div class="contact-card">
                            <h3>📧 Email</h3>
                            <p>sample@email.com</p>
                        </div>
                        <div class="contact-card">
                            <h3>📱 Phone</h3>
                            <p>+1 (555) 123-4567</p>
                        </div>
                        <div class="contact-card">
                            <h3>🌐 Social Media</h3>
                            <p>@abcd_sample</p>
                        </div>
                    </div>

  <div class="contact-form">
                        <h2>Send Me a Message</h2>
                        <form onsubmit="handleSubmit(event)">
                            <div class="form-group">
                                <label for="name">Your Name</label>
                                <input type="text" id="name" name="name" required>
                            </div>
                            <div class="form-group">
                                <label for="email">Your Email</label>
                                <input type="email" id="email" name="email" required>
                            </div>
                            <div class="form-group">
                                <label for="subject">Subject</label>
                                <input type="text" id="subject" name="subject" required>
                            </div>
                            <div class="form-group">
                                <label for="message">Message</label>
                                <textarea id="message" name="message" rows="5" required></textarea>
                            </div>
                            <button type="submit" class="submit-btn">Send Message</button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </main>
<footer>
        <div class="container">
            <p>&copy; 2025 ABCD Sample Web. All rights reserved.</p>
        </div>
    </footer>
 <script>
        // Page navigation
        function showPage(pageId) {
            // Hide all pages
            const pages = document.querySelectorAll('.page');
            pages.forEach(page => page.classList.remove('active'));
            // Show selected page
            document.getElementById(pageId).classList.add('active');
             // Update navigation active state
            const navLinks = document.querySelectorAll('.nav-links a');
            navLinks.forEach(link => link.classList.remove('active'));
            event.target.classList.add('active');
            // Update page title
            const titles = {
                'home': 'ABCD SAMPLE WEB - Home',
                'about': 'ABCD SAMPLE WEB - About',
                'contact': 'ABCD SAMPLE WEB - Contact'
            };
            document.title = titles[pageId];
        }
 // Form submission handler
        function handleSubmit(event) {
            event.preventDefault();
            const formData = new FormData(event.target);
            const data = Object.fromEntries(formData);
            alert(`Thank you, ${data.name}! Your message has been received. I'll get back to you soon!`);
            event.target.reset();
        }
// Smooth scrolling and header effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
            }
        });
// Initialize
        document.addEventListener('DOMContentLoaded', () => {
            showPage('home');
        });
    </script>
</body>
</html>
