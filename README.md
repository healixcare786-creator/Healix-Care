<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Healix Care - Premium Mobile Accessories</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
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
        
        .logo h1 {
            font-size: 24px;
            margin-left: 10px;
        }
        
        .logo i {
            font-size: 28px;
            color: var(--secondary);
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
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(44, 62, 80, 0.9)), url('https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1160&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 80px 0;
            text-align: center;
        }
        
        .hero h2 {
            font-size: 42px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 18px;
            max-width: 700px;
            margin: 0 auto 30px;
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
        
        /* Admin Panel */
        .admin-panel {
            background: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            margin: 40px 0;
        }
        
        .admin-panel h2 {
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
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
        
        /* Admin Login */
        .admin-login {
            max-width: 400px;
            margin: 50px auto;
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .admin-login h2 {
            text-align: center;
            margin-bottom: 20px;
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
            
            .hero h2 {
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
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-shield-alt"></i>
                    <h1>Healix Care</h1>
                </div>
                <nav>
                    <ul>
                        <li><a class="nav-link active" data-page="home">Home</a></li>
                        <li><a class="nav-link" data-page="products">Products</a></li>
                        <li><a class="nav-link" data-page="about">About</a></li>
                        <li><a class="nav-link" data-page="contact">Contact</a></li>
                        <li><a class="nav-link" data-page="admin">Admin</a></li>
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
        <!-- Hero Section -->
        <section class="hero">
            <div class="container">
                <h2 class="hero-title" data-key="heroTitle">Premium Mobile Accessories</h2>
                <p class="hero-subtitle" data-key="heroSubtitle">Discover our high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional.</p>
                <a class="btn shop-now-btn" data-key="shopNow" data-page="products">Shop Now</a>
            </div>
        </section>

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
                        <p><i class="fas fa-phone"></i> <span data-key="phone">+92 300 123 4567</span></p>
                        <p><i class="fas fa-envelope"></i> info@healixcare.com</p>
                        <p><i class="fas fa-clock"></i> <span data-key="businessHours">Mon - Fri: 9:00 AM - 6:00 PM</span></p>
                    </div>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
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

    <!-- Admin Login Page -->
    <section id="admin-login-page" class="page-section">
        <div class="container">
            <div class="admin-login">
                <h2 data-key="adminLogin">Admin Login</h2>
                <form id="admin-login-form">
                    <div class="form-group">
                        <label for="admin-username" data-key="username">Username</label>
                        <input type="text" id="admin-username" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="admin-password" data-key="password">Password</label>
                        <input type="password" id="admin-password" class="form-control" required>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;" data-key="login">Login</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Admin Page -->
    <section id="admin-page" class="page-section">
        <div class="container">
            <div class="admin-panel">
                <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                    <h2 data-key="adminPanel">Admin Panel - Manage Products</h2>
                    <button class="btn btn-danger" id="admin-logout" data-key="logout">Logout</button>
                </div>
                <form id="product-form">
                    <div class="form-group">
                        <label for="product-name" data-key="productName">Product Name</label>
                        <input type="text" id="product-name" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="product-description" data-key="productDescription">Description</label>
                        <textarea id="product-description" class="form-control" required></textarea>
                    </div>
                    <div class="form-group">
                        <label for="product-price" data-key="productPrice">Price ($)</label>
                        <input type="number" id="product-price" class="form-control" step="0.01" required>
                    </div>
                    <div class="form-group">
                        <label for="product-image" data-key="productImage">Image URL</label>
                        <input type="url" id="product-image" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="product-category" data-key="productCategory">Category</label>
                        <select id="product-category" class="form-control" required>
                            <option value="screen-protector" data-key="screenProtector">Screen Protector</option>
                            <option value="phone-case" data-key="phoneCase">Phone Case</option>
                            <option value="cable" data-key="cable">Cable</option>
                            <option value="charger" data-key="charger">Charger</option>
                            <option value="other" data-key="other">Other</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>
                            <input type="checkbox" id="product-featured">
                            <span data-key="featuredProduct">Featured Product</span>
                        </label>
                    </div>
                    <button type="submit" class="btn btn-success" data-key="addProduct">Add Product</button>
                    <button type="button" class="btn btn-danger" id="cancel-edit" style="display: none;" data-key="cancel">Cancel</button>
                </form>
                
                <div class="existing-products" style="margin-top: 40px;">
                    <h3 data-key="existingProducts">Existing Products</h3>
                    <div id="admin-products-list">
                        <!-- Admin product list will be populated here -->
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3 data-key="aboutUs">About Healix Care</h3>
                    <p data-key="aboutText">We provide premium quality mobile accessories to protect and enhance your devices. Our products are designed with care and precision.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3 data-key="quickLinks">Quick Links</h3>
                    <ul>
                        <li><a data-page="home" data-key="home">Home</a></li>
                        <li><a data-page="products" data-key="products">Products</a></li>
                        <li><a data-page="about" data-key="about">About Us</a></li>
                        <li><a data-page="contact" data-key="contact">Contact</a></li>
                        <li><a data-key="privacy">Privacy Policy</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3 data-key="contactInfo">Contact Information</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> <span data-key="address">Faisalabad, Punjab, Pakistan</span></li>
                        <li><i class="fas fa-phone"></i> <span data-key="phone">+92 300 123 4567</span></li>
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
        const translations = {
            en: {
                home: "Home",
                products: "Products",
                about: "About",
                contact: "Contact",
                admin: "Admin",
                language: "Language",
                heroTitle: "Premium Mobile Accessories",
                heroSubtitle: "Discover our high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional.",
                shopNow: "Shop Now",
                featuredProducts: "Featured Products",
                allProducts: "All Products",
                adminPanel: "Admin Panel - Manage Products",
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
                phone: "+92 300 123 4567",
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
                adminLogin: "Admin Login",
                username: "Username",
                password: "Password",
                login: "Login",
                logout: "Logout",
                remove: "Remove",
                quantity: "Quantity",
                featuredProduct: "Featured Product"
            },
            fr: {
                home: "Accueil",
                products: "Produits",
                about: "À propos",
                contact: "Contact",
                admin: "Administrateur",
                language: "Langue",
                heroTitle: "Accessoires Mobiles Premium",
                heroSubtitle: "Découvrez nos protecteurs d'écran, étuis, câbles OTG et plus encore de haute qualité pour garder vos appareils sûrs et fonctionnels.",
                shopNow: "Acheter Maintenant",
                featuredProducts: "Produits Populaires",
                allProducts: "Tous les Produits",
                adminPanel: "Panneau d'administration - Gérer les produits",
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
                phone: "+92 300 123 4567",
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
                adminLogin: "Connexion administrateur",
                username: "Nom d'utilisateur",
                password: "Mot de passe",
                login: "Se connecter",
                logout: "Se déconnecter",
                remove: "Supprimer",
                quantity: "Quantité",
                featuredProduct: "Produit en vedette"
            },
            ar: {
                home: "الرئيسية",
                products: "المنتجات",
                about: "من نحن",
                contact: "اتصل بنا",
                admin: "المشرف",
                language: "اللغة",
                heroTitle: "إكسسوارات الجوال الممتازة",
                heroSubtitle: "اكتشف واقيات الشاشة عالية الجودة والأغطية والكابلات والمزيد للحفاظ على أجهزتك آمنة ووظيفية.",
                shopNow: "تسوق الآن",
                featuredProducts: "المنتجات المميزة",
                allProducts: "جميع المنتجات",
                adminPanel: "لوحة التحكم - إدارة المنتجات",
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
                phone: "+92 300 123 4567",
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
                adminLogin: "تسجيل دخول المسؤول",
                username: "اسم المستخدم",
                password: "كلمة المرور",
                login: "تسجيل الدخول",
                logout: "تسجيل الخروج",
                remove: "إزالة",
                quantity: "الكمية",
                featuredProduct: "منتج مميز"
            }
        };

        // Sample products data
        let products = [
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
            }
        ];

        // Shopping cart
        let cart = [];

        // Admin credentials
        const adminCredentials = {
            username: "admin",
            password: "healix2023"
        };

        // Current language
        let currentLang = 'en';
        let editingProductId = null;
        let isAdminLoggedIn = false;

        // DOM elements
        const languageSelector = document.getElementById('language-selector');
        const pageSections = document.querySelectorAll('.page-section');
        const navLinks = document.querySelectorAll('.nav-link[data-page]');
        const featuredProductsContainer = document.getElementById('featured-products-container');
        const allProductsContainer = document.getElementById('all-products-container');
        const adminProductsList = document.getElementById('admin-products-list');
        const productForm = document.getElementById('product-form');
        const cancelEditBtn = document.getElementById('cancel-edit');
        const contactForm = document.getElementById('contact-form');
        const cartCount = document.querySelector('.cart-count');
        const cartItemsContainer = document.getElementById('cart-items-container');
        const emptyCartMessage = document.getElementById('empty-cart-message');
        const checkoutBtn = document.getElementById('checkout-btn');
        const checkoutForm = document.getElementById('checkout-form');
        const adminLoginForm = document.getElementById('admin-login-form');
        const adminLogoutBtn = document.getElementById('admin-logout');

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            // Load products
            renderFeaturedProducts();
            renderAllProducts();
            renderAdminProducts();
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
            navLinks.forEach(link => {
                link.addEventListener('click', function() {
                    const page = this.getAttribute('data-page');
                    
                    // Special handling for admin page
                    if (page === 'admin' && !isAdminLoggedIn) {
                        navigateToPage('admin-login');
                    } else {
                        navigateToPage(page);
                    }
                });
            });
            
            // Set up product form submission
            productForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                const productData = {
                    name: document.getElementById('product-name').value,
                    description: document.getElementById('product-description').value,
                    price: parseFloat(document.getElementById('product-price').value),
                    image: document.getElementById('product-image').value,
                    category: document.getElementById('product-category').value,
                    featured: document.getElementById('product-featured').checked
                };
                
                if (editingProductId) {
                    // Update existing product
                    updateProduct(editingProductId, productData);
                } else {
                    // Add new product
                    addProduct(productData);
                }
                
                // Reset form
                productForm.reset();
                cancelEditBtn.style.display = 'none';
                editingProductId = null;
            });
            
            // Set up cancel edit button
            cancelEditBtn.addEventListener('click', function() {
                productForm.reset();
                this.style.display = 'none';
                editingProductId = null;
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
            
            // Set up admin login form
            adminLoginForm.addEventListener('submit', function(e) {
                e.preventDefault();
                const username = document.getElementById('admin-username').value;
                const password = document.getElementById('admin-password').value;
                
                if (username === adminCredentials.username && password === adminCredentials.password) {
                    isAdminLoggedIn = true;
                    navigateToPage('admin');
                } else {
                    alert('Invalid username or password');
                }
            });
            
            // Set up admin logout
            adminLogoutBtn.addEventListener('click', function() {
                isAdminLoggedIn = false;
                navigateToPage('home');
            });
        });

        // Navigate to a specific page
        function navigateToPage(page) {
            // Hide all pages
            pageSections.forEach(section => {
                section.classList.remove('active');
            });
            
            // Show the selected page
            document.getElementById(`${page}-page`).classList.add('active');
            
            // Update active nav link
            navLinks.forEach(link => {
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
            document.querySelectorAll('[data-key]').forEach(element => {
                const key = element.getAttribute('data-key');
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
            
            const featuredProducts = products.filter(product => product.featured);
            
            featuredProducts.forEach(product => {
                const productCard = createProductCard(product);
                featuredProductsContainer.appendChild(productCard);
            });
            
            // Update language for newly added elements
            updateLanguage();
        }

        // Render all products on the products page
        function renderAllProducts() {
            allProductsContainer.innerHTML = '';
            
            products.forEach(product => {
                const productCard = createProductCard(product);
                allProductsContainer.appendChild(productCard);
            });
            
            // Update language for newly added elements
            updateLanguage();
        }

        // Create a product card element
        function createProductCard(product) {
            const productCard = document.createElement('div');
            productCard.className = 'product-card';
            productCard.innerHTML = `
                <div class="product-image">
                    <img src="${product.image}" alt="${product.name}">
                </div>
                <div class="product-info">
                    <h3>${product.name}</h3>
                    <p>${product.description}</p>
                    <div class="product-price">
                        <span class="price">$${product.price.toFixed(2)}</span>
                        <button class="btn add-to-cart-btn" data-id="${product.id}" data-key="addToCart">Add to Cart</button>
                    </div>
                </div>
            `;
            
            // Add event listener to Add to Cart button
            const addToCartBtn = productCard.querySelector('.add-to-cart-btn');
            addToCartBtn.addEventListener('click', function() {
                addToCart(product.id);
            });
            
            return productCard;
        }

        // Add product to cart
        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            if (product) {
                const existingItem = cart.find(item => item.id === productId);
                
                if (existingItem) {
                    existingItem.quantity += 1;
                } else {
                    cart.push({
                        ...product,
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
            const totalItems = cart.reduce((total, item) => total + item.quantity, 0);
            cartCount.textContent = totalItems;
            
            // Update cart totals
            const subtotal = cart.reduce((total, item) => total + (item.price * item.quantity), 0);
            const shipping = 5.00;
            const tax = subtotal * 0.1; // 10% tax
            const total = subtotal + shipping + tax;
            
            document.getElementById('cart-subtotal').textContent = `$${subtotal.toFixed(2)}`;
            document.getElementById('cart-shipping').textContent = `$${shipping.toFixed(2)}`;
            document.getElementById('cart-tax').textContent = `$${tax.toFixed(2)}`;
            document.getElementById('cart-total').textContent = `$${total.toFixed(2)}`;
            
            // Update checkout totals
            document.getElementById('checkout-subtotal').textContent = `$${subtotal.toFixed(2)}`;
            document.getElementById('checkout-shipping').textContent = `$${shipping.toFixed(2)}`;
            document.getElementById('checkout-tax').textContent = `$${tax.toFixed(2)}`;
            document.getElementById('checkout-total').textContent = `$${total.toFixed(2)}`;
            
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
            
            cart.forEach(item => {
                const cartItem = document.createElement('div');
                cartItem.className = 'cart-item';
                cartItem.innerHTML = `
                    <div class="cart-item-image">
                        <img src="${item.image}" alt="${item.name}">
                    </div>
                    <div class="cart-item-details">
                        <h3>${item.name}</h3>
                        <p>${item.description}</p>
                        <div class="cart-item-controls">
                            <div class="quantity-controls">
                                <button class="quantity-btn decrease-btn" data-id="${item.id}">-</button>
                                <span class="quantity">${item.quantity}</span>
                                <button class="quantity-btn increase-btn" data-id="${item.id}">+</button>
                            </div>
                            <span class="price">$${(item.price * item.quantity).toFixed(2)}</span>
                            <button class="btn btn-danger remove-btn" data-id="${item.id}" data-key="remove">Remove</button>
                        </div>
                    </div>
                `;
                cartItemsContainer.appendChild(cartItem);
            });
            
            // Add event listeners to quantity buttons
            document.querySelectorAll('.increase-btn').forEach(button => {
                button.addEventListener('click', function() {
                    const productId = parseInt(this.getAttribute('data-id'));
                    const item = cart.find(item => item.id === productId);
                    if (item) {
                        item.quantity += 1;
                        updateCartUI();
                        renderCartItems();
                    }
                });
            });
            
            document.querySelectorAll('.decrease-btn').forEach(button => {
                button.addEventListener('click', function() {
                    const productId = parseInt(this.getAttribute('data-id'));
                    const item = cart.find(item => item.id === productId);
                    if (item && item.quantity > 1) {
                        item.quantity -= 1;
                        updateCartUI();
                        renderCartItems();
                    }
                });
            });
            
            document.querySelectorAll('.remove-btn').forEach(button => {
                button.addEventListener('click', function() {
                    const productId = parseInt(this.getAttribute('data-id'));
                    cart = cart.filter(item => item.id !== productId);
                    updateCartUI();
                    renderCartItems();
                });
            });
            
            // Update language
            updateLanguage();
        }

        // Render checkout items
        function renderCheckoutItems() {
            const checkoutItemsContainer = document.getElementById('checkout-items-container');
            checkoutItemsContainer.innerHTML = '';
            
            cart.forEach(item => {
                const checkoutItem = document.createElement('div');
                checkoutItem.className = 'checkout-item';
                checkoutItem.innerHTML = `
                    <div class="checkout-item-image">
                        <img src="${item.image}" alt="${item.name}">
                    </div>
                    <div class="checkout-item-details">
                        <h4>${item.name}</h4>
                        <p data-key="quantity">Quantity: ${item.quantity}</p>
                        <p>$${(item.price * item.quantity).toFixed(2)}</p>
                    </div>
                `;
                checkoutItemsContainer.appendChild(checkoutItem);
            });
            
            // Update language
            updateLanguage();
        }

        // Render products in admin panel
        function renderAdminProducts() {
            adminProductsList.innerHTML = '';
            
            products.forEach(product => {
                const productItem = document.createElement('div');
                productItem.className = 'admin-product-item';
                productItem.style.cssText = `
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                    padding: 15px;
                    border: 1px solid #eee;
                    border-radius: 4px;
                    margin-bottom: 10px;
                `;
                productItem.innerHTML = `
                    <div>
                        <h4>${product.name}</h4>
                        <p>$${product.price.toFixed(2)}</p>
                    </div>
                    <div>
                        <button class="btn edit-product" data-id="${product.id}">Edit</button>
                        <button class="btn btn-danger delete-product" data-id="${product.id}">Delete</button>
                    </div>
                `;
                adminProductsList.appendChild(productItem);
            });
            
            // Add event listeners to edit and delete buttons
            document.querySelectorAll('.edit-product').forEach(button => {
                button.addEventListener('click', function() {
                    const productId = parseInt(this.getAttribute('data-id'));
                    editProduct(productId);
                });
            });
            
            document.querySelectorAll('.delete-product').forEach(button => {
                button.addEventListener('click', function() {
                    const productId = parseInt(this.getAttribute('data-id'));
                    deleteProduct(productId);
                });
            });
            
            // Update language for buttons
            updateLanguage();
        }

        // Add a new product
        function addProduct(productData) {
            const newProduct = {
                id: products.length > 0 ? Math.max(...products.map(p => p.id)) + 1 : 1,
                ...productData
            };
            
            products.push(newProduct);
            renderFeaturedProducts();
            renderAllProducts();
            renderAdminProducts();
        }

        // Edit a product
        function editProduct(productId) {
            const product = products.find(p => p.id === productId);
            if (product) {
                document.getElementById('product-name').value = product.name;
                document.getElementById('product-description').value = product.description;
                document.getElementById('product-price').value = product.price;
                document.getElementById('product-image').value = product.image;
                document.getElementById('product-category').value = product.category;
                document.getElementById('product-featured').checked = product.featured;
                
                editingProductId = productId;
                cancelEditBtn.style.display = 'inline-block';
            }
        }

        // Update a product
        function updateProduct(productId, productData) {
            const productIndex = products.findIndex(p => p.id === productId);
            if (productIndex !== -1) {
                products[productIndex] = { id: productId, ...productData };
                renderFeaturedProducts();
                renderAllProducts();
                renderAdminProducts();
            }
        }

        // Delete a product
        function deleteProduct(productId) {
            if (confirm('Are you sure you want to delete this product?')) {
                products = products.filter(p => p.id !== productId);
                renderFeaturedProducts();
                renderAllProducts();
                renderAdminProducts();
            }
        }
    </script>
</body>
</html>
