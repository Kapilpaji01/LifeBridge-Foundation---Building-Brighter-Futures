<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LifeBridge Foundation - Building Brighter Futures</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header & Navigation */
        header {
            background: linear-gradient(135deg, #2e7d32 0%, #1b5e20 100%);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #ffb74d;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            margin-top: 0.5rem;
        }

        .btn {
            padding: 0.7rem 1.5rem;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-donate {
            background: #ff6f00;
            color: white;
        }

        .btn-donate:hover {
            background: #e65100;
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(255,111,0,0.4);
        }

        .btn-volunteer {
            background: #43a047;
            color: white;
        }

        .btn-volunteer:hover {
            background: #2e7d32;
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(67,160,71,0.4);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%232e7d32" width="1200" height="600"/><circle cx="300" cy="150" r="80" fill="%2343a047" opacity="0.3"/><circle cx="900" cy="400" r="120" fill="%231b5e20" opacity="0.3"/></svg>');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 8rem 2rem;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 2rem;
        }

        /* Section Styles */
        section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #2e7d32;
        }

        /* Mission Section */
        .mission-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .mission-card {
            text-align: center;
            padding: 2rem;
            background: #f5f5f5;
            border-radius: 10px;
            transition: transform 0.3s;
        }

        .mission-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .mission-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        /* Impact Counter */
        .impact-stats {
            background: linear-gradient(135deg, #1976d2 0%, #1565c0 100%);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .stat-item {
            padding: 1.5rem;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 25px rgba(0,0,0,0.15);
        }

        .project-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #43a047 0%, #2e7d32 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-status {
            display: inline-block;
            padding: 0.3rem 1rem;
            background: #43a047;
            color: white;
            border-radius: 15px;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        /* Get Involved Section */
        .get-involved {
            background: #f9f9f9;
        }

        .involvement-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .involvement-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            text-align: center;
        }

        .involvement-card h3 {
            color: #2e7d32;
            margin: 1rem 0;
        }

        /* Form Styles */
        .form-container {
            max-width: 600px;
            margin: 2rem auto;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 3px 15px rgba(0,0,0,0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
            color: #333;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 100px;
        }

        /* Testimonials */
        .testimonials {
            background: #e8f5e9;
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .testimonial-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }

        .testimonial-text {
            font-style: italic;
            margin-bottom: 1rem;
        }

        .testimonial-author {
            font-weight: bold;
            color: #2e7d32;
        }

        /* Footer */
        footer {
            background: #1b5e20;
            color: white;
            padding: 3rem 2rem 1rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1rem;
        }

        .footer-section a {
            color: white;
            text-decoration: none;
            display: block;
            margin-bottom: 0.5rem;
        }

        .footer-section a:hover {
            color: #ffb74d;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-icon {
            width: 40px;
            height: 40px;
            background: white;
            color: #1b5e20;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            transition: all 0.3s;
        }

        .social-icon:hover {
            background: #ffb74d;
            transform: scale(1.1);
        }

        .footer-bottom {
            text-align: center;
            margin-top: 2rem;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.2);
        }

        .newsletter-form {
            display: flex;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .newsletter-form input {
            flex: 1;
            padding: 0.8rem;
            border: none;
            border-radius: 5px;
        }

        .newsletter-form button {
            padding: 0.8rem 1.5rem;
            background: #ff6f00;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
        }

        .newsletter-form button:hover {
            background: #e65100;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .nav-links {
                display: none;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        /* Hidden sections for single-page navigation */
        .page-section {
            scroll-margin-top: 80px;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">🌉 LifeBridge Foundation</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#get-involved">Get Involved</a></li>
                <li><a href="#impact">Impact</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="cta-buttons">
                <a href="#donate" class="btn btn-donate">Donate Now</a>
                <a href="#volunteer" class="btn btn-volunteer">Join Us</a>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero page-section">
        <h1>Together for Education, Environment, and Empowerment</h1>
        <p>Building brighter futures through compassion and action. Join us in creating sustainable change that uplifts communities and transforms lives.</p>
        <div class="cta-buttons" style="justify-content: center;">
            <a href="#get-involved" class="btn btn-volunteer">Learn More</a>
            <a href="#donate" class="btn btn-donate">Support Our Cause</a>
        </div>
    </section>

    <!-- Mission Snapshot -->
<section class="mission-section">
    <h2 class="section-title">Our Mission</h2>
    <p class="mission-intro">
        At <strong>LifeBridge Foundation</strong>, our mission is to build a bridge of hope and opportunity for communities in need. 
        Through education, environmental protection, community development, and empowerment initiatives, we work hand-in-hand 
        to create sustainable and meaningful change that transforms lives.
    </p>

    <div class="mission-grid">
        <div class="mission-card">
            <div class="mission-icon">📚</div>
            <h3>Education</h3>
            <p>Providing quality education, skill-building programs, and learning resources to unlock potential and inspire brighter futures.</p>
        </div>

        <div class="mission-card">
            <div class="mission-icon">🌱</div>
            <h3>Environment</h3>
            <p>Protecting nature through tree plantation, recycling initiatives, and awareness campaigns for a cleaner, greener planet.</p>
        </div>

        <div class="mission-card">
            <div class="mission-icon">🤝</div>
            <h3>Community</h3>
            <p>Strengthening communities with support programs, health initiatives, and collaborative efforts that promote unity and growth.</p>
        </div>

        <div class="mission-card">
            <div class="mission-icon">💪</div>
            <h3>Empowerment</h3>
            <p>Equipping individuals and families with opportunities, tools, and confidence to shape their own future and thrive.</p>
        </div>
    </div>
</section>

    <!-- Impact Stats -->
    <section class="impact-stats page-section" id="impact">
        <h2 style="font-size: 2.5rem; margin-bottom: 3rem;">Our Impact</h2>
        <div class="stats-grid">
            <div class="stat-item">
                <div class="stat-number">50+</div>
                <div>Volunteers</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">1000+</div>
                <div>Lives Impacted</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">200+</div>
                <div>Trees Planted</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">10+</div>
                <div>Projects Completed</div>
            </div>
        </div>
    </section>

    <!-- About Us -->
    <section id="about" class="page-section">
        <h2 class="section-title">About Us</h2>
        <div style="max-width: 800px; margin: 0 auto;">
            <h3 style="color: #2e7d32; margin-bottom: 1rem;">Our Vision</h3>
            <p style="margin-bottom: 2rem;">A world where every individual has access to education, a healthy environment, and opportunities to thrive within supportive communities.</p>
            
            <h3 style="color: #2e7d32; margin-bottom: 1rem;">Our Values</h3>
            <ul style="list-style-position: inside; margin-bottom: 2rem;">
                <li>Compassion: We lead with empathy and understanding</li>
                <li>Transparency: We operate with honesty and accountability</li>
                <li>Collaboration: We believe in the power of working together</li>
                <li>Sustainability: We focus on long-term, lasting impact</li>
                <li>Inclusivity: We welcome and value every voice</li>
            </ul>

            <h3 style="color: #2e7d32; margin-bottom: 1rem;">Our Story</h3>
            <p>Founded with a vision to bridge communities and create lasting positive change, LifeBridge Foundation began as a small group of passionate individuals committed to making a difference. Today, we've grown into a network of dedicated volunteers, partners, and supporters working together to transform lives across multiple communities.</p>
        </div>
    </section>

    <!-- Projects -->
    <section id="projects" class="page-section">
        <h2 class="section-title">Our Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-image">📖</div>
                <div class="project-content">
                    <span class="project-status">Ongoing</span>
                    <h3>Digital Literacy Program</h3>
                    <p>Providing computer education and digital skills training to 500 students in rural areas. Progress: 65% complete.</p>
                </div>
            </div>
            <div class="project-card">
                <div class="project-image">🌳</div>
                <div class="project-content">
                    <span class="project-status" style="background: #1976d2;">Completed</span>
                    <h3>Green Valley Initiative</h3>
                    <p>Successfully planted 2,000 trees and established 5 community gardens, creating greener spaces for families.</p>
                </div>
            </div>
            <div class="project-card">
                <div class="project-image">💧</div>
                <div class="project-content">
                    <span class="project-status">Ongoing</span>
                    <h3>Clean Water Access</h3>
                    <p>Installing water purification systems in 10 villages, providing clean drinking water to 1,200 families.</p>
                </div>
            </div>
            <div class="project-card">
                <div class="project-image">👩‍🏫</div>
                <div class="project-content">
                    <span class="project-status" style="background: #1976d2;">Completed</span>
                    <h3>Women's Empowerment Workshops</h3>
                    <p>Trained 300 women in vocational skills, helping them start their own small businesses and achieve financial independence.</p>
                </div>
            </div>
            <div class="project-card">
                <div class="project-image">🏥</div>
                <div class="project-content">
                    <span class="project-status">Ongoing</span>
                    <h3>Community Health Camps</h3>
                    <p>Organizing free health checkups and awareness programs in underserved areas. 15 camps completed this year.</p>
                </div>
            </div>
            <div class="project-card">
                <div class="project-image">🎓</div>
                <div class="project-content">
                    <span class="project-status">Ongoing</span>
                    <h3>Scholarship Program</h3>
                    <p>Supporting 100 underprivileged students with scholarships, school supplies, and mentorship opportunities.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Get Involved -->
    <section id="get-involved" class="get-involved page-section">
        <h2 class="section-title">Get Involved</h2>
        <div class="involvement-grid">
            <div class="involvement-card">
                <div style="font-size: 3rem; margin-bottom: 1rem;">🤲</div>
                <h3>Volunteer</h3>
                <p>Join hands with us to make a difference. Whether it's teaching, planting, or simply sharing your time, every effort counts.</p>
                <a href="#volunteer" class="btn btn-volunteer" style="margin-top: 1rem;">Sign Up</a>
            </div>
            <div class="involvement-card">
                <div style="font-size: 3rem; margin-bottom: 1rem;">💝</div>
                <h3>Donate</h3>
                <p>Your contribution isn't just a donation — it's a lifeline. Help us plant more trees, educate more children, and bring hope to more families.</p>
                <a href="#donate" class="btn btn-donate" style="margin-top: 1rem;">Donate Now</a>
            </div>
            <div class="involvement-card">
                <div style="font-size: 3rem; margin-bottom: 1rem;">🤝</div>
                <h3>Partner With Us</h3>
                <p>Organizations and businesses can collaborate with us to create larger impact and reach more communities.</p>
                <a href="#contact" class="btn btn-volunteer" style="margin-top: 1rem;">Partner</a>
            </div>
        </div>
    </section>

    <!-- Volunteer Form -->
    <section id="volunteer" class="page-section">
        <h2 class="section-title">Volunteer Registration</h2>
        <div class="form-container">
            <form id="volunteerForm">
                <div class="form-group">
                    <label for="name">Full Name *</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email *</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="phone">Phone Number *</label>
                    <input type="tel" id="phone" name="phone" required>
                </div>
                <div class="form-group">
                    <label for="skills">Your Skills/Interests</label>
                    <input type="text" id="skills" name="skills" placeholder="e.g., Teaching, Environmental work, Event planning">
                </div>
                <div class="form-group">
                    <label for="availability">Availability</label>
                    <select id="availability" name="availability">
                        <option>Weekends</option>
                        <option>Weekdays</option>
                        <option>Flexible</option>
                        <option>Monthly</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="project">Preferred Project Area</label>
                    <select id="project" name="project">
                        <option>Education</option>
                        <option>Environment</option>
                        <option>Community Service</option>
                        <option>Health</option>
                        <option>Any/All</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="message">Why do you want to volunteer?</label>
                    <textarea id="message" name="message"></textarea>
                </div>
                <button type="submit" class="btn btn-volunteer" style="width: 100%;">Submit Application</button>
            </form>
        </div>
    </section>

    <!-- Donation Section -->
    <section id="donate" class="page-section">
        <h2 class="section-title">Support Our Cause</h2>
        <div class="form-container">
            <p style="text-align: center; margin-bottom: 2rem;">Every contribution makes a real difference. Choose how you'd like to help:</p>
            <div class="involvement-grid">
                <div class="involvement-card">
                    <h3>₹500</h3>
                    <p>Plants 10 trees</p>
                    <button class="btn btn-donate" style="margin-top: 1rem;">Donate</button>
                </div>
                <div class="involvement-card">
                    <h3>₹2,000</h3>
                    <p>Provides school supplies for 5 children</p>
                    <button class="btn btn-donate" style="margin-top: 1rem;">Donate</button>
                </div>
                <div class="involvement-card">
                    <h3>₹5,000</h3>
                    <p>Sponsors a child's education for 6 months</p>
                    <button class="btn btn-donate" style="margin-top: 1rem;">Donate</button>
                </div>
            </div>
            <div style="text-align: center; margin-top: 2rem;">
                <p>Or enter a custom amount:</p>
                <form style="display: flex; gap: 1rem; max-width: 400px; margin: 1rem auto;">
                    <input type="number" placeholder="Enter amount" style="flex: 1; padding: 0.8rem; border: 1px solid #ddd; border-radius: 5px;">
                    <button type="submit" class="btn btn-donate">Donate</button>
                </form>
                <p style="margin-top: 1rem; font-size: 0.9rem; color: #666;">We accept PayPal, Credit/Debit Cards, and UPI</p>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials page-section">
        <h2 class="section-title">What People Say</h2>
        <div class="testimonial-grid">
            <div class="testimonial-card">
                <p class="testimonial-text">"LifeBridge Foundation gave me the opportunity to give back to my community. Being a volunteer here has been one of the most rewarding experiences of my life."</p>
                <p class="testimonial-author">— Kshish Thakre, Volunteer</p>
            </div>
            <div class="testimonial-card">
                <p class="testimonial-text">"Thanks to their scholarship program, my daughter can now continue her education. This organization truly cares about making a difference."</p>
                <p class="testimonial-author">— Hemlata Thakre, Parent</p>
            </div>
            <div class="testimonial-card">
                <p class="testimonial-text">"Working with LifeBridge Foundation on the Green Valley Initiative was inspiring. Their commitment to environmental sustainability is remarkable."</p>
                <p class="testimonial-author">— Rajesh Thakre, Partner Organization</p>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="page-section">
        <h2 class="section-title">Contact Us</h2>
        <div class="form-container">
            <form id="contactForm">
                <div class="form-group">
                    <label for="contact-name">Name *</label>
                    <input type="text" id="contact-name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="contact-email">Email *</label>
                    <input type="email" id="contact-email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="subject">Subject *</label>
                    <input type="text" id="subject" name="subject" required>
                </div>
                <div class="form-group">
                    <label for="contact-message">Message *</label>
                    <textarea id="contact-message" name="message" required></textarea>
                </div>
                <button type="submit" class="btn btn-volunteer" style="width: 100%;">Send Message</button>
            </form>
            <div style="margin-top: 2rem; text-align: center;">
                <p><strong>Email:</strong> info@lifebridgefoundation.org</p>
                <p><strong>Phone:</strong> +91 7617302824</p>
                <p><strong>Address:</strong> 123 thakre brothes , Community Center, Amla, Betul , Madhya Pradesh 460551</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>About LifeBridge Foundation</h3>
                <p>Building connections and creating sustainable change through education, environmental protection, and community empowerment.</p>
                <div class="social-links">
                    <a href="#" class="social-icon">f</a>
                    <a href="#" class="social-icon">📷</a>
                    <a href="#" class="social-icon">in</a>
                    <a href="#" class="social-icon">🐦</a>
                </div>
            </div>
            <div class="footer-section">
                <h3>Quick Links</h3>
                <a href="#about">About Us</a>
                <a href="#projects">Projects</a>
                <a href="#impact">Our Impact</a>
                <a href="#volunteer">Volunteer</a>
                <a href="#donate">Donate</a>
            </div>
            <div class="footer-section">
                <h3>Resources</h3>
                <a href="#">Annual Reports</a>
                <a href="#">Financial Statements</a>
                <a href="#">Blog</a>
                <a href="#">FAQs</a>
                <a href="#">Privacy Policy</a>
            </div>
            <div class="footer-section">
                <h3>Newsletter</h3>
                <p>Get updates on how your support changes lives.</p>
                <form class="newsletter-form">
                    <input type="email" placeholder="Your email">
                    <button type="submit">Subscribe</button>
                </form>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2024 LifeBridge Foundation. All rights reserved. | Registered Non-Profit Organization</p>
        </div>
