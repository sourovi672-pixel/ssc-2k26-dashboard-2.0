<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Login Page</title>

<style>
body {
    margin: 0;
    font-family: Arial;
    background: linear-gradient(135deg, #000428, #004e92);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    color: white;
}

.login-box {
    background: white;
    color: black;
    padding: 30px;
    border-radius: 12px;
    width: 300px;
    text-align: center;
}

.login-box h2 {
    margin-bottom: 20px;
}

input {
    width: 90%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 6px;
}

button {
    width: 100%;
    padding: 10px;
    background: #1e90ff;
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
}

button:hover {
    background: #187bcd;
}

#error {
    color: red;
    font-size: 14px;
}
</style>

</head>
<body>

<div class="login-box">
    <h2>Login Boss 🔥</h2>

    <input type="text" id="username" placeholder="Username">
    <input type="password" id="password" placeholder="Password">

    <button onclick="login()">Login</button>

    <p id="error"></p>
</div>

<script>
function login() {
    let user = document.getElementById("username").value;
    let pass = document.getElementById("password").value;

    if(user === "boss" && pass === "1111") {
        document.body.innerHTML = `
            <div style="text-align:center; margin-top:100px; font-family:Arial;">
                <h1>🔥 Welcome to my website 🔥</h1>
                <h2>Developer Sourov 😎</h2>
            </div>
        `;
    } else {
        document.getElementById("error").innerText = "Wrong username or password!";
    }
}
</script>

</body>
</html>
