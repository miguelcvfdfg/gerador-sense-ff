<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Gerador de Sense do Miguel</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  font-family: Arial, sans-serif;
  background: #eaeaea;
  padding: 20px;
}
.card {
  background: #fff;
  padding: 20px;
  border-radius: 10px;
}
button {
  padding: 12px;
  width: 100%;
  margin-top: 10px;
  font-size: 16px;
}
</style>
</head>

<body>

<div class="card">
  <h2>Sense do dia 🔥</h2>
  <p id="resultado">Carregando...</p>
  <button onclick="novaSense()">gera sense</button>
</div>

<script>
const senses = [
  "Geral: 145 | Red Dot: 7 | 2x: 107 | 4x: 101 | DPI: 500",
  "Geral: 140 | Red Dot: 8 | 2x: 110 | 4x: 98 | DPI: 450",
  "Geral: 150 | Red Dot: 6 | 2x: 105 | 4x: 100 | DPI: 600",
  "Geral: 135 | Red Dot: 9 | 2x: 112 | 4x: 95 | DPI: 480"
];

function gerarAleatoria() {
  return senses[Math.floor(Math.random() * senses.length)];
}

function novaSense() {
  const hoje = new Date().toDateString();
  const valor = gerarAleatoria();

  document.getElementById("resultado").innerText = valor;

  localStorage.setItem("sense_dia", valor);
  localStorage.setItem("data_sense", hoje);
}

window.onload = function () {
  const hoje = new Date().toDateString();
  const dataSalva = localStorage.getItem("data_sense");
  const senseSalva = localStorage.getItem("sense_dia");

  if (dataSalva === hoje && senseSalva) {
    document.getElementById("resultado").innerText = senseSalva;
  } else {
    novaSense();
  }
};
</script>

</body>
</html>
