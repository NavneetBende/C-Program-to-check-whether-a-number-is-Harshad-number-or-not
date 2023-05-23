# C-Program-to-check-whether-a-number-is-Harshad-number-or-not

Write a C Program to check if number is Harshad number or not
In mathematics, a Harshad number is a number that is divisible by the sum of its digits.

Ex- Number is 21

it is divisible by its own sum (1+2) of its digit(2,1)

So it is Harshad's Number

Some other Harshad's Number are 156,54,120 etc
hashed or not in c
Working:-
For user input num

Extract individual digits of num
Calculate the sum of these digits
Check if the num is divisible by sum
If yes, then its a harshad’s number
Else its not
Harshads Number in C
C Program:-
Run
#include <stdio.h>

int checkHarshad(int num){
    
    int sum = 0;
    int temp = num;
    
    while(temp != 0){
        sum = sum + temp % 10;
        temp /= 10;
    }
    
    // will return 1 if num is divisible by sum, else 0
    return num % sum == 0;
}

int main ()
{
    int num = 153;
    
    if(checkHarshad(num))
        printf("%d is Harshad's Number", num);
    else
        printf("%d is not Harshad's Number", num);

    return 0;
}
// Time complexity: O(N)
// Space complexity: O(1)
Output:-
153 is Harshad's Number
