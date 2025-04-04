<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>lvl3.AI | AI Solutions for Domain Experts</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #0a2463;
            --primary-light: #3e92cc;
            --secondary: #1e293b;
            --accent: #3e92cc;
            --accent-bright: #55b0ec;
            --accent-secondary: #7c5295;
            --light: #f8fafc;
            --dark: #1e293b;
            --text: #334155;
            --text-light: #f8fafc;
            --background: #ffffff;
            --gradient-bg: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            --gradient-accent: linear-gradient(135deg, var(--accent) 0%, var(--accent-secondary) 100%);
            --section-padding: 100px 0;
            --slide-min-height: 100vh;
            --border-radius: 12px;
            --card-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
            scroll-padding-top: 70px;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: var(--light);
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--secondary);
            line-height: 1.2;
        }
        
        p {
            margin-bottom: 1rem;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 30px;
        }
        
        .slide {
            min-height: var(--slide-min-height);
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: var(--section-padding);
            position: relative;
        }
        
        /* Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: var(--primary);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s ease;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 18px 30px;
        }
        
        .logo {
            font-size: 22px;
            font-weight: 700;
            color: var(--text-light);
            text-decoration: none;
            letter-spacing: 0.5px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        
        nav ul li a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            font-size: 15px;
            transition: var(--transition);
            opacity: 0.9;
        }
        
        nav ul li a:hover {
            opacity: 1;
            color: var(--accent-bright);
        }
        
        /* Title Slide */
        .title-slide {
            background: var(--gradient-bg);
            color: var(--text-light);
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .title-slide::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('/api/placeholder');
            background-size: cover;
            opacity: 0.1;
            z-index: 0;
        }
        
        .title-slide .container {
            position: relative;
            z-index: 1;
        }
        
        .title-slide h1 {
            font-size: 4rem;
            margin-bottom: 20px;
            color: var(--text-light);
            letter-spacing: 1px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }
        
        .title-slide p {
            font-size: 1.6rem;
            margin-bottom: 30px;
            opacity: 0.9;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            font-weight: 300;
            line-height: 1.5;
        }
        
        /* Section Styling */
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 3rem;
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
            color: var(--primary);
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background-color: var(--accent);
        }
        
        .highlight-text {
            color: var(--accent);
        }
        
        /* Content Styling */
        .content-block {
            margin-bottom: 60px;
        }
        
        .content-block h3 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 25px;
        }
        
        .content-block p {
            font-size: 1.1rem;
            line-height: 1.7;
            margin-bottom: 20px;
        }
        
        /* Feature Cards */
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .feature-card {
            background-color: var(--background);
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 40px;
            transition: var(--transition);
            border-top: 4px solid var(--primary);
        }
        
        .feature-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
            border-top: 4px solid var(--accent-bright);
        }
        
        .feature-icon {
            background-color: rgba(62, 146, 204, 0.1);
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 25px;
        }
        
        .feature-icon i {
            font-size: 28px;
            color: var(--primary);
        }
        
        .feature-card:hover .feature-icon {
            background-color: rgba(62, 146, 204, 0.2);
        }
        
        .feature-card:hover .feature-icon i {
            color: var(--accent-bright);
        }
        
        .feature-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        /* Process Steps */
        .process-flow {
            position: relative;
            margin: 70px 0;
        }
        
        .process-step {
            display: flex;
            margin-bottom: 70px;
            position: relative;
        }
        
        .process-step:last-child {
            margin-bottom: 0;
        }
        
        .process-number {
            flex-shrink: 0;
            width: 80px;
            height: 80px;
            background: var(--gradient-bg);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 30px;
            font-weight: 700;
            margin-right: 40px;
            position: relative;
            z-index: 2;
            box-shadow: 0 5px 15px rgba(10, 36, 99, 0.2);
        }
        
        .process-content {
            background-color: var(--background);
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 30px 40px;
            flex-grow: 1;
            border-left: 3px solid var(--accent);
        }
        
        .process-title {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .process-flow::before {
            content: '';
            position: absolute;
            top: 40px;
            left: 40px;
            width: 2px;
            height: calc(100% - 80px);
            background-color: rgba(62, 146, 204, 0.3);
            z-index: 1;
        }
        
        /* Stats and Metrics */
        .stats-row {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            gap: 30px;
            margin: 50px 0;
        }
        
        .stat-card {
            text-align: center;
            flex: 1;
            min-width: 200px;
            max-width: 300px;
            background-color: var(--background);
            padding: 40px 25px;
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border-bottom: 3px solid var(--accent);
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08);
            border-bottom-color: var(--accent-bright);
        }
        
        .stat-value {
            font-size: 3rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 15px;
            line-height: 1;
        }
        
        .stat-label {
            font-size: 1.1rem;
            color: var(--text);
            font-weight: 500;
        }
        
        /* Team Section */
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 30px;
        }
        
        .team-member {
            background-color: var(--background);
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            overflow: hidden;
            transition: var(--transition);
            border-top: 4px solid var(--primary);
            padding: 10px 0;
        }
        
        .team-member:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
            border-top: 4px solid var(--accent-bright);
        }
        
        .team-info {
            padding: 30px;
        }
        
        .team-name {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 5px;
        }
        
        .team-role {
            font-size: 1.1rem;
            color: var(--accent);
            margin-bottom: 15px;
            font-weight: 500;
        }
        
        .team-bio {
            margin-bottom: 20px;
            line-height: 1.6;
        }
        
        .advisors-section {
            margin-top: 70px;
        }
        
        .advisor-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .advisor-card {
            background-color: var(--background);
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 30px;
            text-align: center;
            transition: var(--transition);
            border-bottom: 3px solid var(--accent-secondary);
        }
        
        .advisor-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08);
            border-bottom-color: var(--accent);
        }
        
        .advisor-role {
            font-size: 1rem;
            color: var(--accent);
            margin-bottom: 10px;
            font-weight: 500;
        }
        
        /* Roadmap */
        .roadmap {
            margin: 60px 0;
        }
        
        .roadmap-container {
            display: flex;
            flex-wrap: wrap;
            position: relative;
            gap: 30px;
        }
        
        .roadmap-item {
            flex: 1;
            min-width: 250px;
            background-color: var(--background);
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 30px;
            transition: var(--transition);
            border-top: 4px solid var(--primary);
        }
        
        .roadmap-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            border-top-color: var(--accent-bright);
        }
        
        .roadmap-date {
            font-weight: 700;
            font-size: 1.2rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        /* CTA Section */
        .cta-slide {
            background: var(--gradient-bg);
            color: var(--text-light);
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .cta-slide::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('/api/placeholder');
            background-size: cover;
            opacity: 0.05;
            z-index: 0;
        }
        
        .cta-slide .container {
            position: relative;
            z-index: 1;
        }
        
        .cta-slide h2 {
            color: var(--text-light);
            font-size: 3rem;
            margin-bottom: 25px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }
        
        .cta-slide p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 50px;
            opacity: 0.9;
            font-weight: 300;
        }
        
        .btn-primary {
            display: inline-block;
            padding: 16px 40px;
            background-color: var(--text-light);
            color: var(--primary);
            text-decoration: none;
            font-weight: 600;
            border-radius: 50px;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1.1rem;
            letter-spacing: 0.5px;
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            background-color: #fff;
        }
        
        /* Highlight Box */
        .highlight-box {
            background: var(--gradient-accent);
            color: white;
            padding: 40px;
            border-radius: var(--border-radius);
            margin: 50px 0;
            box-shadow: 0 15px 30px rgba(62, 146, 204, 0.2);
        }
        
        .highlight-box h3 {
            color: white;
            font-size: 1.8rem;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .highlight-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .highlight-item h4 {
            color: white;
            margin-bottom: 10px;
            font-size: 1.3rem;
        }
        
        /* Market Size Section */
        .market-stats {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin: 50px 0;
            gap: 30px;
        }
        
        .market-stat {
            flex: 1;
            min-width: 220px;
            max-width: 320px;
            background: var(--background);
            padding: 30px;
            border-radius: var(--border-radius);
            text-align: center;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border-bottom: 3px solid var(--accent-secondary);
        }
        
        .market-stat:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08);
            border-bottom-color: var(--accent-bright);
        }
        
        .market-value {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .market-label {
            font-size: 1.1rem;
            color: var(--text);
            font-weight: 500;
        }
        
        .market-growth {
            margin-top: 10px;
            font-size: 1rem;
            color: #2ecc71;
            font-weight: 600;
        }
        
        /* Testimonials */
        .testimonials {
            margin: 70px 0;
        }
        
        .testimonial-card {
            background-color: var(--background);
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            padding: 30px;
            margin-bottom: 30px;
            position: relative;
            border-left: 4px solid var(--accent);
        }
        
        .testimonial-card::before {
            content: '"';
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 60px;
            font-family: Georgia, serif;
            color: rgba(62, 146, 204, 0.2);
            line-height: 1;
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
            padding-left: 40px;
        }
        
        .testimonial-author {
            font-weight: 700;
            color: var(--primary);
        }
        
        .testimonial-position {
            color: var(--accent);
            font-size: 0.9rem;
        }
        
        /* Technology Section */
        .tech-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 30px 0;
        }
        
        .tech-badge {
            background-color: var(--background);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--primary);
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }
        
        .tech-badge:hover {
            background-color: var(--primary);
            color: var(--text-light);
            transform: translateY(-2px);
        }
        
        /* Footer */
        footer {
            background-color: var(--secondary);
            color: var(--text-light);
            padding: 40px 0;
            text-align: center;
        }
        
        footer p {
            opacity: 0.8;
            font-size: 0.9rem;
        }
        
        /* Animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animate-in {
            animation: fadeIn 0.6s ease forwards;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .title-slide h1 {
                font-size: 3.5rem;
            }
            
            .title-slide p {
                font-size: 1.4rem;
            }
            
            .section-title h2 {
                font-size: 2.5rem;
            }
            
            .process-number {
                width: 70px;
                height: 70px;
                font-size: 26px;
                margin-right: 30px;
            }
            
            .process-flow::before {
                left: 35px;
            }
        }
        
        @media (max-width: 768px) {
            .title-slide h1 {
                font-size: 3rem;
            }
            
            .title-slide p {
                font-size: 1.3rem;
            }
            
            .section-title h2 {
                font-size: 2.2rem;
            }
            
            .process-step {
                flex-direction: column;
            }
            
            .process-number {
                margin-bottom: 20px;
                margin-right: 0;
            }
            
            .process-flow::before {
                display: none;
            }
        }
        
        @media (max-width: 576px) {
            .title-slide h1 {
                font-size: 2.5rem;
            }
            
            .title-slide p {
                font-size: 1.2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .cta-slide h2 {
                font-size: 2.2rem;
            }
            
            .cta-slide p {
                font-size: 1.1rem;
            }
            
            .btn-primary {
                padding: 14px 30px;
                font-size: 1rem;
            }
        }
        
        .core-goals {
            margin-top: 60px;
            text-align: center;
        }
        
        .core-goals h3 {
            color: var(--text-light);
            font-size: 2rem;
            margin-bottom: 40px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }
        
        .goals-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        
        .goal-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: var(--border-radius);
            padding: 30px;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .goal-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.15);
            border-color: rgba(255, 255, 255, 0.3);
        }
        
        .goal-icon {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
        }
        
        .goal-icon i {
            font-size: 24px;
            color: var(--text-light);
        }
        
        .goal-card h4 {
            color: var(--text-light);
            font-size: 1.3rem;
            margin-bottom: 15px;
        }
        
        .goal-card p {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1rem;
            line-height: 1.6;
        }
        
        @media (max-width: 768px) {
            .goals-grid {
                grid-template-columns: 1fr;
            }
            
            .core-goals h3 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header Navigation -->
    <header>
        <div class="header-container">
            <a href="#" class="logo">lvl3.AI</a>
            <nav>
                <ul>
                    <li><a href="#problem">Problem</a></li>
                    <li><a href="#solution">Solution</a></li>
                    <li><a href="#how-it-works">Process</a></li>
                    <li><a href="#market">Market</a></li>
                    <li><a href="#tech">Technology</a></li>
                    <li><a href="#verticals">Verticals</a></li>
                    <li><a href="#business">Business</a></li>
                    <li><a href="#roadmap">Roadmap</a></li>
                    <li><a href="#team">Team</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Title Slide -->
    <section class="slide title-slide" id="home">
        <div class="container">
            <h1>lvl3.AI</h1>
            <p>Empowering domain experts to deploy powerful AI agent solutions that work for their unique needs</p>
            
            <div class="core-goals">
                <h3>2025 Core Goals</h3>
                <div class="goals-grid">
                    <div class="goal-card">
                        <div class="goal-icon">
                            <i class="fas fa-trophy"></i>
                        </div>
                        <h4>GAIA Level 3 Leadership</h4>
                        <p>Achieve the top spot on the GAIA Level 3 benchmark, surpassing Manus.AI to establish new standards in AI performance.</p>
                    </div>
                    
                    <div class="goal-card">
                        <div class="goal-icon">
                            <i class="fas fa-code"></i>
                        </div>
                        <h4>Seamless Integration</h4>
                        <p>Enable direct embedding of our General AI system into client platforms, similar to Stripe's payment integration, for frictionless AI deployment.</p>
                    </div>
                    
                    <div class="goal-card">
                        <div class="goal-icon">
                            <i class="fas fa-database"></i>
                        </div>
                        <h4>Domain-Specific Intelligence</h4>
                        <p>Empower clients with 100GB+ data capacity for agentic RAG, creating highly specialized General AI systems with deep domain context.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Problem Slide -->
    <section class="slide" id="problem">
        <div class="container">
            <div class="section-title">
                <h2>The Challenge</h2>
            </div>
            
            <div class="content-block">
                <h3>Domain experts need AI solutions that understand their specialized knowledge</h3>
                <p>In today's rapidly evolving AI landscape, domain experts across industries have valuable specialized knowledge that could be enhanced through AI agents. However, translating this expertise into effective AI solutions presents significant challenges.</p>
            </div>
            
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3 class="feature-title">Complex Knowledge Integration</h3>
                    <p>Existing AI tools often fail to properly integrate specialized domain knowledge, resulting in generic solutions that miss critical industry-specific nuances.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-server"></i>
                    </div>
                    <h3 class="feature-title">Infrastructure Complexity</h3>
                    <p>Building and maintaining specialized AI infrastructure requires expertise in both AI systems and domain-specific requirements, creating unnecessary complexity.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3 class="feature-title">Time to Value</h3>
                    <p>The time required to develop, deploy, and iterate on specialized AI solutions delays the realization of business value and competitive advantages.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-puzzle-piece"></i>
                    </div>
                    <h3 class="feature-title">Siloed Knowledge</h3>
                    <p>Domain-specific AI tools often operate in isolation, preventing cross-domain insights and limiting the potential of AI to solve complex interdisciplinary problems.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Solution Slide -->
    <section class="slide" id="solution">
        <div class="container">
            <div class="section-title">
                <h2>Our Solution</h2>
            </div>
            
            <div class="content-block">
                <h3>We provide the infrastructure for domain experts to deploy specialized AI agents</h3>
                <p>lvl3.AI complements your domain expertise with our AI infrastructure, enabling you to rapidly deploy powerful agentic solutions tailored to your specific industry needs.</p>
            </div>
            
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-database"></i>
                    </div>
                    <h3 class="feature-title">Agentic RAG Vector Database</h3>
                    <p>We host and maintain a sophisticated vector database that powers your AI agents with domain-specific knowledge, continuously improving as more data is processed.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-puzzle-piece"></i>
                    </div>
                    <h3 class="feature-title">Specialized Agent Workflows</h3>
                    <p>Our platform develops and refines industry-specific agent workflows that understand the unique processes, terminology, and requirements of your vertical.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-plug"></i>
                    </div>
                    <h3 class="feature-title">Seamless Integration</h3>
                    <p>Deploy your AI solution directly into your existing website or applications through our simple integration options, maintaining your brand experience.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-sync-alt"></i>
                    </div>
                    <h3 class="feature-title">Virtuous Learning Cycle</h3>
                    <p>Your domain-specific data enriches our vector database, creating a virtuous cycle that continuously improves the performance of AI agents across similar use cases.</p>
                </div>
            </div>
            
            <div class="testimonials">
                <div class="testimonial-card">
                    <p class="testimonial-text">This platform has significantly improved our compliance workflow and documentation processes. The specialized agents truly understand our regulatory needs and have made a remarkable difference in how we approach compliance challenges.</p>
                    <div class="testimonial-author">1st Client</div>
                    <div class="testimonial-position">Stanford MBA, Entrepreneur</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Market Size Section (NEW) -->
    <section class="slide" id="market">
        <div class="container">
            <div class="section-title">
                <h2>Market Opportunity</h2>
            </div>
            
            <div class="content-block">
                <h3>The booming AI agent market presents immense growth potential</h3>
                <p>The global AI agent market is experiencing unprecedented growth as businesses across industries recognize the transformative potential of specialized, domain-specific AI solutions. Our position at the intersection of domain expertise and AI infrastructure places us at the forefront of this expanding market.</p>
            </div>
            
            <div class="market-stats">
                <div class="market-stat">
                    <div class="market-value">$92B</div>
                    <div class="market-label">Global AI Agent Market Size (2025)</div>
                    <div class="market-growth">Growing at 38% CAGR</div>
                </div>
                
                <div class="market-stat">
                    <div class="market-value">$312B</div>
                    <div class="market-label">Projected Market Size by 2030</div>
                    <div class="market-growth">3.4x growth in 5 years</div>
                </div>
                
                <div class="market-stat">
                    <div class="market-value">67%</div>
                    <div class="market-label">Enterprises Adopting AI Agents</div>
                    <div class="market-growth">Up from 23% in 2023</div>
                </div>
            </div>
            
            <div class="highlight-box">
                <h3>Why Domain-Specific AI is the Future</h3>
                <div class="highlight-grid">
                    <div class="highlight-item">
                        <h4>Targeted Value Creation</h4>
                        <p>Domain-specific AI solutions deliver 3-5x more business value than generic AI applications by addressing industry-specific challenges.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>Competitive Advantage</h4>
                        <p>Organizations deploying specialized AI agents are seeing 42% improvement in operational efficiency compared to competitors using general-purpose AI.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>Accelerating Adoption</h4>
                        <p>The market for specialized AI agents is growing 1.5x faster than the overall AI market as businesses seek solutions tailored to their specific needs.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- How It Works Slide -->
    <section class="slide" id="how-it-works">
        <div class="container">
            <div class="section-title">
                <h2>Our Process</h2>
            </div>
            
            <div class="process-flow">
                <div class="process-step">
                    <div class="process-number">1</div>
                    <div class="process-content">
                        <h3 class="process-title">Domain Knowledge Capture</h3>
                        <p>We work closely with you to understand your specialized industry knowledge, key workflows, and unique requirements that will form the foundation of your AI solution.</p>
                    </div>
                </div>
                
                <div class="process-step">
                    <div class="process-number">2</div>
                    <div class="process-content">
                        <h3 class="process-title">Custom Agent Development</h3>
                        <p>Our team builds custom AI agents designed specifically for your use case, incorporating your domain expertise into our agentic RAG framework.</p>
                    </div>
                </div>
                
                <div class="process-step">
                    <div class="process-number">3</div>
                    <div class="process-content">
                        <h3 class="process-title">Vector Database Integration</h3>
                        <p>Your domain-specific data is processed and integrated into our vector database, enabling sophisticated retrieval and reasoning capabilities tailored to your industry.</p>
                    </div>
                </div>
                
                <div class="process-step">
                    <div class="process-number">4</div>
                    <div class="process-content">
                        <h3 class="process-title">Deployment & Integration</h3>
                        <p>We deploy your AI solution and provide simple integration options for your website or applications, allowing you to immediately deliver value to your clients.</p>
                    </div>
                </div>
                
                <div class="process-step">
                    <div class="process-number">5</div>
                    <div class="process-content">
                        <h3 class="process-title">Continuous Improvement</h3>
                        <p>As your solution processes more domain-specific data, our system continuously learns and improves, creating a virtuous cycle that enhances performance for you and similar use cases.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Technology Section -->
    <section class="slide" id="tech">
        <div class="container">
            <div class="section-title">
                <h2>Our Technology</h2>
            </div>
            
            <div class="content-block">
                <h3>Built on cutting-edge AI infrastructure</h3>
                <p>Our platform is powered by state-of-the-art AI technologies that enable unprecedented performance in domain-specific applications.</p>
            </div>
            
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-microchip"></i>
                    </div>
                    <h3 class="feature-title">Optimized Hardware Architecture</h3>
                    <p>Our custom hardware designs specifically optimized for AI agent operations deliver exceptional performance while minimizing energy consumption and operational costs.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-network-wired"></i>
                    </div>
                    <h3 class="feature-title">Advanced Vector Database</h3>
                    <p>Our proprietary vector database technology enables lightning-fast retrieval of relevant domain knowledge, ensuring your agents respond with accuracy and context awareness.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-robot"></i>
                    </div>
                    <h3 class="feature-title">Multi-Agent Orchestration</h3>
                    <p>Our platform coordinates multiple specialized agents working in concert to tackle complex problems that span different knowledge domains and operational contexts.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Verticals Slide -->
    <section class="slide" id="verticals">
        <div class="container">
            <div class="section-title">
                <h2>Specialized Verticals</h2>
            </div>
            
            <div class="content-block">
                <h3>We're focused on high-impact specialized domains</h3>
                <p>Our platform is designed to excel in complex, knowledge-intensive verticals where domain expertise makes the difference between generic AI and truly transformative solutions.</p>
            </div>
            
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-microchip"></i>
                    </div>
                    <h3 class="feature-title">PCB Generation</h3>
                    <p>AI agents that understand electronic design requirements and can assist in generating printed circuit board layouts, component selection, and testing procedures.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-file-contract"></i>
                    </div>
                    <h3 class="feature-title">Compliance Documentation</h3>
                    <p>Specialized agents that understand regulatory requirements across industries and can generate, review, and maintain compliant documentation with minimal human oversight.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-chart-bar"></i>
                    </div>
                    <h3 class="feature-title">Data Gathering & Aggregation</h3>
                    <p>Intelligent agents that can collect, process, and synthesize data from multiple sources, creating structured insights tailored to specific industry requirements.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-industry"></i>
                    </div>
                    <h3 class="feature-title">Manufacturing Optimization</h3>
                    <p>Specialized agents that analyze production data to optimize manufacturing processes, predict equipment failures, and recommend efficiency improvements.</p>
                </div>
            </div>
            
            <div class="highlight-box">
                <h3>Why These Verticals Matter</h3>
                <div class="highlight-grid">
                    <div class="highlight-item">
                        <h4>Complex Domain Knowledge</h4>
                        <p>These fields require deep specialized expertise that generic AI solutions simply cannot provide without proper domain understanding.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>Significant Time Savings</h4>
                        <p>Our AI agents can reduce weeks of work to hours, dramatically accelerating processes that typically require significant manual effort.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>High Business Impact</h4>
                        <p>These domains represent critical business functions where efficiency and accuracy directly impact bottom-line performance and compliance.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Business Model Slide -->
    <section class="slide" id="business">
        <div class="container">
            <div class="section-title">
                <h2>Business Model</h2>
            </div>
            
            <div class="content-block">
                <h3>Simple, transparent pricing that scales with your success</h3>
                <p>Our business model is designed to align our success with yours, providing the infrastructure you need at a predictable cost while allowing you to scale efficiently.</p>
            </div>
            
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-dollar-sign"></i>
                    </div>
                    <h3 class="feature-title">Flat Monthly Fee</h3>
                    <p>$100 monthly base fee for hosting and maintaining your specialized AI agents, providing predictable operational costs as you grow your business.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="feature-title">Usage-Based Surcharge</h3>
                    <p>2-5% surcharge applied only when LLM usage exceeds standard limits, ensuring you only pay extra for significant scale and high-volume processing.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-handshake"></i>
                    </div>
                    <h3 class="feature-title">White-Label Options</h3>
                    <p>Deploy our AI agents under your own brand, allowing you to maintain your client relationships while leveraging our powerful infrastructure.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3 class="feature-title">Enterprise Solutions</h3>
                    <p>Custom pricing and dedicated infrastructure for large-scale implementations with specialized security, compliance, and performance requirements.</p>
                </div>
            </div>
            
            <div class="highlight-box">
                <h3>Domain Expert Benefits</h3>
                <div class="highlight-grid">
                    <div class="highlight-item">
                        <h4>Focus on Your Expertise</h4>
                        <p>Concentrate on your domain knowledge and client relationships while we handle the technical AI infrastructure.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>Rapid Time to Market</h4>
                        <p>Launch specialized AI solutions in days rather than months, capturing market opportunities as they emerge.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>Profitable Margins</h4>
                        <p>Maintain high margins by offering sophisticated AI capabilities with minimal fixed costs and predictable scaling.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Roadmap Slide -->
    <section class="slide" id="roadmap">
        <div class="container">
            <div class="section-title">
                <h2>Roadmap & Vision</h2>
            </div>
            
            <div class="content-block">
                <h3>Building a library of specialized agents across multiple verticals</h3>
                <p>Our vision is to create the world's most comprehensive collection of domain-specific AI agents, powered by a continuously improving vector database that gets smarter with every interaction.</p>
            </div>
            
            <div class="roadmap">
                <div class="roadmap-container">
                    <div class="roadmap-item">
                        <div class="roadmap-date">Q2 2025</div>
                        <h3>Vertical Expansion</h3>
                        <p>Expand beyond our initial verticals to include financial analysis, legal document processing, and medical research assistance, broadening our domain expertise.</p>
                    </div>
                    
                    <div class="roadmap-item">
                        <div class="roadmap-date">Q3 2025</div>
                        <h3>Off-the-Shelf Agent Library</h3>
                        <p>Launch our repository of pre-built agent workflows that can be instantly deployed across similar use cases, dramatically reducing time to market.</p>
                    </div>
                    
                    <div class="roadmap-item">
                        <div class="roadmap-date">Q4 2025</div>
                        <h3>Advanced Customization Tools</h3>
                        <p>Introduce no-code tools that allow domain experts to customize agent workflows without technical expertise, further accelerating deployment.</p>
                    </div>
                    
                    <div class="roadmap-item">
                        <div class="roadmap-date">Q1 2026</div>
                        <h3>Cross-Domain Intelligence</h3>
                        <p>Develop capabilities for agents to leverage insights across related domains, creating more powerful solutions that understand complex interdisciplinary challenges.</p>
                    </div>
                </div>
            </div>
            
            <div class="highlight-box">
                <h3>The Virtuous Knowledge Cycle</h3>
                <div class="highlight-grid">
                    <div class="highlight-item">
                        <h4>Domain-Specific Data Enrichment</h4>
                        <p>Every interaction with your specialized agents contributes to our vector database, enhancing the knowledge available to future solutions.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>Cross-Vertical Learning</h4>
                        <p>Insights gained from one vertical can inform and improve agent performance in related domains, creating compound intelligence growth.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>Expanding Agent Capabilities</h4>
                        <p>As our system processes more domain-specific interactions, our agents develop increasingly sophisticated understanding and problem-solving abilities.</p>
                    </div>
                    <div class="highlight-item">
                        <h4>Advanced Optimization</h4>
                        <p>Our proprietary algorithms continuously improve vector database performance and agent reasoning capabilities.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Team Slide -->
    <section class="slide" id="team">
        <div class="container">
            <div class="section-title">
                <h2>Co-Founders</h2>
            </div>
            
            <div class="content-block">
                <h3>Founded by experts at the intersection of AI and domain knowledge</h3>
            </div>
            
            <div class="team-grid">
                <div class="team-member">
                    <div class="team-info">
                        <h3 class="team-name">Spencer Brown</h3>
                        <div class="team-role">Co-Founder & CTO</div>
                        <p class="team-bio">Master of Finance from Harvard Extension with extensive experience in quantum computing. Previously founded a Quantum Computing Hardware & Software firm, bringing deep technical expertise and entrepreneurial vision to lvl3.AI.</p>
                    </div>
                </div>
                
                <div class="team-member">
                    <div class="team-info">
                        <h3 class="team-name">Omar</h3>
                        <div class="team-role">Co-Founder & CEO</div>
                        <p class="team-bio">Experienced leader with a strong background in AI implementation and business strategy. Omar brings vision and direction to lvl3.AI's mission of empowering domain experts with specialized AI solutions.</p>
                    </div>
                </div>
                
                <div class="team-member">
                    <div class="team-info">
                        <h3 class="team-name">Sam</h3>
                        <div class="team-role">Co-Founder & CPO</div>
                        <p class="team-bio">Product development expert with a focus on creating intuitive AI interfaces that effectively bridge the gap between complex domain knowledge and practical AI applications.</p>
                    </div>
                </div>
                
                <div class="team-member">
                    <div class="team-info">
                        <h3 class="team-name">Khaled</h3>
                        <div class="team-role">Co-Founder & CMO</div>
                        <p class="team-bio">Marketing strategist with extensive experience in AI and SaaS growth. Khaled leads lvl3.AI's efforts to connect domain experts with the right AI solutions for their specialized needs.</p>
                    </div>
                </div>
            </div>
            

        </div>
    </section>

    <!-- CTA Slide -->
    <section class="slide cta-slide" id="contact">
        <div class="container">
            <h2>Transform Your Domain Expertise Into Powerful AI Solutions</h2>
            <p>Let us handle the AI infrastructure while you focus on what you do best: delivering specialized value in your domain.</p>
            
            <a href="#" class="btn-primary">Contact Us</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2025 lvl3.AI. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Smooth Scrolling for Anchor Links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 70,
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // Header Background Change on Scroll
            const header = document.querySelector('header');
            window.addEventListener('scroll', function() {
                if (window.scrollY > 100) {
                    header.style.backgroundColor = 'rgba(10, 36, 99, 0.95)';
                } else {
                    header.style.backgroundColor = 'var(--primary)';
                }
            });
            
            // Animation on Scroll
            const animateElements = document.querySelectorAll('.feature-card, .process-step, .stat-card, .team-member, .advisor-card, .roadmap-item, .market-stat');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animate-in');
                        observer.unobserve(entry.target);
                    }
                });
            }, {
                threshold: 0.1
            });
            
            animateElements.forEach(element => {
                observer.observe(element);
            });
        });
    </script>
</body>
</html>
