// int string bool float double
// int a = 10;
// string b = "hello";
// bool c = true; // false
// float d = 15.4f;
// dooble e =15.4f;

// Тип данных int 
// = присваиваем значение
// string user_name = "Andrey"
// = присвоить
// == сравнить


while (true)
{Console.WriteLine("Введите оператор +/-/*/: или end для выхода");
    string Operator = Console.ReadLine();
    if (Operator == "end")
    {
        break;
    }
    Console.WriteLine("Введите 1 число");
    int number1 = Convert.ToInt32(Console.ReadLine());
    Console.WriteLine("Введите 2 число");
    int number2 = Convert.ToInt32(Console.ReadLine());
if (Operator == "+"){
   Console.WriteLine(number1 + number2); 
}
    else if (Operator == "-")
    {
        Console.WriteLine(number1 - number2);
    }
    else if (Operator == "*")
    {
        Console.WriteLine(number1 * number2);
    }
    else if (Operator == ":")
    {
        Console.WriteLine(number1 / number2);
    }



} 

using System;
 
namespace HelloApp
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Введите первое число: ");
            int num1 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Введите второе число: ");
            int num2 = Convert.ToInt32(Console.ReadLine());
 
            if(num1 > num2)
            {
                Console.WriteLine("Первое число больше второго");
            }
            else if (num1 < num2)
            {
                Console.WriteLine("Первое число меньше второго");
            }
            else
            {
                Console.WriteLine("Оба числа равны");
            }
            Console.ReadKey();
        }
    }
}

1
2
3
4
5
6
7
8
9
10
11
12
13
14
a = int(input())
b = int(input())
c = int(input())
 
res = []
res.append(a)
res.append(b)
res.append(c)
 
print(max(res))
res.remove(max(res))
print(min(res))
res.remove(min(res))
print(res[0])


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
 
namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int a;                             
            Console.Write("введите число: ");
            a= Console.Read();
 
            if (a % 2==1)
            {
                Console.WriteLine("число нечетное");
           
            }
            else
            {
                Console.WriteLine("Число четное");
            }
 
            Console.ReadKey();
        }
    }
}


 
for (int x = 2; x < 101; x++)       
if (x%2==0)            
Console.WriteLine(x);