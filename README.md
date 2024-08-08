<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wi-Fi Access</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .container {
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        button {
            padding: 10px 20px;
            border: none;
            background-color: #007bff;
            color: white;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        .loading {
            display: none;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Wi-Fi Login</h1>
        <form id="loginForm">
            <input type="text" id="wifiPassword" placeholder="Enter Wi-Fi Password" required>
            <button type="submit">Connect</button>
        </form>
        <div id="loading" class="loading">Loading, please wait...</div>
    </div>
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(event) {
            event.preventDefault();
            document.getElementById('loading').style.display = 'block';
            setTimeout(function() {
                // Simulate form submission and redirection
                document.getElementById('loading').textContent = 'Connected!';
                setTimeout(function() {
                    window.location.href = 'www.google.com';
                }, 1000);
            }, 2000);
        });
    </script>
</body>
</html>
