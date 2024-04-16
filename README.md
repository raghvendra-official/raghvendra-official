function playRockPaperScissors() {
  const choices = ["rock", "paper", "scissors"];
  const computerChoice = choices[Math.floor(Math.random() * choices.length)];
  let playerChoice = prompt("Enter your choice (rock, paper, scissors): ").toLowerCase();

  while (!choices.includes(playerChoice)) {
    playerChoice = prompt("Invalid choice. Enter rock, paper, or scissors: ").toLowerCase();
  }

  if (playerChoice === computerChoice) {
    console.log("It's a tie!");
  } else if ((playerChoice === "rock" && computerChoice === "scissors") ||
             (playerChoice === "paper" && computerChoice === "rock") ||
             (playerChoice === "scissors" && computerChoice === "paper")) {
    console.log("You win!");
  } else {
    console.log("You lose!");
  }
}

playRockPaperScissors();
