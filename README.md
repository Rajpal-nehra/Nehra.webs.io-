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
      box-shadow: 0 2px 6px rgba(62, 39, 35, 0.
