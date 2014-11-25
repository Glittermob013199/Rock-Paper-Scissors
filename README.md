Rock-Paper-Scissors
===================

Simple looping rock paper scissors game
var userChoice = prompt("Do you choose rock, paper or scissors?");
function computerDecider() {
var computerChoice = Math.random();
if (computerChoice < 0.34) {
	computerChoice = "rock";
} else if(computerChoice <= 0.67 && computerChoice >= 0.34 ) {
	computerChoice = "paper";
} else {
	computerChoice = "scissors";
} console.log("Computer: " + computerChoice);
return computerChoice;
}

var compare = function(choice1, choice2) {
    if(choice1 === choice2) {
        userChoice = prompt ("It's a tie! Let's play again?")
        compare(userChoice, computerDecider());
    }
    
    else if(choice1 === "rock") {
        
        if(choice2 === "scissors") {
            userChoice = prompt ("rock wins! Let's play again?")
        compare(userChoice, computerDecider());
        }
        else{
            userChoice = prompt ("Paper wins! Let's play again?")
        compare(userChoice, computerDecider());
        }
    }
    else if(choice1 === "paper"){
        if(choice2 === "rock") {
            userChoice = prompt ("Paper wins! Let's play again?")
        compare(userChoice, computerDecider());
        } else {
            userChoice = prompt ("scissors wins! Let's play again?")
        compare(userChoice, computerDecider());
        }
    }
    else if(choice1 === "scissors") {
        if(choice2 === "rock") {
            userChoice = prompt ("rock wins! Let's play again?")
        compare(userChoice, computerDecider());
        } else {
            userChoice = prompt ("Scissors wins! Let's play again?")
        compare(userChoice, computerDecider());
        }
    }
};

compare(userChoice, computerDecider())
