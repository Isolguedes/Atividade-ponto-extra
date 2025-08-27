# Atividade-ponto-extra
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
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background-color: #ffd6e0; /* fundo rosa pastel */
      font-family: Arial, sans-serif;
    }
    button {
      padding: 15px 25px;
      margin: 10px;
      border: 2px solid transparent;
      cursor: pointer;
      font-size: 16px;
      border-radius: 8px;
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
      // Clique → muda a cor do fundo
      botao.addEventListener('click', function() {
        document.body.style.backgroundColor = botao.style.backgroundColor;
      });

      // Mouse em cima → borda preta
      botao.addEventListener("mouseover", function() {
        botao.style.border = "3px solid black";
      });

      // Mouse sai → tira borda
      botao.addEventListener("mouseout", function() {
        botao.style.border = "2px solid transparent";
      });
    });
  </script>
</body>
</html>
