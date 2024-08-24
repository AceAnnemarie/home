<script>
    let leaderboardData = [
      { rank: 1, user: "User1", score: 500 },
      { rank: 2, user: "User2", score: 450 },
      { rank: 3, user: "User3", score: 400 },
      { rank: 4, user: "User4", score: 350 },
      { rank: 5, user: "User5", score: 300 },
    ];
  </script>
  
  <style>
    
    header {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 1em;
    }
  
    .leaderboard-container {
      width: 80%;
      margin: auto;
      background-color: white;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      padding: 20px;
      margin-top: 20px;
      border-radius: 8px;
    }
  
    .leaderboard {
      list-style-type: none;
      padding: 0;
      margin: 0;
    }
  
    .leaderboard-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px;
      border-bottom: 1px solid #ddd;
    }
  
    .rank {
      width: 10%;
    }
  
    .user {
      width: 60%;
    }
  
    .score {
      width: 30%;
      text-align: right;
    }
  </style>
  
  <main>
    <header>
      <h1>Leaderboard</h1>
    </header>
  
    <div class="leaderboard-container">
      <ul class="leaderboard">
        {#each leaderboardData as { rank, user, score }}
          <li class="leaderboard-item">
            <div class="rank">{rank}</div>
            <div class="user">{user}</div>
            <div class="score">{score}</div>
          </li>
        {/each}
      </ul>
    </div>
  </main>