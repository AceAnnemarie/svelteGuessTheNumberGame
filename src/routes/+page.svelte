<script>
	let randomNumber = Math.floor(Math.random() * 10) + 1;
	let userGuess = '';
	let message = '';
  
	function checkGuess() {
  const guess = parseInt(userGuess);

  switch (true) {
    case isNaN(guess):
      message = 'Please enter a valid number.';
      break;
    case guess === randomNumber:
      message = 'Congratulations! You guessed the correct number!';
      break;
    case guess < randomNumber:
      message = 'Too low! Try a higher number.';
      break;
    default:
      message = 'Too high! Try a lower number.';
  }
}

  </script>
  
  <main>
	<h1>Guess the Number Game</h1>
	<p>Guess a number between 1 and 10:</p>
	<input type="text" bind:value={userGuess} placeholder="Enter your guess">
	<button on:click={checkGuess}>Check</button>
	<p>{message}</p>
  </main>
  
  <style>
	main {
	  text-align: center;
	  background-color: #f0f0f0;
	  padding: 20px;
	  border-radius: 10px;
	  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
	}
  
	input {
	  padding: 8px;
	  margin: 10px 0;
	}
  
	button {
	  padding: 10px;
	  cursor: pointer;
	}
  </style>
  