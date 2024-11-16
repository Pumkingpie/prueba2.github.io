<!DOCTYPE html>
<html>

<head>
    <title>Juego de Adivinanzas</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 14vh;
            text-align: center;
            background-attachment: fixed;
            background-size: 100% 100%;
            background-color: rgb(46, 4, 85);
            background-image: url(https://i0.wp.com/www.printmag.com/wp-content/uploads/2021/02/4cbe8d_f1ed2800a49649848102c68fc5a66e53mv2.gif?resize=476%2C280&ssl=1);
        }
        
        h1 {
            color:white;
        }
        
        p {
            margin-bottom: 10px;
        }
        @media (max-width: 767px) {
    body {
        font-size: 20px;
      }
    }

    /* Media query para tabletas */
    @media (min-width: 768px) and (max-width: 1023px) {
     
         body{
        font-size: 24px;
      }
    }

    /* Media query para computadoras de escritorio */
    @media (min-width: 1024px) {
      body {
        font-size: 28px;
      }
    }
    .epic-button {
  position: relative;
  display: inline-block;
  padding: 12px 24px;
  font-size: 18px;
  font-weight: bold;
  color: #fff;
  background-color: #ff5733;
  border: none;
  border-radius: 4px;
  overflow: hidden;
  cursor: pointer;
  z-index: 1;
}

.epic-button::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 0;
  background-color: rgba(255, 255, 255, 0.3);
  z-index: -1;
  transition: height 0.3s;
}

.epic-button:hover::before {
  height: 100%;
}

.epic-button::after {
  content: "";
  position: absolute;
  top: -100%;
  left: -100%;
  width: 200%;
  height: 200%;
  background-color: rgba(255, 255, 255, 0.1);
  transform: rotate(45deg);
  transition: all 0.3s;
}

.epic-button:hover::after {
  top: -10%;
  left: -10%;
}


        
    </style>
    <script>
        function adivinarNumero() {
            var numero = Math.floor(Math.random() * 10) + 1;
            var intentos = 3;

            while (intentos > 0) {
                var respuesta = parseInt(prompt("Adivina el número (1-10). Intentos restantes: " + intentos));

                if (respuesta === numero) {
                    alert("¡Felicidades! ¡Has adivinado el número!");
                    return;
                } else {
                    alert("Número incorrecto. ¡Inténtalo de nuevo!");
                    intentos--;
                }
            }

            alert("Lo siento, has agotado tus intentos. El número correcto era: " + numero);
        }
    </script>
</head>

<body>
    <h1>Juego de Adivinanzas</h1>
    <button class="epic-button" onclick="adivinarNumero()">Comenzar juego</button>
</body>

</html>
