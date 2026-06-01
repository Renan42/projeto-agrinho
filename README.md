# projeto-agrinho
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GameHub</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    background:#0f172a;
    color:white;
}

header{
    background:#1e293b;
    padding:20px;
    text-align:center;
}

header h1{
    color:#38bdf8;
}

.games{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
    gap:20px;
    padding:20px;
}

.card{
    background:#1e293b;
    border-radius:15px;
    padding:20px;
    text-align:center;
}

button{
    background:#38bdf8;
    border:none;
    padding:10px 20px;
    border-radius:8px;
    cursor:pointer;
    margin-top:10px;
}

button:hover{
    background:#0ea5e9;
}

input{
    padding:8px;
    border-radius:5px;
    border:none;
}
</style>
</head>
<body>

<header>
<h1>🎮 GameHub</h1>
<p>Portal de Jogos Online</p>
</header>

<section class="games">

<div class="card">
<h2>⚡ Clique Rápido</h2>
<p>Pontos: <span id="score">0</span></p>
<button onclick="clickGame()">Clique!</button>
</div>

<div class="card">
<h2>🎲 Adivinhe o Número</h2>
<input id="guess" type="number" min="1" max="10">
<br>
<button onclick="guessGame()">Tentar</button>
<p id="guessResult"></p>
</div>

<div class="card">
<h2>✊ Pedra Papel Tesoura</h2>
<button onclick="rps('Pedra')">Pedra</button>
<button onclick="rps('Papel')">Papel</button>
<button onclick="rps('Tesoura')">Tesoura</button>
<p id="rpsResult"></p>
</div>

<div class="card">
<h2>🎯 Jogo da Sorte</h2>
<button onclick="luckGame()">Testar Sorte</button>
<p id="luckResult"></p>
</div>

</section>

<script>

let score = 0;

function clickGame(){
    score++;
    document.getElementById("score").innerText = score;
}

function guessGame(){
    let secret = Math.floor(Math.random()*10)+1;
    let guess = Number(document.getElementById("guess").value);

    document.getElementById("guessResult").innerText =
        guess === secret
        ? "🎉 Você acertou!"
        : "❌ Errou! Era " + secret;
}

function rps(player){
    let choices = ["Pedra","Papel","Tesoura"];
    let cpu = choices[Math.floor(Math.random()*3)];

    let result;

    if(player===cpu){
        result="Empate!";
    }else if(
      (player==="Pedra"&&cpu==="Tesoura")||
      (player==="Papel"&&cpu==="Pedra")||
      (player==="Tesoura"&&cpu==="Papel")
    ){
      result="Você venceu!";
    }else{
      result="Você perdeu!";
    }

    document.getElementById("rpsResult").innerText =
      `Computador: ${cpu} | ${result}`;
}

function luckGame(){
    let n = Math.floor(Math.random()*100)+1;

    if(n > 80){
        document.getElementById("luckResult").innerText =
        "🍀 Incrível! Sorte máxima!";
    }else if(n > 50){
        document.getElementById("luckResult").innerText =
        "😊 Boa sorte!";
    }else{
        document.getElementById("luckResult").innerText =
        "😅 Hoje não foi seu dia.";
    }
}

</script>

</body>
</html>
