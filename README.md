<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ASPHALT | Streetwear Redefined</title>

  <link href="https://fonts.googleapis.com/css2?family=Permanent+Marker&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css">

  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
</head>
<body>

  <div class="theme-toggle" onclick="toggleTheme()">
    <span id="toggle-icon">🌙</span>
  </div>

  <header class="navbar">
    <div class="logo">ASPHALT</div>
    <nav>
      <a href="#hero">Home</a>
      <a href="#shop">Shop</a>
      <a href="#drops">Drops</a>
      <a href="#contact">Contact</a>
      <a href="mailto:info@asphaltwear.com">Email</a>
      <a href="#cart" class="cart-btn">🛒</a>
    </nav>
  </header>

  <section id="hero" class="hero">
    <div class="hero-text">
      <h1 class="brand-title">ASPHALT</h1>
      <p class="tagline">Built for streets. Worn by kings.</p>
      <a href="#shop" class="btn">Explore Collection</a>
    </div>
  </section>

  <section id="shop" class="reveal section">
    <h2 class="section-title">🧥 Featured Collection</h2>
    <div class="items">
      <div class="item">
        <img src="images/hoodie.png" alt="Hoodie">
        <p>Blackout Hoodie</p>
        <button class="add-to-cart" data-name="Blackout Hoodie" data-price="45$">Add to Cart</button>
      </div>
      <div class="item">
        <img src="images/tshirt.png" alt="T-Shirt">
        <p>Street Graphic Tee</p>
        <button class="add-to-cart" data-name="Street Graphic Tee" data-price="30$">Add to Cart</button>
      </div>
      <div class="item">
        <img src="images/cap.png" alt="Cap">
        <p>Classic Snapback</p>
        <button class="add-to-cart" data-name="Classic Snapback" data-price="20$">Add to Cart</button>
      </div>
    </div>
  </section>

  <section id="drops" class="reveal section">
    <h2 class="section-title">🔥 Latest Drops</h2>
    <div class="items">
      <div class="item">
        <img src="images/drop1.png" alt="Drop 1">
        <p>Urban Jungle Jacket</p>
      </div>
      <div class="item">
        <img src="images/drop2.png" alt="Drop 2">
        <p>Futuristic Track Pants</p>
      </div>
    </div>
  </section>

  <section id="contact" class="reveal section">
    <h2 class="section-title">📞 Contact Us</h2>
    <p>Email: <a href="mailto:info@asphaltwear.com">info@asphaltwear.com</a></p>
    <p>Instagram: @asphaltwear</p>
  </section>

  <footer class="footer">
    &copy; 2025 ASPHALT — All Rights Reserved.  
    <br>Stay bold. Stay original.
  </footer>

  <script src="script.js"></script>
</body>
</html>
/* General Reset & Fonts */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  background: #111;
  color: #fff;
  overflow-x: hidden;
}

/* Hero Section */
.hero {
  position: relative;
  height: 100vh;
  background: url('https://images.unsplash.com/photo-1503341455253-b2e723bb3dbb?auto=format&fit=crop&w=1400&q=80') center/cover no-repeat;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5); /* Transparent dark overlay */
  z-index: 1;
}

.hero-text {
  position: relative;
  z-index: 2;
}

.brand-title {
  font-family: 'Permanent Marker', cursive;
  font-size: 4rem;
  color: #fff;
  text-shadow: 2px 2px 10px rgba(0,0,0,0.7);
  margin-bottom: 0.5rem;
}

.tagline {
  font-size: 1.5rem;
  color: #ccc;
  margin-bottom: 2rem;
}

.btn {
  display: inline-block;
  background: #e91e63;
  color: #fff;
  padding: 0.8rem 2rem;
  border: none;
  border-radius: 40px;
  font-weight: 600;
  text-decoration: none;
  box-shadow: 0 4px 20px rgba(233, 30, 99, 0.5);
  transition: background 0.3s ease;
}

.btn:hover {
  background: #c2185b;
}

/* General button base */
button,
.btn {
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
  background-color: #111;         /* dark base */
  color: #fff;
  padding: 0.75em 1.8em;
  border: 2px solid transparent;
  border-radius: 30px;
  cursor: pointer;
  text-transform: uppercase;
  letter-spacing: 1.2px;
  transition: 
    background-color 0.3s ease, 
    color 0.3s ease, 
    box-shadow 0.3s ease,
    transform 0.2s ease;
  box-shadow: 0 4px 8px rgba(0,0,0,0.25);
  user-select: none;
}

/* Button hover effect */
button:hover,
.btn:hover {
  background-color: transparent;
  color: #ff3e00;  /* vibrant orange/red accent */
  border-color: #ff3e00;
  box-shadow: 0 6px 12px rgba(255, 62, 0, 0.6);
  transform: scale(1.05);
}

/* Add-to-cart specific tweaks */
.add-to-cart {
  font-size: 0.9rem;
  padding: 0.5em 1.3em;
  border-radius: 20px;
  box-shadow: 0 3px 6px rgba(0,0,0,0.2);
  background-color: #222;
  color: #f5f5f5;
  border: 2px solid transparent;
}

.add-to-cart:hover {
  background-color: #ff3e00;
  color: #fff;
  border-color: transparent;
  box-shadow: 0 8px 15px rgba(255, 62, 0, 0.7);
  transform: scale(1.1);
}

/* Anchor .btn link style */
a.btn {
  display: inline-block;
  text-decoration: none;
  text-align: center;
}

/* Make sure buttons don't get weird outlines on click */
button:focus,
button:active,
.btn:focus,
.btn:active {
  outline: none;
  box-shadow: 0 0 0 3px rgba(255, 62, 0, 0.5);
}

/* Optional: smooth transition on the cursor */
button,
.btn {
  will-change: transform, background-color, color, box-shadow;
}
window.addEventListener("load", () => {
  const heroText = document.querySelector(".hero-text");
  if (heroText) {
    heroText.style.opacity = 0;
    heroText.style.transform = "translateY(20px)";
    setTimeout(() => {
      heroText.style.transition = "all 1s ease";
      heroText.style.opacity = 1;
      heroText.style.transform = "translateY(0)";
    }, 300);
  }
});

