# SDG
Talk about SDGs 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2030 Agenda - Transforming Our World</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Navigation Bar */
        nav {
            background: #004494;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: background 0.3s;
        }

        nav a:hover {
            background: #003366;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #004494 0%, #0072BC 100%);
            color: white;
            text-align: center;
            padding: 120px 20px 80px;
            margin-top: 70px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn {
            display: inline-block;
            background: #FF6B00;
            color: white;
            padding: 15px 30px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255,107,0,0.3);
        }

        /* Goals Grid */
        .goals-section {
            padding: 80px 20px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #004494;
        }

        .goals-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .goal-card {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            height: 250px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .goal-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .goal-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .goal-card:nth-child(1) { border-top: 5px solid #E5243B; }
        .goal-card:nth-child(2) { border-top: 5px solid #DDA63A; }
        .goal-card:nth-child(3) { border-top: 5px solid #4C9F38; }
        .goal-card:nth-child(4) { border-top: 5px solid #C5192D; }
        .goal-card:nth-child(5) { border-top: 5px solid #FF3A21; }
        .goal-card:nth-child(6) { border-top: 5px solid #26BEBF; }
        .goal-card:nth-child(7) { border-top: 5px solid #FCC30B; }
        .goal-card:nth-child(8) { border-top: 5px solid #A4193D; }
        .goal-card:nth-child(9) { border-top: 5px solid #FD6925; }
        .goal-card:nth-child(10) { border-top: 5px solid #DD1365; }
        .goal-card:nth-child(11) { border-top: 5px solid #FD9D24; }
        .goal-card:nth-child(12) { border-top: 5px solid #BF8B2E; }
        .goal-card:nth-child(13) { border-top: 5px solid #3F7E44; }
        .goal-card:nth-child(14) { border-top: 5px solid #0A97D9; }
        .goal-card:nth-child(15) { border-top: 5px solid #56C2FF; }
        .goal-card:nth-child(16) { border-top: 5px solid #49C785; }
        .goal-card:nth-child(17) { border-top: 5px solid #12A2EA; }

        /* Deep Dive Section */
        .deep-dive {
            background: #f8f9fa;
            padding: 80px 20px;
        }

        .deep-dive-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 3rem;
        }

        .deep-dive-item {
            background: white;
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .deep-dive-item h3 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: #004494;
        }

        .deep-dive-item i {
            font-size: 4rem;
            margin-bottom: 1rem;
            color: #0072BC;
        }

        .deep-dive-item ul {
            list-style: none;
            padding-left: 0;
        }

        .deep-dive-item li {
            padding: 0.8rem 0;
            position: relative;
            padding-left: 2rem;
        }

        .deep-dive-item li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #4CAF50;
            font-weight: bold;
            font-size: 1.2rem;
        }

        /* Pledge Form */
        .pledge-section {
            padding: 80px 20px;
            text-align: center;
            background: linear-gradient(135deg, #0072BC 0%, #004494 100%);
            color: white;
        }

        .pledge-container {
            max-width: 600px;
            margin: 0 auto;
        }

        .pledge-container h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .pledge-container p {
            font-size: 1.2rem;
            margin-bottom: 2.5rem;
        }

        .pledge-form {
            background: rgba(255,255,255,0.1);
            padding: 2.5rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
            text-align: left;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input,
        .form-group select {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        .footer-link {
            color: #0072BC;
            text-decoration: none;
        }

        .footer-link:hover {
            text-decoration: underline;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            nav ul {
                flex-direction: column;
                gap: 1rem;
            }
            
            .deep-dive-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#goals">17 Goals</a></li>
            <li><a href="#deepdive">Deep Dive</a></li>
            <li><a href="#pledge">Take Action</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <h1>Transforming Our World: The 2030 Agenda</h1>
        <p>The United Nations' 2030 Agenda for Sustainable Development seeks to end poverty, protect the planet, and ensure prosperity and peace for all.</p>
        <a href="#goals" class="btn">Learn More</a>
    </section>

    <!-- 17 Goals Grid -->
    <section id="goals" class="goals-section">
        <h2 class="section-title">The 17 Sustainable Development Goals</h2>
        <div class="goals-grid">
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-check-circle"></i></div>
                <h3>SDG 1: No Poverty</h3>
                <p>End poverty in all its forms everywhere.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-seedling"></i></div>
                <h3>SDG 2: Zero Hunger</h3>
                <p>End hunger, achieve food security and improved nutrition.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-hand-holding-heart"></i></div>
                <h3>SDG 3: Good Health</h3>
                <p>Ensure healthy lives and promote well-being for all.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-university"></i></div>
                <h3>SDG 4: Quality Education</h3>
                <p>Ensure inclusive and equitable quality education.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-venus-mars"></i></div>
                <h3>SDG 5: Gender Equality</h3>
                <p>Achieve gender equality and empower all women and girls.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-handshake"></i></div>
                <h3>SDG 6: Clean Water</h3>
                <p>Ensure availability and sustainable management of water.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-dollar-sign"></i></div>
                <h3>SDG 7: Affordable Energy</h3>
                <p>Ensure access to affordable, reliable, sustainable energy.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-suitcase"></i></div>
                <h3>SDG 8: Decent Work</h3>
                <p>Promote sustained, inclusive economic growth and employment.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-industry"></i></div>
                <h3>SDG 9: Industry & Innovation</h3>
                <p>Build resilient infrastructure and foster innovation.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-city"></i></div>
                <h3>SDG 10: Reduced Inequalities</h3>
                <p>Reduce inequality within and among countries.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-solar-panel"></i></div>
                <h3>SDG 11: Sustainable Cities</h3>
                <p>Make cities inclusive, safe, resilient and sustainable.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-life-ring"></i></div>
                <h3>SDG 12: Responsible Consumption</h3>
                <p>Ensure sustainable consumption and production patterns.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-leaf"></i></div>
                <h3>SDG 13: Climate Action</h3>
                <p>Take urgent action to combat climate change.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-life-full"></i></div>
                <h3>SDG 14: Life Below Water</h3>
                <p>Conserve and sustainably use oceans and marine resources.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-tree"></i></div>
                <h3>SDG 15: Life on Land</h3>
                <p>Protect terrestrial ecosystems and biodiversity.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-handshake-slash"></i></div>
                <h3>SDG 16: Peace & Justice</h3>
                <p>Promote peaceful societies and access to justice.</p>
            </div>
            <div class="goal-card">
                <div class="goal-icon"><i class="fas fa-globe"></i></div>
                <h3>SDG 17: Partnerships</h3>
                <p>Strengthen global partnerships for sustainable development.</p>
            </div>
        </div>
    </section>

    <!-- Deep Dive Section -->
    <section id="deepdive" class="deep-dive">
        <div class="deep-dive-container">
            <div class="deep-dive-item">
                <i class="fas fa-leaf"></i>
                <h3>SDG 13: Climate Action</h3>
                <ul>
                    <li>Climate change affects every country and impacts food security, health, and economic growth.</li>
                    <li>Extreme weather events are becoming more frequent and severe worldwide.</li>
                    <li>Requires urgent action to reduce greenhouse gas emissions and build resilience.</li>
                    <li>Essential for protecting future generations and maintaining Earth's habitability.</li>
                </ul>
            </div>
            <div class="deep-dive-item">
                <i class="fas fa-graduation-cap"></i>
                <h3>SDG 4: Quality Education</h3>
                <ul>
                    <li>Education is a fundamental human right and essential for poverty reduction.</li>
                    <li>Quality education empowers individuals and drives sustainable development.</li>
                    <li>Provides skills needed for employment and responsible global citizenship.</li>
                    <li>Critical foundation for improving health, gender equality, and peace.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Pledge Form -->
    <section id="pledge" class="pledge-section">
        <div class="pledge-container">
            <h2>Take Action Today!</h2>
            <p>Make a pledge to support one of the Sustainable Development Goals.</p>
            <form class="pledge-form" onsubmit="handlePledge(event)">
                <div class="form-group">
                    <label for="name">Your Name:</label>
                    <input type="text" id="name" required>
                </div>
                <div class="form-group">
                    <label for="goal">Goal you pledge to support:</label>
                    <select id="goal" required>
                        <option value="">Select a goal...</option>
                        <option value="1">SDG 1: No Poverty</option>
                        <option value="2">SDG 2: Zero Hunger</option>
                        <option value="3">SDG 3: Good Health</option>
                        <option value="4">SDG 4: Quality Education</option>
                        <option value="5">SDG 5: Gender Equality</option>
                        <option value="6">SDG 6: Clean Water</option>
                        <option value="7">SDG 7: Affordable Energy</option>
                        <option value="8">SDG 8: Decent Work</option>
                        <option value="9">SDG 9: Industry & Innovation</option>
                        <option value="10">SDG 10: Reduced Inequalities</option>
                        <option value="11">SDG 11: Sustainable Cities</option>
                        <option value="12">SDG 12: Responsible Consumption</option>
                        <option value="13">SDG 13: Climate Action</option>
                        <option value="14">SDG 14: Life Below Water</option>
                        <option value="15">SDG 15: Life on Land</option>
                        <option value="16">SDG 16: Peace & Justice</option>
                        <option value="17">SDG 17: Partnerships</option>
                    </select>
                </div>
                <button type="submit" class="btn">Make My Pledge!</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>Created by <strong>Aditya</strong> | 9th Class</p>
        <p><a href="https://sdgs.un.org/goals" target="_blank" class="footer-link">Source: United Nations</a></p>
    </footer>

    <script>
        function handlePledge(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const goal = document.getElementById('goal').value;
            
            if (name && goal) {
                alert(`Thank you, ${name}! Your pledge to support SDG ${goal} has been recorded. Together, we can transform our world! 🌍`);
                document.querySelector('.pledge-form').reset();
            }
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
