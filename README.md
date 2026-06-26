<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DERAGON IPHONE - المقر العالمي</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tahoma', 'Segoe UI', sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #0a0a0a;
            color: #fff;
            overflow-x: hidden;
        }

        nav {
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(20px);
            padding: 12px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(201, 162, 39, 0.2);
            flex-wrap: wrap;
            gap: 10px;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            transition: 0.4s;
        }

        nav.scrolled {
            background: rgba(0, 0, 0, 0.98);
            box-shadow: 0 5px 40px rgba(201, 162, 39, 0.1);
        }

        .logo {
            font-size: 28px;
            font-weight: bold;
            color: #FFD700;
            letter-spacing: 2px;
            text-shadow: 0 0 30px rgba(201, 162, 39, 0.3);
        }

        .logo span {
            color: #fff;
        }

        .nav-links {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: #aaa;
            text-decoration: none;
            font-size: 14px;
            transition: 0.3s;
            padding: 5px 0;
            border-bottom: 2px solid transparent;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -2px;
            right: 0;
            width: 0;
            height: 2px;
            background: #FFD700;
            transition: 0.3s;
        }

        .nav-links a:hover::after,
        .nav-links a.active::after {
            width: 100%;
        }

        .nav-links a:hover,
        .nav-links a.active {
            color: #FFD700;
        }

        header {
            background: linear-gradient(135deg, #0a0a0a 50%, #1a1508 100%);
            padding: 140px 20px 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        header::before {
            content: '🐉';
            position: absolute;
            font-size: 500px;
            opacity: 0.05;
            right: -50px;
            top: 50%;
            transform: translateY(-50%);
            animation: floatDragon 8s ease-in-out infinite;
        }

        @keyframes floatDragon {
            0%,
            100% {
                transform: translateY(-50%) rotate(-5deg);
            }
            50% {
                transform: translateY(-60%) rotate(5deg);
            }
        }

        header .glow-ring {
            position: absolute;
            width: 600px;
            height: 600px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(201, 162, 39, 0.08) 0%, transparent 70%);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            animation: pulseGlow 4s ease-in-out infinite;
        }

        @keyframes pulseGlow {
            0%,
            100% {
                transform: translate(-50%, -50%) scale(1);
                opacity: 0.5;
            }
            50% {
                transform: translate(-50%, -50%) scale(1.3);
                opacity: 1;
            }
        }

        header h1 {
            font-size: 72px;
            color: #FFD700;
            margin-bottom: 15px;
            text-shadow: 0 0 60px rgba(201, 162, 39, 0.3);
            position: relative;
            z-index: 2;
            animation: fadeInUp 1s ease;
        }

        header p {
            font-size: 24px;
            color: #ccc;
            max-width: 700px;
            margin: 0 auto 25px;
            position: relative;
            z-index: 2;
            animation: fadeInUp 1.2s ease;
            line-height: 1.8;
        }

        header .highlight {
            color: #FFD700;
            font-weight: bold;
        }

        .global-tag {
            display: inline-block;
            background: linear-gradient(135deg, rgba(201, 162, 39, 0.2), rgba(201, 162, 39, 0.05));
            border: 1px solid rgba(201, 162, 39, 0.3);
            padding: 10px 30px;
            border-radius: 50px;
            font-size: 15px;
            color: #FFD700;
            position: relative;
            z-index: 2;
            animation: fadeInUp 1.4s ease;
            backdrop-filter: blur(10px);
        }

        .header-buttons {
            position: relative;
            z-index: 2;
            animation: fadeInUp 1.6s ease;
            margin-top: 30px;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .btn {
            display: inline-block;
            padding: 16px 40px;
            background: linear-gradient(135deg, #FFD700, #c9a227);
            color: #000;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            border: none;
            cursor: pointer;
            transition: 0.4s;
            font-size: 16px;
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transform: rotate(45deg);
            transition: 0.6s;
        }

        .btn:hover::before {
            left: 100%;
        }

        .btn:hover {
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 15px 50px rgba(201, 162, 39, 0.4);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid #FFD700;
            color: #FFD700;
        }

        .btn-outline:hover {
            background: #FFD700;
            color: #000;
            box-shadow: 0 15px 50px rgba(201, 162, 39, 0.3);
        }

        .btn-sm {
            padding: 10px 25px;
            font-size: 14px;
        }

        .btn-gold {
            background: linear-gradient(135deg, #FFD700, #b8960f);
            color: #000;
        }

        .btn-green {
            background: linear-gradient(135deg, #25D366, #128C7E);
            color: #fff;
        }

        .btn-green:hover {
            box-shadow: 0 15px 50px rgba(37, 211, 102, 0.4);
        }

        section {
            padding: 80px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 42px;
            color: #FFD700;
            text-align: center;
            margin-bottom: 15px;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background: linear-gradient(90deg, transparent, #FFD700, transparent);
            margin: 15px auto 0;
        }

        .section-subtitle {
            text-align: center;
            color: #999;
            margin-bottom: 50px;
            font-size: 18px;
        }

        #about {
            background: linear-gradient(180deg, #0a0a0a, #111);
            border-radius: 30px;
            margin: 20px auto;
            padding: 80px 30px;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-grid .text {
            font-size: 18px;
            line-height: 2;
            color: #ccc;
        }

        .about-grid .text strong {
            color: #FFD700;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            text-align: center;
        }

        .stats .stat {
            background: linear-gradient(145deg, #161616, #0e0e0e);
            padding: 30px 20px;
            border-radius: 16px;
            border: 1px solid rgba(201, 162, 39, 0.1);
            transition: 0.4s;
        }

        .stats .stat:hover {
            border-color: rgba(201, 162, 39, 0.4);
            transform: translateY(-5px);
            box-shadow: 0 10px 40px rgba(201, 162, 39, 0.05);
        }

        .stats .stat .number {
            font-size: 42px;
            color: #FFD700;
            font-weight: bold;
            text-shadow: 0 0 30px rgba(201, 162, 39, 0.2);
        }

        .stats .stat .label {
            font-size: 14px;
            color: #888;
            margin-top: 5px;
        }

        #branches {
            background: linear-gradient(180deg, #111, #0a0a0a);
            border-radius: 30px;
            margin: 20px auto;
            padding: 80px 30px;
        }

        .branches-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .branch-card {
            background: linear-gradient(145deg, #161616, #0e0e0e);
            padding: 35px 25px;
            border-radius: 20px;
            border: 1px solid rgba(201, 162, 39, 0.1);
            text-align: center;
            transition: 0.5s;
            position: relative;
            overflow: hidden;
        }

        .branch-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(145deg, rgba(201, 162, 39, 0.05), transparent);
            opacity: 0;
            transition: 0.5s;
        }

        .branch-card:hover::before {
            opacity: 1;
        }

        .branch-card:hover {
            border-color: rgba(201, 162, 39, 0.4);
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(201, 162, 39, 0.08);
        }

        .branch-card .flag {
            font-size: 56px;
            display: block;
            margin-bottom: 12px;
            position: relative;
        }

        .branch-card h3 {
            color: #FFD700;
            font-size: 22px;
            margin-bottom: 5px;
            position: relative;
        }

        .branch-card .city {
            color: #aaa;
            font-size: 16px;
            position: relative;
        }

        .branch-card .address {
            color: #666;
            font-size: 14px;
            margin: 8px 0 12px;
            position: relative;
        }

        .branch-card .whatsapp-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #25D366;
            text-decoration: none;
            font-weight: bold;
            font-size: 15px;
            transition: 0.3s;
            position: relative;
        }

        .branch-card .whatsapp-link:hover {
            color: #fff;
            transform: scale(1.05);
        }

        .platform-links {
            display: flex;
            justify-content: center;
            gap: 8px;
            flex-wrap: wrap;
            margin-top: 18px;
            padding-top: 18px;
            border-top: 1px solid rgba(201, 162, 39, 0.1);
            position: relative;
        }

        .platform-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 5px;
            padding: 6px 12px;
            border-radius: 25px;
            font-size: 13px;
            text-decoration: none;
            transition: 0.4s;
            font-weight: bold;
            min-width: 36px;
            height: 36px;
        }

        .platform-links a:hover {
            transform: scale(1.2) translateY(-3px);
        }

        .platform-links .linkedin {
            background: #0a66c2;
            color: #fff;
        }
        .platform-links .linkedin:hover {
            background: #fff;
            color: #0a66c2;
            box-shadow: 0 5px 20px rgba(10, 102, 194, 0.4);
        }

        .platform-links .website {
            background: #c9a227;
            color: #000;
        }
        .platform-links .website:hover {
            background: #fff;
            color: #c9a227;
            box-shadow: 0 5px 20px rgba(201, 162, 39, 0.4);
        }

        .platform-links .facebook {
            background: #1877f2;
            color: #fff;
        }
        .platform-links .facebook:hover {
            background: #fff;
            color: #1877f2;
            box-shadow: 0 5px 20px rgba(24, 119, 242, 0.4);
        }

        .platform-links .instagram {
            background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%);
            color: #fff;
        }
        .platform-links .instagram:hover {
            transform: scale(1.2) translateY(-3px);
            box-shadow: 0 5px 20px rgba(214, 36, 159, 0.4);
        }

        .platform-links .twitter {
            background: #000;
            color: #fff;
            border: 1px solid #333;
        }
        .platform-links .twitter:hover {
            background: #fff;
            color: #000;
            box-shadow: 0 5px 20px rgba(255, 255, 255, 0.1);
        }

        .platform-links .youtube {
            background: #ff0000;
            color: #fff;
        }
        .platform-links .youtube:hover {
            background: #fff;
            color: #ff0000;
            box-shadow: 0 5px 20px rgba(255, 0, 0, 0.4);
        }

        .platform-links .tiktok {
            background: #000;
            color: #fff;
            border: 1px solid #333;
            font-weight: bold;
        }
        .platform-links .tiktok:hover {
            background: #fff;
            color: #000;
            border-color: #fff;
            box-shadow: 0 5px 20px rgba(255, 255, 255, 0.1);
        }
        .platform-links .tiktok:hover .tiktok-icon {
            background: linear-gradient(45deg, #25f4ee, #fe2c55);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .platform-links .snapchat {
            background: #fffc00;
            color: #000;
        }
        .platform-links .snapchat:hover {
            background: #000;
            color: #fffc00;
            box-shadow: 0 5px 20px rgba(255, 252, 0, 0.3);
        }

        .platform-label {
            font-size: 12px;
            color: #666;
            display: block;
            margin-top: 14px;
            position: relative;
        }

        #products {
            background: linear-gradient(180deg, #0a0a0a, #111);
            border-radius: 30px;
            margin: 20px auto;
            padding: 80px 30px;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 25px;
        }

        .product-card {
            background: linear-gradient(145deg, #161616, #0e0e0e);
            padding: 30px 20px;
            border-radius: 20px;
            border: 1px solid rgba(201, 162, 39, 0.1);
            text-align: center;
            transition: 0.5s;
            position: relative;
            overflow: hidden;
        }

        .product-card::before {
            content: '';
            position: absolute;
            top: -100%;
            left: -100%;
            width: 300%;
            height: 300%;
            background: radial-gradient(circle, rgba(201, 162, 39, 0.05), transparent 70%);
            transition: 0.6s;
        }

        .product-card:hover::before {
            top: -50%;
            left: -50%;
        }

        .product-card:hover {
            border-color: rgba(201, 162, 39, 0.4);
            transform: translateY(-8px);
            box-shadow: 0 15px 50px rgba(201, 162, 39, 0.08);
        }

        .product-card .icon {
            font-size: 56px;
            display: block;
            margin-bottom: 12px;
            position: relative;
        }

        .product-card h3 {
            font-size: 19px;
            margin-bottom: 5px;
            position: relative;
        }

        .product-card .price {
            color: #FFD700;
            font-size: 26px;
            font-weight: bold;
            margin: 12px 0;
            position: relative;
            text-shadow: 0 0 20px rgba(201, 162, 39, 0.1);
        }

        .product-card .btn {
            padding: 10px 28px;
            font-size: 14px;
            position: relative;
        }

        #accessories {
            background: linear-gradient(180deg, #111, #0a0a0a);
            border-radius: 30px;
            margin: 20px auto;
            padding: 80px 30px;
        }

        .accessories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
        }

        .accessory-card {
            background: linear-gradient(145deg, #161616, #0e0e0e);
            padding: 25px 15px;
            border-radius: 16px;
            borde

            
