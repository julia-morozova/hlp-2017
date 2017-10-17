# Программирование на высокоуровневых платформах - 2017
## Задачи
####1. Реализовать программу, которая вычисляет произвольное математическое выражение (передаётся параметром командной
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

####2. Реализовать программу
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

## Литература
1. Joshua Bloch - Effective Java
2. Bruce Eckel - Thinking in Java
3. Brian Goetz - Java Concurrency in Practice
4. Jeanne Boyarsky - OCA: Oracle Certified Associate Java SE 8 Programmer I Study Guide
5. James Gosling - Language Specification (Java SE 9 Edition) - https://docs.oracle.com/javase/specs/jls/se9/jls9.pdf

на русском:
1. Брюс Эккель - Философия Java
2. Дж. Блох - Java. Эффективное программирование