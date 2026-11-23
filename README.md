<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kaylee McMacken | Professional Cosmetologist</title>
  <!-- Modern Google Fonts -->
  <link rel="preconnect" href="https://googleapis.com">
  <link rel="preconnect" href="https://gstatic.com" crossorigin>
  <link href="https://googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Playfair+Display:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
  
  <style>
    /* Premium Design System Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background-image: url('./assets/images/background.jpg') !important;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      background-attachment: fixed;
      color: #2D2D2D; /* Elegant Charcoal */
      font-family: 'Inter', sans-serif;
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }

    /* Fixed Glassmorphism Header */
    .header-bar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background-color: rgba(253, 251, 252, 0.85); 
      backdrop-filter: blur(20px);               
      -webkit-backdrop-filter: blur(20px);
      padding: 18px 40px;
      border-bottom: 1px solid rgba(0, 0, 0, 0.05);
      display: flex;
      justify-content: space-between;            
      align-items: center;
      z-index: 1000;                             
    }

    .logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.35rem;
      font-weight: 600;
      color: #1A1A1A;
      letter-spacing: 0.5px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 28px;
    }

    .nav-links a {
      text-decoration: none;
      color: #555555;
      font-size: 0.9rem;
      font-weight: 500;
      letter-spacing: 0.5px;
      transition: color 0.3s ease;
    }

    .nav-links a:hover {
      color: #B57C7C; /* Elegant Rose Gold Accent */
    }

    /* Premium Book Now CTA Button */
    .nav-links a.book-btn {
      background-color: #2D2D2D;
      color: #FFFFFF;
      padding: 10px 22px;
      border-radius: 4px; /* Sophisticated slight round */
      font-size: 0.85rem;
      font-weight: 500;
      letter-spacing: 1px;
      text-transform: uppercase;
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
      transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
    }

    .nav-links a.book-btn:hover {
      background-color: #B57C7C;
      color: #FFFFFF;
      transform: translateY(-1px);
      box-shadow: 0 6px 20px rgba(181, 124, 124, 0.25);
    }

    /* Main Content Architecture with a slight overlay for text readability */
    .main-content {
      margin-top: 140px; 
      margin-bottom: 60px;
      padding: 40px;
      max-width: 1200px;
      margin-left: auto;
      margin-right: auto;
      background-color: rgba(253, 251, 252, 0.92); /* Protects readability over background image */
      border-radius: 12px;
      box-shadow: 0 20px 50px rgba(0,0,0,0.05);
	  background: #7BA4C7;
    }

    /* Hero Text Formatting */
    .intro-section {
      text-align: center;
      margin-bottom: 60px;
      max-width: 700px;
      margin-left: auto;
      margin-right: auto;
    }

    .intro-section h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.5rem;
      font-weight: 400;
      color: #1A1A1A;
      margin-bottom: 16px;
    }

    .intro-text {
      font-size: 1.1rem;
      color: #2D3136;
      font-weight: 300;
    }

    /* Modern 2-Column Grid for Videos */
    .video-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 32px;
    }

    /* Individual Video Cards */
    .video-card {
      background: #FFFFFF;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.03);
      border: 1px solid rgba(0, 0, 0, 0.04);
      transition: transform 0.4s cubic-bezier(0.165, 0.84, 0.44, 1), box-shadow 0.4s ease;
    }

    .video-card video {
      display: block;
      width: 100%;
      height: auto;
      aspect-ratio: 16 / 9;
      object-fit: cover;
      background-color: #000000;
      outline: none;
    }

    .video-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
    }

    /* Responsiveness Optimizations */
    @media (max-width: 900px) {
      .video-grid {
        grid-template-columns: 1fr; /* Stack layout seamlessly on smaller devices */
        gap: 24px;
      }
    }

    @media (max-width: 768px) {
      body {
        background-attachment: scroll; /* Fixes potential performance lag on mobile browsers */
      }

      .header-bar {
        padding: 15px 20px;
        flex-direction: column;
        gap: 16px;
        text-align: center;
      }
      
      .nav-links {
        gap: 16px;
        flex-wrap: wrap;       
        justify-content: center;
      }

      .nav-links a {
        font-size: 0.85rem;    
      }

      .main-content {
        margin-top: 180px;    
        padding: 24px 16px;
      }

      .intro-section h1 {
        font-size: 2rem;
      }

      .video-card:hover {
        transform: none; /* Disables hover translation effects on touch devices */
      }
    }
  </style>
</head>
<body>

  <!-- Premium Header Bar Navigation -->
  <header class="header-bar">
    <div class="logo">Kaylee Cosmetology</div>
    <nav class="nav-links">
      <a href="#about">About</a>
      <a href="#gallery">Gallery</a>
      <a href="#videos">Videos</a>
      <a href="#contact">Contact</a>
      <a href="https://tspacoloradosprings.com" class="book-btn">Book Now</a>
    </nav>
  </header>

  <!-- Principal Structural Page Content -->
  <main class="main-content">
    
    <div class="intro-section">
      <h1>Portfolio</h1>
      <p class="intro-text">Full-service cosmetologist. Explore my portfolio and book your appointment today:)</p>
    </div>

    <!-- Symmetrical Professional Media Portfolio Layout -->
    <div class="video-grid" id="videos">
      <div class="video-card">
        <video controls>
          <source src="./assets/videos/vid1.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </div>

      <div class="video-card">
        <video controls>
          <source src="./assets/videos/vid2.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </div>

      <div class="video-card">
        <video controls>
          <source src="./assets/videos/vid3.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </div>

      <div class="video-card">
        <video controls>
          <source src="./assets/videos/vid4.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </div>
    </div>

  </main>

</body>
</html>
