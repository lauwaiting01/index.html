<!DOCTYPE html>
<html lang="zh-Hant-HK">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>九九乘法雙人選擇賽 - 升級版</title>
    <style>
        :root {
            --p1-color: #4a90e2;
            --p2-color: #e91e63;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f2f5;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            user-select: none;
        }
        .container {
            background-color: white;
            border-radius: 16px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.1);
            padding: 30px;
            width: 100%;
            max-width: 800px;
            text-align: center;
        }
        h1 { color: #333; margin-bottom: 30px; }
        .screen { display: none; }
        .active { display: block; }
        
        /* 首頁樣式 */
        .btn-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }
        button {
            background-color: #4caf50;
            color: white;
            border: none;
            padding: 15px 20px;
            font-size: 18px;
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.1s, background-color 0.2s;
        }
        button:hover { background-color: #45a049; transform: scale(1.03); }
        button:active { transform: scale(0.98); }
        .btn-all { grid-column: span 3; background-color: #ff9800; }
        .btn-all:hover { background-color: #e68a00; }
        
        /* 遊戲畫面樣式 */
        .status-bar {
            display: flex;
            justify-content: space-between;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #eee;
        }
        
        /* 題目盒子與轉換動畫 */
        .question-container {
            overflow: hidden;
            margin: 30px 0;
            background: #f7f9fa;
            border-radius: 12px;
            padding: 25px;
            height: 80px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .question-box {
            font-size: 56px;
            font-weight: bold;
            color: #222;
            transition: transform 0.2s ease-out, opacity 0.2s ease-out;
        }
        
        /* 數字跳動/切換時的效果 */
        .rolling {
            animation: rollEffect 0.1s infinite alternate;
            color: #888;
            filter: blur(1px);
        }
        .pop-in {
            animation: popInEffect 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        @keyframes rollEffect {
            0% { transform: translateY(-5px) scale(0.95); }
            100% { transform: translateY(5px) scale(1.05); }
        }
        @keyframes popInEffect {
            0% { transform: scale(0.5); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

        .player-zones {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        .player-zone {
            padding: 20px;
            border-radius: 12px;
            border: 3px solid #ccc;
            background-color: #fafafa;
        }
        .p1-zone { border-color: var(--p1-color); }
        .p2-zone { border-color: var(--p2-color); }
        .p1-zone h3 { color: var(--p1-color); margin-top: 0; }
        .p2-zone h3 { color: var(--p2-color); margin-top: 0; }
        .score-display { font-size: 24px; font-weight: bold; margin-bottom: 20px; color: #333; }
        
        /* 選擇題按鈕樣式 */
        .options-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }
        .option-btn {
            padding: 18px 10px;
            font-size: 22px;
            font-weight: bold;
            border-radius: 10px;
            border: 2px solid #ddd;
            background-color: white;
            color: #333;
            transition: all 0.1s;
        }
        .p1-zone .option-btn { border-color: var(--p1-color); }
        .p1-zone .option-btn:not(:disabled):hover { background-color: var(--p1-color); color: white; }
        .p2-zone .option-btn { border-color: var(--p2-color); }
        .p2-zone .option-btn:not(:disabled):hover { background-color: var(--p2-color); color: white; }
        
        /* 回饋樣式 */
        .option-btn.correct { background-color: #4caf50 !important; color: white !important; border-color: #4caf50 !important; transform: scale(1.05); }
        .option-btn.wrong { background-color: #f44336 !important; color: white !important; border-color: #f44336 !important; opacity: 0.4; transform: scale(0.95); }
        
        /* 結算畫面樣式 */
        .winner-text { font-size: 32px; font-weight: bold; margin: 30px 0; color: #4caf50; }
        .final-scores { font-size: 22px; margin-bottom: 40px; line-height: 1.6; }
        .btn-home { background-color: #2196f3; width: 100%; padding: 15px; }
        .btn-home:hover { background-color: #0b7dda; }
    </style>
</head>
<body>

<div class="container">
    <!-- 1. 首頁：選擇乘法表 -->
    <div id="home-screen" class="screen active">
        <h1>九九乘法雙人選擇賽</h1>
        <p style="color: #666; margin-bottom: 20px;">請選擇要挑戰的乘法範圍：</p>
        <div class="btn-grid">
            <button onclick="startGame(2)">2 階</button>
            <button onclick="startGame(3)">3 階</button>
            <button onclick="startGame(4)">4 階</button>
            <button onclick="startGame(5)">5 階</button>
            <button onclick="startGame(6)">6 階</button>
            <button onclick="startGame(7)">7 階</button>
            <button onclick="startGame(8)">8 階</button>
            <button onclick="startGame(9)">9 階</button>
            <button class="btn-all" onclick="startGame('all')">2-9 全部隨機混合</button>
        </div>
    </div>

    <!-- 2. 遊戲進行畫面 -->
    <div id="game-screen" class="screen">
        <div class="status-bar">
            <span id="current-mode-text">模式</span>
            <span id="round-text">第 1 / 10 題</span>
        </div>
        
        <div class="question-container">
            <div class="question-box" id="question-display">5 × 5 = ?</div>
        </div>
        
        <div class="player-zones">
            <!-- 玩家 1 -->
            <div class="player-zone p1-zone">
                <h3>玩家 1 (藍)</h3>
                <div class="score-display">得分: <span id="p1-score">0</span></div>
                <div class="options-grid" id="p1-options"></div>
            </div>
            <!-- 玩家 2 -->
            <div class="player-zone p2-zone">
                <h3>玩家 2 (紅)</h3>
                <div class="score-display">得分: <span id="p2-score">0</span></div>
                <div class="options-grid" id="p2-options"></div>
            </div>
        </div>
    </div>

    <!-- 3. 結算畫面 -->
    <div id="result-screen" class="screen">
        <h1>比賽結束！</h1>
        <div class="winner-text" id="winner-display">恭喜 玩家 1 獲勝！</div>
        <div class="final-scores">
            <p>玩家 1 最終得分：<span id="final-p1-score" style="color:var(--p1-color); font-weight:bold;">0</span> 分</p>
            <p>玩家 2 最終得分：<span id="final-p2-score" style="color:var(--p2-color); font-weight:bold;">0</span> 分</p>
        </div>
        <button class="btn-home" onclick="goHome()">返回首頁</button>
    </div>
</div>

<script>
    let currentMode = 2; 
    let currentRound = 1;
    const totalRounds = 10;
    let p1Score = 0;
    let p2Score = 0;
    let correctAnswer = 0;
    let roundActive = false;

    function switchScreen(screenId) {
        document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
        document.getElementById(screenId).classList.add('active');
    }

    function startGame(mode) {
        currentMode = mode;
        currentRound = 1;
        p1Score = 0;
        p2Score = 0;
        
        document.getElementById('p1-score').innerText = p1Score;
        document.getElementById('p2-score').innerText = p2Score;
        document.getElementById('current-mode-text').innerText = mode === 'all' ? "模式: 2-9全部" : `模式: ${mode} 階`;
        
        switchScreen('game-screen');
        generateQuestion();
    }

    function generateQuestion() {
        roundActive = false; // 動畫期間不可答題
        let num1, num2;
        
        if (currentMode === 'all') {
            num1 = Math.floor(Math.random() * 8) + 2; 
            num2 = Math.floor(Math.random() * 8) + 2; 
        } else {
            num1 = currentMode;
            num2 = Math.floor(Math.random() * 8) + 2; 
            if(Math.random() > 0.5) {
                let temp = num1; num1 = num2; num2 = temp;
            }
        }
        
        correctAnswer = num1 * num2;
        
        // 生成干擾答案
        let optionsSet = new Set([correctAnswer]);
        while(optionsSet.size < 4) {
            let offset = (Math.floor(Math.random() * 7) - 3) * (Math.random() > 0.5 ? 1 : num1);
            let wrongAns = correctAnswer + offset;
            if(wrongAns > 0 && wrongAns !== correctAnswer) {
                optionsSet.add(wrongAns);
            }
        }
        
        // 核心修改：兩邊的選項與順序完全各自獨立隨機打亂
        let optionsArray = Array.from(optionsSet);
        let p1Options = [...optionsArray].sort(() => Math.random() - 0.5);
        let p2Options = [...optionsArray].sort(() => Math.random() - 0.5);
        
        // 先渲染出空的或預備按鈕，但不允許點擊
        renderOptions(1, p1Options, true);
        renderOptions(2, p2Options, true);

        // 執行數字轉變滾動效果
        const qDisplay = document.getElementById('question-display');
        qDisplay.className = 'question-box rolling';
        document.getElementById('round-text').innerText = `第 ${currentRound} / ${totalRounds} 題`;
        
        let rollCount = 0;
        let rollInterval = setInterval(() => {
            let tempNum1 = Math.floor(Math.random() * 8) + 2;
            let tempNum2 = Math.floor(Math.random() * 8) + 2;
            qDisplay.innerText = `${tempNum1} × ${tempNum2} = ?`;
            rollCount++;
            
            if(rollCount > 8) {
                clearInterval(rollInterval);
                // 顯示真正題目並加入彈出效果
                qDisplay.innerText = `${num1} × ${num2} = ?`;
                qDisplay.className = 'question-box pop-in';
                
                // 啟用按鈕點擊
                renderOptions(1, p1Options, false);
                renderOptions(2, p2Options, false);
                roundActive = true;
            }
        }, 60);
    }

    function renderOptions(playerNum, options, isDisabled) {
        const container = document.getElementById(`p${playerNum}-options`);
        container.innerHTML = ''; 
        
        options.forEach(val => {
            const btn = document.createElement('button');
            btn.className = 'option-btn';
            btn.innerText = val;
            btn.disabled = isDisabled;
            btn.onclick = () => handleChoice(playerNum, val, btn);
            container.appendChild(btn);
        });
    }

    function handleChoice(playerNum, chosenValue, clickedBtn) {
        if (!roundActive) return;

        if (chosenValue === correctAnswer) {
            roundActive = false; 
            clickedBtn.classList.add('correct');
            
            // 答對加分
            if (playerNum === 1) {
                p1Score += 10;
                document.getElementById('p1-score').innerText = p1Score;
            } else {
                p2Score += 10;
                document.getElementById('p2-score').innerText = p2Score;
            }
            
            setTimeout(() => {
                nextRound();
            }, 600);
        } else {
            // 答錯鎖定單個按鈕
            clickedBtn.classList.add('wrong');
            clickedBtn.disabled = true;
        }
    }

    function nextRound() {
        if (currentRound < totalRounds) {
            currentRound++;
            generateQuestion();
        } else {
            endGame();
        }
    }

    function endGame() {
        switchScreen('result-screen');
        
        document.getElementById('final-p1-score').innerText = p1Score;
        document.getElementById('final-p2-score').innerText = p2Score;
        
        const winnerDisplay = document.getElementById('winner-display');
        if (p1Score > p2Score) {
            winnerDisplay.innerText = "🏆 恭喜 玩家 1 (藍) 獲得勝利！";
            winnerDisplay.style.color = "var(--p1-color)";
        } else if (p2Score > p1Score) {
            winnerDisplay.innerText = "🏆 恭喜 玩家 2 (紅) 獲得勝利！";
            winnerDisplay.style.color = "var(--p2-color)";
        } else {
            winnerDisplay.innerText = "🤝 兩位旗鼓相當，平手！";
            winnerDisplay.style.color = "#666";
        }
    }

    function goHome() {
        switchScreen('home-screen');
    }
</script>

</body>
</html>
