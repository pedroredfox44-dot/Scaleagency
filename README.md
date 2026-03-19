<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scale Agency - Venda o que quiser sem perder sua Shopify Payments</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #000000;
            --bg-secondary: #0A0A0A;
            --bg-card: #111111;
            --text-primary: #FFFFFF;
            --text-secondary: #A0A0A0;
            --accent: #00FF88;
            --accent-dark: #00CC6E;
            --border: rgba(255, 255, 255, 0.08);
            --font: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
        }

        body {
            font-family: var(--font);
            background: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.5rem 0;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid var(--border);
            z-index: 1000;
            transition: all 0.3s ease;
        }

        nav.scrolled {
            padding: 1rem 0;
            background: rgba(0, 0, 0, 0.95);
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
            display: grid;
            grid-template-columns: 1fr auto 1fr;
            align-items: center;
        }

        .nav-spacer {
            width: 45px;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            letter-spacing: -0.5px;
            text-align: center;
        }

        .logo-text {
            color: var(--text-primary);
        }

        .logo-accent {
            color: var(--accent);
        }

        .nav-cta {
            padding: 0.75rem;
            background: transparent;
            color: var(--text-primary);
            border: 1px solid var(--border);
            border-radius: 50%;
            width: 45px;
            height: 45px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
            justify-self: end;
        }

        .nav-cta:hover {
            background: var(--accent);
            color: var(--bg-primary);
            border-color: var(--accent);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(0, 255, 136, 0.3);
        }

        .nav-cta svg {
            width: 20px;
            height: 20px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            padding: 8rem 2rem 4rem;
            overflow: hidden;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 30% 20%, rgba(0, 255, 136, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 70% 80%, rgba(0, 255, 136, 0.1) 0%, transparent 50%);
            opacity: 0.5;
        }

        .hero-grid {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: 
                linear-gradient(rgba(255, 255, 255, 0.02) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 255, 255, 0.02) 1px, transparent 1px);
            background-size: 50px 50px;
            opacity: 0.3;
        }

        .hero-content {
            max-width: 1400px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .hero-badge {
            display: inline-block;
            padding: 0.5rem 1.5rem;
            background: rgba(0, 255, 136, 0.1);
            border: 1px solid rgba(0, 255, 136, 0.3);
            border-radius: 50px;
            color: var(--accent);
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 2rem;
            animation: fadeInUp 0.8s ease;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 900;
            line-height: 1.1;
            letter-spacing: -3px;
            margin-bottom: 1.5rem;
            animation: fadeInUp 0.8s ease 0.2s backwards;
        }

        .hero h1 .gradient-text {
            background: linear-gradient(135deg, var(--text-primary) 0%, var(--accent) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-subtitle {
            font-size: clamp(1.1rem, 2vw, 1.4rem);
            color: var(--text-secondary);
            max-width: 700px;
            line-height: 1.8;
            margin-bottom: 3rem;
            animation: fadeInUp 0.8s ease 0.4s backwards;
        }

        .hero-cta {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 1.2rem 3rem;
            background: var(--accent);
            color: var(--bg-primary);
            font-weight: 700;
            font-size: 1rem;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            animation: fadeInUp 0.8s ease 0.6s backwards;
            box-shadow: 0 10px 40px rgba(0, 255, 136, 0.3);
        }

        .hero-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 50px rgba(0, 255, 136, 0.5);
        }

        /* Problem Section */
        .problem {
            padding: 8rem 2rem;
            background: var(--bg-secondary);
            position: relative;
        }

        .section-header {
            max-width: 800px;
            margin: 0 auto 5rem;
            text-align: center;
        }

        .section-label {
            color: var(--accent);
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 1rem;
        }

        .section-title {
            font-size: clamp(2.5rem, 6vw, 4rem);
            font-weight: 900;
            letter-spacing: -2px;
            margin-bottom: 1.5rem;
            line-height: 1.1;
        }

        .section-description {
            font-size: 1.2rem;
            color: var(--text-secondary);
            line-height: 1.7;
        }

        .problem-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .problem-card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 2.5rem;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .problem-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
            transform: scaleX(0);
            transition: transform 0.4s ease;
        }

        .problem-card:hover {
            border-color: rgba(0, 255, 136, 0.3);
            transform: translateY(-5px);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
        }

        .problem-card:hover::before {
            transform: scaleX(1);
        }

        .problem-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            filter: grayscale(1);
            transition: filter 0.4s ease;
        }

        .problem-card:hover .problem-icon {
            filter: grayscale(0);
        }

        .problem-card h3 {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--accent);
        }

        .problem-card p {
            color: var(--text-secondary);
            line-height: 1.7;
        }

        /* Solution Section */
        .solution {
            padding: 8rem 2rem;
            background: var(--bg-primary);
            position: relative;
            overflow: hidden;
        }

        .solution-content {
            max-width: 1400px;
            margin: 0 auto;
        }

        .dual-system {
            display: grid;
            grid-template-columns: 1fr auto 1fr;
            gap: 3rem;
            align-items: center;
            margin-top: 4rem;
        }

        .system-card {
            background: var(--bg-card);
            border: 2px solid var(--accent);
            border-radius: 20px;
            padding: 3rem;
            position: relative;
            transition: all 0.4s ease;
            box-shadow: 0 0 40px rgba(0, 255, 136, 0.2);
        }

        .system-card:hover {
            transform: scale(1.02);
            box-shadow: 0 0 60px rgba(0, 255, 136, 0.4);
        }

        .system-number {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 50px;
            background: var(--accent);
            color: var(--bg-primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 900;
            font-size: 1.5rem;
        }

        .system-card h3 {
            font-size: 2rem;
            font-weight: 900;
            color: var(--accent);
            margin-bottom: 0.5rem;
            text-align: center;
        }

        .system-role {
            text-align: center;
            color: var(--text-secondary);
            font-size: 0.95rem;
            margin-bottom: 2rem;
            font-style: italic;
        }

        .system-features {
            list-style: none;
        }

        .system-features li {
            padding: 0.8rem 0;
            color: var(--text-secondary);
            position: relative;
            padding-left: 2rem;
            border-bottom: 1px solid var(--border);
        }

        .system-features li:last-child {
            border-bottom: none;
        }

        .system-features li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
            font-size: 1.2rem;
        }

        .connector {
            font-size: 4rem;
            color: var(--accent);
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }

        .integration-note {
            text-align: center;
            margin-top: 3rem;
            padding: 2rem;
            background: rgba(0, 255, 136, 0.05);
            border-radius: 12px;
            border: 1px solid rgba(0, 255, 136, 0.2);
        }

        .integration-note p {
            color: var(--accent);
            font-size: 1.1rem;
            font-weight: 600;
        }

        /* Global Reach Section */
        .global-reach {
            padding: 8rem 2rem;
            background: var(--bg-primary);
            position: relative;
        }

        .countries-grid {
            max-width: 1200px;
            margin: 4rem auto 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }

        .country-card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
        }

        .country-card:hover {
            border-color: var(--accent);
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 255, 136, 0.2);
        }

        .country-flag {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .country-card h4 {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--text-primary);
            margin-bottom: 0.5rem;
        }

        .country-card p {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .global-stats {
            max-width: 1000px;
            margin: 5rem auto 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 3rem;
            padding: 3rem;
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 16px;
        }

        .global-stat-item {
            text-align: center;
        }

        .global-stat-number {
            font-size: 3.5rem;
            font-weight: 900;
            color: var(--accent);
            line-height: 1;
            margin-bottom: 0.5rem;
            text-shadow: 0 0 30px rgba(0, 255, 136, 0.4);
        }

        .global-stat-label {
            font-size: 1rem;
            color: var(--text-secondary);
        }

        /* Benefits Section */
        .benefits {
            padding: 8rem 2rem;
            background: var(--bg-secondary);
        }

        .benefits-grid {
            max-width: 1200px;
            margin: 4rem auto 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .benefit-card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 2.5rem;
            text-align: center;
            transition: all 0.3s ease;
        }

        .benefit-card:hover {
            border-color: var(--accent);
            transform: translateY(-5px);
        }

        .benefit-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .benefit-card h3 {
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--accent);
        }

        .benefit-card p {
            color: var(--text-secondary);
            line-height: 1.6;
        }

        /* Stats Section */
        .stats {
            padding: 8rem 2rem;
            background: var(--bg-primary);
        }

        .stats-grid {
            max-width: 1200px;
            margin: 4rem auto 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 5rem;
            font-weight: 900;
            color: var(--accent);
            line-height: 1;
            margin-bottom: 1rem;
            text-shadow: 0 0 30px rgba(0, 255, 136, 0.5);
        }

        .stat-label {
            font-size: 1.1rem;
            color: var(--text-secondary);
        }

        /* Social Proof Section */
        .social-proof-section {
            padding: 8rem 2rem;
            background: var(--bg-secondary);
        }

        .social-proof-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .carousel-container {
            position: relative;
            margin: 4rem 0;
            padding: 0 60px;
        }

        .carousel-wrapper {
            overflow: hidden;
            border-radius: 16px;
        }

        .carousel-track {
            display: flex;
            transition: transform 0.5s ease;
        }

        .proof-card {
            min-width: 100%;
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 3rem 2rem;
            min-height: 350px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
        }

        .proof-placeholder {
            text-align: center;
            opacity: 0.3;
        }

        .proof-placeholder svg {
            stroke: var(--text-secondary);
            margin-bottom: 1rem;
        }

        .proof-placeholder p {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .carousel-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 50px;
            height: 50px;
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
            z-index: 10;
        }

        .carousel-btn:hover {
            background: var(--accent);
            border-color: var(--accent);
            transform: translateY(-50%) scale(1.1);
        }

        .carousel-btn svg {
            stroke: var(--text-primary);
        }

        .carousel-btn:hover svg {
            stroke: var(--bg-primary);
        }

        .carousel-prev {
            left: 0;
        }

        .carousel-next {
            right: 0;
        }

        .carousel-dots {
            display: flex;
            justify-content: center;
            gap: 0.8rem;
            margin-top: 2rem;
        }

        .dot {
            width: 10px;
            height: 10px;
            background: var(--border);
            border-radius: 50%;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .dot:hover {
            background: var(--text-secondary);
        }

        .dot.active {
            background: var(--accent);
            width: 30px;
            border-radius: 5px;
        }

        .proof-note {
            text-align: center;
            padding: 2rem;
            background: rgba(0, 255, 136, 0.05);
            border: 1px solid rgba(0, 255, 136, 0.2);
            border-radius: 12px;
        }

        .proof-note p {
            color: var(--accent);
            font-size: 1.1rem;
            font-weight: 600;
            margin: 0;
        }

        /* Reviews Section */
        .reviews-section {
            padding: 8rem 2rem;
            background: var(--bg-primary);
        }

        .reviews-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }

        .review-card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 2.5rem;
            transition: all 0.3s ease;
        }

        .review-card:hover {
            border-color: var(--accent);
            transform: translateY(-5px);
            box-shadow: 0 20px 60px rgba(0, 255, 136, 0.15);
        }

        .review-stars {
            color: var(--accent);
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            letter-spacing: 2px;
        }

        .review-text {
            color: var(--text-secondary);
            line-height: 1.8;
            margin-bottom: 2rem;
            font-size: 1rem;
        }

        .review-author {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding-top: 1.5rem;
            border-top: 1px solid var(--border);
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            background: var(--accent);
            color: var(--bg-primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1rem;
        }

        .author-name {
            font-weight: 600;
            color: var(--text-primary);
            margin-bottom: 0.25rem;
        }

        .author-role {
            font-size: 0.85rem;
            color: var(--text-secondary);
        }

        /* About Section */
        .about-section {
            padding: 8rem 2rem;
            background: var(--bg-secondary);
        }

        .about-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .about-content {
            margin-top: 4rem;
            display: grid;
            grid-template-columns: 1.5fr 1fr;
            gap: 4rem;
        }

        .about-text p {
            color: var(--text-secondary);
            line-height: 1.8;
            margin-bottom: 1.5rem;
            font-size: 1.05rem;
        }

        .about-lead {
            font-size: 1.3rem !important;
            color: var(--accent) !important;
            font-weight: 600;
            line-height: 1.6 !important;
        }

        .about-text strong {
            color: var(--text-primary);
        }

        .about-features {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .about-feature-item {
            display: flex;
            gap: 1.5rem;
            padding: 2rem;
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 12px;
            transition: all 0.3s ease;
        }

        .about-feature-item:hover {
            border-color: var(--accent);
            transform: translateX(5px);
        }

        .feature-icon {
            font-size: 2.5rem;
            line-height: 1;
        }

        .feature-content h4 {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--text-primary);
            margin-bottom: 0.5rem;
        }

        .feature-content p {
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        /* CTA Section */
        .final-cta {
            padding: 8rem 2rem;
            background: var(--bg-secondary);
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .final-cta::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 800px;
            height: 800px;
            background: radial-gradient(circle, rgba(0, 255, 136, 0.1) 0%, transparent 70%);
        }

        .cta-content {
            max-width: 900px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .cta-content h2 {
            font-size: clamp(2.5rem, 7vw, 5rem);
            font-weight: 900;
            letter-spacing: -2px;
            margin-bottom: 2rem;
            line-height: 1.1;
        }

        .cta-content .highlight {
            color: var(--accent);
        }

        .cta-content p {
            font-size: 1.3rem;
            color: var(--text-secondary);
            margin-bottom: 3rem;
            line-height: 1.7;
        }

        /* Footer */
        footer {
            padding: 3rem 2rem;
            background: var(--bg-primary);
            border-top: 1px solid var(--border);
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-logo {
            font-size: 1.5rem;
            font-weight: 800;
            margin-bottom: 1rem;
        }

        footer p {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            z-index: 10000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background: rgba(0, 0, 0, 0.95);
            backdrop-filter: blur(20px);
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background: var(--bg-secondary);
            margin: 2rem auto;
            padding: 0;
            border: 1px solid var(--border);
            border-radius: 20px;
            width: 90%;
            max-width: 600px;
            position: relative;
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.8);
            max-height: 90vh;
            overflow-y: auto;
        }

        .close-modal {
            position: absolute;
            right: 1.5rem;
            top: 1.5rem;
            color: var(--text-secondary);
            font-size: 2rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            z-index: 1;
        }

        .close-modal:hover {
            color: var(--accent);
            transform: rotate(90deg);
        }

        .form-header {
            padding: 3rem 2rem 2rem;
            text-align: center;
            border-bottom: 1px solid var(--border);
        }

        .form-header h2 {
            font-size: 2rem;
            font-weight: 900;
            color: var(--accent);
            margin-bottom: 0.5rem;
        }

        .form-header p {
            color: var(--text-secondary);
        }

        #leadForm {
            padding: 2rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--text-primary);
            font-weight: 600;
            font-size: 0.9rem;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 8px;
            color: var(--text-primary);
            font-family: var(--font);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 20px rgba(0, 255, 136, 0.2);
        }

        .form-submit {
            width: 100%;
            padding: 1.2rem;
            background: var(--accent);
            color: var(--bg-primary);
            border: none;
            border-radius: 8px;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 1rem;
        }

        .form-submit:hover {
            background: var(--accent-dark);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(0, 255, 136, 0.4);
        }

        .form-disclaimer {
            text-align: center;
            color: var(--text-secondary);
            font-size: 0.85rem;
            margin-top: 1rem;
        }

        .success-message {
            padding: 3rem 2rem;
            text-align: center;
            display: none;
        }

        .success-icon {
            width: 80px;
            height: 80px;
            background: var(--accent);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: var(--bg-primary);
            margin: 0 auto 1.5rem;
        }

        .success-message h3 {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--accent);
            margin-bottom: 1rem;
        }

        .success-message p {
            color: var(--text-secondary);
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .dual-system {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .connector {
                transform: rotate(90deg);
            }
        }

        @media (max-width: 768px) {
            nav {
                padding: 1rem 0;
            }

            .nav-container {
                padding: 0 1.5rem;
            }

            .logo {
                font-size: 1.3rem;
            }

            .nav-cta {
                width: 42px;
                height: 42px;
            }

            .nav-cta svg {
                width: 18px;
                height: 18px;
            }

            .hero {
                padding: 6rem 1.5rem 3rem;
            }

            .problem,
            .solution,
            .global-reach,
            .benefits,
            .stats,
            .social-proof-section,
            .reviews-section,
            .about-section,
            .final-cta {
                padding: 5rem 1.5rem;
            }

            .section-header {
                margin-bottom: 3rem;
            }

            .problem-grid,
            .countries-grid,
            .benefits-grid,
            .stats-grid,
            .reviews-grid {
                gap: 1.5rem;
            }

            .carousel-container {
                padding: 0 50px;
            }

            .carousel-btn {
                width: 40px;
                height: 40px;
            }

            .carousel-btn svg {
                width: 20px;
                height: 20px;
            }

            .proof-card {
                min-height: 300px;
                padding: 2rem 1.5rem;
            }

            .about-content {
                grid-template-columns: 1fr;
                gap: 3rem;
            }

            .modal-content {
                width: 95%;
                margin: 1rem auto;
            }

            .form-header,
            #leadForm {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav id="navbar">
        <div class="nav-container">
            <div class="nav-spacer"></div>
            <div class="logo">
                <span class="logo-text">SCALE</span>
                <span class="logo-accent">AGENCY</span>
            </div>
            <button class="nav-cta" onclick="openModal()" aria-label="Entrar em contato">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"></path>
                </svg>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-bg"></div>
        <div class="hero-grid"></div>
        <div class="hero-content">
            <div class="hero-badge">🌍 Construímos brands globais de e-commerce</div>
            <h1>
                <span class="gradient-text">Marcas de alto nível</span><br>
                preparadas para operar globalmente.
            </h1>
            <p class="hero-subtitle">
                A Scale Agency não apenas cria lojas. Criamos estruturas profissionais prontas para escalar internacionalmente, com sistema de proteção Shopify dual que permite vender qualquer produto sem medo de perder sua Payments.
            </p>
            <button class="hero-cta" onclick="openModal()">
                Começar agora
                <span>→</span>
            </button>
        </div>
    </section>

    <!-- Problem Section -->
    <section class="problem">
        <div class="section-header">
            <div class="section-label">O Desafio</div>
            <h2 class="section-title">O medo que paralisa seu crescimento</h2>
            <p class="section-description">Perder a Shopify Payments é perder todo o seu negócio</p>
        </div>

        <div class="problem-grid">
            <div class="problem-card">
                <div class="problem-icon">🚫</div>
                <h3>Medo de testar produtos</h3>
                <p>Você não testa produtos diferentes com medo de uma reclamação derrubar sua conta Shopify Payments.</p>
            </div>

            <div class="problem-card">
                <div class="problem-icon">💳</div>
                <h3>Payments suspensa = game over</h3>
                <p>Uma única disputa ou violação pode suspender sua Shopify Payments e congelar toda sua receita.</p>
            </div>

            <div class="problem-card">
                <div class="problem-icon">⛔</div>
                <h3>Limitado ao "seguro"</h3>
                <p>Você só vende produtos ultra conservadores porque não pode arriscar perder tudo.</p>
            </div>
        </div>
    </section>

    <!-- Solution Section -->
    <section class="solution">
        <div class="solution-content">
            <div class="section-header">
                <div class="section-label">A Solução</div>
                <h2 class="section-title">Duas lojas, zero risco</h2>
                <p class="section-description">Rode o que quiser na Shopify Black. Sua Shopify Payments fica blindada.</p>
            </div>

            <div class="dual-system">
                <div class="system-card">
                    <div class="system-number">1</div>
                    <h3>SHOPIFY BLACK</h3>
                    <p class="system-role">Liberdade Total</p>
                    <ul class="system-features">
                        <li>Teste QUALQUER produto</li>
                        <li>Rode campanhas agressivas</li>
                        <li>Experimente sem medo</li>
                        <li>Valide novos nichos</li>
                    </ul>
                </div>

                <div class="connector">⚡</div>

                <div class="system-card">
                    <div class="system-number">2</div>
                    <h3>SHOPIFY PAYMENTS</h3>
                    <p class="system-role">100% Protegida</p>
                    <ul class="system-features">
                        <li>Shopify Payments intacta</li>
                        <li>Zero risco de suspensão</li>
                        <li>Compliance perfeito</li>
                        <li>Receita sempre fluindo</li>
                    </ul>
                </div>
            </div>

            <div class="integration-note">
                <p>✓ Cliente compra na Shopify Black, paga na loja segura<br>
                ✓ Integração invisível • Experiência perfeita • Payments blindada</p>
            </div>
        </div>
    </section>

    <!-- Global Reach Section -->
    <section class="global-reach">
        <div class="section-header">
            <div class="section-label">Operação Internacional</div>
            <h2 class="section-title">Opere globalmente com uma estrutura preparada para múltiplos mercados</h2>
            <p class="section-description">Sua marca pronta para conquistar os maiores mercados de e-commerce do mundo</p>
        </div>

        <div class="countries-grid">
            <div class="country-card">
                <div class="country-flag">🇺🇸</div>
                <h4>Estados Unidos</h4>
                <p>Maior mercado e-commerce mundial</p>
            </div>

            <div class="country-card">
                <div class="country-flag">🇨🇦</div>
                <h4>Canadá</h4>
                <p>Alto poder de compra e confiança</p>
            </div>

            <div class="country-card">
                <div class="country-flag">🇬🇧</div>
                <h4>Reino Unido</h4>
                <p>Gateway estratégico para Europa</p>
            </div>

            <div class="country-card">
                <div class="country-flag">🇪🇺</div>
                <h4>União Europeia</h4>
                <p>27 países, 450 milhões de consumidores</p>
            </div>

            <div class="country-card">
                <div class="country-flag">🇦🇺</div>
                <h4>Austrália</h4>
                <p>Mercado premium e em crescimento</p>
            </div>

            <div class="country-card">
                <div class="country-flag">🌍</div>
                <h4>+ 100 países</h4>
                <p>Infraestrutura para alcance mundial</p>
            </div>
        </div>

        <div class="global-stats">
            <div class="global-stat-item">
                <div class="global-stat-number">195+</div>
                <div class="global-stat-label">Países disponíveis</div>
            </div>
            <div class="global-stat-item">
                <div class="global-stat-number">135+</div>
                <div class="global-stat-label">Moedas suportadas</div>
            </div>
            <div class="global-stat-item">
                <div class="global-stat-number">24/7</div>
                <div class="global-stat-label">Operação global</div>
            </div>
        </div>
    </section>

    <!-- Benefits Section -->
    <section class="benefits">
        <div class="section-header">
            <div class="section-label">Infraestrutura Premium</div>
            <h2 class="section-title">Construímos brands globais de e-commerce</h2>
            <p class="section-description">Não apenas uma loja. Uma marca internacional completa.</p>
        </div>

        <div class="benefits-grid">
            <div class="benefit-card">
                <div class="benefit-icon">🌍</div>
                <h3>Marca global</h3>
                <p>Estrutura completa para operar em múltiplos países desde o primeiro dia</p>
            </div>

            <div class="benefit-card">
                <div class="benefit-icon">🔓</div>
                <h3>Liberdade total</h3>
                <p>Teste produtos e campanhas sem medo de perder sua Shopify Payments</p>
            </div>

            <div class="benefit-card">
                <div class="benefit-icon">🛡️</div>
                <h3>Payments blindada</h3>
                <p>Sistema dual que protege sua conta principal 24/7</p>
            </div>

            <div class="benefit-card">
                <div class="benefit-icon">💰</div>
                <h3>Escala internacional</h3>
                <p>Infraestrutura pronta para crescimento sem limites geográficos</p>
            </div>

            <div class="benefit-card">
                <div class="benefit-icon">⚡</div>
                <h3>Deploy rápido</h3>
                <p>Sua marca no ar e operando globalmente em tempo recorde</p>
            </div>

            <div class="benefit-card">
                <div class="benefit-icon">🎯</div>
                <h3>Compliance total</h3>
                <p>Estrutura legal e fiscal preparada para mercados internacionais</p>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="section-header">
            <div class="section-label">Resultados</div>
            <h2 class="section-title">Números que falam por si</h2>
            <p class="section-description">Resultados reais de quem protegeu sua Payments</p>
        </div>

        <div class="stats-grid">
            <div class="stat">
                <div class="stat-number">0</div>
                <div class="stat-label">Payments suspensas</div>
            </div>

            <div class="stat">
                <div class="stat-number">100%</div>
                <div class="stat-label">Receita protegida</div>
            </div>

            <div class="stat">
                <div class="stat-number">∞</div>
                <div class="stat-label">Produtos testados</div>
            </div>

            <div class="stat">
                <div class="stat-number">24/7</div>
                <div class="stat-label">Operação ativa</div>
            </div>
        </div>
    </section>

    <!-- Social Proof Section -->
    <section class="social-proof-section">
        <div class="social-proof-container">
            <div class="section-header">
                <div class="section-label">Prova Social</div>
                <h2 class="section-title">Mais de 10M faturados por clientes utilizando nossa estrutura</h2>
                <p class="section-description">Resultados reais de clientes reais.</p>
            </div>

            <div class="carousel-container">
                <div class="carousel-wrapper">
                    <div class="carousel-track">
                        <div class="proof-card">
                            <div class="proof-placeholder">
                                <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                    <rect x="3" y="3" width="18" height="18" rx="2" ry="2"></rect>
                                    <circle cx="8.5" cy="8.5" r="1.5"></circle>
                                    <polyline points="21 15 16 10 5 21"></polyline>
                                </svg>
                                <p>Print WhatsApp 1</p>
                            </div>
                        </div>

                        <div class="proof-card">
                            <div class="proof-placeholder">
                                <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                    <line x1="12" y1="1" x2="12" y2="23"></line>
                                    <path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"></path>
                                </svg>
                                <p>Resultado Shopify 1</p>
                            </div>
                        </div>

                        <div class="proof-card">
                            <div class="proof-placeholder">
                                <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                    <polyline points="22 12 18 12 15 21 9 3 6 12 2 12"></polyline>
                                </svg>
                                <p>Comprovante 1</p>
                            </div>
                        </div>

                        <div class="proof-card">
                            <div class="proof-placeholder">
                                <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                    <rect x="3" y="3" width="18" height="18" rx="2" ry="2"></rect>
                                    <circle cx="8.5" cy="8.5" r="1.5"></circle>
                                    <polyline points="21 15 16 10 5 21"></polyline>
                                </svg>
                                <p>Print WhatsApp 2</p>
                            </div>
                        </div>

                        <div class="proof-card">
                            <div class="proof-placeholder">
                                <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                    <line x1="12" y1="1" x2="12" y2="23"></line>
                                    <path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"></path>
                                </svg>
                                <p>Resultado Shopify 2</p>
                            </div>
                        </div>

                        <div class="proof-card">
                            <div class="proof-placeholder">
                                <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                    <polyline points="22 12 18 12 15 21 9 3 6 12 2 12"></polyline>
                                </svg>
                                <p>Comprovante 2</p>
                            </div>
                        </div>
                    </div>
                </div>

                <button class="carousel-btn carousel-prev" onclick="moveCarousel(-1)">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <polyline points="15 18 9 12 15 6"></polyline>
                    </svg>
                </button>
                <button class="carousel-btn carousel-next" onclick="moveCarousel(1)">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <polyline points="9 18 15 12 9 6"></polyline>
                    </svg>
                </button>

                <div class="carousel-dots">
                    <span class="dot active" onclick="goToSlide(0)"></span>
                    <span class="dot" onclick="goToSlide(1)"></span>
                    <span class="dot" onclick="goToSlide(2)"></span>
                    <span class="dot" onclick="goToSlide(3)"></span>
                    <span class="dot" onclick="goToSlide(4)"></span>
                    <span class="dot" onclick="goToSlide(5)"></span>
                </div>
            </div>

            <div class="proof-note">
                <p>💰 Estrutura validada por empreendedores que escalaram de 6 a 7 dígitos com segurança total</p>
            </div>
        </div>
    </section>

    <!-- Reviews Section -->
    <section class="reviews-section">
        <div class="reviews-container">
            <div class="section-header">
                <div class="section-label">Depoimentos</div>
                <h2 class="section-title">O que nossos clientes dizem</h2>
                <p class="section-description">Feedbacks reais de quem transformou seu e-commerce</p>
            </div>

            <div class="reviews-grid">
                <div class="review-card">
                    <div class="review-stars">★★★★★</div>
                    <p class="review-text">"Finalmente consigo testar produtos sem medo de perder minha conta. A estrutura dual mudou completamente meu negócio."</p>
                    <div class="review-author">
                        <div class="author-avatar">R.S.</div>
                        <div class="author-info">
                            <div class="author-name">R.S.</div>
                            <div class="author-role">E-commerce Owner</div>
                        </div>
                    </div>
                </div>

                <div class="review-card">
                    <div class="review-stars">★★★★★</div>
                    <p class="review-text">"Escalei de R$80k para R$500k/mês em 6 meses. A Shopify Payments nunca teve problema. Melhor investimento que fiz."</p>
                    <div class="review-author">
                        <div class="author-avatar">M.L.</div>
                        <div class="author-info">
                            <div class="author-name">M.L.</div>
                            <div class="author-role">Brand Owner</div>
                        </div>
                    </div>
                </div>

                <div class="review-card">
                    <div class="review-stars">★★★★★</div>
                    <p class="review-text">"Opero em 3 países diferentes com total tranquilidade. A estrutura internacional funciona perfeitamente."</p>
                    <div class="review-author">
                        <div class="author-avatar">A.F.</div>
                        <div class="author-info">
                            <div class="author-name">A.F.</div>
                            <div class="author-role">International Seller</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about-section">
        <div class="about-container">
            <div class="section-header">
                <div class="section-label">Sobre nós</div>
                <h2 class="section-title">Sobre a Scale Agency</h2>
            </div>

            <div class="about-content">
                <div class="about-text">
                    <p class="about-lead">
                        Fundada para resolver um dos maiores problemas do e-commerce: bloqueios e limitação de escala.
                    </p>
                    <p>
                        A Scale Agency não é apenas mais uma agência digital. Somos especialistas em criar infraestruturas globais de e-commerce que permitem empreendedores escalarem sem medo de perder tudo.
                    </p>
                    <p>
                        Nossa missão é clara: <strong>construir marcas de alto nível preparadas para operar globalmente</strong>, com estruturas que garantem liberdade total para testar produtos e campanhas, enquanto mantêm a Shopify Payments 100% protegida.
                    </p>
                    <p>
                        Combinamos tecnologia de ponta, conhecimento profundo da plataforma Shopify e anos de experiência em e-commerce internacional para entregar resultados que vão além de "criar uma loja".
                    </p>
                </div>

                <div class="about-features">
                    <div class="about-feature-item">
                        <div class="feature-icon">🎯</div>
                        <div class="feature-content">
                            <h4>Missão</h4>
                            <p>Escala global com segurança total</p>
                        </div>
                    </div>

                    <div class="about-feature-item">
                        <div class="feature-icon">🌍</div>
                        <div class="feature-content">
                            <h4>Alcance</h4>
                            <p>Estruturas em 195+ países</p>
                        </div>
                    </div>

                    <div class="about-feature-item">
                        <div class="feature-icon">🛡️</div>
                        <div class="feature-content">
                            <h4>Diferencial</h4>
                            <p>Sistema dual exclusivo</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="final-cta">
        <div class="cta-content">
            <h2>Pare de perder lojas.<br><span class="highlight">Comece a escalar.</span></h2>
            <p>Descubra como criar uma infraestrutura de e-commerce preparada para operar internacionalmente, com proteção total da sua Shopify Payments.</p>
            <button class="hero-cta" onclick="openModal()">
                Quero minha estrutura
                <span>→</span>
            </button>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-logo">
                <span class="logo-text">SCALE</span>
                <span class="logo-accent">AGENCY</span>
            </div>
            <p>&copy; 2026 Scale Agency. Infraestrutura escalável para e-commerce de alto desempenho.</p>
        </div>
    </footer>

    <!-- Modal Form -->
    <div id="formModal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal()">&times;</span>
            <div class="form-header">
                <h2>ESCALE COM SEGURANÇA</h2>
                <p>Preencha o formulário e receba uma análise gratuita</p>
            </div>

            <form id="leadForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
                <div class="form-group">
                    <label for="nome">Nome completo</label>
                    <input type="text" id="nome" name="nome" required placeholder="Seu nome completo">
                </div>

                <div class="form-group">
                    <label for="email">E-mail</label>
                    <input type="email" id="email" name="email" required placeholder="seu@email.com">
                </div>

                <div class="form-group">
                    <label for="whatsapp">WhatsApp (com DDD)</label>
                    <input type="tel" id="whatsapp" name="whatsapp" required placeholder="(61) 99999-9999">
                </div>

                <div class="form-group">
                    <label for="faturamento">Qual seu faturamento mensal atual?</label>
                    <select id="faturamento" name="faturamento" required>
                        <option value="">Selecione uma opção</option>
                        <option value="Ainda não vendo">Ainda não vendo</option>
                        <option value="Até R$5.000">Até R$5.000</option>
                        <option value="R$5.000 a R$20.000">R$5.000 a R$20.000</option>
                        <option value="R$20.000 a R$50.000">R$20.000 a R$50.000</option>
                        <option value="R$50.000+">R$50.000+</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="experiencia">Você já tem experiência com e-commerce?</label>
                    <select id="experiencia" name="experiencia" required>
                        <option value="">Selecione uma opção</option>
                        <option value="Nunca vendi online">Nunca vendi online</option>
                        <option value="Já vendi mas parei">Já vendi mas parei</option>
                        <option value="Vendo atualmente">Vendo atualmente</option>
                        <option value="Tenho várias lojas">Tenho várias lojas</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="desafios">Qual seu maior problema atual?</label>
                    <textarea id="desafios" name="desafios" rows="3" required placeholder="Ex: Medo de perder minha conta Shopify, quero expandir internacionalmente..."></textarea>
                </div>

                <button type="submit" class="form-submit">Quero escalar com segurança</button>

                <p class="form-disclaimer">
                    🔒 Seus dados estão 100% seguros. Entraremos em contato apenas para entender seu negócio.
                </p>
            </form>

            <div id="successMessage" class="success-message">
                <div class="success-icon">✓</div>
                <h3>Recebemos suas informações!</h3>
                <p>Em breve entraremos em contato para agendar sua análise gratuita.</p>
            </div>
        </div>
    </div>

    <script>
        // Carousel functionality
        let currentSlide = 0;
        const track = document.querySelector('.carousel-track');
        const slides = document.querySelectorAll('.proof-card');
        const dots = document.querySelectorAll('.dot');
        const totalSlides = slides.length;
        let autoPlayInterval;

        function updateCarousel() {
            const offset = -currentSlide * 100;
            track.style.transform = `translateX(${offset}%)`;
            
            // Update dots
            dots.forEach((dot, index) => {
                dot.classList.toggle('active', index === currentSlide);
            });
        }

        function moveCarousel(direction) {
            currentSlide += direction;
            
            if (currentSlide < 0) {
                currentSlide = totalSlides - 1;
            } else if (currentSlide >= totalSlides) {
                currentSlide = 0;
            }
            
            updateCarousel();
            resetAutoPlay();
        }

        function goToSlide(index) {
            currentSlide = index;
            updateCarousel();
            resetAutoPlay();
        }

        function autoPlay() {
            autoPlayInterval = setInterval(() => {
                moveCarousel(1);
            }, 4000); // Muda a cada 4 segundos
        }

        function resetAutoPlay() {
            clearInterval(autoPlayInterval);
            autoPlay();
        }

        // Start autoplay when page loads
        autoPlay();

        // Pause autoplay on hover
        const carouselContainer = document.querySelector('.carousel-container');
        carouselContainer.addEventListener('mouseenter', () => {
            clearInterval(autoPlayInterval);
        });
        carouselContainer.addEventListener('mouseleave', () => {
            autoPlay();
        });

        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Modal functions
        const modal = document.getElementById('formModal');
        const leadForm = document.getElementById('leadForm');
        const successMessage = document.getElementById('successMessage');

        function openModal() {
            modal.style.display = 'flex';
            document.body.style.overflow = 'hidden';
        }

        function closeModal() {
            modal.style.display = 'none';
            document.body.style.overflow = 'auto';
        }

        window.onclick = (e) => {
            if (e.target === modal) {
                closeModal();
            }
        };

        // Form submission
        leadForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            const formData = new FormData(leadForm);
            
            try {
                const response = await fetch(leadForm.action, {
                    method: 'POST',
                    body: formData,
                    headers: { 'Accept': 'application/json' }
                });

                if (response.ok) {
                    leadForm.style.display = 'none';
                    successMessage.style.display = 'block';
                    
                    setTimeout(() => {
                        closeModal();
                        leadForm.style.display = 'block';
                        successMessage.style.display = 'none';
                        leadForm.reset();
                    }, 3000);
                }
            } catch (error) {
                alert('Erro ao enviar. Tente novamente.');
            }
        });

        // WhatsApp mask
        document.getElementById('whatsapp').addEventListener('input', (e) => {
            let value = e.target.value.replace(/\D/g, '');
            if (value.length > 11) value = value.slice(0, 11);
            
            if (value.length > 6) {
                value = value.replace(/^(\d{2})(\d{5})(\d{0,4}).*/, '($1) $2-$3');
            } else if (value.length > 2) {
                value = value.replace(/^(\d{2})(\d{0,5})/, '($1) $2');
            } else if (value.length > 0) {
                value = value.replace(/^(\d*)/, '($1');
            }
            
            e.target.value = value;
        });
    </script>
</body>
</html>
