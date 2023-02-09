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

# Homework starts right here

## Working with remote repository walkthrough

To start your work with remote repository you must create new account on [github.com](https://github.com/).

Then use sent link to open remote repository. 

For ex:
[Homework](https://github.com/cheklinim/seminar3_HW).

## Forking like a lifestyle

Someone sometime decided that it was very funny to call copying a **fork**. 

So if you need to copy remote repository to your private account on Github you need to click on **Fork** button.

The fork creation window will open after clicking.

## Fork creation window

In opened window you can select next options:

1. Select owner
2. Change repository name
3. Add some description
4. Copying only main branch flag

After choosing you must press **Create fork**.

Then window with forked repository will open.

## Copying forked repository to your local PC with **CLONE**

The next step to be a professional programmer will be downloading forked repository to your local PC.

So in opened window press **<> CODE** button and copy selected link.

Then open Visual studio code, open terminal and use:

    git clone (https:\\link_here)

After the process will be ended open folder of downloaded repository with VSC. (default in windows: C:\Users\User\Repository_name).

Now you can create new branch and start doing your changes.

## **Push**ing your changes back to github

After some new commits added to processed file you need to apply them back to remote repository on your github account. Just use:

    git push

Now you can check your remote repository on github to make sure it worked.

## **Pull**ing last changes from remote repository

If you adding changes to one remote repository from diffrent PCs or you working with it by a team of developers you will need to often upgrate your local file.

To do it easely just use from oppened repository:

    git pull

And all new remote changes will update your local file.

## Push-request to source repository

You made a lot of good changes, awesome commits and other stuff. Now you need to sent it back to creator and suggest them to him.

So you getting back to you remote repository on your github account. You can see there green button with text: *Compare & pull request*. Press it.

Now you can see *Comparing changes* window.

Here you should add title and description to your changes. Be careful, you need to explain all your changes clearly.

After you did that press green button with text *Create pull request*.

*My pull request* window will open and you can see it status and some comments.