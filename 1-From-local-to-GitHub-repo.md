# ## 1. Отправка изменений из локальной папки на GitHub-репозиторий

// Как записать изменения
// Как отправить изменения с компа в удалённый репо
// Что такое файл gitignore и как пользоваться

Создам ещё один git-репо для текущего урока
result_school_test-git-3-main

Инициализирую git проект в папке, привяжу папку к удалённому репо, проверю привязку папки к репо, поменяю юзернейм и емейл
# git init
# git remote add origin https://github.com/PashaMozhet1/result_school_test-git-3-main.git
# git remote -v
# git config user.name "Pavel Sitnikov"
# git config user.email "sit.pro@yandex.ru"



Теперь файлы в эксплорере VSCode светятся зелёным и есть значок магнита (типа буквы U)
Это значит, что сейчас эти файлы видны Гиту, но они пока помечены как Untracked files

ЧТобы проверить все изменения и текущеее состояние, есть команда:
# git status

Такие untracked files означаю, что они были созданы или изменены. Они подсвечены красным в терминале.
Дальше нужно файлы добавить в stage - особая промежуточная зона перед передачей изменённых файлов в репо.



Чтобы подготовить файлы к записи в Git, используется 
# git add [files]
где files - файлы, которые хочу добавить для записи в Гит
git add index.html index.js README.md
- Названия файлов пишутся просто через пробел

Но если таких файлов 100+? Вручную не пропишешь все.

Чтобы добавить все файлы из папки, используется точка .
# git add .

Эта команда подготавливает файлы для записи, добавляя их в подгтовительную область STAGE

Теперь у файлов символ A рядом с названием в эксплорере, тоже подсвечены зелёным
При вызове git status все файлы отображаются зелёным цветом.
А в интерфейсе VSCode строки с изменениями теперь выделяются.



Чтобы записать файлы из stage в git, используется 
# git commit
Обычно Гит Коммит пишут с комментарием, в кот. указывают кратко, что именно поменялось/какая работа проделана. Например:
git commit -m "init project"

Где -m это флаг для комментария, сам коммент пишется в кавычках

Теперь запись хранится локально на компе. В репо на GitHub ещё не отправлена.



Чтобы проверить записи в Git, используется 
# git log
Эта запись покажет полный лог/список изменений в Гит с комментами по коммитам, автором, емейлом, датой изменения, в какую ветку была запись, id.

commit c7db2e06c95eece00e520341d093b05a683a9b6a (HEAD -> master)
Author: Pavel Sitnikov <sit.pro@yandex.ru>
Date:   Wed Jun 11 20:20:56 2025 +0300

    init project

Короткая команда для просмотра коммитов:
# git log --oneline
c7db2e0 (HEAD -> master) init project




Чтобы отправить файлы в удалённый репозиторий на GitHub, используется
# git push [repo_link] [branch_name]

# !!!
В уроке не было этого, но сейчас на июль 2025 года запушить коммит удалось с флагом -u
# git push -u [repo_link] [branch_name]



Ссылку на репо можно проверить командой 
# git remote -v
Репозиторий этого урока у меня:
origin https://github.com/PashaMozhet1/result_school_test-git-3-main.git

В git push можно использовать либо ссылку на репозиторий, либо название (в моём случае origin).
В этом проекте пишу:
# git push origin master
(пока что про название ветки не смотрю, про них в следующих уроках)(сейчас отправляю в главную ветку с названием master)

После этого файлы загрузились на удалённый репо, теперь они доступны в моём профиле на сайте GitHub.
В терминале информация о загрузке:

info: please complete authentication in your browser...
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 16 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (11/11), 3.32 KiB | 3.32 MiB/s, done.
Total 11 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/PashaMozhet1/result_school_test-git-3-main.git
 * [new branch]      master -> master