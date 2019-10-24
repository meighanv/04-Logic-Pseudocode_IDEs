# Choose Two additional Programming Projects along with the (Mandatory) one. (Three Total) 

##  Payroll Program with Input Validation


Design a payroll program that prompts the user to enter an employee’s hourly pay rate and the number of hours worked. Validate the user’s input so that only pay rates in the range of $7.50 through $18.25 and hours in the range of 0 through 40 are accepted. The program should display the employee’s gross pay.

## Theater Seating Revenue with Input Validation

A dramatic theater has three seating sections, and it charges the following prices for tickets in each section: section A seats cost $20 each, section B seats cost $15 each, and section C seats cost $10 each. The theater has 300 seats in section A, 500 seats in section B, and 200 seats in section C. Design a program that asks for the number of tickets sold in each section and then displays the amount of income generated from ticket sales. The program should validate the numbers that are entered for each section.

## Fat Gram Calculator

Design a program that asks for the number of fat grams and calories in a food item. Validate the input as follows:

Make sure the number of fat grams and calories is not less than 0.

According to nutritional formulas, the number of calories cannot exceed "fat grams X 9 "

Make sure that the number of calories entered is not greater than "fat grams X 9"

Once correct data has been entered, the program should calculate and display the percentage of calories that come from fat. Use the following formula:

![image](https://user-images.githubusercontent.com/47218880/67504468-0ba93a80-f64f-11e9-85d0-f080ac66a64a.png)

Some nutritionists classify a food as “low fat” if less than 30 percent of its calories come from fat. If the results of this formula are less than 0.3, the program should display a message indicating the food is low in fat.

## Speeding Violation Calculator

Design a program that calculates and displays the number of miles per hour over the speed limit that a speeding driver was doing. The program should ask for the speed limit and the driver’s speed. Validate the input as follows:

The speed limit should be at least 20, but not greater than 70.

The driver’s speed should be at least the value entered for the speed limit ­(otherwise the driver was not speeding).
Once correct data has been entered, the program should calculate and display the number of miles per hour over the speed limit that the driver was doing.
```
module main()
	declare integer speed 
	declare integer limit 
	declare integer excess
	limit = getLimit()
	speed = getSpeed(limit)
	excess = getExcess(speed, limit)
	Display "You were going $ MPH over the $ MPH speed limit", excess, limit
endmodule

function getLimit()
	declare integer limit = 0
	while limit <= 20 OR limit >= 70
		Display "What was the speed limit?"
		input limit
	endWhile
	return limit
endFunction

function integer getSpeed(limit)
	declare integer speed = 0
	while speed <= limit
		Display "How fast were you going?"
		input limit
	endWhile
	return speed
endFunction

function excess(speed,limit)
	return speed - limit
endFunction 

```

# Rock, Paper, Scissors Modification (MANDATORY)

In a previous Programming Exercise option you were asked to design a program that plays the Rock, Paper, Scissors game. In the program, the user enters one of the three strings—"rock", "paper", or "scissors"—at the keyboard. Add input validation (with a case-insensitive comparison) to make sure the user enters one of those strings only.
(If you didnt design one, here is a version of that game program to work with) 

### Program "Rock,Paper,Scissors"

```
// main module
Module main()
// Local variables
Declare Integer computer, player
Declare string selection

// Get computer number
Set computer = Rand(1, 3)

// Get player Selection
Call getSelection(selection)
set player = Call convertSelection(selection)

// Show winner
Call showWinner(computer, player)

End Module

// The getSelection module gets a string with input validation for valid choices then it will return the appropriate integer
Module getSelection(Integer Ref inputAnswer)
		while toupper(inputAnswer) != 'ROCK' OR toupper(inputAnswer) != 'PAPER' OR toupper(inputAnswer) != 'SCISSORS'
			Display "Enter 'rock', 'paper', or 'scissors':"
			Input inputAnswer
		endwhile
End Module

//To convert the choice to an integer
module convertSelection(string inputAnswer)
	declare integer choice 
	select inputAnswer
		case: 'ROCK'
			set choice = 1
		case: 'PAPER'
			set choice = 2
		case: 'SCISSORS'
			set choice = 3
		default:
			set choice = 1
	endSelect
	return choice
endModule


// The showWinner module shows if number is a prime
Module showWinner(Integer computer, player)
Declare Integer which

Display “Computer chose “, whichChoice(computer)
If computer == player Then
	Display “Player made same choice.  Play again.”
Else
Set which = whoWon(computer, player)
If which == 1 Then
		Display “Computer wins.”
Else
If which == 2 Then
			Display “Player wins.”
		Else
			Display “No winner.”
		End If
End If
End If

End Module

// The whichChoice function displays choice 
Function String whichChoice (Integer number)

If number == 1 Then
	Return “rock”
Else
If number == 2 Then
		Return “paper”
	Else
		Return “scissors
	End If

End Function

// The whoWon function selects winner 
Function Integer whoWon(computer, player)
// 1 = rock, 2 = paper, 3 = scissors
// rock smashes scissors
// scissors cuts paper
// paper wraps rock

	// both choose same no winner
If computer == player then
		Return 0
	End If

	// test computer chose rock
	If computer == 1 then
		If player == 2 then
			Return 2  // paper wraps rock
		End If
Else
		If player == 3 then
			Return 1  // rock smashes scissors
		End If
End If

	// test computer chose paper
	If computer == 2 then
		If player == 1 then
			Return 1  // paper wraps rock
		End If
Else
		If player == 3 then
			Return 2  // scissors cuts paper
		End If
End If

	// test computer chose scissors
	If computer == 3 then
		If player == 1 then
			Return 2  // rock smashes scissors 
		End If
Else
		If player == 2 then
			Return 1  // scissors cuts paper
		End If
End If

	Return 0

End Function
```
