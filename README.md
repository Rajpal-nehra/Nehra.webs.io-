
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nehra Webs</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f6f4ef;
      color: #333;
    }
    header {
      background: #fff;
      text-align: center;
      padding: 40px 20px;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.05);
    }
    .logo {
      width: 120px;
      height: auto;
      margin-bottom: 10px;
    }
    h1 {
      font-size: 2.4rem;
      color: #222;
      margin: 10px 0;
    }
    .contact-buttons a {
      text-decoration: none;
      color: white;
      padding: 12px 28px;
      border-radius: 30px;
      margin: 10px;
      display: inline-block;
      font-weight: bold;
      transition: 0.3s ease;
    }
    .contact-buttons .instagram {
      background: linear-gradient(to right, #f00073, #ff8800);
    }
    .contact-buttons .whatsapp {
      background: #25d366;
    }
    .contact-buttons a:hover {
      opacity: 0.85;
    }
    .posts-section {
      max-width: 700px;
      margin: 40px auto;
      padding: 20px;
      background: #fff;
      border-radius: 20px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.08);
    }
    .posts-section h2 {
      font-size: 1.8rem;
      margin-bottom: 20px;
    }
    .post {
      margin-bottom: 16px;
      padding: 12px;
      background: #f7f7f7;
      border-left: 4px solid #222;
      border-radius: 6px;
    }
    footer {
      background: #1c1c1c;
      color: #ccc;
      text-align: center;
      padding: 30px 10px;
      margin-top: 40px;
      font-size: 14px;
    }
    .admin-panel {
      text-align: center;
      margin-top: 40px;
    }
    .admin-panel input,
    .admin-panel textarea {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 6px;
      border: 1px solid #ccc;
    }
    .admin-panel button {
      padding: 10px 20px;
      background-color: #222;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }
  </style>
</head>
<body>

<header>
  <img src="logo.png" alt="Nehra Webs Logo" class="logo" />
  <h1>Nehra Webs</h1>
  <div class="contact-buttons">
    <a href="https://www.instagram.com/rajpalnehra001" target="_blank" class="instagram">Instagram</a>
    <a href="https://wa.me/917851867154?text=I%20need%20a%20website" target="_blank" class="whatsapp">WhatsApp</a>
  </div>
</header>

<section class="posts-section">
  <h2>My Posts</h2>
  <div id="posts"></div>
</section>

<div class="admin-panel">
  <h3>Post Something (Only for Rajpal)</h3>
  <textarea id="newPost" placeholder="Write your post here..."></textarea><br />
  <button onclick="addPost()">Add Post</button>
</div>

<footer>
  &copy; 2025 <strong>Nehra Webs</strong>. Crafted with passion and coffee ☕ <br />
  Owner: <strong>Rajpal Nehra</strong>
</footer>

<script>
  function addPost() {
    const postText = document.getElementById("newPost").value;
    if (postText.trim() === "") return;
    const postDiv = document.createElement("div");
    postDiv.className = "post";
    postDiv.innerText = postText;
    document.getElementById("posts").prepend(postDiv);
    document.getElementById("newPost").value = "";
  }
</script>

</body>
</html>
