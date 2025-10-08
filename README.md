
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TECHIZO - Premium Mobile Accessories</title>
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
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.5);
            animation: pulse 2s infinite;
            overflow: hidden;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 10px rgba(212, 175, 55, 0.5); }
            50% { box-shadow: 0 0 20px rgba(212, 175, 55, 0.8); }
            100% { box-shadow: 0 0 10px rgba(212, 175, 55, 0.5); }
        }
        
        .logo-img img {
            width: 100%;
            height: 100%;
            object-fit: contain;
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
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <a href="#" class="logo" data-page="home">
                    <div class="logo-img">
                        <img src="https://drive.google.com/uc?export=download&id=1XOt-PieewIUE4GsP9YFpwlXKBu7Xv5pe" alt="TECHIZO Logo">
                    </div>
                    <h1>TECHIZO</h1>
                </a>
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
                    <span>Language:</span>
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
                <h1 class="hero-title">Premium Mobile Accessories</h1>
                <p class="hero-subtitle">Discover TECHIZO's high-quality screen protectors, cases, OTG cables, and more to keep your devices safe and functional. Experience the perfect blend of protection and style.</p>
                <a class="btn shop-now-btn" data-page="products">Shop Now</a>
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
                    <h2>Meet TECHIZO Bot</h2>
                    <p>Our friendly robot assistant is here to guide you through TECHIZO's premium collection of mobile accessories. From cutting-edge screen protectors to stylish phone cases, TECHIZO Bot ensures you find the perfect match for your device.</p>
                    <p>With advanced technology and a passion for protection, TECHIZO Bot represents our commitment to quality and innovation in every product we offer.</p>
                    <a class="btn btn-gold explore-products-btn" data-page="products">Explore Products</a>
                </div>
            </div>
        </section>

        <!-- Product Slider Section -->
        <section class="slider-section">
            <div class="container">
                <div class="section-title">
                    <h2>Featured Collections</h2>
                </div>
            </div>
            <div class="slider-container">
                <div class="slider" id="product-slider">
                    <div class="slide">
                        <div class="slide-content">
                            <h2>Ultimate Screen Protection</h2>
                            <p>Our premium tempered glass screen protectors offer 9H hardness and oleophobic coating to resist fingerprints and scratches. Designed for maximum clarity and touch sensitivity.</p>
                        </div>
                        <div class="slide-image">
                            <img src="https://images.unsplash.com/photo-1601593346740-925612772716?ixlib=rb-4.0.3&auto=format&fit=crop&w=687&q=80" alt="Screen Protectors">
                        </div>
                    </div>
                    <div class="slide">
                        <div class="slide-content">
                            <h2>Stylish Phone Cases</h2>
                            <p>Protect your device in style with our collection of premium phone cases. From slim silicone to rugged armor cases, we have options for every lifestyle and preference.</p>
                        </div>
                        <div class="slide-image">
                            <img src="https://images.unsplash.com/photo-1556656793-08538906a9f8?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Phone Cases">
                        </div>
                    </div>
                    <div class="slide">
                        <div class="slide-content">
                            <h2>Fast Charging Solutions</h2>
                            <p>Keep your devices powered with our high-speed charging cables and adapters. Featuring durable construction and fast charging capabilities for all your mobile needs.</p>
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
                    <h2>Featured Products</h2>
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
                <h2>All Products</h2>
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
                <h2>About TECHIZO</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Our Story</h3>
                    <p>Founded in 2020, TECHIZO started with a simple mission: to provide high-quality, affordable mobile accessories that genuinely protect your devices. We noticed a gap in the market for products that combined excellent protection with stylish design.</p>
                    <p>Today, we serve customers across Europe, the Middle East, and Pakistan, with our headquarters based in Faisalabad. Our products are tested rigorously to ensure they meet the highest standards of quality and durability.</p>
                    <h3>Our Mission</h3>
                    <p>To become the leading provider of mobile accessories by offering innovative products that enhance device protection while maintaining aesthetic appeal. We believe your mobile accessories should reflect your personal style while providing maximum protection.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Page -->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TECHIZO - Contact Us</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary: #121212;
            --secondary: #FF9800; /* Light Orange */
            --accent: #FFB74D; /* Lighter Orange */
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
            background: linear-gradient(135deg, var(--secondary) 0%, #E65100 100%);
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            text-decoration: none;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.4s ease;
            box-shadow: 0 4px 15px rgba(255, 152, 0, 0.3);
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
            box-shadow: 0 8px 25px rgba(255, 152, 0, 0.5);
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
        
        /* Orange Glow Animation */
        @keyframes orangeGlow {
            0% { box-shadow: 0 0 10px rgba(255, 152, 0, 0.5); }
            50% { box-shadow: 0 0 20px rgba(255, 152, 0, 0.8); }
            100% { box-shadow: 0 0 10px rgba(255, 152, 0, 0.5); }
        }
        
        .contact-icon {
            animation: orangeGlow 3s infinite;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .contact-container {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            
            .contact-info, .contact-form {
                padding: 30px;
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
    <!-- Contact Page -->
    <section id="contact-page" class="page-section active">
        <div class="contact-page">
            <div class="container">
                <div class="section-title">
                    <h2>Contact Us</h2>
                    <p style="text-align: center; color: var(--text-secondary); max-width: 600px; margin: 0 auto; margin-top: 20px;">
                        Have questions about our products or need assistance? We're here to help! 
                        Reach out to our friendly support team.
                    </p>
                </div>
            </div>
            
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Get In Touch</h3>
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div class="contact-text">
                                <h4>Our Location</h4>
                                <p>Faisalabad, Punjab, Pakistan</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon light">
                                <i class="fas fa-phone-alt"></i>
                            </div>
                            <div class="contact-text">
                                <h4>Phone Numbers</h4>
                                <p>+92 3481869972<br>+92 3197247048</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div class="contact-text">
                                <h4>Email Address</h4>
                                <p>healixcare786@gmail.com</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon light">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div class="contact-text">
                                <h4>Business Hours</h4>
                                <p>Monday - Friday: 9:00 AM - 6:00 PM</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="social-section">
                        <h4>Follow Us</h4>
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
                    <h3>Send us a Message</h3>
                    <form id="contact-form">
                        <div class="form-group">
                            <label for="contact-name">Your Name</label>
                            <input type="text" id="contact-name" class="form-control" placeholder="Enter your full name" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="contact-email">Your Email</label>
                            <input type="email" id="contact-email" class="form-control" placeholder="Enter your email address" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="contact-phone">Phone Number</label>
                            <input type="tel" id="contact-phone" class="form-control" placeholder="Enter your phone number">
                        </div>
                        
                        <div class="form-group">
                            <label for="contact-subject">Subject</label>
                            <select id="contact-subject" class="form-control" required>
                                <option value="" disabled selected>Select a subject</option>
                                <option value="general">General Inquiry</option>
                                <option value="product">Product Information</option>
                                <option value="order">Order Support</option>
                                <option value="warranty">Warranty Claim</option>
                                <option value="other">Other</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="contact-message">Message</label>
                            <textarea id="contact-message" class="form-control" placeholder="Tell us how we can help you..." required></textarea>
                        </div>
                        
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <script>
        // Contact form submission
        document.getElementById('contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('contact-name').value;
            const email = document.getElementById('contact-email').value;
            const subject = document.getElementById('contact-subject').value;
            const message = document.getElementById('contact-message').value;
            
            // Simple validation
            if (!name || !email || !subject || !message) {
                alert('Please fill in all required fields.');
                return;
            }
            
            // In a real application, you would send this data to a server
            // For now, we'll just show a success message
            alert(`Thank you, ${name}! Your message has been sent successfully. We'll get back to you soon.`);
            
            // Reset the form
            document.getElementById('contact-form').reset();
        });
    </script>
</body>
</html>

    <!-- Cart Page -->
    <section id="cart-page" class="page-section">
        <div class="container">
            <div class="section-title">
                <h2>Shopping Cart</h2>
            </div>
            <div class="cart-container">
                <div class="cart-items" id="cart-items-container">
                    <div class="empty-cart" id="empty-cart-message" style="text-align: center; padding: 40px;">
                        <i class="fas fa-shopping-bag" style="font-size: 48px; color: rgba(212, 175, 55, 0.3); margin-bottom: 20px;"></i>
                        <h3>Your cart is empty</h3>
                        <p>Add some products to your cart</p>
                        <a class="btn" data-page="products" style="margin-top: 20px;">Continue Shopping</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- WhatsApp Help - Fixed on all pages -->
    <div class="whatsapp-help">
        <a href="https://wa.me/923481869972?text=Hi%20TECHIZO,%20I%20need%20help%20with%20my%20order" class="whatsapp-btn" target="_blank">
            <i class="fab fa-whatsapp"></i>
            <span>Need Help?</span>
        </a>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>About TECHIZO</h3>
                    <p>We provide premium quality mobile accessories to protect and enhance your devices. Our products are designed with care and precision.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="https://wa.me/923481869972" class="btn-whatsapp" target="_blank"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a data-page="home">Home</a></li>
                        <li><a data-page="products">Products</a></li>
                        <li><a data-page="about">About Us</a></li>
                        <li><a data-page="contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Information</h3>
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

    <script>
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
                alert('Thank you for your message! We will get back to you soon.');
                contactForm.reset();
            });
            
            // Set up WhatsApp buttons to open both numbers
            setupWhatsAppButtons();
            
            // Initialize parallax effect
            initParallax();
            
            // Initialize slider
            initSlider();
        });

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
                        <h3 style="margin-bottom: 20px; color: var(--accent);">Contact TECHIZO Support</h3>
                        <p style="margin-bottom: 25px; color: var(--text-secondary);">Choose a WhatsApp number to contact our support team:</p>
                        <div style="display: flex; flex-direction: column; gap: 15px;">
                            <a href="https://wa.me/923481869972?text=Hi%20TECHIZO,%20I%20need%20help%20with%20my%20order" 
                               class="btn" 
                               target="_blank" 
                               style="background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);">
                                Contact +92 3481869972
                            </a>
                            <a href="https://wa.me/923197247048?text=Hi%20TECHIZO,%20I%20need%20help%20with%20my%20order" 
                               class="btn" 
                               target="_blank" 
                               style="background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);">
                                Contact +92 3197247048
                            </a>
                            <button class="btn" onclick="this.parentElement.parentElement.parentElement.remove()" style="background: rgba(255,255,255,0.1);">Cancel</button>
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
                        '<button class="btn add-to-cart-btn" data-id="' + product.id + '">Add to Cart</button>' +
                    '</div>';
            } else {
                priceHtml = 
                    '<div class="product-price">' +
                        '<span class="price">$' + finalPrice.toFixed(2) + '</span>' +
                        '<button class="btn add-to-cart-btn" data-id="' + product.id + '">Add to Cart</button>' +
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
                            '<button class="btn btn-danger remove-btn" data-id="' + item.id + '">Remove</button>' +
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
