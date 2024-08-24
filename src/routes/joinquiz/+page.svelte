<style>
  #quiz-container {
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      text-align: center;
      max-width: 500px;
      width: 100%;
  }

  h3 {
      margin-bottom: 15px;
      color: #333;
  }

  p {
      margin-bottom: 10px;
      color: #555;
  }

  div {
      margin-bottom: 10px;
  }

  .option-box {
      display: inline-block;
      background-color: #4caf50;
      color: #fff;
      border: 2px solid #4caf50;
      border-radius: 5px;
      padding: 10px 20px;
      cursor: pointer;
      transition: background-color 0.3s;
      margin-right: 10px;
  }

  .option-box:hover {
      background-color: #118617;
  }

  .score {
      font-weight: bold;
      color: #4caf50;
  }

  button {
      background-color: darkgreen;
      color: #fff;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
  }

  button:hover {
      background-color: #1ca923;
  }
</style>

<script>
  let currentQuestionIndex = 0;
  const questions = [
      {
          question: 'What is the capital of France?',
          options: ['Paris', 'London', 'Berlin', 'Rome'],
          answer: 'Paris'
      },
      {
          question: 'What is 2 + 2?',
          options: ['3', '4', '5', '6'],
          answer: '4'
      },
      // Add more questions here...
  ];
  let userAnswer = null;
  let showResult = false;
  let score = 0; // Initialize the score variable

  function checkAnswer() {
      const currentQuestion = questions[currentQuestionIndex];

      if (userAnswer === null) {
          alert('Please select an answer before submitting.');
          return;
      }

      if (userAnswer === currentQuestion.answer) {
          alert('Correct!');
          score++; // Increment the score for correct answers
      } else {
          alert('Incorrect. The correct answer is: ' + currentQuestion.answer);
      }

      currentQuestionIndex++;

      if (currentQuestionIndex < questions.length) {
          userAnswer = null; // Reset user's answer for the next question
      } else {
          showResult = true; // Display congratulations message when all questions are answered
      }
  }
</script>

<div id="quiz-container">
  {#if currentQuestionIndex < questions.length}
      <h3>{questions[currentQuestionIndex].question}</h3>
      <p class="score">Score: {score}/{currentQuestionIndex}</p> <!-- Display the current score -->
      {#each questions[currentQuestionIndex].options as option, index}
          <div class="option-box" on:click={() => userAnswer = option}>
              {String.fromCharCode(65 + index)}. {option}
          </div>
      {/each}
      <button on:click={checkAnswer}>Submit</button>
  {:else}
      {#if showResult}
          <p class="score">Congratulations! You have completed the quiz.</p>
          <p class="score">Final Score: {score}/{questions.length}</p> <!-- Display the final score -->
      {/if}
  {/if}
</div>
