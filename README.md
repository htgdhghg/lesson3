// Задача 19: Напишите программу, которая принимается на пятизначное число и возникает, если оно палиндромом.
// 14212 -> нет
// 23432 -> да
// 12821 -> да

Console.WriteLine("Задача 19");
Console.Write("Введите число: ");
нить? номер = Console.ReadLine();

void CheckingNumber (номер строки) {
  если (число[0]==число[4] || число[1]==число[3]){
    Console.WriteLine($"Ваше число: {number} - палиндром.");
  }
  else Console.WriteLine($"Ваше число: {number} - НЕ палиндром.");
}

если (число!.Длина == 5){
  Контрольный номер(число);
}
else Console.WriteLine($"Введите правильное число");


// Задача 21: Напишите программу, которая принимает вход в координаты двух точек и нахождение расстояния между ними в 3D-пространствах.
// А (3,6,8); В (2,1,-7), -> 15,84
// А (7,-5, 0); В (1,-1,9) -> 11,53

Console.WriteLine("\n Задача 21");
int x1 = Координата ("x", "A");
int y1 = Координата ("y", "A");
int z1 = Координата ("z", "A");
int x2 = Координата ("x", "B");
int y2 = Координата ("y", "B");
int z2 = Координата ("z", "B");

int Coordinate (строка coorName, строка pointName)
{
    Console.Write($"Ввести координату {coorName} точки {pointName}: ");
    вернуть Convert.ToInt16(Console.ReadLine());
}

двойное решение(двойное x1, двойное x2,
                двойной у1, двойной у2,
                двойной z1, двойной z2){
  вернуть Math.Sqrt(Math.Pow((x2-x1), 2) +
                   Math.Pow((y2-y1), 2) +
                   Math.Pow((z2-z1), 2));
}

double segmentLength = Math.Round (Решение (x1, x2, y1, y2, z1, z2), 2 );

Console.WriteLine($"Длина отрезка {segmentLength}");


//Задача 23: Напишите программу, которая принимает на вход число (N) и выдает таблетку кубов числами от 1 до N.
// 3 -> 1, 8, 27
// 5 -> 1, 8, 27, 64, 125

Console.WriteLine("\n Задача 23");
Console.Write("Введите число: ");
куб int = Convert.ToInt32(Console.ReadLine());

пустой куб (int [] куб) {
  Целый счетчик = 0;
  целая длина = куб.Длина;
  в то время как (счетчик < длина) {
    куб[счетчик] = Convert.ToInt32(Math.Pow(счетчик, 3));
    счетчик++;
  }
}

недействительным PrintArry (int [] колл) {
  int count = кол.Длина;
  внутренний индекс = 0;
  в то время как (индекс < количество) {
    Console.Write(coll[index]+ " ");
    индекс++;
  }
}

int[] массив = новый int[cube+1];
Куб(арри);
РаспечататьАрри(Арри);

