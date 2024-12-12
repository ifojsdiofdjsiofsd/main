#include <stdio.h>
int get_clock_strikes(int hours, int minutes) {
int total_strikes = 0;
// Определяем количество ударов в начале каждого часа
for (int i = 1; i <= hours; i++) {
total_strikes += i;
}
// Определяем количество ударов в середине каждого часа
total_strikes += hours;
// Если время находится в последние 30 минут часа, добавляем еще 1 удар
if (minutes >= 30) {
total_strikes++;
}
return total_strikes;
}
int main() {
int hours, minutes;
printf("Введите количество часов и минут: ");
scanf("%d %d", &hours, &minutes);
int total_strikes = get_clock_strikes(hours, minutes);
printf("Часы сделали %d ударов за это время.\n", total_strikes);
return 0;
}
