# My-Personal-Portfolio
index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Portfolio</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <div class="container">
      <h1>Meenakshi Rathod</h1>
      <p>Web Developer, designer & Business Analyst</p>
      <nav>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <section id="about">
    <div class="container">
      <h2>About Me</h2>
      <p>Hello! I'm Meenakshi, a passionate front-end developer creating beautiful and functional websites. I specialize in HTML, CSS, JavaScript, and responsive design.
      Apart from this I also have a genuine interest in business analyzing and problem solving</p>
    </div>
  </section>

  <section id="projects">
    <div class="container">
      <h2>Projects</h2>
      <div class="project-grid">
        <div class="project">
          <h3>Portfolio Website</h3>
          <p>A responsive personal portfolio site built with HTML, CSS, and JS.</p>
        </div>
        <div class="project">
          <h3>To-Do App</h3>
          <p>A simple task manager using localStorage and vanilla JavaScript.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="container">
      <h2>Contact Me</h2>
      <form id="contact-form">
        <input type="text" id="name" placeholder="Your Name" required />
        <input type="email" id="email" placeholder="Your Email" required />
        <textarea id="message" rows="5" placeholder="Your Message" required></textarea>
        <button type="submit">Send</button>
        <p id="form-status"></p>
      </form>
    </div>
  </section>

  <footer>
    <div class="container">
      <p>&copy; 2025 Meenakshi Rathod. All rights reserved.</p>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>


style.css

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

body {
  font-family: 'Segoe UI', sans-serif;
  background-color: #f9f9f9;
  color: #333;
}

.container {
  width: 90%;
  max-width: 1100px;
  margin: auto;
  padding: 20px 0;
}

header {
  background-color: #333;
  color: white;
  padding: 40px 0;
  text-align: center;
}

header h1 {
  margin-bottom: 10px;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  gap: 20px;
}

nav a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

section {
  padding: 60px 0;
  border-bottom: 1px solid #ddd;
}

h2 {
  margin-bottom: 20px;
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.project {
  background: #fff;
  padding: 20px;
  box-shadow: 0 0 10px #ccc;
  border-radius: 10px;
}

form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

form input,
form textarea {
  padding: 10px;
  border: 1px solid #aaa;
  border-radius: 5px;
}

form button {
  padding: 10px;
  background-color: #333;
  color: white;
  border: none;
  cursor: pointer;
}

form button:hover {
  background-color: #555;
}

footer {
  text-align: center;
  padding: 20px;
  background: #eee;
}


scipt.js

document.getElementById('contact-form').addEventListener('submit', function (e) {
  e.preventDefault();

  // Simulate sending the message
  const status = document.getElementById('form-status');
  status.textContent = 'Sending...';

  setTimeout(() => {
    status.textContent = 'Thank you! Your message has been sent.';
    document.getElementById('contact-form').reset();
  }, 1000);
});
