Thirty different type to c programming problems:                                                    
1.Write a program to find a number entered is positive,negative or zero?
#include <stdio.h>
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    if (n > 0) 
    {
        printf("The given number is Positive.\n");
    }
    else if (n < 0) 
    {
        printf("The given number is Negative.\n");
    }
    else 
    {
        printf("The given number is Zero.\n");
    }
    return 0;
}

2.Write a program to find character entered is a alphabet?
#include <stdio.h>
int main()
{
    char ch;
    printf("Enter a character: ");
    scanf("%c", &ch);
    if (ch >= 'A' && ch <= 'Z')
    {
        printf("It's a Uppercase alphabet.");
    }
    else if(ch >= 'a' && ch <= 'z')
    {
        printf("It's a Lowercase alphabet.");
    }
    else
    {
    printf("It's not a alphabet");
    }
    return 0;
}

3.Write a program to find character entered is a vowel or not?
#include <stdio.h>
int main()
{
    char ch;
    printf("Enter a character: ");
    scanf("%c", &ch);
    if (ch=='a' || ch=='e' || ch=='i' || ch=='o' || ch=='u' )
    {
        printf("It's a Lowercase vowel.");
    }
    else if( ch=='A' || ch=='E' || ch=='I' || ch=='O' || ch=='U')
    {
        printf("It's a Uppercase vowel");
    }
    else
    {
    printf("It's not a vowel");
    }
    return 0;
}

4.Write a program to find given year is leap year or not?
#include <stdio.h>
int main() 
{
    int n;
    printf("Enter a year: ");
    scanf("%d", &n);
    if ((year % 400 == 0) || (year % 4 == 0 && year % 100 != 0)) 
    {
        printf("It's a leap year.");
    }
    else 
    {
        printf("It's not a leap year.");
    }
    return 0;
}

5.Write a program to find the maximum number among three number?
#include <stdio.h>
int main() {
    int x, y, z;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &x, &y, &z);
    if (x >= y && x >= z)
    {
        printf("%d is the largest number.", x);
    }
    else if (y >= x && y >= z) 
    {
       printf("%d is the largest number.", y);
    }
    else 
    {
        printf("%d is the largest number.", z);
    }
    return 0;
}

6.Write a program where shop keeper given 10% discount if bill is more than 1000. Then calculate the actual bill?
#include <stdio.h>

int main()
{
    float bill, discount, finalAmount;
    printf("Enter total bill amount: ");
    scanf("%f", &bill);
    if (bill > 1000) 
    {
        discount = bill * 0.10;    // 10% discount
        finalAmount = bill - discount;
    }
    else 
    {
        discount = 0;
        finalAmount = bill;
    }
    printf("Discount Given: %.2f\n", discount);
    printf("Final Bill Amount: %.2f\n", finalAmount);
    return 0;
}

7.Write a program in C to display the first 10 natural numbers?
#include <stdio.h>
void main() 
{     
    int i;  
    printf("The first 10 natural numbers are:\n");  
    for (i=1; i<=10; i++)
	{      
		printf("%d ", i); 
	}
    printf("\n");  
}

8.Write a C program to compute the sum of the first 10 natural numbers?
#include <stdio.h>
int main() 
{  
    int j, sum = 0; 
    printf("The first 10 natural numbers are :\n");  
    for (j = 1; j <= 10; j++)
    {
        sum = sum + j;  
        printf("%d ", j);  
    }
    printf("\nThe Sum is : %d\n", sum);  
    return 0; 
}

9.Write a C program to make such a pattern like a pyramid with a number which will repeat the number in the same row?
#include<stdio.h>
void main()
{
   int i, j, spc, rows, k;  
   printf("Input number of rows : ");  
   scanf("%d", &rows); 
   spc = rows + 4 - 1;  
   for(i = 1; i <= rows; i++) 
   {
         for(k = spc; k >= 1; k--) 
         {
            printf(" ");
         }
	   for(j = 1; j <= i; j++)
	   {
	       printf("%d ", i);
	   }
	printf("\n");  
    spc--;  
   }
}

10.Write a C program to print numbers from 1 to 10 and 10 to 1 using a do-while loop?
#include <stdio.h>
int main()
{
    int i = 1;  
    printf("Print numbers from 1 to 10:\n");
    do {
        printf("%d ", i);  
        i++;  
    } while (i <= 10); 
    printf("\n");
    i = 10;  
    printf("\nPrint numbers from 10 to 1:\n");
    do {
        printf("%d ", i); 
        i--;  
    } while (i >= 1);
    return 0;
}

11.Write a C program that prompts the user to enter a positive integer and then calculates and prints the sum of the squares of each digit in that number using a do-while loop?
#include <stdio.h>
int main() 
{
    int num, digit, sum = 0;
    printf("Input a positive integer: ");
    scanf("%d", &num);
    if (num <= 0) 
    {
        printf("Please input a positive integer.\n");
        return 1;
}
    do 
    {
        digit = num % 10;  
        sum += digit * digit;  
        num /= 10;  
    } 
    while (num != 0); 
    printf("Sum of the squares of each digit: %d\n", sum);
    return 0;
}

12.Write a C program that calculates and prints the sum of prime numbers up to a specified limit  using a do-while loop?
#include <stdio.h>
int isPrime(int num)
{
    if (num < 2) 
    {
        return 0;  
    }
    for (int i = 2; i * i <= num; i++)
    {
        if (num % i == 0) 
        {
            return 0;  
        }
    }
    return 1; 
}

int main() 
{
    int limit;
    int num = 2;  
    int sum = 0;
    printf("Input the limit for prime numbers: ");
    scanf("%d", &limit);
    do
    {
        if (isPrime(num))
        {
            sum += num; 
        }
        num++; 
    } 
    while (num <= limit);
    printf("Sum of prime numbers up to %d: %d\n", limit, sum);
    return 0; 
}

13.Write a C program to print numbers from 0 to 10 and 10 to 0 using two while loops?
#include <stdio.h>
int main()
{
    int i = 0;  
    printf("Numbers from 0 to 10:\n");
    while (i <= 10) 
    {
        printf("%d ", i); 
        i++; 
    }
    printf("\n");  
    i = 10; 
    printf("\nNumbers from 10 to 0:\n");
	while (i >= 0) 
    {
        printf("%d ", i); 
        i--;  
    }
    return 0;  
}

14.Write a C program that calculates the product of numbers from 1 to 5 using a while loop?
#include <stdio.h>
int main() 
{
    int number = 1;  
    int product = 1; 
    while (number <= 5) 
    {
        product *= number;
        printf("Current number: %d, Current product: %d\n", number, product);
        number++;
    }
    return 0; 
}

15.Write a program in C to read any digit and display it in the word?
#include <stdio.h>
void main()
{
   int cdigit; 
   printf("Input Digit(0-9) : ");
   scanf("%d",&cdigit);  
   switch(cdigit)  
   {
	 case 0:
	       printf("Zero\n"); 
	       break;
	 case 1:
	       printf("One\n"); 
	       break;
	case 2:
	       printf("Two\n"); 
	       break;
	case 3:
	       printf("Three\n"); 
	       break;
	case 4:
	       printf("Four\n"); 
	       break;
	case 5:
	       printf("Five\n"); 
	       break;
	case 6:
	       printf("Six\n"); 
	       break;
	case 7:
	       printf("Seven\n");  
	       break;
	case 8:
	       printf("Eight\n");  
	       break;
	case 9:
	       printf("Nine\n"); 
	       break;
	default:
	       printf("Invalid digit. \nPlease try again ....\n"); 
	       break;
      }
}

16.Write a program in c to copy one string to another string?
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
int main() 
{
    char str1[100], str2[100]; 
    int i;
    printf("\n\nCopy one string into another string :\n"); 
    printf("-----------------------------------------\n");
    printf("Input the string : ");
    fgets(str1, sizeof str1, stdin); 
    i = 0; 
    while (str1[i] != '\0')
	{ 
        str2[i] = str1[i]; 
        i++; 
    }
    str2[i] = '\0'; 
    printf("\nThe First string is : %s\n", str1);
    printf("The Second string is : %s\n", str2);
    printf("Number of characters copied : %d\n\n", i);
	return 0; 
}

17.Write a program in c to chech whether a letter is uppercase or not?
#include <stdio.h>
#include <ctype.h>
int main()
{
    char ch;
    printf("Enter a character: ");
    scanf("%c", &ch);
    if (isupper(ch)) {
        printf("The character is uppercase.\n");
    } else {
        printf("The character is NOT uppercase.\n");
    }
    return 0;
}

18.Write a program in c to check whether a letter is lowercase or not?
#include <stdio.h>
#include <ctype.h>
int main() 
{
    char ch;
    printf("Enter a character: ");
    scanf("%c", &ch);
    if (islower(ch)) {
        printf("The character is lowercase.\n");
    } else {
        printf("The character is NOT lowercase.\n");
    }
    return 0;
}

19.Write a program in c to store elements in an array and print them?
#include <stdio.h>
int main()  
{  
    int arr[10];  
    int i;  
    printf("\n\nRead and Print elements of an array:\n");
    printf("-----------------------------------------\n");	
    printf("Input 10 elements in the array :\n");  
    for(i=0; i<10; i++)  
    {  
	    printf("element - %d : ",i); 
        scanf("%d", &arr[i]);  
    }  
    printf("\nElements in array are: ");  
    for(i=0; i<10; i++)  
    {  
        printf("%d  ", arr[i]); 
		}
    printf("\n");
	return 0;	
}

20.Write a program in c to merge two array of the same size sorted in descending order?
#include <stdio.h>
int main()
{
    int arr1[100], arr2[100], arr3[200];
    int s1, s2, s3;
    int i, j, k;
       printf("\n\nMerge two arrays of same size sorted in decending order.\n");
       printf("------------------------------------------------------------\n");	
       printf("Input the number of elements to be stored in the first array :");
       scanf("%d",&s1);
       printf("Input %d elements in the array :\n",s1);
       for(i=0;i<s1;i++)
            {
	      printf("element - %d : ",i);
	      scanf("%d",&arr1[i]);
	    }
       printf("Input the number of elements to be stored in the second array :");
       scanf("%d",&s2);
       printf("Input %d elements in the array :\n",s2);
       for(i=0;i<s2;i++)
            {
	      printf("element - %d : ",i);
	      scanf("%d",&arr2[i]);
	    }
    s3 = s1 + s2;
    for(i=0;i<s1; i++)
        {
            arr3[i] = arr1[i];
         }
     for(j=0;j<s2; j++)
        {
            arr3[i] = arr2[j];
            i++; 
        }
   for(i=0;i<s3; i++)
        {
           for(k=0;k<s3-1;k++)
             {
                if(arr3[k]<=arr3[k+1])
                 {
                   j=arr3[k+1];
                   arr3[k+1]=arr3[k];
                   arr3[k]=j;
                 }  
              }
         }                      
     printf("\nThe merged array in decending order is :\n");
    for(i=0; i<s3; i++)
    {
        printf("%d   ", arr3[i]);
    }
	printf("\n\n");
	return 0;
}


21.Write a program in c using a structure named student that contains two members?
#include <stdio.h>
struct Student
{
    int roll;
    float marks;
};
int main()
{
    struct Student S1, S2;
    printf("Enter Roll & Marks: ");
    scanf("%d %f", &S1.roll, &S1.marks);
    S2 = S1; 
    printf("%d %.2f\n", S2.roll, S2.marks);
    return 0;
}

22.Write a program in c to accept 9 integers from the user and store them in a 3*3 matrix. Display
the matrix in proper row and column format?
#include <stdio.h>
int main()
{
    int matrix[3][3];
    int i, j;
    printf("Enter 9 integers for the 3x3 matrix:\n");
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 3; j++) {
            printf("Enter element [%d][%d]: ", i, j);
            scanf("%d", &matrix[i][j]);
        }
    }
    printf("\nThe 3x3 Matrix is:\n");
    for(i = 0; i < 3; i++) {
        for(j = 0; j < 3; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }
    return 0;
}


23.Write a program to find the factorial of a number using a recursive function?
#include <stdio.h>
int fact(int x);
int main()
{
    int n, f;
    printf("Enter the number: ");
    scanf("%d", &n);
    f = fact(n);
    printf("Factorial = %d\n", f);  // <-- fixed 'count<<f' to 'printf'
    return 0;
}
int fact(int x)
{
    if (x == 1 || x == 0)  
        return 1;
    else
        return x * fact(x - 1);  
 }




                                                                Logic-building-programs
                                                                       
