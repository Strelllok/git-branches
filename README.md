git clone - клонировать репо(в конце адреса url можно вводить/создавать название директории)

git push - внести изменения в репозиторий

git fetch - подтянуть изменения

git merge branchName - внести актуальные изменения в текущую ветку(объеденения 2-х веток)

git pull = git fetch + git merge

git log --online --graph --decorate --all - вывести/посмотреть дерево коммитов

git branch - посмотреть текущую ветку

git branch branchName - создание ветки

git checkout branchName - перключиться на ветку

git checkout -b branchName - создать и переключиться на созданную ветку

git branch -m newBranchName - переиминовать текущую ветку

git checkout numberCommit-переключение на коммит в истории

git branch -v - текущее состояние дерева

git branch --merged - посмотреть все смердженные ветки

git branch --no-merged - посмотреть все не смердженные ветки

git branch -d branchName - удалить ветку
git branch -D branchName - удалить ветку (в том случае если гит ругается что невозможно удалить не смердженную ветку)

================ Отмена изменения , удаление коммита ==================

git diff - посмотреть внесенные изменения

git checkout -- fileName / . - отменить изменения в файле / отменить все изменения

git reset fileName / . - отменить изменения внесенные в стейдж(stage)/ отменить все изменения в стейдж(stage)

git reset --soft HEAD^1 - отмена последнего коммита(^1-указываем количество коммитов)

git reset --hard HEAD^1 - удалить последний коммит (^1-указываем количество коммитов)

========Git commit: Помещение нескольких файлов в репозиторий отдельными коммитами====

git add . - добавить все файлы

git add fileName / pathName - добавить конкретный коммит

==========Git cherry pick: переносим коммиты в другую ветку==============

git cherry-pick hashNumberCommit - поместить коммит в необходимую ветку,через пробел можно указать все hashи необходимы в ветке

Если закомитили в мастер , а необходимо в другое место

git checkout -b newBranch
git checkout master
git reset --hard HEAD^1

============Git config: настройка (редактор, пользователь, команды)==========

cat ~/.gitconfig
git config --global user.name 'Name'-созадать имя
git config --global user.email 'Email'- создать почту
git config --list --global- проверить
git config --list --local - посмотреть локальную конфигурацию
git config --global color.ui true - включить подсветку

Создание alias =====
git config alias.commandName 'your command'
Пример(Дерево )
git config alias.last 'log --oneline --graph --decorate --' -created alias
git last - call alias
git -A -посмотреть список запущенных процессов

===============Git stash: прячем изменения в коде в буфер (на полку, в "заначку")=====

Необходимо когда нужно срочно переключиться или заняться чем то другим,но текущая работа в текущей ветке не закончена

git stash - спрятать файл

git stash list - посмотреть спрятаные файлы

git stash apply - восстановить последний незавершеный файл

git stash pop stash@{numInStash} - восстановить последние изменения (необходимый файл)

git stash drop stash@{numInStash} - удалить выбранный stash

git stash clear - очистить stash полностью

=========Git rebase: перемещение ветки (перебазирование), изменение истории git====

Rebase в гите ,это функция которая позволяет перенести ветку в начало другой ветки

git rebase branchName - перенести из текущей ветки в начало указанной

git rebase --onto branchName commitWhat commitNeeded -

======Git merge: слияние веток (объединение), "закрытие" веток (удаление влитых)===

========Git unmerge (+ git revert) - отмена слияния, откат изменений========

git revert hashCommit - отменить влитый коммит

git revert ^startedHashCommit..endedHashCommit

=========Command git =======

git mv oldNameFile newNameFile - переиминовать

git rm fileName - удалить выбраный файл

git mv fileName whear/fileName - перенести в указанную директорию
все это надо знать
