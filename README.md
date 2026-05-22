
                 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- SEO -->
  <title>Modern Responsive Website</title>
  <meta name="description" content="Professional modern responsive website with animations and SEO optimization." />
  <meta name="keywords" content="web design, responsive website, modern UI UX, SEO website" />
  <meta name="author" content="Your Name" />

  <!-- Open Graph -->
  <meta property="og:title" content="Modern Responsive Website" />
  <meta property="og:description" content="Professional UI/UX responsive website." />
  <meta property="og:type" content="website" />

  <!-- Google Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      scroll-behavior:smooth;
    }

    body{
      font-family: Arial, sans-serif;
      background:#0f172a;
      color:white;
      line-height:1.6;
      overflow-x:hidden;
    }

    a{
      text-decoration:none;
      color:white;
    }

    img{
      max-width:100%;
    }

    .container{
      width:90%;
      max-width:1200px;
      margin:auto;
    }

    /* NAVBAR */
    nav{
      position:fixed;
      width:100%;
      top:0;
      left:0;
      background:rgba(15,23,42,0.9);
      backdrop-filter:blur(10px);
      z-index:1000;
    }

    .nav-container{
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:18px 0;
    }

    .logo{
      font-size:1.5rem;
      font-weight:bold;
      color:#38bdf8;
    }

    .nav-links{
      display:flex;
      gap:25px;
    }

    .nav-links a{
      transition:0.3s;
    }

    .nav-links a:hover{
      color:#38bdf8;
    }

    .menu-toggle{
      display:none;
      font-size:2rem;
      cursor:pointer;
    }

    /* HERO */
    .hero{
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      padding:100px 20px;
      background:
      linear-gradient(rgba(15,23,42,.7), rgba(15,23,42,.9)),
      url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1400') center/cover;
    }

    .hero-content{
      animation:fadeUp 1s ease;
    }

    .hero h1{
      font-size:4rem;
      margin-bottom:20px;
    }

    .hero p{
      max-width:700px;
      margin:auto;
      margin-bottom:30px;
      color:#cbd5e1;
    }

    .btn{
      display:inline-block;
      background:#38bdf8;
      color:#0f172a;
      padding:14px 28px;
      border-radius:50px;
      font-weight:bold;
      transition:0.3s;
    }

    .btn:hover{
      transform:translateY(-3px);
      background:#0ea5e9;
    }

    /* SECTION */
    section{
      padding:100px 0;
    }

    .section-title{
      text-align:center;
      margin-bottom:60px;
      font-size:2.5rem;
    }

    /* SERVICES */
    .services{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:30px;
    }

    .card{
      background:#1e293b;
      padding:30px;
      border-radius:20px;
      transition:0.4s;
      border:1px solid transparent;
    }

    .card:hover{
      transform:translateY(-10px);
      border-color:#38bdf8;
    }

    .card h3{
      margin-bottom:15px;
      color:#38bdf8;
    }

    /* ABOUT */
    .about{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:50px;
      align-items:center;
    }

    .about img{
      border-radius:20px;
    }

    /* CONTACT */
    form{
      max-width:700px;
      margin:auto;
      display:flex;
      flex-direction:column;
      gap:20px;
    }

    input, textarea{
      padding:16px;
      border:none;
      border-radius:10px;
      background:#1e293b;
      color:white;
    }

    textarea{
      resize:none;
      height:150px;
    }

    button{
      border:none;
      cursor:pointer;
    }

    /* FOOTER */
    footer{
      text-align:center;
      padding:30px 20px;
      background:#020617;
      color:#94a3b8;
    }

    /* ANIMATIONS */
    @keyframes fadeUp{
      from{
        opacity:0;
        transform:translateY(50px);
      }
      to{
        opacity:1;
        transform:translateY(0);
      }
    }

    /* RESPONSIVE */
    @media(max-width:768px){

      .hero h1{
        font-size:2.5rem;
      }

      .about{
        grid-template-columns:1fr;
      }

      .nav-links{
        position:absolute;
        top:70px;
        right:-100%;
        flex-direction:column;
        background:#0f172a;
        width:220px;
        padding:20px;
        transition:0.4s;
      }

      .nav-links.active{
        right:20px;
      }

      .menu-toggle{
        display:block;
      }
    }
  </style>
</head>
<body>

  <!-- NAVBAR -->
  <nav>
    <div class="container nav-container">
      <div class="logo">Brand.</div>

      <div class="nav-links" id="navLinks">
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </div>

      <div class="menu-toggle" id="menuToggle">
        ☰
      </div>
    </div>
  </nav>

  <!-- HERO -->
  <section class="hero" id="home">
    <div class="hero-content">
      <h1>Build Stunning Digital Experiences</h1>
      <p>
        Modern responsive website with fast performance,
        SEO optimization, smooth animations, and professional UI/UX.
      </p>
      <a href="#contact" class="btn">Get Started</a>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services">
    <div class="container">
      <h2 class="section-title">Our Services</h2>

      <div class="services">

        <div class="card">
          <h3>Web Design</h3>
          <p>
            Beautiful modern interfaces designed for performance and conversions.
          </p>
        </div>

        <div class="card">
          <h3>Development</h3>
          <p>
            Fast and scalable websites optimized for all devices.
          </p>
        </div>

        <div class="card">
          <h3>SEO Optimization</h3>
          <p>
            Improve rankings and visibility with technical SEO best practices.
          </p>
        </div>

      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="container about">

      <div>
        <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?q=80&w=1200" alt="Team">
      </div>

      <div>
        <h2 class="section-title">About Us</h2>

        <p>
          We create premium digital products with clean code,
          smooth user experiences, and high-speed performance.
        </p>

        <br>

        <p>
          Our mission is to help businesses grow online through
          modern web technologies and strategic design.
        </p>
      </div>

    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="container">

      <h2 class="section-title">Contact Us</h2>

      <form>
        <input type="text" placeholder="Your Name" required>

        <input type="email" placeholder="Your Email" required>

        <textarea placeholder="Your Message"></textarea>

        <button class="btn">Send Message</button>
      </form>

    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>© 2026 Modern Website. All Rights Reserved.</p>
  </footer>

  <script>
    const menuToggle = document.getElementById("menuToggle");
    const navLinks = document.getElementById("navLinks");

    menuToggle.addEventListener("click", () => {
      navLinks.classList.toggle("active");
    });

    // Smooth reveal animation
    const cards = document.querySelectorAll('.card');

    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.style.opacity = "1";
          entry.target.style.transform = "translateY(0)";
        }
      });
    });

    cards.forEach(card => {
      card.style.opacity = "0";
      card.style.transform = "translateY(40px)";
      card.style.transition = "0.6s ease";
      observer.observe(card);
    });
  </script>

</body>
</html>
             
