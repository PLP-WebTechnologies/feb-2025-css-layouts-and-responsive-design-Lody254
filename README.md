<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Layout</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <nav class="navbar">
    <div class="logo">MySite</div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <main class="content-grid">
    <section class="item item1">Content 1</section>
    <section class="item item2">Content 2</section>
    <section class="item item3">Content 3</section>
    <section class="item item4">Content 4</section>
  </main>

  <footer class="footer">© 2025 MySite. All rights reserved.</footer>
</body>
</html>


/* General Reset and Fonts */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

/* Navigation Bar using Flexbox */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #0a192f;
  color: white;
  padding: 1rem 2rem;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links li a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

/* Grid Layout */
.content-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  padding: 2rem;
  flex: 1;
}

.item {
  background-color: #e3e3e3;
  padding: 1.5rem;
  border-radius: 8px;
  text-align: center;
  font-size: 1.2rem;
}

.footer {
  background-color: #0a192f;
  color: white;
  text-align: center;
  padding: 1rem;
}

/* Media Queries for Responsive Design */
@media (max-width: 768px) {
  .content-grid {
    grid-template-columns: 1fr;
  }

  .nav-links {
    flex-direction: column;
    gap: 0.5rem;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  .content-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1025px) {
  .content-grid {
    grid-template-columns: repeat(4, 1fr);
  }
}
