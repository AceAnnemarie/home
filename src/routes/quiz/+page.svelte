<script>
    let activeTab = 'startQuiz';
  
    function openTab(tabName) {
      activeTab = tabName;
    }
  </script>
  
  <style>
    .tab-button {
      background-color: #4CAF50;
      color: white;
      padding: 10px 20px;
      border: none;
      cursor: pointer;
    }
  
    .tab {
      display: none;
    }
  
    .tab.active {
      display: block;
    }
  </style>
  
  <body>
    <button class="tab-button"><a href="#" onclick="openTab('startQuiz')">Create Quiz</a></button>
    <button class="tab-button"><a href="/joinquiz">Join Game</a></button>

    <div class="tab {activeTab === 'startQuiz' ? 'active' : ''}">
    </div>

    <div class="tab {activeTab === 'joinGame' ? 'active' : ''}">
    </div>
</body>
  