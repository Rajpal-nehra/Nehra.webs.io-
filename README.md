<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Nehra Webs</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #FFF8E7;
      color: #3E2723;
    }
    header {
      background: linear-gradient(to right, #5D4037, #3E2723);
      color: #FFF8E7;
      padding: 1rem;
      text-align: center;
      font-size: 2rem;
      font-weight: bold;
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
      color: #FFF8E7;
      font-weight: bold;
      transition: 0.3s;
      box-shadow: 0 2px 5px rgba(62, 39, 35, 0.3);
    }
    .contact-buttons a:first-child {
      background: linear-gradient(to right, #6D4C41, #3E2723);
    }
    .contact-buttons a:last-child {
      background: #4E342E;
    }
    .contact-buttons a:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 16px rgba(62, 39, 35, 0.5);
    }
    .posts {
      max-width: 600px;
      margin: 2rem auto;
      background: #FFF8E7;
      padding: 2rem;
      border-radius: 16px;
      box-shadow: 0 4px 10px rgba(62, 39, 35, 0.1);
      border: 2px solid #3E2723;
    }
    .posts h2 {
      text-align: center;
      margin-bottom: 1.5rem;
      color: #3E2723;
    }
    .new-post {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      margin-bottom: 1rem;
    }
    .new-post input[type="text"],
    .new-post textarea,
    .new-post select,
    .new-post input[type="file"] {
      width: 100%;
      padding: 0.75rem;
      border: 1.5px solid #3E2723;
      border-radius: 8px;
      font-size: 1rem;
      background: #FFF8E7;
      color: #3E2723;
      transition: border-color 0.3s;
    }
    .new-post input[type="text"]:focus,
    .new-post textarea:focus,
    .new-post select:focus,
    .new-post input[type="file"]:focus {
      border-color: #5D4037;
      outline: none;
    }
    .new-post button {
      padding: 0.75rem;
      background: linear-gradient(to right, #5D4037, #3E2723);
      color: #FFF8E7;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.3s;
      box-shadow: 0 4px 8px rgba(62, 39, 35, 0.3);
    }
    .new-post button:hover {
      background: linear-gradient(to right, #3E2723, #5D4037);
      box-shadow: 0 6px 14px rgba(62, 39, 35, 0.5);
    }
    .post-list {
      margin-top: 2rem;
    }
    .post {
      background: #F5EAD6;
      border-left: 6px solid #5D4037;
      padding: 1rem;
      border-radius: 8px;
      margin-bottom: 1rem;
      opacity: 0;
      animation: fadeIn 0.5s ease forwards;
      color: #3E2723;
      box-shadow: 0 2px 6px rgba(62, 39, 35, 0.1);
    }
    .post img {
      max-width: 100%;
      margin-top: 10px;
      border-radius: 8px;
      border: 1px solid #3E2723;
    }
    #preview-image {
      max-width: 100%;
      margin-top: 10px;
      border-radius: 8px;
      display: none;
      border: 1px solid #3E2723;
    }
    footer {
      text-align: center;
      padding: 1rem;
      background: #3E2723;
      color: #FFF8E7;
      font-weight: bold;
      letter-spacing: 0.05em;
    }
    .admin-star {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #3E2723;
      color: white;
      font-size: 1.5rem;
      padding: 10px 15px;
      border-radius: 50%;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
      transition: transform 0.2s;
      z-index: 999;
    }
    .admin-star:hover {
      transform: scale(1.2);
      background: #5D4037;
    }
    @keyframes fadeIn {
      to {
        opacity: 1;
      }
    }
  </style>
</head>
<body>
  <header style="color: #3E2723;">Nehra.webs.io</header>

  <div class="contact-buttons">
    <a href="https://www.instagram.com/rajpalnehra001" target="_blank">Instagram</a>
    <a href="https://wa.me/917851867154?text=I%20need%20a%20website" target="_blank">WhatsApp</a>
  </div>

  <section class="posts" id="posts-section" style="display:none;">
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
      <input type="file" id="post-image" accept="image/*" />
      <img id="preview-image" alt="Image preview" />
      <button onclick="addPost()">Post</button>
    </div>
    <div class="post-list" id="posts"></div>
  </section>

  <div class="admin-star" onclick="checkAdminLogin()">☆</div>

  <footer>
    &copy; 2025 <b>Nehra Webs</b>. Made with ♥ by Rajpal Nehra
  </footer>

  <script>
    const postsContainer = document.getElementById('posts');
    const imageInput = document.getElementById('post-image');
    const previewImage = document.getElementById('preview-image');
    let imageDataUrl = "";

    function checkAdminLogin() {
      const pwd = prompt("Enter admin password:");
      if (pwd === "admin123") {
        document.getElementById('posts-section').style.display = "block";
        loadPosts();
      } else {
        alert("Wrong password! You cannot access post section.");
      }
    }

    imageInput.addEventListener('change', () => {
      const file = imageInput.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = e => {
          imageDataUrl = e.target.result;
          previewImage.src = imageDataUrl;
          previewImage.style.display = 'block';
        };
        reader.readAsDataURL(file);
      } else {
        imageDataUrl = "";
        previewImage.style.display = 'none';
      }
    });

    function loadPosts() {
      const posts = JSON.parse(localStorage.getItem("nehra_posts") || "[]");
      postsContainer.innerHTML = posts.map(p => `
        <div class="post">
          <strong>${escapeHtml(p.title)}</strong>
          <p>${escapeHtml(p.content)}</p>
          ${p.image ? `<img src="${p.image}" alt="Post image" />` : ""}
          <small><i>${escapeHtml(p.category)}</i></small>
        </div>
      `).join("");
    }

    function addPost() {
      const title = document.getElementById("post-title").value.trim();
      const content = document.getElementById("post-content").value.trim();
      const category = document.getElementById("post-category").value;
      if (!title || !content) {
        alert("Please enter both title and content.");
        return;
      }
      const posts = JSON.parse(localStorage.getItem("nehra_posts") || "[]");
      posts.unshift({ title, content, category, image: imageDataUrl });
      localStorage.setItem("nehra_posts", JSON.stringify(posts));
      document.getElementById("post-title").value = "";
      document.getElementById("post-content").value = "";
      document.getElementById("post-category").value = "";
      imageInput.value = "";
      previewImage.style.display = "none";
      imageDataUrl = "";
      loadPosts();
    }

    function escapeHtml(text) {
      return text
        .replace(/&/g, "&amp;")
        .replace(/</g, "&lt;")
        .replace(/>/g, "&gt;")
        .replace(/"/g, "&quot;")
        .replace(/'/g, "&#039;");
    }
  </script>
</body>
</html>
