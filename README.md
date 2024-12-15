<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Love Q&A</title>
    <style>
        body {
            background-color: #ffc0cb;
            font-family: "Brush Script MT", cursive;
            text-align: center;
            padding: 50px;
            color: #333;
            animation: fadeIn 2s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        button {
            padding: 10px 20px;
            background-color: #ff6f91;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.2em;
            cursor: pointer;
            animation: pop 0.5s infinite alternate;
        }

        @keyframes pop {
            from { transform: scale(1); }
            to { transform: scale(1.1); }
        }

        button:hover {
            background-color: #ff497a;
        }

        .gif {
            max-width: 80%;
            height: auto;
            margin: 20px auto;
        }

        .message {
            margin-top: 30px;
            font-size: 1.5em;
            animation: fadeInMessage 2s ease-in-out;
        }

        @keyframes fadeInMessage {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
    <h1>Do you love me?</h1>
    <button onclick="askLove()">Yes</button>
    <button onclick="askAgain()">No</button>

    <div id="content"></div>

    <script>
        function askLove() {
            document.getElementById("content").innerHTML = `
                <h1>Am I the girl you love the most?</h1>
                <button onclick="loveMostYes()">Yes</button>
                <button onclick="loveMostNo()">No</button>
            `;
        }

        function askAgain() {
            document.getElementById("content").innerHTML = "<h1>Keep thinking... Do you really not love me? 💔</h1>";
        }

        function loveMostYes() {
            document.getElementById("content").innerHTML = `
                <img src="https://media.tenor.com/1VDIVkm5tM8AAAAC/wriorinde-wriolinde.gif" alt="Happy Gif" class="gif">
                <h1>Merry Christmas, I love you! 🎄❤️</h1>
                <img src="https://media.tenor.com/zMbVC2R8gt8AAAAC/snoopy-peanuts.gif" alt="Merry Christmas Gif" class="gif">
                <div class="message">
                    <p>**Merry Christmas, My Love** 🎄❤️</p>
                    <p>Every time I think about us, my heart feels so full I could burst. This Christmas, I just want to say how much you mean to me. You’re not just my boyfriend—you’re my safe place, my home, and my whole world.</p>
                    <p>I love how you’re so dominant yet so gentle and caring with me. The way you always make me feel like I’m your soft spot melts me every time you say it. You’re this strong, confident man, and yet, when it comes to me, you turn into this sweet, loving person who makes me feel like the most special girl in the world.</p>
                    <p>Our little inside jokes, like calling you Furqan Fart Face (which you so graciously accepted 😂), make my day so much better. The way we laugh at the silliest things and have those moments that no one else could ever understand—it’s like we have our own secret language.</p>
                    <p>I wish I could bottle up the way you make me feel because it’s honestly the best thing in the world. Whether it’s watching you sleep on FaceTime (you’re the cutest, even if you snore sometimes) or laughing about our ridiculous jokes, every moment with you is perfect to me.</p>
                    <p>I can’t wait to do so much more with you. Studying together, building our future, and creating the life we’ve dreamed of—it’s all I want. You’re my favorite person in every way, and I’m so lucky to have you.</p>
                    <p>You’re my love, my partner, my everything, and my Furqan Fart Face forever. I love you more than words can ever say, and I’m so excited for all the memories we’re going to make.</p>
                    <p>Merry Christmas, my heart. ❤️ Here’s to us—our love, our laughter, and our happily ever after.</p>
                    <p>Yours always and forever,<br>[Your Name] 💖</p>
                </div>
            `;
        }

        function loveMostNo() {
            document.getElementById("content").innerHTML = `
                <img src="https://media.tenor.com/Q3-IJ4e9lYMAAAAC/mario-sad.gif" alt="Sad Mario Gif" class="gif">
                <h1>Oh no! 💔</h1>
            `;
        }
    </script>
</body>
</html>
