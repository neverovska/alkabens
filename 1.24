#include <stdio.h>

long double factor(unsigned long int a);
void summa(void);

	void main(void)
	{
		int k;
		do {
			printf("Enter point of menu:\n1.Calculate\n2.Finish\n");
			scanf_s("%d", &k);
			while (getchar() != '\n');
			if (k == 1)
			{
				summa();
				k = 0;
			}
			else if (k!=1&&k!=2)
				printf("Enter right point!\n");
		} while (k != 2);

	}

	long double factor(unsigned long int a) 
	{
		if (a < 0)
			return 0;
		if (a == 0)
			return 1;
		else
			return a * factor(a - 1);
	}

	void summa(void) 
	{
		int n;
		long double pr = 1, sum = 0;

		do {
			printf("Enter positive  n: ");
			scanf_s("%d", &n);
			while (getchar() != '\n');
			if (n > 0 && n < 21) {
				for (int i = 1; i <= n; i++) {
					for (int j = 1; j <= i; j++)
						pr *= factor(i + j) / factor(i);
					sum += pr;
					pr = 1;
				}
				printf("Summa = %llf\n", sum);
			}
			else
				printf("Enter right n!\n");
		} while (n <= 0 ||n >= 21);

	}
