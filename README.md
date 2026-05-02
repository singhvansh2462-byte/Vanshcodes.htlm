<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vansh | Web Designer</title>
  <style>
    /* Background Animation */
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(-45deg, #0f2027, #203a43, #2c5364, #007BFF, #00C9FF, #92FE9D);
      background-size: 600% 600%;
      animation: gradientBG 20s ease infinite;
      color: white;
      transition: background 0.5s ease, color 0.5s ease;
    }
    @keyframes gradientBG {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }

    /* Dark Mode */
    body.dark {
      background: #121212;
      color: #f5f5f5;
    }
    body.dark header, body.dark footer {
      background: #1f1f1f;
    }
    body.dark nav {
      background: #333;
    }
    body.dark .card {
      background: #222;
      color: #f5f5f5;
    }

    /* Header */
    header {
      text-align: center;
      padding: 40px;
      background: rgba(0,123,255,0.85);
      box-shadow: 0 5px 25px rgba(0,0,0,0.5);
      animation: fadeInDown 2s ease;
      position: relative;
    }
    @keyframes fadeInDown {
      from {opacity: 0; transform: translateY(-50px);}
      to {opacity: 1; transform: translateY(0);}
    }

    /* Toggle Button */
    #toggleBtn {
      position: absolute;
      top: 15px;
      right: 20px;
      padding: 8px 15px;
      background: #FFD700;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
    }

    /* Navigation */
    nav {
      display: flex;
      justify-content: center;
      background: rgba(0,86,179,0.9);
      padding: 15px;
      animation: fadeIn 2s ease;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    nav a {
      color: white;
      text-decoration: none;
      margin: 0 20px;
      font-weight: bold;
      font-size: 18px;
      transition: color 0.3s ease, transform 0.3s ease;
    }
    nav a:hover {
      color: #FFD700;
      transform: scale(1.2);
    }

    /* Sections with Parallax */
    section {
      padding: 80px 20px;
      text-align: center;
      animation: fadeInUp 1.5s ease;
      background-attachment: fixed;
      background-size: cover;
      background-position: center;
    }
    #home {background-image: url('https://picsum.photos/1600/900?random=1');}
    #about {background-image: url('https://picsum.photos/1600/900?random=2');}
    #pricing {background-image: url('https://picsum.photos/1600/900?random=3');}
    #contact {background-image: url('https://picsum.photos/1600/900?random=4');}

    @keyframes fadeInUp {
      from {opacity: 0; transform: translateY(50px);}
      to {opacity: 1; transform: translateY(0);}
    }

    /* Cards */
    .card {
      background: white;
      color: #333;
      margin: 20px auto;
      padding: 25px;
      border-radius: 15px;
      width: 320px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.4);
      transform: perspective(1000px) rotateY(5deg);
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }
    .card:hover {
      transform: perspective(1000px) rotateY(0deg) scale(1.08);
      box-shadow: 0 20px 40px rgba(0,123,255,0.8);
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 25px;
      background: rgba(0,123,255,0.85);
      animation: fadeIn 2s ease;
    }

    /* Links */
    a {
      color: #FFD700;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <h1>Vansh - Professional Web Designer</h1>
    <p>I design modern, responsive, and professional websites 🚀</p>
    <button id="toggleBtn">Toggle Dark/Light</button>
  </header>

  <!-- Navigation -->
  <nav>
    <a href="#" onclick="showPage('home')">Home</a>
    <a href="#" onclick="showPage('about')">About</a>
    <a href="#" onclick="showPage('pricing')">Pricing</a>
    <a href="#" onclick="showPage('contact')">Contact</a>
  </nav>

  <!-- Pages -->
  <section id="home">
    <h2>Welcome to My Portfolio</h2>
    <p>Hi, I’m Vansh 👋 — A professional website designer helping businesses build their online presence.</p>
  </section>

  <section id="about" class="hidden">
    <h2>About Me</h2>
    <p>I specialize in creating modern, responsive, and SEO-friendly websites. My goal is to deliver high-quality designs that help businesses grow online.</p>
  </section>

  <section id="pricing" class="hidden">
    <h2>🌐 Professional Website Development Services</h2>
    <div class="card">
      <h3>Basic Website (Starter)</h3>
      <p>₹5,000 – ₹10,000</p>
      <ul>
        <li>1–3 Pages</li>
        <li>Mobile Responsive</li>
        <li>Basic SEO</li>
      </ul>
    </div>
    <div class="card">
      <h3>Standard Website (Business)</h3>
      <p>₹12,000 – ₹25,000</p>
      <ul>
        <li>4–8 Pages</li>
        <li>Custom Design</li>
        <li>WhatsApp Integration</li>
      </ul>
    </div>
    <div class="card">
      <h3>Advanced Website (Professional)</h3>
      <p>₹30,000 – ₹70,000+</p>
      <ul>
        <li>8–15 Pages</li>
        <li>Custom UI/UX</li>
        <li>Admin Panel</li>
      </ul>
    </div>
    <div class="card">
      <h3>E-commerce Website</h3>
      <p>₹40,000 – ₹1,50,000+</p>
      <ul>
        <li>Product Listings</li>
        <li>Shopping Cart</li>
        <li>Payment Gateway</li>
      </ul>
    </div>
  </section>

  <section id="contact" class="hidden">
    <h2>📞 Contact Me</h2>
    <p>Phone: <a href="tel:+919456853697">+91 9456853697</a></p>
    <p>Email: <a href="mailto:anubhavv8777@gmail.com">anubhavv8777@gmail.com</a></p>
    <p>Instagram: <a href="https://www.instagram.com/vanshcodes.x/" target="_blank">vanshcodes.x</a></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2026 Vansh | All Rights Reserved</p>
  </footer>

  <script>
    function showPage(pageId) {
      document.querySelectorAll('section').forEach(sec => sec.classList.add('hidden'));
      document.getElementById(pageId).classList.remove('hidden');
    }

    // Dark/Light Mode Toggle
    document.getElementById('toggleBtn').addEventListener('click', () => {
      document.body.classList.toggle('dark');
    });
  </script>
