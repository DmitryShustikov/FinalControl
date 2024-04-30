### Ввод исходного массива строк с клавиатуры

```
 Console.Write("Введите элементы массива через пробел: ");
```
### Формирование нового массива строк с длиной меньше или равной 3 символами

```
string[] resultArray = FilterArray(inputArray);
```
### Вывод нового массива
```
Console.WriteLine("Новый массив строк:");
```
### Проходим по всем строкам массива
```
foreach (string str in resultArray)
```
### Эта функция принимает исходный массив строк в качестве аргумента, фильтрует его и возвращает новый массив, содержащий только строки с длиной меньше или равной 3 символам. 
```
string[] FilterArray(string[] inputArray)
```

### Создание нового массива подходящих строк и счетчика
```
string[] resultArray = new string[inputArray.Length];
        int count = 0;
```
### Фильтрация исходного массива и добавление подходящих строк в новый массив
```
foreach (string str in inputArray)
        {
            if (str.Length <= 3)
            {
                resultArray[count] = str;
                count++;
            }
        }
```
### Обрезаем resultArray до фактической длины и выводим на экран
```
Array.Resize(ref resultArray, count);
        return resultArray;
```
