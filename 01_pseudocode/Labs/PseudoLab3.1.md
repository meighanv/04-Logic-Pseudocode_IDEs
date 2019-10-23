1. Design an If-Then statement (or a flowchart with a single alternative decision structure) that assigns 20 to the variable y and assigns 40 to the variable z if the variable x is greater than 100.
```
if x > 100 then 
   y = 20
   z = 40
```  

2. Design an If-Then statement (or a flowchart with a single alternative decision structure) that assigns 0 to the variable b and assigns 1 to the variable c if the variable a is less than 10.
```
if a < 10 then
   b = 0
   c = 1
```  

3. Design an If-Then-Else statement (or a flowchart with a dual alternative decision structure) that assigns 0 to the variable b if the variable a is less than 10. Otherwise, it should assign 99 to the variable b.
```
if a < 10 then
   b = 0 
else
   b = 99
```

4. The following pseudocode contains several nested If-Then-Else statements. Unfortunately, it was written without proper alignment and indentation. Rewrite the code and use the proper conventions of alignment and indentation.
```
If score < 60 Then
<<<<<<< HEAD
   Display "Your grade is F."
   Else
      If score < 70 Then
         Display "Your grade is D."
         Else
            If score < 80 Then
               Display "Your grade is C."
               Else
                  If score < 90 Then
                     Display "Your grade is B."
                     Else
                        Display "Your grade is A."
                  End If
            End If
      End If
End If
```
5. Design nested decision structures that perform the following: If amount1 is greater than 10 and amount2 is less than 100, display the greater of amount1 and amount2.
```
if amount 1 > 10 AND amount2 < 100 then
   if amount1 > amount2 then
      Display amount1
      else
         if amount2 > amount1 then
            Display amount2
         endif
   endif
   else
      break
endif
```

6. Rewrite the following If-Then-Else If statement as a Select Case statement.
```
case selection
   1: Display "You selected A."
   2: Display "You selected 2."
   3: Display "You selected 3."
   4: Display "You selected 4."
   default: Display "Not good with numbers, eh?"
endcase
```
7. Design an If-Then-Else statement (or a flowchart with a dual alternative decision structure) that displays “Speed is normal” if the speed variable is within the range of 24 to 56. If speed holds a value outside this range, display “Speed is abnormal.”
```
if speed >= 24 and speed <= 56 then 
   Display "Speed is normal"
   else 
      Display "Speed abnormal"
endif
```
8. Design an If-Then-Else statement (or a flowchart with a dual alternative decision structure) that determines whether the points variable is outside the range of 9 to 51. If the variable holds a value outside this range it should display “Invalid points.” Otherwise, it should display “Valid points.”
```
If points >= 9 and points <= 51 then
   Display "Valid points"
   else 
      Display "Invalid points"
endif
```
=======
Display "Your grade is F."
Else
If score < 70 Then
Display "Your grade is D."
Else
If score < 80 Then
Display "Your grade is C."
Else
If score < 90 Then
Display "Your grade is B."
Else
Display "Your grade is A."
End If
End If
End If
End If
```
5. Design nested decision structures that perform the following: If amount1 is greater than 10 and amount2 is less than 100, display the greater of amount1 and amount2.

6. Rewrite the following If-Then-Else If statement as a Select Case statement.
```
If selection == 1 Then
   Display "You selected A."
Else If selection == 2 Then
   Display "You selected 2."
Else If selection == 3 Then
   Display "You selected 3."
Else If selection == 4 Then
   Display "You selected 4."
Else
   Display "Not good with numbers, eh?"
End If
```
7. Design an If-Then-Else statement (or a flowchart with a dual alternative decision structure) that displays “Speed is normal” if the speed variable is within the range of 24 to 56. If speed holds a value outside this range, display “Speed is abnormal.”

8. Design an If-Then-Else statement (or a flowchart with a dual alternative decision structure) that determines whether the points variable is outside the range of 9 to 51. If the variable holds a value outside this range it should display “Invalid points.” Otherwise, it should display “Valid points.”

>>>>>>> upstream/master
9. Design a case structure that tests the month variable and does the following:

* If the month variable is set to 1, it displays “January has 31 days.”

* If the month variable is set to 2, it displays “February has 28 days.”

* If the month variable is set to 3, it displays “March has 31 days.”

* If the month variable is set to anything else, it displays “Invalid selection.”
<<<<<<< HEAD
```
case month
   1: Display “January has 31 days.”
   2: Display “February has 28 days.”
   3: Display “March has 31 days.”
   default: Display “Invalid selection.”
endcase
```
10. Write an If-Then statement that sets the variable hours to 10 when the flag variable minimum is set.

```
if minimum then
   hours = 10
endif
```
=======

10. Write an If-Then statement that sets the variable hours to 10 when the flag variable minimum is set.

>>>>>>> upstream/master
