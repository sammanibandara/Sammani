<!DOCTYPE html>
<html lang="en">
<head> 
            
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
