## Тема 1: ООП

1.	Задание: Создайте класс Person с полями name и age. Добавьте метод introduce(), который выводит строку вида: "Привет! Меня зовут [name], и мне [age] лет."

Пример вызова:
```kotlin
fun main() {
    val person = Person("Алиса", 25)
    person.introduce()
}
```

---

2.	Задание: Реализуйте класс Employee, наследующий Person. Добавьте поле position (должность) и переопределите метод introduce() так, чтобы он выводил строку: "Привет! Меня зовут [name], и я работаю [position]."

Пример вызова:
```kotlin
fun main() {
    val employee = Employee("Боб", 30, "программист")
    employee.introduce()
}
```

---

3.	Задание: Реализуйте абстрактный класс Shape с методом area(): Double. Создайте два класса-наследника: Circle (с полем radius) и Rectangle (с полями width и height). Реализуйте метод area() для каждого из классов.

Пример вызова:
```kotlin
fun main() {
    val shapes = listOf(
        Circle(5.0),
        Rectangle(4.0, 6.0)
    )
    shapes.forEach { printShapeInfo(it) }
}
```

---

## Тема 2: Функциональное программирование

1.	Задание: Напишите функцию filterEvenNumbers, которая принимает список чисел и возвращает только чётные числа. Используйте лямбда-выражение.

Пример вызова:
```kotlin
fun main() {
    val numbers = listOf(1, 2, 3, 4, 5, 6)
    println(filterEvenNumbers(numbers)) // Ожидаемый результат: [2, 4, 6]
}
```

---

2.	Задание: Реализуйте функцию transformNames, которая принимает список строк и возвращает список в формате: "[Имя: имя]". Используйте map.

Пример вызова:
```kotlin
fun main() {
    val names = listOf("Алиса", "Боб", "Клара")
    println(transformNames(names)) // Ожидаемый результат: ["[Имя: Алиса]", "[Имя: Боб]", "[Имя: Клара]"]
}
```

---

3.	Задание: Напишите функцию groupAndCount, которая принимает список строк и возвращает карту, где ключ — это первая буква строки, а значение — количество строк с этой буквы. Используйте groupBy и mapValues.

Пример вызова:
```kotlin
fun main() {
    val words = listOf("apple", "banana", "apricot", "blueberry", "cherry")
    println(groupAndCount(words)) // Ожидаемый результат: {a=2, b=2, c=1}
}
```

---

4. Задание: Реализуйте функцию applyToEach, которая принимает список чисел и лямбда-выражение. Функция должна применять переданную лямбду к каждому элементу списка и возвращать новый список с результатами.

Пример вызова:
```kotlin
fun main() {
    val numbers = listOf(1, 2, 3, 4, 5)
    val result = applyToEach(numbers) { it * 2 }
    println(result) // Ожидаемый результат: [2, 4, 6, 8, 10]
}
```

---

5. Задание: Напишите функцию filterAndTransform, которая принимает список строк и два лямбда-выражения: одно для фильтрации, другое для преобразования. Функция должна вернуть новый список, отфильтрованный и преобразованный в соответствии с лямбдами.

```kotlin
fun main() {
    val words = listOf("cat", "dog", "elephant", "crow")
    val result = filterAndTransform(words, { it.length > 3 }, { it.uppercase() })
    println(result) // Ожидаемый результат: ["ELEPHANT", "CROW"]
}
```

---

6. Задание: Напишите функцию-расширение для списка List<Int> под названием sumEvenNumbers, которая возвращает сумму всех чётных чисел в списке.

```kotlin
fun main() {
    val numbers = listOf(1, 2, 3, 4, 5, 6)
    println(numbers.sumEvenNumbers()) // Ожидаемый результат: 12
}
```

---

7. Задание: Напишите функцию-расширение для класса String под названием isPalindrome, которая проверяет, является ли строка палиндромом (одинаково читается слева направо и справа налево).

```kotlin
fun main() {
    val word = "level"
    println(word.isPalindrome()) // Ожидаемый результат: true
    println("hello".isPalindrome()) // Ожидаемый результат: false
}
```
