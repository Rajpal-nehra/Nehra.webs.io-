<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nehra Webs</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f5f5f5;
      color: #2d2d2d;
    }
    header {
      background: linear-gradient(to right, #6a11cb, #2575fc);
      color: white;
      padding: 1rem;
      text-align: center;
      font-size: 2rem;
      font-weight: bold;
    }
    .logo-container {
      text-align: center;
      margin: 2rem 0;
    }
    .logo-container img {
      max-width: 200px;
      height: auto;
      border-radius: 12px;
    }
    .contact-buttons {
      display: flex;
      justify-content: center;
      gap: 1rem;
      margin: 2rem 0;
    }
    .contact-buttons a {
      padding: 0.75rem 1.5rem;
      border-radius: 30px;
      text-decoration: none;
      color: white;
      font-weight: bold;
      transition: 0.3s;
    }
    .contact-buttons a:first-child {
      background: linear-gradient(to right, #f953c6, #b91d73);
    }
    .contact-buttons a:last-child {
      background: #25D366;
    }
    .contact-buttons a:hover {
      transform: scale(1.05);
      box-shadow: 0 6px 12px rgba(0,0,0,0.2);
    }
    .posts {
      max-width: 600px;
      margin: 2rem auto;
      background: white;
      padding: 2rem;
      border-radius: 16px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .posts h2 {
      text-align: center;
      margin-bottom: 1.5rem;
    }
    .new-post {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
    .new-post input[type="text"],
    .new-post textarea,
    .new-post select {
      width: 100%;
      padding: 0.75rem;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
    }
    .new-post button {
      padding: 0.75rem;
      background: #6a11cb;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.3s;
    }
    .new-post button:hover {
      background: #2575fc;
    }
    .post-list {
      margin-top: 2rem;
    }
    .post {
      background: #f9f9f9;
      border-left: 4px solid #6a11cb;
      padding: 1rem;
      border-radius: 8px;
      margin-bottom: 1rem;
    }
    footer {
      text-align: center;
      padding: 1rem;
      background: #1a1a1a;
      color: white;
    }
  </style>
</head>
<body>
  <header>Nehra.webs.io</header>  <div class="logo-container">
    <img id="site-logo" src="logo.png" alt="Nehra Webs Logo" />
  </div>  <div class="contact-buttons">
    <a href="https://www.instagram.com/rajpalnehra001" target="_blank">Instagram</a>
    <a href="https://wa.me/917851867154?text=I%20need%20a%20website" target="_blank">WhatsApp</a>
  </div>  <section class="posts">
    <h2>New Post</h2>
    <div class="new-post">
      <input type="text" id="post-title" placeholder="Type a title" />
      <textarea id="post-content" rows="5" placeholder="Share your thoughts with pictures"></textarea>
      <select id="post-category">
        <option value="">Select Category</option>
        <option value="Update">Update</option>
        <option value="Tech">Tech</option>
        <option value="Music">Music</option>
      </select>
      <button onclick="addPost()">Post</button>
    </div><div class="post-list" id="posts"></div>

  </section>  <footer>
    &copy; 2025 <b>Nehra Webs</b>. Made with ♥ by Rajpal Nehra
  </footer>  <script>
    const postsContainer = document.getElementById('posts');

    function loadPosts() {
      const posts = JSON.parse(localStorage.getItem("nehra_posts") || "[]");
      postsContainer.innerHTML = posts.map(p => `
        <div class="post">
          <strong>${p.title}</strong>
          <p>${p.content}</p>
          <small><i>${p.category}</i></small>
        </div>
      `).join("");
    }

    function addPost() {
      const title = document.getElementById("post-title").value.trim();
      const content = document.getElementById("post-content").value.trim();
      const category = document.getElementById("post-category").value;
      if (title && content) {
        const posts = JSON.parse(localStorage.getItem("nehra_posts") || "[]");
        posts.unshift({ title, content, category });
        localStorage.setItem("nehra_posts", JSON.stringify(posts));
        document.getElementById("post-title").value = "";
        document.getElementById("post-content").value = "";
        loadPosts();
      }
    }

    window.onload = loadPosts;
  </script></body>
</html>
