# Дополнительные команды git reset, git diff, git reset --hard

1. git reset [file_name]
Позволяет удалить выбранные файлы из промежуточной области (stage)
-- Тут я внёс изменения в index.html, теперь по команде git status он красный (change not staged for commit)
-- Дальше добавляю его в stage с помощью git add
-- Но мне не нужно добавлять его в stage, убираю с помощь git reset index.html
-- Теперь он снова красный (не подготовлен для коммита)


2. git diff
Команда позволяет просмотреть все строки, кот. были изменены или добавлены
Знак + рядом со строкой значит, что строку добавили.
Знак - показывает, что строка была удалена.

Если указать имя файла в команде, то git diff применится к определённому файлу
git diff [file_name]



3. git reset --hard
Команда уберёт все изменения, которые сделаны, и вернёт всё к предыдущему состоянию (к предыдущему коммиту)
Используется, когда были сделаны изменения, но стало понятно, что надо всё вернуть в предыдущее состояние.




4. git restore [file_name]
или git restore .

Это вернёт файлы к состоянию последнего коммита, т.е. удалит изменения, и git diff ничего не покажет.