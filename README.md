function rollSingleDice() { const randomDice = Math.floor(Math.random() * 6) + 1; return randomDice; }

function rollDice() { 
     const result1 = rollSingleDice(); 
     const result2 = rollSingleDice();

document.getElementById("dice1").src = `dice-${result1}.svg`;
document.getElementById("dice2").src = `dice-${result2}.svg`;

dice1.classList.add("roll"); dice2.classList.add("roll");

setTimeout(() => { 
    dice1.classList.remove("roll"); dice2.classList.remove("roll"); }, 500); 
}

rollButton.addEventListener('click', rollDice);
