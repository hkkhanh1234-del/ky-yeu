<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>KỶ YẾU | ID CARD</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Font -->
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400&family=Nanum+Pen+Script&display=swap" rel="stylesheet">

    <style>
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            font-family: 'Lato', sans-serif;
            overflow: hidden;
        }

        /* ===== BACKGROUND ===== */
        #background {
            position: fixed;
            inset: 0;
            background-image: url("https://raw.githubusercontent.com/hkkhanh1234-del/ky-yeu/main/Image.png");
            background-size: cover;
            background-position: center;
            filter: brightness(0.75);
        }

        /* ===== WRAPPER ===== */
        #wrapper {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 50vw;
            height: 31.7vw;
        }

        /* ===== ID CARD ===== */
        #card {
            position: relative;
            width: 100%;
            height: 100%;
            background: #faefcf;
            border: 2px solid #000;
            box-shadow: 0 10px 30px rgba(0,0,0,.4);
        }

        /* LEFT IMAGE BOX */
        .image-box {
            position: absolute;
            top: 4vw;
            left: 3vw;
            width: 18vw;
            height: 22vw;
            border: 2px solid #000;
            background: rgba(255,255,255,.6);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.6vw;
        }

        /* RIGHT TEXT INPUTS */
        .handwriting {
            font-family: 'Nanum Pen Script', cursive;
            background: transparent;
            border: none;
            outline: none;
            text-align: center;
            width: 18vw;
            color: #000;
        }

        #call-me {
            position: absolute;
            top: 6vw;
            right: 3vw;
            font-size: 2.1vw;
        }

        #three-words {
            position: absolute;
            top: 9vw;
            right: 3vw;
            font-size: 2vw;
        }

        #future-self {
            position: absolute;
            top: 12vw;
            right: 3vw;
            font-size: 1.7vw;
            resize: none;
        }

        /* SIGNATURE */
        .signature {
            position: absolute;
            bottom: 3vw;
            right: 3vw;
            font-family: 'Nanum Pen Script', cursive;
            font-size: 1.8vw;
        }

        /* MOBILE */
        @media (max-width: 900px) {
            #wrapper {
                width: 90vw;
                height: 57vw;
            }
            .image-box {
                width: 30vw;
                height: 36vw;
                font-size: 4vw;
            }
            .handwriting {
                width: 35vw;
            }
        }
    </style>
</head>

<body>
    <div id="background"></div>

    <div id="wrapper">
        <div id="card">

            <!-- LEFT -->
            <div class="image-box">
                Your photo
            </div>

            <!-- RIGHT -->
            <input id="call-me" class="handwriting"
                   placeholder="You can call me">

            <input id="three-words" class="handwriting"
                   placeholder="3 words describe me">

            <textarea id="future-self" class="handwriting" rows="3"
                      placeholder="To my future self:"></textarea>

            <div class="signature">
                Signature
            </div>

        </div>
    </div>
</body>
</html>
