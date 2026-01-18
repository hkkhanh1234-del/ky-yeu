<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>KỶ YẾU – ID CARD</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@300;400&family=Nanum+Pen+Script&display=swap" rel="stylesheet">

    <style>
        * {
            box-sizing: border-box;
        }

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
            z-index: -1;
        }

        /* ===== CARD WRAPPER ===== */
        #wrapper {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 52vw;
            height: 33vw;
        }

        /* ===== CARD ===== */
        #card {
            width: 100%;
            height: 100%;
            background: #faefcf;
            border: 2px solid #000;
            box-shadow: 0 12px 30px rgba(0,0,0,0.4);
            position: relative;
        }

        /* ===== PHOTO BOX ===== */
        .photo-box {
            position: absolute;
            top: 4vw;
            left: 3vw;
            width: 18vw;
            height: 22vw;
            border: 2px solid #000;
            background: rgba(255,255,255,0.6);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.6vw;
            cursor: pointer;
        }

        .photo-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* ===== INPUT STYLE ===== */
        .handwriting {
            font-family: 'Nanum Pen Script', cursive;
            background: transparent;
            border: none;
            outline: none;
            text-align: center;
            color: #000;
            width: 18vw;
        }

        #call-me {
            position: absolute;
            top: 6vw;
            right: 3vw;
            font-size: 2.2vw;
        }

        #three-words {
            position: absolute;
            top: 10vw;
            right: 3vw;
            font-size: 2vw;
        }

        #future-self {
            position: absolute;
            top: 14vw;
            right: 3vw;
            font-size: 1.7vw;
            resize: none;
            height: 6vw;
        }

        .signature {
            position: absolute;
            bottom: 3vw;
            right: 3vw;
            font-family: 'Nanum Pen Script', cursive;
            font-size: 1.8vw;
        }

        /* ===== MOBILE ===== */
        @media (max-width: 900px) {
            #wrapper {
                width: 90vw;
                height: 57vw;
            }

            .photo-box {
                width: 30vw;
                height: 36vw;
                font-size: 4vw;
            }

            .handwriting {
                width: 40vw;
            }

            #call-me {
                font-size: 4vw;
            }

            #three-words {
                font-size: 3.6vw;
            }

            #future-self {
                font-size: 3.2vw;
            }

            .signature {
                font-size: 3.4vw;
            }
        }
    </style>
</head>

<body>
    <div id="background"></div>

    <div id="wrapper">
        <div id="card">

            <!-- PHOTO -->
            <label class="photo-box">
                <input type="file" accept="image/*" hidden onchange="loadPhoto(event)">
                Click to add photo
            </label>

            <!-- TEXT -->
            <input id="call-me" class="handwriting" placeholder="You can call me">

            <input id="three-words" class="handwriting" placeholder="3 words describe me">

            <textarea id="future-self" class="handwriting"
                placeholder="To my future self"></textarea>

            <div class="signature">Signature</div>

        </div>
    </div>

    <script>
        function loadPhoto(event) {
            const box = document.querySelector('.photo-box');
            box.innerHTML = '';
            const img = document.createElement('img');
            img.src = URL.createObjectURL(event.target.files[0]);
            box.appendChild(img);
        }
    </script>
</body>
</html>
