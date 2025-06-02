<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nehra Webs</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f9f5ef;
      color: #5c3a23;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
    }

    #site-logo {
      max-width: 200px;
      margin-bottom: 20px;
    }

    h1 {
      margin: 0;
      font-size: 2em;
    }

    .login-button {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: transparent;
      border: none;
      font-size: 24px;
      cursor: pointer;
      color: #5c3a23;
    }

    .login-modal {
      display: none;
      position: fixed;
      bottom: 80px;
      right: 20px;
      background-color: white;
      border: 1px solid #ddd;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
      z-index: 1000;
    }

    .login-modal input {
      width: 100%;
      padding: 8px;
      margin-top: 10px;
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    .login-modal button {
      width: 100%;
      padding: 8px;
      background-color: #5c3a23;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .login-modal button:hover {
      background-color: #7a4e2f;
    }
  </style>
</head>
<body>

  <!-- Logo -->
  <img id="site-logo" src="logo.png" alt="Nehra Webs Logo" />
  <h1>Nehra Webs</h1>

  <!-- Admin Login Icon Button -->
  <button class="login-button" onclick="toggleLogin()">☆</button>

  <!-- Login Modal -->
  <div class="login-modal" id="loginModal">
    <h3>Admin Login</h3>
    <input type="text" placeholder="Username" id="username" />
    <input type="password" placeholder="Password" id="password" />
    <button onclick="submitLogin()">Login</button>
  </div>

  <script>
    function toggleLogin() {
      const modal = document.getElementById('loginModal');
      modal.style.display = modal.style.display === 'block' ? 'none' : 'block';
    }

    function submitLogin() {
      const username = document.getElementById('username').value;
      const password = document.getElementById('password').value;
      // Replace with real logic
      alert(`Username: ${username}\nPassword: ${password}`);
    }
  </script>

</body>
</html>
