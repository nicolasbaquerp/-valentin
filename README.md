# -valentin
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>San Valentín para Brenda Ortega</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
        }

        h1 {
            color: #e74c3c;
            font-size: 3rem;
            text-align: center;
            margin-bottom: 20px;
        }

        .message {
            background-color: #fff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 500px;
            text-align: center;
        }

        .message p {
            font-size: 1.2rem;
            color: #555;
            line-height: 1.6;
        }

        .heart {
            font-size: 5rem;
            color: #e74c3c;
            margin-top: 20px;
        }

        .footer {
            font-size: 1rem;
            margin-top: 30px;
            color: #777;
        }

        .button {
            background-color: #e74c3c;
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            font-size: 1.2rem;
            text-decoration: none;
            display: inline-block;
            margin-top: 20px;
            transition: background-color 0.3s;
        }

        .button:hover {
            background-color: #c0392b;
        }

        .no-button {
            background-color: #3498db;
        }

        .no-button:hover {
            background-color: #2980b9;
        }

        /* Animación de movimiento para el botón "No" */
        .no-button-move {
            animation: moveButton 0.5s ease-in-out;
        }

        @keyframes moveButton {
            0% {
                transform: translateX(0);
            }
            25% {
                transform: translateX(-10px);
            }
            50% {
                transform: translateX(10px);
            }
            75% {
                transform: translateX(-10px);
            }
            100% {
                transform: translateX(0);
            }
        }

        .no-button-text {
            display: inline;
        }

        .no-button-text.hide {
            display: none;
        }

        .no-button-text.show {
            display: inline;
            color: #e74c3c;
            font-weight: bold;
            font-size: 1.2rem;
        }
    </style>
</head>
<body>

    <h1>Feliz San Valentín, Brenda Ortega</h1>

    <div class="message">
        <p>Brenda, en este día tan especial quiero expresarte lo mucho que significas para mí. 
        Cada momento a tu lado es una bendición y mi vida ha sido mucho más feliz desde que te conocí. 
        ¿Te gustaría ser mi Valentín?</p>

        <div class="heart">❤️</div>

        <!-- Botones para la respuesta -->
        <a href="mailto:brenda@ejemplo.com?subject=¡Sí, mi vida!" class="button">¡Sí, mi vida!</a>
        
        <a href="#" id="no-button" class="button no-button" onclick="moveButton()">No</a>
        <div id="no-button-text" class="no-button-text hide">Por favor</div>
    </div>

    <div class="footer">
        <p>Hecho con ❤️ por un admirador muy especial.</p>
    </div>

    <script>
        let clickCount = 0; // Contador para los clics

        function moveButton() {
            const button = document.getElementById("no-button");
            const text = document.getElementById("no-button-text");

            // Agregar la clase de animación
            button.classList.add("no-button-move");

            // Primera vez que hace clic: "Por favor"
            if (clickCount === 0) {
                setTimeout(() => {
                    text.classList.remove("hide");
                    text.classList.add("show");
                    clickCount++;
                }, 500);
            } 
            // Segunda vez que hace clic: "Pecu"
            else if (clickCount === 1) {
                setTimeout(() => {
                    text.textContent = "Pecu";
                    button.classList.add("no-button-move");
                    clickCount++;
                }, 500);
            }
            // Tercera vez que hace clic: "No me importa, te obligo"
            else if (clickCount === 2) {
                setTimeout(() => {
                    text.textContent = "No me importa, te obligo";
                    button.classList.add("no-button-move");
                    clickCount++;
                }, 500);
            }
            // Cuarta vez que hace clic: "Ya sabes"
            else if (clickCount === 3) {
                setTimeout(() => {
                    text.textContent = "Ya sabes";
                    button.classList.add("no-button-move");
                    clickCount++;
                }, 500);
            }
            // Evitar que el botón enlace a alguna parte
            return false;
        }
    </script>

</body>
</html>
