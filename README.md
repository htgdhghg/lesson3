// Задача 41. Пользователь вводит с клавиатуры M чисел. Почитайте, сколько чисел больше 0 ввёл пользователей.
// 0, 7, 8, -2, -2 -> 2
// -1, -7, 567, 89, 223-> 3

Консоль.Очистить();

Console.WriteLine($"Задача 41. Cколько чисел больше 0 ввёл пользователей \n");
Console.Write($"Введите число М(количество чисел): ");
int m = Convert.ToInt32(Console.ReadLine());
int[] massNumbers = новый int[m];

недействительными InputNumbers (int m) {
для (целое я = 0; я < м; я ++)
  {
    Console.Write($"Введите {i+1} число: ");
    массивныеЧисла[i] = Convert.ToInt32(Console.ReadLine());
  }
}


int Сравнение (int [] массивные числа)
{
  количество счетчиков = 0;
  for (int я = 0; я < массивныйNumbers.Length; я ++)
  {
    если (massiveNumbers[i] > 0 ) count += 1;
  }
  количество возвратов;
}

InputNumbers (м);

Console.WriteLine($"Введено чисел больше 0: {Comparison(massiveNumbers)} ");

// Задача 43. Напишите программу, которая найдёт точку пересечения двух прав, заданных задачами y = k1 * x + b1, y = k2 * x + b2; значения b1, k1, b2 и k2 задаются пользователем.
// b1 = 2, k1 = 5, b2 = 4, k2 = 9 -> (-0,5; 5,5)


Console.WriteLine($"\nЗадача 43. Найти точку пересечения двух прав \n");

double[,] coeff = new double[2, 2];
двойной[] crossPoint = новый двойной[2];

недействительными входными коэффициентами () {
  for (int i = 0; i < coeff.GetLength(0); i++)
  {
    Console.Write($"Введите коэффициенты {i+1}-го уравнения (y = k * x + b):\n");
    for (int j = 0; j < coeff.GetLength(1); j++)
    {
      if(j==0) Console.Write($"Включить коэффициент k: ");
      else Console.Write($"Ввести коэффициент b: ");
      coeff[i,j] = Convert.ToInt32(Console.ReadLine());
    }
  }
}

double[] Решение(double[,] coeff)
{
  crossPoint[0] = (coeff[1,1] - coeff[0,1]) / (coeff[0,0] - coeff[1,0]);
  crossPoint[1] = crossPoint[0] * coeff[0,0] + coeff[0,1];
  вернуть точку пересечения;
}

void OutputResponse (двойной [,] коэф.)
{
  if (coeff[0,0] == coeff[1,0] && coeff[0,1] == coeff[1,1])
  {
    Console.Write($"\nПрямые совпадают");
  }
  иначе если (coeff[0,0] == coeff[1,0] && coeff[0,1] != coeff[1,1])
  {
    Console.Write($"\nПрямые симметричны");
  }
  еще
  {
    Решение(коэфф);
    Console.Write($"\nТочка пересечения прав: ({crossPoint[0]}, {crossPoint[1]})");
  }
}

ВходныеКоэффициенты();
Выходной ответ (коэффициент); 