<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Nehra Webs</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #f4f0ec;
      color: #222;
      line-height: 1.6;
    }

    header {
      text-align: center;
      padding: 40px 20px;
      background: #fff;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    }

    .logo {
      height: 120px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    h1 {
      font-family: 'Playfair Display', serif;
      font-size: 36px;
      margin-top: 20px;
    }

    .contact-buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin: 40px 0;
      flex-wrap: wrap;
    }

    .contact-buttons a {
      padding: 14px 32px;
      border-radius: 32px;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.3s ease;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    }

    .contact-buttons a:first-child {
      background: linear-gradient(135deg, #833ab4, #fd1d1d, #fcb045);
      color: white;
    }

    .contact-buttons a:last-child {
      background: #25D366;
      color: white;
    }

    .contact-buttons a:hover {
      transform: scale(1.05);
    }

    .posts-section {
      padding: 40px 20px;
      background: #fff;
      border-radius: 16px;
      max-width: 800px;
      margin: 0 auto 40px;
      box-shadow: 0 6px 18px rgba(0,0,0,0.06);
    }

    .posts-section h2 {
      font-family: 'Playfair Display', serif;
      font-size: 28px;
      margin-bottom: 20px;
    }

    .post {
      background: #fefefe;
      padding: 20px;
      margin-bottom: 16px;
      border-left: 4px solid #6e3b2e;
      border-radius: 8px;
    }

    footer {
      text-align: center;
      background-color: #1a1a1a;
      color: #ccc;
      padding: 30px 20px;
      font-family: 'Playfair Display', serif;
    }

    footer strong {
      color: #fff;
    }
  </style>
</head>
<body>

  <header>
    <!-- Make sure this image exists in your GitHub repo -->
    <img src="nehra-logo.png" alt="Nehra Webs Logo" class="logo">
    <h1>Nehra Webs</h1>
  </header>

  <div class="contact-buttons">
    <a href="https://www.instagram.com/rajpalnehra001" target="_blank">Instagram</a>
    <a href="https://wa.me/917851867154?text=I%20need%20a%20website" target="_blank">WhatsApp</a>
  </div>

  <section class="posts-section">
    <h2>My Posts</h2>
    <!-- Add your posts/updates here -->
    <div class="post">🎧 New ringtone released this week — check my Instagram!</div>
    <div class="post">🚀 Working on a new Android app, launching soon...</div>
    <div class="post">🔥 Realme UI 6.0 gaming review coming next Friday!</div>
  </section>

  <footer>
    &copy; 2025 <strong>Nehra Webs</strong>. Crafted with passion and coffee ☕<br>
    Owner: <strong>Rajpal Nehra</strong>
  </footer>

</body>
</html>
