# Exercise Workbench
* Design a While loop that lets the user enter a number. The number should be multiplied by 10, and the result stored in a variable named product. The loop should iterate as long as product contains a value less than 100.
```
Declare real num
Display "provide a number less than 100"
input num
while num < 100 do 
   product = num * 10
   Display "$ times 10 is equal to $", num, product
   num += 10
endwhile
```

* Design a Do-While loop that asks the user to enter two numbers. The numbers should be added and the sum displayed. The loop should ask the user whether he or she wishes to perform the operation again. If so, the loop should repeat; otherwise it should terminate.
```
declare real num1, num2
declare string continue = 'y'
do
   Display "Provide a number:"
   input num1 
   Display "Provide another number:"
   input num2

   Display "Would you like to do this again? ('y' or 'Y' for yes)"
while continue == 'y' OR continue == 'Y'
   
```
* Design a For loop that displays the following set of numbers:

0, 10, 20, 30, 40, 50, . . . , 1000

for i=0; 1000; i+=10
   Display "$", i
EndFor

* Design a loop that asks the user to enter a number. The loop should iterate 10 times and keep a running total of the numbers entered.
```
declare real total = 0
declare real num
for i=1; 10; i++
   Display "Please provide a number:"
   input num
   total += num
   Display "Current Total: $", total
endfor
```
* Design a For loop that calculates the total of the following series of numbers:
![image](https://user-images.githubusercontent.com/47218880/67423054-31740800-f599-11e9-9565-031c1f729e1c.png)
```
```

* Design a nested loop that displays 10 rows of # characters. There should be 15 # characters in each row.

* Convert the While loop in the following code to a Do-While loop:
```
Declare Integer x = 1
Do
   Display "Enter a number."
   Input x
While x > 0
```
* Convert the Do-While loop in the following code to a While loop:
```
Declare String sure
While sure != "Y" AND sure != "y"
  Display "Are you sure you want to quit?"
  Input sure
endwhile
```
* Convert the following While loop to a For loop:
```
for count=0; count<50; count++
   Display "The count is ", count
EndFor
```
* Convert the following For loop to a While loop:
```
Declare Integer count
For count = 1 To 50
   Display count
End For
```
