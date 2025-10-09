<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TECHIZO - Premium Mobile Accessories</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary: #121212;
            --secondary: #FF5722;
            --accent: #D4AF37;
            --light: #1E1E1E;
            --dark: #0A0A0A;
            --success: #4CAF50;
            --danger: #F44336;
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
        
        /* RTL Support */
        body[dir="rtl"] {
            direction: rtl;
            text-align: right;
        }
        
        body[dir="rtl"] .header-content,
        body[dir="rtl"] .footer-content,
        body[dir="rtl"] .contact-container,
        body[dir="rtl"] .robot-container,
        body[dir="rtl"] .slide {
            direction: rtl;
        }
        
        body[dir="rtl"] .logo-img {
            margin-right: 0;
            margin-left: 12px;
        }
        
        body[dir="rtl"] nav ul li {
            margin-left: 0;
            margin-right: 20px;
        }
        
        body[dir="rtl"] .cart-icon .cart-count {
            right: auto;
            left: -8px;
        }
        
        body[dir="rtl"] .language-selector {
            margin-left: 0;
            margin-right: 20px;
        }
        
        body[dir="rtl"] .language-selector select {
            margin-left: 0;
            margin-right: 10px;
        }
        
        body[dir="rtl"] .section-title h2::after {
            left: auto;
            right: 50%;
            transform: translateX(50%);
        }
        
        body[dir="rtl"] .contact-icon {
            margin-right: 0;
            margin-left: 20px;
        }
        
        body[dir="rtl"] .whatsapp-help {
            right: auto;
            left: 20px;
        }
        
        body[dir="rtl"] .robot-info {
            padding: 0 0 0 40px;
        }
        
        body[dir="rtl"] .slide-content {
            padding-right: 0;
            padding-left: 40px;
        }
        
        body[dir="rtl"] .cart-item-image {
            margin-right: 0;
            margin-left: 20px;
        }
        
        body[dir="rtl"] .footer-column h3::after {
            left: auto;
            right: 0;
        }
        
        body[dir="rtl"] .social-links-contact a,
        body[dir="rtl"] .social-links a {
            margin-right: 0;
            margin-left: 15px;
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
        
        .btn-success {
            background: linear-gradient(135deg, var(--success) 0%, #2E7D32 100%);
            box-shadow: 0 4px 15px rgba(76, 175, 80, 0.3);
        }
        
        .btn-success:hover {
            box-shadow: 0 8px 25px rgba(76, 175, 80, 0.5);
        }
        
        .btn-danger {
            background: linear-gradient(135deg, var(--danger) 0%, #C62828 100%);
            box-shadow: 0 4px 15px rgba(244, 67, 54, 0.3);
        }
        
        .btn-danger:hover {
            box-shadow: 0 8px 25px rgba(244, 67, 54, 0.5);
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
            flex-direction: column;
            align-items: center;
            position: relative;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
            margin-bottom: 15px;
        }
        
        .logo-text {
            font-size: 36px;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
            display: flex;
            align-items: center;
        }
        
        .power-button {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--accent) 0%, #B8860B 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-left: 5px;
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.5);
            animation: pulse 2s infinite;
            position: relative;
            overflow: hidden;
        }
        
        .power-button::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: 0.5s;
        }
        
        .power-button:hover::before {
            left: 100%;
        }
        
        .power-button i {
            color: white;
            font-size: 20px;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 10px rgba(212, 175, 55, 0.5); }
            50% { box-shadow: 0 0 20px rgba(212, 175, 55, 0.8); }
            100% { box-shadow: 0 0 10px rgba(212, 175, 55, 0.5); }
        }
        
        nav ul {
            display: flex;
            list-style: none;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        nav ul li {
            margin: 0 15px;
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
        
        /* Language Selector - Below Header */
        .language-selector {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-top: 15px;
            background: rgba(30, 30, 30, 0.8);
            padding: 8px 15px;
            border-radius: 20px;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }
        
        .language-selector span {
            font-size: 14px;
            color: var(--text-secondary);
            margin-right: 10px;
        }
        
        .language-selector select {
            padding: 5px 10px;
            border-radius: 6px;
            border: 1px solid rgba(212, 175, 55, 0.3);
            background: rgba(30, 30, 30, 0.8);
            color: var(--text);
            font-size: 14px;
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
        
        /* Robot Animation Section */
        .robot-section {
            position: relative;
            padding: 80px 0;
            background: linear-gradient(135deg, rgba(30,30,30,0.9) 0%, rgba(10,10,10,0.9) 100%);
            overflow: hidden;
            border-top: 1px solid rgba(212, 175, 55, 0.1);
            border-bottom: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .robot-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .robot-animation {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            height: 400px;
        }
        
        .robot {
            position: relative;
            width: 180px;
            height: 280px;
            transform-style: preserve-3d;
            animation: robotFloat 4s ease-in-out infinite;
        }
        
        @keyframes robotFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
        }
        
        .robot-head {
            position: absolute;
            width: 120px;
            height: 100px;
            background: linear-gradient(135deg, #4A4A4A, #2A2A2A);
            border-radius: 50% 50% 40% 40%;
            top: 0;
            left: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.5);
            overflow: hidden;
            z-index: 10;
        }
        
        .robot-face {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .robot-eyes {
            display: flex;
            justify-content: space-between;
            width: 70px;
            margin-top: 20px;
        }
        
        .robot-eye {
            width: 20px;
            height: 20px;
            background: linear-gradient(135deg, #00FFFF, #0080FF);
            border-radius: 50%;
            position: relative;
            animation: eyeBlink 5s infinite;
        }
        
        @keyframes eyeBlink {
            0%, 90%, 100% { transform: scaleY(1); }
            95% { transform: scaleY(0.1); }
        }
        
        .robot-eye::after {
            content: '';
            position: absolute;
            width: 8px;
            height: 8px;
            background: white;
            border-radius: 50%;
            top: 3px;
            left: 3px;
        }
        
        .robot-mouth {
            width: 40px;
            height: 10px;
            background: linear-gradient(135deg, #FF5252, #B71C1C);
            border-radius: 10px;
            margin-top: 15px;
            animation: mouthTalk 3s infinite;
        }
        
        @keyframes mouthTalk {
            0%, 50%, 100% { height: 10px; }
            25%, 75% { height: 5px; }
        }
        
        .robot-body {
            position: absolute;
            width: 140px;
            height: 140px;
            background: linear-gradient(135deg, #5A5A5A, #3A3A3A);
            border-radius: 20px;
            top: 80px;
            left: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.5);
            z-index: 5;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .robot-screen {
            width: 80px;
            height: 60px;
            background: linear-gradient(135deg, #1E88E5, #0D47A1);
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 10px;
            text-align: center;
            padding: 5px;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.5);
            animation: screenGlow 3s infinite alternate;
        }
        
        @keyframes screenGlow {
            0% { box-shadow: inset 0 0 10px rgba(0,0,0,0.5), 0 0 10px rgba(30, 136, 229, 0.5); }
            100% { box-shadow: inset 0 0 10px rgba(0,0,0,0.5), 0 0 20px rgba(30, 136, 229, 0.8); }
        }
        
        .robot-arms {
            position: absolute;
            width: 100%;
            height: 100px;
            top: 120px;
            display: flex;
            justify-content: space-between;
        }
        
        .robot-arm {
            width: 20px;
            height: 100px;
            background: linear-gradient(135deg, #4A4A4A, #2A2A2A);
            border-radius: 10px;
            position: relative;
        }
        
        .robot-arm.left {
            left: -10px;
            transform-origin: top center;
            animation: leftArmMove 4s infinite;
        }
        
        .robot-arm.right {
            right: -10px;
            transform-origin: top center;
            animation: rightArmMove 4s infinite;
        }
        
        @keyframes leftArmMove {
            0%, 100% { transform: rotate(0deg); }
            50% { transform: rotate(-30deg); }
        }
        
        @keyframes rightArmMove {
            0%, 100% { transform: rotate(0deg); }
            50% { transform: rotate(30deg); }
        }
        
        .robot-legs {
            position: absolute;
            width: 100%;
            height: 80px;
            top: 220px;
            display: flex;
            justify-content: space-between;
            padding: 0 40px;
        }
        
        .robot-leg {
            width: 25px;
            height: 80px;
            background: linear-gradient(135deg, #4A4A4A, #2A2A2A);
            border-radius: 10px;
            position: relative;
        }
        
        .robot-leg.left {
            transform-origin: top center;
            animation: leftLegMove 2s infinite;
        }
        
        .robot-leg.right {
            transform-origin: top center;
            animation: rightLegMove 2s infinite 1s;
        }
        
        @keyframes leftLegMove {
            0%, 100% { transform: rotate(0deg); }
            50% { transform: rotate(15deg); }
        }
        
        @keyframes rightLegMove {
            0%, 100% { transform: rotate(0deg); }
            50% { transform: rotate(-15deg); }
        }
        
        .robot-info {
            flex: 1;
            padding: 0 40px;
        }
        
        .robot-info h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        
        .robot-info p {
            font-size: 1.1rem;
            line-height: 1.7;
            margin-bottom: 25px;
            color: var(--text-secondary);
        }
        
        /* Product Slider Section */
        .slider-section {
            padding: 80px 0;
            background: linear-gradient(135deg, rgba(18,18,18,0.9) 0%, rgba(10,10,10,0.9) 100%);
        }
        
        .slider-container {
            position: relative;
            max-width: 1200px;
            margin: 0 auto;
            overflow: hidden;
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.4);
            border: 1px solid rgba(212, 175, 55, 0.2);
        }
        
        .slider {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }
        
        .slide {
            min-width: 100%;
            padding: 40px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: linear-gradient(135deg, rgba(30,30,30,0.9) 0%, rgba(18,18,18,0.9) 100%);
        }
        
        .slide-content {
            flex: 1;
            padding-right: 40px;
        }
        
        .slide-content h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .slide-content p {
            font-size: 1.1rem;
            line-height: 1.7;
            margin-bottom: 25px;
            color: var(--text-secondary);
        }
        
        .slide-image {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .slide-image img {
            max-width: 100%;
            max-height: 400px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            transition: transform 0.5s;
        }
        
        .slide-image img:hover {
            transform: scale(1.05);
        }
        
        .slider-controls {
            position: absolute;
            bottom: 20px;
            left: 0;
            right: 0;
            display: flex;
            justify-content: center;
            gap: 10px;
        }
        
        .slider-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: rgba(255,255,255,0.3);
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .slider-dot.active {
            background: var(--accent);
            transform: scale(1.2);
        }
        
        .slider-arrow {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 50px;
            height: 50px;
            background: rgba(30,30,30,0.8);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            color: white;
            font-size: 24px;
            transition: all 0.3s;
            z-index: 10;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }
        
        .slider-arrow:hover {
            background: rgba(212, 175, 55, 0.2);
            transform: translateY(-50%) scale(1.1);
        }
        
        .slider-arrow.prev {
            left: 20px;
        }
        
        .slider-arrow.next {
            right: 20px;
        }
        
        /* Featured Products */
        .products-section {
            padding: 80px 0;
        }
        
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
            position: relative;
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
        
        /* IMPROVED ADD TO CART BUTTON */
        .add-to-cart-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            padding: 10px 16px;
            background: linear-gradient(135deg, var(--secondary) 0%, #E64A19 100%);
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(255, 87, 34, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .add-to-cart-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: 0.5s;
        }
        
        .add-to-cart-btn:hover::before {
            left: 100%;
        }
        
        .add-to-cart-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(255, 87, 34, 0.4);
        }
        
        .add-to-cart-btn:active {
            transform: translateY(0);
        }
        
        .add-to-cart-btn.added {
            background: linear-gradient(135deg, var(--success) 0%, #2E7D32 100%);
            box-shadow: 0 4px 10px rgba(76, 175, 80, 0.3);
        }
        
        .add-to-cart-btn.added::after {
            content: '✓ Added';
        }
        
        .add-to-cart-btn.added .btn-text {
            display: none;
        }
        
        .add-to-cart-btn i {
            font-size: 14px;
        }
        
        /* Cart notification */
        .cart-notification {
            position: fixed;
            top: 100px;
            right: 20px;
            background: linear-gradient(135deg, var(--success) 0%, #2E7D32 100%);
            color: white;
            padding: 15px 20px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            z-index: 1001;
            display: flex;
            align-items: center;
            gap: 10px;
            transform: translateX(150%);
            transition: transform 0.4s ease;
        }
        
        .cart-notification.show {
            transform: translateX(0);
        }
        
        .cart-notification i {
            font-size: 20px;
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
        
        /* Contact Page Specific Styles */
        .contact-page {
            padding: 80px 0;
            background: linear-gradient(135deg, rgba(18,18,18,0.95) 0%, rgba(10,10,10,0.95) 100%);
            min-height: 80vh;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .contact-info {
            padding: 40px;
            background: rgba(30, 30, 30, 0.7);
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
            border: 1px solid rgba(255, 152, 0, 0.2);
            backdrop-filter: blur(10px);
            height: fit-content;
        }
        
        .contact-info h3 {
            font-size: 2rem;
            margin-bottom: 30px;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(0,0,0,0.3);
            position: relative;
            padding-bottom: 15px;
        }
        
        .contact-info h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 3px;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
            border-radius: 3px;
        }
        
        .contact-details {
            margin-bottom: 30px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
            padding: 15px;
            border-radius: 12px;
            transition: all 0.3s ease;
            background: rgba(10, 10, 10, 0.5);
            border: 1px solid rgba(255,255,255,0.05);
        }
        
        .contact-item:hover {
            background: rgba(30, 30, 30, 0.9);
            transform: translateX(10px);
            border-color: rgba(255, 152, 0, 0.3);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--secondary) 0%, #E65100 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 20px;
            box-shadow: 0 5px 15px rgba(255, 152, 0, 0.3);
        }
        
        .contact-icon.light {
            background: linear-gradient(135deg, var(--accent) 0%, #FF9800 100%);
            box-shadow: 0 5px 15px rgba(255, 183, 77, 0.3);
        }
        
        .contact-icon i {
            font-size: 20px;
            color: white;
        }
        
        .contact-text h4 {
            font-size: 16px;
            margin-bottom: 5px;
            color: var(--accent);
        }
        
        .contact-text p {
            color: var(--text);
            font-size: 16px;
        }
        
        .social-section {
            margin-top: 30px;
        }
        
        .social-section h4 {
            font-size: 18px;
            margin-bottom: 15px;
            color: var(--text);
        }
        
        .social-links-contact {
            display: flex;
            gap: 15px;
        }
        
        .social-links-contact a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s;
            font-size: 20px;
            text-decoration: none;
        }
        
        .social-links-contact a:hover {
            background: var(--secondary);
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(255, 152, 0, 0.4);
        }
        
        .social-links-contact a.facebook:hover {
            background: #3b5998;
        }
        
        .social-links-contact a.instagram:hover {
            background: #E1306C;
        }
        
        .social-links-contact a.whatsapp:hover {
            background: #25D366;
        }
        
        .contact-form {
            padding: 40px;
            background: rgba(30, 30, 30, 0.7);
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
            border: 1px solid rgba(255, 152, 0, 0.2);
            backdrop-filter: blur(10px);
        }
        
        .contact-form h3 {
            font-size: 2rem;
            margin-bottom: 30px;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(0,0,0,0.3);
            position: relative;
            padding-bottom: 15px;
        }
        
        .contact-form h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 3px;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
            border-radius: 3px;
        }
        
        .form-group {
            margin-bottom: 25px;
            position: relative;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--text);
            font-weight: 500;
            font-size: 16px;
        }
        
        .form-control {
            width: 100%;
            padding: 15px 20px;
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 12px;
            background: rgba(10, 10, 10, 0.5);
            color: var(--text);
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 15px rgba(255, 183, 77, 0.3);
            background: rgba(30, 30, 30, 0.8);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            display: block;
            width: 100%;
            padding: 15px;
            background: linear-gradient(135deg, var(--secondary) 0%, #E65100 100%);
            color: white;
            border: none;
            border-radius: 12px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.4s ease;
            box-shadow: 0 5px 15px rgba(255, 152, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .submit-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: 0.5s;
        }
        
        .submit-btn:hover::before {
            left: 100%;
        }
        
        .submit-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(255, 152, 0, 0.5);
        }
        
        .map-container {
            margin-top: 30px;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            height: 200px;
            background: linear-gradient(135deg, rgba(30,30,30,0.9) 0%, rgba(18,18,18,0.9) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid rgba(255, 152, 0, 0.2);
        }
        
        .map-placeholder {
            text-align: center;
            padding: 20px;
        }
        
        .map-placeholder i {
            font-size: 40px;
            color: var(--accent);
            margin-bottom: 15px;
        }
        
        .map-placeholder p {
            color: var(--text-secondary);
        }
        
        /* Cart Styles */
        .cart-container {
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .cart-item {
            display: flex;
            background: rgba(30, 30, 30, 0.7);
            border-radius: 12px;
            margin-bottom: 20px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .cart-item-image {
            width: 120px;
            height: 120px;
            margin-right: 20px;
            border-radius: 10px;
            overflow: hidden;
        }
        
        .cart-item-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .cart-item-details {
            flex: 1;
        }
        
        .cart-item-details h3 {
            font-size: 18px;
            margin-bottom: 10px;
            color: var(--text);
        }
        
        .cart-item-details p {
            color: var(--text-secondary);
            margin-bottom: 15px;
        }
        
        .cart-item-controls {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .quantity-controls {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .quantity-btn {
            width: 30px;
            height: 30px;
            background: rgba(212, 175, 55, 0.2);
            border: none;
            border-radius: 50%;
            color: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .quantity {
            font-weight: bold;
            width: 30px;
            text-align: center;
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
        
        /* Admin Portal Styles */
        .admin-header {
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
        
        .admin-header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .admin-logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        
        .admin-logo h1 {
            font-size: 26px;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }
        
        .admin-nav ul {
            display: flex;
            list-style: none;
        }
        
        .admin-nav ul li {
            margin-left: 20px;
        }
        
        .admin-nav ul li a {
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
        
        .admin-nav ul li a.active {
            color: white;
            background: rgba(212, 175, 55, 0.2);
        }
        
        /* EXIT BUTTON STYLES */
        .exit-admin-btn {
            background: linear-gradient(135deg, var(--danger) 0%, #C62828 100%);
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(244, 67, 54, 0.3);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .exit-admin-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(244, 67, 54, 0.4);
        }
        
        /* Admin Login */
        .admin-login {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 80vh;
            padding: 40px 0;
        }
        
        .login-form {
            background: rgba(30, 30, 30, 0.9);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.4);
            width: 100%;
            max-width: 450px;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }
        
        .login-form h2 {
            text-align: center;
            margin-bottom: 30px;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-size: 2rem;
        }
        
        .admin-form-group {
            margin-bottom: 20px;
        }
        
        .admin-form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--text);
        }
        
        .admin-form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 8px;
            background: rgba(10, 10, 10, 0.7);
            color: var(--text);
            font-size: 16px;
            transition: all 0.3s;
        }
        
        .admin-form-control:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 10px rgba(212, 175, 55, 0.3);
        }
        
        /* Admin Dashboard */
        .admin-dashboard {
            display: none;
            padding: 40px 0;
            min-height: 80vh;
        }
        
        .dashboard-section {
            display: none;
            padding: 30px 0;
        }
        
        .dashboard-section.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        .admin-section-title {
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
        }
        
        .admin-section-title h2 {
            font-size: 2rem;
            background: linear-gradient(45deg, var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        /* Stats Cards */
        .stats-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .stat-card {
            background: rgba(30, 30, 30, 0.7);
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 1px solid rgba(212, 175, 55, 0.1);
            text-align: center;
            transition: all 0.3s;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.4);
            border-color: rgba(212, 175, 55, 0.3);
        }
        
        .stat-card h3 {
            font-size: 2.5rem;
            color: var(--accent);
            margin-bottom: 10px;
        }
        
        .stat-card p {
            color: var(--text-secondary);
        }
        
        /* Tables */
        .table-container {
            overflow-x: auto;
            margin-bottom: 30px;
        }
        
        .admin-table {
            width: 100%;
            border-collapse: collapse;
            background: rgba(30, 30, 30, 0.7);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        
        .admin-table th, .admin-table td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }
        
        .admin-table th {
            background: rgba(212, 175, 55, 0.2);
            color: var(--accent);
            font-weight: 600;
        }
        
        .admin-table tr:last-child td {
            border-bottom: none;
        }
        
        .admin-table tr:hover {
            background: rgba(255,255,255,0.05);
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
        }
        
        .action-btn {
            padding: 6px 12px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s;
        }
        
        /* Forms */
        .admin-form {
            background: rgba(30, 30, 30, 0.7);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            margin-bottom: 30px;
            border: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .form-row {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .form-actions {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }
        
        .image-preview {
            max-width: 200px;
            max-height: 200px;
            margin-top: 15px;
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }
        
        .image-preview img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Settings */
        .settings-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .setting-card {
            background: rgba(30, 30, 30, 0.7);
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .setting-card h3 {
            margin-bottom: 20px;
            color: var(--accent);
            font-size: 1.3rem;
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
                position: static;
                margin-top: 15px;
                background: transparent;
                border: none;
                padding: 0;
            }
            
            .hero-title {
                font-size: 2.5rem;
            }
            
            .robot-container {
                flex-direction: column;
            }
            
            .robot-info {
                padding: 40px 0 0;
                text-align: center;
            }
            
            .slide {
                flex-direction: column;
                text-align: center;
            }
            
            .slide-content {
                padding-right: 0;
                margin-bottom: 30px;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            
            .contact-info, .contact-form {
                padding: 30px;
            }
            
            .admin-header-content {
                flex-direction: column;
                text-align: center;
            }
            
            .admin-nav ul {
                margin-top: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .admin-nav ul li {
                margin: 5px 10px;
            }
            
            .form-row {
                grid-template-columns: 1fr;
            }
            
            .action-buttons {
                flex-direction: column;
            }
        }
        
        @media (max-width: 576px) {
            .contact-info, .contact-form {
                padding: 20px;
            }
            
            .contact-item {
                flex-direction: column;
                text-align: center;
            }
            
            .contact-icon {
                margin-right: 0;
                margin-bottom: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Main Website -->
    <div id="main-website">
        <!-- Header -->
        <header>
            <div class="container">
                <div class="header-content">
                    <a href="#" class="logo" data-page="home">
                        <h1 class="logo-text">
                            TECHIZ<span class="power-button"><i class="fas fa-power-off"></i></span>
                        </h1>
                    </a>
                    <nav>
                        <ul>
                            <li><a class="nav-link active" data-page="home" data-key="nav.home">Home</a></li>
                            <li><a class="nav-link" data-page="products" data-key="nav.products">Products</a></li>
                            <li><a class="nav-link" data-page="about" data-key="nav.about">About</a></li>
                            <li><a class="nav-link" data-page="contact" data-key="nav.contact">Contact</a></li>
                            <li class="cart-icon">
                                <a class="nav-link" data-page="cart">
                                    <i class="fas fa-shopping-bag"></i>
                                    <span class="cart-count">0</span>
                                </a>
                            </li>
                            <li><a id="admin-access-link" data-key="nav.admin">Admin</a></li>
                        </ul>
                    </nav>
                    <div class="language-selector">
                        <span data-key="language">Language:</span>
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
                    <h1 class="hero-title" data-key="hero.title">Premium Mobile Accessories</h1>
                    <p class="hero-subtitle" data-key="hero.subtitle">Discover TECHIZO's high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional. Experience the perfect blend of protection and style.</p>
                    <a class="btn shop-now-btn" data-page="products" data-key="hero.button">Shop Now</a>
                </div>
            </div>

            <!-- Robot Animation Section -->
            <section class="robot-section">
                <div class="robot-container">
                    <div class="robot-animation">
                        <div class="robot">
                            <div class="robot-head">
                                <div class="robot-face">
                                    <div class="robot-eyes">
                                        <div class="robot-eye"></div>
                                        <div class="robot-eye"></div>
                                    </div>
                                    <div class="robot-mouth"></div>
                                </div>
                            </div>
                            <div class="robot-body">
                                <div class="robot-screen">TECHIZO</div>
                            </div>
                            <div class="robot-arms">
                                <div class="robot-arm left"></div>
                                <div class="robot-arm right"></div>
                            </div>
                            <div class="robot-legs">
                                <div class="robot-leg left"></div>
                                <div class="robot-leg right"></div>
                            </div>
                        </div>
                    </div>
                    <div class="robot-info">
                        <h2 data-key="robot.title">Meet TECHIZO Bot</h2>
                        <p data-key="robot.text1">Our friendly robot assistant is here to guide you through TECHIZO's premium collection of mobile accessories. From cutting-edge screen protectors to stylish phone cases, TECHIZO Bot ensures you find the perfect match for your device.</p>
                        <p data-key="robot.text2">With advanced technology and a passion for protection, TECHIZO Bot represents our commitment to quality and innovation in every product we offer.</p>
                        <a class="btn btn-gold explore-products-btn" data-page="products" data-key="robot.button">Explore Products</a>
                    </div>
                </div>
            </section>

            <!-- Product Slider Section -->
            <section class="slider-section">
                <div class="container">
                    <div class="section-title">
                        <h2 data-key="slider.title">Featured Collections</h2>
                    </div>
                </div>
                <div class="slider-container">
                    <div class="slider" id="product-slider">
                        <div class="slide">
                            <div class="slide-content">
                                <h2 data-key="slider.slide1.title">Ultimate Screen Protection</h2>
                                <p data-key="slider.slide1.text">Our premium tempered glass screen protectors offer 9H hardness and oleophobic coating to resist fingerprints and scratches. Designed for maximum clarity and touch sensitivity.</p>
                            </div>
                            <div class="slide-image">
                                <img src="https://images.unsplash.com/photo-1601593346740-925612772716?ixlib=rb-4.0.3&auto=format&fit=crop&w=687&q=80" alt="Screen Protectors">
                            </div>
                        </div>
                        <div class="slide">
                            <div class="slide-content">
                                <h2 data-key="slider.slide2.title">Stylish Phone Cases</h2>
                                <p data-key="slider.slide2.text">Protect your device in style with our collection of premium phone cases. From slim silicone to rugged armor cases, we have options for every lifestyle and preference.</p>
                            </div>
                            <div class="slide-image">
                                <img src="https://images.unsplash.com/photo-1556656793-08538906a9f8?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Phone Cases">
                            </div>
                        </div>
                        <div class="slide">
                            <div class="slide-content">
                                <h2 data-key="slider.slide3.title">Fast Charging Solutions</h2>
                                <p data-key="slider.slide3.text">Keep your devices powered with our high-speed charging cables and adapters. Featuring durable construction and fast charging capabilities for all your mobile needs.</p>
                            </div>
                            <div class="slide-image">
                                <img src="https://images.unsplash.com/photo-1605784407953-8fe7c72dab4d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Charging Accessories">
                            </div>
                        </div>
                    </div>
                    <div class="slider-arrow prev" id="prev-slide">&#10094;</div>
                    <div class="slider-arrow next" id="next-slide">&#10095;</div>
                    <div class="slider-controls">
                        <div class="slider-dot active" data-slide="0"></div>
                        <div class="slider-dot" data-slide="1"></div>
                        <div class="slider-dot" data-slide="2"></div>
                    </div>
                </div>
            </section>

            <!-- Featured Products -->
            <section class="products-section">
                <div class="container">
                    <div class="section-title">
                        <h2 data-key="products.featured">Featured Products</h2>
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
                    <h2 data-key="products.all">All Products</h2>
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
                    <h2 data-key="about.title">About TECHIZO</h2>
                </div>
                <div class="about-content">
                    <div class="about-text">
                        <h3 data-key="about.story">Our Story</h3>
                        <p data-key="about.story.text1">Founded in 2020, TECHIZO started with a simple mission: to provide high-quality, affordable mobile accessories that genuinely protect your devices. We noticed a gap in the market for products that combined excellent protection with stylish design.</p>
                        <p data-key="about.story.text2">Today, we serve customers across Europe, the Middle East, and Pakistan, with our headquarters based in Faisalabad. Our products are tested rigorously to ensure they meet the highest standards of quality and durability.</p>
                        <h3 data-key="about.mission">Our Mission</h3>
                        <p data-key="about.mission.text">To become the leading provider of mobile accessories by offering innovative products that enhance device protection while maintaining aesthetic appeal. We believe your mobile accessories should reflect your personal style while providing maximum protection.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Page -->
        <section id="contact-page" class="page-section">
            <div class="contact-page">
                <div class="container">
                    <div class="section-title">
                        <h2 data-key="contact.title">Contact Us</h2>
                        <p style="text-align: center; color: var(--text-secondary); max-width: 600px; margin: 0 auto; margin-top: 20px;" data-key="contact.subtitle">
                            Have questions about our products or need assistance? We're here to help! 
                            Reach out to our friendly support team.
                        </p>
                    </div>
                </div>
                
                <div class="contact-container">
                    <div class="contact-info">
                        <h3 data-key="contact.getintouch">Get In Touch</h3>
                        <div class="contact-details">
                            <div class="contact-item">
                                <div class="contact-icon">
                                    <i class="fas fa-map-marker-alt"></i>
                                </div>
                                <div class="contact-text">
                                    <h4 data-key="contact.location">Our Location</h4>
                                    <p>Faisalabad, Punjab, Pakistan</p>
                                </div>
                            </div>
                            
                            <div class="contact-item">
                                <div class="contact-icon light">
                                    <i class="fas fa-phone-alt"></i>
                                </div>
                                <div class="contact-text">
                                    <h4 data-key="contact.phone">Phone Numbers</h4>
                                    <p>+92 3481869972<br>+92 3197247048</p>
                                </div>
                            </div>
                            
                            <div class="contact-item">
                                <div class="contact-icon">
                                    <i class="fas fa-envelope"></i>
                                </div>
                                <div class="contact-text">
                                    <h4 data-key="contact.email">Email Address</h4>
                                    <p>healixcare786@gmail.com</p>
                                </div>
                            </div>
                            
                            <div class="contact-item">
                                <div class="contact-icon light">
                                    <i class="fas fa-clock"></i>
                                </div>
                                <div class="contact-text">
                                    <h4 data-key="contact.hours">Business Hours</h4>
                                    <p data-key="contact.hours.text">Monday - Friday: 9:00 AM - 6:00 PM</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="social-section">
                            <h4 data-key="contact.follow">Follow Us</h4>
                            <div class="social-links-contact">
                                <a href="#" class="facebook"><i class="fab fa-facebook-f"></i></a>
                                <a href="#" class="instagram"><i class="fab fa-instagram"></i></a>
                                <a href="https://wa.me/923481869972" class="whatsapp" target="_blank"><i class="fab fa-whatsapp"></i></a>
                            </div>
                        </div>
                        
                        <div class="map-container">
                            <div class="map-placeholder">
                                <i class="fas fa-map-marked-alt"></i>
                                <p>Faisalabad, Punjab, Pakistan</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="contact-form">
                        <h3 data-key="contact.message">Send us a Message</h3>
                        <form id="contact-form">
                            <div class="form-group">
                                <label for="contact-name" data-key="contact.form.name">Your Name</label>
                                <input type="text" id="contact-name" class="form-control" placeholder="Enter your full name" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="contact-email" data-key="contact.form.email">Your Email</label>
                                <input type="email" id="contact-email" class="form-control" placeholder="Enter your email address" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="contact-phone" data-key="contact.form.phone">Phone Number</label>
                                <input type="tel" id="contact-phone" class="form-control" placeholder="Enter your phone number">
                            </div>
                            
                            <div class="form-group">
                                <label for="contact-subject" data-key="contact.form.subject">Subject</label>
                                <select id="contact-subject" class="form-control" required>
                                    <option value="" disabled selected data-key="contact.form.subject.select">Select a subject</option>
                                    <option value="general" data-key="contact.form.subject.general">General Inquiry</option>
                                    <option value="product" data-key="contact.form.subject.product">Product Information</option>
                                    <option value="order" data-key="contact.form.subject.order">Order Support</option>
                                    <option value="warranty" data-key="contact.form.subject.warranty">Warranty Claim</option>
                                    <option value="other" data-key="contact.form.subject.other">Other</option>
                                </select>
                            </div>
                            
                            <div class="form-group">
                                <label for="contact-message" data-key="contact.form.message">Message</label>
                                <textarea id="contact-message" class="form-control" placeholder="Tell us how we can help you..." required></textarea>
                            </div>
                            
                            <button type="submit" class="submit-btn" data-key="contact.form.submit">Send Message</button>
                        </form>
                    </div>
                </div>
            </div>
        </section>

        <!-- Cart Page -->
        <section id="cart-page" class="page-section">
            <div class="container">
                <div class="section-title">
                    <h2 data-key="cart.title">Shopping Cart</h2>
                </div>
                <div class="cart-container">
                    <div class="cart-items" id="cart-items-container">
                        <div class="empty-cart" id="empty-cart-message" style="text-align: center; padding: 40px;">
                            <i class="fas fa-shopping-bag" style="font-size: 48px; color: rgba(212, 175, 55, 0.3); margin-bottom: 20px;"></i>
                            <h3 data-key="cart.empty">Your cart is empty</h3>
                            <p data-key="cart.empty.text">Add some products to your cart</p>
                            <a class="btn" data-page="products" style="margin-top: 20px;" data-key="cart.continue">Continue Shopping</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Cart Notification -->
        <div class="cart-notification" id="cart-notification">
            <i class="fas fa-check-circle"></i>
            <span data-key="cart.notification">Product added to cart!</span>
        </div>

        <!-- WhatsApp Help - Fixed on all pages -->
        <div class="whatsapp-help">
            <a href="https://wa.me/923481869972?text=Hi%20TECHIZO,%20I%20need%20help%20with%20my%20order" class="whatsapp-btn" target="_blank">
                <i class="fab fa-whatsapp"></i>
                <span data-key="whatsapp.help">Need Help?</span>
            </a>
        </div>

        <!-- Footer -->
        <footer>
            <div class="container">
                <div class="footer-content">
                    <div class="footer-column">
                        <h3 data-key="footer.about">About TECHIZO</h3>
                        <p data-key="footer.about.text">We provide premium quality mobile accessories to protect and enhance your devices. Our products are designed with care and precision.</p>
                        <div class="social-links">
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-instagram"></i></a>
                            <a href="https://wa.me/923481869972" class="btn-whatsapp" target="_blank"><i class="fab fa-whatsapp"></i></a>
                        </div>
                    </div>
                    <div class="footer-column">
                        <h3 data-key="footer.links">Quick Links</h3>
                        <ul>
                            <li><a data-page="home" data-key="nav.home">Home</a></li>
                            <li><a data-page="products" data-key="nav.products">Products</a></li>
                            <li><a data-page="about" data-key="nav.about">About Us</a></li>
                            <li><a data-page="contact" data-key="nav.contact">Contact</a></li>
                        </ul>
                    </div>
                    <div class="footer-column">
                        <h3 data-key="footer.contact">Contact Information</h3>
                        <ul>
                            <li><i class="fas fa-map-marker-alt"></i> Faisalabad, Punjab, Pakistan</li>
                            <li><i class="fas fa-phone"></i> +92 3481869972</li>
                            <li><i class="fas fa-phone"></i> +92 3197247048</li>
                            <li><i class="fas fa-envelope"></i> healixcare786@gmail.com</li>
                        </ul>
                    </div>
                </div>
                <div class="copyright">
                    <p>&copy; 2023 TECHIZO. All rights reserved.</p>
                </div>
            </div>
        </footer>
    </div>

    <!-- Admin Portal -->
    <div id="admin-portal" style="display: none;">
        <!-- Admin Header -->
        <header class="admin-header">
            <div class="container">
                <div class="admin-header-content">
                    <div class="admin-logo">
                        <h1>TECHIZO Admin</h1>
                    </div>
                    <nav class="admin-nav">
                        <ul>
                            <li><a class="dashboard-link active" data-section="dashboard">Dashboard</a></li>
                            <li><a class="dashboard-link" data-section="products">Products</a></li>
                            <li><a class="dashboard-link" data-section="orders">Orders</a></li>
                            <li><a class="dashboard-link" data-section="settings">Settings</a></li>
                            <li><a id="logout-btn">Logout</a></li>
                            <li><button class="exit-admin-btn" id="exit-admin-btn"><i class="fas fa-sign-out-alt"></i> Exit</button></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </header>

        <!-- Admin Login -->
        <section class="admin-login" id="admin-login">
            <div class="container">
                <div class="login-form">
                    <h2>Admin Login</h2>
                    <div class="admin-form-group">
                        <label for="username">Username</label>
                        <input type="text" id="username" class="admin-form-control" placeholder="Enter username">
                    </div>
                    <div class="admin-form-group">
                        <label for="password">Password</label>
                        <input type="password" id="password" class="admin-form-control" placeholder="Enter password">
                    </div>
                    <button class="btn btn-gold" id="login-btn" style="width: 100%;">Login</button>
                    <div id="login-error" style="color: var(--danger); margin-top: 15px; display: none;">Invalid username or password</div>
                </div>
            </div>
        </section>

        <!-- Admin Dashboard -->
        <section class="admin-dashboard" id="admin-dashboard">
            <div class="container">
                <!-- Dashboard Overview -->
                <div class="dashboard-section active" id="dashboard-section">
                    <div class="admin-section-title">
                        <h2>Dashboard Overview</h2>
                    </div>
                    
                    <div class="stats-cards">
                        <div class="stat-card">
                            <h3 id="total-products">0</h3>
                            <p>Total Products</p>
                        </div>
                        <div class="stat-card">
                            <h3 id="total-orders">0</h3>
                            <p>Total Orders</p>
                        </div>
                        <div class="stat-card">
                            <h3 id="pending-orders">0</h3>
                            <p>Pending Orders</p>
                        </div>
                        <div class="stat-card">
                            <h3 id="total-revenue">$0</h3>
                            <p>Total Revenue</p>
                        </div>
                    </div>
                    
                    <div class="admin-section-title">
                        <h2>Recent Orders</h2>
                    </div>
                    
                    <div class="table-container">
                        <table class="admin-table">
                            <thead>
                                <tr>
                                    <th>Order ID</th>
                                    <th>Customer</th>
                                    <th>Date</th>
                                    <th>Amount</th>
                                    <th>Status</th>
                                </tr>
                            </thead>
                            <tbody id="recent-orders-table">
                                <!-- Recent orders will be populated here -->
                            </tbody>
                        </table>
                    </div>
                </div>
                
                <!-- Products Management -->
                <div class="dashboard-section" id="products-section">
                    <div class="admin-section-title">
                        <h2>Product Management</h2>
                    </div>
                    
                    <div class="admin-form">
                        <h3 style="margin-bottom: 20px; color: var(--accent);" id="product-form-title">Add New Product</h3>
                        
                        <div class="form-row">
                            <div class="admin-form-group">
                                <label for="product-name">Product Name</label>
                                <input type="text" id="product-name" class="admin-form-control" placeholder="Enter product name">
                            </div>
                            <div class="admin-form-group">
                                <label for="product-category">Category</label>
                                <select id="product-category" class="admin-form-control">
                                    <option value="">Select Category</option>
                                    <option value="screen-protector">Screen Protector</option>
                                    <option value="phone-case">Phone Case</option>
                                    <option value="cable">Cable</option>
                                    <option value="charger">Charger</option>
                                    <option value="other">Other</option>
                                </select>
                            </div>
                        </div>
                        
                        <div class="form-row">
                            <div class="admin-form-group">
                                <label for="product-price">Price ($)</label>
                                <input type="number" id="product-price" class="admin-form-control" placeholder="Enter price" min="0" step="0.01">
                            </div>
                            <div class="admin-form-group">
                                <label for="product-discount">Discount (%)</label>
                                <input type="number" id="product-discount" class="admin-form-control" placeholder="Enter discount" min="0" max="100" step="1">
                            </div>
                        </div>
                        
                        <div class="admin-form-group">
                            <label for="product-description">Description</label>
                            <textarea id="product-description" class="admin-form-control" rows="4" placeholder="Enter product description"></textarea>
                        </div>
                        
                        <div class="admin-form-group">
                            <label for="product-image">Product Image</label>
                            <input type="file" id="product-image" class="admin-form-control" accept="image/*">
                            <div class="image-preview" id="image-preview"></div>
                        </div>
                        
                        <div class="form-actions">
                            <button class="btn btn-success" id="save-product">Save Product</button>
                            <button class="btn btn-danger" id="cancel-edit" style="display: none;">Cancel</button>
                        </div>
                    </div>
                    
                    <div class="admin-section-title">
                        <h2>All Products</h2>
                    </div>
                    
                    <div class="table-container">
                        <table class="admin-table">
                            <thead>
                                <tr>
                                    <th>Image</th>
                                    <th>Name</th>
                                    <th>Category</th>
                                    <th>Price</th>
                                    <th>Discount</th>
                                    <th>Actions</th>
                                </tr>
                            </thead>
                            <tbody id="products-table">
                                <!-- Products will be populated here -->
                            </tbody>
                        </table>
                    </div>
                </div>
                
                <!-- Orders Management -->
                <div class="dashboard-section" id="orders-section">
                    <div class="admin-section-title">
                        <h2>Order Management</h2>
                    </div>
                    
                    <div class="table-container">
                        <table class="admin-table">
                            <thead>
                                <tr>
                                    <th>Order ID</th>
                                    <th>Customer</th>
                                    <th>Email</th>
                                    <th>Phone</th>
                                    <th>Address</th>
                                    <th>Products</th>
                                    <th>Total</th>
                                    <th>Status</th>
                                    <th>Actions</th>
                                </tr>
                            </thead>
                            <tbody id="orders-table">
                                <!-- Orders will be populated here -->
                            </tbody>
                        </table>
                    </div>
                </div>
                
                <!-- Settings -->
                <div class="dashboard-section" id="settings-section">
                    <div class="admin-section-title">
                        <h2>Website Settings</h2>
                    </div>
                    
                    <div class="settings-grid">
                        <div class="setting-card">
                            <h3>Discount Settings</h3>
                            <div class="admin-form-group">
                                <label for="global-discount">Global Discount (%)</label>
                                <input type="number" id="global-discount" class="admin-form-control" min="0" max="100" step="1">
                            </div>
                            <div class="admin-form-group">
                                <label for="min-order-discount">Minimum Order for Discount ($)</label>
                                <input type="number" id="min-order-discount" class="admin-form-control" min="0" step="0.01">
                            </div>
                            <button class="btn btn-gold" id="save-discount-settings">Save Discount Settings</button>
                        </div>
                        
                        <div class="setting-card">
                            <h3>Delivery Settings</h3>
                            <div class="admin-form-group">
                                <label for="delivery-charges">Delivery Charges ($)</label>
                                <input type="number" id="delivery-charges" class="admin-form-control" min="0" step="0.01">
                            </div>
                            <div class="admin-form-group">
                                <label for="free-delivery-threshold">Free Delivery Threshold ($)</label>
                                <input type="number" id="free-delivery-threshold" class="admin-form-control" min="0" step="0.01">
                            </div>
                            <button class="btn btn-gold" id="save-delivery-settings">Save Delivery Settings</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <script>
        // Translation data
        const translations = {
            en: {
                // Navigation
                "nav.home": "Home",
                "nav.products": "Products",
                "nav.about": "About",
                "nav.contact": "Contact",
                "nav.admin": "Admin",
                "language": "Language:",
                
                // Hero section
                "hero.title": "Premium Mobile Accessories",
                "hero.subtitle": "Discover TECHIZO's high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional. Experience the perfect blend of protection and style.",
                "hero.button": "Shop Now",
                
                // Robot section
                "robot.title": "Meet TECHIZO Bot",
                "robot.text1": "Our friendly robot assistant is here to guide you through TECHIZO's premium collection of mobile accessories. From cutting-edge screen protectors to stylish phone cases, TECHIZO Bot ensures you find the perfect match for your device.",
                "robot.text2": "With advanced technology and a passion for protection, TECHIZO Bot represents our commitment to quality and innovation in every product we offer.",
                "robot.button": "Explore Products",
                
                // Slider section
                "slider.title": "Featured Collections",
                "slider.slide1.title": "Ultimate Screen Protection",
                "slider.slide1.text": "Our premium tempered glass screen protectors offer 9H hardness and oleophobic coating to resist fingerprints and scratches. Designed for maximum clarity and touch sensitivity.",
                "slider.slide2.title": "Stylish Phone Cases",
                "slider.slide2.text": "Protect your device in style with our collection of premium phone cases. From slim silicone to rugged armor cases, we have options for every lifestyle and preference.",
                "slider.slide3.title": "Fast Charging Solutions",
                "slider.slide3.text": "Keep your devices powered with our high-speed charging cables and adapters. Featuring durable construction and fast charging capabilities for all your mobile needs.",
                
                // Products section
                "products.featured": "Featured Products",
                "products.all": "All Products",
                
                // About section
                "about.title": "About TECHIZO",
                "about.story": "Our Story",
                "about.story.text1": "Founded in 2020, TECHIZO started with a simple mission: to provide high-quality, affordable mobile accessories that genuinely protect your devices. We noticed a gap in the market for products that combined excellent protection with stylish design.",
                "about.story.text2": "Today, we serve customers across Europe, the Middle East, and Pakistan, with our headquarters based in Faisalabad. Our products are tested rigorously to ensure they meet the highest standards of quality and durability.",
                "about.mission": "Our Mission",
                "about.mission.text": "To become the leading provider of mobile accessories by offering innovative products that enhance device protection while maintaining aesthetic appeal. We believe your mobile accessories should reflect your personal style while providing maximum protection.",
                
                // Contact section
                "contact.title": "Contact Us",
                "contact.subtitle": "Have questions about our products or need assistance? We're here to help! Reach out to our friendly support team.",
                "contact.getintouch": "Get In Touch",
                "contact.location": "Our Location",
                "contact.phone": "Phone Numbers",
                "contact.email": "Email Address",
                "contact.hours": "Business Hours",
                "contact.hours.text": "Monday - Friday: 9:00 AM - 6:00 PM",
                "contact.follow": "Follow Us",
                "contact.message": "Send us a Message",
                "contact.form.name": "Your Name",
                "contact.form.email": "Your Email",
                "contact.form.phone": "Phone Number",
                "contact.form.subject": "Subject",
                "contact.form.subject.select": "Select a subject",
                "contact.form.subject.general": "General Inquiry",
                "contact.form.subject.product": "Product Information",
                "contact.form.subject.order": "Order Support",
                "contact.form.subject.warranty": "Warranty Claim",
                "contact.form.subject.other": "Other",
                "contact.form.message": "Message",
                "contact.form.submit": "Send Message",
                
                // Cart section
                "cart.title": "Shopping Cart",
                "cart.empty": "Your cart is empty",
                "cart.empty.text": "Add some products to your cart",
                "cart.continue": "Continue Shopping",
                "cart.notification": "Product added to cart!",
                
                // WhatsApp
                "whatsapp.help": "Need Help?",
                
                // Footer
                "footer.about": "About TECHIZO",
                "footer.about.text": "We provide premium quality mobile accessories to protect and enhance your devices. Our products are designed with care and precision.",
                "footer.links": "Quick Links",
                "footer.contact": "Contact Information",
                
                // Logo
                "logo": "TECHIZO"
            },
            ar: {
                // Navigation
                "nav.home": "الرئيسية",
                "nav.products": "المنتجات",
                "nav.about": "من نحن",
                "nav.contact": "اتصل بنا",
                "nav.admin": "المشرف",
                "language": "اللغة:",
                
                // Hero section
                "hero.title": "إكسسوارات الجوال الممتازة",
                "hero.subtitle": "اكتشف واقيات الشاشة عالية الجودة من TECHIZO، والهواتف، وكابلات OTG، والمزيد للحفاظ على أجهزتك آمنة ووظيفية. جرب المزيج المثالي من الحماية والأناقة.",
                "hero.button": "تسوق الآن",
                
                // Robot section
                "robot.title": "تعرف على روبوت TECHIZO",
                "robot.text1": "مساعد الروبوت الودود لدينا هنا لإرشادك خلال مجموعة TECHIZO المميزة من إكسسوارات الجوال. من واقيات الشاشة المتطورة إلى هواتف أنيقة، يضمن لك روبوت TECHIZO العثور على المطابقة المثالية لجهازك.",
                "robot.text2": "مع التكنولوجيا المتقدمة وشغف الحماية، يمثل روبوت TECHIZO التزامنا بالجودة والابتكار في كل منتج نقدمه.",
                "robot.button": "استكشف المنتجات",
                
                // Slider section
                "slider.title": "المجموعات المميزة",
                "slider.slide1.title": "حماية الشاشة المثالية",
                "slider.slide1.text": "توفر واقيات الشاشة الزجاجية الممتازة لدينا صلابة 9H وطلاء أوليوفوبي لمقاومة البصمات والخدوش. مصممة لأقصى درجات الوضوح وحساسية اللمس.",
                "slider.slide2.title": "هواتف أنيقة",
                "slider.slide2.text": "احمي جهازك بأناقة مع مجموعتنا من هواتف الجوال المميزة. من السيليكون النحيف إلى هواتف الدروع القوية، لدينا خيارات لكل نمط حياة وتفضيل.",
                "slider.slide3.title": "حلول الشحن السريع",
                "slider.slide3.text": "احتفظ بأجهزتك مشحونة مع كابلات الشحن والمحولات عالية السرعة لدينا. تتميز ببناء متين وقدرات شحن سريعة لجميع احتياجاتك المحمولة.",
                
                // Products section
                "products.featured": "المنتجات المميزة",
                "products.all": "جميع المنتجات",
                
                // About section
                "about.title": "عن TECHIZO",
                "about.story": "قصتنا",
                "about.story.text1": "تأسست TECHIZO في عام 2020 بمهمة بسيطة: توفير إكسسوارات جوال عالية الجودة وبأسعار معقولة تحمي أجهزتك حقًا. لاحظنا فجوة في السوق للمنتجات التي تجمع بين الحماية الممتازة والتصميم الأنيق.",
                "about.story.text2": "اليوم، نخدم العملاء في جميع أنحاء أوروبا والشرق الأوسط وباكستان، مع مقرنا الرئيسي في فيصل آباد. يتم اختبار منتجاتنا بدقة لضمان تلبية أعلى معايير الجودة والمتانة.",
                "about.mission": "مهمتنا",
                "about.mission.text": "أن نصبح المزود الرائد لإكسسوارات الجوال من خلال تقديم منتجات مبتكرة تعزز حماية الجهاز مع الحفاظ على الجاذبية الجمالية. نعتقد أن إكسسوارات الجوال الخاصة بك يجب أن تعكس أسلوبك الشخصي مع توفير أقصى حماية.",
                
                // Contact section
                "contact.title": "اتصل بنا",
                "contact.subtitle": "هل لديك أسئلة حول منتجاتنا أو تحتاج إلى مساعدة؟ نحن هنا لمساعدتك! تواصل مع فريق الدعم الودود لدينا.",
                "contact.getintouch": "ابقى على تواصل",
                "contact.location": "موقعنا",
                "contact.phone": "أرقام الهاتف",
                "contact.email": "عنوان البريد الإلكتروني",
                "contact.hours": "ساعات العمل",
                "contact.hours.text": "الإثنين - الجمعة: 9:00 صباحًا - 6:00 مساءً",
                "contact.follow": "تابعنا",
                "contact.message": "أرسل لنا رسالة",
                "contact.form.name": "اسمك",
                "contact.form.email": "بريدك الإلكتروني",
                "contact.form.phone": "رقم الهاتف",
                "contact.form.subject": "الموضوع",
                "contact.form.subject.select": "اختر موضوعًا",
                "contact.form.subject.general": "استفسار عام",
                "contact.form.subject.product": "معلومات المنتج",
                "contact.form.subject.order": "دعم الطلب",
                "contact.form.subject.warranty": "مطالبة الضمان",
                "contact.form.subject.other": "آخر",
                "contact.form.message": "الرسالة",
                "contact.form.submit": "إرسال الرسالة",
                
                // Cart section
                "cart.title": "سلة التسوق",
                "cart.empty": "سلة التسوق الخاصة بك فارغة",
                "cart.empty.text": "أضف بعض المنتجات إلى سلة التسوق الخاصة بك",
                "cart.continue": "مواصلة التسوق",
                "cart.notification": "تمت إضافة المنتج إلى سلة التسوق!",
                
                // WhatsApp
                "whatsapp.help": "تحتاج مساعدة؟",
                
                // Footer
                "footer.about": "عن TECHIZO",
                "footer.about.text": "نوفر إكسسوارات جوال عالية الجودة لحماية وتحسين أجهزتك. تم تصميم منتجاتنا بعناية ودقة.",
                "footer.links": "روابط سريعة",
                "footer.contact": "معلومات الاتصال",
                
                // Logo
                "logo": "TECHIZO"
            }
        };

        // Current language
        let currentLanguage = 'en';

        // Sample products data
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
            }
        ];

        // Shopping cart
        var cart = [];

        // DOM elements
        var pageSections = document.querySelectorAll('.page-section');
        var navLinks = document.querySelectorAll('.nav-link[data-page]');
        var featuredProductsContainer = document.getElementById('featured-products-container');
        var allProductsContainer = document.getElementById('all-products-container');
        var cartCount = document.querySelector('.cart-count');
        var cartItemsContainer = document.getElementById('cart-items-container');
        var emptyCartMessage = document.getElementById('empty-cart-message');
        var contactForm = document.getElementById('contact-form');
        var productSlider = document.getElementById('product-slider');
        var prevSlideBtn = document.getElementById('prev-slide');
        var nextSlideBtn = document.getElementById('next-slide');
        var sliderDots = document.querySelectorAll('.slider-dot');
        var shopNowBtn = document.querySelector('.shop-now-btn');
        var exploreProductsBtn = document.querySelector('.explore-products-btn');
        var whatsappBtn = document.querySelector('.whatsapp-btn');
        var adminAccessLink = document.getElementById('admin-access-link');
        var cartNotification = document.getElementById('cart-notification');
        var languageSelector = document.getElementById('language-selector');

        // Admin Portal Elements
        var mainWebsite = document.getElementById('main-website');
        var adminPortal = document.getElementById('admin-portal');
        var adminLogin = document.getElementById('admin-login');
        var adminDashboard = document.getElementById('admin-dashboard');
        var loginBtn = document.getElementById('login-btn');
        var logoutBtn = document.getElementById('logout-btn');
        var exitAdminBtn = document.getElementById('exit-admin-btn');
        var usernameInput = document.getElementById('username');
        var passwordInput = document.getElementById('password');
        var loginError = document.getElementById('login-error');
        var dashboardLinks = document.querySelectorAll('.dashboard-link');
        var dashboardSections = document.querySelectorAll('.dashboard-section');
        
        // Products management elements
        const productFormTitle = document.getElementById('product-form-title');
        const productName = document.getElementById('product-name');
        const productCategory = document.getElementById('product-category');
        const productPrice = document.getElementById('product-price');
        const productDiscount = document.getElementById('product-discount');
        const productDescription = document.getElementById('product-description');
        const productImage = document.getElementById('product-image');
        const imagePreview = document.getElementById('image-preview');
        const saveProductBtn = document.getElementById('save-product');
        const cancelEditBtn = document.getElementById('cancel-edit');
        const productsTable = document.getElementById('products-table');
        
        // Settings elements
        const globalDiscount = document.getElementById('global-discount');
        const minOrderDiscount = document.getElementById('min-order-discount');
        const deliveryCharges = document.getElementById('delivery-charges');
        const freeDeliveryThreshold = document.getElementById('free-delivery-threshold');
        const saveDiscountSettingsBtn = document.getElementById('save-discount-settings');
        const saveDeliverySettingsBtn = document.getElementById('save-delivery-settings');
        
        // Dashboard elements
        const totalProducts = document.getElementById('total-products');
        const totalOrders = document.getElementById('total-orders');
        const pendingOrders = document.getElementById('pending-orders');
        const totalRevenue = document.getElementById('total-revenue');
        const recentOrdersTable = document.getElementById('recent-orders-table');
        const ordersTable = document.getElementById('orders-table');
        
        // State variables
        let orders = [];
        let settings = {};
        let editingProductId = null;

        // Admin credentials
        const ADMIN_USERNAME = "He@lixcare786";
        const ADMIN_PASSWORD = "Abdull@H1122";
        
        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            // Load products
            renderFeaturedProducts();
            renderAllProducts();
            updateCartUI();
            
            // Set up navigation
            navLinks.forEach(function(link) {
                link.addEventListener('click', function() {
                    var page = this.getAttribute('data-page');
                    navigateToPage(page);
                });
            });
            
            // Set up shop now button
            shopNowBtn.addEventListener('click', function() {
                navigateToPage('products');
            });
            
            // Set up explore products button
            exploreProductsBtn.addEventListener('click', function() {
                navigateToPage('products');
            });
            
            // Set up contact form
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert(currentLanguage === 'en' ? 'Thank you for your message! We will get back to you soon.' : 'شكرًا لك على رسالتك! سوف نعود إليك قريبًا.');
                contactForm.reset();
            });
            
            // Set up WhatsApp buttons to open both numbers
            setupWhatsAppButtons();
            
            // Initialize parallax effect
            initParallax();
            
            // Initialize slider
            initSlider();
            
            // Set up admin portal
            setupAdminPortal();
            
            // Set up language selector
            languageSelector.addEventListener('change', function() {
                changeLanguage(this.value);
            });
            
            // Load saved language from localStorage
            const savedLanguage = localStorage.getItem('techizo_language');
            if (savedLanguage) {
                languageSelector.value = savedLanguage;
                changeLanguage(savedLanguage);
            }
        });

        // Change language function
        function changeLanguage(lang) {
            currentLanguage = lang;
            document.documentElement.dir = lang === 'ar' ? 'rtl' : 'ltr';
            document.documentElement.lang = lang;
            
            // Update all elements with data-key
            const elements = document.querySelectorAll('[data-key]');
            elements.forEach(element => {
                const key = element.getAttribute('data-key');
                if (translations[lang] && translations[lang][key]) {
                    if (element.tagName === 'INPUT' || element.tagName === 'TEXTAREA') {
                        element.placeholder = translations[lang][key];
                    } else {
                        element.textContent = translations[lang][key];
                    }
                }
            });
            
            // Update select options
            const subjectSelect = document.getElementById('contact-subject');
            if (subjectSelect) {
                const options = subjectSelect.querySelectorAll('option');
                options.forEach(option => {
                    const key = option.getAttribute('data-key');
                    if (translations[lang] && translations[lang][key]) {
                        option.textContent = translations[lang][key];
                    }
                });
            }
            
            // Save language preference
            localStorage.setItem('techizo_language', lang);
        }

        // Set up admin portal
        function setupAdminPortal() {
            // Load data from localStorage
            loadProducts();
            loadOrders();
            loadSettings();
            
            // Set up event listeners
            setupAdminEventListeners();
            
            // Update dashboard stats
            updateDashboardStats();
        }
        
        // Set up admin event listeners
        function setupAdminEventListeners() {
            // Admin access
            adminAccessLink.addEventListener('click', function() {
                showAdminPortal();
            });
            
            // Exit admin
            exitAdminBtn.addEventListener('click', function() {
                showMainWebsite();
            });
            
            // Login
            loginBtn.addEventListener('click', handleLogin);
            
            // Logout
            logoutBtn.addEventListener('click', handleLogout);
            
            // Dashboard navigation
            dashboardLinks.forEach(link => {
                link.addEventListener('click', function() {
                    const section = this.getAttribute('data-section');
                    navigateToAdminSection(section);
                    
                    // Update active link
                    dashboardLinks.forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Product image preview
            productImage.addEventListener('change', function(e) {
                const file = e.target.files[0];
                if (file) {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        imagePreview.innerHTML = `<img src="${e.target.result}" alt="Product Preview">`;
                    };
                    reader.readAsDataURL(file);
                }
            });
            
            // Save product
            saveProductBtn.addEventListener('click', saveProduct);
            
            // Cancel edit
            cancelEditBtn.addEventListener('click', cancelEdit);
            
            // Save settings
            saveDiscountSettingsBtn.addEventListener('click', saveDiscountSettings);
            saveDeliverySettingsBtn.addEventListener('click', saveDeliverySettings);
        }
        
        // Handle login
        function handleLogin() {
            const username = usernameInput.value;
            const password = passwordInput.value;
            
            if (username === ADMIN_USERNAME && password === ADMIN_PASSWORD) {
                localStorage.setItem('adminLoggedIn', 'true');
                showAdminDashboard();
            } else {
                loginError.style.display = 'block';
            }
        }
        
        // Handle logout
        function handleLogout() {
            localStorage.removeItem('adminLoggedIn');
            showAdminLogin();
            resetForm();
        }
        
        // Show admin portal
        function showAdminPortal() {
            mainWebsite.style.display = 'none';
            adminPortal.style.display = 'block';
            
            // Check if admin is already logged in
            if (localStorage.getItem('adminLoggedIn') === 'true') {
                showAdminDashboard();
            } else {
                showAdminLogin();
            }
        }
        
        // Show main website
        function showMainWebsite() {
            mainWebsite.style.display = 'block';
            adminPortal.style.display = 'none';
        }
        
        // Show admin login
        function showAdminLogin() {
            adminLogin.style.display = 'flex';
            adminDashboard.style.display = 'none';
        }
        
        // Show admin dashboard
        function showAdminDashboard() {
            adminLogin.style.display = 'none';
            adminDashboard.style.display = 'block';
        }
        
        // Navigate to admin section
        function navigateToAdminSection(section) {
            dashboardSections.forEach(sec => {
                sec.classList.remove('active');
            });
            
            document.getElementById(`${section}-section`).classList.add('active');
        }
        
        // Load products from localStorage
        function loadProducts() {
            const storedProducts = localStorage.getItem('techizo_products');
            if (storedProducts) {
                products = JSON.parse(storedProducts);
                renderProductsTable();
            }
        }
        
        // Load orders from localStorage
        function loadOrders() {
            const storedOrders = localStorage.getItem('techizo_orders');
            if (storedOrders) {
                orders = JSON.parse(storedOrders);
                renderOrdersTable();
                renderRecentOrdersTable();
            }
        }
        
        // Load settings from localStorage
        function loadSettings() {
            const storedSettings = localStorage.getItem('techizo_settings');
            if (storedSettings) {
                settings = JSON.parse(storedSettings);
                
                // Update settings form
                if (settings.globalDiscount !== undefined) {
                    globalDiscount.value = settings.globalDiscount;
                }
                
                if (settings.minOrderDiscount !== undefined) {
                    minOrderDiscount.value = settings.minOrderDiscount;
                }
                
                if (settings.deliveryCharges !== undefined) {
                    deliveryCharges.value = settings.deliveryCharges;
                }
                
                if (settings.freeDeliveryThreshold !== undefined) {
                    freeDeliveryThreshold.value = settings.freeDeliveryThreshold;
                }
            }
        }
        
        // Save product
        function saveProduct() {
            // Validation
            if (!productName.value || !productCategory.value || !productPrice.value) {
                alert(currentLanguage === 'en' ? 'Please fill in all required fields' : 'يرجى ملء جميع الحقول المطلوبة');
                return;
            }
            
            const product = {
                id: editingProductId || Date.now(),
                name: productName.value,
                category: productCategory.value,
                price: parseFloat(productPrice.value),
                discount: parseInt(productDiscount.value) || 0,
                description: productDescription.value,
                featured: false
            };
            
            // Handle image
            if (productImage.files.length > 0) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    product.image = e.target.result;
                    
                    // Save product
                    if (editingProductId) {
                        // Update existing product
                        const index = products.findIndex(p => p.id === editingProductId);
                        if (index !== -1) {
                            products[index] = product;
                        }
                    } else {
                        // Add new product
                        products.push(product);
                    }
                    
                    // Save to localStorage and update UI
                    localStorage.setItem('techizo_products', JSON.stringify(products));
                    renderProductsTable();
                    updateDashboardStats();
                    resetForm();
                    
                    // Update main website
                    renderFeaturedProducts();
                    renderAllProducts();
                };
                reader.readAsDataURL(productImage.files[0]);
            } else {
                // If no new image, keep existing image when editing
                if (editingProductId) {
                    const existingProduct = products.find(p => p.id === editingProductId);
                    if (existingProduct) {
                        product.image = existingProduct.image;
                    }
                } else {
                    // Use default image for new products without image
                    product.image = 'https://images.unsplash.com/photo-1601593346740-925612772716?ixlib=rb-4.0.3&auto=format&fit=crop&w=687&q=80';
                }
                
                // Save product
                if (editingProductId) {
                    // Update existing product
                    const index = products.findIndex(p => p.id === editingProductId);
                    if (index !== -1) {
                        products[index] = product;
                    }
                } else {
                    // Add new product
                    products.push(product);
                }
                
                // Save to localStorage and update UI
                localStorage.setItem('techizo_products', JSON.stringify(products));
                renderProductsTable();
                updateDashboardStats();
                resetForm();
                
                // Update main website
                renderFeaturedProducts();
                renderAllProducts();
            }
        }
        
        // Edit product
        function editProduct(id) {
            const product = products.find(p => p.id === id);
            if (product) {
                productName.value = product.name;
                productCategory.value = product.category;
                productPrice.value = product.price;
                productDiscount.value = product.discount;
                productDescription.value = product.description;
                
                // Show image preview
                if (product.image) {
                    imagePreview.innerHTML = `<img src="${product.image}" alt="Product Preview">`;
                }
                
                // Update form title and buttons
                productFormTitle.textContent = currentLanguage === 'en' ? 'Edit Product' : 'تحرير المنتج';
                saveProductBtn.textContent = currentLanguage === 'en' ? 'Update Product' : 'تحديث المنتج';
                cancelEditBtn.style.display = 'inline-block';
                
                // Set editing mode
                editingProductId = id;
                
                // Scroll to form
                document.getElementById('products-section').scrollIntoView({ behavior: 'smooth' });
            }
        }
        
        // Delete product
        function deleteProduct(id) {
            if (confirm(currentLanguage === 'en' ? 'Are you sure you want to delete this product?' : 'هل أنت متأكد أنك تريد حذف هذا المنتج؟')) {
                products = products.filter(p => p.id !== id);
                localStorage.setItem('techizo_products', JSON.stringify(products));
                renderProductsTable();
                updateDashboardStats();
                
                // Update main website
                renderFeaturedProducts();
                renderAllProducts();
            }
        }
        
        // Cancel edit
        function cancelEdit() {
            resetForm();
        }
        
        // Reset form
        function resetForm() {
            productName.value = '';
            productCategory.value = '';
            productPrice.value = '';
            productDiscount.value = '';
            productDescription.value = '';
            productImage.value = '';
            imagePreview.innerHTML = '';
            
            productFormTitle.textContent = currentLanguage === 'en' ? 'Add New Product' : 'إضافة منتج جديد';
            saveProductBtn.textContent = currentLanguage === 'en' ? 'Save Product' : 'حفظ المنتج';
            cancelEditBtn.style.display = 'none';
            
            editingProductId = null;
        }
        
        // Render products table
        function renderProductsTable() {
            productsTable.innerHTML = '';
            
            if (products.length === 0) {
                productsTable.innerHTML = '<tr><td colspan="6" style="text-align: center;">No products found</td></tr>';
                return;
            }
            
            products.forEach(product => {
                const row = document.createElement('tr');
                
                row.innerHTML = `
                    <td><img src="${product.image}" alt="${product.name}" style="width: 50px; height: 50px; object-fit: cover; border-radius: 5px;"></td>
                    <td>${product.name}</td>
                    <td>${product.category}</td>
                    <td>$${product.price.toFixed(2)}</td>
                    <td>${product.discount}%</td>
                    <td class="action-buttons">
                        <button class="action-btn btn-gold" onclick="editProduct(${product.id})">${currentLanguage === 'en' ? 'Edit' : 'تحرير'}</button>
                        <button class="action-btn btn-danger" onclick="deleteProduct(${product.id})">${currentLanguage === 'en' ? 'Delete' : 'حذف'}</button>
                    </td>
                `;
                
                productsTable.appendChild(row);
            });
        }
        
        // Render orders table
        function renderOrdersTable() {
            ordersTable.innerHTML = '';
            
            if (orders.length === 0) {
                ordersTable.innerHTML = '<tr><td colspan="9" style="text-align: center;">No orders found</td></tr>';
                return;
            }
            
            orders.forEach(order => {
                const row = document.createElement('tr');
                
                // Format products list
                const productsList = order.items.map(item => 
                    `${item.name} (x${item.quantity})`
                ).join(', ');
                
                row.innerHTML = `
                    <td>#${order.id}</td>
                    <td>${order.customer.name}</td>
                    <td>${order.customer.email}</td>
                    <td>${order.customer.phone}</td>
                    <td>${order.customer.address}</td>
                    <td>${productsList}</td>
                    <td>$${order.total.toFixed(2)}</td>
                    <td>${order.status}</td>
                    <td class="action-buttons">
                        <button class="action-btn btn-success" onclick="updateOrderStatus(${order.id}, 'completed')">${currentLanguage === 'en' ? 'Complete' : 'إكمال'}</button>
                        <button class="action-btn btn-danger" onclick="updateOrderStatus(${order.id}, 'cancelled')">${currentLanguage === 'en' ? 'Cancel' : 'إلغاء'}</button>
                    </td>
                `;
                
                ordersTable.appendChild(row);
            });
        }
        
        // Render recent orders table
        function renderRecentOrdersTable() {
            recentOrdersTable.innerHTML = '';
            
            // Get recent orders (last 5)
            const recentOrders = orders.slice(-5).reverse();
            
            if (recentOrders.length === 0) {
                recentOrdersTable.innerHTML = '<tr><td colspan="5" style="text-align: center;">No recent orders</td></tr>';
                return;
            }
            
            recentOrders.forEach(order => {
                const row = document.createElement('tr');
                
                row.innerHTML = `
                    <td>#${order.id}</td>
                    <td>${order.customer.name}</td>
                    <td>${new Date(order.date).toLocaleDateString()}</td>
                    <td>$${order.total.toFixed(2)}</td>
                    <td>${order.status}</td>
                `;
                
                recentOrdersTable.appendChild(row);
            });
        }
        
        // Update order status
        function updateOrderStatus(orderId, status) {
            const order = orders.find(o => o.id === orderId);
            if (order) {
                order.status = status;
                localStorage.setItem('techizo_orders', JSON.stringify(orders));
                renderOrdersTable();
                renderRecentOrdersTable();
                updateDashboardStats();
            }
        }
        
        // Save discount settings
        function saveDiscountSettings() {
            settings.globalDiscount = parseInt(globalDiscount.value) || 0;
            settings.minOrderDiscount = parseFloat(minOrderDiscount.value) || 0;
            
            localStorage.setItem('techizo_settings', JSON.stringify(settings));
            alert(currentLanguage === 'en' ? 'Discount settings saved successfully!' : 'تم حفظ إعدادات الخصم بنجاح!');
        }
        
        // Save delivery settings
        function saveDeliverySettings() {
            settings.deliveryCharges = parseFloat(deliveryCharges.value) || 0;
            settings.freeDeliveryThreshold = parseFloat(freeDeliveryThreshold.value) || 0;
            
            localStorage.setItem('techizo_settings', JSON.stringify(settings));
            alert(currentLanguage === 'en' ? 'Delivery settings saved successfully!' : 'تم حفظ إعدادات التوصيل بنجاح!');
        }
        
        // Update dashboard statistics
        function updateDashboardStats() {
            // Total products
            totalProducts.textContent = products.length;
            
            // Total orders
            totalOrders.textContent = orders.length;
            
            // Pending orders
            const pending = orders.filter(order => order.status === 'pending').length;
            pendingOrders.textContent = pending;
            
            // Total revenue
            const revenue = orders
                .filter(order => order.status === 'completed')
                .reduce((total, order) => total + order.total, 0);
            totalRevenue.textContent = `$${revenue.toFixed(2)}`;
        }

        // Set up WhatsApp buttons
        function setupWhatsAppButtons() {
            // Update the main WhatsApp button to open a menu for both numbers
            whatsappBtn.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Create a modal or dropdown to choose between the two numbers
                var modal = document.createElement('div');
                modal.style.cssText = `
                    position: fixed;
                    top: 0;
                    left: 0;
                    width: 100%;
                    height: 100%;
                    background: rgba(0,0,0,0.8);
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    z-index: 2000;
                `;
                
                modal.innerHTML = `
                    <div style="background: rgba(30,30,30,0.95); padding: 30px; border-radius: 15px; text-align: center; max-width: 400px; width: 90%; border: 1px solid rgba(212,175,55,0.3);">
                        <h3 style="margin-bottom: 20px; color: var(--accent);">${currentLanguage === 'en' ? 'Contact TECHIZO Support' : 'اتصل بدعم TECHIZO'}</h3>
                        <p style="margin-bottom: 25px; color: var(--text-secondary);">${currentLanguage === 'en' ? 'Choose a WhatsApp number to contact our support team:' : 'اختر رقم واتساب للتواصل مع فريق الدعم لدينا:'}</p>
                        <div style="display: flex; flex-direction: column; gap: 15px;">
                            <a href="https://wa.me/923481869972?text=Hi%20TECHIZO,%20I%20need%20help%20with%20my%20order" 
                               class="btn" 
                               target="_blank" 
                               style="background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);">
                                ${currentLanguage === 'en' ? 'Contact +92 3481869972' : 'اتصل بـ +92 3481869972'}
                            </a>
                            <a href="https://wa.me/923197247048?text=Hi%20TECHIZO,%20I%20need%20help%20with%20my%20order" 
                               class="btn" 
                               target="_blank" 
                               style="background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);">
                                ${currentLanguage === 'en' ? 'Contact +92 3197247048' : 'اتصل بـ +92 3197247048'}
                            </a>
                            <button class="btn" onclick="this.parentElement.parentElement.parentElement.remove()" style="background: rgba(255,255,255,0.1);">${currentLanguage === 'en' ? 'Cancel' : 'إلغاء'}</button>
                        </div>
                    </div>
                `;
                
                document.body.appendChild(modal);
                
                // Close modal when clicking outside
                modal.addEventListener('click', function(e) {
                    if (e.target === modal) {
                        document.body.removeChild(modal);
                    }
                });
            });
            
            // Update footer WhatsApp button to open the first number directly
            var footerWhatsappBtn = document.querySelector('.footer-column .btn-whatsapp');
            if (footerWhatsappBtn) {
                footerWhatsappBtn.href = "https://wa.me/923481869972?text=Hi%20TECHIZO,%20I%20need%20help%20with%20my%20order";
            }
        }

        // Initialize parallax effect
        function initParallax() {
            var parallaxBg = document.getElementById('parallax-bg');
            
            window.addEventListener('mousemove', function(e) {
                var x = e.clientX / window.innerWidth;
                var y = e.clientY / window.innerHeight;
                
                parallaxBg.style.transform = 'translate(-' + x * 20 + 'px, -' + y * 20 + 'px)';
            });
        }

        // Initialize slider
        function initSlider() {
            let currentSlide = 0;
            const slides = document.querySelectorAll('.slide');
            const totalSlides = slides.length;
            
            // Function to go to a specific slide
            function goToSlide(slideIndex) {
                if (slideIndex < 0) {
                    currentSlide = totalSlides - 1;
                } else if (slideIndex >= totalSlides) {
                    currentSlide = 0;
                } else {
                    currentSlide = slideIndex;
                }
                
                productSlider.style.transform = `translateX(-${currentSlide * 100}%)`;
                
                // Update dots
                sliderDots.forEach((dot, index) => {
                    dot.classList.toggle('active', index === currentSlide);
                });
            }
            
            // Next slide
            nextSlideBtn.addEventListener('click', () => {
                goToSlide(currentSlide + 1);
            });
            
            // Previous slide
            prevSlideBtn.addEventListener('click', () => {
                goToSlide(currentSlide - 1);
            });
            
            // Dot navigation
            sliderDots.forEach(dot => {
                dot.addEventListener('click', () => {
                    const slideIndex = parseInt(dot.getAttribute('data-slide'));
                    goToSlide(slideIndex);
                });
            });
            
            // Auto slide every 5 seconds
            setInterval(() => {
                goToSlide(currentSlide + 1);
            }, 5000);
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
            
            // Update cart page if needed
            if (page === 'cart') {
                renderCartItems();
            }
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
        }

        // Render all products on the products page
        function renderAllProducts() {
            allProductsContainer.innerHTML = '';
            
            products.forEach(function(product) {
                var productCard = createProductCard(product);
                allProductsContainer.appendChild(productCard);
            });
        }

        // Create a product card element
        function createProductCard(product) {
            var productCard = document.createElement('div');
            productCard.className = 'product-card';
            
            var finalPrice = product.price;
            var discountAmount = 0;
            
            // Apply product-specific discount
            if (product.discount > 0) {
                discountAmount = product.price * (product.discount / 100);
                finalPrice = product.price - discountAmount;
            }
            
            var priceHtml = '';
            if (discountAmount > 0) {
                priceHtml = 
                    '<div class="product-price">' +
                        '<div>' +
                            '<span class="original-price">$' + product.price.toFixed(2) + '</span>' +
                            '<span class="price">$' + finalPrice.toFixed(2) + '</span>' +
                            '<span class="discount-badge">-' + product.discount + '%</span>' +
                        '</div>' +
                    '</div>';
            } else {
                priceHtml = 
                    '<div class="product-price">' +
                        '<span class="price">$' + finalPrice.toFixed(2) + '</span>' +
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
                    '<button class="add-to-cart-btn" data-id="' + product.id + '">' +
                        '<i class="fas fa-shopping-cart"></i>' +
                        '<span class="btn-text">' + (currentLanguage === 'en' ? 'Add to Cart' : 'أضف إلى السلة') + '</span>' +
                    '</button>' +
                '</div>';
            
            // Add event listener to Add to Cart button
            var addToCartBtn = productCard.querySelector('.add-to-cart-btn');
            addToCartBtn.addEventListener('click', function() {
                addToCart(product.id, this);
            });
            
            return productCard;
        }

        // Add product to cart
        function addToCart(productId, button) {
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
                
                // Show cart notification
                showCartNotification();
                
                // Update button state
                button.classList.add('added');
                setTimeout(function() {
                    button.classList.remove('added');
                }, 2000);
            }
        }

        // Show cart notification
        function showCartNotification() {
            cartNotification.classList.add('show');
            setTimeout(function() {
                cartNotification.classList.remove('show');
            }, 3000);
        }

        // Update cart UI
        function updateCartUI() {
            // Update cart count
            var totalItems = cart.reduce(function(total, item) {
                return total + item.quantity;
            }, 0);
            cartCount.textContent = totalItems;
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
                            '<button class="btn btn-danger remove-btn" data-id="' + item.id + '">' + (currentLanguage === 'en' ? 'Remove' : 'إزالة') + '</button>' +
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
        }
    </script>
</body>
</html>
