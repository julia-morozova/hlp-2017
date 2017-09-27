# Программирование на высокоуровневых платформах - 2017
## Задачи
1. Реализовать программу, которая вычисляет произвольное математическое выражение (передаётся параметром командной строки), и пакет скриптов к ней:
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

## Лекции:
### 2017-09-12
* JDK = JRE + Development/debugging tools
  JRE = JVM + Java Packages Classes(like util, math, lang, awt,swing etc)+runtime libraries.
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