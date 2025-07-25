<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Convite Inadiável: Jão, é hoje!</title>
    <style>
        body {
            background-color: #1a1a1a;
            color: #fff;
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        ::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1586190848861-99aa4a171e90?auto=format&fit=crop&w=1500&q=80') no-repeat center center fixed;
            background-size: cover;
            filter: blur(5px) brightness(0.6);
            z-index: -1;
        }

        h1, p {
            text-shadow: 1px 1px 4px rgba(255, 255, 255, 0.4);
        }

        .btn {
            background-color: #ff6347;
            color: white;
            font-size: 20px;
            padding: 15px 30px;
            border-radius: 20px;
            cursor: pointer;
            margin-top: 30px;
            border: none;
            box-shadow: 0 5px 15px rgba(255, 99, 71, 0.6);
            transition: all 0.3s ease-in-out;
        }

        .btn:hover {
            background-color: #ffcc00;
            color: #000;
            transform: scale(1.05);
        }

        #pagina1, #pagina2 {
            background: rgba(0, 0, 0, 0.5);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.8);
        }

        #btn-nao {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            transition: transform 0.2s ease-in-out;
        }

        #btn-nao:hover {
            transform: translate(-50%, -50%) scale(1.2);
        }
    </style>
</head>
<body>
    <div id="pagina1">
        <h1>Jão Emidio, temos uma missão crítica!</h1>
        <p>Operação: *Strogonoff do Balacobaco + Coca* 🥩🥄🥤<br>
        Local: minha casa. Horário: hoje à noite.<br>
        Sua presença é indispensável.</p>
        <button class="btn" id="btn-aceitar">Recebo a missão! 🍽️</button>
    </div>

    <div id="pagina2" style="display: none;">
        <h1>Confirmando protocolo final...</h1>
        <p>Você está pronto para saborear o melhor strogonoff da cidade ao lado de uma pessoa incrível? 👩‍🍳❤️</p>
        <button class="btn" id="btn-sim">Sim, partiu comer cadáver de frango! 😋</button>
        <button class="btn" id="btn-nao" onclick="mudarPosicao()">Não, eu tenho autismo! </button>
    </div>

    <script>
        document.getElementById('btn-aceitar').addEventListener('click', function() {
            document.getElementById('pagina1').style.display = 'none';
            document.getElementById('pagina2').style.display = 'block';
        });

        function mudarPosicao() {
            var btnNao = document.getElementById("btn-nao");
            var posX = Math.random() * (window.innerWidth - btnNao.offsetWidth);
            var posY = Math.random() * (window.innerHeight - btnNao.offsetHeight);

            btnNao.style.left = posX + "px";
            btnNao.style.top = posY + "px";
        }

        document.getElementById('btn-sim').addEventListener('click', function() {
            alert('Parabéns! O strogonoff do balacobaco será servido 🍗😎💥(leve a coca)');
        });
    </script>
</body>
</html>
