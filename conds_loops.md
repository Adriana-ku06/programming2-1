


# Structures and characteristics of selective control structures in algorithm coding:

## Simple conditional 
It is one of the powerful conditional statement. If statement is responsible for modifying the flow of execution of a program. If statement is always used with a condition. The condition is evaluated first before executing any statement inside the body of If. The syntax for if statement is as follows:
``` C
/*if (condition) 
     instruction;*/
     #include<stdio.h>
int main()
{
	int num1=1;
	int num2=2;
	if(num1<num2)		//test-condition
	{
		printf("num1 is smaller than num2");
	}
	return 0;
} 
          
```


## Double conditional 
The if-else is statement is an extended version of If. The general form of if-else is as follows:
This type of a construct, if the value of test-expression is true, then the true block of statements will be executed. If the value of test-expression if false, then the false block of statements will be executed. In any case, after the execution, the control will be automatically transferred to the statements appearing outside the block of If.

Following programs illustrate the use of the if-else construct:

We will initialize a variable with some value and write a program to determine if the value is less than ten or greater than ten.


``` C
/*if (test-expression)
{
    True block of statements
}
Else
{
    False block of statements
}
Statements;;*/
     #include<stdio.h>
int main()
{
	int num=19;
	if(num<10)
	{
		printf("The value is less than 10");
	}
	else
	{
		printf("The value is greater than 10");
	}
	return 0;
}
          
```


## Multiple conditional 
Then a series of decision is required, nested if-else is used. Nesting means using one if-else construct within another one.

Let's write a program to illustrate the use of nested if-else.
n nested if-else, we have to be careful with the indentation because multiple if-else constructs are involved in this process, so it becomes difficult to figure out individual constructs. Proper indentation makes it easy to read the program.
``` C
#include<stdio.h>
int main()
{
	int num=1;
	if(num<10)
	{
		if(num==1)
		{
			printf("The value is:%d\n",num);
		}
		else
		{
			printf("The value is greater than 1");
		}
	}
	else
	{
		printf("The value is greater than 10");
	}
	return 0;
}


```

## Nested conditional 

Nested else-if is used when multipath decisions are required.

The general syntax of how else-if ladders are constructed in 'C' programming is as follows:
```
 if (test - expression 1) {
    statement1;
} else if (test - expression 2) {
    Statement2;
} else if (test - expression 3) {
    Statement3;
} else if (test - expression n) {
    Statement n;
} else {
    default;
}
Statement x;
```
This type of structure is known as the else-if ladder. This chain generally looks like a ladder hence it is also called as an else-if ladder. The test-expressions are evaluated from top to bottom. Whenever a true test-expression if found, statement associated with it is executed. When all the n test-expressions becomes false, then the default else statement is executed.


```C
#include<stdio.h>
int main()
{
	int marks=83;
	if(marks>75){
		printf("First class");
	}
	else if(marks>65){
		printf("Second class");
	}
	else if(marks>55){
		printf("Third class");
	}
	else{
		printf("Fourth class");
	}
	return 0;
}
```

# Iterative control structures 
in iteration control structures, a statement or block is executed until the program reaches a certain state, or operations have been applied to every element of a collection. This is usually expressed with keywords such as while, repeat, for, or do..until.

## For 
For loop provides facility to write initialization, termination and flow at same place, in the parenthesis of for. Notice the two semicolons inside for’s round braces, these are part of syntax, hence should always be mentioned. Two semicolons created three sections. First section is used for initialization, second section is used for termination condition and third section is used to mention flow.
```
for(initialization; condition; increment)

{
  ……
  ……
}
```

## Nested For 
The placing of one loop inside the body of another loop is called nesting.  When you "nest" two loops, the outer loop takes control of the number of complete repetitions of the inner loop.  While all types of loops may be nested, the most commonly nested loops are for loops.


nested loops

    

Let's look at an example of nested loops at work.

We have all seen web page counters that resemble the one shown below ( well, OK, maybe not quite this spastic!!).  Your car's odometer works in a similar manner.



This counter (if it worked properly) and your car's odometer are little more than seven or eight nested for loops, each going from 0 to 9.  The far-right number iterates the fastest, visibly moving from 0 to 9 as you drive your car or increasing by one as people visit a web site.  A for loop which imitates the movement of the far-right number is shown below:


``` C
for(num1 = 0; num1 <= 9; num1++)
{
      cout << num1 << endl;
} 
```

The far-right number, however, is not the only number that is moving.  All of the other numbers are moving also, but at a much slower pace.  For every 10 numbers that move in the column on the right, the adjacent column is incremented by one.  The two nested loops shown below may be used to imitate the movement of the two far-right numbers of a web counter or an odometer:



## While 
Syntax of while is similar to if. In the case of if, when the condition is TRUE control moves inside if block and execute statements of if-block. After executing if-block control moves to the statement written immediately after if-block (outside if-block).

In the case of while, when the condition is TRUE control moves inside while-block and execute statements of while-block. After executing while-block control does not move to the statement written immediately after while-block rather it goes back to the condition of while block. This condition will be checked again and if it is again TRUE control moves again inside while-block. This repeats till the condition becomes FALSE. while loop executes the set of statements until the condition is true or non-zero value.

```
int main()
{
   	….
….
	while(condition)
	{
	….
	….
}
…
}
```

## Do-While 
do-while works similar to while but the only difference is, earlier is executed at least once. in while loop condition is evaluated first then goes into loop body, on the other hand in do while loop first control enters in loop body then condition will be checked. This makes possible to control enters in loop body even though the condition is false.
do while loop is exit control loop, because condition is checked on exit from the block.
```
int main()

{
 int i=5;
 do
 {
  printf(“mysirg.com”);

  }while(i>6);
getch();
return(0);

 }

```


## Break and Continue 
The break statement ends the loop immediately when it is encountered. Its syntax is:
```
 break
```
The break statement is almost always used with if...else statement inside the loop.
``` C
# include <stdio.h>
int main()
{
    int i;
    double number, sum = 0.0;

    for(i=1; i <= 10; ++i)
    {
        printf("Enter a n%d: ",i);
        scanf("%lf",&number);

        // If the user enters a negative number, the loop ends
        if(number < 0.0)
        {
            break;
        }

        sum += number; // sum = sum + number;
    }

    printf("Sum = %.2lf",sum);
    
    return 0;
}

```
The continue statement skips the current iteration of the loop and continues with the next iteration. Its syntax is:
```
continue;
```

The continue statement is almost always used with the if...else statement.

```
# include <stdio.h>
int main()
{
    int i;
    double number, sum = 0.0;

    for(i=1; i <= 10; ++i)
    {
        printf("Enter a n%d: ",i);
        scanf("%lf",&number);

        if(number < 0.0)
        {
            continue;
        }

        sum += number; // sum = sum + number;
    }

    printf("Sum = %.2lf",sum);
    
    return 0;
}
```

# References

* [programming fundamental](shttps://press.rebus.community/programmingfundamentals/chapter/iteration-control-structures/)
* [if-else-statement](https://www.guru99.com/c-if-else-statement.html)
* [Structur Control](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a77069/03_struc.html)
* [Loops](https://www.mysirg.com/iterative-control-instruction-loops/)
* [Looping](http://www.mrroberts.com/MathBits/CompSci/looping/nested.htm)

