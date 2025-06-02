<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nehra Webs | Premium Site Builder</title>
  <style>
    :root {
      --cream: #fef8f3;
      --coffee: #a67b5b;
      --brown: #7c5c45;
      --text-dark: #3e2e1f;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      scroll-behavior: smooth;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--cream);
      color: var(--text-dark);
    }

    .hero {
      height: 100vh;
      position: relative;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 20px;
    }

    video.background-video {
      position: absolute;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      z-index: -1;
      opacity: 0.15;
    }

    .logo { 
      width: 120px;
      margin-bottom: 20px;
      border-radius: 12px;
    }

    .namaste {
      font-size: 3rem;
      font-weight: bold;
      color: var(--brown);
      margin-bottom: 20px;
      animation: fadeIn 2s ease;
    }

    .question {
      font-size: 1.5rem;
      margin-bottom: 30px;
      color: var(--text-dark);
    }

    .yes-button {
      padding: 14px 35px;
      font-size: 1.1rem;
      font-weight: 600;
      border: none;
      border-radius: 30px;
      background: var(--coffee);
      color: #fff;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    .yes-button:hover {
      background: var(--brown);
      transform: translateY(-2px);
    }

    .section {
      padding: 60px 20px;
      background-color: #fff9f2;
      text-align: center;
    }

    .section h2 {
      color: var(--brown);
      font-size: 2rem;
      margin-bottom: 20px;
    }

    .contact-buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 25px;
    }

    .contact-buttons a {
      text-decoration: none;
      padding: 12px 24px;
      background-color: var(--coffee);
      color: white;
      border-radius: 25px;
      font-weight: bold;
      transition: background 0.3s;
    }

    .contact-buttons a:hover {
      background-color: var(--brown);
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    footer {
      background: var(--brown);
      color: #fff;
      text-align: center;
      padding: 20px 10px;
    }
  </style>
</head>
<body>

  <section class="hero">
    <video class="background-video" autoplay loop muted>
      <source src="namaste.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>

    <img src="new_logo.png" alt="Nehra Webs Logo" class="logo" />
    <div class="namaste">🙏 Namaste</div>
    <div class="question">Do you want to get a website built?</div>
    <button class="yes-button" onclick="scrollToContact()">Yes</button>
  </section>

  <section class="section" id="contact">
    <h2>Let's Get You Online!</h2>
    <p>Click below to connect with us on your favorite platform:</p>

    <div class="contact-buttons">
      <a href="https://www.instagram.com/rajpalnehra001" target="_blank">Instagram</a>
      <a href="https://wa.me/917851867154 text=I%20need%20a%20website" target="_blank">WhatsApp</a>
    </div>
  </section>

  <footer>
    &copy; 2025 Nehra Webs. Crafted with passion and coffee ☕
  </footer>

  <script>
    function scrollToContact() {
      document.getElementById("contact").scrollIntoView({ behavior: "smooth" });
    }
  </script>

</body>
</html>
