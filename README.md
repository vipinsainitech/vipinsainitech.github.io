<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vipin Saini - Lead iOS Developer Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            color: #ffffff;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            padding: 80px 0 60px;
            background: linear-gradient(135deg, rgba(0, 122, 255, 0.1) 0%, rgba(52, 199, 89, 0.1) 100%);
            border-radius: 20px;
            margin-bottom: 60px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(0, 122, 255, 0.1) 0%, transparent 50%);
            animation: rotate 20s linear infinite;
            z-index: -1;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #007AFF, #34C759);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 30px;
            font-size: 3em;
            animation: pulse 2s ease-in-out infinite alternate;
        }

        @keyframes pulse {
            from { box-shadow: 0 0 20px rgba(0, 122, 255, 0.5); }
            to { box-shadow: 0 0 40px rgba(52, 199, 89, 0.8); }
        }

        h1 {
            font-size: 3.5em;
            font-weight: 700;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #007AFF, #34C759);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle {
            font-size: 1.8em;
            color: #00D4FF;
            margin-bottom: 20px;
            font-weight: 600;
        }

        .experience-badge {
            background: linear-gradient(135deg, #007AFF, #34C759);
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.2em;
            display: inline-block;
            margin: 20px 0;
            box-shadow: 0 10px 30px rgba(0, 122, 255, 0.3);
        }

        .intro-text {
            font-size: 1.3em;
            color: #e0e0e0;
            max-width: 800px;
            margin: 0 auto 40px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .stat-item {
            text-align: center;
            padding: 25px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            border: 1px solid rgba(0, 122, 255, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .stat-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 122, 255, 0.2);
        }

        .stat-number {
            font-size: 3em;
            font-weight: 700;
            color: #00D4FF;
            margin-bottom: 10px;
            text-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
        }

        .stat-label {
            color: #cccccc;
            font-size: 1.1em;
            font-weight: 500;
        }

        /* Section Styles */
        .section {
            margin-bottom: 80px;
            padding: 60px 40px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }

        .section h2 {
            font-size: 2.8em;
            margin-bottom: 40px;
            text-align: center;
            color: #ffffff;
            font-weight: 700;
        }

        .section-subtitle {
            font-size: 1.2em;
            color: #b0b0b0;
            text-align: center;
            margin-bottom: 50px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .skill-card {
            background: linear-gradient(135deg, rgba(0, 122, 255, 0.15) 0%, rgba(88, 86, 214, 0.15) 100%);
            padding: 35px;
            border-radius: 20px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(0, 122, 255, 0.3);
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0, 122, 255, 0.2);
            border-color: rgba(0, 122, 255, 0.5);
        }

        .skill-card h3 {
            font-size: 1.6em;
            margin-bottom: 20px;
            color: #00D4FF;
            font-weight: 600;
        }

        .skill-list {
            list-style: none;
            padding: 0;
        }

        .skill-list li {
            margin-bottom: 12px;
            padding-left: 25px;
            position: relative;
            color: #e0e0e0;
            font-size: 1.1em;
        }

        .skill-list li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #34C759;
            font-weight: bold;
            font-size: 1.2em;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 35px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(135deg, #007AFF, #34C759);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.3);
            border-color: rgba(0, 122, 255, 0.4);
        }

        .project-title {
            color: #ffffff;
            font-size: 1.5em;
            margin-bottom: 15px;
            font-weight: 600;
        }

        .project-desc {
            color: #cccccc;
            margin-bottom: 20px;
            font-size: 1.1em;
            line-height: 1.6;
        }

        .project-status {
            background: linear-gradient(135deg, #34C759, #00D4FF);
            color: white;
            padding: 8px 16px;
            border-radius: 25px;
            font-size: 0.9em;
            display: inline-block;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(52, 199, 89, 0.3);
        }

        /* Experience Timeline */
        .experience-timeline {
            margin-top: 40px;
        }

        .experience-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            margin-bottom: 30px;
            border-radius: 20px;
            border-left: 5px solid #007AFF;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .experience-item:hover {
            transform: translateX(10px);
            box-shadow: 0 15px 30px rgba(0, 122, 255, 0.2);
        }

        .experience-role {
            color: #00D4FF;
            font-size: 1.6em;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .experience-company {
            color: #34C759;
            font-size: 1.2em;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .experience-duration {
            color: #888888;
            font-size: 1em;
            margin-bottom: 20px;
            font-style: italic;
        }

        .experience-desc {
            color: #e0e0e0;
            font-size: 1.1em;
            line-height: 1.7;
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .contact-card {
            background: linear-gradient(135deg, rgba(0, 122, 255, 0.1), rgba(52, 199, 89, 0.1));
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(0, 122, 255, 0.2);
        }

        .contact-card:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 40px rgba(0, 122, 255, 0.2);
        }

        .contact-card h3 {
            color: #00D4FF;
            font-size: 1.4em;
            margin-bottom: 15px;
            font-weight: 600;
        }

        .contact-card p {
            color: #e0e0e0;
            font-size: 1.1em;
            line-height: 1.5;
        }

        /* SwiftUI Showcase */
        .swiftui-showcase {
            background: linear-gradient(135deg, rgba(0, 122, 255, 0.1), rgba(88, 86, 214, 0.1));
            padding: 50px;
            border-radius: 25px;
            margin-top: 40px;
            border: 1px solid rgba(0, 122, 255, 0.3);
        }

        .swiftui-showcase h3 {
            color: #00D4FF;
            font-size: 2em;
            margin-bottom: 20px;
            text-align: center;
            font-weight: 600;
        }

        .swiftui-showcase p {
            color: #e0e0e0;
            font-size: 1.2em;
            text-align: center;
            line-height: 1.7;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            h1 {
                font-size: 2.5em;
            }
            
            .section {
                padding: 40px 20px;
                margin-bottom: 50px;
            }
            
            .section h2 {
                font-size: 2.2em;
            }
            
            .skills-grid,
            .projects-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }

        /* Floating animation for background elements */
        .floating-element {
            position: fixed;
            pointer-events: none;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
        }

        .floating-element:nth-child(1) {
            top: 10%;
            left: 10%;
            animation-delay: 0s;
        }

        .floating-element:nth-child(2) {
            top: 20%;
            right: 10%;
            animation-delay: 2s;
        }

        .floating-element:nth-child(3) {
            bottom: 20%;
            left: 20%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
    </style>
</head>
<body>
    <!-- Floating background elements -->
    <div class="floating-element">📱</div>
    <div class="floating-element">⚡</div>
    <div class="floating-element">🚀</div>

    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <div class="profile-img">📱</div>
            <h1>Vipin Saini</h1>
            <p class="subtitle">Lead iOS Developer & Project Coordinator</p>
            <div class="experience-badge">10+ Years of iOS Excellence</div>
            <p class="intro-text">Passionate iOS developer and project leader specializing in Swift, SwiftUI, and building high-performance mobile applications. Currently leading teams at JHAVTECH STUDIOS in Melbourne, Australia, delivering exceptional user experiences across the Apple ecosystem.</p>
            
            <div class="stats-grid">
                <div class="stat-item">
                    <div class="stat-number">18+</div>
                    <div class="stat-label">Apps Published</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">10</div>
                    <div class="stat-label">Years Experience</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">5+</div>
                    <div class="stat-label">Countries Served</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Success Rate</div>
                </div>
            </div>
        </header>

        <!-- Technical Skills Section -->
        <section class="section">
            <h2>Technical Expertise</h2>
            <p class="section-subtitle">Comprehensive iOS development skills with focus on modern Swift and SwiftUI development, architectural patterns, and project leadership.</p>
            
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>📱 iOS Development</h3>
                    <ul class="skill-list">
                        <li>Swift (Expert Level)</li>
                        <li>SwiftUI (Advanced)</li>
                        <li>Objective-C</li>
                        <li>UIKit & Combine</li>
                        <li>iOS 18 & Xcode 16</li>
                        <li>Live Activities & Widgets</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>🏗️ Architecture & Patterns</h3>
                    <ul class="skill-list">
                        <li>MVC, MVVM, Clean Architecture</li>
                        <li>Singleton, Delegation, Observer</li>
                        <li>Performance Optimization</li>
                        <li>Code Reviews & Best Practices</li>
                        <li>Unit & UI Testing</li>
                        <li>Dependency Injection</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>🔧 Frameworks & APIs</h3>
                    <ul class="skill-list">
                        <li>Firebase, MapKit, AVFoundation</li>
                        <li>Alamofire, Core Data, Realm</li>
                        <li>Push Notifications (APNs)</li>
                        <li>MapBox, Google Maps API</li>
                        <li>Socket.IO, XMPP</li>
                        <li>Charts & Data Visualization</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>💰 Payment & Integration</h3>
                    <ul class="skill-list">
                        <li>Apple Pay, In-App Purchase</li>
                        <li>Stripe, PayPal Integration</li>
                        <li>Paytm, PayUMoney, Cashfree</li>
                        <li>Social Media APIs</li>
                        <li>REST APIs & GraphQL</li>
                        <li>Third-party SDK Integration</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>🚀 Project Management</h3>
                    <ul class="skill-list">
                        <li>Team Leadership</li>
                        <li>Agile & Scrum Methodologies</li>
                        <li>Sprint Planning & Tracking</li>
                        <li>Client Communication</li>
                        <li>Resource Planning</li>
                        <li>Quality Assurance</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>🛠️ Tools & DevOps</h3>
                    <ul class="skill-list">
                        <li>GitHub, GitLab, BitBucket</li>
                        <li>Jira, Trello, ClickUp</li>
                        <li>Figma, Sketch, Adobe XD</li>
                        <li>Firebase Analytics</li>
                        <li>TestFlight & App Store</li>
                        <li>CI/CD with GitHub Actions</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Featured Projects Section -->
        <section class="section">
            <h2>Featured Projects</h2>
            <p class="section-subtitle">Showcase of successful iOS applications delivered across various industries and markets worldwide.</p>
            
            <div class="projects-grid">
                <div class="project-card">
                    <h3 class="project-title">🦉 Owl Eye - Sleep Test</h3>
                    <p class="project-desc">Advanced sleep tracking app with sophisticated analytics, user-friendly interface, and comprehensive sleep monitoring features for the Australian healthcare market.</p>
                    <div class="project-status">Live on App Store</div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">💄 CosMe</h3>
                    <p class="project-desc">Beauty and cosmetics application with product discovery, reviews, and personalized recommendations. Features advanced UI/UX and social sharing capabilities.</p>
                    <div class="project-status">Australia Market</div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">🏏 Cricket Pulse Live</h3>
                    <p class="project-desc">Real-time cricket scoring and live updates app with comprehensive match statistics, push notifications, and engaging user interface for cricket fans globally.</p>
                    <div class="project-status">Global Release</div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">🍸 Lines - Bars & Nightclubs</h3>
                    <p class="project-desc">Social networking app for nightlife discovery with location services, event management, user check-ins, and real-time updates for the Australian entertainment industry.</p>
                    <div class="project-status">Australia Exclusive</div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">🏨 Holisto - Hotel Deals</h3>
                    <p class="project-desc">Comprehensive travel booking platform with advanced search algorithms, secure payment integration, personalized recommendations, and seamless booking experience.</p>
                    <div class="project-status">International</div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">🚗 Road Trip Navigation</h3>
                    <p class="project-desc">GPS navigation app with offline maps, route optimization, travel planning features, and real-time traffic updates for road trip enthusiasts worldwide.</p>
                    <div class="project-status">Global Launch</div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">🎮 ManaPlay</h3>
                    <p class="project-desc">Gaming platform application with social features, leaderboards, and interactive gameplay elements. Built for the Canadian gaming market with advanced user engagement.</p>
                    <div class="project-status">Canada Market</div>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title">📞 FanFone</h3>
                    <p class="project-desc">VOIP calling and communication app with video-audio call functionalities, integrated ML models, and secure messaging features for the US market.</p>
                    <div class="project-status">US Market</div>
                </div>
            </div>
        </section>

        <!-- SwiftUI Expertise Section -->
        <section class="section">
            <h2>SwiftUI Excellence</h2>
            <p class="section-subtitle">Demonstrating modern iOS development with SwiftUI and advanced architectural patterns</p>
            
            <div class="swiftui-showcase">
                <h3>🐦 Twitter Clone - SwiftUI Showcase</h3>
                <p>Built a comprehensive Twitter clone using SwiftUI with MVVM architecture, Firebase backend integration, real-time updates, user authentication, profile management, tweet interactions, and social features - demonstrating mastery of modern iOS development best practices and clean architecture principles.</p>
            </div>
            
            <div class="skills-grid" style="margin-top: 40px;">
                <div class="skill-card">
                    <h3>🏗️ Architecture</h3>
                    <ul class="skill-list">
                        <li>MVVM Pattern Implementation</li>
                        <li>Clean Architecture Principles</li>
                        <li>Dependency Injection</li>
                        <li>State Management</li>
                        <li>Reactive Programming</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>🔥 Firebase Integration</h3>
                    <ul class="skill-list">
                        <li>Authentication System</li>
                        <li>Firestore Database</li>
                        <li>Real-time Updates</li>
                        <li>Cloud Storage</li>
                        <li>Analytics & Crashlytics</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>✨ Advanced Features</h3>
                    <ul class="skill-list">
                        <li>Custom UI Components</li>
                        <li>Animation & Transitions</li>
                        <li>Combine Framework</li>
                        <li>Live Activities</li>
                        <li>Dynamic Type Support</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Professional Experience Section -->
        <section class="section">
            <h2>Professional Journey</h2>
            <p class="section-subtitle">A decade of progressive growth in iOS development and project leadership across multiple companies and diverse projects.</p>
            
            <div class="experience-timeline">
                <div class="experience-item">
                    <div class="experience-role">Lead iOS Developer & Project Coordinator</div>
                    <div class="experience-company">JHAVTECH STUDIOS - Melbourne, Australia</div>
                    <div class="experience-duration">June 2022 - Present (2+ Years)</div>
                    <p class="experience-desc">Leading iOS development and project coordination for multiple high-profile applications. Managing cross-functional teams, implementing advanced iOS features including Live Activities and MapBox integration, ensuring timely delivery of high-quality mobile applications while maintaining code quality standards and mentoring junior developers.</p>
                </div>
                
                <div class="experience-item">
                    <div class="experience-role">Senior iOS Developer</div>
                    <div class="experience-company">ZOBI WEB SOLUTIONS - Ahmedabad, India</div>
                    <div class="experience-duration">June 2021 - April 2022 (10 Months)</div>
                    <p class="experience-desc">Spearheaded the adoption of SwiftUI and Combine framework, transforming development processes and enhancing code maintainability. Utilized Alamofire, HorizonCalendar, and GoogleMaps frameworks to deliver performant and visually appealing iOS applications with responsive UI components.</p>
                </div>
                
                <div class="experience-item">
                    <div class="experience-role">Senior iOS Developer</div>
                    <div class="experience-company">CREATIVE-HUSTLERS - Ahmedabad, India</div>
                    <div class="experience-duration">January 2021 - June 2021 (6 Months)</div>
                    <p class="experience-desc">Developed VOIP calling and video-audio call functionalities using PushKit and ML Models. Created custom calendar features and navigation animations, integrated Stripe Payment and Keychain for secure transactions, and implemented data visualization with charts module for analytics.</p>
                </div>
                
                <div class="experience-item">
                    <div class="experience-role">Senior iOS Developer</div>
                    <div class="experience-company">NETCLUES TECHNOLOGIES - Ahmedabad, India</div>
                    <div class="experience-duration">November 2019 - December 2020 (1+ Year)</div>
                    <p class="experience-desc">Developed and maintained multiple iOS applications with In-App Purchase, gesture-based interactions, and social media integration. Integrated XMPP and OpenFire for real-time messaging, implemented offline data management using Yapdatabase and Realm, and integrated offline maps for enhanced user experience.</p>
                </div>
                
                <div class="experience-item">
                    <div class="experience-role">Senior iOS Developer</div>
                    <div class="experience-company">WALTER TECHNOLOGIES - Ahmedabad, India</div>
                    <div class="experience-duration">November 2015 - November 2019 (4 Years)</div>
                    <p class="experience-desc">Developed comprehensive iOS applications using MapKit, advanced animations, ScrollView, CollectionView, and TableView. Implemented JSON parsing for data retrieval and processing, focusing on performance optimization and user experience enhancement.</p>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section class="section">
            <h2>Let's Build Something Amazing</h2>
            <p class="section-subtitle">Ready to collaborate on your next iOS project or discuss leadership opportunities in mobile development. Available for both full-time positions and contract work.</p>
            
            <div class="contact-grid">
                <div class="contact-card">
                    <h3>📱 Mobile</h3>
                    <p>+91-7048749984<br>Available for calls & meetings</p>
                </div>
                <div class="contact-card">
                    <h3>🌐 Portfolio</h3>
                    <p>www.vipinsaini.tech<br>Complete project showcase</p>
                </div>
                <div class="contact-card">
                    <h3>🏢 Current Position</h3>
                    <p>Lead iOS Developer<br>JHAVTECH STUDIOS<br>Melbourne, Australia</p>
                </div>
                <div class="contact-card">
                    <h3>💼 Availability</h3>
                    <p>Full-time & Contract<br>Remote & On-site<br>Immediate Start</p>
                </div>
                <div class="contact-card">
                    <h3>🗣️ Languages</h3>
                    <p>English (Professional)<br>Hindi (Native)<br>Gujarati (Professional)</p>
                </div>
                <div class="contact-card">
                    <h3>🎯 Specialization</h3>
                    <p>iOS Development<br>Project Leadership<br>SwiftUI Expert</p>
                </div>
            </div>
        </section>
    </div>
</body>
</html>
