<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nancy's Zen Yoga</title>
    <style>
        /* ===== RESET & BASE ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            color: #2d3f50;
            background-color: #f0f7ff;
        }

        /* ===== NAVIGATION ===== */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(240, 247, 255, 0.95);
            padding: 15px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
        }

        .logo {
            font-size: 1.6rem;
            color: #4a90b8;
            letter-spacing: 2px;
            font-style: bold;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: #2d3f50;
            font-size: 0.95rem;
            letter-spacing: 1px;
            text-transform: uppercase;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #4a90b8;
        }

        /* ===== HERO SECTION ===== */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #d6eaf8 0%, #e8f4fd 50%, #d0e8f5 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 20px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            color: #2471a3;
            margin-bottom: 15px;
            letter-spacing: 3px;
        }

        .hero-content p {
            font-size: 1.3rem;
            color: #5d7f99;
            margin-bottom: 30px;
            font-style: italic;
            max-width: 550px;
        }

        .btn {
            display: inline-block;
            padding: 14px 36px;
            background-color: #4a90b8;
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-size: 1rem;
            letter-spacing: 1px;
            transition: background-color 0.3s, transform 0.2s;
        }

        .btn:hover {
            background-color: #2471a3;
            transform: translateY(-2px);
        }

        .hero-emoji {
            font-size: 5rem;
            margin-bottom: 20px;
            display: block;
        }

        /* ===== ABOUT SECTION ===== */
        #about {
            padding: 90px 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 60px;
            max-width: 1100px;
            margin: 0 auto;
        }

        .about-image {
            width: 320px;
            height: 400px;
            background: linear-gradient(135deg, #aed6f1, #d6eaf8);
            border-radius: 60% 40% 55% 45% / 50% 60% 40% 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 8rem;
            flex-shrink: 0;
        }

        .about-text h2 {
            font-size: 2.2rem;
            color: #2471a3;
            margin-bottom: 20px;
        }

        .about-text p {
            font-size: 1.05rem;
            line-height: 1.9;
            color: #4a6478;
            margin-bottom: 15px;
        }

        .certifications {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .cert-badge {
            background-color: #d6eaf8;
            color: #2471a3;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: bold;
            border: 1px solid #aed6f1;
        }

        /* ===== SERVICES SECTION ===== */
        #services {
            background-color: #e8f4fd;
            padding: 90px 40px;
            text-align: center;
        }

        #services h2 {
            font-size: 2.2rem;
            color: #2471a3;
            margin-bottom: 12px;
        }

        #services .subtitle {
            color: #7a9cb5;
            font-style: italic;
            margin-bottom: 50px;
            font-size: 1.05rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 30px;
            max-width: 1100px;
            margin: 0 auto;
        }

        .service-card {
            background: white;
            padding: 40px 25px;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(74, 144, 184, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .service-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 10px 30px rgba(74, 144, 184, 0.2);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .service-card h3 {
            font-size: 1.2rem;
            color: #2471a3;
            margin-bottom: 12px;
        }

        .service-card p {
            color: #6a8fa8;
            font-size: 0.95rem;
            line-height: 1.7;
            margin-bottom: 15px;
        }

        .price {
            font-size: 1.3rem;
            font-weight: bold;
            color: #4a90b8;
        }

        /* ===== TESTIMONIALS SECTION ===== */
        #testimonials {
            padding: 90px 40px;
            text-align: center;
            background-color: #f0f7ff;
        }

        #testimonials h2 {
            font-size: 2.2rem;
            color: #2471a3;
            margin-bottom: 12px;
        }

        #testimonials .subtitle {
            color: #7a9cb5;
            font-style: italic;
            margin-bottom: 50px;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            max-width: 1000px;
            margin: 0 auto;
        }

        .testimonial-card {
            background: white;
            padding: 35px 28px;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(74, 144, 184, 0.1);
            text-align: left;
            border-top: 4px solid #4a90b8;
        }

        .stars {
            color: #f0c060;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .testimonial-card p {
            color: #4a6478;
            font-style: italic;
            line-height: 1.8;
            margin-bottom: 20px;
        }

        .client-name {
            font-weight: bold;
            color: #2471a3;
            font-size: 0.95rem;
        }

        /* ===== SCHEDULE SECTION ===== */
        #schedule {
            background: linear-gradient(135deg, #d6eaf8, #dce8f5);
            padding: 90px 40px;
            text-align: center;
        }

        #schedule h2 {
            font-size: 2.2rem;
            color: #2471a3;
            margin-bottom: 12px;
        }

        #schedule .subtitle {
            color: #7a9cb5;
            font-style: italic;
            margin-bottom: 50px;
        }

        .schedule-table {
            max-width: 700px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(74, 144, 184, 0.15);
        }

        .schedule-row {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            padding: 18px 30px;
            border-bottom: 1px solid #d6eaf8;
            align-items: center;
        }

        .schedule-row:last-child {
            border-bottom: none;
        }

        .schedule-row.header {
            background-color: #4a90b8;
            color: white;
            font-weight: bold;
            letter-spacing: 1px;
        }

        .schedule-row:not(.header):hover {
            background-color: #eaf4fb;
        }

        .schedule-row span {
            font-size: 0.95rem;
            color: #4a6478;
        }

        .schedule-row.header span {
            color: white;
        }

        .available {
            color: #2471a3 !important;
            font-weight: bold;
        }

        /* ===== CONTACT SECTION ===== */
        #contact {
            padding: 90px 40px;
            text-align: center;
            background-color: #f0f7ff;
        }

        #contact h2 {
            font-size: 2.2rem;
            color: #2471a3;
            margin-bottom: 12px;
        }

        #contact .subtitle {
            color: #7a9cb5;
            font-style: italic;
            margin-bottom: 50px;
        }

        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            max-width: 900px;
            margin: 0 auto;
            text-align: left;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 18px;
        }

        .contact-form input,
        .contact-form select,
        .contact-form textarea {
            padding: 14px 18px;
            border: 1px solid #aed6f1;
            border-radius: 10px;
            font-size: 0.95rem;
            font-family: 'Georgia', serif;
            background: #f0f7ff;
            color: #2d3f50;
            transition: border-color 0.3s;
            outline: none;
        }

        .contact-form input:focus,
        .contact-form select:focus,
        .contact-form textarea:focus {
            border-color: #4a90b8;
        }

        .contact-form textarea {
            height: 130px;
            resize: vertical;
        }

        .contact-form button {
            padding: 14px;
            background-color: #4a90b8;
            color: white;
            border: none;
            border-radius: 30px;
            font-size: 1rem;
            cursor: pointer;
            letter-spacing: 1px;
            transition: background-color 0.3s, transform 0.2s;
        }

        .contact-form button:hover {
            background-color: #2471a3;
            transform: translateY(-2px);
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
            justify-content: center;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .contact-item .icon {
            width: 50px;
            height: 50px;
            background-color: #d6eaf8;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            flex-shrink: 0;
        }

        .contact-item p {
            color: #4a6478;
            font-size: 0.95rem;
            line-height: 1.6;
        }

        .contact-item strong {
            color: #2471a3;
            display: block;
            margin-bottom: 3px;
        }

        /* ===== FOOTER ===== */
        footer {
            background-color: #2471a3;
            color: #d6eaf8;
            text-align: center;
            padding: 40px 20px;
        }

        footer .footer-logo {
            font-size: 1.8rem;
            font-style: italic;
            letter-spacing: 2px;
            margin-bottom: 15px;
        }

        footer p {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 8px;
        }

        footer .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
            font-size: 1.5rem;
        }

        footer .social-links a {
            text-decoration: none;
            transition: transform 0.2s;
            display: inline-block;
        }

        footer .social-links a:hover {
            transform: scale(1.2);
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.2rem;
            }

            #about {
                flex-direction: column;
                padding: 70px 30px;
                text-align: center;
            }

            .about-image {
                width: 220px;
                height: 270px;
                font-size: 5rem;
            }

            .contact-container {
                grid-template-columns: 1fr;
            }

            nav {
                padding: 15px 20px;
            }

            .nav-links {
                gap: 15px;
            }

            .nav-links a {
                font-size: 0.8rem;
            }
        }
    </style>
</head>
<body>

    <!-- NAVIGATION -->
    <nav>
        <div class="logo">Nancy's Zen Yoga</div>
        <ul class="nav-links">
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#testimonials">Reviews</a></li>
            <li><a href="#schedule">Schedule</a></li>
            <li><a href="#contact">Book Now</a></li>
        </ul>
    </nav>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="hero-content">
            <span class="hero-emoji">🧘‍♀️</span>
            <h1>Find Your Flow</h1>
            <p>Personalized yoga instruction in the comfort of your own home or location of your choosing</p>
            <a href="#contact" class="btn">Book a Session</a>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about">
        <div class="about-image">🧘</div>
        <div class="about-text">
            <h2>Hello, I'm Nancy</h2>
            <p>
                With over 10 years of practice and 5 years of teaching experience,
                I bring the studio to you. I believe yoga should be accessible to
                everyone — beginners, busy parents, seniors, or seasoned practitioners.
            </p>
            <p>
                My approach blends mindful movement, breathwork, and relaxation
                techniques tailored specifically to your body and goals. Every
                session is uniquely yours.
            </p>
            <div class="certifications">
                <span class="cert-badge">✅ RYT-500 Certified</span>
                <span class="cert-badge">✅ Prenatal Yoga</span>
                <span class="cert-badge">✅ Restorative Yoga</span>
                <span class="cert-badge">✅ First Aid Certified</span>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section id="services">
        <h2>Services & Pricing</h2>
        <p class="subtitle">Bringing balance and wellness to your doorstep</p>
        <div class="services-grid">

            <div class="service-card">
                <div class="service-icon">🌱</div>
                <h3>Beginner Session</h3>
                <p>Perfect for those new to yoga. Learn foundational poses, breathing, and mindfulness in a gentle, supportive environment.</p>
                <div class="price">$65 / hr</div>
            </div>

            <div class="service-card">
                <div class="service-icon">🔥</div>
                <h3>Power Flow</h3>
                <p>A dynamic, energizing practice linking breath with movement. Build strength, flexibility, and endurance.</p>
                <div class="price">$75 / hr</div>
            </div>

            <div class="service-card">
                <div class="service-icon">🌙</div>
                <h3>Restorative Yoga</h3>
                <p>Deep relaxation using props and supported poses. Ideal for stress relief, recovery, and nervous system regulation.</p>
                <div class="price">$65 / hr</div>
            </div>

            <div class="service-card">
                <div class="service-icon">🤰</div>
                <h3>Prenatal Yoga</h3>
                <p>Safe, nurturing yoga designed for all stages of pregnancy. Support comfort, connection, and preparation for birth.</p>
                <div class="price">$75 / hr</div>
            </div>

            <div class="service-card">
                <div class="service-icon">👨‍👩‍👧</div>
                <h3>Couples / Pairs</h3>
                <p>Practice together with a partner, friend, or family member. Shared sessions split the cost and double the fun!</p>
                <div class="price">$95 / hr</div>
            </div>

            <div class="service-card">
                <div class="service-icon">📦</div>
                <h3>Monthly Package</h3>
                <p>Commit to your wellness journey with 8 sessions per month. Best value for consistent, transformative practice.</p>
                <div class="price">$450 / mo</div>
            </div>

        </div>
    </section>

    <!-- TESTIMONIALS SECTION -->
    <section id="testimonials">
        <h2>What Clients Say</h2>
        <p class="subtitle">Real experiences from real people</p>
        <div class="testimonials-grid">

            <div class="testimonial-card">
                <div class="stars">★★★★★</div>
                <p>"Nancy completely transformed my mornings. Having her come to my home means no commute, no excuses — just pure yoga. I've never felt better!"</p>
                <span class="client-name">— Jessica M.</span>
            </div>

            <div class="testimonial-card">
                <div class="stars">★★★★★</div>
                <p>"As a total beginner, I was nervous, but Nancy made me feel so comfortable. She adapts every session to exactly what I need. Highly recommend!"</p>
                <span class="client-name">— Tom R.</span>
            </div>

            <div class="testimonial-card">
                <div class="stars">★★★★★</div>
                <p>"The prenatal sessions were a lifesaver during my third trimester. Nancy is knowledgeable, caring, and so professional. Booking continued after baby!"</p>
                <span class="client-name">— Amanda K.</span>
            </div>

        </div>
    </section>

    <!-- SCHEDULE SECTION -->
    <section id="schedule">
        <h2>Availability</h2>
        <p class="subtitle">Flexible scheduling to fit your lifestyle</p>
        <div class="schedule-table">
            <div class="schedule-row header">
                <span>Day</span>
                <span>Morning</span>
                <span>Evening</span>
            </div>
            <div class="schedule-row">
                <span>Monday</span>
                <span class="available">✓ 7am–11am</span>
                <span class="available">✓ 5pm–8pm</span>
            </div>
            <div class="schedule-row">
                <span>Tuesday</span>
                <span class="available">✓ 7am–11am</span>
                <span>— Unavailable</span>
            </div>
            <div class="schedule-row">
                <span>Wednesday</span>
                <span class="available">✓ 8am–12pm</span>
                <span class="available">✓ 5pm–8pm</span>
            </div>
            <div class="schedule-row">
                <span>Thursday</span>
                <span>— Unavailable</span>
                <span class="available">✓ 4pm–8pm</span>
            </div>
            <div class="schedule-row">
                <span>Friday</span>
                <span class="available">✓ 7am–11am</span>
                <span class="available">✓ 5pm–7pm</span>
            </div>
            <div class="schedule-row">
                <span>Saturday</span>
                <span class="available">✓ 8am–1pm</span>
                <span>— Unavailable</span>
            </div>
            <div class="schedule-row">
                <span>Sunday</span>
                <span class="available">✓ 9am–12pm</span>
                <span>— Unavailable</span>
            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact">
        <h2>Book a Session</h2>
        <p class="subtitle">Ready to begin your journey? Reach out today!</p>
        <div class="contact-container">

            <form class="contact-form">
                <input type="text" placeholder="Your Name" required />
                <input type="email" placeholder="Your Email" required />
                <input type="tel" placeholder="Your Phone Number" />
                <select>
                    <option value="" disabled selected>Select a Service</option>
                    <option>Beginner Session – $65/hr</option>
                    <option>Power Flow – $75/hr</option>
                    <option>Restorative Yoga – $65/hr</option>
                    <option>Prenatal Yoga – $75/hr</option>
                    <option>Couples / Pairs – $95/hr</option>
                    <option>Monthly Package – $450/mo</option>
                </select>
                <input type="text" placeholder="Preferred Day & Time" />
                <textarea placeholder="Any health considerations, goals, or questions?"></textarea>
                <button type="submit">Send Booking Request 💙</button>
            </form>

            <div class="contact-info">
                <div class="contact-item">
                    <div class="icon">📍</div>
                    <p>
                        <strong>Service Area</strong>
                        Serving the greater San Diego, CA area<br>
                        within a 15-mile radius
                    </p>
                </div>
                <div class="contact-item">
                    <div class="icon">📞</div>
                    <p>
                        <strong>Phone</strong>
                        (619) 555-0198
                    </p>
                </div>
                <div class="contact-item">
                    <div class="icon">📧</div>
                    <p>
                        <strong>Email</strong>
                        nancy@zenyoga.com
                    </p>
                </div>
                <div class="contact-item">
                    <div class="icon">⏱️</div>
                    <p>
                        <strong>Response Time</strong>
                        I typically respond within 24 hours
                    </p>
                </div>
                <div class="contact-item">
                    <div class="icon">🧘</div>
                    <p>
                        <strong>First Session</strong>
                        Free 15-minute consultation call included with your first booking!
                    </p>
                </div>
            </div>

        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-logo">Zen Yoga</div>
        <div class="social-links">
            <a href="#" title="Instagram">📸</a>
            <a href="#" title="Facebook">📘</a>
            <a href="#" title="YouTube">▶️</a>
        </div>
        <p>© 2024 Nanc's Zen Yoga | Nancy Malabarba, RYT-500</p>
        <p>Bringing wellness to your doorstep in San Diego, CA</p>
    </footer>

</body>
</html>
