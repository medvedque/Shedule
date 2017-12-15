/*Медведев Алексей .
Семинар 3,задача 25.
Построить график функции, фигурировавшей в уравнении, которое решалось после 
предыдущего семинара в окрестности найденного корня уравнения.*/

#include <iostream>
#include <stdlib.h>
#include <math.h>

using namespace std;
#define X 50
#define Y 100

char A[X][Y] = {};


double f(double x)
{
	return (exp(-x*x) - x);
}

void print_table(char A[X][Y])
{
	for (int i = Y-1; i > 0; i--)
	{
		for (int j = 0; j < X; j++)
		{
			cout << A[j][i];
		}

		cout << endl;
	}
}

int main()
{
	double a = 0;

	for (int i =0; i < X-1; i++)
	{
		for (int j = 0; j < Y-1; j++)
		{
			A[i][49] = '-';
			A[24][j] = '.';
		}
	}

	for (int i =0; i < X; i++)
	{
		a = (f(i-24))+25;
		int b = a*2;
		if ( b-49 < X)
			if (f(b)<Y)
		{
			A[i][b] = '*';
		}
	}
	A[49][49] = 'x';
	A[24][99] = 'y';

	print_table(A);
	return 0;
}
