```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Williams Dakota | Creative Developer</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --purple: #8b5cf6;
      --dark-purple: #6d28d9;
      --black: #07070a;
      --card: #111116;
      --white: #ffffff;
      --gray: #a1a1aa;
      --border: rgba(139, 92, 246, 0.25);
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: var(--black);
      color: var(--white);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font-family: inherit;
    }

    /* NAVIGATION */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(7, 7, 10, 0.88);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid var(--border);
    }

    nav {
      max-width: 1200px;
      margin: auto;
      height: 75px;
      padding: 0 25px;

      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 23px;
      font-weight: 900;
      color: var(--white);
    }

    .logo span {
      color: var(--purple);
    }

    .nav-links {
      display: flex;
      list-style: none;
      gap: 30px;
    }

    .nav-links a {
      color: #ddd;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: var(--purple);
    }

    .menu-btn {
      display: none;
      background: transparent;
      border: none;
      color: white;
      font-size: 28px;
      cursor: pointer;
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      padding: 150px 25px 80px;

      display: flex;
      align-items: center;
      justify-content: center;

      background:
        radial-gradient(circle at 20% 30%, rgba(139, 92, 246, 0.22), transparent 30%),
        radial-gradient(circle at 80% 70%, rgba(109, 40, 217, 0.15), transparent 30%),
        var(--black);
    }

    .hero-content {
      max-width: 1100px;
      width: 100%;
    }

    .welcome {
      color: var(--purple);
      font-weight: bold;
      letter-spacing: 3px;
      text-transform: uppercase;
      margin-bottom: 15px;
    }

    .hero h1 {
      font-size: clamp(50px, 9vw, 105px);
      line-height: 0.95;
      max-width: 900px;
      margin-bottom: 25px;
    }

    .hero h1 span {
      color: var(--purple);
    }

    .hero p {
      max-width: 700px;
      color: var(--gray);
      font-size: 20px;
      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
    }

    .btn {
      display: inline-block;
      padding: 14px 24px;
      border-radius: 10px;
      font-weight: bold;
      cursor: pointer;
      border: none;
      transition: 0.3s;
    }

    .btn-primary {
      background: var(--purple);
      color: white;
    }

    .btn-primary:hover {
      background: var(--dark-purple);
      transform: translateY(-3px);
    }

    .btn-outline {
      border: 1px solid var(--purple);
      background: transparent;
      color: white;
    }

    .btn-outline:hover {
      background: var(--purple);
      transform: translateY(-3px);
    }

    /* GENERAL */

    section {
      padding: 100px 25px;
    }

    .container {
      max-width: 1200px;
      margin: auto;
    }

    .section-title {
      margin-bottom: 45px;
    }

    .section-title small {
      color: var(--purple);
      font-weight: bold;
      text-transform: uppercase;
      letter-spacing: 2px;
    }

    .section-title h2 {
      font-size: clamp(35px, 5vw, 60px);
      margin-top: 8px;
    }

    .section-title p {
      color: var(--gray);
      max-width: 650px;
      margin-top: 10px;
    }

    /* ABOUT */

    .about {
      background: #0c0c10;
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 50px;
      align-items: center;
    }

    .about-text p {
      color: var(--gray);
      font-size: 18px;
      margin-bottom: 20px;
    }

    .about-box {
      border: 1px solid var(--border);
      background: var(--card);
      padding: 35px;
      border-radius: 20px;
      box-shadow: 0 20px 50px rgba(0,0,0,0.3);
    }

    .about-box h3 {
      color: var(--purple);
      margin-bottom: 15px;
    }

    /* SERVICES */

    .services-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
    }

    .service {
      padding: 28px;
      border-radius: 18px;
      background: var(--card);
      border: 1px solid var(--border);
      transition: 0.3s;
    }

    .service:hover {
      transform: translateY(-8px);
      border-color: var(--purple);
    }

    .service-icon {
      font-size: 35px;
      margin-bottom: 15px;
    }

    .service h3 {
      margin-bottom: 10px;
    }

    .service p {
      color: var(--gray);
      font-size: 14px;
    }

    /* WORK */

    .work-section {
      background: #0c0c10;
    }

    .work-controls {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      margin-bottom: 30px;
      flex-wrap: wrap;
    }

    .work-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .project {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 18px;
      overflow: hidden;
      transition: 0.3s;
    }

    .project:hover {
      transform: translateY(-8px);
      border-color: var(--purple);
    }

    .project-image {
      width: 100%;
      height: 210px;
      object-fit: cover;
      display: block;
      background: #18181d;
    }

    .project-body {
      padding: 22px;
    }

    .project-category {
      color: var(--purple);
      font-size: 12px;
      text-transform: uppercase;
      font-weight: bold;
    }

    .project h3 {
      margin: 7px 0;
    }

    .project p {
      color: var(--gray);
      font-size: 14px;
      margin-bottom: 18px;
    }

    .project-actions {
      display: flex;
      gap: 8px;
    }

    .small-btn {
      padding: 9px 13px;
      border-radius: 8px;
      border: 1px solid var(--border);
      background: transparent;
      color: white;
      cursor: pointer;
    }

    .small-btn:hover {
      background: var(--purple);
    }

    .delete-btn:hover {
      background: #dc2626;
      border-color: #dc2626;
    }

    /* DEVELOPER REVIEW */

    .developer-section {
      background: var(--black);
    }

    .review-list {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
    }

    .review-item {
      padding: 22px;
      border: 1px solid var(--border);
      background: var(--card);
      border-radius: 15px;
      cursor: pointer;
      transition: 0.3s;
    }

    .review-item:hover {
      border-color: var(--purple);
      transform: translateX(5px);
    }

    .review-number {
      color: var(--purple);
      font-weight: bold;
      margin-right: 10px;
    }

    /* CONTACT */

    .contact {
      text-align: center;
      background:
        radial-gradient(circle at center, rgba(139, 92, 246, 0.18), transparent 40%),
        var(--black);
    }

    .contact p {
      color: var(--gray);
      max-width: 600px;
      margin: 15px auto 30px;
    }

    /* MODAL */

    .modal {
      display: none;
      position: fixed;
      z-index: 2000;
      inset: 0;
      background: rgba(0,0,0,0.8);
      padding: 30px;
      overflow-y: auto;
    }

    .modal.active {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .modal-content {
      width: 100%;
      max-width: 600px;
      background: #111116;
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 30px;
      position: relative;
    }

    .close {
      position: absolute;
      right: 20px;
      top: 15px;
      font-size: 25px;
      cursor: pointer;
    }

    .modal-content h2 {
      margin-bottom: 20px;
    }

    .form-group {
      margin-bottom: 18px;
    }

    .form-group label {
      display: block;
      margin-bottom: 7px;
      color: #ddd;
    }

    .form-group input,
    .form-group textarea,
    .form-group select {
      width: 100%;
      padding: 13px;
      border-radius: 9px;
      border: 1px solid #333;
      background: #08080b;
      color: white;
      outline: none;
    }

    .form-group textarea {
      min-height: 120px;
      resize: vertical;
    }

    .form-group input:focus,
    .form-group textarea:focus,
    .form-group select:focus {
      border-color: var(--purple);
    }

    /* FOOTER */

    footer {
      padding: 30px 25px;
      border-top: 1px solid var(--border);
      text-align: center;
      color: var(--gray);
    }

    footer span {
      color: var(--purple);
    }

    /* RESPONSIVE */

    @media (max-width: 900px) {
      .services-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .work-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .about-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 650px) {
      .nav-links {
        display: none;
        position: absolute;
        top: 75px;
        left: 0;
        width: 100%;
        background: #08080b;
        flex-direction: column;
        padding: 25px;
        text-align: center;
      }

      .nav-links.active {
        display: flex;
      }

      .menu-btn {
        display: block;
      }

      .services-grid,
      .work-grid,
      .review-list {
        grid-template-columns: 1fr;
      }

      .hero {
        padding-top: 130px;
      }

      .hero p {
        font-size: 17px;
      }

      section {
        padding: 75px 20px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <header>
    <nav>
      <a href="#home" class="logo">Williams<span>Dakota</span></a>

      <button class="menu-btn" onclick="toggleMenu()">☰</button>

      <ul class="nav-links" id="navLinks">
        <li><a href="#home" onclick="closeMenu()">Home</a></li>
        <li><a href="#about" onclick="closeMenu()">About</a></li>
        <li><a href="#services" onclick="closeMenu()">Services</a></li>
        <li><a href="#work" onclick="closeMenu()">My Work</a></li>
        <li><a href="#contact" onclick="closeMenu()">Contact</a></li>
      </ul>
    </nav>
  </header>


  <!-- HERO -->

  <section class="hero" id="home">
    <div class="hero-content">

      <div class="welcome">Welcome to my portfolio</div>

      <h1>
        I'm <span>Williams</span> Dakota.
        <br>
        I bring ideas to life through code.
      </h1>

      <p>
        I'm a creative developer who builds games, flyers, websites,
        UI/UX experiences and digital products that turn ideas into
        something people can actually use and enjoy.
      </p>

      <div class="buttons">
        <a href="#work" class="btn btn-primary">Explore My Work</a>
        <a href="#contact" class="btn btn-outline">Let's Work Together</a>
      </div>

    </div>
  </section>


  <!-- ABOUT -->

  <section class="about" id="about">
    <div class="container">

      <div class="section-title">
        <small>About Me</small>
        <h2>Turning ideas into reality.</h2>
      </div>

      <div class="about-grid">

        <div class="about-text">
          <p>
            Welcome! I'm Williams Dakota, a developer and creative
            designer who enjoys turning concepts into digital experiences.
          </p>

          <p>
            From game development to UI/UX design and promotional flyers,
            I combine creativity and technology to create projects that
            stand out.
          </p>

          <p>
            Every project is an opportunity to learn something new,
            solve a problem and create something meaningful.
          </p>
        </div>

        <div class="about-box">
          <h3>What I Believe</h3>
          <p>
            Great digital products start with a good idea,
            but great execution brings that idea to life.
          </p>
        </div>

      </div>
    </div>
  </section>


  <!-- SERVICES -->

  <section id="services">
    <div class="container">

      <div class="section-title">
        <small>What I Do</small>
        <h2>My Services</h2>
        <p>
          Creative and development services for digital projects.
        </p>
      </div>

      <div class="services-grid">

        <div class="service">
          <div class="service-icon">🎮</div>
          <h3>Game Development</h3>
          <p>I develop interactive games and gameplay experiences.</p>
        </div>

        <div class="service">
          <div class="service-icon">🎨</div>
          <h3>Flyer Design</h3>
          <p>Modern promotional graphics for brands and projects.</p>
        </div>

        <div class="service">
          <div class="service-icon">🖥️</div>
          <h3>UI Design</h3>
          <p>Clean and attractive interfaces for websites and apps.</p>
        </div>

        <div class="service">
          <div class="service-icon">✨</div>
          <h3>UX Design</h3>
          <p>User-focused experiences designed around real needs.</p>
        </div>

      </div>
    </div>
  </section>


  <!-- WORK -->

  <section class="work-section" id="work">
    <div class="container">

      <div class="section-title">
        <small>Portfolio</small>
        <h2>My Work</h2>
        <p>
          Add, edit and remove your projects directly from this page.
        </p>
      </div>

      <div class="work-controls">
        <p id="projectCount">0 projects</p>

        <button class="btn btn-primary" onclick="openAddModal()">
          + Add New Work
        </button>
      </div>

      <div class="work-grid" id="workGrid"></div>

    </div>
  </section>


  <!-- DEVELOPER REVIEW -->

  <section class="developer-section">
    <div class="container">

      <div class="section-title">
        <small>Development Standards</small>
        <h2>How I Build</h2>
        <p>
          A clean development process focused on quality,
          maintainability and real-world results.
        </p>
      </div>

      <div class="review-list">

        <div class="review-item">
          <span class="review-number">01</span>
          Review the code and find bugs before changing anything. 🔍
        </div>

        <div class="review-item">
          <span class="review-number">02</span>
          Refactor code without changing its behavior. 🛠️
        </div>

        <div class="review-item">
          <span class="review-number">03</span>
          Make UI responsive for mobile, tablet and desktop. 📱
        </div>

        <div class="review-item">
          <span class="review-number">04</span>
          Explain errors and fix the root cause. 🐛
        </div>

        <div class="review-item">
          <span class="review-number">05</span>
          Improve performance and explain what changed. ⚡
        </div>

        <div class="review-item">
          <span class="review-number">06</span>
          Add proper error handling and edge-case validation. 🛡️
        </div>

        <div class="review-item">
          <span class="review-number">07</span>
          Write clean, production-ready code with clear comments. 🚀
        </div>

        <div class="review-item">
          <span class="review-number">08</span>
          Create tests and cover important edge cases. 🧪
        </div>

        <div class="review-item">
          <span class="review-number">09</span>
          Think about accessibility and user experience.
        </div>

        <div class="review-item">
          <span class="review-number">10</span>
          Approach every project like a senior developer.
        </div>

      </div>
    </div>
  </section>


  <!-- CONTACT -->

  <section class="contact" id="contact">
    <div class="container">

      <div class="section-title">
        <small>Let's Create</small>
        <h2>Have an idea?</h2>
      </div>

      <p>
        Let's turn your idea into something real.
        Whether it's a game, website, flyer or UI/UX project,
        I'm ready to build.
      </p>

      <a
        href="mailto:your@email.com"
        class="btn btn-primary">
        Contact Williams
      </a>

    </div>
  </section>


  <!-- FOOTER -->

  <footer>
    © 2026 <span>Williams Dakota</span>. Built with code & creativity.
  </footer>


  <!-- ADD/EDIT MODAL -->

  <div class="modal" id="projectModal">

    <div class="modal-content">

      <span class="close" onclick="closeModal()">×</span>

      <h2 id="modalTitle">Add New Work</h2>

      <form id="projectForm">

        <div class="form-group">
          <label>Project Name</label>
          <input
            type="text"
            id="projectName"
            placeholder="e.g. My Roblox Game"
            required>
        </div>

        <div class="form-group">
          <label>Category</label>

          <select id="projectCategory">
            <option>Game Development</option>
            <option>Flyer Design</option>
            <option>UI Design</option>
            <option>UX Design</option>
            <option>Website</option>
            <option>Other</option>
          </select>
        </div>

        <div class="form-group">
          <label>Project Description</label>

          <textarea
            id="projectDescription"
            placeholder="Describe your project..."
            required></textarea>
        </div>

        <div class="form-group">
          <label>Project Image URL</label>

          <input
            type="url"
            id="projectImage"
            placeholder="https://example.com/image.jpg"
            required>
        </div>

        <div class="form-group">
          <label>Project Link</label>

          <input
            type="url"
            id="projectLink"
            placeholder="https://yourproject.com">
        </div>

        <button
          type="submit"
          class="btn btn-primary"
          style="width:100%;">
          Save Project
        </button>

      </form>

    </div>
  </div>


  <script>

    /*
      PORTFOLIO DATA
      -----------------------------
      Projects are stored in localStorage.
    */

    let projects = JSON.parse(
      localStorage.getItem("williamsPortfolioProjects")
    ) || [];

    let editingId = null;


    /* MOBILE MENU */

    function toggleMenu() {
      document
        .getElementById("navLinks")
        .classList.toggle("active");
    }

    function closeMenu() {
      document
        .getElementById("navLinks")
        .classList.remove("active");
    }


    /* MODAL */

    function openAddModal() {

      editingId = null;

      document.getElementById("modalTitle").textContent =
        "Add New Work";

      document.getElementById("projectForm").reset();

      document
        .getElementById("projectModal")
        .classList.add("active");
    }

    function closeModal() {

      document
        .getElementById("projectModal")
        .classList.remove("active");

      editingId = null;
    }


    /* SAVE */

    document
      .getElementById("projectForm")
      .addEventListener("submit", function(event) {

        event.preventDefault();

        const name =
          document.getElementById("projectName").value.trim();

        const category =
          document.getElementById("projectCategory").value;

        const description =
          document.getElementById("projectDescription").value.trim();

        const image =
          document.getElementById("projectImage").value.trim();

        const link =
          document.getElementById("projectLink").value.trim();


        if (!name || !description || !image) {
          alert("Please complete the required fields.");
          return;
        }


        if (editingId) {

          const project = projects.find(
            p => p.id === editingId
          );

          if (project) {
            project.name = name;
            project.category = category;
            project.description = description;
            project.image = image;
            project.link = link;
          }

        } else {

          projects.push({

            id: Date.now(),

            name,
            category,
            description,
            image,
            link

          });

        }


        saveProjects();

        renderProjects();

        closeModal();

      });


    /* SAVE TO BROWSER */

    function saveProjects() {

      localStorage.setItem(
        "williamsPortfolioProjects",
        JSON.stringify(projects)
      );

    }


    /* DISPLAY PROJECTS */

    function renderProjects() {

      const grid =
        document.getElementById("workGrid");

      const count =
        document.getElementById("projectCount");


      grid.innerHTML = "";

      count.textContent =
        `${projects.length} project${projects.length === 1 ? "" : "s"}`;


      if (projects.length === 0) {

        grid.innerHTML = `

          <div style="
            grid-column:1/-1;
            text-align:center;
            padding:70px 20px;
            border:1px dashed #333;
            border-radius:18px;
          ">

            <div style="font-size:45px;">🚀</div>

            <h3>No projects yet</h3>

            <p style="color:#999;margin:10px 0 20px;">
              Add your first project to start building your portfolio.
            </p>

            <button
              class="btn btn-primary"
              onclick="openAddModal()">
              Add My First Work
            </button>

          </div>

        `;

        return;
      }


      projects.forEach(project => {

        const card =
          document.createElement("div");

        card.className = "project";


        card.innerHTML = `

          <img
            class="project-image"
            src="${escapeHTML(project.image)}"
            alt="${escapeHTML(project.name)}"
            onerror="this.src='https://placehold.co/800x500/111116/ffffff?text=Project+Image'"
          >

          <div class="project-body">

            <div class="project-category">
              ${escapeHTML(project.category)}
            </div>

            <h3>
              ${escapeHTML(project.name)}
            </h3>

            <p>
              ${escapeHTML(project.description)}
            </p>

            <div class="project-actions">

              ${
                project.link
                ? `
                  <a
                    href="${escapeHTML(project.link)}"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="small-btn">
                    View ↗
                  </a>
                `
                : ""
              }

              <button
                class="small-btn"
                onclick="editProject(${project.id})">
                Edit
              </button>

              <button
                class="small-btn delete-btn"
                onclick="deleteProject(${project.id})">
                Delete
              </button>

            </div>

          </div>

        `;


        grid.appendChild(card);

      });

    }


    /* EDIT */

    function editProject(id) {

      const project =
        projects.find(p => p.id === id);

      if (!project) return;

      editingId = id;


      document.getElementById("modalTitle").textContent =
        "Edit Work";


      document.getElementById("projectName").value =
        project.name;

      document.getElementById("projectCategory").value =
        project.category;

      document.getElementById("projectDescription").value =
        project.description;

      document.getElementById("projectImage").value =
        project.image;

      document.getElementById("projectLink").value =
        project.link || "";


      document
        .getElementById("projectModal")
        .classList.add("active");

    }


    /* DELETE */

    function deleteProject(id) {

      const project =
        projects.find(p => p.id === id);

      if (!project) return;


      const confirmed =
        confirm(
          `Delete "${project.name}" from your portfolio?`
        );


      if (!confirmed) return;


      projects =
        projects.filter(p => p.id !== id);

      saveProjects();

      renderProjects();

    }


    /* SECURITY */

    function escapeHTML(value) {

      return String(value)
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;")
        .replace(/'/g, "&#039;");

    }


    /* CLOSE MODAL WHEN CLICKING OUTSIDE */

    document
      .getElementById("projectModal")
      .addEventListener("click", function(event) {

        if (event.target === this) {
          closeModal();
        }

      });


    /* START */

    renderProjects();

  </script>

</body>
</html>
```

