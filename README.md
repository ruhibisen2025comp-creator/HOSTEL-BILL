#include <stdio.h>
int main() {
    int id, num, months, mess, wifi, points, total, discount = 0;
    char name[50];
    const int room_fee = 2000, mess_fee = 1500, wifi_fee = 500;

    printf("Enter Customer ID: "); scanf("%d", &id);
    printf("Enter Contact Number: "); scanf("%d", &num);
    printf("Enter Name: "); scanf("%s", name);
    printf("Months Stayed: "); scanf("%d", &months);
    printf("Mess Facility (1=Yes,0=No): "); scanf("%d", &mess);
    printf("WiFi Facility (1=Yes,0=No): "); scanf("%d", &wifi);
    printf("Housekeeping Points (0-100): "); scanf("%d", &points);

    if (points >= 90) discount = 150;
    else if (points >= 75) discount = 50;
    else if (points >= 50) discount = 10;

    total = room_fee * months;
    if (mess) total += mess_fee * months;
    if (wifi) total += wifi_fee * months;
    total -= discount;

    printf("\n======HOSTEL BILL =======\n");
    printf("ID:%d  Name:%s\n", id, name);
    printf("Months:%d  Points:%d\n", months, points);
    printf("Total: ₹%d  (Discount:₹%d)\n", total, discount);

    if (points >= 90) printf("CLEANLINESS CHAMPION!\n");
    else if (points >= 75) printf("NEATNESS STAR!\n");
    else if (points >= 50) printf("ROOM CARE MEMBER!\n");
    else printf("Try keeping cleaner next time!\n");
    printf("=========================");
    return 0;
}

