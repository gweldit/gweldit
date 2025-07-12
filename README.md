<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ghebrebrhan Weldit - Research Associate</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .profile-header {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .profile-header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            animation: shimmer 3s infinite;
        }
        
        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }
        
        .visitor-badge {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 12px;
            color: white;
            backdrop-filter: blur(5px);
        }
        
        .typing-animation {
            font-size: 2.5rem;
            font-weight: bold;
            color: white;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            position: relative;
            z-index: 1;
        }
        
        .wave {
            animation: wave 2s infinite;
            display: inline-block;
        }
        
        @keyframes wave {
            0%, 20%, 60%, 100% { transform: rotate(0deg); }
            10% { transform: rotate(14deg); }
            30% { transform: rotate(-8deg); }
            40% { transform: rotate(14deg); }
            50% { transform: rotate(-4deg); }
            70% { transform: rotate(10deg); }
        }
        
        .role-title {
            font-size: 1.3rem;
            color: #e0e0e0;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }
        
        .role-title a {
            color: #ffd700;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .role-title a:hover {
            color: #ffed4e;
        }
        
        .description {
            font-size: 1.1rem;
            color: #f0f0f0;
            max-width: 600px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }
        
        .info-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .info-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .info-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        
        .info-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            color: white;
        }
        
        .info-item:last-child {
            margin-bottom: 0;
        }
        
        .info-icon {
            font-size: 1.2rem;
            margin-right: 12px;
            min-width: 25px;
        }
        
        .info-text {
            flex: 1;
        }
        
        .info-text strong {
            color: #ffd700;
        }
        
        .info-text a {
            color: #87ceeb;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .info-text a:hover {
            color: #b6e5ff;
        }
        
        .projects-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 30px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .section-title {
            font-size: 1.8rem;
            color: white;
            margin-bottom: 25px;
            text-align: center;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .project-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            padding: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            transition: background 0.3s ease;
        }
        
        .project-item:hover {
            background: rgba(255, 255, 255, 0.1);
        }
        
        .project-icon {
            font-size: 1.5rem;
            margin-right: 15px;
            min-width: 30px;
        }
        
        .project-text {
            color: #f0f0f0;
            flex: 1;
        }
        
        .project-text a {
            color: #87ceeb;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .project-text a:hover {
            color: #b6e5ff;
        }
        
        .current-work {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .work-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
            padding: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            transition: background 0.3s ease;
        }
        
        .work-item:hover {
            background: rgba(255, 255, 255, 0.1);
        }
        
        .work-icon {
            font-size: 1.3rem;
            margin-right: 15px;
            margin-top: 2px;
            min-width: 25px;
        }
        
        .work-text {
            color: #f0f0f0;
            flex: 1;
        }
        
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .floating-element {
            position: absolute;
            opacity: 0.1;
            animation: float 20s infinite linear;
        }
        
        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); }
            100% { transform: translateY(-100px) rotate(360deg); }
        }
        
        .floating-element:nth-child(1) { left: 10%; animation-delay: 0s; }
        .floating-element:nth-child(2) { left: 20%; animation-delay: 2s; }
        .floating-element:nth-child(3) { left: 30%; animation-delay: 4s; }
        .floating-element:nth-child(4) { left: 40%; animation-delay: 6s; }
        .floating-element:nth-child(5) { left: 50%; animation-delay: 8s; }
        .floating-element:nth-child(6) { left: 60%; animation-delay: 10s; }
        .floating-element:nth-child(7) { left: 70%; animation-delay: 12s; }
        .floating-element:nth-child(8) { left: 80%; animation-delay: 14s; }
        .floating-element:nth-child(9) { left: 90%; animation-delay: 16s; }
        
        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            
            .profile-header {
                padding: 20px;
            }
            
            .typing-animation {
                font-size: 1.8rem;
            }
            
            .info-cards {
                grid-template-columns: 1fr;
            }
            
            .visitor-badge {
                position: static;
                margin-bottom: 20px;
                display: inline-block;
            }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-element">🔬</div>
        <div class="floating-element">🤖</div>
        <div class="floating-element">🛡️</div>
        <div class="floating-element">🧠</div>
        <div class="floating-element">📊</div>
        <div class="floating-element">🔍</div>
        <div class="floating-element">💻</div>
        <div class="floating-element">🎯</div>
        <div class="floating-element">⚡</div>
    </div>
    
    <div class="container">
        <div class="profile-header">
            <div class="visitor-badge">👀 Profile Views</div>
            <div class="typing-animation">
                Hi There! <span class="wave">👋</span> I'm Ghebrebrhan Weldit
            </div>
            <div class="role-title">
                Research Associate at <a href="https://www.ku.ac.ae/c2ps" target="_blank">C2PS Lab</a>
            </div>
            <div class="description">
                I design and apply deep learning and generative models to real-world challenges in malware detection and anomaly detection.
            </div>
        </div>
        
        <div class="info-cards">
            <div class="info-card">
                <div class="info-item">
                    <span class="info-icon">🎓</span>
                    <span class="info-text"><strong>Current Role:</strong> Research Associate at Khalifa University</span>
                </div>
                <div class="info-item">
                    <span class="info-icon">📍</span>
                    <span class="info-text"><strong>Location:</strong> Abu Dhabi, UAE</span>
                </div>
            </div>
            
            <div class="info-card">
                <div class="info-item">
                    <span class="info-icon">🧠</span>
                    <span class="info-text"><strong>Expertise:</strong> GANs, Transformers, Causal Learning, Sequence Modeling</span>
                </div>
                <div class="info-item">
                    <span class="info-icon">🔬</span>
                    <span class="info-text"><strong>Applications:</strong> Malware behavior modeling, biometric authentication, African language processing</span>
                </div>
            </div>
            
            <div class="info-card">
                <div class="info-item">
                    <span class="info-icon">📄</span>
                    <span class="info-text"><strong>Portfolio:</strong> <a href="https://gweldit.github.io" target="_blank">gweldit.github.io</a></span>
                </div>
                <div class="info-item">
                    <span class="info-icon">📫</span>
                    <span class="info-text"><strong>Email:</strong> <a href="mailto:gereweldit@gmail.com">gereweldit@gmail.com</a></span>
                </div>
            </div>
        </div>
        
        <div class="projects-section">
            <h2 class="section-title">📌 Selected Projects & Publications</h2>
            
            <div class="project-item">
                <span class="project-icon">🧾</span>
                <div class="project-text">
                    <a href="https://doi.org/10.1109/TAI.2025.3537966" target="_blank">First-author IEEE TAI paper on Generative Models for Malware Behavior</a>
                </div>
            </div>
            
            <div class="project-item">
                <span class="project-icon">🛡️</span>
                <div class="project-text">
                    GANs for heavy-tailed malware generation — presented at SecureComm 2024
                </div>
            </div>
            
            <div class="project-item">
                <span class="project-icon">🧬</span>
                <div class="project-text">
                    YOLOv7-based parasitic egg detection done in collaboration with <a href="https://github.com/Murdism" target="_blank">Murad</a>
                </div>
            </div>
        </div>
        
        <div class="current-work">
            <h2 class="section-title">🚀 Current Focus</h2>
            
            <div class="work-item">
                <span class="work-icon">🔭</span>
                <div class="work-text">
                    Currently working on generative models (GANs, Transformers) for malware behavior generation and polymorphic malware detection
                </div>
            </div>
            
            <div class="work-item">
                <span class="work-icon">🌱</span>
                <div class="work-text">
                    Learning advanced sequence modeling and causal reward optimization for GANs
                </div>
            </div>
            
            <!--
            <div class="work-item">
                <span class="work-icon">⚡</span>
                <div class="work-text">
                    <strong>Fun fact:</strong> I've built detection systems for both cyber threats and parasitic eggs — same precision, different                             domains!
                </div>
            <!--
            </div>
        </div>
    </div>
</body>
</html>
