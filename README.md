# Sunpeng's About Me
My personal about me website: [nhok-them.github.io/AboutMe](https://nhok-them.github.io/AboutMe/)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sunpeng ~ nhok_them</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        /* Global styles */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Lato', sans-serif;
            font-size: 16px;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(to right, #e0eafc, #cfdef3);
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: #ff6f61;
            transition: color 0.3s ease;
        }

        a:hover {
            color: #ff9f7f;
        }

        /* Header styles */
        header {
            background-color: #1e1e1e;
            color: #fff;
            padding: 20px;
            text-align: center;
            border-bottom: 5px solid #ff6f61;
            position: relative;
            font-weight: bold;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
        }

        header .container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        header .avatar {
            margin-bottom: 10px;
        }

        header .avatar img {
            border-radius: 50%;
            width: 120px; /* Adjust the size as needed */
            height: 120px; /* Adjust the size as needed */
            object-fit: cover;
            border: 4px solid #ff6f61;
        }

        header h1 {
            font-size: 2.5em;
            letter-spacing: 2px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
            margin: 0;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to right, #ff6f61, #ff9f7f);
            z-index: -1;
            opacity: 0.5;
        }

        /* Container styles */
        .container {
            width: 85%;
            margin: 30px auto;
        }

        /* Section styles */
        section {
            padding: 20px;
            background: #fff;
            margin: 20px 0;
            border-radius: 15px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        section:hover {
            transform: translateY(-10px);
        }

        section h2 {
            font-size: 2em;
            margin-bottom: 10px;
            color: #333;
            position: relative;
        }

        section h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #ff6f61;
            margin-top: 10px;
        }

        section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: #ff6f61;
            border-top-left-radius: 15px;
            border-bottom-left-radius: 15px;
        }

        .content {
            display: none;
        }

        section:hover .content,
        .active .content {
            display: block;
        }

        /* Blog section styles */
        .blog-section {
            background: #f7f7f7;
            padding: 40px 20px;
            margin: 40px 0;
            border-radius: 15px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }

        .blog-card {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .blog-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
        }

        .blog-card h3 {
            margin-bottom: 15px;
            font-size: 1.8em;
            color: #333;
        }

        .blog-card p {
            color: #666;
            font-size: 1.1em;
        }

        /* Modal styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .modal-content {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            width: 80%;
            max-width: 800px;
            text-align: center;
        }

        .modal-content h3 {
            font-size: 2em;
            margin-bottom: 15px;
        }

        .modal-content p {
            font-size: 1.2em;
            color: #333;
        }

        .close-modal {
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 2em;
            color: #fff;
            cursor: pointer;
        }

        /* Grid container styles */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        /* Footer styles */
        footer {
            background: #1e1e1e;
            color: #fff;
            padding: 15px;
            text-align: center;
            margin-top: 40px;
        }

        footer p {
            margin: 10px 0;
        }

        .social-icons a {
            color: #fff;
            margin: 0 10px;
            font-size: 1.5em;
            transition: color 0.3s ease;
        }

        .social-icons a:hover {
            color: #ff9f7f;
        }

        /* Media queries */
        @media (max-width: 768px) {
            .container {
                width: 95%;
            }

            section h2 {
                font-size: 1.75em;
            }

            footer .footer-content {
                flex-direction: column;
                gap: 20px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="avatar">
                <img src="D:\JPA\Resources\images\avatar.jpg.png" alt="Sunpeng Lim">
            </div>
            <h1>Sunpeng Lim</h1>
        </div>
    </header>

    <div class="container">
        <section class="intro" id="aboutMeSection">
            <h2>About Me</h2>
            <div class="content">
                <p>Hello, I’m Sunpeng Lim, a senior at Jay Pritzker Academy yearning to explore the world of AI and programming. I currently live by a bustling market in a small village near Siem Reap, Cambodia with my father, my mother, and my older sister. My passion for technology ignited when I got to my own computer for the first time ever. The features and settings were the playground I hung around in, diving deeper into the world of programming and machine learning as I immersed myself in the coding community. My eager nature to wander into the depths of technology drives my motivation to pursue a career in computer engineering at a collegiate level. With the possibility of the future beholding a world of cutting-edge technology, AI and computer software will enable my community to a new perspective in life, by incorporating technology to fulfill their basic needs in life and introducing my country to the fast-growing digital world. </p>
            </div>
        </section>

        <section class="things-ive-done" id="thingsDoneSection">
            <h2>Things I've Done</h2>
            <div class="content">
                <p>• Model United Nations (2023 - 2024) Cambodia</p>
                <p>• World Robotic Olympiad (2023) Cambodia </p>
            </div>
        </section>

        <section class="my-activities" id="activitiesSection">
            <h2>My Activities</h2>
            <div class="content">
                <p>• Coding (2022 - ongoing): I’m passionate about learning new programming languages and expanding my skills in web development and software engineering.</p>
                <p>• Local Mathematics Tutor (2024 - ongoing): Provided public school students 10th grade mathematics class in Khmer for free every Sunday. </p>
                <p>• Part of Project Motiv8 (Jan 2024) New Hope Orphanage Center: Provided orphans with a positive and creative setting and allowing their voices to be heard (showcasing talents and interests).</p>
                <p>• Household Responsibilities (2021 – Ongoing): Managing the students’ scores for my father (Homeroom Teacher) using Microsoft Excel, spend weekend afternoons helping mom with selling at the market, and tutoring older siblings with English. </p>
                <p>• Chess Club Co-Founder (Jan 2024 - Aug 2024)</p>
                <p>• Running Club (2023) JPA</p>
                <p>• Guitar Self-Teach (2024 - ongoing)</p>
            </div>
        </section>

        <!-- Blog Section -->
        <section class="blog-section">
            <h2>My Blog</h2>
            <div class="grid-container">
                <div class="blog-card" data-title="My Coding Journey" data-content="Starting from scratch to learning advanced programming techniques, this is the story of how I fell in love with code.">
                    <h3>Post 1: My Coding Journey</h3>
                    <p>Starting from scratch to learning advanced programming techniques, this is the story of how I fell in love with code.</p>
                </div>
                <div class="blog-card" data-title="Machine Learning Basics" data-content="Introduction to machine learning concepts and how I'm applying them in real-world projects.">
                    <h3>Post 2: Machine Learning Basics</h3>
                    <p>Introduction to machine learning concepts and how I'm applying them in real-world projects.</p>
                </div>
                <div class="blog-card" data-title="Tech in Cambodia" data-content="Exploring the growth of technology in Cambodia and how it can shape the future of the country.">
                    <h3>Post 3: Tech in Cambodia</h3>
                    <p>Exploring the growth of technology in Cambodia and how it can shape the future of the country.</p>
                </div>
            </div>
        </section>

        <!-- Modal Structure -->
        <div class="modal" id="blogModal">
            <span class="close-modal" id="closeModal">&times;</span>
            <div class="modal-content">
                <h3 id="modalTitle"></h3>
                <p id="modalContent"></p>
            </div>
        </div>

        <footer>
            <div class="footer-content">
                <p>&copy; 2024 Sunpeng Lim. All rights reserved.</p>
                <p>Contact me via: <a href="mailto:limsunpeng07@gmail.com">limsunpeng07@gmail.com</a></p>
                <p>Discord: <a href="https://discord.com/users/d3m1g0d.69" target="_blank">d3m1g0d.69</a></p>
                <p>Chess: <a href="https://www.chess.com/member/nhok_them" target="_blank">@nhok_them</a></p>
                <div class="social-icons">
                    <a href="https://github.com/yourusername" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
                    <a href="https://www.linkedin.com/in/yourusername/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
                </div>
            </div>
        </footer>
    </div>

    <script>
        // Show modal with blog content
        const blogCards = document.querySelectorAll('.blog-card');
        const modal = document.getElementById('blogModal');
        const modalTitle = document.getElementById('modalTitle');
        const modalContent = document.getElementById('modalContent');
        const closeModal = document.getElementById('closeModal');

        blogCards.forEach(card => {
            card.addEventListener('click', function() {
                const title = this.getAttribute('data-title');
                const content = this.getAttribute('data-content');
                modalTitle.innerText = title;
                modalContent.innerText = content;
                modal.style.display = 'flex';
            });
        });

        closeModal.addEventListener('click', function() {
            modal.style.display = 'none';
        });

        window.addEventListener('click', function(event) {
            if (event.target == modal) {
                modal.style.display = 'none';
            }
        });

        // Handle section clicks to toggle visibility of content
        const sections = document.querySelectorAll('section');

        sections.forEach(section => {
            section.addEventListener('click', function() {
                this.classList.toggle('active');
            });
        });
    </script>
</body>
</html>
