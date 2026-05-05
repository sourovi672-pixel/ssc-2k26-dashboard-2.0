<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Pro Sound System</title>

<style>
body{
    margin:0;
    font-family:Arial;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#000428,#004e92);
    transition:0.5s;
    overflow:hidden;
}

/* LOGIN */
.login{
    background:white;
    padding:30px;
    border-radius:15px;
    width:340px;
    text-align:center;
    box-shadow:0 0 25px rgba(0,0,0,0.4);
    animation:pop 1s;
}

@keyframes pop{
    from{transform:scale(0.7);opacity:0;}
    to{transform:scale(1);opacity:1;}
}

input{
    width:90%;
    padding:10px;
    margin:10px 0;
    border-radius:6px;
    border:1px solid #ccc;
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

/* DASHBOARD */
.dashboard{
    display:none;
    width:100%;
    color:white;
    text-align:center;
    animation:fadeIn 0.8s ease;
}

@keyframes fadeIn{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}

/* NAV */
.nav{
    position:fixed;
    top:0;
    width:100%;
    padding:15px;
    background:rgba(0,0,0,0.6);
    display:flex;
    justify-content:space-between;
    color:white;
}

/* PROFILE */
.profile{
    margin-top:90px;
    width:130px;
    height:130px;
    border-radius:50%;
    border:3px solid #00c6ff;
    box-shadow:0 0 20px #00c6ff;
}

/* CARDS */
.card{
    background:white;
    color:black;
    width:250px;
    margin:10px auto;
    padding:20px;
    border-radius:12px;
    transition:0.3s;
}

.card:hover{
    transform:scale(1.08);
}

/* BUTTON */
.logout{
    padding:10px 25px;
    background:red;
    border:none;
    color:white;
    border-radius:6px;
    cursor:pointer;
    margin-top:20px;
}
</style>

</head>

<body>

<!-- 🔊 SOUND FILES -->
<audio id="loginSound" src="https://www.soundjay.com/buttons/sounds/button-09.mp3"></audio>
<audio id="clickSound" src="https://www.soundjay.com/buttons/sounds/button-16.mp3"></audio>

<!-- LOGIN -->
<div class="login" id="loginBox">

<h2>👋 Friend of Sourov</h2>
<p>Login to enter system</p>

<input id="username" placeholder="Username">
<input id="password" type="password" placeholder="Password">

<button onclick="login()">Login</button>

<p id="error"></p>

</div>

<!-- DASHBOARD -->
<div class="dashboard" id="dashboard">

<div class="nav">
<div>🔥 Dashboard</div>
<div>Sourov Dev</div>
</div>

<img class="profile" src="https://i.imgur.com/8QfQZ5F.png">

<h1>Welcome Boss 🔥</h1>
<h2>Developer Sourov 😎</h2>

<div class="card">
<p>👤 User: sourov</p>
<p>📊 Status: Online 🟢</p>
</div>

<div class="card">
<p>⚡ System: PRO SOUND MODE</p>
<p>🚀 Speed: Ultra</p>
</div>

<!-- BUTTON WITH SOUND -->
<button class="logout" onclick="clickSound.play(); logout()">Logout</button>

</div>

<script>
function login(){
    let u=document.getElementById("username").value.trim();
    let p=document.getElementById("password").value.trim();

    if(u==="sourov" && p==="sourov"){
        
        // 🔊 LOGIN SOUND
        document.getElementById("loginSound").play();

        // hide login + show dashboard
        document.getElementById("loginBox").style.display="none";
        document.getElementById("dashboard").style.display="block";

        // background change
        document.body.style.background="linear-gradient(135deg,#0f2027,#203a43,#2c5364)";
    } 
    else {
        document.getElementById("error").innerText="❌ Wrong username or password!";
    }
}

function logout(){
    document.getElementById("loginBox").style.display="block";
    document.getElementById("dashboard").style.display="none";
    document.body.style.background="linear-gradient(135deg,#000428,#004e92)";
}
</script>

</body>
</html>
