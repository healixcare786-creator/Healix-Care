<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Healix Care - Premium Mobile Accessories</title>
    <style>
        /* Global Styles */
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #2ecc71;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            text-decoration: none;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: #2980b9;
            transform: translateY(-2px);
        }
        
        .btn-danger {
            background: var(--accent);
        }
        
        .btn-danger:hover {
            background: #c0392b;
        }
        
        .btn-success {
            background: var(--success);
        }
        
        .btn-success:hover {
            background: #27ae60;
        }
        
        .btn-whatsapp {
            background: #25D366;
        }
        
        .btn-whatsapp:hover {
            background: #128C7E;
        }
        
        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo-img {
            height: 50px;
            margin-right: 10px;
        }
        
        .logo h1 {
            font-size: 24px;
            background: linear-gradient(45deg, #3498db, #2ecc71);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            cursor: pointer;
        }
        
        nav ul li a:hover, nav ul li a.active {
            color: var(--secondary);
        }
        
        .cart-icon {
            position: relative;
        }
        
        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: var(--accent);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
        }
        
        .language-selector {
            display: flex;
            align-items: center;
        }
        
        .language-selector select {
            padding: 8px 12px;
            border-radius: 4px;
            border: none;
            background: white;
            margin-left: 10px;
        }
        
        /* Hero Slider */
        .hero-slider {
            position: relative;
            height: 500px;
            overflow: hidden;
            margin-bottom: 50px;
        }
        
        .slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            transition: opacity 1s ease;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
        }
        
        .slide.active {
            opacity: 1;
        }
        
        .slide-content {
            background: rgba(44, 62, 80, 0.8);
            color: white;
            padding: 40px;
            max-width: 600px;
            border-radius: 8px;
            margin-left: 10%;
        }
        
        .slide-content h2 {
            font-size: 42px;
            margin-bottom: 20px;
        }
        
        .slide-content p {
            font-size: 18px;
            margin-bottom: 30px;
        }
        
        .slider-nav {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
        }
        
        .slider-dot {
            width: 12px;
            height: 12px;
            background: rgba(255,255,255,0.5);
            border-radius: 50%;
            margin: 0 5px;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .slider-dot.active {
            background: white;
        }
        
        /* Page Sections */
        .page-section {
            display: none;
            padding: 80px 0;
            min-height: 60vh;
        }
        
        .page-section.active {
            display: block;
        }
        
        /* Products Section */
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 32px;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: var(--secondary);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
        }
        
        .product-image {
            height: 200px;
            background-color: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        
        .product-image img {
            max-width: 100%;
            max-height: 100%;
            object-fit: cover;
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-info h3 {
            font-size: 18px;
            margin-bottom: 10px;
        }
        
        .product-info p {
            color: #666;
            margin-bottom: 15px;
            font-size: 14px;
        }
        
        .product-price {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .price {
            font-weight: bold;
            font-size: 18px;
            color: var(--primary);
        }
        
        /* Cart Page */
        .cart-container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
        }
        
        .cart-items {
            background: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .cart-item {
            display: flex;
            padding: 15px 0;
            border-bottom: 1px solid #eee;
        }
        
        .cart-item:last-child {
            border-bottom: none;
        }
        
        .cart-item-image {
            width: 100px;
            height: 100px;
            margin-right: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #f5f5f5;
            border-radius: 4px;
        }
        
        .cart-item-image img {
            max-width: 100%;
            max-height: 100%;
        }
        
        .cart-item-details {
            flex: 1;
        }
        
        .cart-item-details h3 {
            margin-bottom: 5px;
        }
        
        .cart-item-details p {
            color: #666;
            margin-bottom: 10px;
        }
        
        .cart-item-controls {
            display: flex;
            align-items: center;
        }
        
        .quantity-controls {
            display: flex;
            align-items: center;
            margin-right: 15px;
        }
        
        .quantity-btn {
            width: 30px;
            height: 30px;
            background: #f0f0f0;
            border: none;
            border-radius: 4px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }
        
        .quantity {
            margin: 0 10px;
            font-weight: bold;
        }
        
        .cart-summary {
            background: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            height: fit-content;
        }
        
        .summary-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }
        
        .summary-total {
            font-weight: bold;
            font-size: 18px;
            color: var(--primary);
        }
        
        /* Checkout Page */
        .checkout-container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
        }
        
        .checkout-form {
            background: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .checkout-summary {
            background: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            height: fit-content;
        }
        
        .checkout-item {
            display: flex;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }
        
        .checkout-item-image {
            width: 60px;
            height: 60px;
            margin-right: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #f5f5f5;
            border-radius: 4px;
        }
        
        .checkout-item-image img {
            max-width: 100%;
            max-height: 100%;
        }
        
        .checkout-item-details {
            flex: 1;
        }
        
        .checkout-item-details h4 {
            margin-bottom: 5px;
            font-size: 14px;
        }
        
        .checkout-item-details p {
            font-size: 12px;
            color: #666;
        }
        
        /* About Page */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }
        
        .about-image {
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .about-text h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .about-text p {
            margin-bottom: 15px;
        }
        
        /* Contact Page */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }
        
        .contact-info {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .contact-info h3 {
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .contact-details {
            margin-bottom: 30px;
        }
        
        .contact-details p {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        
        .contact-details i {
            margin-right: 10px;
            color: var(--secondary);
            width: 20px;
        }
        
        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 10px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        /* WhatsApp Help */
        .whatsapp-help {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
        }
        
        .whatsapp-btn {
            display: flex;
            align-items: center;
            background: #25D366;
            color: white;
            padding: 12px 20px;
            border-radius: 50px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .whatsapp-btn:hover {
            background: #128C7E;
            transform: translateY(-3px);
        }
        
        .whatsapp-btn i {
            font-size: 24px;
            margin-right: 10px;
        }
        
        /* Footer */
        footer {
            background: var(--primary);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 18px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background: var(--secondary);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
            cursor: pointer;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: var(--secondary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #bbb;
            font-size: 14px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 5px 10px;
            }
            
            .language-selector {
                margin-top: 15px;
            }
            
            .hero-slider {
                height: 400px;
            }
            
            .slide-content {
                margin-left: 5%;
                padding: 20px;
            }
            
            .slide-content h2 {
                font-size: 32px;
            }
            
            .about-content,
            .contact-container,
            .cart-container,
            .checkout-container {
                grid-template-columns: 1fr;
            }
        }
        
        /* Language-specific styles */
        .rtl {
            direction: rtl;
            text-align: right;
        }
        
        .rtl .footer-column h3::after {
            left: auto;
            right: 0;
        }
        
        .rtl .section-title h2::after {
            left: auto;
            right: 50%;
            transform: translateX(50%);
        }
        
        .rtl .contact-details i {
            margin-right: 0;
            margin-left: 10px;
        }
        
        .rtl .cart-item-image,
        .rtl .checkout-item-image {
            margin-right: 0;
            margin-left: 20px;
        }
        
        /* Font Awesome Icons */
        .fa, .fas, .far, .fal, .fab {
            font-family: 'Font Awesome 5 Free';
            font-weight: 900;
        }
        
        .fab {
            font-family: 'Font Awesome 5 Brands';
        }
        
        .fa-shield-alt:before { content: "\f3ed"; }
        .fa-shopping-bag:before { content: "\f290"; }
        .fa-map-marker-alt:before { content: "\f3c5"; }
        .fa-phone:before { content: "\f095"; }
        .fa-envelope:before { content: "\f0e0"; }
        .fa-clock:before { content: "\f017"; }
        .fa-facebook-f:before { content: "\f39e"; }
        .fa-instagram:before { content: "\f16d"; }
        .fa-whatsapp:before { content: "\f232"; }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <!-- Logo will be created with CSS -->
                    <div class="logo-img">
                        <svg width="50" height="50" viewBox="0 0 50 50">
                            <circle cx="25" cy="25" r="20" fill="#3498db" opacity="0.8"/>
                            <path d="M25,10 L30,20 L40,22 L32,30 L34,40 L25,35 L16,40 L18,30 L10,22 L20,20 Z" fill="#2ecc71"/>
                            <circle cx="25" cy="25" r="8" fill="#2c3e50"/>
                        </svg>
                    </div>
                    <h1>Healix Care</h1>
                </div>
                <nav>
                    <ul>
                        <li><a class="nav-link active" data-page="home">Home</a></li>
                        <li><a class="nav-link" data-page="products">Products</a></li>
                        <li><a class="nav-link" data-page="about">About</a></li>
                        <li><a class="nav-link" data-page="contact">Contact</a></li>
                        <li class="cart-icon">
                            <a class="nav-link" data-page="cart">
                                <i class="fas fa-shopping-bag"></i>
                                <span class="cart-count">0</span>
                            </a>
                        </li>
                    </ul>
                </nav>
                <div class="language-selector">
                    <span class="nav-link" data-key="language">Language:</span>
                    <select id="language-selector">
                        <option value="en">English</option>
                        <option value="fr">Français</option>
                        <option value="de">Deutsch</option>
                        <option value="es">Español</option>
                        <option value="it">Italiano</option>
                        <option value="ar">العربية</option>
                    </select>
                </div>
            </div>
        </div>
    </header>

    <!-- Home Page -->
    <section id="home-page" class="page-section active">
        <!-- Hero Slider -->
        <div class="hero-slider">
            <div class="slide active" style="background-image: url('https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');">
                <div class="slide-content">
                    <h2 class="hero-title" data-key="heroTitle1">Premium Mobile Accessories</h2>
                    <p class="hero-subtitle" data-key="heroSubtitle1">Discover our high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional.</p>
                    <a class="btn shop-now-btn" data-key="shopNow" data-page="products">Shop Now</a>
                </div>
            </div>
            <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1556656793-08538906a9f8?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');">
                <div class="slide-content">
                    <h2 class="hero-title" data-key="heroTitle2">Protect Your Investment</h2>
                    <p class="hero-subtitle" data-key="heroSubtitle2">Quality cases and screen protectors designed to keep your phone looking new.</p>
                    <a class="btn shop-now-btn" data-key="shopNow" data-page="products">Shop Now</a>
                </div>
            </div>
            <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1605784407953-8fe7c72dab4d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');">
                <div class="slide-content">
                    <h2 class="hero-title" data-key="heroTitle3">Fast Charging Solutions</h2>
                    <p class="hero-subtitle" data-key="heroSubtitle3">High-speed cables and chargers to power your devices quickly and safely.</p>
                    <a class="btn shop-now-btn" data-key="shopNow" data-page="products">Shop Now</a>
                </div>
            </div>
            <div class="slider-nav">
                <div class="slider-dot active"></div>
                <div class="slider-dot"></div>
                <div class="slider-dot"></div>
            </div>
        </div>

        <!-- Featured Products -->
        <section class="products-section">
            <div class="container">
                <div class="section-title">
                    <h2 class="section-title-text" data-key="featuredProducts">Featured Products</h2>
                </div>
                <div class="products-grid" id="featured-products-container">
                    <!-- Featured products will be dynamically added here -->
                </div>
            </div>
        </section>
    </section>

    <!-- Products Page -->
    <section id="products-page" class="page-section">
        <div class="container">
            <div class="section-title">
                <h2 class="section-title-text" data-key="allProducts">All Products</h2>
            </div>
            <div class="products-grid" id="all-products-container">
                <!-- All products will be dynamically added here -->
            </div>
        </div>
    </section>

    <!-- About Page -->
    <section id="about-page" class="page-section">
        <div class="container">
            <div class="section-title">
                <h2 data-key="aboutUs">About Healix Care</h2>
            </div>
            <div class="about-content">
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="About Healix Care">
                </div>
                <div class="about-text">
                    <h3 data-key="ourStory">Our Story</h3>
                    <p data-key="aboutText1">Founded in 2020, Healix Care started with a simple mission: to provide high-quality, affordable mobile accessories that genuinely protect your devices. We noticed a gap in the market for products that combined excellent protection with stylish design.</p>
                    <p data-key="aboutText2">Today, we serve customers across Europe, the Middle East, and Pakistan, with our headquarters based in Faisalabad. Our products are tested rigorously to ensure they meet the highest standards of quality and durability.</p>
                    <h3 data-key="ourMission">Our Mission</h3>
                    <p data-key="aboutText3">To become the leading provider of mobile accessories by offering innovative products that enhance device protection while maintaining aesthetic appeal. We believe your mobile accessories should reflect your personal style while providing maximum protection.</p>
                    <h3 data-key="whyChooseUs">Why Choose Us?</h3>
                    <p data-key="aboutText4">- Premium quality materials</p>
                    <p data-key="aboutText5">- Rigorous testing procedures</p>
                    <p data-key="aboutText6">- International shipping</p>
                    <p data-key="aboutText7">- Multilingual customer support</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Page -->
    <section id="contact-page" class="page-section">
        <div class="container">
            <div class="section-title">
                <h2 data-key="contactUs">Contact Us</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3 data-key="getInTouch">Get In Touch</h3>
                    <div class="contact-details">
                        <p><i class="fas fa-map-marker-alt"></i> <span data-key="address">Faisalabad, Punjab, Pakistan</span></p>
                        <p><i class="fas fa-phone"></i> <span data-key="phone">+92 3481869972</span></p>
                        <p><i class="fas fa-phone"></i> <span data-key="phone2">+92 3279000242</span></p>
                        <p><i class="fas fa-envelope"></i> info@healixcare.com</p>
                        <p><i class="fas fa-clock"></i> <span data-key="businessHours">Mon - Fri: 9:00 AM - 6:00 PM</span></p>
                    </div>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="btn-whatsapp"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <h3 data-key="sendMessage">Send us a Message</h3>
                    <form id="contact-form">
                        <div class="form-group">
                            <label for="contact-name" data-key="yourName">Your Name</label>
                            <input type="text" id="contact-name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="contact-email" data-key="yourEmail">Your Email</label>
                            <input type="email" id="contact-email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="contact-subject" data-key="subject">Subject</label>
                            <input type="text" id="contact-subject" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="contact-message" data-key="message">Message</label>
                            <textarea id="contact-message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn" data-key="sendMessage">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Cart Page -->
    <section id="cart-page" class="page-section">
        <div class="container">
            <div class="section-title">
                <h2 data-key="shoppingCart">Shopping Cart</h2>
            </div>
            <div class="cart-container">
                <div class="cart-items" id="cart-items-container">
                    <!-- Cart items will be dynamically added here -->
                    <div class="empty-cart" id="empty-cart-message" style="text-align: center; padding: 40px;">
                        <i class="fas fa-shopping-bag" style="font-size: 48px; color: #ddd; margin-bottom: 20px;"></i>
                        <h3 data-key="emptyCart">Your cart is empty</h3>
                        <p data-key="addItems">Add some products to your cart</p>
                        <a class="btn" data-page="products" data-key="continueShopping" style="margin-top: 20px;">Continue Shopping</a>
                    </div>
                </div>
                <div class="cart-summary">
                    <h3 data-key="orderSummary">Order Summary</h3>
                    <div class="summary-row">
                        <span data-key="subtotal">Subtotal:</span>
                        <span id="cart-subtotal">$0.00</span>
                    </div>
                    <div class="summary-row">
                        <span data-key="shipping">Shipping:</span>
                        <span id="cart-shipping">$5.00</span>
                    </div>
                    <div class="summary-row">
                        <span data-key="tax">Tax:</span>
                        <span id="cart-tax">$0.00</span>
                    </div>
                    <div class="summary-row summary-total">
                        <span data-key="total">Total:</span>
                        <span id="cart-total">$0.00</span>
                    </div>
                    <button class="btn btn-success" id="checkout-btn" style="width: 100%; margin-top: 20px;" data-key="proceedToCheckout" data-page="checkout">Proceed to Checkout</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Checkout Page -->
    <section id="checkout-page" class="page-section">
        <div class="container">
            <div class="section-title">
                <h2 data-key="checkout">Checkout</h2>
            </div>
            <div class="checkout-container">
                <div class="checkout-form">
                    <h3 data-key="shippingDetails">Shipping Details</h3>
                    <form id="checkout-form">
                        <div class="form-group">
                            <label for="checkout-name" data-key="fullName">Full Name</label>
                            <input type="text" id="checkout-name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="checkout-email" data-key="emailAddress">Email Address</label>
                            <input type="email" id="checkout-email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="checkout-address" data-key="streetAddress">Street Address</label>
                            <input type="text" id="checkout-address" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="checkout-city" data-key="city">City</label>
                            <input type="text" id="checkout-city" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="checkout-zip" data-key="zipCode">ZIP Code</label>
                            <input type="text" id="checkout-zip" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="checkout-country" data-key="country">Country</label>
                            <select id="checkout-country" class="form-control" required>
                                <option value="pakistan">Pakistan</option>
                                <option value="uae">United Arab Emirates</option>
                                <option value="saudi">Saudi Arabia</option>
                                <option value="uk">United Kingdom</option>
                                <option value="usa">United States</option>
                                <option value="germany">Germany</option>
                                <option value="france">France</option>
                                <option value="spain">Spain</option>
                                <option value="italy">Italy</option>
                            </select>
                        </div>
                        
                        <h3 style="margin-top: 30px;" data-key="paymentInformation">Payment Information</h3>
                        <div class="form-group">
                            <label for="checkout-card" data-key="cardNumber">Card Number</label>
                            <input type="text" id="checkout-card" class="form-control" placeholder="1234 5678 9012 3456" required>
                        </div>
                        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
                            <div class="form-group">
                                <label for="checkout-expiry" data-key="expiryDate">Expiry Date</label>
                                <input type="text" id="checkout-expiry" class="form-control" placeholder="MM/YY" required>
                            </div>
                            <div class="form-group">
                                <label for="checkout-cvv" data-key="cvv">CVV</label>
                                <input type="text" id="checkout-cvv" class="form-control" placeholder="123" required>
                            </div>
                        </div>
                        
                        <button type="submit" class="btn btn-success" style="width: 100%; margin-top: 20px;" data-key="placeOrder">Place Order</button>
                    </form>
                </div>
                <div class="checkout-summary">
                    <h3 data-key="orderSummary">Order Summary</h3>
                    <div id="checkout-items-container">
                        <!-- Checkout items will be dynamically added here -->
                    </div>
                    <div class="summary-row">
                        <span data-key="subtotal">Subtotal:</span>
                        <span id="checkout-subtotal">$0.00</span>
                    </div>
                    <div class="summary-row">
                        <span data-key="shipping">Shipping:</span>
                        <span id="checkout-shipping">$5.00</span>
                    </div>
                    <div class="summary-row">
                        <span data-key="tax">Tax:</span>
                        <span id="checkout-tax">$0.00</span>
                    </div>
                    <div class="summary-row summary-total">
                        <span data-key="total">Total:</span>
                        <span id="checkout-total">$0.00</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- WhatsApp Help -->
    <div class="whatsapp-help">
        <a href="https://wa.me/923481869972?text=Hi%20Healix%20Care,%20I%20need%20help%20with%20my%20order" class="whatsapp-btn" target="_blank">
            <i class="fab fa-whatsapp"></i>
            <span data-key="whatsappHelp">Need Help?</span>
        </a>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3 data-key="aboutUs">About Healix Care</h3>
                    <p data-key="aboutText">We provide premium quality mobile accessories to protect and enhance your devices. Our products are designed with care and precision.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="https://wa.me/923481869972" class="btn-whatsapp" target="_blank"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3 data-key="quickLinks">Quick Links</h3>
                    <ul>
                        <li><a data-page="home" data-key="home">Home</a></li>
                        <li><a data-page="products" data-key="products">Products</a></li>
                        <li><a data-page="about" data-key="about">About Us</a></li>
                        <li><a data-page="contact" data-key="contact">Contact</a></li>
                        <li><a href="/p/admin.html" data-key="admin">Admin</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3 data-key="contactInfo">Contact Information</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> <span data-key="address">Faisalabad, Punjab, Pakistan</span></li>
                        <li><i class="fas fa-phone"></i> <span data-key="phone">+92 3481869972</span></li>
                        <li><i class="fas fa-phone"></i> <span data-key="phone2">+92 3279000242</span></li>
                        <li><i class="fas fa-envelope"></i> info@healixcare.com</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Healix Care. <span data-key="allRights">All rights reserved</span>.</p>
            </div>
        </div>
    </footer>

    <script>
        // Language translations
        var translations = {
            en: {
                home: "Home",
                products: "Products",
                about: "About",
                contact: "Contact",
                admin: "Admin",
                language: "Language",
                heroTitle1: "Premium Mobile Accessories",
                heroSubtitle1: "Discover our high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional.",
                heroTitle2: "Protect Your Investment",
                heroSubtitle2: "Quality cases and screen protectors designed to keep your phone looking new.",
                heroTitle3: "Fast Charging Solutions",
                heroSubtitle3: "High-speed cables and chargers to power your devices quickly and safely.",
                shopNow: "Shop Now",
                featuredProducts: "Featured Products",
                allProducts: "All Products",
                productName: "Product Name",
                productDescription: "Description",
                productPrice: "Price ($)",
                productImage: "Image URL",
                productCategory: "Category",
                screenProtector: "Screen Protector",
                phoneCase: "Phone Case",
                cable: "Cable",
                charger: "Charger",
                other: "Other",
                addProduct: "Add Product",
                cancel: "Cancel",
                existingProducts: "Existing Products",
                aboutUs: "About Healix Care",
                ourStory: "Our Story",
                ourMission: "Our Mission",
                whyChooseUs: "Why Choose Us?",
                aboutText: "We provide premium quality mobile accessories to protect and enhance your devices. Our products are designed with care and precision.",
                aboutText1: "Founded in 2020, Healix Care started with a simple mission: to provide high-quality, affordable mobile accessories that genuinely protect your devices. We noticed a gap in the market for products that combined excellent protection with stylish design.",
                aboutText2: "Today, we serve customers across Europe, the Middle East, and Pakistan, with our headquarters based in Faisalabad. Our products are tested rigorously to ensure they meet the highest standards of quality and durability.",
                aboutText3: "To become the leading provider of mobile accessories by offering innovative products that enhance device protection while maintaining aesthetic appeal. We believe your mobile accessories should reflect your personal style while providing maximum protection.",
                aboutText4: "- Premium quality materials",
                aboutText5: "- Rigorous testing procedures",
                aboutText6: "- International shipping",
                aboutText7: "- Multilingual customer support",
                contactUs: "Contact Us",
                getInTouch: "Get In Touch",
                sendMessage: "Send Message",
                yourName: "Your Name",
                yourEmail: "Your Email",
                subject: "Subject",
                message: "Message",
                businessHours: "Mon - Fri: 9:00 AM - 6:00 PM",
                quickLinks: "Quick Links",
                contactInfo: "Contact Information",
                address: "Faisalabad, Punjab, Pakistan",
                phone: "+92 3481869972",
                phone2: "+92 3279000242",
                allRights: "All rights reserved",
                privacy: "Privacy Policy",
                edit: "Edit",
                delete: "Delete",
                addToCart: "Add to Cart",
                shoppingCart: "Shopping Cart",
                orderSummary: "Order Summary",
                subtotal: "Subtotal",
                shipping: "Shipping",
                tax: "Tax",
                total: "Total",
                proceedToCheckout: "Proceed to Checkout",
                emptyCart: "Your cart is empty",
                addItems: "Add some products to your cart",
                continueShopping: "Continue Shopping",
                checkout: "Checkout",
                shippingDetails: "Shipping Details",
                fullName: "Full Name",
                emailAddress: "Email Address",
                streetAddress: "Street Address",
                city: "City",
                zipCode: "ZIP Code",
                country: "Country",
                paymentInformation: "Payment Information",
                cardNumber: "Card Number",
                expiryDate: "Expiry Date",
                cvv: "CVV",
                placeOrder: "Place Order",
                remove: "Remove",
                quantity: "Quantity",
                featuredProduct: "Featured Product",
                whatsappHelp: "Need Help?"
            },
            fr: {
                home: "Accueil",
                products: "Produits",
                about: "À propos",
                contact: "Contact",
                admin: "Administrateur",
                language: "Langue",
                heroTitle1: "Accessoires Mobiles Premium",
                heroSubtitle1: "Découvrez nos protecteurs d'écran, étuis, câbles OTG et plus encore de haute qualité pour garder vos appareils sûrs et fonctionnels.",
                heroTitle2: "Protégez Votre Investissement",
                heroSubtitle2: "Des étuis et protecteurs d'écran de qualité conçus pour garder votre téléphone comme neuf.",
                heroTitle3: "Solutions de Charge Rapide",
                heroSubtitle3: "Câbles et chargeurs haute vitesse pour alimenter vos appareils rapidement et en toute sécurité.",
                shopNow: "Acheter Maintenant",
                featuredProducts: "Produits Populaires",
                allProducts: "Tous les Produits",
                productName: "Nom du produit",
                productDescription: "Description",
                productPrice: "Prix (€)",
                productImage: "URL de l'image",
                productCategory: "Catégorie",
                screenProtector: "Protecteur d'écran",
                phoneCase: "Étui de téléphone",
                cable: "Câble",
                charger: "Chargeur",
                other: "Autre",
                addProduct: "Ajouter un produit",
                cancel: "Annuler",
                existingProducts: "Produits existants",
                aboutUs: "À propos de Healix Care",
                ourStory: "Notre Histoire",
                ourMission: "Notre Mission",
                whyChooseUs: "Pourquoi Nous Choisir?",
                aboutText: "Nous fournissons des accessoires mobiles de qualité premium pour protéger et améliorer vos appareils. Nos produits sont conçus avec soin et précision.",
                aboutText1: "Fondée en 2020, Healix Care a commencé avec une mission simple: fournir des accessoires mobiles de haute qualité et abordables qui protègent véritablement vos appareils. Nous avons remarqué un manque sur le marché pour des produits alliant excellente protection et design élégant.",
                aboutText2: "Aujourd'hui, nous servons des clients à travers l'Europe, le Moyen-Orient et le Pakistan, avec notre siège social basé à Faisalabad. Nos produits sont rigoureusement testés pour garantir qu'ils répondent aux normes de qualité et de durabilité les plus élevées.",
                aboutText3: "Devenir le principal fournisseur d'accessoires mobiles en offrant des produits innovants qui améliorent la protection des appareils tout en maintenant un attrait esthétique. Nous croyons que vos accessoires mobiles doivent refléter votre style personnel tout en offrant une protection maximale.",
                aboutText4: "- Matériaux de qualité premium",
                aboutText5: "- Procédures de test rigoureuses",
                aboutText6: "- Livraison internationale",
                aboutText7: "- Support client multilingue",
                contactUs: "Contactez-Nous",
                getInTouch: "Entrer en Contact",
                sendMessage: "Envoyer un Message",
                yourName: "Votre Nom",
                yourEmail: "Votre Email",
                subject: "Sujet",
                message: "Message",
                businessHours: "Lun - Ven: 9h00 - 18h00",
                quickLinks: "Liens rapides",
                contactInfo: "Informations de contact",
                address: "Faisalabad, Pendjab, Pakistan",
                phone: "+92 3481869972",
                phone2: "+92 3279000242",
                allRights: "Tous droits réservés",
                privacy: "Politique de confidentialité",
                edit: "Modifier",
                delete: "Supprimer",
                addToCart: "Ajouter au panier",
                shoppingCart: "Panier d'achat",
                orderSummary: "Résumé de la commande",
                subtotal: "Sous-total",
                shipping: "Livraison",
                tax: "Taxe",
                total: "Total",
                proceedToCheckout: "Passer à la caisse",
                emptyCart: "Votre panier est vide",
                addItems: "Ajoutez des produits à votre panier",
                continueShopping: "Continuer vos achats",
                checkout: "Caisse",
                shippingDetails: "Détails de livraison",
                fullName: "Nom complet",
                emailAddress: "Adresse e-mail",
                streetAddress: "Adresse",
                city: "Ville",
                zipCode: "Code postal",
                country: "Pays",
                paymentInformation: "Informations de paiement",
                cardNumber: "Numéro de carte",
                expiryDate: "Date d'expiration",
                cvv: "CVV",
                placeOrder: "Passer la commande",
                remove: "Supprimer",
                quantity: "Quantité",
                featuredProduct: "Produit en vedette",
                whatsappHelp: "Besoin d'aide?"
            },
            ar: {
                home: "الرئيسية",
                products: "المنتجات",
                about: "من نحن",
                contact: "اتصل بنا",
                admin: "المشرف",
                language: "اللغة",
                heroTitle1: "إكسسوارات الجوال الممتازة",
                heroSubtitle1: "اكتشف واقيات الشاشة عالية الجودة والأغطية والكابلات والمزيد للحفاظ على أجهزتك آمنة ووظيفية.",
                heroTitle2: "احمي استثمارك",
                heroSubtitle2: "أغطية وواقيات شاشة عالية الجودة مصممة للحفاظ على هاتفك يبدو جديدًا.",
                heroTitle3: "حلول الشحن السريع",
                heroSubtitle3: "كابلات وشواحن عالية السرعة لتشغيل أجهزتك بسرعة وأمان.",
                shopNow: "تسوق الآن",
                featuredProducts: "المنتجات المميزة",
                allProducts: "جميع المنتجات",
                productName: "اسم المنتج",
                productDescription: "الوصف",
                productPrice: "السعر ($)",
                productImage: "رابط الصورة",
                productCategory: "الفئة",
                screenProtector: "واقي الشاشة",
                phoneCase: "غطاء الهاتف",
                cable: "كابل",
                charger: "شاحن",
                other: "أخرى",
                addProduct: "إضافة منتج",
                cancel: "إلغاء",
                existingProducts: "المنتجات الحالية",
                aboutUs: "حول هيلكس كير",
                ourStory: "قصتنا",
                ourMission: "مهمتنا",
                whyChooseUs: "لماذا تختارنا؟",
                aboutText: "نوفر إكسسوارات جوال عالية الجودة لحماية وتحسين أجهزتك. تم تصميم منتجاتنا بعناية ودقة.",
                aboutText1: "تأسست هيلكس كير في عام 2020 بمهمة بسيطة: توفير إكسسوارات جوال عالية الجودة وبأسعار معقولة تحمي أجهزتك حقًا. لاحظنا فجوة في السوق لمنتجات تجمع بين الحماية الممتازة والتصميم الأنيق.",
                aboutText2: "اليوم، نخدم العملاء في جميع أنحاء أوروبا والشرق الأوسط وباكستان، مع مقرنا الرئيسي في فيصل آباد. يتم اختبار منتجاتنا بدقة لضمان تلبية أعلى معايير الجودة والمتانة.",
                aboutText3: "أن نصبح المزود الرائد للإكسسوارات الجوالة من خلال تقديم منتجات مبتكرة تعزز حماية الجهاز مع الحفاظ على الجاذبية الجمالية. نعتقد أن إكسسواراتك الجوالة يجب أن تعكس أسلوبك الشخصي مع توفير أقصى حماية.",
                aboutText4: "- مواد عالية الجودة",
                aboutText5: "- إجراءات اختبار صارمة",
                aboutText6: "- الشحن الدولي",
                aboutText7: "- دعم العملاء متعدد اللغات",
                contactUs: "اتصل بنا",
                getInTouch: "ابق على تواصل",
                sendMessage: "إرسال رسالة",
                yourName: "اسمك",
                yourEmail: "بريدك الإلكتروني",
                subject: "الموضوع",
                message: "الرسالة",
                businessHours: "الإثنين - الجمعة: 9:00 ص - 6:00 م",
                quickLinks: "روابط سريعة",
                contactInfo: "معلومات الاتصال",
                address: "فيصل آباد، البنجاب، باكستان",
                phone: "+92 3481869972",
                phone2: "+92 3279000242",
                allRights: "جميع الحقوق محفوظة",
                privacy: "سياسة الخصوصية",
                edit: "تعديل",
                delete: "حذف",
                addToCart: "أضف إلى السلة",
                shoppingCart: "سلة التسوق",
                orderSummary: "ملخص الطلب",
                subtotal: "المجموع الفرعي",
                shipping: "الشحن",
                tax: "الضريبة",
                total: "المجموع",
                proceedToCheckout: "تابع للدفع",
                emptyCart: "سلة التسوق فارغة",
                addItems: "أضف بعض المنتجات إلى سلة التسوق",
                continueShopping: "مواصلة التسوق",
                checkout: "الدفع",
                shippingDetails: "تفاصيل الشحن",
                fullName: "الاسم الكامل",
                emailAddress: "عنوان البريد الإلكتروني",
                streetAddress: "عنوان الشارع",
                city: "المدينة",
                zipCode: "الرمز البريدي",
                country: "البلد",
                paymentInformation: "معلومات الدفع",
                cardNumber: "رقم البطاقة",
                expiryDate: "تاريخ الانتهاء",
                cvv: "CVV",
                placeOrder: "تقديم الطلب",
                remove: "إزالة",
                quantity: "الكمية",
                featuredProduct: "منتج مميز",
                whatsappHelp: "تحتاج مساعدة؟"
            }
        };

        // Sample products data (15 products)
        var products = [
            {
                id: 1,
                name: "Tempered Glass Screen Protector",
                description: "9H hardness tempered glass with oleophobic coating to resist fingerprints.",
                price: 12.99,
                image: "https://images.unsplash.com/photo-1601593346740-925612772716?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80",
                category: "screen-protector",
                featured: true
            },
            {
                id: 2,
                name: "Silicone Phone Case",
                description: "Shock-absorbent silicone case with raised edges for screen protection.",
                price: 18.99,
                image: "https://images.unsplash.com/photo-1556656793-08538906a9f8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "phone-case",
                featured: true
            },
            {
                id: 3,
                name: "USB-C to USB Adapter",
                description: "High-speed OTG adapter for connecting USB devices to your smartphone.",
                price: 8.99,
                image: "https://images.unsplash.com/photo-1583394838336-acd977736f90?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=684&q=80",
                category: "cable",
                featured: false
            },
            {
                id: 4,
                name: "Fast Charging Cable",
                description: "Durable braided USB-C cable with fast charging capability.",
                price: 14.99,
                image: "https://images.unsplash.com/photo-1605784407953-8fe7c72dab4d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "cable",
                featured: true
            },
            {
                id: 5,
                name: "Wireless Charging Pad",
                description: "10W fast wireless charging pad with LED indicator.",
                price: 24.99,
                image: "https://images.unsplash.com/photo-1572569511254-d8f925fe2cbb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1169&q=80",
                category: "charger",
                featured: false
            },
            {
                id: 6,
                name: "Car Phone Holder",
                description: "Adjustable car vent phone holder with strong grip.",
                price: 15.99,
                image: "https://images.unsplash.com/photo-1586953208448-b95a79798f07?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 7,
                name: "Bluetooth Earbuds",
                description: "Wireless earbuds with noise cancellation and 20hr battery.",
                price: 49.99,
                image: "https://images.unsplash.com/photo-1590658165737-15a047b8b5e9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1012&q=80",
                category: "other",
                featured: true
            },
            {
                id: 8,
                name: "Phone Stand",
                description: "Adjustable aluminum phone stand for desktop use.",
                price: 12.99,
                image: "https://images.unsplash.com/photo-1545454675-3531b543be5d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 9,
                name: "Power Bank 10000mAh",
                description: "Compact power bank with fast charging support.",
                price: 29.99,
                image: "https://images.unsplash.com/photo-1609592810793-abeb6c64b5c6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1169&q=80",
                category: "charger",
                featured: true
            },
            {
                id: 10,
                name: "Phone Cleaning Kit",
                description: "Complete kit for cleaning phone screens and ports.",
                price: 9.99,
                image: "https://images.unsplash.com/photo-1616343932295-68d2596765f8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 11,
                name: "Magnetic Car Mount",
                description: "Strong magnetic car mount for easy phone placement.",
                price: 19.99,
                image: "https://images.unsplash.com/photo-1565842777185-6aea8d30f23c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 12,
                name: "Waterproof Phone Pouch",
                description: "Transparent waterproof pouch for beach and pool use.",
                price: 14.99,
                image: "https://images.unsplash.com/photo-1558618666-fcd25856cd63?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "phone-case",
                featured: false
            },
            {
                id: 13,
                name: "Phone Grip Ring",
                description: "Adhesive phone grip for secure one-handed use.",
                price: 7.99,
                image: "https://images.unsplash.com/photo-1616343932295-68d2596765f8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 14,
                name: "Multi-Port USB Hub",
                description: "4-port USB hub for expanding connectivity.",
                price: 22.99,
                image: "https://images.unsplash.com/photo-1598300042247-d088f8ab3a91?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1064&q=80",
                category: "cable",
                featured: false
            },
            {
                id: 15,
                name: "Phone Lens Kit",
                description: "Clip-on lens kit for wide-angle and macro photography.",
                price: 24.99,
                image: "https://images.unsplash.com/photo-1555774698-0b77e0d5fac6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: true
            }
        ];

        // Shopping cart
        var cart = [];

        // Current language
        var currentLang = 'en';

        // DOM elements
        var languageSelector = document.getElementById('language-selector');
        var pageSections = document.querySelectorAll('.page-section');
        var navLinks = document.querySelectorAll('.nav-link[data-page]');
        var featuredProductsContainer = document.getElementById('featured-products-container');
        var allProductsContainer = document.getElementById('all-products-container');
        var cartCount = document.querySelector('.cart-count');
        var cartItemsContainer = document.getElementById('cart-items-container');
        var emptyCartMessage = document.getElementById('empty-cart-message');
        var checkoutBtn = document.getElementById('checkout-btn');
        var checkoutForm = document.getElementById('checkout-form');
        var contactForm = document.getElementById('contact-form');
        var slides = document.querySelectorAll('.slide');
        var dots = document.querySelectorAll('.slider-dot');

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            // Load products
            renderFeaturedProducts();
            renderAllProducts();
            updateCartUI();
            
            // Set up language change listener
            languageSelector.addEventListener('change', function() {
                currentLang = this.value;
                updateLanguage();
                
                // Update RTL for Arabic
                if (currentLang === 'ar') {
                    document.body.classList.add('rtl');
                } else {
                    document.body.classList.remove('rtl');
                }
            });
            
            // Set up navigation
            navLinks.forEach(function(link) {
                link.addEventListener('click', function() {
                    var page = this.getAttribute('data-page');
                    navigateToPage(page);
                });
            });
            
            // Set up contact form
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Thank you for your message! We will get back to you soon.');
                contactForm.reset();
            });
            
            // Set up checkout form
            checkoutForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Thank you for your order! Your order has been placed successfully.');
                // Clear cart
                cart = [];
                updateCartUI();
                navigateToPage('home');
            });
            
            // Initialize slider
            initSlider();
        });

        // Initialize hero slider
        function initSlider() {
            var currentSlide = 0;
            
            function showSlide(n) {
                slides.forEach(function(slide) {
                    slide.classList.remove('active');
                });
                dots.forEach(function(dot) {
                    dot.classList.remove('active');
                });
                
                currentSlide = (n + slides.length) % slides.length;
                
                slides[currentSlide].classList.add('active');
                dots[currentSlide].classList.add('active');
            }
            
            // Auto slide
            setInterval(function() {
                showSlide(currentSlide + 1);
            }, 5000);
            
            // Dot click events
            dots.forEach(function(dot, index) {
                dot.addEventListener('click', function() {
                    showSlide(index);
                });
            });
        }

        // Navigate to a specific page
        function navigateToPage(page) {
            // Hide all pages
            pageSections.forEach(function(section) {
                section.classList.remove('active');
            });
            
            // Show the selected page
            document.getElementById(page + '-page').classList.add('active');
            
            // Update active nav link
            navLinks.forEach(function(link) {
                link.classList.remove('active');
                if (link.getAttribute('data-page') === page) {
                    link.classList.add('active');
                }
            });
            
            // Scroll to top
            window.scrollTo(0, 0);
            
            // Update cart and checkout pages if needed
            if (page === 'cart') {
                renderCartItems();
            } else if (page === 'checkout') {
                renderCheckoutItems();
            }
        }

        // Update language across the page
        function updateLanguage() {
            document.querySelectorAll('[data-key]').forEach(function(element) {
                var key = element.getAttribute('data-key');
                if (translations[currentLang][key]) {
                    if (element.tagName === 'INPUT' && element.type !== 'submit' && element.type !== 'button' && element.type !== 'checkbox') {
                        element.placeholder = translations[currentLang][key];
                    } else if (element.tagName === 'OPTION') {
                        element.textContent = translations[currentLang][key];
                    } else {
                        element.textContent = translations[currentLang][key];
                    }
                }
            });
        }

        // Render featured products on the home page
        function renderFeaturedProducts() {
            featuredProductsContainer.innerHTML = '';
            
            var featuredProducts = products.filter(function(product) {
                return product.featured;
            });
            
            featuredProducts.forEach(function(product) {
                var productCard = createProductCard(product);
                featuredProductsContainer.appendChild(productCard);
            });
            
            // Update language for newly added elements
            updateLanguage();
        }

        // Render all products on the products page
        function renderAllProducts() {
            allProductsContainer.innerHTML = '';
            
            products.forEach(function(product) {
                var productCard = createProductCard(product);
                allProductsContainer.appendChild(productCard);
            });
            
            // Update language for newly added elements
            updateLanguage();
        }

        // Create a product card element
        function createProductCard(product) {
            var productCard = document.createElement('div');
            productCard.className = 'product-card';
            productCard.innerHTML = 
                '<div class="product-image">' +
                    '<img src="' + product.image + '" alt="' + product.name + '">' +
                '</div>' +
                '<div class="product-info">' +
                    '<h3>' + product.name + '</h3>' +
                    '<p>' + product.description + '</p>' +
                    '<div class="product-price">' +
                        '<span class="price">$' + product.price.toFixed(2) + '</span>' +
                        '<button class="btn add-to-cart-btn" data-id="' + product.id + '" data-key="addToCart">Add to Cart</button>' +
                    '</div>' +
                '</div>';
            
            // Add event listener to Add to Cart button
            var addToCartBtn = productCard.querySelector('.add-to-cart-btn');
            addToCartBtn.addEventListener('click', function() {
                addToCart(product.id);
            });
            
            return productCard;
        }

        // Add product to cart
        function addToCart(productId) {
            var product = products.find(function(p) {
                return p.id === productId;
            });
            if (product) {
                var existingItem = cart.find(function(item) {
                    return item.id === productId;
                });
                
                if (existingItem) {
                    existingItem.quantity += 1;
                } else {
                    cart.push({
                        id: product.id,
                        name: product.name,
                        description: product.description,
                        price: product.price,
                        image: product.image,
                        quantity: 1
                    });
                }
                
                updateCartUI();
                alert('Product added to cart!');
            }
        }

        // Update cart UI
        function updateCartUI() {
            // Update cart count
            var totalItems = cart.reduce(function(total, item) {
                return total + item.quantity;
            }, 0);
            cartCount.textContent = totalItems;
            
            // Update cart totals
            var subtotal = cart.reduce(function(total, item) {
                return total + (item.price * item.quantity);
            }, 0);
            var shipping = 5.00;
            var tax = subtotal * 0.1; // 10% tax
            var total = subtotal + shipping + tax;
            
            document.getElementById('cart-subtotal').textContent = '$' + subtotal.toFixed(2);
            document.getElementById('cart-shipping').textContent = '$' + shipping.toFixed(2);
            document.getElementById('cart-tax').textContent = '$' + tax.toFixed(2);
            document.getElementById('cart-total').textContent = '$' + total.toFixed(2);
            
            // Update checkout totals
            document.getElementById('checkout-subtotal').textContent = '$' + subtotal.toFixed(2);
            document.getElementById('checkout-shipping').textContent = '$' + shipping.toFixed(2);
            document.getElementById('checkout-tax').textContent = '$' + tax.toFixed(2);
            document.getElementById('checkout-total').textContent = '$' + total.toFixed(2);
            
            // Enable/disable checkout button
            checkoutBtn.disabled = cart.length === 0;
        }

        // Render cart items
        function renderCartItems() {
            cartItemsContainer.innerHTML = '';
            
            if (cart.length === 0) {
                cartItemsContainer.appendChild(emptyCartMessage.cloneNode(true));
                return;
            }
            
            cart.forEach(function(item) {
                var cartItem = document.createElement('div');
                cartItem.className = 'cart-item';
                cartItem.innerHTML = 
                    '<div class="cart-item-image">' +
                        '<img src="' + item.image + '" alt="' + item.name + '">' +
                    '</div>' +
                    '<div class="cart-item-details">' +
                        '<h3>' + item.name + '</h3>' +
                        '<p>' + item.description + '</p>' +
                        '<div class="cart-item-controls">' +
                            '<div class="quantity-controls">' +
                                '<button class="quantity-btn decrease-btn" data-id="' + item.id + '">-</button>' +
                                '<span class="quantity">' + item.quantity + '</span>' +
                                '<button class="quantity-btn increase-btn" data-id="' + item.id + '">+</button>' +
                            '</div>' +
                            '<span class="price">$' + (item.price * item.quantity).toFixed(2) + '</span>' +
                            '<button class="btn btn-danger remove-btn" data-id="' + item.id + '" data-key="remove">Remove</button>' +
                        '</div>' +
                    '</div>';
                cartItemsContainer.appendChild(cartItem);
            });
            
            // Add event listeners to quantity buttons
            document.querySelectorAll('.increase-btn').forEach(function(button) {
                button.addEventListener('click', function() {
                    var productId = parseInt(this.getAttribute('data-id'));
                    var item = cart.find(function(item) {
                        return item.id === productId;
                    });
                    if (item) {
                        item.quantity += 1;
                        updateCartUI();
                        renderCartItems();
                    }
                });
            });
            
            document.querySelectorAll('.decrease-btn').forEach(function(button) {
                button.addEventListener('click', function() {
                    var productId = parseInt(this.getAttribute('data-id'));
                    var item = cart.find(function(item) {
                        return item.id === productId;
                    });
                    if (item && item.quantity > 1) {
                        item.quantity -= 1;
                        updateCartUI();
                        renderCartItems();
                    }
                });
            });
            
            document.querySelectorAll('.remove-btn').forEach(function(button) {
                button.addEventListener('click', function() {
                    var productId = parseInt(this.getAttribute('data-id'));
                    cart = cart.filter(function(item) {
                        return item.id !== productId;
                    });
                    updateCartUI();
                    renderCartItems();
                });
            });
            
            // Update language
            updateLanguage();
        }

        // Render checkout items
        function renderCheckoutItems() {
            var checkoutItemsContainer = document.getElementById('checkout-items-container');
            checkoutItemsContainer.innerHTML = '';
            
            cart.forEach(function(item) {
                var checkoutItem = document.createElement('div');
                checkoutItem.className = 'checkout-item';
                checkoutItem.innerHTML = 
                    '<div class="checkout-item-image">' +
                        '<img src="' + item.image + '" alt="' + item.name + '">' +
                    '</div>' +
                    '<div class="checkout-item-details">' +
                        '<h4>' + item.name + '</h4>' +
                        '<p data-key="quantity">Quantity: ' + item.quantity + '</p>' +
                        '<p>$' + (item.price * item.quantity).toFixed(2) + '</p>' +
                    '</div>';
                checkoutItemsContainer.appendChild(checkoutItem);
            });
            
            // Update language
            updateLanguage();
        }
    </script>
</body>
</html>
