Вычислите с использованием цикла for значение ряда для заданного значения x
<img width="1884" height="3444" alt="image" src="https://github.com/user-attachments/assets/75eb542e-8ca6-4465-9808-fdb875c7d627" />

# Lab-8
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <locale.h>
int main() {
    setlocale(LC_ALL, "rus");
    double x, numerator = 1.0, denominator = 1.0;
    printf("Введите x: ");
    scanf("%lf", &x);
    for (int n = 1; n <= 6; n++) {
        numerator *= (x - ((1 << n) - 1));
        denominator *= (x - (1 << n));
    }
    printf("Результат: %lf\n", numerator / denominator);
    return 0;
}
