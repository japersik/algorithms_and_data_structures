#  Задача 7 (1322. Шпион)

## Условие

Спецслужбы обнаружили действующего иностранного агента. Шпиона то есть. Установили наблюдение и выяснили, что каждую неделю он через Интернет посылает кому-то странные нечитаемые тексты. Чтобы выяснить, к какой информации получил доступ шпион, требуется расшифровать информацию. Сотрудники спецслужб проникли в квартиру разведчика, изучили шифрующее устройство и выяснили принцип его работы.S<sub>1</sub> = s<sub>1</sub>s<sub>2</sub>...s<sub>N</sub>. Получив ее, устройство строит все циклические перестановки этой строки, то есть S<sub>2</sub> = s<sub>2</sub>s<sub>3</sub>...s<sub>N</sub>s<sub>1</sub>, ..., S<sub>N</sub> = s<sub>N</sub>s<sub>1</sub>s<sub>2</sub>...s<sub>N-1</sub>. Затем множество строк S<sub>1</sub>, S<sub>2</sub>, ..., S<sub>N</sub> сортируется лексикографически по возрастанию. И в этом порядке строчки выписываются в столбец, одна под другой. Получается таблица размером N × N. В какой-то строке K этой таблицы находится исходное слово. Номер этой строки вместе с последним столбцом устройство и выдает на выход.
Например, если исходное слово S<sub>1</sub> = abracadabra, то таблица имеет такой вид:<br>
    aabracadabr = S<sub>11</sub><br>
    abraabracad = S<sub>8</sub><br>
    abracadabra = S<sub>1</sub><br>
    acadabraabr = S<sub>4</sub><br>
    adabraabrac = S<sub>6</sub><br>
    braabracada = S<sub>9</sub><br>
    bracadabraa = S<sub>2</sub><br>
    cadabraabra = S<sub>5</sub><br>
    dabraabraca = S<sub>7</sub><br>
    raabracadab = S<sub>10</sub><br>
    racadabraab = S<sub>3</sub><br>
И результатом работы устройства является число 3 и строка rdarcaaaabb.
Это все, что известно про шифрующее устройство. А вот дешифрующего устройства не нашли. Но поскольку заведомо известно, что декодировать информацию можно (а иначе зачем же ее передавать?), Вам предложили помочь в борьбе с хищениями секретов и придумать алгоритм для дешифровки сообщений. А заодно и реализовать дешифратор.

## Исходные данные

В первой и второй строках находятся соответственно целое число и строка, возвращаемые шифратором. Длина строки и число не превосходят 100000. Строка содержит лишь следующие символы: a-z, A-Z, символ подчеркивания. Других символов в строке нет. Лексикографический порядок на множестве слов задается таким порядком символов:
`ABCDEFGHIJKLMNOPQRSTUVWXYZ_abcdefghijklmnopqrstuvwxyz`
Символы здесь выписаны в порядке возрастания.

## Результат
Выведите декодированное сообщение в единственной строке.

## Примеры
| Исходные данные | Результат  |
|---|---|
|3 <br> rdarcaaaabb| abracadabra |