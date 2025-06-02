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
    .logo-container {
      text-align: center;
      margin: 2rem 0;
    }
    .logo-container img {
      max-width: 200px;
      height: auto;
      border-radius: 12px;
      border: 2px solid #3E2723;
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
    }
    .new-post input:focus,
    .new-post textarea:focus,
    .new-post select:focus {
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
      transform: translateY(10px);
      animation: fadeSlideIn 0.6s ease forwards;
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
    #logout-btn {
      display: none;
      margin: 0 auto;
      padding: 0.5rem 1rem;
      background: #8D6E63;
      border: none;
      border-radius: 6px;
      color: white;
      cursor: pointer;
      font-weight: bold;
    }
    @keyframes fadeSlideIn {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>
  <header>Nehra.webs.io</header>
  <div class="logo-container">
    <img id="site-logo" src="logo.png" alt="Nehra Webs Logo" />
  </div>

  <div class="contact-buttons">
    <a href="https://www.instagram.com/rajpalnehra001" target="_blank">Instagram</a>
    <a href="https://wa.me/917851867154?text=I%20need%20a%20website" target="_blank">WhatsApp</a>
  </div>

  <button id="logout-btn" onclick="logout()">Logout</button>

  <section class="posts" id="posts-section">
    <div id="admin-only" style="display:none;">
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
    </div>
    <div class="post-list" id="posts"></div>
  </section>

  <footer>
    &copy; 2025 <b>Nehra Webs</b>. Made with ♥ by Rajpal Nehra
  </footer>

  <script>
    const postsContainer = document.getElementById('posts');
    const imageInput = document.getElementById('post-image');
    const previewImage = document.getElementById('preview-image');
    const logoutBtn = document.getElementById('logout-btn');
    let imageDataUrl = "";

    function addWatermarkToImage(dataUrl, watermarkText, callback) {
      const img = new Image();
      img.onload = () => {
        const canvas = document.createElement("canvas");
        canvas.width = img.width;
        canvas.height = img.height;
        const ctx = canvas.getContext("2d");
        ctx.drawImage(img, 0, 0);
        ctx.font = `${Math.floor(canvas.width / 20)}px Arial`;
        ctx.fillStyle = "rgba(62, 39, 35, 0.3)";
        ctx.textAlign = "right";
        ctx.textBaseline = "bottom";
        ctx.fillText(watermarkText, canvas.width - 10, canvas.height - 10);
        callback(canvas.toDataURL("image/png"));
      };
      img.src = dataUrl;
    }

    imageInput.addEventListener('change', () => {
      const file = imageInput.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = e => {
          addWatermarkToImage(e.target.result, "Nehra Webs", (watermarkedUrl) => {
            imageDataUrl = watermarkedUrl;
            previewImage.src = imageDataUrl;
            previewImage.style.display = 'block';
          });
        };
        reader.readAsDataURL(file);
      } else {
        imageDataUrl = "";
        previewImage.style.display = 'none';
      }
    });

    function escapeHtml(text) {
      return text.replace(/&/g, "&amp;")
                 .replace(/</g, "&lt;")
                 .replace(/>/g, "&gt;")
                 .replace(/"/g, "&quot;")
                 .replace(/'/g, "&#039;");
    }

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

    function checkAdminLogin() {
      const pwd = prompt("Enter admin password:");
      if (pwd === "admin123") {
        sessionStorage.setItem("isAdmin", "true");
        showAdminControls();
      } else {
        alert("Wrong password! You cannot access post section.");
      }
    }

    function showAdminControls() {
      document.getElementById("admin-only").style.display = "block";
      logoutBtn.style.display = "block";
    }

    function logout() {
      sessionStorage.removeItem("isAdmin");
      document.getElementById("admin-only").style.display = "none";
      logoutBtn.style.display = "none";
    }

    function addLoginButton() {
      const starBtn = document.createElement("div");
      starBtn.textContent = "☆";
      starBtn.style.cssText = `
        position: fixed;
        bottom: 10px;
        right: 10px;
        font-size: 28px;
        cursor: pointer;
        color: #3E2723;
      `;
      starBtn.onclick = checkAdminLogin;
      document.body.appendChild(starBtn);
    }

    window.onload = () => {
      loadPosts();
      if (sessionStorage.getItem("isAdmin") === "true") {
        showAdminControls();
      } else {
        addLoginButton();
      }
    };
  </script>
</body>
</html>
