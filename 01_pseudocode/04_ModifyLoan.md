<<<<<<< HEAD
# Using the If-Then-Else Statement

Chris owns an auto repair business and has several employees. If an employee works over 40 hours in a week, Chris pays that employee 1.5 times his or her regular hourly pay rate for all hours over 40. Chris has asked you to design a simple payroll program that calculates an employee’s gross pay, including any overtime wages. You design the following algorithm:
```
Get the number of hours worked.

Get the hourly pay rate.

If the employee worked more than 40 hours, calculate the gross pay with overtime. Otherwise, calculate the gross pay as usual.

Display the gross pay.
```
You go through the top-down design process and create the hierarchy chart shown in Figure 4-10. As shown in the hierarchy chart, the main module will call four other modules. The following are summaries of those modules:
![image](https://user-images.githubusercontent.com/47218880/67346573-d0025980-f504-11e9-9bfa-311f7c3c4a9a.png)
Figure 4-10 Hierarchy chart

```
getHoursWorked—This module will ask the user to enter the number of hours worked.

getPayRate—This module will ask the user to enter the hourly pay rate.

calcPayWithOT—This module will calculate an employee’s pay with overtime.

calcRegularPay—This module will calculate the gross pay for an employee with no overtime.
```
The main module, which executes when the program is run, will call these modules and then display the gross pay. The pseudocode for the program is shown in Program 4-2. Figures 4-11 and 4-12 show flowcharts for each of the modules.

![image](https://user-images.githubusercontent.com/47218880/67346613-ef998200-f504-11e9-9796-d92fb0f25d46.png)

Figure 4-11 Flowchart for the main module

![image](https://user-images.githubusercontent.com/47218880/67346685-2a031f00-f505-11e9-8755-9743ff8ac8b3.png)

Figure 4-12 Flowcharts for the other modules

## Program 4-2
```
 1  // Global constants
 2  Constant Integer BASE_HOURS = 40
 3  Constant Real OT_MULTIPLIER = 1.5
 4
 5  Module main()
 6     // Local variables
 7     Declare Real hoursWorked, payRate, grossPay
 8
 9     // Get the number of hours worked.
10     Call getHoursWorked(hoursWorked)
11
12     // Get the hourly pay rate.
13     Call getPayRate(payRate)
14
15     // Calculate the gross pay.
16     If hoursWorked > BASE_HOURS Then
17        Call calcPayWithOT(hoursWorked, payRate,
18                          grossPay)
19     Else
20        Call calcRegularPay(hoursWorked, payRate,
21                           grossPay)
22     End If
23
24     // Display the gross pay.
25     Display "The gross pay is $", grossPay
26  End Module
27
28  // The getHoursWorked module gets the number
29  // of hours worked and stores it in the
30  // hours parameter.
31  Module getHoursWorked(Real Ref hours)
32     Display "Enter the number of hours worked."
33     Input hours
34  End Module
35
36  // The getPayRate module gets the hourly
37  // pay rate and stores it in the rate
38  // parameter.
39  Module getPayRate(Real Ref rate)
40     Display "Enter the hourly pay rate."
41     Input rate
42  End Module
43
44  // The calcPayWithOT module calculates pay
45  // with overtime. The gross pay is stored
46  // in the gross parameter.
47  Module calcPayWithOT(Real hours, Real rate,
48                       Real Ref gross)
49     // Local variables
50     Declare Real overtimeHours, overtimePay
51
52     // Calculate the number of overtime hours.
53     Set overtimeHours = hours - BASE_HOURS
54
55     // Calculate the overtime pay
56     Set overtimePay = overtimeHours * rate * 
57 OT_MULTIPLIER
58
59     // Calculate the gross pay.
60     Set gross = BASE_HOURS * rate + overtimePay
61  End Module
62
63  // The calcRegularPay module calculates
64  // pay with no overtime and stores it in
65  // the gross parameter.
66  Module calcRegularPay(Real hours, Real rate,
67                        Real Ref gross)
68     Set gross = hours * rate
69  End Module
```
#  Program Output (with Input Shown in Bold)
Enter the number of hours worked.
## 40 [Enter] 
Enter the hourly pay rate.
## 20 [Enter] 
The gross pay is $800

# Program Output (with Input Shown in Bold)
Enter the number of hours worked.
## 50 [Enter] 
Enter the hourly pay rate.
## 20 [Enter] 
The gross pay is $1100
Notice that two global constants are declared in lines 2 and 3. The BASE_HOURS constant is set to 40, which is the number of hours an employee can work in a week without getting paid overtime. The OT_MULTIPLIER constant is set to 1.5, which is the pay rate multiplier for overtime hours. This means that the employee’s hourly pay rate is multiplied by 1.5 for all overtime hours.
=======

For example, consider a program that determines whether a bank customer qualifies for a loan. To qualify, two conditions must exist: (1) the customer must earn at least $30,000 per year, and (2) the customer must have been employed at his or her current job for at least two years. Figure 4-15 shows a flowchart for an algorithm that could be used in such a program. Assume that the salary variable contains the customer’s annual salary, and the yearsOnJob variable contains the number of years that the customer has worked on his or her current job.

If we follow the flow of execution, we see that the condition salary >= 30000 is tested. If this condition is false, there is no need to perform further tests; we know that the customer does not qualify for the loan. If the condition is true, however, we need to test the second condition. This is done with a nested decision structure that tests the condition yearsOnJob >= 2. If this condition is true, then the customer qualifies for the loan. If this condition is false, then the customer does not qualify. Program 4-5 shows the pseudocode for the complete program.

Figure 4-15 A nested decision structure

![image](https://user-images.githubusercontent.com/47218880/67347297-430ccf80-f507-11e9-8089-093774b868d4.png)

##  Program 4-5
```
 1  // Declare variables
 2  Declare Real salary, yearsOnJob
 3
 4  // Get the annual salary.
 5  Display "Enter your annual salary."
 6  Input salary
 7
 8  // Get the number of years on the current job.
 9  Display "Enter the number of years on your"
10  Display "current job."
11  Input yearsOnJob
12
13  // Determine whether the user qualifies.
14  If salary >= 30000 Then
15     If yearsOnJob >= 2 Then
16        Display "You qualify for the loan."
17     Else
18        Display "You must have been on your current"
19        Display "job for at least two years to qualify."
20     End If
21  Else
22     Display "You must earn at least $30,000"
23     Display "per year to qualify."
24  End If
```
# Program Output (with Input Shown in Bold)
Enter your annual salary.
##  35000 [Enter] 
Enter the number of years on your
current job.
## 1 [Enter] 
You must have been on your current
job for at least two years to qualify.
# Program Output (with Input Shown in Bold)
Enter your annual salary.
## 25000 [Enter] 
Enter the number of years on your
current job.
## 5 [Enter] 
You must earn at least $30,000
per year to qualify.
# Program Output (with Input Shown in Bold)
Enter your annual salary.
## 35000 [Enter] 
Enter the number of years on your
current job.
## 5 [Enter] 
You qualify for the loan.


# The Loan Qualifier Program Revisited
In some situations the AND operator can be used to simplify nested decision structures. For example, recall that the loan qualifier program in Program 4-5 uses the following nested If-Then-Else statements:
```
If salary >= 30000 Then
    If yearsOnJob >= 2 Then
       Display "You qualify for the loan."
    Else
       Display "You must have been on your current"
       Display "job for at least two years to qualify."
    End If
Else
    Display "You must earn at least $30,000"
    Display "per year to qualify."
End If
```
The purpose of this decision structure is to determine that a person’s salary is at least $30,000 and that he or she has been at his or her current job for at least two years. Program 4-9 shows a way to perform a similar task with simpler code.

# Program 4-9
```
 1  // Declare variables
2  Declare Real salary, yearsOnJob
3
 4  // Get the annual salary.
5  Display "Enter your annual salary."
6  Input salary
7
 8  // Get the number of years on the current job.
9  Display "Enter the number of years on your ",
10          "current job."
11  Input yearsOnJob
12
13  // Determine whether the user qualifies.
14  If salary >= 30000 AND yearsOnJob >= 2 Then
15     Display "You qualify for the loan."
16  Else
17     Display "You do not qualify for this loan." 
18  End If
```
# Program Output (with Input Shown in Bold)
Enter your annual salary.
## 35000 [Enter] 
Enter the number of years on your current job.
## 1 [Enter] 
You do not qualify for this loan.
# Program Output (with Input Shown in Bold)
Enter your annual salary.
## 25000 [Enter] 
Enter the number of years on your current job.
## 5 [Enter] 
You do not qualify for this loan.
# Program Output (with Input Shown in Bold)
Enter your annual salary.
## 35000 [Enter] 
Enter the number of years on your current job.
## 5 [Enter] 
You qualify for the loan.

The If-Then-Else statement in lines 14 through 18 tests the compound expression salary >= 30000 AND yearsOnJob >= 2. If both subexpressions are true, the compound expression is true and the message “You qualify for the loan” is displayed. If either of the subexpressions is false, the compound expression is false and the message “You do not qualify for this loan” is displayed.

 ### NOTE:
 
A careful observer will realize that Program 4-9 is similar to Program 4-5, but it is not equivalent. If the user does not qualify for the loan, Program 4-9 displays only the message “You do not qualify for this loan,” whereas Program 4-5 displays one of two possible messages explaining why the user did not qualify.

# Yet Another Loan Qualifier Program
Suppose the bank is losing customers to a competing bank that isn’t as strict about whom it loans money to. In response, the bank decides to change its loan requirements. Now, customers have to meet only one of the previous conditions, not both. Program 4-10 shows the pseudocode for the new loan qualifier program. The compound expression that is tested by the If-Then-Else statement in line 14 now uses the OR operator.

# Program 4-10
```
1  // Declare variables
 2  Declare Real salary, yearsOnJob
 3
 4  // Get the annual salary.
 5  Display "Enter your annual salary."
 6  Input salary
 7
 8  // Get the number of years on the current job.
 9  Display "Enter the number of years on your"
10  Display "current job."
11  Input yearsOnJob
12
13  // Determine whether the user qualifies.
14  If salary >= 30000 OR yearsOnJob >= 2 Then
15     Display "You qualify for the loan."
16  Else
17     Display "You do not qualify for this loan." 
18  End If
```
# Program Output (with Input Shown in Bold)
Enter your annual salary.
## 35000 [Enter] 
Enter the number of years on your 
current job.
## 1 [Enter]
You qualify for the loan.
# Program Output (with Input Shown in Bold)
Enter your annual salary.
## 25000 [Enter] 
Enter the number of years on your
current job.
## 5 [Enter]
You qualify for the loan.
# Program Output (with Input Shown in Bold)
Enter your annual salary.
## 12000 [Enter] 
Enter the number of years on your
current job.
## 1 [Enter] 
You do not qualify for this loan.










>>>>>>> upstream/master
