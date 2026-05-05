<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Login</title>

<style>
body{
    margin:0;
    font-family:Arial;
    background:linear-gradient(135deg,#000428,#004e92);
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}

.box{
    background:white;
    padding:30px;
    border-radius:12px;
    width:320px;
    text-align:center;
}

input{
    width:90%;
    padding:10px;
    margin:10px 0;
}

button{
    width:100%;
    padding:10px;
    background:#1e90ff;
    border:none;
    color:white;
    border-radius:6px;
    cursor:pointer;
}

#error{
    color:red;
    font-size:14px;
}
</style>

</head>

<body>

<div class="box">

<h3>👋 You are friend of Sourov</h3>
<p>Please login to continue</p>

<input id="username" placeholder="Username">
<input id="password" type="password" placeholder="Password">

<button onclick="login()">Login</button>

<p id="error"></p>

</div>

<script>
function login(){
    let u = document.getElementById("username").value.trim();
    let p = document.getElementById("password").value.trim();

    if(u==="sourov" && p==="sourov"){
        window.location.href="<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Dashboard</title>

<style>
body{
    margin:0;
    font-family:Arial;
    background:linear-gradient(135deg,#0f2027,#203a43,#2c5364);
    color:white;
    text-align:center;
}

.top{
    background:#111;
    padding:15px;
}

.card{
    background:white;
    color:black;
    width:250px;
    margin:20px auto;
    padding:20px;
    border-radius:12px;
}

button{
    padding:10px 20px;
    background:red;
    border:none;
    color:white;
    border-radius:6px;
    cursor:pointer;
}
</style>

</head>

<body>

<div class="top">
<h2>🔥 Dashboard</h2>
</div>

<h2>Welcome to my website 🔥</h2>
<h3>Developer Sourov 😎</h3>

<div class="card">
<p>👤 User: sourov</p>
<p>📊 Status: Active</p>
</div>

<button onclick="logout()">Logout</button>

<script>
function logout(){
    window.location.href="index.html";
}
</script>

</body>
</html>";
    } else {
        document.getElementById("error").innerText="❌ Wrong username or password!";
    }
}
</script>

</body>
</html>
