# Phase5-project
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Simple Login</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-box {
      background: #fff;
      padding: 20px 30px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    .login-box h2 {
      margin-bottom: 20px;
      text-align: center;
    }

    .login-box input[type="text"],
    .login-box input[type="password"] {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    .login-box button {
      width: 100%;
      padding: 10px;
      background: #28a745;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    .login-box button:hover {
      background: #218838;
    }

    .message {
      margin-top: 10px;
      text-align: center;
      color: red;
    }
  </style>
</head>
<body>

  <div class="login-box">
    <h2>Login</h2>
    <input type="text" id="username" placeholder="Username" />
    <input type="password" id="password" placeholder="Password" />
    <button onclick="authenticate()">Login</button>
    <div class="message" id="message"></div>
  </div>

  <script>
    function authenticate() {
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;
      const message = document.getElementById("message");

      // Hardcoded credentials (for demo only!)
      const validUsername = "admin";
      const validPassword = "12345";

      if (username === validUsername && password === validPassword) {
        message.style.color = "green";
        message.textContent = "Login successful!";
        // Redirect or load new content here
      } else {
        message.style.color = "red";
        message.textContent = "Invalid username or password.";
      }
    }
  </script>

</body>
</html>
