# Techcart-Ecommerce-Site
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechCart - Home</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header>
    <h1>TechCart</h1>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="products.html">Products</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero">
      <h2>Welcome to TechCart</h2>
      <p>Your one-stop shop for all things tech!</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 TechCart. All rights reserved.</p>
  </footer>
</body>
</html>

<!-- products.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechCart - Products</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header>
    <h1>TechCart</h1>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="products.html">Products</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="product-list">
      <article class="product">
        <h3>Smartphone</h3>
        <img src="images/smartphone.jpg" alt="Smartphone">
        <p>$699</p>
        <button onclick="addToCart('Smartphone')">Add to Cart</button>
      </article>
      <article class="product">
        <h3>Laptop</h3>
        <img src="images/laptop.jpg" alt="Laptop">
        <p>$999</p>
        <button onclick="addToCart('Laptop')">Add to Cart</button>
      </article>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 TechCart. All rights reserved.</p>
  </footer>
  <script src="js/script.js"></script>
</body>
</html>

<!-- contact.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechCart - Contact</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header>
    <h1>TechCart</h1>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="products.html">Products</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="contact-form">
      <h2>Contact Us</h2>
      <form id="contactForm">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>

        <label for="message">Message:</label>
        <textarea id="message" name="message" required></textarea>

        <button type="submit">Send</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 TechCart. All rights reserved.</p>
  </footer>
  <script src="js/script.js"></script>
</body>
</html>

/* style.css */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.6;
}

header {
  background-color: #333;
  color: #fff;
  padding: 1rem;
  text-align: center;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  padding: 0;
}

nav ul li {
  margin: 0 15px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
}

.hero {
  text-align: center;
  padding: 2rem;
}

.product-list {
  display: flex;
  justify-content: center;
  gap: 2rem;
  padding: 2rem;
}

.product {
  border: 1px solid #ccc;
  padding: 1rem;
  text-align: center;
  max-width: 200px;
}

.contact-form {
  padding: 2rem;
  max-width: 600px;
  margin: auto;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 0.5rem;
  margin-bottom: 1rem;
}

footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 1rem;
  position: fixed;
  width: 100%;
  bottom: 0;
}

/* script.js */
function addToCart(productName) {
  alert(productName + " added to cart!");
}

document.getElementById("contactForm")?.addEventListener("submit", function (e) {
  e.preventDefault();
  const name = document.getElementById("name").value;
  const email = document.getElementById("email").value;
  const message = document.getElementById("message").value;

  if (name && email && message) {
    alert("Thank you, " + name + "! Your message has been sent.");
    this.reset();
  } else {
    alert("Please fill in all fields.");
  }
});
