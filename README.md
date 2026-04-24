Execute the following programs and create a  document in github with question, code and output and then upload the pdf file generated from github and also give the github link in the submission

##1. Write a C program to find the maximum of three numbers without using logical operators.

##code :
```
#include <stdio.h>

int main() {
    int a, b, c, max;
    scanf("%d %d %d", &a, &b, &c);

    max = a;
    if (b > max)
        max = b;
    if (c > max)
        max = c;

    printf("Maximum = %d", max);
    return 0;
}
```

##output:
<img src="https://img.sanishtech.com/u/ddb3d1f62a70e6646a39ddeb1ad55759.jpg" alt="d277d1fd-e66a-4651-bd91-9ba90ca53270" loading="lazy" style="max-width:100%;height:auto;">

##2.  Write a  C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)
##code:
```
#include <stdio.h>

int main() {
    int year;
    scanf("%d", &year);

    if (year % 400 == 0)
        printf("%d is a century leap year", year);
    else if (year % 100 == 0)
        printf("%d is not a leap year", year);
    else if (year % 4 == 0)
        printf("%d is a non-century leap year", year);
    else
        printf("%d is not a leap year", year);

    return 0;
}
```
##output:
<img src="https://img.sanishtech.com/u/d3f524af7b062c25e0c272a2e9554199.jpg" alt="2e7e3c1d-68ff-4e01-b3b3-fb1581eba4f7" loading="lazy" style="max-width:100%;height:auto;">


##3. Write a C program to find whether the entered character is alphabet / digit / special character. If the entered character is an alphabet then say it is vowel or consonant without using built in functions.
##code:
```
#include <stdio.h>

int main() {
    char ch;
    scanf("%c", &ch);

    if ((ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z')) {
        printf("Alphabet\n");
        if (ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||
            ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U')
            printf("Vowel");
        else
            printf("Consonant");
    } 
    else if (ch >= '0' && ch <= '9')
        printf("Digit");
    else
        printf("Special Character");

    return 0;
}
```
##output:
<img src="https://img.sanishtech.com/u/a9df760350a6f08bfd6ac34212dddde5.jpg" alt="0d4670ec-3cff-4f82-a0e8-5f8819399d8d" width="825" height="226" loading="lazy" style="max-width:100%;height:auto;">


##4. Write a  C program for simple ATM simulation with operations Check Balance, Deposit,  Withdraw,  Exit using switch and update balance accordingly.
##code:
```
#include <stdio.h>

int main() {
    int choice;
    float balance = 1000, amount;

    do {
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Balance = %.2f\n", balance);
                break;

            case 2:
                scanf("%f", &amount);
                balance += amount;
                printf("Updated Balance = %.2f\n", balance);
                break;

            case 3:
                scanf("%f", &amount);
                if (amount <= balance) {
                    balance -= amount;
                    printf("Updated Balance = %.2f\n", balance);
                } else {
                    printf("Insufficient Balance\n");
                }
                break;

            case 4:
                break;

            default:
                printf("Invalid Choice\n");
        }
    } while (choice != 4);

    return 0;
}
```
##output:
<img src="https://img.sanishtech.com/u/5dfa159d6e833b08f9daf80406ba2218.jpg" alt="9def4a3d-c756-4c38-9110-4d61cadd09ed" width="809" height="188" loading="lazy" style="max-width:100%;height:auto;">

##5. Write a C program for menu driven calculator using switch statement.
##code:
```
#include <stdio.h>

int main() {
    int choice;
    float a, b;

    scanf("%d", &choice);
    scanf("%f %f", &a, &b);

    switch (choice) {
        case 1:
            printf("Result = %.2f", a + b);
            break;
        case 2:
            printf("Result = %.2f", a - b);
            break;
        case 3:
            printf("Result = %.2f", a * b);
            break;
        case 4:
            if (b != 0)
                printf("Result = %.2f", a / b);
            else
                printf("Division by zero error");
            break;
        default:
            printf("Invalid Choice");
    }

    return 0;
}
```
##output:

<img src="https://img.sanishtech.com/u/b3c6433094d65caa2faa22bed696455b.jpg" alt="27249fad-2dda-427a-afbc-e935e0022d7f" width="821" height="251" loading="lazy" style="max-width:100%;height:auto;">

