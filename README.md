# Interactive-navigation-menu
navigation menu that changes the color or style while scrolling or exploring the website.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Creative Digital Solutions</title>
  
  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet">
  
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.8;
      color: #444;
    }

    /* Navbar styling */
    nav.navbar {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      transition: background-color 0.3s ease;
      background-color: transparent;
    }

    nav.navbar ul li a {
      color: #fff;
      transition: background-color 0.3s, color 0.3s;
    }

    nav.navbar ul li a:hover {
      background-color: #FF6347; /* Tomato color */
      color: #fff;
      border-radius: 5px;
    }

    nav.scrolled {
      background-color: #222 !important;
    }

    /* Section styling */
    section {
      height: 100vh;
      padding: 100px 20px; /* Adjust for fixed navbar */
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: #fff;
      transition: background-color 1s ease;
    }

    /* Section-specific colors */
    #home {
      background-color: #1abc9c; /* Turquoise */
    }

    #about {
      background-color: #f39c12; /* Orange */
    }

    #services {
      background-color: #9b59b6; /* Purple */
    }

    #contact {
      background-color: #e74c3c; /* Red */
    }

    /* Headings and paragraphs */
    h1, h2 {
      font-weight: bold;
      margin-bottom: 20px;
    }

    p {
      font-size: 18px;
      margin-bottom: 30px;
    }

    .btn-primary {
      background-color: #e67e22;
      border-color: #e67e22;
    }

    .btn-primary:hover {
      background-color: #d35400;
      border-color: #d35400;
    }

    /* Service section icons */
    .service-icon {
      font-size: 50px;
      color: #fff;
      margin-bottom: 20px;
      transition: transform 0.3s ease;
    }

    .service-icon:hover {
      transform: scale(1.2);
    }

    /* Email Subscription Styling */
    .subscribe-box {
      margin-top: 50px;
      background-color: #f39c12;
      padding: 30px;
      border-radius: 10px;
    }

    .subscribe-box input[type="email"] {
      width: 80%;
      padding: 10px;
      border-radius: 5px;
      border: none;
      margin-right: 10px;
    }

    .subscribe-box button {
      background-color: #2980b9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease, box-shadow 0.3s ease;
    }

    .subscribe-box button.glow {
      background-color: #27ae60 !important;
      box-shadow: 0 0 15px #27ae60;
    }

    .subscribe-box button:hover {
      background-color: #1a6fa8;
    }

    /* Success Message Styling */
    .subscribe-success {
      display: none;
      margin-top: 20px;
      font-size: 18px;
      color: #fff;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark" id="navbar">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Creative Solutions</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
          <li class="nav-item"><a class="nav-link" href="#services">Services</a></li>
          <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Home Section -->
  <section id="home">
    <div class="container text-center">
      <h1>Welcome to Creative Digital Solutions</h1>
      <p class="lead">Unleashing the power of innovation to craft digital experiences that resonate, captivate, and inspire.</p>
      <a href="#about" class="btn btn-primary">Discover More</a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about">
    <div class="container">
      <h2>Our Mission</h2>
      <p>At Creative Digital Solutions, our mission is to empower businesses and individuals through innovative digital strategies. We strive to blend creativity with technology, providing tailored solutions that enhance user experiences and drive success. Our dedicated team believes in the power of collaboration and is committed to turning your vision into a reality. Together, let's embark on a journey of digital transformation, where your goals inspire our creativity!</p>
      <a href="#services" class="btn btn-primary">Discover Our Approach</a>
    </div>
  </section>
  

  <!-- Services Section -->
  <section id="services">
    <div class="container">
      <h2>Our Expertise</h2>
      <div class="row mt-4">
        <div class="col-md-4">
          <i class="fas fa-laptop-code service-icon"></i>
          <h4>Custom Web Design</h4>
          <p>Our talented designers create stunning websites that are not only aesthetically pleasing but also user-friendly and responsive across all devices.</p>
        </div>
        <div class="col-md-4">
          <i class="fas fa-mobile-alt service-icon"></i>
          <h4>Mobile Application Development</h4>
          <p>We develop intuitive mobile apps that offer seamless user experiences, bringing engagement to your customers’ fingertips wherever they are.</p>
        </div>
        <div class="col-md-4">
          <i class="fas fa-chart-line service-icon"></i>
          <h4>SEO & Digital Marketing</h4>
          <p>Our expert team ensures that your online presence thrives through powerful SEO strategies, increasing conversions, traffic, and brand awareness.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <div class="container text-center">
      <h2>Get in Touch</h2>
      <p>Have an idea, a project, or a question? We’re here to help! Send us a message, and let’s create something extraordinary together.</p>
      
      <!-- Contact Form -->
      <form action="submit.php" method="POST" class="mt-4">
        <div class="mb-3">
          <label for="name" class="form-label">Name</label>
          <input type="text" class="form-control" id="name" name="name" required>
        </div>
        <div class="mb-3">
          <label for="email" class="form-label">Email address</label>
          <input type="email" class="form-control" id="email" name="email" required>
        </div>
        <div class="mb-3">
          <label for="message" class="form-label">Message</label>
          <textarea class="form-control" id="message" name="message" rows="3" required></textarea>
        </div>
        <button type="submit" class="btn btn-primary">Send Message</button>
      </form>

      <!-- Email Subscription Box -->
      <div class="subscribe-box mt-5">
        <h3>Stay in the Loop!</h3>
        <p>Subscribe to our newsletter to receive the latest updates, offers, and insights straight to your inbox.</p>
        <form id="subscribe-form">
          <input type="email" id="subscribe-email" placeholder="Enter your email address" required>
          <button type="submit">Subscribe</button>
        </form>
        <div class="subscribe-success" id="subscribe-success">Thank you for
