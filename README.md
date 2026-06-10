<body>

<div id="loginScreen">
    <h1>🐶 Mi Schnauzer Virtual</h1>
    <p>Ingresa la contraseña de 3 dígitos para jugar</p>

    <input type="password" id="password" maxlength="3" placeholder="***">
    <br><br>
    <button onclick="checkPassword()">Entrar</button>

    <p id="loginMessage" style="color:red;"></p>
</div>

<div id="gameContainer" style="display:none;">

    <!-- AQUÍ VA TODO TU JUEGO DEL SCHNAUZER -->

</div>

<script>
const PASSWORD = "123";

function checkPassword() {
    const pass = document.getElementById("password").value;

    if(pass === PASSWORD) {
        document.getElementById("loginScreen").style.display = "none";
        document.getElementById("gameContainer").style.display = "block";
    } else {
        document.getElementById("loginMessage").textContent =
            "Contraseña incorrecta";
    }
}
</script>

</body>
