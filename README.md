# Don't Give Up Animation

A simple animated message "Don't Give Up" built with HTML, CSS, and JavaScript. The animation fades in and blinks the text for a few seconds before stopping the blinking.

## Demo

![Don't Give Up Animation](https://your-demo-link.gif)

## Features

- Fades in the message "Don't Give Up!"
- Blinks the message for 5 seconds
- Stops the blinking after 5 seconds for better readability

## Usage

To run this animation:

1. Copy the code below and save it as `index.html`:
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

2. Open the file in your browser to view the animation.

## How it Works

- The **HTML** creates a centered message.
- **CSS** handles the animation:
  - `fadeIn`: Gradually shows the message over 2 seconds.
  - `blink`: Makes the message blink.
- **JavaScript** stops the blinking after 5 seconds.

## License

This project is open-source and free to use.
