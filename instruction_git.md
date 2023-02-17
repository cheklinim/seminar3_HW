# **Инструкция по работе с системой контроля версий Git**

![Эмблема Git](git.jpg)

Git (произносится «гит») — распределённая система управления версиями. Проект был создан Линусом Торвальдсом для управления разработкой ядра Linux, первая версия выпущена 7 апреля 2005 года. На сегодняшний день его поддерживает Джунио Хамано.

## Инициализация репозитория

Чтобы создать (инициализировать) новый репозиторий нужно в терминале ввести команду:

    git init

Репозиторий будет создан в той папке, из которой вызывалась команда

## Проверка состояния репозитория

Чтобы проверить текущее состояние репозитория нужно ввести в терминале команду:

    git status

## Добавление изменения к отслеживанию версионности

Чтобы добавить сделанное изменение к отслеживанию (поместить в индекс) нужно ввести команду:

    git add <имя файла>

где вместо <имя файла> вводится путь к файлу относительно расположения репозитория.

## Фиксация изменений

Чтобы зафиксировать изменение используется команда:

    git commit

В таком случае откроется окно для ввоба краткого описания сделанных изменений.

Чтобы сделать это одновременно с фиксацией используется команда:

    git commit -m "комментарий"

## Просмотр истории изменений

Чтобы посмотреть историю изменений используется комада

    git log

Для просмотра изменений с выводом одного коммита в одну строку используется команда

    git log --oneline

Для просмотра всех имеющихся коммитов используется команда

    git log --all

Для просмотра лога с графическим изображением веток используется команда

    git log --graph

Все указанные флаги могут использоваться вместе:

    git log --all --oneline --graph

## Просмотр различий между изменениями

Для просмотра отличий между текущим состоянием репозитория и последним сохраненным изменением используется команда

    git diff

Можно также посмотреть разницу между любыми двуми коммитами. Для этого используется команда

    git diff <хэш1> <хэш2>

## Переключение на нужное изменение

Чтобы переключиться на нужный коммит используется команда

    git checkout <хэш>

## Ветки в Git

### Создание новой ветки

Чтобы создать новую ветку используется команда

    git branch <имя_ветки>

### Просмотр всех веток

Чтобы посмотреть какие ветки существуют и на какой мы находимся используется команда

    git branch

### Переключение между ветками

Чтобы переключиться на другую ветку используется команда

    git checkout <имя_ветки>

### Слияние веток

Чтобы влить одну ветку в другую необходимо находясь в целевой ветке (КУДА будем делать слияние) выполнить команду

    git merge <имя_вливаемой_ветки>

### Конфликты при слиянии

Если одна и та же строка в разный версиях записана по разному возникнет конфликт.
Чистый гит автоматически сохраняет оба изменения, далее требуется вручную внести нужные правки и сделать коммит.

VSСode дает возможность выбрать какое изменение сохранить (входящее, существующее или оба).

### Удаление ветки

Чтобы удалить ветку, которая больше не нужно (например после слияния) используется команда

    git branch -d <имя_ветки>

## Remote repositories

Remote repositories are versions of your project saved on the Internet. You can have several remote repositories.

Repository management includes both the ability to add new repositories and the ability to delete outdated repositories, as well as the ability to manage various remote branches, declare them tracked or not, and so on.

### Create a repositories

To put your project up on GitHub, you will need to create a repository for it to live in.

1. In the upper-right corner of any page, use the "__+__" drop-down menu, and select __New repository__
2. Type a short, memorable name for your repository. Optionally, add a description of your repository.
3. Choose a repository visibility.
4. Click Create repository.

Next you can push an existing repository from the command line.

In a local repository, in the terminal enter the following commands:

    git remote add origin <url remote repositories>
    git branch -M <name local branch>
    git push -u origin <name local branch>

### Git Clone

The command is used to create a copy of a specific repository or branch within a repository.

When you clone a repository, you don't get one file, like you may in other centralized version control systems. By cloning with Git, you get the entire repository - all files, all branches, and all commits

Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits:

    git clone [url]

### Git Pull

git pull updates your current local working branch, and all of the remote tracking branches. It's a good idea to run git pull regularly on the branches you are working on locally.

Without git pull, (or the effect of it,) your local branch wouldn't have any of the updates that are present on the remote.

Update your local working branch with commits from the remote, and update all remote tracking branches:

    git pull

### Git push

Uploads all local branch commits to the corresponding remote branc:

    git push

### Fork a repositories

A fork is a new repository that shares code and visibility settings with the original “upstream” repository. Forks are often used to iterate on ideas or changes before they are proposed back to the upstream repository, such as in open source projects or when a user does not have write access to the upstream repository. 

1. On GitHub.com, navigate to the repository.
2. In the top-right corner of the page, click __Fork__.
3. Select an owner for the forked repository.
4. By default, forks are named the same as their upstream repositories. You can change the name of the fork to distinguish it further.
5. Optionally, add a description of your fork.
6. Choose whether to copy only the default branch or all branches to the new fork. For many forking scenarios, such as contributing to open-source projects, you only need to copy the default branch. By default, only the default branch is copied.
7. Click Create fork.

