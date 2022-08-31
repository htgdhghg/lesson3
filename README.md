//Задача 54: Задайте двумерный массив. Напишите программу, которая упорядочивает по убыванию элементов каждой строки двумерного массива.

Консоль.Очистить();
Console.WriteLine($"Задача 54: Задайте двумерный массив. Напишите программу, которая упорядочивает по убыванию элементов каждой строки двумерного массива.");
Console.WriteLine($"\nВведите размер массива mxn и диапазон случайных значений:");
int m = InputNumbers("Введите m: ");
int n = InputNumbers("Введите n: ");
int range = InputNumbers("Включить диапазон: от 1 до ");

int[,] массив = новый int[m, n];
СоздатьМассив(массив);
ЗаписатьМассив(массив);

Console.WriteLine($"\nОтсортированный массив: ");
OrderArrayLines(массив);
ЗаписатьМассив(массив);

недействительным OrderArrayLines (массив int [,])
{
  for (int i = 0; i < array.GetLength(0); i++)
  {
    for (int j = 0; j < array.GetLength(1); j++)
    {
      for (int k = 0; k < array.GetLength(1) - 1; k++)
      {
        если (массив [i, k] < массив [i, k + 1])
        {
          int temp = массив [i, k + 1];
          массив [i, k + 1] = массив [i, k];
          массив [я, к] = темп;
        }
      }
    }
  }
}

int InputNumbers (строковый ввод)
{
  Консоль.Запись(ввод);
  int output = Convert.ToInt32(Console.ReadLine());
  обратный вывод;
}

недействительным CreateArray (массив int [,])
{
  for (int i = 0; i < array.GetLength(0); i++)
  {
    for (int j = 0; j < array.GetLength(1); j++)
    {
      массив [i, j] = новый Random(). Далее (диапазон);
    }
  }
}

недействительным WriteArray (массив int [,])
{
  for (int i = 0; i < array.GetLength(0); i++)
  {
    for (int j = 0; j < array.GetLength(1); j++)
    {
      Console.Write(массив [i, j] + " ");
    }
    Консоль.ЗаписьЛинии();
  }
}


// Задача 56: Задайте прямоугольный двумерный массив. Напишите программу, которая будет находить кожу с наименьшим количеством элементов.

Консоль.Очистить();
Console.WriteLine($"Задача 56: Задайте прямоугольный двумерный массив. Напишите программу, которая будет находить строку с наименьшей суммой элементов.");
Console.WriteLine($"\nВведите размер массива mxn и диапазон случайных значений:");
int m = InputNumbers("Введите m: ");
int n = InputNumbers("Введите n: ");
int range = InputNumbers("Включить диапазон: от 1 до ");

int[,] массив = новый int[m, n];
СоздатьМассив(массив);
ЗаписатьМассив(массив);

интервал minSumLine = 0;
int sumLine = SumLineElements (массив, 0);
for (int i = 1; i < array.GetLength(0); i++)
{
  int tempSumLine = SumLineElements (массив, i);
  если (sumLine > tempSumLine)
  {
    СуммаСтрока = временнаяСуммаСтрока;
    минимальнаяСуммаЛиния = я;
  }
}

Console.WriteLine($"\n{minSumLine+1} - строки с наименьшей суммой ({sumLine}) элементов ");


int SumLineElements (int [,] массив, int i)
{
  int sumLine = массив [i, 0];
  for (int j = 1; j < array.GetLength(1); j++)
  {
    sumLine += массив[i,j];
  }
  вернуть суммуСтрока;
}

int InputNumbers (строковый ввод)
{
  Консоль.Запись(ввод);
  int output = Convert.ToInt32(Console.ReadLine());
  обратный вывод;
}

недействительным CreateArray (массив int [,])
{
  for (int i = 0; i < array.GetLength(0); i++)
  {
    for (int j = 0; j < array.GetLength(1); j++)
    {
      массив [i, j] = новый Random(). Далее (диапазон);
    }
  }
}

void WriteArray (массив int[,])
{
  for (int i = 0; i < array.GetLength(0); i++)
  {
    for (int j = 0; j < array.GetLength(1); j++)
    {
      Console.Write(массив [i,j] + " ");
    }
    Консоль.ЗаписьЛинии();
  }
}


// Задача 58: Задайте две матрицы. Напишите программу, которая будет находить две матрицы произведения.

Консоль.Очистить();
Console.WriteLine($"Задача 58: Задайте две матрицы. Напишите программу, которая будет находить произведение двух матриц.\n\nСразу задаем матрицу, которую можно перемножить, т.е. количество столбцов первого равно количеству строк второй");
Console.WriteLine($"\nВведите размеры матрицы и диапазон случайных значений:");
int m = InputNumbers("Введите число строк 1-й матрицы: ");
int n = InputNumbers("Введите число столбцов 1-й матрицы (и строк 2-й): ");
int p = InputNumbers("Введите число столбцов 2-й матрицы: ");
int range = InputNumbers("Включить диапазон случайных чисел: от 1 до ");

int[,] firstMartrix = new int[m, n];
СоздатьМассив(перваяМатрица);
Console.WriteLine($"\nПервая матрица:");
WriteArray (первая матрица);

int[,] secomdMartrix = new int[n, p];
CreateArray (вторая матрица);
Console.WriteLine($"\nВторая матрица:");
WriteArray (вторая матрица);

int[,] resultMatrix = new int[m,p];

MultiplyMatrix (первая матрица, вторая матрица, результирующая матрица);
Console.WriteLine($"\nПроведение первой и второй матрицы:");
ЗаписатьМассив(РезультатМатрица);

void MultiplyMatrix(int[,] firstMartrix, int[,] secondMartrix, int[,] resultMatrix)
{
  for (int i = 0; i < resultMatrix.GetLength (0); i++)
  {
    for (int j = 0; j <resultMatrix.GetLength(1); j++)
    {
      целая сумма = 0;
      for (int k = 0; k < firstMartrix.GetLength(1); k++)
      {
        сумма += первая матрица [i, k] * вторая матрица [k, j];
      }
      Матрица результата[i,j] = сумма;
    }
  }
}

int InputNumbers (строковый ввод)
{
  Консоль.Запись(ввод);
  int output = Convert.ToInt32(Console.ReadLine());
  обратный вывод;
}

недействительным CreateArray (массив int [,])
{
  for (int i = 0; i < array.GetLength(0); i++)
  {
    for (int j = 0; j < array.GetLength(1); j++)
    {
      массив [i, j] = новый Random(). Далее (диапазон);
    }
  }
}

void WriteArray (массив int[,])
{
  for (int i = 0; i < array.GetLength(0); i++)
  {
    for (int j = 0; j < array.GetLength(1); j++)
    {
      Console.Write(массив [i,j] + " ");
    }
    Консоль.ЗаписьЛинии();
  }
}


// Задача 60: Сформируйте трехмерный массив из неповторяющихся двузначных чисел. Напишите программу, которая будет построчно выводить массив, добавляя индексы каждого элемента.

Консоль.Очистить();
Console.WriteLine($"Задача 60: Сформируйте трехмерный массив из неповторяющихся двузначных чисел. Напишите программу, которая будет построчно выводить массив, добавляя индексы каждого элемента.");
Console.WriteLine($"\nВведите размер массива X x Y x Z:");
int x = InputNumbers("Введите X: ");
int y = InputNumbers("Введите Y: ");
int z = InputNumbers("Введите Z: ");
Console.WriteLine($"");

int[,,] array3D = новый int[x, y, z];
СоздатьМассив(массив3D);
ЗаписатьМассив(массив3D);

int InputNumbers (строковый ввод)
{
  Консоль.Запись(ввод);
  int output = Convert.ToInt32(Console.ReadLine());
  обратный вывод;
}

void WriteArray (int[,,] array3D)
{
  for (int i = 0; i < array3D.GetLength(0); i++)
  {
    for (int j = 0; j < array3D.GetLength(1); j++)
    {
      Console.Write($"X({i}) Y({j}) ");
      for (int k = 0; k < array3D.GetLength(2); k++)
      {
        Console.Write($"Z({k})={array3D[i,j,k]}; ");
      }
      Консоль.ЗаписьЛинии();
    }
    Консоль.ЗаписьЛинии();
  }
}

недействительным CreateArray (int [,,] array3D)
{
  int[] temp = new int[array3D.GetLength(0) * array3D.GetLength(1) * array3D.GetLength(2)];
  внутренний номер;
  for (int я = 0; я < temp.GetLength (0); я ++)
  {
    temp[i] = новый Random().Next(10, 100);
    число = темп[i];
    если (я >= 1)
    {
      для (int j = 0; j < i; j++)
      {
        пока (temp[i] == temp[j])
        {
          temp[i] = новый Random().Next(10, 100);
          j = 0;
          число = темп[i];
        }
          число = темп[i];
      }
    }
  }
  количество счетчиков = 0;
  for (int x = 0; x < array3D.GetLength(0); x++)
  {
    for (int y = 0; y < array3D.GetLength(1); y++)
    {
      for (int z = 0; z < array3D.GetLength(2); z++)
      {
        array3D[x, y, z] = temp[count];
        количество++;
      }
    }
  }
}


// Задача 62: Напишите программу, которая заполнит спирально массив 4 на 4.
// Например, на выходе получается вот такой массив:
// 01 02 03 04
// 12 13 14 5
// 11 16 15 6
// 10 9 8 7

Консоль.Очистить();
Console.WriteLine($"Задача 62: Заполнить спирально массив 4 на 4.");

инт п = 4;
int[,] sqareMatrix = new int[n, n];

инт темп = 1;
интервал я = 0;
интервал j = 0;

в то время как (temp <= sqareMatrix.GetLength(0) * sqareMatrix.GetLength(1))
{
  sqareMatrix[i, j] = temp;
  темп++;
  если (i <= j + 1 && i + j < sqareMatrix.GetLength(1) - 1)
    j++;
  иначе, если (i < j && i + j >= sqareMatrix.GetLength(0) - 1)
    я++;
  иначе, если (i >= j && i + j > sqareMatrix.GetLength(1) - 1)
    ж--;
  еще
    я--;
}

ЗаписатьМассив(КвадратнаяМатрица);

void WriteArray (массив int[,])
{
  for (int i = 0; i < array.GetLength(0); i++)
  {
    for (int j = 0; j < array.GetLength(1); j++)
    {
      если (массив[i,j]/10 <= 0)
      Console.Write($"{массив[i,j]}");

      еще Console.Write($"{массив [i,j]} ");
    }
    Консоль.ЗаписьЛинии();
  }
}
