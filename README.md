## Список вопросов к зачету

1. В чем разница `=` и `:=` в присвоении переменной значения? [answer](#1-разница-между--и--в-присвоении-переменной-значения)
2. На что влияет регистр первой буквы в имени переменной/типа/функции (`Hello` vs `hello`)? [answer](#2-влияние-регистра-первой-буквы-в-имени-переменнойтипафункции)
3. Чем инициализируется вновь созданная переменная, если явно не указывать значение (`var x int`)? [answer](#3-инициализация-новой-переменной-по-умолчанию)
4. В какой момент инициализируются глобальные переменные? [answer](#4-момент-инициализации-глобальных-переменных)
5. Как будет вести себя краткий синтаксис инициализации (`:=`) в конструкции `i, j := 1, 2` в зависимости от статуса "объявленности" переменных `i` и `j` в коде выше? [answer](#5-поведение-краткого-синтаксиса-инициализации-с-)
6. Что такое указатель и какие операции с ним можно произвести? [answer](#6-что-такое-указатель-и-операции-с-ним)
7. Как передаются агрументы в функцию (по значению, по ссылке)? Всегда ли? [answer](#7-передача-аргументов-в-функцию)
8. Что делает функция `new`? [answer](#8-что-делает-функция-new)
9. Корректно ли возвращать из функции указатель на локальную переменную? Почему? [answer](#9-возвращение-указателя-на-локальную-переменную)
10. Что такое escape analysis? [answer](#10-что-такое-escape-analysis)
11. Для чего вместо имени переменной иногда используют `_`? Приведите примеры. [answer](#11-использование-_-вместо-имени-переменной)
12. Чем особенна функция `func init() {...}`? Когда она вызывается? [answer](#12-функция-func-init-)
13. Разрешены ли циклические импорты пакетов? Если да, то как разрешается последовательность инициализации? [answer](#13-циклические-импорты-пакетов)
14. Что такое область видимости переменной? [answer](#14-область-видимости-переменной)
15. Как работает область видимости переменной при наличии вложенных областей? [answer](#15-область-видимости-переменной-при-вложенных-областях)
16. В чем особенность `:=` при перекрытии (shadow) имен переменных во вложенной области видимости? [answer](#16-особенность--при-перекрытии-имен-переменных)
17. Какие значения будут принимать переменные `i` и `j` в цикце `for i, j := range "Hello, Мир!"`? Почему? [answer](#17-значения-переменных-i-и-j-в-цикле-for-i-j--range-hello-мир)
18. Что такое `iota`? Для чего используется? [answer](#18-что-такое-iota)
19. Как устроен внутри слайс? Как узнать его длину и емкость? [answer](#19-структура-слайса)
20. При передачу внутрь функции слайс передается по ссылке или по значению? Почему? [answer](#20-передача-слайса-в-функцию)
21. Как работает функция `append`? [answer](#21-как-работает-функция-append)
22. Как работает сабслайсинг (оператор `[:]`)? [answer](#22-как-работает-сабслайсинг-оператор-)
23. Валидно ли использовать неинициализированные slice и map (т.е. равные `nil`)? [answer](#23-использование-неинициализированных-slice-и-map-равные-nil)
24. Как с помощью функции `append` вставить элемент в середину слайса? [answer](#24-как-вставить-элемент-в-середину-слайса-с-помощью-append)
25. Какая структура данных (с т.з. алгоритмов) лежит в основе `map`? [answer](#25-какая-структура-данных-лежит-в-основе-map)
26. Как можно инициализировать `map`? [answer](#26-как-можно-инициализировать-map)
27. Что произойдет, если в `map` обратиться по несуществующему (в нем) ключу? [answer](#27-что-произойдет-если-обратиться-по-несуществующему-ключу-в-map)
28. Как проверить, что ключа нет в `map`? [answer](#28-как-проверить-что-ключа-нет-в-map)
29. Можно ли взять адрес от элемента, лежащего в `map`? [answer](#29-можно-ли-взять-адрес-от-элемента-лежащего-в-map)
30. Какой порядок элементов гарантируется при итерации по `map` через `for-range`? [answer](#30-какой-порядок-элементов-гарантируется-при-итерации-по-map-через-for-range
)
31. На что влияет регистр первой буквы поля или метода в структуре? [answer](#31-на-что-влияет-регистр-первой-буквы-поля-или-метода-в-структуре)
32. Что такое встраивание (embedding) в структурах? [answer](#32-что-такое-встраивание-embedding-в-структурах
)
33. Что такое именованные возвращаемые значения? Как их использовать? [answer](#33-что-такое-именованные-возвращаемые-значения)
34. Что выведет код ниже?
```go
func main() {
	var x = 0
	func() {
		x = 42
	}()
	fmt.Println(x)
}
```
[answer](#34-что-выведет-следующий-код)

35. Какой тип используется для возврата ошибок? Чем он является? [answer](#35-какой-тип-используется-для-возврата-ошибок)

36. Для чего ипользуются `errors.Is` и `errors.As`? В чем между ними разница? [answer](#36-для-чего-используются-errorsis-и-errorsas-в-чем-разница)
37. Что такое `defer`? Приведите сценарий использования? [answer](#37-что-такое-defer-приведите-сценарий-использования)
38. В каком порядке вызываются объявленные в `defer` функции при наличии нескольких объявлений? [answer](#38-в-каком-порядке-вызываются-объявленные-в-defer-функции)
39. Вызывается ли `defer` при панике? [answer](#39-вызывается-ли-defer-при-панике)
40. В какой момент вычисляются аргументы функции, вызываемой в `defer`? [answer](#40-в-какой-момент-вычисляются-аргументы-функции-вызываемой-в-defer)
41. Что такое `panic`? Что происходит в программе, когда вылетает паника? [answer](#41-что-такое-panic-что-происходит-в-программе-когда-вылетает-паника)
42. Как остановить выполнение паники? Что произойдет, если этого не сделать? [answer](#42-как-остановить-выполнение-паники
)
43. В чем разница (в идеологии) между паниками и ошибками? [answer](#43-разница-между-паниками-и-ошибками)
44. В каком месте программы осмысленно использовать функцию `recover`? [answer](#44-в-каком-месте-программы-осмысленно-использовать-функцию-recover)
45. Что такое `receiver` в методе? В чем разница между `pointer receiver` и `value receiver`? [answer](#45-что-такое-receiver-в-методе-в-чем-разница-между-pointer-receiver-и-value-receiver)
46. Что выведется в следующем коде? Почему?
```go
type Foo struct {
}

func (f *Foo) Bar() {
	fmt.Println("Hello!")
}

func main() {
	var m = make(map[int]Foo)
	m[1] = Foo{}
	m[1].Bar()
}
```
[answer](#46-что-выведется-в-следующем-коде-почему)

47. Можно ли вызвать метод на `nil` указателе какого-либо типа? Что произойдет?
[answer](#47-можно-ли-вызвать-метод-на-nil-указателе-какого-либо-типа-что-произойдет)
48. Что такое интерфейс (interface)? Как он устроен?
[answer](#48-что-такое-интерфейс-interface-как-он-устроен)
49. Как указать в типе, что данный тип удовлетворяет некоторому интерфейсу?
[answer](#49-как-указать-в-типе-что-данный-тип-удовлетворяет-некоторому-интерфейсу)
50. В чем разница между nil-интерфейсами и интерфейсами, содержащими nil?
[answer](#50-в-чем-разница-между-nil-интерфейсами-и-интерфейсами-содержащими-nil)
51. Как проверить, какой тип находится за интерфейсом (при условии, что мы предполагаем что там может быть)?
[answer](#51-как-проверить-какой-тип-находится-за-интерфейсом)
52. Что такое `type switch`? В каких сценариях может использоваться?
[answer](#52-что-такое-type-switch-в-каких-сценариях-может-использоваться)
53. Что такое горутина (`goroutine`)? Как запустить горутину?
[answer](#53-что-такое-горутина-goroutine-как-запустить-горутину)
54. Как горутины связаны с потоками ОС? Как работает шедулер?
[answer](#54-как-горутины-связаны-с-потоками-ос-как-работает-шедулер)
55. Что произойдет, если функция `main` завершит исполнение раньше, чем закончится выполянться какая-либо другая горутина? [answer](#55-что-произойдет-если-функция-main-завершит-исполнение-раньше-чем-закончится-выполняться-какая-либо-другая-горутина)
56. Как дождаться выполнения горутины? [answer](#56-как-дождаться-выполнения-горутины)
57. Как вручную задать количество потоков ОС в программе? [answer](#57-как-вручную-задать-количество-потоков-ос-в-программе)
58. Что такое канал (`chan`)? Какие каналы бывают? [answer](#58-что-такое-канал-chan-какие-каналы-бывают)
59. Можно ли читать и писать в/из закрытого канала? [answer](#59-можно-ли-читать-и-писать-виз-закрытого-канала)
60. Как создать канал с размером буфера 10? [answer](#60-как-создать-канал-с-размером-буфера-10)
61. Почему операции записи/чтения в/из канала могут блокироваться? В каких ситуациях блокировки не будет? [answer](#61-почему-операции-записичтения-виз-канала-могут-блокироваться-в-каких-ситуациях-блокировки-не-будет)
62. Как сделать неблокирующее чтение из канала в любом исходе (т.е. даже если в канале ничего нет)? [answer](#62-как-сделать-неблокирующее-чтение-из-канала-в-любом-исходе-те-даже-если-в-канале-ничего-нет)
63. Что такое состояние гонки (race condition)? Приведите пример. [answer](#63-что-такое-состояние-гонки-race-condition-приведите-пример)
64. Для чего используется мьютекс (`sync.Mutex`)? Каков сценарий использования? [answer](#64-для-чего-используется-мьютекс-syncmutex-каков-сценарий-использования)
65. В чем разница между `sync.Mutex` и `sync.RWMutex`? [answer](#65-в-чем-разница-между-syncmutex-и-syncrwmutex)
66. Для чего используется `sync.Once`? Приведите сценарий использования. [answer](#66-для-чего-используется-synconce-приведите-сценарий-использования)
67. Как можно проверить (например, тестами), что в программе нет состояния гонки (race condition)? [answer](#67-как-можно-проверить-например-тестами-что-в-программе-нет-состояния-гонки)
68. В чем разница между blackbox- и whitebox-тестами? Как в Go можно явно сделать blackbox-тесты (технически запретить доступаться до неэкспортируемых сущностей)? [answer](#68-в-чем-разница-между-blackbox--и-whitebox-тестами-как-в-go-можно-явно-сделать-blackbox-тесты)
69. Что такое `generics`? Приведите пример, когда дженерики упрощают написание кода. [answer](#69-что-такое-generics-приведите-пример-когда-дженерики-упрощают-написание-кода)

---
---

# 1. **Разница между `=` и `:=` в присвоении переменной значения**:
   - `=` используется для присвоения значения уже объявленной переменной.
   - `:=` является сокращённой формой для объявления новой переменной с инициализацией её значения. Например, `x := 1` эквивалентно `var x int = 1`.

[Вопросы](#список-вопросов-к-зачету)

# 2. **Влияние регистра первой буквы в имени переменной/типа/функции**:
   - В Go регистр первой буквы имеет значение. Если имя начинается с заглавной буквы (например, `Hello`), это означает, что переменная, функция или тип будут доступны вне пакета (экспортируемые).
   - Если имя начинается со строчной буквы (например, `hello`), то оно будет доступно только внутри пакета (неэкспортируемые).

[Вопросы](#список-вопросов-к-зачету)

# 3. **Инициализация новой переменной по умолчанию**:
   - Если переменная объявляется через `var` без явного указания начального значения, она инициализируется значением по умолчанию для типа. Например, `var x int` инициализируется значением `0`.

[Вопросы](#список-вопросов-к-зачету)

# 4. **Момент инициализации глобальных переменных**:
   - Глобальные переменные (или переменные уровня пакета) инициализируются при загрузке и инициализации пакета, что происходит перед выполнением функции `main`.

[Вопросы](#список-вопросов-к-зачету)

# 5. **Поведение краткого синтаксиса инициализации с `:=`**:
   - Если переменные `i` и `j` уже были объявлены выше по тексту программы, то конструкция `i, j := 1, 2` приведёт к ошибке компиляции, так как краткий синтаксис предполагает объявление новых переменных. Если одна из переменных объявлена, а другая нет, то вторая переменная будет объявлена, а первой будет присвоено новое значение.

[Вопросы](#список-вопросов-к-зачету)

# 6. **Что такое указатель и операции с ним**:
   - Указатель — это переменная, хранящая адрес памяти другой переменной. С указателями можно выполнять следующие операции:
     - Получение адреса переменной: `&x`.
     - Разыменование: получение значения по адресу указателя, например, `*ptr`.
     - Сложение или вычитание целочисленных значений при арифметических операциях с указателями (для перехода к следующим или предыдущим адресам памяти).

[Вопросы](#список-вопросов-к-зачету)

# 7. **Передача аргументов в функцию**:
   - В Go все аргументы передаются в функцию по значению. Это означает, что функция получает копию каждого аргумента. Если аргумент является указателем, то копируется сам указатель, но не значение, на которое он указывает.

[Вопросы](#список-вопросов-к-зачету)


# 8. **Что делает функция `new`**:
   - Функция `new(T)` создаёт переменную типа `T`, инициализирует её значением по умолчанию и возвращает указатель на неё.
[Вопросы](#список-вопросов-к-зачету)

# 9. **Возвращение указателя на локальную переменную**:
   - В Go возвращать указатель на локальную переменную считается безопасным. Компилятор определяет, что переменная "вырывается" за пределы своей области видимости (escape analysis) и выделяет её на куче, а не на стеке.

[Вопросы](#список-вопросов-к-зачету)

# 10. **Что такое escape analysis**:
- Escape analysis — это процесс, используемый компилятором Go для определения, должна ли переменная быть выделена на стеке или на куче. Если переменная используется только внутри функции, она может быть выделена на стеке. Если переменная доступна из других функций или возвращается из функции, она "вырывается" и выделяется на куче для предотвращения ошибок доступа после завершения функции.

[Вопросы](#список-вопросов-к-зачету)


# 11. **Использование `_` вместо имени переменной**:
   - `_` используется в Go, когда необходимо проигнорировать переменную в операции присваивания. Это бывает полезно, когда функция возвращает несколько значений, и некоторые из них нам не нужны.
     ```go
     _, err := someFunction() // Игнорируем первое возвращаемое значение, но обрабатываем ошибку
     ```
[Вопросы](#список-вопросов-к-зачету)


# 12. **Функция `func init() {...}`**:
   - `init` — это специальная функция, которая автоматически вызывается при инициализации пакета, до выполнения функции `main`. Пакет может содержать несколько функций `init`, и все они будут вызваны в порядке их объявления.

[Вопросы](#список-вопросов-к-зачету)


# 13. **Циклические импорты пакетов**:
   - В Go циклические импорты не разрешены. Это означает, что если два разных пакета импортируют друг друга напрямую или косвенно, компилятор выдаст ошибку.

[Вопросы](#список-вопросов-к-зачету)


# 14. **Область видимости переменной**:
   - Область видимости переменной определяет, в какой части программы эта переменная доступна. В Go области видимости могут быть определены блоком (локальная переменная внутри функции), уровнем пакета или глобальным уровнем (если переменная экспортируемая).

[Вопросы](#список-вопросов-к-зачету)


# 15. **Область видимости переменной при вложенных областях**:
   - Переменные во вложенных областях могут перекрывать (shadow) переменные во внешних областях. Например:
     ```go
     var x = "outside"
     func someFunc() {
         var x = "inside"  // Переменная x здесь перекрывает внешнюю переменную x
         fmt.Println(x)    // Выведет "inside"
     }
     ```

[Вопросы](#список-вопросов-к-зачету)


# 16. **Особенность `:=` при перекрытии имен переменных**:
   - Синтаксис `:=` может быть использован для объявления новой переменной во вложенной области, что приведет к перекрытию переменной с тем же именем из внешней области.

[Вопросы](#список-вопросов-к-зачету)


# 17. **Значения переменных `i` и `j` в цикле `for i, j := range "Hello, Мир!"`**:
   - `i` будет индексом каждого символа в строке, а `j` — значением кода руны UTF-8 для каждого символа. Строка в Go — это последовательность рун, и индексация происходит по байтовым позициям, что означает, что символы в UTF-8 могут занимать более одного байта.

| i  | j   |
|----|:-----:|
| 0  | 72  |
| 1  | 101 |
| 2  | 108 |
| 3  | 108 |
| 4  | 111 |
| 5  | 44  |
| 6  | 32  |
| 7  | 1052|
| 9  | 1080|
| 11 | 1088|
| 13 | 33  |



[Вопросы](#список-вопросов-к-зачету)


# 18. **Что такое `iota`**:
   - `iota` — это предопределенный идентификатор в Go для генерации последовательных чисел в `const` блоках, начиная с 0.

[Вопросы](#список-вопросов-к-зачету)


# 19. **Структура слайса**:
   - Слайс в Go состоит из трех компонентов: указатель на массив, длина (количество элементов) и емкость (максимальное количество элементов до расширения массива). Длину и емкость слайса можно узнать с помощью функций `len()` и `cap()` соответственно.

[Вопросы](#список-вопросов-к-зачету)


# 20. **Передача слайса в функцию**:
- Слайс передается в функцию по значению, но так как слайс — это структура содержащая указатель на массив, изменения элементов массива внутри функции изменяют массив на который указывает слайс.

[Вопросы](#список-вопросов-к-зачету)


# 21. **Как работает функция `append`**:
- `append` добавляет элементы в конец слайса. Если в слайсе достаточно емкости для добавления элементов, они добавляются в существующий массив. Если емкости недостаточно, `append` создает новый массив большего размера, копирует существующие элементы и возвращает новый слайс, указывающий на этот новый массив.

[Вопросы](#список-вопросов-к-зачету)


# 22. **Как работает сабслайсинг (оператор `[:]`)?**
   - Сабслайсинг использует оператор `[:]` для получения подмножества слайса. Например, `a[1:4]` возвращает элементы со второго по четвертый. Если опустить первое число (`a[:n]`), сабслайс будет начинаться с начала слайса до `n`, а если второе (`a[m:]`), то с `m` до конца.

[Вопросы](#список-вопросов-к-зачету)


# 23. **Использование неинициализированных slice и map (равные `nil`)**:
   - `nil`-слайс ведёт себя как пустой слайс при большинстве операций, включая добавление элементов через `append`. Однако, неинициализированная (nil) карта не может быть использована для добавления ключей без предварительной инициализации (`make` или литерал карты).

[Вопросы](#список-вопросов-к-зачету)


# 24. **Как вставить элемент в середину слайса с помощью `append`?**
   - Чтобы вставить элемент в середину слайса, можно использовать `append` следующим образом:
     ```go
     s := []int{1, 2, 4, 5}
     index := 2 // Позиция, куда вставляем элемент
     value := 3 // Вставляемое значение
     s = append(s[:index+1], s[index:]...) // Расширяем слайс
     s[index] = value // Вставляем элемент
     ```

[Вопросы](#список-вопросов-к-зачету)


# 25. **Какая структура данных лежит в основе `map`?**
   - В основе `map` лежит хеш-таблица. Это структура данных, которая предоставляет операции вставки, удаления и поиска с высокой производительностью в среднем случае.

[Вопросы](#список-вопросов-к-зачету)


# 26. **Как можно инициализировать `map`?**
   - Карту можно инициализировать с помощью литерала карты или функции `make`:
     ```go
     m1 := make(map[string]int)
     m2 := map[string]int{"foo": 1, "bar": 2}
     ```

[Вопросы](#список-вопросов-к-зачету)


# 27. **Что произойдет, если обратиться по несуществующему ключу в `map`?**
   - Обращение по несуществующему ключу возвращает нулевое значение для типа значений карты.

[Вопросы](#список-вопросов-к-зачету)


# 28. **Как проверить, что ключа нет в `map`?**
   - При обращении к ключу можно получить второе возвращаемое значение, которое является булевым и указывает, существует ли ключ:
     ```go
     value, ok := m[key]
     if !ok {
         // ключа нет
     }
     ```

[Вопросы](#список-вопросов-к-зачету)


# 29. **Можно ли взять адрес от элемента, лежащего в `map`?**
   - Нельзя взять адрес элемента в `map` напрямую, так как доступ к элементам карты может быть реорганизован внутренне, и адрес может быть недействителен.

[Вопросы](#список-вопросов-к-зачету)


# 30. **Какой порядок элементов гарантируется при итерации по `map` через for-range?**
   - Порядок элементов при итерации по `map` не гарантирован и может изменяться при каждом запуске.

[Вопросы](#список-вопросов-к-зачету)


# 31. **На что влияет регистр первой буквы поля или метода в структуре?**
- Точно так же, как и для переменных и функций, если поле или метод структуры начинается с заглавной буквы, оно/он будет доступно/доступен вне пакета (public). Если с маленькой, то только внутри пакета (private).

[Вопросы](#список-вопросов-к-зачету)


# 32. **Что такое встраивание (embedding) в структурах?**
- Встраивание позволяет одной структуре включать другую как подполе, обеспечивая доступ к полям и методам вложенной структуры напрямую у внешней структуры. Это используется для достижения поведения, подобного наследованию:
    ```go
    type Engine struct {
        Power int
    }

    type Car struct {
        Engine // встраивание структуры Engine
    }

    c := Car{}
    c.Power = 150 // доступ к полю Power встроенной структуры Engine
    ```

[Вопросы](#список-вопросов-к-зачету)


# 33. **Что такое именованные возвращаемые значения?**
   - В Go можно определить имена для возвращаемых значений функции прямо в её сигнатуре. Это позволяет возвращать значения, просто указав `return` без необходимости явного указания возвращаемых переменных. Это также позволяет использовать эти переменные в теле функции как предопределенные:
     ```go
     func sum(a, b int) (result int) {
         result = a + b
         return // не нужно указывать result явно
     }
     ```

[Вопросы](#список-вопросов-к-зачету)


# 34. **Что выведет следующий код?**
   ```go
   func main() {
       var x = 0
       func() {
           x = 42
       }()
       fmt.Println(x)
   }
   ```
   - Этот код выведет `42`. Замыкание в анонимной функции захватывает переменную `x` из внешней функции `main` и изменяет её.

[Вопросы](#список-вопросов-к-зачету)


# 35. **Какой тип используется для возврата ошибок?**
   - В Go для возврата и обработки ошибок используется интерфейс `error`. Это стандартный интерфейс, включающий метод `Error() string`.

[Вопросы](#список-вопросов-к-зачету)


# 36. **Для чего используются `errors.Is` и `errors.As`? В чем разница?**
   - `errors.Is` проверяет, является ли ошибка или её обертка экземпляром конкретной ошибки.
   - `errors.As` находит первую ошибку в цепочке, которая удовлетворяет определенному типу, и если находит, присваивает её указателю на этот тип.
   - Разница в том, что `errors.Is` используется для проверки эквивалентности ошибок, а `errors.As` для извлечения конкретной информации об ошибке по типу.

[Вопросы](#список-вопросов-к-зачету)


# 37. **Что такое `defer`? Приведите сценарий использования.**
   - `defer` позволяет отложить вызов функции до того момента, как внешняя функция завершит выполнение. Используется для гарантии выполнения очистки ресурсов, например, закрытия файлов:
     ```go
     func readFile(filename string) (content string, err error) {
         f, err := os.Open(filename)
         if err != nil {
             return
         }
         defer f.Close() // Гарантируем закрытие файла после чтения

         // Чтение файла
     }
     ```

[Вопросы](#список-вопросов-к-зачету)


# 38. **В каком порядке вызываются объявленные в `defer` функции?**
   - Функции, объявленные через `defer`, вызываются в порядке LIFO (last in, first out) — последний объявленный `defer` вызовется первым.

[Вопросы](#список-вопросов-к-зачету)


# 39. **Вызывается ли `defer` при панике?**
   - Да, вызывается. Это одна из особенностей `defer`, позволяющая выполнять очистку или другие важные операции даже при аварийном завершении функции из-за паники.

[Вопросы](#список-вопросов-к-зачету)


# 40. **В какой момент вычисляются аргументы функции, вызываемой в `defer`?**
   - Аргументы функции в `defer` вычисляются в момент объявления `defer`, а не в момент её выполнения.

[Вопросы](#список-вопросов-к-зачету)


# 41. **Что такое `panic`? Что происходит в программе, когда вылетает паника?**
   - `Panic` — это встроенная функция в Go, которая вызывает аварийное завершение программы. При вызове `panic` начинается "размотка стека", при которой вызываются все функции `defer`. Если паника не обработана, программа завершается с ошибкой.

[Вопросы](#список-вопросов-к-зачету)


# 42. **Как остановить выполнение паники?**
- Выполнение паники можно остановить с помощью функции `recover`, вызванной внутри блока `defer`. Если `recover` вызвана и паника произошла, она возвращает значение паники и предотвращает завершение программы:
    ```go
    defer func() {
        if r := recover(); r != nil {
            fmt.Println("Recovered from panic:", r)
        }
    }()
    ```

[Вопросы](#список-вопросов-к-зачету)


# 43. **Разница между паниками и ошибками?**
- Ошибки в Go — это предпочтительный способ обработки ожидаемых проблем в программах, и они не прерывают нормальное выполнение программы. Паники предназначены для неожиданных ошибок, нарушающих нормальный поток выполнения, и часто указывают на ошибки программирования или другие критические проблемы.

[Вопросы](#список-вопросов-к-зачету)


# 44. **В каком месте программы осмысленно использовать функцию `recover`?**
   - Функцию `recover` целесообразно использовать в тех частях программы, где паника может критически повлиять на исполнение или стабильность программы, например, в серверных приложениях, где важно обеспечить продолжительную работу сервера. Чаще всего `recover` используется в функциях, вызываемых через `defer`, чтобы перехватить и обработать панику перед выходом из функции.

[Вопросы](#список-вопросов-к-зачету)


# 45. **Что такое receiver в методе? В чем разница между pointer receiver и value receiver?**
   - Receiver в методе определяет на каком типе (или его указателе) будет вызван метод. Разница между pointer receiver (`func (f *Foo) Bar()`) и value receiver (`func (f Foo) Bar()`) заключается в том, что pointer receiver позволяет методу модифицировать значения в структуре, к которой он применён, в то время как value receiver работает с копией значения.

[Вопросы](#список-вопросов-к-зачету)


# 46. **Что выведется в следующем коде? Почему?**
   ```go
   type Foo struct {
   }

   func (f *Foo) Bar() {
       fmt.Println("Hello!")
   }

   func main() {
       var m = make(map[int]Foo)
       m[1] = Foo{}
       m[1].Bar()  // Этот вызов вызовет ошибку компиляции
   }
   ```
   - Этот код вызовет ошибку компиляции, так как попытка вызова метода `Bar` через указатель на элемент, который является значением в map (`Foo`), не допустима. Элементы map не являются адресуемыми, так что метод, требующий указатель (`*Foo`), не может быть вызван напрямую.

[Вопросы](#список-вопросов-к-зачету)


# 47. **Можно ли вызвать метод на `nil` указателе какого-либо типа? Что произойдет?**
   - Да, можно вызвать метод на `nil` указателе, если метод корректно обрабатывает случай, когда его receiver `nil`. Это поведение может быть полезным для реализации интерфейсов, где объекты могут быть допустимо `nil`.

[Вопросы](#список-вопросов-к-зачету)


# 48. **Что такое интерфейс (interface)? Как он устроен?**
   - Интерфейс в Go — это абстракция, которая определяет поведение объектов: набор методов, который должен иметь тип для удовлетворения интерфейса. Тип, значения которого могут быть `nil`, может реализовывать интерфейс, и такое значение может быть присвоено переменной интерфейса.

[Вопросы](#список-вопросов-к-зачету)


# 49. **Как указать в типе, что данный тип удовлетворяет некоторому интерфейсу?**
   - В Go для указания, что тип удовлетворяет интерфейсу, достаточно просто реализовать все методы интерфейса. Явное указание не требуется.

[Вопросы](#список-вопросов-к-зачету)


# 50. **В чем разница между `nil`-интерфейсами и интерфейсами, содержащими `nil`?**
   - `nil`-интерфейс — это интерфейс без типа и значения. Интерфейс, содержащий `nil`, имеет конкретный тип, но значение `nil`. Различие важно для поведения программы, особенно при сравнении и методах.

[Вопросы](#список-вопросов-к-зачету)


# 51. **Как проверить, какой тип находится за интерфейсом?**
   - Используйте оператор type assertion:
```go
if t, ok := iface.(MyType); ok {
    fmt.Println("Type is MyType:", t)
}
```

[Вопросы](#список-вопросов-к-зачету)


# 52. **Что такое type switch? В каких сценариях может использоваться?**
   - `type switch` позволяет проверить и обработать различные типы, которые может содержать переменная интерфейса. Он используется для упрощения кода, который должен различать множество типов:
     ```go
     switch v := iface.(type) {
     case MyType:
         fmt.Println("MyType:", v)
     case AnotherType:
         fmt.Println("AnotherType:", v)
     default:
         fmt.Println("Unknown type")
     }
     ```

[Вопросы](#список-вопросов-к-зачету)


# 53. **Что такое горутина (goroutine)? Как запустить горутину?**
- Горутина — это легковесный поток выполнения. Запустить горутину можно с помощью ключевого слова `go` перед вызовом функции:
    ```go
    go func() {
        fmt.Println("Inside a goroutine")
    }()
    ```

[Вопросы](#список-вопросов-к-зачету)


# 54. **Как горутины связаны с потоками ОС? Как работает шедулер?**
- Горутины мультиплексируются на меньшее число потоков ОС. Шедулер Go распределяет горутины по доступным потокам ОС, оптимизируя использование ресурсов и обеспечивая высокую производительность при параллельных операциях.

[Вопросы](#список-вопросов-к-зачету)


# 55. **Что произойдет, если функция `main` завершит исполнение раньше, чем закончится выполняться какая-либо другая горутина?**
- Если функция `main` завершится, то программа полностью завершит работу, и все выполняющиеся горутины будут прерваны.

[Вопросы](#список-вопросов-к-зачету)


# 56. **Как дождаться выполнения горутины?**
- Для синхронизации завершения горутин часто используются каналы или `sync.WaitGroup`. Пример с `sync.WaitGroup`:
    ```go
    var wg sync.WaitGroup
    wg.Add(1) // Указываем количество ожидаемых горутин
    go func() {
        defer wg.Done() // По завершении горутины уменьшаем счетчик
        // Выполнение работы
    }()
    wg.Wait() // Ожидание завершения всех горутин
    ```

[Вопросы](#список-вопросов-к-зачету)


# 57. **Как вручную задать количество потоков ОС в программе?**
- Количество потоков ОС можно задать с помощью функции `runtime.GOMAXPROCS`:
    ```go
    import "runtime"
    runtime.GOMAXPROCS(4) // Устанавливаем 4 потока ОС
    ```

[Вопросы](#список-вопросов-к-зачету)


# 58. **Что такое канал (`chan`)? Какие каналы бывают?**
- Канал в Go — это средство передачи данных между горутинами, поддерживающее синхронизацию без использования других примитивов синхронизации. Бывают небуферизированные каналы (блокируются при операции до завершения совпадающей операции другой горутины) и буферизированные (имеют внутренний буфер определенного размера).

[Вопросы](#список-вопросов-к-зачету)


# 59. **Можно ли читать и писать в/из закрытого канала?**
- Писать в закрытый канал вызовет панику. Читать из закрытого канала можно; если в канале есть данные, они будут прочитаны, после чего чтения вернут нулевое значение типа данных канала.

[Вопросы](#список-вопросов-к-зачету)


# 60. **Как создать канал с размером буфера 10?**
- Канал с буфером создается так:
    ```go
    ch := make(chan int, 10) // Канал для int с буфером размером в 10 элементов
    ```

[Вопросы](#список-вопросов-к-зачету)


# 61. **Почему операции записи/чтения в/из канала могут блокироваться? В каких ситуациях блокировки не будет?**
- Операции блокируются, когда буфер полный (для записи) или пустой (для чтения) в буферизированных каналах. В небуферизированных каналах блокировка происходит до тех пор, пока другая горутина не выполнит соответствующую операцию (чтение при записи и наоборот). Блокировки не будет, если есть свободное место в буфере или другая горутина уже ожидает операцию.

[Вопросы](#список-вопросов-к-зачету)


# 62. **Как сделать неблокирующее чтение из канала в любом исходе (т.е. даже если в канале ничего нет)?**
- Неблокирующее чтение из канала можно осуществить с помощью оператора `select` с `default` веткой:
    ```go
    select {
    case msg := <-ch:
        fmt.Println("Received", msg)
    default:
        fmt.Println("No data")
    }
    ```

[Вопросы](#список-вопросов-к-зачету)



# 63. **Что такое состояние гонки (race condition)? Приведите пример.**
- Состояние гонки происходит, когда две или более горутин конкурентно изменяют общие данные без должной синхронизации, что приводит к недетерминированным результатам. Пример:
    ```go
    var count int
    go func() {
        count++ // Инкремент без защиты мьютексом
    }()
    go func() {
        count++ // Инкремент без защиты мьютексом
    }()
    ```
      
[Вопросы](#список-вопросов-к-зачету)



# 64. **Для чего используется мьютекс (`sync.Mutex`)? Каков сценарий использования?**
- Мьютекс используется для блокировки доступа к данным, что предотвращает состояние гонки. Пример использования:
    ```go
    var mu sync.Mutex
    var count int
    go func() {
        mu.Lock()  // Блокируем доступ
        count++
        mu.Unlock()  // Открываем доступ
    }()
    ```

[Вопросы](#список-вопросов-к-зачету)


# 65. **В чем разница между `sync.Mutex` и `sync.RWMutex`?**
- `sync.Mutex` предоставляет эксклюзивную блокировку, `sync.RWMutex` предоставляет блокировку для чтения и записи, позволяя множественным горутинам одновременно читать данные, но требует эксклюзивного доступа для записи.

[Вопросы](#список-вопросов-к-зачету)


# 66. **Для чего используется `sync.Once`? Приведите сценарий использования.**
- `sync.Once` используется для выполнения действия один раз независимо от количества вызовов. Это полезно для инициализации, выполняемой однократно:
    ```go
    var once sync.Once
    once.Do(func() {
        fmt.Println("This will run only once")
    })
    ```

[Вопросы](#список-вопросов-к-зачету)


# 67. **Как можно проверить (например, тестами), что в программе нет состояния гонки?**
- В Go для проверки наличия гонок можно использовать инструмент `go test -race`.

[Вопросы](#список-вопросов-к-зачету)


# 68. **В чем разница между blackbox- и whitebox-тестами? Как в Go можно явно сделать blackbox-тесты?**
- Blackbox-тестирование проверяет функциональность без знания внутренней структуры кода, whitebox-тестирование использует знания о внутреннем устройстве программы. В Go для blackbox-тестирования можно разместить тесты в отдельном пакете, добавив `_test` к названию пакета.

[Вопросы](#список-вопросов-к-зачету)


# 69. **Что такое `generics`? Приведите пример, когда дженерики упрощают написание кода.**
- `Generics` (обобщённое программирование) позволяет функциям и типам работать с различными типами данных. Пример упрощения:
    ```go
    func Sum[T numeric](a, b T) T {
        return a + b
    }
    ```
    Это позволяет использовать функцию `Sum` с любым числовым типом без дублирования кода для каждого типа.

[Вопросы](#список-вопросов-к-зачету)
