# Growth-Mindset-Community
its a website for a new professional program community that embraces all the professions and new rising generations 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Growth Mindset Community</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <!-- Navbar -->
  <nav class="navbar">
    <div class="logo">Growth Mindset</div>
    <div class="menu-toggle" id="mobile-menu">
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>
    </div>
    <ul class="nav-links">
      <li><a href="#intro">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#membership">Membership</a></li>
      <li><a href="#schedule">Schedule</a></li>
      <li><a href="#participation">Participate</a></li>
    </ul>
  </nav>

  <!-- Intro Section -->
  <section id="intro" class="section-intro">
    <h1>Welcome to the Growth Mindset Community</h1>
    <p>Professionals uniting to inspire and uplift the next generation.</p>
  </section>

  <!-- About Section -->
  <section id="about" class="section-about">
    <h2>About the Community</h2>
    <p>We are a network of driven professionals dedicated to personal development, lifelong learning, and mentorship. Together, we build a foundation to guide emerging leaders.</p>
  </section>

  <!-- Membership Section -->
  <section id="membership" class="section-membership">
    <h2>Membership</h2>
    <div class="cards">
      <div class="card">
        <h3>Standard</h3>
        <p>Access to forums, monthly newsletter, and community events.</p>
      </div>
      <div class="card">
        <h3>Premium</h3>
        <p>All Standard perks plus exclusive workshops and mentorship circles.</p>
      </div>
      <div class="card">
        <h3>Champion</h3>
        <p>All Premium benefits plus speaking opportunities and leadership roles.</p>
      </div>
    </div>
  </section>

  <!-- Schedule Section -->
  <section id="schedule" class="section-schedule">
    <h2>Upcoming Events</h2>
    <ul class="schedule-list">
      <li><strong>May 10, 2025</strong> — Workshop: "Mentorship in the Digital Age"</li>
      <li><strong>June 1, 2025</strong> — Lecture: "Building a Personal Brand"</li>
      <li><strong>July 15, 2025</strong> — Debate: "AI in Professional Development"</li>
    </ul>
  </section>

  <!-- Participation Section -->
  <section id="participation" class="section-participation">
    <h2>Get Involved</h2>
    <p>Submit an article or apply to be a guest speaker:</p>
    <form id="participation-form" class="participation-form">
      <input type="text" name="name" placeholder="Your Name" required />
      <input type="email" name="email" placeholder="Your Email" required />
      <select name="role">
        <option value="article">Article Contributor</option>
        <option value="speaker">Guest Speaker</option>
      </select>
      <textarea name="details" placeholder="Describe your topic..." required></textarea>
      <button type="submit">Submit</button>
      <p id="form-msg" class="form-msg"></p>
    </form>
  </section>

  <footer class="footer">
    <p>&copy; 2025 Growth Mindset Community</p>
  </footer>

  <!-- Scripts -->
  <script>
    const mobileMenu = document.getElementById('mobile-menu');
    const navLinks = document.querySelector('.nav-links');
    mobileMenu.addEventListener('click', () => {
      mobileMenu.classList.toggle('is-active');
      navLinks.classList.toggle('active');
    });

    document.getElementById('participation-form').addEventListener('submit', function(e) {
      e.preventDefault();
      document.getElementById('form-msg').innerText = 'Thank you for your submission!';
      this.reset();
    });
  </script>
</body>
</html>

/* styles.css */
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f0f4f8;
  color: #002244;
  scroll-behavior: smooth;
}
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #001833;
  padding: 1rem 2rem;
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 100;
}
.logo {
  color: #ffffff;
  font-size: 1.5rem;
  font-weight: bold;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}
.nav-links li a {
  color: #ffffff;
  text-decoration: none;
  transition: color 0.3s;
}
.nav-links li a:hover {
  color: #69a1ff;
}
.menu-toggle {
  display: none;
  flex-direction: column;
  cursor: pointer;
}
.bar {
  height: 3px;
  width: 25px;
  background-color: #ffffff;
  margin: 4px 0;
  transition: 0.3s;
}
.section-intro {
  text-align: center;
  padding: 8rem 2rem 4rem;
  background: #e1eaf4;
}
.section-intro h1 {
  font-size: 2.5rem;
  margin: 0 0 1rem;
  animation: fadeInDown 1s ease-out;
}
.section-intro p {
  font-size: 1.2rem;
  animation: fadeInUp 1s ease-out;
}
.section {
  padding: 4rem 2rem;
  max-width: 900px;
  margin: auto;
}
.section-membership .cards {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}
.card {
  background: #ffffff;
  border: 1px solid #ccddee;
  padding: 1.5rem;
  flex: 1;
  min-width: 250px;
  transition: transform 0.3s;
}
.card:hover {
  transform: translateY(-5px);
}
.section-schedule .schedule-list {
  list-style: none;
  padding: 0;
}
.section-schedule .schedule-list li {
  background: #ffffff;
  margin-bottom: 1rem;
  padding: 1rem;
  border-left: 4px solid #002244;
  opacity: 0;
  animation: fadeIn 0.8s forwards;
}
.section-participation .form-msg {
  color: #004488;
  margin-top: 0.5rem;
}
.participation-form input,
.participation-form select,
.participation-form textarea {
  width: 100%;
  margin-bottom: 1rem;
  padding: 0.75rem;
  border: 1px solid #ccddee;
  transition: border-color 0.3s;
}
.participation-form input:focus,
.participation-form select:focus,
.participation-form textarea:focus {
  border-color: #69a1ff;
}
.participation-form button {
  background: #002244;
  color: #ffffff;
  border: none;
  padding: 0.75rem 1.5rem;
  cursor: pointer;
  transition: background 0.3s;
}
.participation-form button:hover {
  background: #003366;
}
.footer {
  text-align: center;
  padding: 2rem;
  background: #001833;
  color: #ffffff;
}
/* Responsive */
@media (max-width: 768px) {
  .nav-links {
    position: absolute;
    right: 0;
    top: 70px;
    background: #001833;
    height: calc(100vh - 70px);
    flex-direction: column;
    width: 100%;
    align-items: center;
    transform: translateX(100%);
    transition: transform 0.3s ease-in;
  }
  .nav-links.active {
    transform: translateX(0);
  }
  .menu-toggle {
    display: flex;
  }
}
/* Animations */
@keyframes fadeInDown {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
