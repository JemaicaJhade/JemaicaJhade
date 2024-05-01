#include <stdio.h>
#include <stdlib.h>

#define MAX_EMPLOYEES 100

struct Employee {
    int empNumber;
    char name[50];
    float basicPay;
    float allowance;
    float deductions;
};

int main() {
    int numEmployees;
    printf("Enter the number of employees: ");
    scanf("%d", &numEmployees);

    struct Employee employees[MAX_EMPLOYEES];

    for (int i = 0; i < numEmployees; i++) {
        printf("\nEnter the employee number: ");
        scanf("%d", &employees[i].empNumber);

        printf("Enter the name: ");
        scanf("%s", employees[i].name);

        printf("Enter the basic pay: ");
        scanf("%f", &employees[i].basicPay);

        printf("Enter the allowance: ");
        scanf("%f", &employees[i].allowance);

        printf("Enter the deductions: ");
        scanf("%f", &employees[i].deductions);
    }

    // Displaying stored data
    printf("\nEmployee Data:\n");
    for (int i = 0; i < numEmployees; i++) {
        printf("\nEmployee Number: %d\n", employees[i].empNumber);
        printf("Name: %s\n", employees[i].name);
        printf("Basic Pay: %.2f\n", employees[i].basicPay);
        printf("Allowance: %.2f\n", employees[i].allowance);
        printf("Deductions: %.2f\n", employees[i].deductions);
    }

    return 0;
}
