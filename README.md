<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>OzagaVenture</title>
  <meta name="description" content="OzagaVenture gadget store" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- External CSS file (optional) -->
  <!-- <link rel="stylesheet" href="style.css" /> -->

  <!-- Internal CSS -->
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f9f9f9;
      color: #333;
      line-height: 1.6;
      font-size: 16px;
      scroll-behavior: smooth;
    }

    a {
      color: #0d6efd;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    header, section, footer {
      padding: 20px;
      max-width: 1000px;
      margin: auto;
    }

    img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
    }

    .lightbox-img {
      cursor: pointer;
    }

    nav {
      background-color: #003566;
      padding: 10px;
      display: none;
    }

    nav a {
      color: #fff;
      margin-right: 10px;
    }

    #scrollToTop {
      display: none;
      position: fixed;
      bottom: 20px;
      right: 20px;
    }
  </style>
</head>
<body>

  <header>
    <h1>Best dealer in all kinds of gadgets</h1>
    <p>Shop with us and explore our collection of gadgets and home appliances.</p>
  </header>

  <figure>
    <img src="pexels-kaiya-inouye-559644190-32239167.jpg" alt="Store display" loading="lazy" />
    <figcaption>Ozaga <strong>sells</strong> gadgets</figcaption>
  </figure>

  <section>
    <h2>Top Laptops</h2>
    <ol>
      <li>HP EliteBook 830 8th Gen. Intel Core i5, 256GB SSD</li>
      <li>MacBook Pro 2020, Core i7, 16GB RAM, 512GB SSD</li>
      <li>MacBook Pro 2019, Core i7, 16GB RAM, 512GB SSD</li>
      <li>Dell Latitude E6440, Core i5-4310M, 8GB RAM, 320GB HDD</li>
      <li>HP EliteBook 840 G3, 8GB RAM, 256GB SSD</li>
      <li>HP EliteBook 1030 G3 360°, 16GB RAM, 512GB SSD</li>
    </ol>
  </section>

  <section>
    <h2>Visit Our Physical Store</h2>
    <p>Our first branch is located at No. 12 Indy Hall, University of Ibadan.</p>
    <figure>
      <img src="annie-spratt-xsOWB5IN8II-unsplash.jpg" alt="Gadget shop" loading="lazy" />
      <figcaption>Ozaga <strong>sells</strong> gadgets</figcaption>
    </figure>
    <ol>
      <li>iPhone 14 Pro Max, 128GB, Factory Unlocked, eSIM</li>
      <li>Samsung Galaxy A06, 50MP Camera, 5000mAh Battery</li>
      <li>iPhone 11 Pro Max, 256GB, Factory Unlocked</li>
      <li>iPhone 12 Pro Max, 128GB, Factory Unlocked</li>
    </ol>
  </section>

  <section>
    <h3>Why Choose Ozaga?</h3>
    <p>We offer top-quality gadgets at affordable prices. Many customers across Nigeria and on campus have praised our service, product quality, and reliability.</p>
    <figure>
      <img src="willi-nuchterlein-e-2NTM8fDKs-unsplash.jpg" alt="Laptops on display" />
      <figcaption>Ozaga <strong>sells</strong> gadgets</figcaption>
    </figure>
    <ol>
      <li>Dell Latitude 3380, Core i3, 4GB RAM, 128GB SSD</li>
      <li>HP EliteBook 840 G1, Core i5, 8GB RAM, 500GB HDD</li>
      <li>Dell Latitude 7400 360°, Core i7, 16GB RAM, 256GB SSD</li>
      <li>Lenovo Legion 5 Pro, i7-11800H, 32GB RAM, 2TB SSD</li>
    </ol>
  </section>

  <!-- YouTube Video -->
  <iframe width="100%" height="315" src="https://www.youtube.com/embed/yB9tCJFjiXM" frameborder="0" allowfullscreen loading="lazy"></iframe>

  <!-- iFrame to Website -->
  <div style="position:relative; padding-bottom: 56.25%; height:0; overflow:hidden;">
    <iframe src="https://ozagaventure.com" 
            style="position:absolute; top:0; left:0; width:100%; height:100%; border:none;" 
            allowfullscreen 
            loading="lazy"></iframe>
  </div>

  <!-- Menu Toggle -->
  <button id="menu-toggle">☰ Menu</button>
  <nav id="mobile-menu">
    <a href="#">Home</a>
    <a href="#">Products</a>
    <a href="#">Contact</a>
  </nav>

  <!-- Scroll to Top -->
  <button id="scrollToTop">↑</button>

  <!-- Lightbox Image -->
  <img src="your-product.jpg" class="lightbox-img" alt="Product preview" />

  <!-- JavaScript -->
  <script>
    document.getElementById('menu-toggle').addEventListener('click', () => {
      document.getElementById('mobile-menu').classList.toggle('hidden');
    });

    const scrollBtn = document.getElementById('scrollToTop');
    window.onscroll = () => {
      scrollBtn.style.display = window.scrollY > 300 ? 'block' : 'none';
    };
    scrollBtn.onclick = () => window.scrollTo({ top: 0, behavior: 'smooth' });

    document.querySelectorAll('.lightbox-img').forEach(img => {
      img.addEventListener('click', () => {
        const modal = document.createElement('div');
        modal.style.cssText = 'position:fixed;top:0;left:0;width:100%;height:100%;background:black;display:flex;justify-content:center;align-items:center;';
        modal.innerHTML = `<img src="${img.src}" style="max-width:90%;max-height:90%;cursor:pointer;" />`;
        modal.onclick = () => document.body.removeChild(modal);
        document.body.appendChild(modal);
      });
    });

    document.addEventListener("DOMContentLoaded", function () {
      document.getElementById("currentYear").textContent = new Date().getFullYear();
    });
  </script>

  <footer>
    <p>© <span id="currentYear"></span> Ozaga Venture. All rights reserved.</p>
    <p>All content on this website, including text, graphics, logos, images, videos, and other material, is the property of Ozaga Venture unless otherwise stated. Unauthorized use, reproduction, or distribution is prohibited without written permission.</p>
    <p>Contact us at: <a href="mailto:info@ozagaventure.com">info@ozagaventure.com</a></p>
  </footer>

</body>
</html>

