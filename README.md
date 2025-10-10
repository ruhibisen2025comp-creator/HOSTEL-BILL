#include <stdio.h>
int main() {
    int id, months, mess, wifi, num;
    char name[50];
    int total = 0; 
    int room_fee = 2000; 
    int mess_fee = 1500;   
    int wifi_fee = 500;   

   printf("Enter Customer ID (numbers only): ");
    if (scanf("%d", &id) != 1) {
        printf("Oops! Wrong input. ID must be a number.\n");
        return 0;
    }
    printf("Enter contact number:");
    scanf("%d", &num);
    printf("Enter Customer Name (alphabets only): ");
    scanf("%s", name);
    printf("Enter number of months: ");
    if (scanf("%d", &months) != 1 || months <= 0) {
        printf("Oops! Wrong input. Months must be positive.\n");
        return 0;
    }
  printf("Do you want Mess? (1=Yes, 0=No): ");
    scanf("%d", &mess);

    printf("Do you want WiFi? (1=Yes, 0=No): ");
    scanf("%d", &wifi);
      total = months * room_fee;
    if (mess == 1) total += months * mess_fee;
    if (wifi == 1) total += months * wifi_fee;

   printf("\n===== HOSTEL FEE BILL =====\n");
    printf("Customer ID   : %d\n", id);
    printf("Customer Name : %s\n", name);
    printf("Months Stay   : %d\n", months);
    printf("---------------------------\n");
    printf("Room Fee      : %d\n", months * room_fee);
    if (mess == 1) printf("Mess Fee      : %d\n", months * mess_fee);
    if (wifi == 1) printf("WiFi Fee      : %d\n", months * wifi_fee);
    printf("---------------------------\n");
    printf("TOTAL BILL    : %d\n", total);
    printf("===========================\n");

    return 0;
}
