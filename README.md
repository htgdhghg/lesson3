// Задача 34: Задать массивный массив случайных вычислений трехзначными числами. Напишите программу, которая показывает количество считываемых чисел в массиве.
// [345, 897, 568, 234] -> 2

Консоль.Очистить();
Console.WriteLine($"Задача 34. Количество чётных чисел в массиве:\n");
int[] числа = новый int[10];

void FillArray (массив int [], int min, int max) {
  for (int i = 0; i<array.Length; i++) {
    array[i] = new Random(). Next(min, max);
  }
}

недействительным WriteArray (массив int []) {
    for (int i = 0; i<array.Length; i++) {
    Console.Write(массив[i] + " ");
  }
  Консоль.ЗаписьЛинии();
}

int QuantityPositive (массив int []) {
    целое количество = 0;
    for (int i = 0; i<array.Length; i++) {
    если (массив [i] % 2 == 1)
    {
      количество++;
    }
  }
  возвращаемое количество;
}

ЗаполнитьМассив(числа, 100, 1000);
ЗаписатьМассив(числа);
Консоль.ЗаписьЛинии();

int количество = QuantityPositive (числа);
Console.WriteLine($"Количество чётных чисел в массиве: {quantity}");


// Задача 36: Задайте одномерный массив, зарегистрированный случайными числами. Появляются количества элементов, стоящих на нечётных позициях.
// [3, 7, 23, 12] -> 19
// [-4, -6, 89, 6] -> 0


// Консоль.Очистить();
Console.WriteLine($"\nЗадача 36. Сумма элементов, стоящих на нечётных позициях:\n");
Console.Write($"Введите количество элементов массива: ");
int numberElements = Convert.ToInt32(Console.ReadLine());

int RandomNumbers (int numberElements, int min, int max)
  {
  int[] randomNumbers = новый int[numberElements];
  интервал элементов = 0;
  Console.Write("Получившийся массив: ");

    for (int i = 0; i <randomNumbers.Length; i++) {
      randomNumbers[i] = new Random().Next(min, max);

      Console.Write(randomNumbers[i] + " ");

      если (я % 2 != 1)
      {
        sumElements = sumElements + randomNumbers[i];
      }
    }
  вернуть элементы суммы;
  }

int randomNumbers = RandomNumbers (numberElements, 1, 10);

Console.WriteLine($"\nСумма элементов, стоящих на нечётных позициях: {randomNumbers}");


// Задача 38: Задайте массив множественных чисел. Внешний вид между максимальным и наличием элементов массива.
// [3 7 22 2 78] -> 76

Console.WriteLine($"\nЗадача 38. Выявленные различия между максимальным и присутствием массива элементов из выделенных чисел:\n");

double[] arrayRealNumbers = new double[10];
  for (int i = 0; i < arrayRealNumbers.Length; i++)
  {
    arrayRealNumbers[i] = new Random().Next(1, 10);
    Console.Write(arrayRealNumbers[i] + " ");
  }

двойное максимальное число = массив реальных чисел [0];
двойное минимальное число = массив реальных чисел [0];

  for (int i = 1; i < arrayRealNumbers.Length; i++)
  {
    если (maxNumber < arrayRealNumbers[i])
    {
      maxNumber = arrayRealNumbers[i];
    }
        если (minNumber > arrayRealNumbers[i])
    {
      minNumber = arrayRealNumbers[i];
    }
  }

  двойное решение = maxNumber - minNumber;

  Console.WriteLine($"\nразница между максимальным ({maxNumber}) и владением({minNumber}) приложениями: {decision}");


  // Задача 35: Задайте одномерный массив из 123 случайных чисел. Найдите количество элементов массива, значения которых лежат в отрезке [10,99].

int[] array = new int[123];
int count=0;

for (int i = 0; i < array.Length; i++)
{
    array[i] = new Random().Next(0, 1000);
    Console.Write(array[i] + " ");
}
Console.WriteLine();
for (int j = 0; j < array.Length; j++)
{
    if(array[j] > 9 & array[j] < 100) count = count + 1;
}
Console.WriteLine();
Console.Write("Массив совержит следующее количество элементов из отрезка [10,99] - ");
Console.Write(count);


// Задача 37: Найдите произведение пар чисел в одномерном массиве. Парой считаем первый и последний элемент, второй и предпоследний и т.д. Результат запишите в новом массиве.

int N = 10;
int[] array = new int[N];

for (int i = 0; i < array.Length; i++)
{
    array[i] = new Random().Next(0, 10);
    Console.Write(array[i] + " ");
}
Console.WriteLine();

int j = array.Length - 1;
for (int i = 0; i < (array.Length + 1) / 2; i++)
{
    Console.Write(array[i] * array[j] + " ");
    j--;
}
