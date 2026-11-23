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

    .nav-links button, .nav-links a {
      background: none;
      border: none;
      text-decoration: none;
      color: #555555;
      font-family: 'Inter', sans-serif;
      font-size: 0.9rem;
      font-weight: 500;
      letter-spacing: 0.5px;
      transition: color 0.3s ease;
      cursor: pointer;
    }

    .nav-links button:hover, .nav-links button.active {
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

    /* Modern 2-Column Grid for Videos and Images */
    .video-grid, .gallery-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 32px;
    }

    /* Individual Cards */
    .video-card, .gallery-card {
      background: #FFFFFF;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.03);
      border: 1px solid rgba(0, 0, 0, 0.04);
      transition: transform 0.4s cubic-bezier(0.165, 0.84, 0.44, 1), box-shadow 0.4s ease;
    }

    .video-card video, .gallery-card img {
      display: block;
      width: 100%;
      height: auto;
      aspect-ratio: 16 / 9;
      object-fit: cover;
      outline: none;
    }

    .video-card video {
      background-color: #000000;
    }

    .video-card:hover, .gallery-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
    }

    /* Form Design */
    .contact-form {
      max-width: 600px;
      margin: 0 auto;
      background: #FFFFFF;
      padding: 30px;
      border-radius: 8px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.03);
    }

    .form-group {
      margin-bottom: 20px;
    }

    .form-group label {
      display: block;
      font-size: 0.9rem;
      font-weight: 500;
      margin-bottom: 6px;
      color: #1A1A1A;
    }

    .form-group input, .form-group textarea {
      width: 100%;
      padding: 12px;
      border: 1px solid #DDDDDD;
      border-radius: 4px;
      font-family: 'Inter', sans-serif;
      font-size: 0.95rem;
    }

    .form-group textarea {
      resize: vertical;
      min-height: 120px;
    }

    .submit-btn {
      background-color: #2D2D2D;
      color: #FFFFFF;
      padding: 12px 24px;
      border: none;
      border-radius: 4px;
      font-size: 0.9rem;
      font-weight: 500;
      cursor: pointer;
      width: 100%;
      transition: background-color 0.3s;
    }

    .submit-btn:hover {
      background-color: #B57C7C;
    }

    /* Content Switching Utility Classes */
    .portfolio-section {
      display: none;
    }
    
    .portfolio-section.active {
      display: block;
    }

    /* Responsiveness Optimizations */
    @media (max-width: 900px) {
      .video-grid, .gallery-grid {
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

      .nav-links button, .nav-links a {
        font-size: 0.85rem;    
      }

      .main-content {
        margin-top: 180px;    
        padding: 24px 16px;
      }

      .intro-section h1 {
        font-size: 2rem;
      }

      .video-card:hover, .gallery-card:hover {
        transform: none; /* Disables hover translation effects on touch devices */
      }
    }
  </style>
</head>
<body>

  <!-- Premium Header Bar Navigation -->
  <header class="header-bar">
    <div class="logo">@kayleescosmicbliss</div>
    <nav class="nav-links" id="navLinks">
      <button id="btn-about" onclick="showSection('about')">About</button>
      <button id="btn-gallery" onclick="showSection('gallery')">Gallery</button>
      <button id="btn-videos" onclick="showSection('videos')">Videos</button>
      <button id="btn-contact" onclick="showSection('contact')">Contact</button>
      <a href="tel:7192669400" class="book-btn">Book Now</a>
    </nav>
  </header>

  <!-- Principal Structural Page Content -->
  <main class="main-content">
    
    <div class="intro-section">
      <h1 id="sectionTitle">Portfolio</h1>
      <p class="intro-text" id="sectionDesc">Full-service cosmetologist. Explore my portfolio and book your appointment today :)</p>
    </div>

    <!-- About Section -->
    <section id="about" class="portfolio-section">
      <div style="background: #FFFFFF; padding: 40px; border-radius: 8px; max-width: 800px; margin: 0 auto;">
        <h2 style="font-family: 'Playfair Display', serif; margin-bottom: 20px;">Hi, I'm Kaylee McMacken</h2>
        <p style="margin-bottom: 15px;">Welcome to my cosmic oasis! As a  cosmetology student, I specialize in transforming hair - particularly curly hair, skin, and nails to help my clients look and feel their absolute best.</p>
      </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="portfolio-section">
      <div class="gallery-grid">
        <div class="gallery-card">
          <img src="./assets/images/nail1.jpeg" alt="Cosmetology Work 1" onerror="this.style.background='#eee'; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'100\' height=\'50\'><text x=\'10\' y=\'30\'>Gallery Image 1</text></svg>'">
        </div>
        <div class="gallery-card">
          <img src="./assets/images/nail2.jpeg" alt="Cosmetology Work 2" onerror="this.style.background='#eee'; this.src='data:image/svg+xml;utf8,<svg xmlns=\'http://www.w3.org/2000/svg\' width=\'100\' height=\'50\'><text x=\'10\' y=\'30\'>Gallery Image 2</text></svg>'">
        </div>
        <div class="gallery-card">
          <img src="./assets/images/nail3.jpeg" alt="Cosmetology Work 3" onerror="this.style.background='#eee'; this.src='data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='100' height='50'><text x='10' y='30'><text x=\'10\' y=\'30\'>Gallery Image 3</text></svg>'">
        </div>
        <div class="gallery-card">
          <img src="./assets/images/facial.jpeg" alt="Cosmetology Work 4" onerror="this.style.background='#eee'; this.src='data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='100' height='50'><text x='10' y='30'><text x=\'10\' y=\'30\'>Gallery Image 4</text></svg>'">
        </div>
      </div>
    </section>
	
    <!-- Videos Section -->
    <section id="videos" class="portfolio-section">
		<div class="video-grid">
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
	</section>

    <!-- Contact Section -->
    <section id="contact" class="portfolio-section">
      <form class="contact-form" onsubmit="event.preventDefault(); alert('Message sent successfully!');">
        <div class="form-group">
          <label for="name">Your Name</label>
          <input type="text" id="name" required placeholder="Enter your full name">
        </div>
        <div class="form-group">
          <label for="email">Email Address</label>
          <input type="email" id="email" required placeholder="kayleemcmacken2003@gmail.com">
        </div>
        <div class="form-group">
          <label for="message">Your Message</label>
          <textarea id="message" required placeholder="Tell me about the services you're interested in..."></textarea>
        </div>
        <button type="submit" class="submit-btn">Send Message</button>
      </form>
    </section>

  </main>

  <script>
    const contentData = {
      'about': { title: 'About Me', desc: 'Cosmetology Student at The Salon Professional Academy' },
      'gallery': { title: 'Transformation Highlights', desc: '' },
      'videos': { title: 'Transformation and Relaxation', desc: '' },
      'contact': { title: 'Get In Touch', desc: 'Have questions or ready to update your look? Drop a message here.' }
    };

    function showSection(sectionId) {
      // Hide all content containers
      document.querySelectorAll('.portfolio-section').forEach(section => {
        section.classList.remove('active');
      });
      
      // Reveal targeted section container explicitly
      const activeSection = document.getElementById(sectionId);
      if (activeSection) {
        activeSection.classList.add('active');
      }

      // Update header details cleanly
      if (contentData[sectionId]) {
        document.getElementById('sectionTitle').innerText = contentData[sectionId].title;
        document.getElementById('sectionDesc').innerText = contentData[sectionId].desc;
      }

      // Update button active styling highlights
      document.querySelectorAll('.nav-links button').forEach(btn => {
        btn.classList.remove('active');
      });
      const activeBtn = document.getElementById('btn-' + sectionId);
      if (activeBtn) {
        activeBtn.classList.add('active');
      }
      
      // Reset view smooth positioning
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // Default initializer step: sets page to land on a general welcome view where sections are hidden until a button is clicked.
    // To land on a specific section right away, change 'about' below to 'videos', 'gallery', etc.
    window.addEventListener('DOMContentLoaded', () => {
      showSection('about');
    });
  </script>

</body>
</html>
