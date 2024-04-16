<!-- Add this to your GitHub profile README.md -->

### Let's play a game!

I've created a simple "Guess the Number" game using JavaScript. Can you guess the correct number between 1 and 100?

Click the button below to start the game!

<button onclick="startGame()">Start Game</button>

<script>
// Generate a random number between 1 and 100
const randomNumber = Math.floor(Math.random() * 100) + 1;

// Function to start the game
function startGame() {
    const userGuess = prompt("I'm thinking of a number between 1 and 100. What is your guess?");

    // Convert user's guess to a number
    const guess = parseInt(userGuess);

    // Check if the guess is correct
    if (guess === randomNumber) {
        alert("Congratulations! You guessed the correct number!");
    } else {
        let message = guess > randomNumber ? "Too high! Try again." : "Too low! Try again.";
        alert(message);
    }
}
</script>

