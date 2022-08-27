// Задача 47: Задайте двумерный массив размером m×n, обнаруженный случайным выявленным числом.
Console.WriteLine("введите количество строк");
int linesVol = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("введите количество столбцов");
int columnsVol = Convert.ToInt32(Console.ReadLine());
двойные [,] числа = новые двойные [linesVol, columnsVol];
FillArrayRandomNumbers(числа);
РаспечататьМассив(числа);

void FillArrayRandomNumbers (массив double [,])
{
    for (int i = 0; i < array.GetLength(0); i++)
    {
        for (int j = 0; j < array.GetLength(1); j++)
        {
            array[i, j] = Convert.ToDouble(new Random().Next(-100, 100))/10;
        }
    }
}

void PrintArray (двойной [,] массив)
{
    for (int i = 0; i < array.GetLength(0); i++)
    {
        Консоль.Написать("[ ");
        for (int j = 0; j < array.GetLength(1); j++)
        {
            Console.Write(массив [i, j] + " ");
        }
        Console.Write("]");
        Консоль.WriteLine("");
    }
}


// Задача 50: Напишите программу, которая принимает позицию элемента в двумерном массиве, и возвращает значение этого элемента или же указывает, что такого элемента нет.

Console.WriteLine("введите номер строки");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("введите номер столбца");
int m = Convert.ToInt32(Console.ReadLine());
int [,] числа = новые int [10,10];
FillArrayRandomNumbers(числа);

если (n > числа.GetLength(0) || m > числа.GetLength(1))
{
    Console.WriteLine("такого элемента нет");
}
еще
{
    Console.WriteLine($"значение элемента {n} строки и {m} столбца равно {numbers[n-1,m-1]}");
}

РаспечататьМассив(числа);

недействительным FillArrayRandomNumbers (массив int [,])
{
    for (int i = 0; i < array.GetLength(0); i++)
        {        
            for (int j = 0; j < array.GetLength(1); j++)
            {
                массив [i,j] = новый Random().Next(-100, 100)/10;
            }   
        }
}

недействительным PrintArray (массив int [,])
{
    for (int i = 0; i < array.GetLength(0); i++)
    {
        Консоль.Написать("[ ");
        for (int j = 0; j < array.GetLength(1); j++)
        {
            Console.Write(массив [i,j] + " ");
        }   
        Console.Write("]");
        Консоль.WriteLine("");
    }
}


//Задача 52: Задайте двумерный массив из множественных чисел. Появляются среднее арифметическое элементы в каждом столбце.

Console.WriteLine("введите количество строк");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("введите количество столбцов");
int m = Convert.ToInt32(Console.ReadLine());

int[,] numbers = new int[n, m];
FillArrayRandomNumbers(числа);


for (int j = 0; j < number.GetLength(1); j++)
{
    двойное среднее = 0;
    for (int i = 0; i < numbers.GetLength (0); i++)
    {
        среднее = (среднее + числа [i, j]);
    }
    среднее = среднее/n;
    Console.Write(среднее + "; ");
}
Консоль.ЗаписьЛинии();
РаспечататьМассив(числа);



недействительным FillArrayRandomNumbers (массив int [,])
{
    for (int i = 0; i < array.GetLength(0); i++)
    {
        for (int j = 0; j < array.GetLength(1); j++)
        {
            array[i, j] = new Random().Next(0, 10);
        }
    }
}

недействительным PrintArray (массив int [,])
{

    for (int i = 0; i < array.GetLength(0); i++)
    {
        Консоль.Написать("[ ");
        for (int j = 0; j < array.GetLength(1); j++)
        {
            Console.Write(массив [i, j] + " ");
        }
        Console.Write("]");
        Консоль.WriteLine("");
    }
}
