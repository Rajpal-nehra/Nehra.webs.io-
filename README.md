<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Nehra Webs</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
    }

    header {
      background-color: #f9f9f9;
      padding: 20px;
    }

    .logo {
      height: 120px;
      width: auto;
    }

    .contact-buttons {
      margin: 30px 0;
    }

    .contact-buttons a {
      text-decoration: none;
      color: white;
      background-color: #25D366; /* WhatsApp green */
      padding: 12px 24px;
      margin: 10px;
      border-radius: 8px;
      display: inline-block;
      font-weight: bold;
    }

    .contact-buttons a:first-child {
      background-color: #E1306C; /* Instagram pink */
    }

    footer {
      background-color: #222;
      color: #fff;
      padding: 20px;
      font-size: 14px;
    }
  </style>
</head>
<body>

<header>
  <!-- Update the file name if different -->
  <img src="nehra-logo.jpg" alt="Nehra Webs Logo" class="logo">
</header>

<section id="contact">
  <div class="contact-buttons">
    <a href="https://www.instagram.com/rajpalnehra001" target="_blank">Instagram</a>
    <a href="https://wa.me/917851867154?text=I%20need%20a%20website" target="_blank">WhatsApp</a>
  </div>
</section>

<footer>
  &copy; 2025 Nehra Webs. Crafted with passion and coffee ☕<br>
  Owner: Rajpal Nehra
</footer>

<script>
  function scrollToContact() {
    document.getElementById("contact").scrollIntoView({ behavior: "smooth" });
  }
</script>

</body>
</html>
