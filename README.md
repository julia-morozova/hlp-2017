# Программирование на высокоуровневых платформах - 2017
## Задачи
#### 1. Базовые операции. Классы, методы, тесты.
Реализовать программу, которая вычисляет произвольное математическое выражение (передаётся параметром командной
строки), и пакет скриптов к ней:
* компиляция и запуск приложения средствами JDK
* сборка утилитой maven/gradle в jar и запуск приложения

* Выражение может содержать математические операции: */-+! и ().
* Необходимо провести валидацию входных параметров (проверка на то, что выражение вычисляемо).
* Покрытие кода тестами - 90%. Рекомендация: использовать метологию TDD (Test Driven Development).
* Провести статический анализ кода с использованием PMD и Findbugs
* Использовать логирование при необходимости.
* Можно использовать подключаемые библиотеки: google guava, apache commons, junit, testng, mockito и т.д.

Вывод: результат вычислений или сообщение о невозможности вычисления выражения.

RTFM and use:
* https://git-scm.com/
* https://habrahabr.ru/post/106912/
* https://www.atlassian.com/git/tutorials/merging-vs-rebasing - optional
* http://agiledata.org/essays/tdd.html
* https://pmd.github.io/
* http://findbugs.sourceforge.net/
* https://gradle.org/
* https://maven.apache.org/
* https://search.maven.org/
* https://github.com/google/guava
* https://commons.apache.org/
* http://junit.org/junit5/
* http://testng.org/doc/
* http://site.mockito.org/

#### 2. IO/NIO, работа со строками
ВХОД:
путь к файлу или каталогу (может содержать подпапки) с исходными данными (строка) - (1).    
путь к каталогу с результатами выполнения программы (строка) - (2)

ВЫХОД:
При успешном завершении должен быть создан каталог с указанным именем, включающий в себя подпапки: txt и binary, а 
также файл skipped.txt. Каталог binary содержит в себе единственный файл - ZIP-архив. В каталог txt содержатся
исключительно обработанные текстовые файлы. Файл skipped.txt содержит имена пропущенных файлов (абсолютный или 
относительный путь) в естественном порядке.       
В случае ошибки вывести на экран сообщение об ошибке.

ПОСТАНОВКА ЗАДАЧИ:
Для всех файлов, включая файлы содержащиеся в подпапках произвести следующие операции:

Для ZIP-архивов:       
* Содержимое ZIP-архива обрабатывается по тем же правилам, что текстовые и бинарные данные.

Для текстовых файлов (с расширением .txt):
* Отсортировать содержимое файла по количеству слов в строке и длине строки
* Полученный результат должен быть помещён в каталог txt с тем же именем, что исходный файл. Исходный файл не должен
быть изменён.
* Пустые файлы должны быть пропущены, а путь к ним добавлен в файл skipped.txt в алфавитном порядке.
* Файлы могут быть большого объёма (больше размера свободной памяти).

Все остальные файлы:
* Помещаются в единый ZIP-архив в соответствующие подкаталоги.
* Пустые файлы пропускаются, а их имена заносятся в файл skipped.txt.

Осуществить логирование.
Контроль качества кода:
* Провести тестирование - модульные тесты (80%)
* Провести статический анализ кода (PMD/Findbugs)

RTFM and use:
* https://docs.oracle.com/javase/8/docs/api/java/util/zip/ZipEntry.html
* https://docs.oracle.com/javase/8/docs/api/index.html?java/util/zip/ZipOutputStream.html
* https://docs.oracle.com/javase/8/docs/api/java/util/zip/ZipInputStream.html
* https://docs.oracle.com/javase/8/docs/api/java/util/logging/Logger.html
* https://habrahabr.ru/post/130195/
* https://docs.oracle.com/javase/tutorial/essential/io/index.html

#### 3. Коллекции

#### 4. Многопоточность и работа с БД?


## Лекции:
### 2017-09-12
* JDK = JRE + Development/debugging tools
  JRE = JVM + Java Packages Classes(like util, math, lang, awt,swing etc) + runtime libraries.   
  JVM = Class loader system + runtime data area + Execution Engine.
* https://habrahabr.ru/post/269621/ - GC
* https://docs.oracle.com/javase/8/docs/api/java/lang/Object.html
* Jeanne Boyarsky - OCA: Oracle Certified Associate Java SE 8 Programmer I Study Guide (chapters 1, 2) или Bruce Eckel - Thinking in Java (страницы 5 - 51)
* Joshua Bloch - Effective Java (страницы 5 - 54)

!!! Контракт equals и hashCode!!!

### 2017-09-26
Comparable vs Comparator
* https://docs.oracle.com/javase/9/docs/api/java/util/Comparator.html
* https://docs.oracle.com/javase/9/docs/api/java/lang/Comparable.html

Arrays
* https://docs.oracle.com/javase/9/docs/api/java/util/Arrays.html

Модификаторы доступа
* Bruce Eckel - Thinking in Java (страницы 107 - 217)
* Jeanne Boyarsky - OCA: Oracle Certified Associate Java SE 8 Programmer I Study Guide (страницы 165 - 202, 233-291)

Вложенные классы
* Bruce Eckel - Thinking in Java (страницы 243 - 273)
* https://docs.oracle.com/javase/tutorial/java/javaOO/nested.html

Перечисляемые типы
* https://docs.oracle.com/javase/tutorial/java/javaOO/enum.html
* Joshua Bloch - Effective Java (главы 30, 31 ,34)
* Bruce Eckel - Thinking in Java (страницы 725 - 734)

### 2017-10-10
IO/NIO/NIO2
* Bruce Eckel - Thinking in Java (страницы 647 - 725, раздел IO) - английский, но есть перевод
* Joshua Bloch - Effective Java (раздел Serialization) - английский, но есть перевод
* http://tutorials.jenkov.com/java-nio/index.html - английский, схемы, примеры
* https://docs.oracle.com/javase/tutorial/essential/io/fileio.html (до Legacy File I/O Code, не включительно) - английский, примеры
* http://www.quizful.net/post/java-nio-tutorial - русский, примеры

### 2017-10-24
Collection API, Generics
* Bruce Eckel - Thinking in Java (всё из Holding Your Objects и Generics) - английский
* Bruce Eckel - Философия Java (разделы Коллекции и Параметризация) - то же самое, но на русском
* Joshua Bloch - Effective Java (Generics) - английский
* https://habrahabr.ru/post/128017/
* https://habrahabr.ru/post/128269/
* https://habrahabr.ru/post/127864/ - можно, в принципе, пробежать по диагонали
* https://habrahabr.ru/post/162017/

Итераторы
* https://docs.oracle.com/javase/9/docs/api/java/util/Iterator.html
* https://docs.oracle.com/javase/9/docs/api/java/util/ListIterator.html
* http://www.seostella.com/ru/article/2012/10/07/bezopasnyy-sposob-udaleniya-elementov-iz-kollekcii-v-java.html

!!! Самое важное и полезное !!!

### 2017-11-07
JMM (Java Memory Model)
* https://docs.oracle.com/javase/specs/jls/se9/jls9.pdf (Threads and Locks)
* http://www.javaspecialist.ru/2011/06/java-memory-model.html - то же, что и выше, но вкратце и ущербно
* https://shipilev.net/#jmm - видео

### 2017-11-21
Concurrency
* https://habrahabr.ru/post/164487/
* https://docs.oracle.com/javase/tutorial/essential/concurrency/index.html
* https://habrahabr.ru/post/187854/
* https://habrahabr.ru/company/luxoft/blog/157273/
* https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/locks/ReentrantReadWriteLock.html - он такой классный)))

В базах данных
* https://habrahabr.ru/post/86302/
* https://habrahabr.ru/post/121858/ - там отличная ссылка на Fowler's Patterns of Enterprise Application Architecture

Ликбез
* https://ru.wikipedia.org/wiki/Взаимная_блокировка
* https://urvanov.ru/2016/05/27/java-8-многопоточность/ - deadlock, livelock, starvation

!!! Жизненный цикл потока, synchronized, final, ReentrantReadWriteLock, volatile, Thread, Runnable!!!

### 2017-12-05
Шаблоны
* Одиночка
* Фабрика
* Декоратор
* Фасад
* Блокировка с двойной проверкой

JDBC
* https://docs.oracle.com/javase/tutorial/jdbc/basics/index.html

### 2017-12-19
Stream API
* https://www.youtube.com/watch?v=0BsXi3qvv68
* https://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html
* https://javadevblog.com/polnoe-rukovodstvo-po-java-8-stream.html

Reflection
* https://docs.oracle.com/javase/tutorial/reflect/
* http://javadevblog.com/polnoe-rukovodstvo-po-java-reflection-api-refleksiya-na-primerah.html
* https://habrahabr.ru/post/318418/


## Литература
1. Joshua Bloch - Effective Java
2. Bruce Eckel - Thinking in Java
3. Brian Goetz - Java Concurrency in Practice
4. Jeanne Boyarsky - OCA: Oracle Certified Associate Java SE 8 Programmer I Study Guide
5. James Gosling - Language Specification (Java SE 9 Edition) - https://docs.oracle.com/javase/specs/jls/se9/jls9.pdf

на русском:
1. Брюс Эккель - Философия Java
2. Дж. Блох - Java. Эффективное программирование