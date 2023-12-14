# MagicBall
git init
git add .
git commit -m "Перший коміт: Додано магічний шар предсказань"
git remote add origin https://github.com/Hyakkimary/magic-8-ball.git
git push -u origin master

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Магічний Шар Предсказань</title>
    <style>
        body {
            background-image: url(/Users/HomePC/Desktop/Magic%20ball/Space.jpg);
            background-size: cover;
            background-position: center;
            color: black;
            font-family: Arial, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            flex-direction: column;
        }

        #question {
            margin-bottom: 20px;
            padding: 5px;
            width: 80%;
            box-sizing: border-box;
        }

        #magicBall {
            width: 600px;
            height: 600px;
            background-image: url(/Users/HomePC/Desktop/Magic%20ball/Magic-Ball.png);
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            text-align: center;
            cursor: pointer;
        }

        #answer {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div id="question">
        <p>Задайте своє питання магічному шару</p>
        <input type="text" id="userQuestion" placeholder="Ваше питання...">
    </div>

    <div id="magicBall" onclick="shakeMagicBall()">
        <p id="answer"></p>
    </div>

    <script>
        const answers = [
            "Безперспективно",
            "Так",
            "Ні",
            "Спробуйте пізніше",
            "Це велика можливість",
            "Важко сказати",
        ];

        function getRandomAnswer() {
            const randomIndex = Math.floor(Math.random() * answers.length);
            return answers[randomIndex];
        }

        function shakeMagicBall() {
            const question = document.getElementById("userQuestion").value;
            const answer = getRandomAnswer();

            document.getElementById("answer").innerText = `Питання: ${question}\nВідповідь: ${answer}`;
        }
    </script>
</body>
</html>
