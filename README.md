<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav ul {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center;
        }
        nav ul li {
            margin: 0 15px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
            font-size: 18px;
        }
        section {
            margin: 20px;
            padding: 20px;
        }
        .about, .projects, .contact {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .projects img {
            width: 100%;
            border-radius: 10px;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        /* Responsive Design */
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>My Portfolio</h1>
        <nav>
            <ul>
                <li><a href="#about">About Me</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="about" class="about">
        <h2>About Me</h2>
        <p>Hi! I'm a passionate developer skilled in DevOps and web development. I enjoy creating projects that improve efficiency and solve real-world problems.</p>
    </section>

    <section id="projects" class="projects">
        <h2>My Projects</h2>
        <div class="project">
            <h3>Project 1: DevOps Pipeline</h3>
            <p>This project demonstrates an automated CI/CD pipeline for web applications using Jenkins, Docker, and Kubernetes.</p>
            <img src="https://via.placeholder.com/600x300" alt="Project Screenshot">
        </div>
        <div class="project">
            <h3>Project 2: Personal Portfolio Website</h3>
            <p>This portfolio website showcases my skills and projects. It's built with HTML, CSS, and JavaScript.</p>
            <img src="https://via.placeholder.com/600x300" alt="Portfolio Screenshot">
        </div>
    </section>

    <section id="contact" class="contact">
        <h2>Contact Me</h2>
        <form id="contactForm">
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name" required><br><br>
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email" required><br><br>
            <label for="message">Message:</label><br>
            <textarea id="message" name="message" required></textarea><br><br>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 My Portfolio</p>
    </footer>

    <script>
        // JavaScript for form submission
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', function(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            
            if (name && email && message) {
                alert('Thank you for your message, ' + name + '! I will get back to you soon.');
                contactForm.reset();
            } else {
                alert('Please fill out all fields before submitting.');
            }
        });
    </script>

</body>
</html>
