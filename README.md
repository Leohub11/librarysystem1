function rollSingleDice() {
  const randomDice = Math.floor(Math.random() * 6) + 1;
  return randomDice;
}

function rollDice() {
  const result1 = rollSingleDice();
  const result2 = rollSingleDice();

  const dice1 = document.getElementById("dice1");
  const dice2 = document.getElementById("dice2");

  // Update dice images
  dice1.src = `dice-${result1}.svg`;
  dice2.src = `dice-${result2}.svg`;

  // Add roll animation class
  dice1.classList.add("roll");
  dice2.classList.add("roll");

  // Remove roll animation class after 500ms
  setTimeout(() => {
    dice1.classList.remove("roll");
    dice2.classList.remove("roll");
  }, 500);
}

// Attach event listener to roll button
const rollButton = document.getElementById("rollButton");
rollButton.addEventListener("click", rollDice);
