<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Healix Care - Premium Mobile Accessories</title>
    <style>
        /* Global Styles */
        :root {
            --primary: #121212;
            --secondary: #FF5722;
            --accent: #D4AF37;
            --light: #1E1E1E;
            --dark: #0A0A0A;
            --success: #4CAF50;
            --text: #E0E0E0;
            --text-secondary: #B0B0B0;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, var(--secondary) 0%, #E64A19 100%);
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            text-decoration: none;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.4s ease;
            box-shadow: 0 4px 15px rgba(255, 87, 34, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: 0.5s;
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 87, 34, 0.5);
        }
        
        .btn-gold {
            background: linear-gradient(135deg, var(--accent) 0%, #B8860B 100%);
            box-shadow: 0 4px 15px rgba(212, 175, 55, 0.3);
        }
        
        .btn-gold:hover {
            box-shadow: 0 8px 25px rgba(212, 175, 55, 0.5);
        }
        
        .btn-danger {
            background: linear-gradient(135deg, #F44336 0%, #B71C1C 100%);
            box-shadow: 0 4px 15px rgba(244, 67, 54, 0.3);
        }
        
        .btn-danger:hover {
            box-shadow: 0 8px 25px rgba(244, 67, 54, 0.5);
        }
        
        .btn-success {
            background: linear-gradient(135deg, var(--success) 0%, #2E7D32 100%);
            box-shadow: 0 4px 15px rgba(76, 175, 80, 0.3);
        }
        
        .btn-success:hover {
            box-shadow: 0 8px 25px rgba(76, 175, 80, 0.5);
        }
        
        /* Header Styles */
        header {
            background: rgba(18, 18, 18, 0.95);
            backdrop-filter: blur(10px);
            color: white;
            padding: 15px 0;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        
        .logo-img {
            width: 50px;
            height: 50px;
            margin-right: 12px;
            background: linear-gradient(135deg, var(--accent) 0%, var(--secondary) 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.5);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 10px rgba(212, 175, 55, 0.5); }
            50% { box-shadow: 0 0 20px rgba(212, 175, 55, 0.8); }
            100% { box-shadow: 0 0 10px rgba(212, 175, 55, 0.5); }
        }
        
        .logo-img svg {
            width: 30px;
            height: 30px;
            filter: drop-shadow(0 0 5px rgba(0,0,0,0.5));
        }
        
        .logo h1 {
            font-size: 26px;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: var(--text);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            cursor: pointer;
            padding: 8px 12px;
            border-radius: 6px;
            position: relative;
            overflow: hidden;
        }
        
        nav ul li a::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover::before, nav ul li a.active::before {
            width: 100%;
        }
        
        nav ul li a:hover, nav ul li a.active {
            color: white;
        }
        
        .cart-icon {
            position: relative;
        }
        
        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: linear-gradient(135deg, var(--secondary) 0%, #E64A19 100%);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            font-weight: bold;
            box-shadow: 0 2px 8px rgba(255, 87, 34, 0.5);
        }
        
        .language-selector {
            display: flex;
            align-items: center;
        }
        
        .language-selector select {
            padding: 8px 12px;
            border-radius: 6px;
            border: 1px solid rgba(212, 175, 55, 0.3);
            background: rgba(30, 30, 30, 0.8);
            color: var(--text);
            margin-left: 10px;
            transition: all 0.3s;
        }
        
        .language-selector select:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }
        
        /* Enhanced Hero Animation - Apple/Samsung Style */
        .hero-animation {
            position: relative;
            height: 80vh;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 50px;
            background: radial-gradient(ellipse at center, rgba(30,30,30,0.8) 0%, rgba(10,10,10,0.9) 70%);
            perspective: 1000px;
        }
        
        .parallax-bg {
            position: absolute;
            width: 120%;
            height: 120%;
            top: -10%;
            left: -10%;
            background: 
                radial-gradient(circle at 20% 30%, rgba(212, 175, 55, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(255, 87, 34, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 80%, rgba(76, 175, 80, 0.1) 0%, transparent 50%);
            transform-style: preserve-3d;
            will-change: transform;
        }
        
        .floating-product {
            position: absolute;
            width: 200px;
            height: 200px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 175, 55, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            transform-style: preserve-3d;
            transition: transform 0.5s ease;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            overflow: hidden;
        }
        
        .floating-product img {
            max-width: 80%;
            max-height: 80%;
            object-fit: contain;
            filter: drop-shadow(0 10px 20px rgba(0,0,0,0.5));
        }
        
        .floating-product:nth-child(1) {
            top: 15%;
            left: 10%;
            animation: floatProduct 15s ease-in-out infinite;
        }
        
        .floating-product:nth-child(2) {
            top: 60%;
            left: 75%;
            animation: floatProduct 18s ease-in-out infinite reverse;
        }
        
        .floating-product:nth-child(3) {
            top: 75%;
            left: 15%;
            animation: floatProduct 20s ease-in-out infinite 2s;
        }
        
        .floating-product:nth-child(4) {
            top: 25%;
            left: 70%;
            animation: floatProduct 16s ease-in-out infinite 1s;
        }
        
        @keyframes floatProduct {
            0%, 100% {
                transform: translateY(0px) rotateX(0deg) rotateY(0deg);
            }
            25% {
                transform: translateY(-20px) rotateX(5deg) rotateY(5deg);
            }
            50% {
                transform: translateY(-10px) rotateX(-5deg) rotateY(-5deg);
            }
            75% {
                transform: translateY(-15px) rotateX(3deg) rotateY(-3deg);
            }
        }
        
        .hero-content {
            text-align: center;
            z-index: 10;
            max-width: 800px;
            padding: 0 20px;
            transform-style: preserve-3d;
        }
        
        .hero-title {
            font-size: 4rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--accent), var(--secondary), #4CAF50);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(0,0,0,0.3);
            animation: titleGlow 4s ease-in-out infinite alternate;
            font-weight: 800;
            letter-spacing: -1px;
        }
        
        @keyframes titleGlow {
            from {
                filter: drop-shadow(0 0 10px rgba(212, 175, 55, 0.5));
            }
            to {
                filter: drop-shadow(0 0 25px rgba(212, 175, 55, 0.8)) drop-shadow(0 0 35px rgba(255, 87, 34, 0.6));
            }
        }
        
        .hero-subtitle {
            font-size: 1.3rem;
            margin-bottom: 30px;
            color: var(--text-secondary);
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.8;
        }
        
        /* Page Sections */
        .page-section {
            display: none;
            padding: 80px 0;
            min-height: 60vh;
        }
        
        .page-section.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Products Section */
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--text);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
            border-radius: 3px;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            transition: all 0.4s ease;
            border: 1px solid rgba(212, 175, 55, 0.1);
            backdrop-filter: blur(10px);
        }
        
        .product-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 40px rgba(0,0,0,0.4), 0 0 20px rgba(212, 175, 55, 0.2);
            border-color: rgba(212, 175, 55, 0.3);
        }
        
        .product-image {
            height: 200px;
            background: linear-gradient(135deg, rgba(30,30,30,0.9) 0%, rgba(10,10,10,0.9) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            position: relative;
        }
        
        .product-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(212, 175, 55, 0.1), transparent);
            opacity: 0;
            transition: opacity 0.4s;
        }
        
        .product-card:hover .product-image::before {
            opacity: 1;
        }
        
        .product-image img {
            max-width: 100%;
            max-height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .product-card:hover .product-image img {
            transform: scale(1.05);
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-info h3 {
            font-size: 18px;
            margin-bottom: 10px;
            color: var(--text);
        }
        
        .product-info p {
            color: var(--text-secondary);
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
            color: var(--accent);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }
        
        .original-price {
            text-decoration: line-through;
            color: var(--text-secondary);
            font-size: 14px;
            margin-right: 5px;
        }
        
        .discount-badge {
            background: linear-gradient(135deg, var(--success) 0%, #2E7D32 100%);
            color: white;
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: bold;
            margin-left: 5px;
        }
        
        /* Enhanced Admin Panel */
        .admin-panel {
            background: rgba(30, 30, 30, 0.8);
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            margin: 40px 0;
            border: 1px solid rgba(212, 175, 55, 0.2);
            backdrop-filter: blur(10px);
        }
        
        .admin-panel h2 {
            color: var(--accent);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }
        
        .admin-tabs {
            display: flex;
            margin-bottom: 20px;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }
        
        .admin-tab {
            padding: 10px 20px;
            cursor: pointer;
            border-bottom: 3px solid transparent;
            transition: all 0.3s;
        }
        
        .admin-tab.active {
            border-bottom-color: var(--accent);
            color: var(--accent);
        }
        
        .admin-tab-content {
            display: none;
        }
        
        .admin-tab-content.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--text);
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid rgba(212, 175, 55, 0.3);
            border-radius: 8px;
            font-size: 16px;
            background: rgba(18, 18, 18, 0.7);
            color: var(--text);
            transition: all 0.3s;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }
        
        /* File Upload */
        .file-upload {
            position: relative;
            overflow: hidden;
            display: inline-block;
            width: 100%;
        }
        
        .file-upload-btn {
            background: linear-gradient(135deg, var(--secondary) 0%, #E64A19 100%);
            color: white;
            padding: 12px 20px;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            display: block;
            text-align: center;
            transition: all 0.3s;
        }
        
        .file-upload-btn:hover {
            background: linear-gradient(135deg, #E64A19 0%, var(--secondary) 100%);
        }
        
        .file-upload-input {
            position: absolute;
            left: 0;
            top: 0;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }
        
        /* Admin Login */
        .admin-login {
            max-width: 400px;
            margin: 50px auto;
            background: rgba(30, 30, 30, 0.8);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 1px solid rgba(212, 175, 55, 0.2);
            backdrop-filter: blur(10px);
        }
        
        .admin-login h2 {
            text-align: center;
            margin-bottom: 20px;
            color: var(--accent);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }
        
        /* Cart Page */
        .cart-container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
        }
        
        .cart-items {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 1px solid rgba(212, 175, 55, 0.1);
            backdrop-filter: blur(10px);
        }
        
        .cart-item {
            display: flex;
            padding: 15px 0;
            border-bottom: 1px solid rgba(212, 175, 55, 0.1);
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
            background: rgba(18, 18, 18, 0.7);
            border-radius: 8px;
            overflow: hidden;
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
            color: var(--text);
        }
        
        .cart-item-details p {
            color: var(--text-secondary);
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
            background: rgba(212, 175, 55, 0.2);
            border: none;
            border-radius: 6px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            color: var(--text);
            transition: all 0.3s;
        }
        
        .quantity-btn:hover {
            background: rgba(212, 175, 55, 0.4);
        }
        
        .quantity {
            margin: 0 10px;
            font-weight: bold;
            color: var(--text);
        }
        
        .cart-summary {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 1px solid rgba(212, 175, 55, 0.1);
            backdrop-filter: blur(10px);
            height: fit-content;
        }
        
        .summary-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .summary-total {
            font-weight: bold;
            font-size: 18px;
            color: var(--accent);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }
        
        /* Checkout Page */
        .checkout-container {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 30px;
        }
        
        .checkout-form {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 1px solid rgba(212, 175, 55, 0.1);
            backdrop-filter: blur(10px);
        }
        
        .checkout-summary {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 1px solid rgba(212, 175, 55, 0.1);
            backdrop-filter: blur(10px);
            height: fit-content;
        }
        
        .checkout-item {
            display: flex;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .checkout-item-image {
            width: 60px;
            height: 60px;
            margin-right: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(18, 18, 18, 0.7);
            border-radius: 8px;
            overflow: hidden;
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
            color: var(--text);
        }
        
        .checkout-item-details p {
            font-size: 12px;
            color: var(--text-secondary);
        }
        
        /* Shipping Management */
        .shipping-rates {
            margin-top: 20px;
        }
        
        .shipping-rate {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;
            border-bottom: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .shipping-rate:last-child {
            border-bottom: none;
        }
        
        /* Category Management */
        .categories-list {
            margin-top: 20px;
        }
        
        .category-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;
            border-bottom: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .category-item:last-child {
            border-bottom: none;
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
            background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);
            color: white;
            padding: 12px 20px;
            border-radius: 50px;
            box-shadow: 0 5px 15px rgba(37, 211, 102, 0.4);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .whatsapp-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(37, 211, 102, 0.6);
        }
        
        .whatsapp-btn i {
            font-size: 24px;
            margin-right: 10px;
        }
        
        /* Footer */
        footer {
            background: rgba(10, 10, 10, 0.95);
            color: white;
            padding: 60px 0 30px;
            border-top: 1px solid rgba(212, 175, 55, 0.2);
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
            color: var(--accent);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: var(--text-secondary);
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
            color: var(--text-secondary);
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
            
            .hero-title {
                font-size: 2.5rem;
            }
            
            .about-content,
            .contact-container,
            .cart-container,
            .checkout-container {
                grid-template-columns: 1fr;
            }
            
            .hero-animation {
                height: 60vh;
            }
            
            .form-row {
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
        .fa-upload:before { content: "\f093"; }
        .fa-truck:before { content: "\f0d1"; }
        .fa-tags:before { content: "\f02c"; }
        .fa-layer-group:before { content: "\f5fd"; }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <a href="#" class="logo" data-page="home">
                    <div class="logo-img">
                        <svg viewBox="0 0 100 100">
                            <defs>
                                <linearGradient id="goldGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                                    <stop offset="0%" stop-color="#D4AF37" />
                                    <stop offset="100%" stop-color="#FFD700" />
                                </linearGradient>
                                <filter id="glow">
                                    <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
                                    <feMerge>
                                        <feMergeNode in="coloredBlur"/>
                                        <feMergeNode in="SourceGraphic"/>
                                    </feMerge>
                                </filter>
                            </defs>
                            <circle cx="50" cy="50" r="45" fill="url(#goldGradient)" filter="url(#glow)" />
                            <path d="M50,15 L60,40 L85,45 L65,65 L70,90 L50,75 L30,90 L35,65 L15,45 L40,40 Z" fill="#121212" />
                            <circle cx="50" cy="50" r="15" fill="url(#goldGradient)" />
                        </svg>
                    </div>
                    <h1>Healix Care</h1>
                </a>
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
                        <option value="ar">العربية</option>
                    </select>
                </div>
            </div>
        </div>
    </header>

    <!-- Home Page -->
    <section id="home-page" class="page-section active">
        <!-- Enhanced Hero Animation -->
        <div class="hero-animation">
            <div class="parallax-bg" id="parallax-bg"></div>
            <div class="floating-product">
                <img src="https://images.unsplash.com/photo-1601593346740-925612772716?ixlib=rb-4.0.3&auto=format&fit=crop&w=687&q=80" alt="Screen Protector">
            </div>
            <div class="floating-product">
                <img src="https://images.unsplash.com/photo-1556656793-08538906a9f8?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Phone Case">
            </div>
            <div class="floating-product">
                <img src="https://images.unsplash.com/photo-1583394838336-acd977736f90?ixlib=rb-4.0.3&auto=format&fit=crop&w=684&q=80" alt="USB Adapter">
            </div>
            <div class="floating-product">
                <img src="https://images.unsplash.com/photo-1605784407953-8fe7c72dab4d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Charging Cable">
            </div>
            <div class="hero-content">
                <h1 class="hero-title" data-key="heroTitle">Premium Mobile Accessories</h1>
                <p class="hero-subtitle" data-key="heroSubtitle">Discover our high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional. Experience the perfect blend of protection and style.</p>
                <a class="btn shop-now-btn" data-key="shopNow" data-page="products">Shop Now</a>
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
                    <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="About Healix Care">
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
                        <p><i class="fas fa-envelope"></i> healixcare786@gmail.com</p>
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
                        <i class="fas fa-shopping-bag" style="font-size: 48px; color: rgba(212, 175, 55, 0.3); margin-bottom: 20px;"></i>
                        <h3 data-key="emptyCart">Your cart is empty</h3>
                        <p data-key="addItems">Add some products to your cart</p>
                        <a class="btn" data-page="products" data-key="continueShopping" style="margin-top: 20px;">Continue Shopping</a>
                    </div>
                </div>
                <div class="cart-summary">
                    <h3 data-key="orderSummary">Order Summary</h3>
                    <div class="form-group">
                        <label for="delivery-charge" data-key="deliveryCharge">Delivery Charge ($)</label>
                        <input type="number" id="delivery-charge" class="form-control" value="5.00" step="0.01" min="0" readonly>
                        <small style="color: var(--text-secondary);">Shipping charges are controlled by admin</small>
                    </div>
                    <div class="summary-row">
                        <span data-key="subtotal">Subtotal:</span>
                        <span id="cart-subtotal">$0.00</span>
                    </div>
                    <div class="summary-row">
                        <span data-key="shipping">Shipping:</span>
                        <span id="cart-shipping">$5.00</span>
                    </div>
                    <div class="summary-row">
                        <span data-key="discount">Discount:</span>
                        <span id="cart-discount">-$0.00</span>
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

    <!-- Enhanced Checkout Page -->
    <section id="checkout-page" class="page-section">
        <div class="container">
            <div class="section-title">
                <h2 data-key="checkout">Checkout</h2>
            </div>
            <div class="checkout-container">
                <div class="checkout-form">
                    <h3 data-key="customerDetails">Customer Details</h3>
                    <form id="checkout-form">
                        <div class="form-row">
                            <div class="form-group">
                                <label for="checkout-firstname" data-key="firstName">First Name *</label>
                                <input type="text" id="checkout-firstname" class="form-control" required>
                            </div>
                            <div class="form-group">
                                <label for="checkout-lastname" data-key="lastName">Last Name *</label>
                                <input type="text" id="checkout-lastname" class="form-control" required>
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="checkout-email" data-key="emailAddress">Email Address *</label>
                            <input type="email" id="checkout-email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="checkout-phone" data-key="phoneNumber">Phone Number *</label>
                            <input type="tel" id="checkout-phone" class="form-control" required>
                        </div>
                        
                        <h3 style="margin-top: 30px;" data-key="shippingAddress">Shipping Address</h3>
                        <div class="form-group">
                            <label for="checkout-address" data-key="streetAddress">Street Address *</label>
                            <input type="text" id="checkout-address" class="form-control" required>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label for="checkout-city" data-key="city">City *</label>
                                <input type="text" id="checkout-city" class="form-control" required>
                            </div>
                            <div class="form-group">
                                <label for="checkout-region" data-key="region">Region/State *</label>
                                <input type="text" id="checkout-region" class="form-control" required>
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label for="checkout-zip" data-key="zipCode">ZIP/Postal Code *</label>
                                <input type="text" id="checkout-zip" class="form-control" required>
                            </div>
                            <div class="form-group">
                                <label for="checkout-country" data-key="country">Country *</label>
                                <select id="checkout-country" class="form-control" required>
                                    <option value="">Select Country</option>
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
                        </div>
                        
                        <h3 style="margin-top: 30px;" data-key="deliveryInstructions">Delivery Instructions</h3>
                        <div class="form-group">
                            <label for="delivery-instructions" data-key="specialInstructions">Special Instructions (Optional)</label>
                            <textarea id="delivery-instructions" class="form-control" placeholder="Any special delivery instructions..."></textarea>
                        </div>
                        
                        <h3 style="margin-top: 30px;" data-key="paymentInformation">Payment Information</h3>
                        <div class="form-group">
                            <label for="checkout-card" data-key="cardNumber">Card Number *</label>
                            <input type="text" id="checkout-card" class="form-control" placeholder="1234 5678 9012 3456" required>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label for="checkout-expiry" data-key="expiryDate">Expiry Date *</label>
                                <input type="text" id="checkout-expiry" class="form-control" placeholder="MM/YY" required>
                            </div>
                            <div class="form-group">
                                <label for="checkout-cvv" data-key="cvv">CVV *</label>
                                <input type="text" id="checkout-cvv" class="form-control" placeholder="123" required>
                            </div>
                        </div>
                        
                        <div class="form-group" style="margin-top: 20px;">
                            <label>
                                <input type="checkbox" id="subscribe-email" checked>
                                <span data-key="subscribeNewsletter">Subscribe to our newsletter for updates and special offers</span>
                            </label>
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
                        <span data-key="discount">Discount:</span>
                        <span id="checkout-discount">-$0.00</span>
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

    <!-- Enhanced Admin Page -->
    <section id="admin-page" class="page-section">
        <div class="container">
            <div class="admin-panel">
                <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                    <h2 data-key="adminPanel">Admin Panel - Healix Care</h2>
                    <button class="btn btn-danger" id="admin-logout" data-key="logout">Logout</button>
                </div>
                
                <div class="admin-tabs">
                    <div class="admin-tab active" data-tab="products">Products</div>
                    <div class="admin-tab" data-tab="categories">Categories</div>
                    <div class="admin-tab" data-tab="shipping">Shipping</div>
                    <div class="admin-tab" data-tab="discounts">Discounts</div>
                    <div class="admin-tab" data-tab="orders">Orders</div>
                </div>
                
                <!-- Products Tab -->
                <div class="admin-tab-content active" id="products-tab">
                    <h3 data-key="manageProducts">Manage Products</h3>
                    <form id="product-form">
                        <div class="form-group">
                            <label for="product-name" data-key="productName">Product Name</label>
                            <input type="text" id="product-name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="product-description" data-key="productDescription">Description</label>
                            <textarea id="product-description" class="form-control" required></textarea>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label for="product-price" data-key="productPrice">Price ($)</label>
                                <input type="number" id="product-price" class="form-control" step="0.01" min="0" required>
                            </div>
                            <div class="form-group">
                                <label for="product-discount" data-key="productDiscount">Discount (%)</label>
                                <input type="number" id="product-discount" class="form-control" step="1" min="0" max="100" value="0">
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="product-image" data-key="productImage">Product Image</label>
                            <div class="file-upload">
                                <div class="file-upload-btn">
                                    <i class="fas fa-upload"></i> <span data-key="chooseImage">Choose Image</span>
                                </div>
                                <input type="file" id="product-image" class="file-upload-input" accept="image/*" required>
                            </div>
                            <div id="image-preview" style="margin-top: 10px; display: none;">
                                <img id="preview-img" src="#" alt="Preview" style="max-width: 200px; max-height: 150px; border-radius: 8px;">
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="product-category" data-key="productCategory">Category</label>
                            <select id="product-category" class="form-control" required>
                                <!-- Categories will be populated dynamically -->
                            </select>
                        </div>
                        <div class="form-group">
                            <label>
                                <input type="checkbox" id="product-featured">
                                <span data-key="featuredProduct">Featured Product</span>
                            </label>
                        </div>
                        <button type="submit" class="btn btn-success" id="product-submit-btn" data-key="addProduct">Add Product</button>
                        <button type="button" class="btn btn-danger" id="cancel-edit" style="display: none;" data-key="cancel">Cancel</button>
                    </form>
                    
                    <div class="existing-products" style="margin-top: 40px;">
                        <h3 data-key="existingProducts">Existing Products</h3>
                        <div id="admin-products-list">
                            <!-- Admin product list will be populated here -->
                        </div>
                    </div>
                </div>
                
                <!-- Categories Tab -->
                <div class="admin-tab-content" id="categories-tab">
                    <h3 data-key="manageCategories">Manage Categories</h3>
                    <form id="category-form">
                        <div class="form-group">
                            <label for="category-name" data-key="categoryName">Category Name</label>
                            <input type="text" id="category-name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="category-description" data-key="categoryDescription">Description</label>
                            <textarea id="category-description" class="form-control"></textarea>
                        </div>
                        <button type="submit" class="btn btn-success" data-key="addCategory">Add Category</button>
                    </form>
                    
                    <div class="categories-list" style="margin-top: 40px;">
                        <h3 data-key="existingCategories">Existing Categories</h3>
                        <div id="admin-categories-list">
                            <!-- Categories list will be populated here -->
                        </div>
                    </div>
                </div>
                
                <!-- Shipping Tab -->
                <div class="admin-tab-content" id="shipping-tab">
                    <h3 data-key="manageShipping">Manage Shipping Charges</h3>
                    <form id="shipping-form">
                        <div class="form-group">
                            <label for="shipping-country" data-key="country">Country</label>
                            <select id="shipping-country" class="form-control" required>
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
                        <div class="form-group">
                            <label for="shipping-charge" data-key="shippingCharge">Shipping Charge ($)</label>
                            <input type="number" id="shipping-charge" class="form-control" step="0.01" min="0" required>
                        </div>
                        <button type="submit" class="btn btn-success" data-key="setShipping">Set Shipping Charge</button>
                    </form>
                    
                    <div class="shipping-rates" style="margin-top: 40px;">
                        <h3 data-key="shippingRates">Current Shipping Rates</h3>
                        <div id="admin-shipping-list">
                            <!-- Shipping rates will be populated here -->
                        </div>
                    </div>
                </div>
                
                <!-- Discounts Tab -->
                <div class="admin-tab-content" id="discounts-tab">
                    <h3 data-key="manageDiscounts">Manage Discounts</h3>
                    <div class="form-group">
                        <label for="global-discount" data-key="globalDiscount">Global Discount (%)</label>
                        <input type="number" id="global-discount" class="form-control" step="1" min="0" max="100" value="0">
                        <small style="color: var(--text-secondary);" data-key="globalDiscountDesc">This discount will apply to all products</small>
                    </div>
                    <button class="btn btn-success" id="apply-global-discount" data-key="applyDiscount">Apply Global Discount</button>
                    
                    <div style="margin-top: 40px;">
                        <h3 data-key="productDiscounts">Product-specific Discounts</h3>
                        <p data-key="productDiscountsDesc">Set individual discounts for each product in the Products tab</p>
                    </div>
                </div>
                
                <!-- Orders Tab -->
                <div class="admin-tab-content" id="orders-tab">
                    <h3 data-key="orderManagement">Order Management</h3>
                    <div id="admin-orders-list">
                        <!-- Orders will be populated here -->
                        <p data-key="noOrders">No orders placed yet</p>
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
                        <li><a data-page="admin" data-key="admin">Admin</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3 data-key="contactInfo">Contact Information</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> <span data-key="address">Faisalabad, Punjab, Pakistan</span></li>
                        <li><i class="fas fa-phone"></i> <span data-key="phone">+92 3481869972</span></li>
                        <li><i class="fas fa-phone"></i> <span data-key="phone2">+92 3279000242</span></li>
                        <li><i class="fas fa-envelope"></i> healixcare786@gmail.com</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Healix Care. <span data-key="allRights">All rights reserved</span>.</p>
            </div>
        </div>
    </footer>

    <script>
        // Language translations - Only English and Arabic
        var translations = {
            en: {
                home: "Home",
                products: "Products",
                about: "About",
                contact: "Contact",
                admin: "Admin",
                language: "Language",
                heroTitle: "Premium Mobile Accessories",
                heroSubtitle: "Discover our high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional. Experience the perfect blend of protection and style.",
                shopNow: "Shop Now",
                featuredProducts: "Featured Products",
                allProducts: "All Products",
                adminPanel: "Admin Panel - Healix Care",
                manageProducts: "Manage Products",
                productName: "Product Name",
                productDescription: "Description",
                productPrice: "Price ($)",
                productDiscount: "Discount (%)",
                productImage: "Product Image",
                productCategory: "Category",
                addProduct: "Add Product",
                updateProduct: "Update Product",
                cancel: "Cancel",
                existingProducts: "Existing Products",
                manageCategories: "Manage Categories",
                categoryName: "Category Name",
                categoryDescription: "Description",
                addCategory: "Add Category",
                existingCategories: "Existing Categories",
                manageShipping: "Manage Shipping Charges",
                shippingCharge: "Shipping Charge ($)",
                setShipping: "Set Shipping Charge",
                shippingRates: "Current Shipping Rates",
                manageDiscounts: "Manage Discounts",
                globalDiscount: "Global Discount (%)",
                globalDiscountDesc: "This discount will apply to all products",
                applyDiscount: "Apply Global Discount",
                productDiscounts: "Product-specific Discounts",
                productDiscountsDesc: "Set individual discounts for each product in the Products tab",
                orderManagement: "Order Management",
                noOrders: "No orders placed yet",
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
                edit: "Edit",
                delete: "Delete",
                addToCart: "Add to Cart",
                shoppingCart: "Shopping Cart",
                orderSummary: "Order Summary",
                subtotal: "Subtotal",
                shipping: "Shipping",
                discount: "Discount",
                deliveryCharge: "Delivery Charge ($)",
                total: "Total",
                proceedToCheckout: "Proceed to Checkout",
                emptyCart: "Your cart is empty",
                addItems: "Add some products to your cart",
                continueShopping: "Continue Shopping",
                checkout: "Checkout",
                customerDetails: "Customer Details",
                firstName: "First Name",
                lastName: "Last Name",
                emailAddress: "Email Address",
                phoneNumber: "Phone Number",
                shippingAddress: "Shipping Address",
                streetAddress: "Street Address",
                city: "City",
                region: "Region/State",
                zipCode: "ZIP/Postal Code",
                country: "Country",
                deliveryInstructions: "Delivery Instructions",
                specialInstructions: "Special Instructions (Optional)",
                paymentInformation: "Payment Information",
                cardNumber: "Card Number",
                expiryDate: "Expiry Date",
                cvv: "CVV",
                placeOrder: "Place Order",
                subscribeNewsletter: "Subscribe to our newsletter for updates and special offers",
                adminLogin: "Admin Login",
                username: "Username",
                password: "Password",
                login: "Login",
                logout: "Logout",
                remove: "Remove",
                quantity: "Quantity",
                featuredProduct: "Featured Product",
                whatsappHelp: "Need Help?",
                chooseImage: "Choose Image",
                screenProtector: "Screen Protector",
                phoneCase: "Phone Case",
                cable: "Cable",
                charger: "Charger",
                other: "Other"
            },
            ar: {
                home: "الرئيسية",
                products: "المنتجات",
                about: "من نحن",
                contact: "اتصل بنا",
                admin: "المشرف",
                language: "اللغة",
                heroTitle: "إكسسوارات الجوال الممتازة",
                heroSubtitle: "اكتشف واقيات الشاشة عالية الجودة والأغطية والكابلات والمزيد للحفاظ على أجهزتك آمنة ووظيفية. جرب المزيج المثالي بين الحماية والأناقة.",
                shopNow: "تسوق الآن",
                featuredProducts: "المنتجات المميزة",
                allProducts: "جميع المنتجات",
                adminPanel: "لوحة التحكم - هيلكس كير",
                manageProducts: "إدارة المنتجات",
                productName: "اسم المنتج",
                productDescription: "الوصف",
                productPrice: "السعر ($)",
                productDiscount: "الخصم (%)",
                productImage: "صورة المنتج",
                productCategory: "الفئة",
                addProduct: "إضافة منتج",
                updateProduct: "تحديث المنتج",
                cancel: "إلغاء",
                existingProducts: "المنتجات الحالية",
                manageCategories: "إدارة الفئات",
                categoryName: "اسم الفئة",
                categoryDescription: "الوصف",
                addCategory: "إضافة فئة",
                existingCategories: "الفئات الحالية",
                manageShipping: "إدارة رسوم الشحن",
                shippingCharge: "رسوم الشحن ($)",
                setShipping: "تعيين رسوم الشحن",
                shippingRates: "أسعار الشحن الحالية",
                manageDiscounts: "إدارة الخصومات",
                globalDiscount: "الخصم العام (%)",
                globalDiscountDesc: "سيتم تطبيق هذا الخصم على جميع المنتجات",
                applyDiscount: "تطبيق الخصم العام",
                productDiscounts: "خصومات المنتجات الفردية",
                productDiscountsDesc: "تعيين خصومات فردية لكل منتج في علامة تبويب المنتجات",
                orderManagement: "إدارة الطلبات",
                noOrders: "لم يتم تقديم أي طلبات بعد",
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
                edit: "تعديل",
                delete: "حذف",
                addToCart: "أضف إلى السلة",
                shoppingCart: "سلة التسوق",
                orderSummary: "ملخص الطلب",
                subtotal: "المجموع الفرعي",
                shipping: "الشحن",
                discount: "الخصم",
                deliveryCharge: "رسوم التوصيل ($)",
                total: "المجموع",
                proceedToCheckout: "تابع للدفع",
                emptyCart: "سلة التسوق فارغة",
                addItems: "أضف بعض المنتجات إلى سلة التسوق",
                continueShopping: "مواصلة التسوق",
                checkout: "الدفع",
                customerDetails: "تفاصيل العميل",
                firstName: "الاسم الأول",
                lastName: "اسم العائلة",
                emailAddress: "عنوان البريد الإلكتروني",
                phoneNumber: "رقم الهاتف",
                shippingAddress: "عنوان الشحن",
                streetAddress: "عنوان الشارع",
                city: "المدينة",
                region: "المنطقة/المحافظة",
                zipCode: "الرمز البريدي",
                country: "البلد",
                deliveryInstructions: "تعليمات التوصيل",
                specialInstructions: "تعليمات خاصة (اختياري)",
                paymentInformation: "معلومات الدفع",
                cardNumber: "رقم البطاقة",
                expiryDate: "تاريخ الانتهاء",
                cvv: "CVV",
                placeOrder: "تقديم الطلب",
                subscribeNewsletter: "اشترك في نشرتنا الإخبارية للحصول على التحديثات والعروض الخاصة",
                adminLogin: "تسجيل دخول المسؤول",
                username: "اسم المستخدم",
                password: "كلمة المرور",
                login: "تسجيل الدخول",
                logout: "تسجيل الخروج",
                remove: "إزالة",
                quantity: "الكمية",
                featuredProduct: "منتج مميز",
                whatsappHelp: "تحتاج مساعدة؟",
                chooseImage: "اختر صورة",
                screenProtector: "واقي الشاشة",
                phoneCase: "غطاء الهاتف",
                cable: "كابل",
                charger: "شاحن",
                other: "أخرى"
            }
        };

        // Sample products data (15 products)
        var products = [
            {
                id: 1,
                name: "Tempered Glass Screen Protector",
                description: "9H hardness tempered glass with oleophobic coating to resist fingerprints.",
                price: 12.99,
                discount: 10,
                image: "https://images.unsplash.com/photo-1601593346740-925612772716?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80",
                category: "screen-protector",
                featured: true
            },
            {
                id: 2,
                name: "Silicone Phone Case",
                description: "Shock-absorbent silicone case with raised edges for screen protection.",
                price: 18.99,
                discount: 15,
                image: "https://images.unsplash.com/photo-1556656793-08538906a9f8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "phone-case",
                featured: true
            },
            {
                id: 3,
                name: "USB-C to USB Adapter",
                description: "High-speed OTG adapter for connecting USB devices to your smartphone.",
                price: 8.99,
                discount: 0,
                image: "https://images.unsplash.com/photo-1583394838336-acd977736f90?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=684&q=80",
                category: "cable",
                featured: false
            },
            {
                id: 4,
                name: "Fast Charging Cable",
                description: "Durable braided USB-C cable with fast charging capability.",
                price: 14.99,
                discount: 20,
                image: "https://images.unsplash.com/photo-1605784407953-8fe7c72dab4d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "cable",
                featured: true
            },
            {
                id: 5,
                name: "Wireless Charging Pad",
                description: "10W fast wireless charging pad with LED indicator.",
                price: 24.99,
                discount: 5,
                image: "https://images.unsplash.com/photo-1572569511254-d8f925fe2cbb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1169&q=80",
                category: "charger",
                featured: false
            },
            {
                id: 6,
                name: "Car Phone Holder",
                description: "Adjustable car vent phone holder with strong grip.",
                price: 15.99,
                discount: 0,
                image: "https://images.unsplash.com/photo-1586953208448-b95a79798f07?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 7,
                name: "Bluetooth Earbuds",
                description: "Wireless earbuds with noise cancellation and 20hr battery.",
                price: 49.99,
                discount: 25,
                image: "https://images.unsplash.com/photo-1590658165737-15a047b8b5e9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1012&q=80",
                category: "other",
                featured: true
            },
            {
                id: 8,
                name: "Phone Stand",
                description: "Adjustable aluminum phone stand for desktop use.",
                price: 12.99,
                discount: 0,
                image: "https://images.unsplash.com/photo-1545454675-3531b543be5d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 9,
                name: "Power Bank 10000mAh",
                description: "Compact power bank with fast charging support.",
                price: 29.99,
                discount: 10,
                image: "https://images.unsplash.com/photo-1609592810793-abeb6c64b5c6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1169&q=80",
                category: "charger",
                featured: true
            },
            {
                id: 10,
                name: "Phone Cleaning Kit",
                description: "Complete kit for cleaning phone screens and ports.",
                price: 9.99,
                discount: 0,
                image: "https://images.unsplash.com/photo-1616343932295-68d2596765f8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 11,
                name: "Magnetic Car Mount",
                description: "Strong magnetic car mount for easy phone placement.",
                price: 19.99,
                discount: 15,
                image: "https://images.unsplash.com/photo-1565842777185-6aea8d30f23c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 12,
                name: "Waterproof Phone Pouch",
                description: "Transparent waterproof pouch for beach and pool use.",
                price: 14.99,
                discount: 0,
                image: "https://images.unsplash.com/photo-1558618666-fcd25856cd63?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "phone-case",
                featured: false
            },
            {
                id: 13,
                name: "Phone Grip Ring",
                description: "Adhesive phone grip for secure one-handed use.",
                price: 7.99,
                discount: 0,
                image: "https://images.unsplash.com/photo-1616343932295-68d2596765f8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: false
            },
            {
                id: 14,
                name: "Multi-Port USB Hub",
                description: "4-port USB hub for expanding connectivity.",
                price: 22.99,
                discount: 10,
                image: "https://images.unsplash.com/photo-1598300042247-d088f8ab3a91?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1064&q=80",
                category: "cable",
                featured: false
            },
            {
                id: 15,
                name: "Phone Lens Kit",
                description: "Clip-on lens kit for wide-angle and macro photography.",
                price: 24.99,
                discount: 20,
                image: "https://images.unsplash.com/photo-1555774698-0b77e0d5fac6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
                category: "other",
                featured: true
            }
        ];

        // Categories data
        var categories = [
            { id: "screen-protector", name: "Screen Protector", description: "Screen protection products" },
            { id: "phone-case", name: "Phone Case", description: "Phone cases and covers" },
            { id: "cable", name: "Cable", description: "Charging and data cables" },
            { id: "charger", name: "Charger", description: "Chargers and power accessories" },
            { id: "other", name: "Other", description: "Other mobile accessories" }
        ];

        // Shipping rates
        var shippingRates = {
            "pakistan": 5.00,
            "uae": 15.00,
            "saudi": 12.00,
            "uk": 18.00,
            "usa": 20.00,
            "germany": 16.00,
            "france": 16.00,
            "spain": 16.00,
            "italy": 16.00
        };

        // Global discount
        var globalDiscount = 0;

        // Shopping cart
        var cart = [];

        // Orders
        var orders = [];

        // Admin credentials
        var adminCredentials = {
            username: "He@lixcare786",
            password: "Abdull@H1122"
        };

        // Current language
        var currentLang = 'en';
        var editingProductId = null;
        var isAdminLoggedIn = false;

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
        var adminLoginForm = document.getElementById('admin-login-form');
        var adminLogoutBtn = document.getElementById('admin-logout');
        var productForm = document.getElementById('product-form');
        var categoryForm = document.getElementById('category-form');
        var shippingForm = document.getElementById('shipping-form');
        var cancelEditBtn = document.getElementById('cancel-edit');
        var adminProductsList = document.getElementById('admin-products-list');
        var adminCategoriesList = document.getElementById('admin-categories-list');
        var adminShippingList = document.getElementById('admin-shipping-list');
        var adminOrdersList = document.getElementById('admin-orders-list');
        var productImageInput = document.getElementById('product-image');
        var imagePreview = document.getElementById('image-preview');
        var previewImg = document.getElementById('preview-img');
        var deliveryChargeInput = document.getElementById('delivery-charge');
        var productCategorySelect = document.getElementById('product-category');
        var adminTabs = document.querySelectorAll('.admin-tab');
        var adminTabContents = document.querySelectorAll('.admin-tab-content');
        var productSubmitBtn = document.getElementById('product-submit-btn');
        var globalDiscountInput = document.getElementById('global-discount');
        var applyGlobalDiscountBtn = document.getElementById('apply-global-discount');

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            // Load products
            renderFeaturedProducts();
            renderAllProducts();
            renderAdminProducts();
            renderCategories();
            renderShippingRates();
            renderOrders();
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
                    
                    // Special handling for admin page
                    if (page === 'admin' && !isAdminLoggedIn) {
                        navigateToPage('admin-login');
                    } else {
                        navigateToPage(page);
                    }
                });
            });
            
            // Set up admin tabs
            adminTabs.forEach(function(tab) {
                tab.addEventListener('click', function() {
                    var tabId = this.getAttribute('data-tab');
                    
                    // Remove active class from all tabs and contents
                    adminTabs.forEach(function(t) {
                        t.classList.remove('active');
                    });
                    adminTabContents.forEach(function(content) {
                        content.classList.remove('active');
                    });
                    
                    // Add active class to clicked tab and corresponding content
                    this.classList.add('active');
                    document.getElementById(tabId + '-tab').classList.add('active');
                });
            });
            
            // Set up product form submission
            productForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                var productData = {
                    name: document.getElementById('product-name').value,
                    description: document.getElementById('product-description').value,
                    price: parseFloat(document.getElementById('product-price').value),
                    discount: parseInt(document.getElementById('product-discount').value),
                    image: previewImg.src,
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
                imagePreview.style.display = 'none';
                productSubmitBtn.textContent = translations[currentLang].addProduct;
            });
            
            // Set up category form submission
            categoryForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                var categoryData = {
                    name: document.getElementById('category-name').value,
                    description: document.getElementById('category-description').value
                };
                
                addCategory(categoryData);
                categoryForm.reset();
            });
            
            // Set up shipping form submission
            shippingForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                var country = document.getElementById('shipping-country').value;
                var charge = parseFloat(document.getElementById('shipping-charge').value);
                
                setShippingRate(country, charge);
                shippingForm.reset();
            });
            
            // Set up global discount
            applyGlobalDiscountBtn.addEventListener('click', function() {
                globalDiscount = parseInt(globalDiscountInput.value);
                alert('Global discount applied successfully!');
                renderFeaturedProducts();
                renderAllProducts();
                updateCartUI();
            });
            
            // Set up cancel edit button
            cancelEditBtn.addEventListener('click', function() {
                productForm.reset();
                this.style.display = 'none';
                editingProductId = null;
                imagePreview.style.display = 'none';
                productSubmitBtn.textContent = translations[currentLang].addProduct;
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
                
                // Collect customer data
                var customerData = {
                    firstName: document.getElementById('checkout-firstname').value,
                    lastName: document.getElementById('checkout-lastname').value,
                    email: document.getElementById('checkout-email').value,
                    phone: document.getElementById('checkout-phone').value,
                    address: document.getElementById('checkout-address').value,
                    city: document.getElementById('checkout-city').value,
                    region: document.getElementById('checkout-region').value,
                    zipCode: document.getElementById('checkout-zip').value,
                    country: document.getElementById('checkout-country').value,
                    instructions: document.getElementById('delivery-instructions').value,
                    subscribe: document.getElementById('subscribe-email').checked
                };
                
                // Create order
                var orderId = 'ORD' + Date.now();
                var order = {
                    id: orderId,
                    customer: customerData,
                    items: [...cart],
                    total: calculateCartTotal(),
                    date: new Date().toISOString(),
                    status: 'pending'
                };
                
                // Add to orders
                orders.push(order);
                renderOrders();
                
                // Send email notifications
                sendOrderEmail(order);
                
                alert('Thank you for your order! Your order has been placed successfully. Order ID: ' + orderId);
                
                // Clear cart
                cart = [];
                updateCartUI();
                navigateToPage('home');
                
                // Reset form
                checkoutForm.reset();
            });
            
            // Set up admin login form
            adminLoginForm.addEventListener('submit', function(e) {
                e.preventDefault();
                var username = document.getElementById('admin-username').value;
                var password = document.getElementById('admin-password').value;
                
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
            
            // Set up image preview
            productImageInput.addEventListener('change', function() {
                if (this.files && this.files[0]) {
                    var reader = new FileReader();
                    
                    reader.onload = function(e) {
                        previewImg.src = e.target.result;
                        imagePreview.style.display = 'block';
                    }
                    
                    reader.readAsDataURL(this.files[0]);
                }
            });
            
            // Set up delivery charge change (readonly for customers)
            deliveryChargeInput.addEventListener('change', function() {
                updateCartUI();
            });
            
            // Initialize parallax effect
            initParallax();
        });

        // Initialize parallax effect
        function initParallax() {
            var parallaxBg = document.getElementById('parallax-bg');
            
            window.addEventListener('mousemove', function(e) {
                var x = e.clientX / window.innerWidth;
                var y = e.clientY / window.innerHeight;
                
                parallaxBg.style.transform = 'translate(-' + x * 20 + 'px, -' + y * 20 + 'px)';
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
            
            var finalPrice = product.price;
            var discountAmount = 0;
            
            // Apply global discount first
            if (globalDiscount > 0) {
                discountAmount = product.price * (globalDiscount / 100);
                finalPrice = product.price - discountAmount;
            }
            
            // Apply product-specific discount
            if (product.discount > 0) {
                discountAmount = product.price * (product.discount / 100);
                finalPrice = product.price - discountAmount;
            }
            
            var priceHtml = '';
            if (discountAmount > 0) {
                var totalDiscount = globalDiscount + product.discount;
                priceHtml = 
                    '<div class="product-price">' +
                        '<div>' +
                            '<span class="original-price">$' + product.price.toFixed(2) + '</span>' +
                            '<span class="price">$' + finalPrice.toFixed(2) + '</span>' +
                            '<span class="discount-badge">-' + totalDiscount + '%</span>' +
                        '</div>' +
                        '<button class="btn add-to-cart-btn" data-id="' + product.id + '" data-key="addToCart">Add to Cart</button>' +
                    '</div>';
            } else {
                priceHtml = 
                    '<div class="product-price">' +
                        '<span class="price">$' + finalPrice.toFixed(2) + '</span>' +
                        '<button class="btn add-to-cart-btn" data-id="' + product.id + '" data-key="addToCart">Add to Cart</button>' +
                    '</div>';
            }
            
            productCard.innerHTML = 
                '<div class="product-image">' +
                    '<img src="' + product.image + '" alt="' + product.name + '">' +
                '</div>' +
                '<div class="product-info">' +
                    '<h3>' + product.name + '</h3>' +
                    '<p>' + product.description + '</p>' +
                    priceHtml +
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
                        discount: product.discount,
                        image: product.image,
                        quantity: 1
                    });
                }
                
                updateCartUI();
                alert('Product added to cart!');
            }
        }

        // Calculate cart total
        function calculateCartTotal() {
            var subtotal = cart.reduce(function(total, item) {
                var itemPrice = item.price;
                var discountAmount = 0;
                
                // Apply global discount
                if (globalDiscount > 0) {
                    discountAmount = item.price * (globalDiscount / 100);
                    itemPrice = item.price - discountAmount;
                }
                
                // Apply product-specific discount
                if (item.discount > 0) {
                    discountAmount = item.price * (item.discount / 100);
                    itemPrice = item.price - discountAmount;
                }
                
                return total + (itemPrice * item.quantity);
            }, 0);
            
            var shipping = parseFloat(deliveryChargeInput.value) || 5.00;
            return subtotal + shipping;
        }

        // Update cart UI
        function updateCartUI() {
            // Update cart count
            var totalItems = cart.reduce(function(total, item) {
                return total + item.quantity;
            }, 0);
            cartCount.textContent = totalItems;
            
            // Get delivery charge
            var deliveryCharge = parseFloat(deliveryChargeInput.value) || 5.00;
            
            // Update cart totals
            var subtotal = cart.reduce(function(total, item) {
                var itemPrice = item.price;
                var discountAmount = 0;
                
                // Apply global discount
                if (globalDiscount > 0) {
                    discountAmount = item.price * (globalDiscount / 100);
                    itemPrice = item.price - discountAmount;
                }
                
                // Apply product-specific discount
                if (item.discount > 0) {
                    discountAmount = item.price * (item.discount / 100);
                    itemPrice = item.price - discountAmount;
                }
                
                return total + (itemPrice * item.quantity);
            }, 0);
            
            var totalDiscount = cart.reduce(function(total, item) {
                var discountAmount = 0;
                
                // Apply global discount
                if (globalDiscount > 0) {
                    discountAmount += item.price * (globalDiscount / 100) * item.quantity;
                }
                
                // Apply product-specific discount
                if (item.discount > 0) {
                    discountAmount += item.price * (item.discount / 100) * item.quantity;
                }
                
                return total + discountAmount;
            }, 0);
            
            var total = subtotal + deliveryCharge;
            
            document.getElementById('cart-subtotal').textContent = '$' + subtotal.toFixed(2);
            document.getElementById('cart-shipping').textContent = '$' + deliveryCharge.toFixed(2);
            document.getElementById('cart-discount').textContent = '-$' + totalDiscount.toFixed(2);
            document.getElementById('cart-total').textContent = '$' + total.toFixed(2);
            
            // Update checkout totals
            document.getElementById('checkout-subtotal').textContent = '$' + subtotal.toFixed(2);
            document.getElementById('checkout-shipping').textContent = '$' + deliveryCharge.toFixed(2);
            document.getElementById('checkout-discount').textContent = '-$' + totalDiscount.toFixed(2);
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
                var itemPrice = item.price;
                var discountAmount = 0;
                
                // Apply global discount
                if (globalDiscount > 0) {
                    discountAmount = item.price * (globalDiscount / 100);
                    itemPrice = item.price - discountAmount;
                }
                
                // Apply product-specific discount
                if (item.discount > 0) {
                    discountAmount = item.price * (item.discount / 100);
                    itemPrice = item.price - discountAmount;
                }
                
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
                            '<span class="price">$' + (itemPrice * item.quantity).toFixed(2) + '</span>' +
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
                var itemPrice = item.price;
                var discountAmount = 0;
                
                // Apply global discount
                if (globalDiscount > 0) {
                    discountAmount = item.price * (globalDiscount / 100);
                    itemPrice = item.price - discountAmount;
                }
                
                // Apply product-specific discount
                if (item.discount > 0) {
                    discountAmount = item.price * (item.discount / 100);
                    itemPrice = item.price - discountAmount;
                }
                
                var checkoutItem = document.createElement('div');
                checkoutItem.className = 'checkout-item';
                checkoutItem.innerHTML = 
                    '<div class="checkout-item-image">' +
                        '<img src="' + item.image + '" alt="' + item.name + '">' +
                    '</div>' +
                    '<div class="checkout-item-details">' +
                        '<h4>' + item.name + '</h4>' +
                        '<p data-key="quantity">Quantity: ' + item.quantity + '</p>' +
                        '<p>$' + (itemPrice * item.quantity).toFixed(2) + '</p>' +
                    '</div>';
                checkoutItemsContainer.appendChild(checkoutItem);
            });
            
            // Update language
            updateLanguage();
        }

        // Render categories in admin panel
        function renderCategories() {
            // Populate category select in product form
            productCategorySelect.innerHTML = '';
            categories.forEach(function(category) {
                var option = document.createElement('option');
                option.value = category.id;
                option.textContent = category.name;
                productCategorySelect.appendChild(option);
            });
            
            // Render categories list
            adminCategoriesList.innerHTML = '';
            categories.forEach(function(category) {
                var categoryItem = document.createElement('div');
                categoryItem.className = 'category-item';
                categoryItem.innerHTML = 
                    '<div>' +
                        '<h4>' + category.name + '</h4>' +
                        '<p>' + category.description + '</p>' +
                    '</div>' +
                    '<div>' +
                        '<button class="btn btn-danger delete-category" data-id="' + category.id + '">Delete</button>' +
                    '</div>';
                adminCategoriesList.appendChild(categoryItem);
            });
            
            // Add event listeners to delete category buttons
            document.querySelectorAll('.delete-category').forEach(function(button) {
                button.addEventListener('click', function() {
                    var categoryId = this.getAttribute('data-id');
                    deleteCategory(categoryId);
                });
            });
            
            // Update language
            updateLanguage();
        }

        // Render shipping rates in admin panel
        function renderShippingRates() {
            adminShippingList.innerHTML = '';
            
            for (var country in shippingRates) {
                var shippingRate = document.createElement('div');
                shippingRate.className = 'shipping-rate';
                shippingRate.innerHTML = 
                    '<div>' +
                        '<h4>' + country.charAt(0).toUpperCase() + country.slice(1) + '</h4>' +
                    '</div>' +
                    '<div>' +
                        '<span>$' + shippingRates[country].toFixed(2) + '</span>' +
                    '</div>';
                adminShippingList.appendChild(shippingRate);
            }
        }

        // Render orders in admin panel
        function renderOrders() {
            adminOrdersList.innerHTML = '';
            
            if (orders.length === 0) {
                adminOrdersList.innerHTML = '<p data-key="noOrders">No orders placed yet</p>';
                return;
            }
            
            orders.forEach(function(order) {
                var orderItem = document.createElement('div');
                orderItem.className = 'category-item';
                orderItem.innerHTML = 
                    '<div>' +
                        '<h4>Order #' + order.id + '</h4>' +
                        '<p><strong>Customer:</strong> ' + order.customer.firstName + ' ' + order.customer.lastName + '</p>' +
                        '<p><strong>Email:</strong> ' + order.customer.email + '</p>' +
                        '<p><strong>Total:</strong> $' + order.total.toFixed(2) + '</p>' +
                        '<p><strong>Date:</strong> ' + new Date(order.date).toLocaleDateString() + '</p>' +
                        '<p><strong>Status:</strong> ' + order.status + '</p>' +
                    '</div>' +
                    '<div>' +
                        '<button class="btn view-order" data-id="' + order.id + '">View Details</button>' +
                    '</div>';
                adminOrdersList.appendChild(orderItem);
            });
            
            // Add event listeners to view order buttons
            document.querySelectorAll('.view-order').forEach(function(button) {
                button.addEventListener('click', function() {
                    var orderId = this.getAttribute('data-id');
                    viewOrderDetails(orderId);
                });
            });
            
            // Update language
            updateLanguage();
        }

        // View order details
        function viewOrderDetails(orderId) {
            var order = orders.find(function(o) {
                return o.id === orderId;
            });
            
            if (order) {
                var details = 'Order #' + order.id + '\n\n';
                details += 'Customer Information:\n';
                details += 'Name: ' + order.customer.firstName + ' ' + order.customer.lastName + '\n';
                details += 'Email: ' + order.customer.email + '\n';
                details += 'Phone: ' + order.customer.phone + '\n\n';
                details += 'Shipping Address:\n';
                details += order.customer.address + '\n';
                details += order.customer.city + ', ' + order.customer.region + ' ' + order.customer.zipCode + '\n';
                details += order.customer.country + '\n\n';
                details += 'Order Items:\n';
                order.items.forEach(function(item) {
                    details += '- ' + item.name + ' x' + item.quantity + ' - $' + (item.price * item.quantity).toFixed(2) + '\n';
                });
                details += '\nTotal: $' + order.total.toFixed(2);
                
                alert(details);
            }
        }

        // Render products in admin panel
        function renderAdminProducts() {
            adminProductsList.innerHTML = '';
            
            products.forEach(function(product) {
                var productItem = document.createElement('div');
                productItem.className = 'admin-product-item';
                productItem.style.cssText = 
                    'display: flex; justify-content: space-between; align-items: center; ' +
                    'padding: 15px; border: 1px solid rgba(212, 175, 55, 0.2); ' +
                    'border-radius: 8px; margin-bottom: 10px; ' +
                    'background: rgba(18, 18, 18, 0.5);';
                productItem.innerHTML = 
                    '<div>' +
                        '<h4>' + product.name + '</h4>' +
                        '<p>$' + product.price.toFixed(2) + ' | Discount: ' + product.discount + '% | Category: ' + product.category + '</p>' +
                    '</div>' +
                    '<div>' +
                        '<button class="btn edit-product" data-id="' + product.id + '">Edit</button>' +
                        '<button class="btn btn-danger delete-product" data-id="' + product.id + '">Delete</button>' +
                    '</div>';
                adminProductsList.appendChild(productItem);
            });
            
            // Add event listeners to edit and delete buttons
            document.querySelectorAll('.edit-product').forEach(function(button) {
                button.addEventListener('click', function() {
                    var productId = parseInt(this.getAttribute('data-id'));
                    editProduct(productId);
                });
            });
            
            document.querySelectorAll('.delete-product').forEach(function(button) {
                button.addEventListener('click', function() {
                    var productId = parseInt(this.getAttribute('data-id'));
                    deleteProduct(productId);
                });
            });
            
            // Update language for buttons
            updateLanguage();
        }

        // Add a new product
        function addProduct(productData) {
            var newProduct = {
                id: products.length > 0 ? Math.max.apply(null, products.map(function(p) { return p.id; })) + 1 : 1,
                name: productData.name,
                description: productData.description,
                price: productData.price,
                discount: productData.discount,
                image: productData.image,
                category: productData.category,
                featured: productData.featured
            };
            
            products.push(newProduct);
            renderFeaturedProducts();
            renderAllProducts();
            renderAdminProducts();
            alert('Product added successfully!');
        }

        // Edit a product
        function editProduct(productId) {
            var product = products.find(function(p) {
                return p.id === productId;
            });
            if (product) {
                document.getElementById('product-name').value = product.name;
                document.getElementById('product-description').value = product.description;
                document.getElementById('product-price').value = product.price;
                document.getElementById('product-discount').value = product.discount;
                document.getElementById('product-category').value = product.category;
                document.getElementById('product-featured').checked = product.featured;
                
                previewImg.src = product.image;
                imagePreview.style.display = 'block';
                
                editingProductId = productId;
                cancelEditBtn.style.display = 'inline-block';
                productSubmitBtn.textContent = translations[currentLang].updateProduct;
            }
        }

        // Update a product
        function updateProduct(productId, productData) {
            var productIndex = products.findIndex(function(p) {
                return p.id === productId;
            });
            if (productIndex !== -1) {
                products[productIndex] = { 
                    id: productId,
                    name: productData.name,
                    description: productData.description,
                    price: productData.price,
                    discount: productData.discount,
                    image: productData.image,
                    category: productData.category,
                    featured: productData.featured
                };
                renderFeaturedProducts();
                renderAllProducts();
                renderAdminProducts();
                alert('Product updated successfully!');
            }
        }

        // Delete a product
        function deleteProduct(productId) {
            if (confirm('Are you sure you want to delete this product?')) {
                products = products.filter(function(p) {
                    return p.id !== productId;
                });
                renderFeaturedProducts();
                renderAllProducts();
                renderAdminProducts();
                alert('Product deleted successfully!');
            }
        }

        // Add a new category
        function addCategory(categoryData) {
            var newCategory = {
                id: categoryData.name.toLowerCase().replace(/\s+/g, '-'),
                name: categoryData.name,
                description: categoryData.description
            };
            
            categories.push(newCategory);
            renderCategories();
            alert('Category added successfully!');
        }

        // Delete a category
        function deleteCategory(categoryId) {
            if (confirm('Are you sure you want to delete this category? Products in this category will be moved to "Other".')) {
                // Move products to "Other" category
                products.forEach(function(product) {
                    if (product.category === categoryId) {
                        product.category = 'other';
                    }
                });
                
                categories = categories.filter(function(c) {
                    return c.id !== categoryId;
                });
                
                renderCategories();
                renderAdminProducts();
                renderFeaturedProducts();
                renderAllProducts();
                alert('Category deleted successfully!');
            }
        }

        // Set shipping rate
        function setShippingRate(country, charge) {
            shippingRates[country] = charge;
            renderShippingRates();
            
            // Update delivery charge input if the current country matches
            var currentCountry = document.getElementById('checkout-country').value;
            if (currentCountry === country) {
                deliveryChargeInput.value = charge.toFixed(2);
                updateCartUI();
            }
            
            alert('Shipping rate for ' + country + ' set to $' + charge.toFixed(2));
        }

        // Send order email
        function sendOrderEmail(order) {
            var customerEmail = order.customer.email;
            var storeEmail = 'healixcare786@gmail.com';
            
            // Customer email content
            var customerSubject = 'Order Confirmation - Healix Care';
            var customerBody = 
                'Dear ' + order.customer.firstName + ' ' + order.customer.lastName + ',\n\n' +
                'Thank you for your order! Your order has been received and is being processed.\n\n' +
                'Order Details:\n' +
                'Order ID: ' + order.id + '\n' +
                'Total Amount: $' + order.total.toFixed(2) + '\n\n' +
                'Shipping Address:\n' +
                order.customer.address + '\n' +
                order.customer.city + ', ' + order.customer.region + ' ' + order.customer.zipCode + '\n' +
                order.customer.country + '\n\n' +
                'We will send you shipping confirmation once your order is on its way!\n\n' +
                'Best regards,\nHealix Care Team';
            
            // Store email content
            var storeSubject = 'New Order Received - ' + order.id;
            var storeBody = 
                'New Order Received!\n\n' +
                'Order ID: ' + order.id + '\n' +
                'Customer: ' + order.customer.firstName + ' ' + order.customer.lastName + '\n' +
                'Email: ' + order.customer.email + '\n' +
                'Phone: ' + order.customer.phone + '\n\n' +
                'Shipping Address:\n' +
                order.customer.address + '\n' +
                order.customer.city + ', ' + order.customer.region + ' ' + order.customer.zipCode + '\n' +
                order.customer.country + '\n\n' +
                'Order Items:\n';
            
            order.items.forEach(function(item) {
                storeBody += '- ' + item.name + ' x' + item.quantity + ' - $' + (item.price * item.quantity).toFixed(2) + '\n';
            });
            
            storeBody += '\nOrder Total: $' + order.total.toFixed(2);
            
            // In a real application, you would send these emails using a server-side service
            // For this demo, we'll just log them to the console
            console.log('Sending email to customer:', customerEmail);
            console.log('Subject:', customerSubject);
            console.log('Body:', customerBody);
            
            console.log('Sending email to store:', storeEmail);
            console.log('Subject:', storeSubject);
            console.log('Body:', storeBody);
            
            // Subscribe customer to newsletter if they opted in
            if (order.customer.subscribe) {
                console.log('Subscribing customer to newsletter:', customerEmail);
            }
            
            alert('Order confirmation emails have been sent!');
        }
    </script>
</body>
</html>
