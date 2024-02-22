<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>与AI助手交互的五子棋游戏</title>
  <style>
    /* 样式代码 */
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #f0f0f0;
    }
    #board {
      display: grid;
      grid-template-columns: repeat(15, 40px);
      grid-template-rows: repeat(15, 40px);
      gap: 1px;
    }
    .cell {
      width: 40px;
      height: 40px;
      border: 1px solid #000;
      background-color: #ccc;
    }
    .black {
      background-color: #000;
      border-radius: 50%;
    }
    .white {
      background-color: #fff;
      border-radius: 50%;
    }
  </style>
</head>
<body>

<div id="board"></div>

<script>
  const board = document.getElementById('board');
  let currentPlayer = 'black';
  let gameOver = false;

  // 创建棋盘
  for (let i = 0; i < 15; i++) {
    for (let j = 0; j < 15; j++) {
      const cell = document.createElement('div');
      cell.className = 'cell';
      cell.dataset.row = i;
      cell.dataset.col = j;
      cell.addEventListener('click', handleClick);
      board.appendChild(cell);
    }
  }

  // 处理点击事件
  function handleClick() {
    if (gameOver) return;
    if (this.classList.contains('black') || this.classList.contains('white')) return;
    
    const row = parseInt(this.dataset.row);
    const col = parseInt(this.dataset.col);
    this.classList.add(currentPlayer);

    if (checkWinner(row, col)) {
      alert(currentPlayer === 'black' ? '黑棋获胜！' : '白棋获胜！');
      gameOver = true;
      return;
    }

    currentPlayer = currentPlayer === 'black' ? 'white' : 'black';

    // 调用AI助手
    callAI();
  }

  // 调用AI助手
  function callAI() {
    const currentBoardState = getCurrentBoardState();
    // 这里替换为您的API密钥
    const api_key = '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';
    const url = 'https://api.openai.com/v1/ai/move';
    fetch(url, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'Authorization': `Bearer ${api_key}`
      },
      body: JSON.stringify({
        player: currentPlayer,
        board: currentBoardState
      })
    })
    .then(response => response.json())
    .then(data => {
      const aiMove = data.move;
      const aiCell = document.querySelector(`.cell[data-row='${aiMove.row}'][data-col='${aiMove.col}']`);
      aiCell.click(); // AI助手落子
    })
    .catch(error => {
      console.error('Error:', error);
    });
  }

  // 获取当前棋盘状态
  function getCurrentBoardState() {
    const cells = document.querySelectorAll('.cell');
    let boardState = '';
    cells.forEach(cell => {
      if (cell.classList.contains('black')) {
        boardState += 'B';
      } else if (cell.classList.contains('white')) {
        boardState += 'W';
      } else {
        boardState += '-';
      }
    });
    return boardState;
  }

  // 检查是否有玩家获胜
 // 检查是否有玩家获胜
function checkWinner(row, col) {
  const directions = [[1, 0], [0, 1], [1, 1], [1, -1]]; // 检查的四个方向：竖直、水平、对角线（正斜线、反斜线）
  for (const [dx, dy] of directions) {
    let count = 1;
    for (let step = 1; step < 5; step++) {
      const newRow = row + step * dx;
      const newCol = col + step * dy;
      const cell = document.querySelector(`.cell[data-row='${newRow}'][data-col='${newCol}']`);
      if (cell && cell.classList.contains(currentPlayer)) {
        count++;
      } else {
        break;
      }
    }
    for (let step = 1; step < 5; step++) {
      const newRow = row - step * dx;
      const newCol = col - step * dy;
      const cell = document.querySelector(`.cell[data-row='${newRow}'][data-col='${newCol}']`);
      if (cell && cell.classList.contains(currentPlayer)) {
        count++;
      } else {
        break;
      }
    }
    if (count >= 5) {
      return true; // 找到获胜的连续棋子
    }
  }
  return false; // 没有找到获胜的情况
}

</script>

</body>
</html>
