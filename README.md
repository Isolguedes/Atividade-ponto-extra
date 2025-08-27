<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Painel de Cores</title>
  <style>
    body {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #ffd6e0;
      font-family: Arial, sans-serif;
    }
    h1 {
      margin-bottom: 20px;
    }
    button {
      padding: 15px 25px;
      margin: 10px;
      border: 2px solid transparent;
      cursor: pointer;
      font-size: 16px;
      border-radius: 8px;
      transition: 0.2s;
    }
    #cinza { background-color: gray; color: white; }
    #verde { background-color: green; color: white; }
    #vermelho { background-color: red; color: white; }
  </style>
</head>
<body>
  <h1>Escolha uma cor 🌸</h1>
  <button id="cinza" class="botoes">Cinza</button>
  <button id="verde" class="botoes">Verde</button>
  <button id="vermelho" class="botoes">Vermelho</button>

  <script>
    const botoes = document.querySelectorAll('.botoes');

    botoes.forEach(function(botao) {
      botao.addEventListener('click', function() {
        document.body.style.backgroundColor = getComputedStyle(botao).backgroundColor;
      });

      botao.addEventListener("mouseover", function() {
        botao.style.border = "3px solid black";
      });

      botao.addEventListener("mouseout", function() {
        botao.style.border = "2px solid transparent";
      });
    });
  </script>
</body>
</html>
