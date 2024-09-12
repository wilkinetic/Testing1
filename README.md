 ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Don't Give Up Animation</title>
        <style>
            body {
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100vh;
                margin: 0;
                background-color: #f0f0f0;
                font-family: 'Arial', sans-serif;
            }

            #message {
                font-size: 50px;
                font-weight: bold;
                color: #333;
                opacity: 0;
                animation: fadeIn 2s forwards, blink 0.5s step-end infinite alternate;
            }

            @keyframes fadeIn {
                to {
                    opacity: 1;
                }
            }

            @keyframes blink {
                50% {
                    opacity: 0;
                }
            }
        </style>
    </head>
    <body>
        <div id="message">Don't Give Up!</div>

        <script>
            let message = document.getElementById("message");
            setTimeout(() => {
                message.style.animation = "none"; // Stop blinking after 5 seconds
            }, 5000);
        </script>
    </body>
    </html>
    ```
