# My-Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Digital Portfolio - Maimuna Samreen U</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }

        header {
            background-color: #4CAF50;
            color: white;
            padding: 1.5rem;
            text-align: center;
        }

        nav {
            background-color: #333;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            padding: 0;
            margin: 0;
        }

        nav li {
            margin: 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 1rem;
            display: block;
        }

        nav a:hover {
            background-color: #555;
        }

        section {
            padding: 2rem;
            max-width: 800px;
            margin: auto;
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .skill {
            background-color: #4CAF50;
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 5px;
            font-weight: bold;
        }

        .project-card {
            background-color: white;
            border-radius: 5px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            padding: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .project-card h3 {
            margin-top: 0;
        }

        .project-card a {
            text-decoration: none;
            color: #4CAF50;
            font-weight: bold;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        input, textarea {
            padding: 0.75rem;
            border-radius: 5px;
            border: 1px solid #ccc;
            font-size: 1rem;
            width: 100%;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 0.75rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
        }

        button:hover {
            background-color: #45a049;
        }

        footer {
            text-align: center;
            padding: 1rem;
            background-color: #333;
            color: white;
        }

        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Maimuna Samreen U</h1>
        <p>Bachelor of Computer Application | M.M.E.S Arts and Science College</p>
    </header>

    <nav>
        <ul>
            <li><a href="#about">About Me</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="about">
        <h2>About Me</h2>
        <p>
            I am a passionate computer application student with hands-on experience in web development and project work.
            This portfolio showcases my academic achievements, technical skills, and project experience.
        </p>
    </section>

    <section id="skills">
        <h2>Skills</h2>
        <div class="skills-container">
            <div class="skill">HTML</div>
            <div class="skill">CSS</div>
            <div class="skill">JavaScript</div>
            <div class="skill">React</div>
            <div class="skill">Node.js</div>
            <div class="skill">Git</div>
            <div class="skill">Figma</div>
        </div>
    </section>

    <section id="projects">
        <h2>Projects</h2>
        <div class="project-card">
            <h3>Project Showcase</h3>
            <p>Case studies with live demos and code links to demonstrate my problem-solving and development skills.</p>
            <a href="https://github.com/" target="_blank">View on GitHub</a>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Me</h2>
        <form id="contactForm">
            <input type="text" id="name" placeholder="Your Name" required />
            <input type="email" id="email" placeholder="Your Email" required />
            <textarea id="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
        <p id="responseMsg"></p>
    </section>

    <footer>
        <p>&copy; 2025 Maimuna Samreen U. All rights reserved.</p>
    </footer>

    <script>
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();
            const response = document.getElementById('responseMsg');

            if(name && email && message){
                response.textContent = "Thank you, " + name + "! Your message has been sent.";
                response.style.color = "green";
                this.reset();
            } else {
                response.textContent = "Please fill in all fields.";
                response.style.color = "red";
            }
        });
    </script>
</body>
</html>
