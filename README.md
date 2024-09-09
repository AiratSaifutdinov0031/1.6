Легенда:
Вы пришли в магазин, чтобы обменять своё золото на кристаллы. У вас есть определённое количество золота, и продавец спрашивает, сколько кристаллов вы хотите приобрести. После покупки у вас останется часть золота и появятся кристаллы.
Формально:
При запуске программы пользователь вводит количество золота. Затем ему предлагается купить кристаллы по установленной цене N (задать в программе). Пользователь вводит количество кристаллов, и его золото конвертируется. 
Выведите остаток золота и количество кристаллов. Проверка на достаточность золота не требуется.

ОТВЕТ:

В данной программе мы реализуем три переменных типа int, но в последнем мы указываем установленную цену N за одну единицу кристалла. Выбор переменной int свзяан с целыми числами и без остатка. В случае. когда количество монет меньше стоимости нужных кристаллов выводится результат
операции, но с отрицательным количеством золота

using System;

namespace MyFirstApp
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            int goldCount;
            int crystalsCount;
            int сrystalPrice = 3;

            Console.WriteLine("Вы находитесь в обменом пункте, где производится обмен золота на кристаллы.");
            Console.Write("Сколько у вас золота? Введите количество: ");
            goldCount = Convert.ToInt32(Console.ReadLine());
            Console.Write("Какое количество кристаллов вы хотите купить? Введите число: ");
            crystalsCount = Convert.ToInt32(Console.ReadLine());

            goldCount -= crystalsCount * сrystalPrice;

            Console.WriteLine($"Ваш баланс: {crystalsCount} кристаллов, {goldCount} золота.");
        }
    }
}