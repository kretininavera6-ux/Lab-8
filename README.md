Вычислите с использованием цикла for значение ряда для заданного значения x
<img width="1788" height="3331" alt="deepseek_mermaid_20251104_611a32 (1)" src="https://github.com/user-attachments/assets/866a4e73-f196-48fd-8f23-57ceae7c3609" />

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
