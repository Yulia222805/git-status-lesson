Хеш - идентификатор коммита в Git.
Хеширование - преобразование набора данных для получения их "отпечатка".
Хеш коммита получается с помощью алгоритма SHA-1.
Хеш состоит из цифр 0-9 и латинских букв A-F.
Свойства хеша: если дважды получить хеш для одного набора данных, результат будет одинаковым.
Если изменить хоть что-то в исходных данных, хеш изменится.
Хеш - основной идентификатор коммита, позволяет узнать автора, дату и содержимое закоммиченных файлов.
Хеши и таблицу хеш → информация о коммите Git сохраняет в служебных файлах в папке .git.

Лог содержит описание коммита: хеш, автор, дата, сообщение.
Сокращенный лог помогает быстро найти нужный коммит среди множества.
Команда git log --oneline выводит сокращенный лог с хешами и комментариями.
Уникальная длина сокращенных хешей помогает идентифицировать коммит.

Файл HEAD (голова, головной) указывает на последний коммит в системе git.
Файл HEAD находится в папке .git.
Для проверки содержимого файла HEAD можно использовать команду cat.
Внутри файла HEAD находится ссылка на служебный файл refs/heads/master, содержащий хеш последнего коммита.
При работе с Git указатель HEAD используется часто, его можно заменить на слово HEAD для передачи последнего коммита.

```mermaid 
 Типичный жизненный цикл файла в Git TD;
 A[untracked(неотслеживаемый)]-git add-> B[staged(в списке на коммит) + tracked];
 C[modified(измененный)]-git add-> B;
 B-git commit-> D[tracked(отслеживаемый)];
 D-Изменения->C
 B-Изменения->С; 
```
