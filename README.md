<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>URGENTE: Caso para o Doutor José Neto</title>
    <style>
        body {
            background-color: #000;
            color: #fff;
            font-family: 'Arial', sans-serif;
            text-align: center;
            padding: 50px;
        }
        h1 {
            font-size: 50px;
            text-transform: uppercase;
            text-shadow: 3px 3px 10px rgba(255, 0, 0, 0.8), 0 0 25px rgba(0, 255, 255, 0.6);
        }
        p {
            font-size: 30px;
            margin-top: 20px;
            text-shadow: 3px 3px 10px rgba(255, 0, 0, 0.8), 0 0 25px rgba(0, 255, 255, 0.6);
        }
        .btn {
            background-color: #ff00ff;
            color: black;
            font-size: 25px;
            padding: 20px;
            border-radius: 10px;
            cursor: pointer;
            margin-top: 30px;
            border: 2px solid #fff;
            box-shadow: 3px 3px 10px rgba(0, 255, 255, 0.6);
        }
        .btn:hover {
            background-color: #ff7700;
            color: white;
        }
        #btn-nao {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    </style>
</head>
<body>
    <div id="pagina1">
        <h1>URGENTE: Doutor José Neto,</h1>
        <p>Recebemos um caso complexo e sigiloso. Só podemos discutir pessoalmente. ⚖️</p>
        <button class="btn" id="btn-aceitar">Aceito a causa!</button>
    </div>

    <div id="pagina2" style="display: none;">
        <h1>Agora a questão principal...</h1>
        <p>Você topa discutir os termos desse caso tomando aquele café do balacobaco que estávamos falando? ☕</p>
        <button class="btn" id="btn-sim">Sim, é do meu interesse! 📜</button>
        <button class="btn" id="btn-nao" onclick="mudarPosicao()">Não, prefiro arquivar esse caso 😬</button>
    </div>

    <script>
        // Função para mudar de "página"
        document.getElementById('btn-aceitar').addEventListener('click', function() {
            document.getElementById('pagina1').style.display = 'none';
            document.getElementById('pagina2').style.display = 'block';
        });

        // Função para mudar a posição do botão "Não"
        function mudarPosicao() {
            var btnNao = document.getElementById("btn-nao");
            var posX = Math.random() * (window.innerWidth - btnNao.offsetWidth);
            var posY = Math.random() * (window.innerHeight - btnNao.offsetHeight);

            btnNao.style.left = posX + "px";
            btnNao.style.top = posY + "px";
        }

        // Função para quando clicar "Sim"
        document.getElementById('btn-sim').addEventListener('click', function() {
            alert('Parabéns, Doutor! O café do balacobaco será servido! ☕⚖️');
        });
    </script>
</body>
</html>
