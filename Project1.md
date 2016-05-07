#include <tchar.h>
#include <iostream>
#include <string>
#include <ctime>

using namespace std;

int _tmain(int argc, wchar_t argv[]) // функция для юникода и не юникода
{
	srand(time(NULL)); // использование даты для генерации псевдослучайного числа 
	setlocale(LC_ALL, "Russian"); // поддержка работы с русским языком в консоле
	int arr[10][10]; // создание целочисленной матрицы
	for (int i = 0; i < 10; i++)
	{
		for (int j = 0; j < 10; j++)
		{
			arr[i][j] = rand() % 100 - 30; // заполнение каждого эл-та массива рандомным числом, 30% отрицательных чисел
			cout << arr[i][j] << " ";  // вывод каждого элемента матрицы
		}
		cout << "\n" << endl;
	}
	int s = 0;
	double a = 0;
	{for (int i = 0; i < 10; i++)
	{
		for (int j = 0; j < 10; j++)
			s = s + arr[i][j];  
	}}
	a = s / 100; 
	cout << "\n\n Сумма элементов массива равна " << s;
	cout << "\n\n Среднее арифметическое матрицы равно " << a;
	cin.get();
	return 0;
}