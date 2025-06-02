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
      background-color: #f8f5f2;
      color: #333;
    }

    header {
      background-color: #fff;
      padding: 40px 20px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .logo {
      height: 100px;
      width: auto;
      border-radius: 8px;
    }

    section {
      padding: 60px 20px;
      text-align: center;
    }

    .contact-buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }

    .contact-buttons a {
      padding: 14px 30px;
      border-radius: 30px;
      font-weight: 600;
      font-size: 16px;
      text-decoration: none;
      transition: all 0.3s ease;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
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
      transform: translateY(-3px);
      box-shadow: 0 12px 20px rgba(0, 0, 0, 0.15);
    }

    footer {
      background-color: #1f1f1f;
      color: #ccc;
      text-align: center;
      padding: 40px 20px;
      font-size: 15px;
      font-family: 'Playfair Display', serif;
    }

    footer strong {
      color: #fff;
    }
  </style>
</head>
<body>

<header>
  <img src="nehra-logo.jpg" alt="Nehra Webs Logo" class="logo">
</header>

<section id="contact">
  <h2 style="font-family:'Playfair Display', serif; font-size: 32px; margin-bottom: 30px;">Connect with Me</h2>
  <div class="contact-buttons">
    <a href="https://www.instagram.com/rajpalnehra001" target="_blank">Instagram</a>
    <a href="https://wa.me/917851867154?text=I%20need%20a%20website" target="_blank">WhatsApp</a>
  </div>
</section>

<footer>
  &copy; 2025 <strong>Nehra Webs</strong>. Crafted with passion and coffee ☕<br>
  Owner: <strong>Rajpal Nehra</strong>
</footer>

</body>
</html>
