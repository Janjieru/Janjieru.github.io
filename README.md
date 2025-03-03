<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        input {
            display: block;
            width: 100%;
            margin: 10px 0;
            padding: 8px;
        }
        button {
            background: #a72828;
            color: white;
            padding: 10px;
            border: none;
            width: 100%;
            cursor: pointer;
            border-radius: 4px;
        }
        button:hover {
            background: #282188;
        }
    </style>
</head>
<body>

    <div class="container">
        <h2>Login</h2>
        <input type="text" id="username" placeholder="Enter Username">
        <input type="password" id="passcode" placeholder="Enter Passcode">
        <button onclick="checkLogin()">Login</button>
        <p id="message"></p>
    </div>

    <script>
        function checkLogin() {
            const correctUsername = "Jhanzielle";
            const correctPasscode = "102608"; // Passcode stored as a string

            let inputUser = document.getElementById("username").value;
            let inputPass = document.getElementById("passcode").value;
            let message = document.getElementById("message");

            if (inputUser === correctUsername) {
                if (inputPass === correctPasscode) {
                    message.style.color = "green";
                    message.textContent = "SUCCESS!";
                    
                    // Redirect to homepage after 1 second
                    setTimeout(() => {
                        window.location.href = "homepage.html";
                    }, 1000);
                } else {
                    message.style.color = "red";
                    message.textContent = "WRONG PASSCODE!";
                }
            } else {
                message.style.color = "red";
                message.textContent = "WRONG USERNAME!";
            }
        }
    </script>

</body>
</html>
