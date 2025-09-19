<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1.0">
  <title>Student Portfolio - All Projects</title>

  <!-- Styles -->
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial, sans-serif; }
    body { line-height: 1.6; background: #f9f9f9; color: #333; }

    /* Navbar */
    header { background: #333; color: #fff; padding: 1rem; }
    .navbar { display: flex; justify-content: space-between; align-items: center; }
    .nav-links { list-style: none; display: flex; gap: 1rem; }
    .nav-links a { color: white; text-decoration: none; }
    .nav-links a:hover { text-decoration: underline; }

    /* Hero */
    .hero { display: flex; justify-content: center; align-items: center; height: 80vh; background: #444; color: #fff; text-align: center; }
    .hero h1 span { color: #ffd700; }
    .btn { display: inline-block; margin-top: 1rem; padding: 10px 20px; background: #fff; color: #333; border-radius: 5px; text-decoration: none; }
    .btn:hover { background: #ffd700; }

    /* Sections */
    section { padding: 50px 20px; max-width: 1000px; margin: auto; }
    h2 { text-align: center; margin-bottom: 20px; }

    /* About */
    .about-content { display: flex; gap: 20px; align-items: center; justify-content: center; flex-wrap: wrap; }
    .about-content img { width: 200px; border-radius: 50%; }

    /* Projects */
    .project-grid { display: grid; grid-template-columns: repeat(auto-fit,minmax(250px,1fr)); gap: 20px; }
    .project-card { background: #fff; padding: 20px; border-radius: 10px; box-shadow: 0 0 5px rgba(0,0,0,0.2); text-align: center; }

    /* Contact */
    form { display: flex; flex-direction: column; gap: 10px; max-width: 500px; margin: auto; }
    input, textarea { padding: 10px; border: 1px solid #ccc; border-radius: 5px; }
    button { padding: 10px; background: #333; color: white; border: none; border-radius: 5px; cursor: pointer; }
    button:hover { background: #555; }
    #form-status { text-align: center; margin-top: 10px; }

    /* Quiz App */
    .quiz-container { background: white; padding: 20px; border-radius: 10px; width: 90%; max-width: 500px; box-shadow: 0 0 10px rgba(0,0,0,0.2); margin: auto; }
    .quiz-container h2 { margin-bottom: 15px; }
    .quiz-container ul { list-style: none; margin-bottom: 20px; }
    .quiz-container li { margin: 10px 0; }
    .result { font-size: 18px; font-weight: bold; text-align: center; }

    /* Blog */
    .post { background: white; padding: 15px; margin-bottom: 20px; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.1); }

    /* Responsive Website Demo */
    .responsive-demo nav { display: flex; justify-content: center; background: #444; flex-wrap: wrap; }
    .responsive-demo nav a { color: white; padding: 1rem; text-decoration: none; }
    .responsive-demo nav a:hover { background: #666; }
    .responsive-demo .container { display: grid; grid-template-columns: 3fr 1fr; gap: 1rem; padding: 1rem; }
    .responsive-demo .content, .responsive-demo .sidebar { padding: 1rem; border-radius: 8px; }
    .responsive-demo .content { background: #f4f4f4; }
    .responsive-demo .sidebar { background: #e2e2e2; }
    @media (max-width: 768px) {
      .responsive-demo .container { grid-template-columns: 1fr; }
    }

    footer { text-align: center; background: #333; color: white; padding: 1rem; margin-top: 1rem; }
  </style>

  <!-- EmailJS SDK -->
  <script src="https://cdn.emailjs.com/dist/email.min.js"></script>
  <script>
    (function(){ emailjs.init("YOUR_PUBLIC_KEY"); })();
  </script>
</head>
<body>

  <!-- Navbar -->
  <header>
    <nav class="navbar">
      <div class="logo">MyPortfolio</div>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#quiz">Quiz App</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#responsive">Responsive Demo</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Hello, I'm <span>MR__ YOGA</span></h1>
      <p>I am a student</p>
      <a href="#projects" class="btn">View My Work</a>
    </div>
  </section>

  <!-- About -->
  <section id="about">
    <h2>About Me</h2>
    <div class="about-content">
      <img src="IMG_2017.jpg" alt="Profile Photo">
      <p>
        I am a student enthusiastic about technology and design. I love building interactive,
        user-friendly web applications and exploring new tools in the tech world.
      </p>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card"><h3>Project 1</h3><p>A simple responsive website.</p></div>
      <div class="project-card"><h3>Project 2</h3><p>JavaScript-based quiz app.</p></div>
      <div class="project-card"><h3>Project 3</h3><p>Personal blog with CMS.</p></div>
    </div>
  </section>

  <!-- Quiz App -->
  <section id="quiz">
    <h2>Simple Quiz App</h2>
    <div class="quiz-container" id="quiz-box">
      <h2 id="question">Question text</h2>
      <ul>
        <li><label><input type="radio" name="answer" class="answer" id="a"> <span id="a_text">Answer A</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="b"> <span id="b_text">Answer B</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="c"> <span id="c_text">Answer C</span></label></li>
        <li><label><input type="radio" name="answer" class="answer" id="d"> <span id="d_text">Answer D</span></label></li>
      </ul>
      <button id="submit">Submit</button>
      <div class="result" id="result"></div>
    </div>
  </section>

  <!-- Blog -->
  <section id="blog">
    <h2>My Blog</h2>
    <div class="container" id="postsContainer"></div>
  </section>

  <!-- Responsive Website Demo -->
  <section id="responsive" class="responsive-demo">
    <h2>Responsive Website Demo</h2>
    <nav>
      <a href="#">Home</a><a href="#">About</a><a href="#">Services</a><a href="#">Contact</a>
    </nav>
    <div class="container">
      <div class="content"><h2>Main Content</h2><p>This is the main content area. Resize the window to see the responsive effect.</p></div>
      <div class="sidebar"><h3>Sidebar</h3><p>This is a sidebar with some extra information or links.</p></div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact Me</h2>
    <form id="contact-form">
      <input type="text" name="user_name" placeholder="Your Name" required>
      <input type="email" name="user_email" placeholder="Your Email" required>
      <textarea name="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="form-status"></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 MR__ Abishek | All rights reserved</p>
  </footer>

  <!-- Scripts -->
  <script>
    /* Quiz Logic */
    const quizData = [
      { question: "which HTML tag is used to create a hyperlink?", a: "<link>", b: "<a>", c: "<href>", d: "<url>", correct: "b" },
      { question: "Which language is used for styling web pages?", a: "HTML", b: "JQuery", c: "CSS", d: "XML", correct: "c" },
      { question: "Which is not a JavaScript Framework?", a: "React", b: "Angular", c: "Vue", d: "Django", correct: "d" },
      { question: "Which is used for database?", a: "PHP", b: "MySQL", c: "HTML", d: "CSS", correct: "b" }
    ];
    const quiz = document.getElementById("quiz-box");
    const answerEls = document.querySelectorAll(".answer");
    const questionEl = document.getElementById("question");
    const a_text = document.getElementById("a_text");
    const b_text = document.getElementById("b_text");
    const c_text = document.getElementById("c_text");
    const d_text = document.getElementById("d_text");
    const submitBtn = document.getElementById("submit");
    const resultEl = document.getElementById("result");
    let currentQuiz = 0, score = 0;
    loadQuiz();
    function loadQuiz() {
      deselectAnswers();
      const currentQuizData = quizData[currentQuiz];
      questionEl.innerText = currentQuizData.question;
      a_text.innerText = currentQuizData.a;
      b_text.innerText = currentQuizData.b;
      c_text.innerText = currentQuizData.c;
      d_text.innerText = currentQuizData.d;
    }
    function getSelected() {
      let answer = undefined;
      answerEls.forEach((el) => { if (el.checked) answer = el.id; });
      return answer;
    }
    function deselectAnswers() { answerEls.forEach((el) => el.checked = false); }
    submitBtn.addEventListener("click", () => {
      const answer = getSelected();
      if (answer) {
        if (answer === quizData[currentQuiz].correct) score++;
        currentQuiz++;
        if (currentQuiz < quizData.length) loadQuiz();
        else quiz.innerHTML = `<h2 class="result">You answered correctly ${score}/${quizData.length} questions.</h2><button onclick="location.reload()">Restart</button>`;
      }
    });

    /* Blog Loader */
    function loadPosts() {
      const postsContainer = document.getElementById("postsContainer");
      const posts = JSON.parse(localStorage.getItem("blogPosts")) || [];
      postsContainer.innerHTML = "";
      posts.reverse().forEach(post => {
        const postEl = document.createElement("div");
        postEl.classList.add("post");
        postEl.innerHTML = `<h2>${post.title}</h2><small>${new Date(post.date).toLocaleString()}</small><p>${post.content}</p>`;
        postsContainer.appendChild(postEl);
      });
    }
    loadPosts();
  </script>
</body>
</html>
