<style>
  /* Reset margins for a clean layout */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    background-image: url('./assets/images/background.jpg') !important;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  /* Fixed Header Bar at the top of the screen */
  .header-bar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: rgba(255, 255, 255, 0.9); /* Semi-transparent white background */
    backdrop-filter: blur(10px);               /* Modern blurred glass effect */
    padding: 15px 30px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);    /* Subtle shadow under the bar */
    display: flex;
    justify-content: space-between;            /* Puts logo left, links right */
    align-items: center;
    z-index: 1000;                             /* Keeps the header on top of videos */
  }

  .logo {
    font-size: 1.4rem;
    font-weight: bold;
    color: #333;
    letter-spacing: 1px;
  }

  .nav-links {
    display: flex;
    align-items: center;
  }

  .nav-links a {
    text-decoration: none;
    color: #555;
    margin-left: 20px;
    font-weight: 500;
    transition: color 0.3s;
  }

  .nav-links a:hover {
    color: #ff6b81; /* Soft pink accent color on hover */
  }

  /* Special CTA style button for "Book" */
  .nav-links a.book-btn {
    background-color: #ff6b81;
    color: white;
    padding: 8px 16px;
    border-radius: 20px;
    transition: background-color 0.3s, transform 0.2s;
  }

  .nav-links a.book-btn:hover {
    background-color: #ff4757;
    transform: scale(1.05);
  }

  /* Main content wrapper to push everything down below the fixed header */
  .main-content {
    margin-top: 100px; 
    padding: 20px;
  }

  .intro-text {
    text-align: center;
    font-size: 1.2rem;
    font-weight: bold;
    color: #222;
    margin-bottom: 40px;
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
    background-color: rgba(255, 255, 255, 0.7); /* Readable background overlay */
    padding: 15px;
    border-radius: 8px;
  }

  /* Flexbox container to center all videos inside it */
  .video-container {
    display: flex;
    flex-direction: column; 
    align-items: center;    
    gap: 40px;              /* Increased gap for a cleaner layout */
    padding-bottom: 60px;
  }

  /* Modernized individual video frames */
  .video-container video {
    display: block;
    max-width: 100%;                          
    border-radius: 16px;                      /* Rounder, friendlier modern corners */
    background-color: #111;                   /* Richer deep dark fallback background */
    outline: none;
    
    /* Premium frosted glass-like border stroke */
    border: 1px solid rgba(255, 255, 255, 0.4); 
    
    /* Dual layer drop shadow: 1 soft ambient glow + 1 sleek dark positioning shadow */
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15), 0 0 25px rgba(255, 107, 129, 0.05); 
    
    /* Fluid timing curve for modern smooth movement transitions */
    transition: transform 0.4s cubic-bezier(0.165, 0.84, 0.44, 1), box-shadow 0.4s ease;
  }

  /* Interactive hover micro-effects */
  .video-container video:hover {
    transform: translateY(-6px) scale(1.015); /* Elegantly lifts up and micro-zooms on pointer hover */
    box-shadow: 0 30px 50px rgba(0, 0, 0, 0.25), 0 0 35px rgba(255, 107, 129, 0.15); /* Glow intensifies */
  }

  /* Custom classes for desktop sizes */
  .vid-large { width: 55%; }
  .vid-small { width: 35%; }

  /* Mobile Responsive Optimizations */
  @media (max-width: 768px) {
    .header-bar {
      padding: 15px 10px;
      flex-direction: column;
      gap: 12px;
      text-align: center;
    }
    
    .nav-links {
      width: 100%;
      justify-content: center;
      flex-wrap: wrap;       
      gap: 10px;
    }

    .nav-links a {
      margin-left: 0;       
      font-size: 0.9rem;    
    }

    .main-content {
      margin-top: 160px;    
    }

    /* Force all videos to take up optimal mobile viewing width */
    .video-container video.vid-large,
    .video-container video.vid-small {
      width: 92%;
    }

    /* Tones down hover lift movement on touch screens */
    .video-container video:hover {
      transform: none;
    }
  }
</style>

<body>

  <!-- Header Bar Element with updated menu buttons -->
  <header class="header-bar">
    <div class="logo">Kaylee McMacken - Cosmetologist</div>
    <nav class="nav-links">
      <a href="#about">About</a>
      <a href="#gallery">Gallery</a>
      <a href="#videos">Videos</a>
      <a href="#contact">Contact</a>
      <a href="https://tspacoloradosprings.com" class="book-btn">Book Now</a>
    </nav>
  </header>

  <!-- Pushes content down so the fixed header doesn't block it -->
  <main class="main-content">
    
    <p class="intro-text">I am a full service cosmotologist- check out my portfolio below and book today!</p>

    <!-- Center-aligned videos with mobile responsive classes -->
    <div class="video-container" id="videos">
      <video class="vid-large" controls>
        <source src="./assets/videos/vid1.mp4" type="video/mp4">
        Your browser does not support the video tag
      </video>

      <video class="vid-large" controls>
        <source src="./assets/videos/vid2.mp4" type="video/mp4">
        Your browser does not support the video tag
      </video>

      <video class="vid-small" controls>
        <source src="./assets/videos/vid3.mp4" type="video/mp4">
        Your browser does not support the video tag
      </video>

      <video class="vid-small" controls>
        <source src="./assets/videos/vid4.mp4" type="video/mp4">
        Your browser does not support the video tag
      </video>
    </div>

  </main>

</body>
