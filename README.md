<!DOCTYPE html>  <html lang="pt-BR">  
<head>  
  <meta charset="UTF-8">  
  <title>Auxílio Premium</title>  
  <style>  
    body {  
      margin: 0;  
      height: 100vh;  
      font-family: Arial, sans-serif;  
      background: #000;  
      overflow: hidden;  
      display: flex;  
      justify-content: center;  
      align-items: center;  
    }  #particles-js {  
  position: absolute;  
  width: 100%;  
  height: 100%;  
  top: 0;  
  left: 0;  
  z-index: -1;  
}  

.container {  
  background: rgba(20, 20, 20, 0.9);  
  padding: 20px;  
  border-radius: 12px;  
  box-shadow: 0 0 20px rgba(0,0,0,0.6);  
  width: 300px;  
  color: #fff;  
}  

h2 {  
  text-align: center;  
  margin-bottom: 20px;  
}  

details {  
  background: #2b2b2b;  
  border-radius: 6px;  
  margin-bottom: 12px;  
  padding: 8px;  
}  

details summary {  
  cursor: pointer;  
  font-weight: bold;  
  padding: 5px;  
}  

label {  
  display: block;  
  margin: 6px 0;  
}  

.status {  
  background: #1e1e1e;  
  padding: 10px;  
  border-radius: 6px;  
  font-size: 14px;  
  margin-top: 10px;  
  white-space: pre-line;  
}  

/* Login */  
.login-box {  
  background: rgba(20, 20, 20, 0.9);  
  padding: 20px;  
  border-radius: 12px;  
  box-shadow: 0 0 20px rgba(0,0,0,0.6);  
  width: 300px;  
  color: #fff;  
  text-align: center;  
}  

.login-box input {  
  width: 90%;  
  padding: 10px;  
  margin: 8px 0;  
  border: none;  
  border-radius: 6px;  
  outline: none;  
}  

.login-box button {  
  width: 100%;  
  padding: 10px;  
  margin-top: 10px;  
  background: #2b2b2b;  
  border: none;  
  border-radius: 6px;  
  color: #fff;  
  font-weight: bold;  
  cursor: pointer;  
}  

.error {  
  color: red;  
  margin-bottom: 10px;  
  display: none;  
}  

#app {  
  display: none;  
}

  </style>  
</head>  
<body>  
  <div id="particles-js"></div>    <!-- Tela de Login -->    <div id="login" class="login-box">  
    <h2>Login</h2>  
    <div class="error" id="errorMsg">Usuário ou senha incorretos</div>  
    <input type="text" id="username" placeholder="Usuário">  
    <input type="password" id="password" placeholder="Senha">  
    <button onclick="login()">Entrar</button>  
  </div>    <!-- App -->    <div id="app" class="container">  
    <h2>Auxílio Premium</h2>  <details open>  
  <summary>Sistema Avançado</summary>  
  <label><input type="checkbox" id="fps"> 120 FPS</label>  
  <label><input type="checkbox" id="norecoil"> No Recoil</label>  
</details>  

<details open>  
  <summary>Ajustes de Mira</summary>  
  <label><input type="checkbox" id="aimbot"> Aimbot 90%</label>  
  <label><input type="checkbox" id="headtrick"> Head Trick</label>  
  <label><input type="checkbox" id="neural"> Neural Aim</label>  
</details>  

<div class="status" id="statusBox">  
  120 FPS: Desativado  
  No Recoil: Desativado  
  Aimbot 90%: Desativado  
  Head Trick: Desativado  
  Neural Aim: Desativado  
</div>

  </div>    <!-- Partículas -->    <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>    <script>  
    particlesJS("particles-js", {  
      "particles": {  
        "number": { "value": 80 },  
        "color": { "value": "#ffffff" },  
        "shape": { "type": "circle" },  
        "opacity": { "value": 0.5 },  
        "size": { "value": 3 },  
        "line_linked": {  
          "enable": true,  
          "distance": 150,  
          "color": "#ffffff",  
          "opacity": 0.4,  
          "width": 1  
        },  
        "move": {  
          "enable": true,  
          "speed": 2  
        }  
      }  
    });  
  
    function login() {  
      const user = document.getElementById("username").value;  
      const pass = document.getElementById("password").value;  
      const error = document.getElementById("errorMsg");  
  
      if (user === "dxzinn" && pass === "6305") {  
        document.getElementById("login").style.display = "none";  
        document.getElementById("app").style.display = "block";  
      } else {  
        error.style.display = "block";  
      }  
    }  
  
    const checkboxes = document.querySelectorAll("input[type=checkbox]");  
    const statusBox = document.getElementById("statusBox");  
  
    function updateStatus() {  
      statusBox.textContent =  
        `120 FPS: ${document.getElementById("fps").checked ? "Ativado" : "Desativado"}\n` +  
        `No Recoil: ${document.getElementById("norecoil").checked ? "Ativado" : "Desativado"}\n` +  
        `Aimbot 90%: ${document.getElementById("aimbot").checked ? "Ativado" : "Desativado"}\n` +  
        `Head Trick: ${document.getElementById("headtrick").checked ? "Ativado" : "Desativado"}\n` +  
        `Neural Aim: ${document.getElementById("neural").checked ? "Ativado" : "Desativado"}`;  
    }  
  
    checkboxes.forEach(chk => chk.addEventListener("change", updateStatus));  
  </script>  </body>  
</html>
