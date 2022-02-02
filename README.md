// Online C compiler to run C program online
#include <stdio.h>
#include<string.h>

typedef struct account {
    int accn;
    char name[100];
    float amount;
    int day;
    int month;
    int year;
}acc;
void display (acc d){
   printf("Your account number is:- %d\n",d.accn);
   printf("Account holder name is:- %s\n",d.name);
printf("Total balance in your account is:- %f\n",d.amount);
printf("Your account number opened on:- %d-%d-%d \n",d.day,d.month,d.year);
printf("***********************");
   
}

int main() {
    int n;
    printf("How many bank accounts details you want to enter:-");
    scanf("%d\n",&n);
    acc dacc[n];
    for(int i=0;i<n;i++){
        
    printf("%d.......Enter the account number:-",i+1);
    scanf("%d\n",&dacc[i].accn);
    
    printf("Enter the account holder name:-");
    scanf("%s\n",dacc[i].name);
    
    printf("Enter the total amount:-");
     scanf("%f\n",&dacc[i].amount);
    
    printf("Enter the date of account opening\n");
    printf("Day :-");
    scanf("%d\n",&dacc[i].day);
      printf("Month :-");
      scanf("%d\n",&dacc[i].month);
        printf("Year :-");
    scanf("%d\n",&dacc[i].year);
    }
    for(int i=0;i<n;i++){
        display (dacc[i]);
    }
    
    
    return 0;
}
