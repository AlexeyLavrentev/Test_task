# Итоговая проверочная работа первого блока обучения по программе РАЗРАБОТЧИК
## Задание

    Создать репозиторий на GitHub
    Нарисовать блок-схему алгоритма
    Снабдить репозиторий оформленным текстовым описанием решения (файл README.md)
    Написать программу, решающую поставленную задачу
    Использовать контроль версий в работе над этим небольшим проектом

### Задача

Написать программу, которая из имеющегося массива строк формирует массив из строк, длина которых меньше, либо равна 3 символа. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

Выполнение:

Блок-схема задачи представлена в [файле](https://github.com/AlexeyLavrentev/Test_task/blob/main/%D0%91%D0%BB%D0%BE%D0%BA-%D1%81%D1%85%D0%B5%D0%BC%D0%B0%20%D0%B0%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC%D0%B0.jpg)

Текст программы на языке программирования C#

```
string[] source = { "one", "two", "34", "District", "Vi", "один", "Book", "Woo", "Normal" };

void PrintArray(string[] m)
{
    for (int x = 0; x < m.Length; x++)
        Console.Write($"\"{m[x]}\" ");
    Console.WriteLine();
}
string[] copyStringsBelowOrEqual3InNewArray(string[] strArray)
{
    int k = 0;
    for (int i = 0; i < strArray.Length; i++)
        if (strArray[i].Length <= 3) k++;
    string[] newArray = new string[k];
    k = 0;
    for (int i = 0; i < strArray.Length; i++)
        if (strArray[i].Length <= 3) newArray[k++]=strArray[i];

    return newArray;
}

Console.WriteLine("Исходный массив строк:");
PrintArray(source);
string[] target = copyStringsBelowOrEqual3InNewArray(source);
Console.WriteLine("Результат:");
PrintArray(target);
Console.WriteLine();
```
