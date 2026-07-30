[code_artifact.html](https://github.com/user-attachments/files/30528165/code_artifact.html)
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>색깔 반응 속도 게임</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { font-family: 'Inter', sans-serif; }
    </style>
</head>
<body class="bg-gray-100 flex flex-col items-center justify-center min-h-screen p-4">

    <div id="game-container" class="bg-white p-8 rounded-2xl shadow-xl w-full max-w-md text-center">
        <h1 class="text-3xl font-bold mb-4">색깔 판별 게임</h1>
        <p class="mb-6 text-gray-600">글자의 <b>색깔</b>이 글자 내용과 일치하면 '예', 아니면 '아니오'를 누르세요!</p>
        
        <div id="color-box" class="text-5xl font-extrabold mb-8 h-24 flex items-center justify-center transition-all duration-200">
            준비 중...
        </div>

        <div class="grid grid-cols-2 gap-4">
            <button onclick="checkAnswer(true)" class="bg-green-500 hover:bg-green-600 text-white font-bold py-4 rounded-xl text-xl transition">예</button>
            <button onclick="checkAnswer(false)" class="bg-red-500 hover:bg-red-600 text-white font-bold py-4 rounded-xl text-xl transition">아니오</button>
        </div>

        <div class="mt-8 text-xl">
            점수: <span id="score" class="font-bold">0</span>
        </div>
    </div>

    <script>
        const colors = [
            { name: '빨강', hex: '#EF4444' },
            { name: '파랑', hex: '#3B82F6' },
            { name: '초록', hex: '#22C55E' },
            { name: '노랑', hex: '#EAB308' }
        ];

        let score = 0;
        let currentMatch = false;

        function nextRound() {
            const wordIdx = Math.floor(Math.random() * colors.length);
            const colorIdx = Math.floor(Math.random() * colors.length);
            
            const box = document.getElementById('color-box');
            box.innerText = colors[wordIdx].name;
            box.style.color = colors[colorIdx].hex;
            
            currentMatch = (wordIdx === colorIdx);
        }

        function checkAnswer(userChoice) {
            if (userChoice === currentMatch) {
                score++;
                document.getElementById('score').innerText = score;
            } else {
                score = Math.max(0, score - 1);
                document.getElementById('score').innerText = score;
            }
            nextRound();
        }

        // Initialize game
        nextRound();
    </script>
</body>
</html>
