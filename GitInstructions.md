# How to work with git

main commands

# Instructions for github communication

git clone - скопировать удаленный репозиторий на локальный компьютер
git remote add origin URL - указать в соответствие локальному репо удаленный репо
git push -u origin main - отправка локального репо на адрес origin в ветвь main
git pull - стянуть удаленный репо

# Это репозиторий для обучения pull request

# Основные команды Git
>Я бы хотел умереть на Марсе — но только не от удара о поверхность.

*Илон Маск*
* **git init** - инициализация локального репозитория
* **git status** - получить информацию от git о его текущем состоянии
* **git add** - получить файл к следующему коммиту
* **git commit -m "message"** - отправить коммит с комментарием "message"
* **git log** - вывод на экран всех коммитов с их хэш кодами
* **git checkout** - переход от одного коммита к другому
* **git checkout master** - вернуться к актуальному состоянию и продолжить работу
* **git diff** - увидеть разницу между текущим файлом и закоммиченным файлом


* **git init** - инициализация локального репозитория
* **git status** - получить информацию от git о его текущем состоянии
* **git add** - получить файл к следующему коммиту
* **git commit -m "message"** - отправить коммит с комментарием "message"
* **git log** - вывод на экран всех коммитов с их хэш кодами
* **git checkout** - переход от одного коммита к другому
* **git checkout master** - вернуться в главную ветвь
* **git diff** - увидеть разницу между текущим файлом и закоммиченным файлом
* **git branch** - посмотреть список веток в репозитории
* **git branch branch_name** - создать ветвь с именем branch_name
* **git checkout branch_name** - перейти в ветвь с именем branch_name
* **git checkout -b branch_name** - создать ветвь с именем branch_name и перейти в нее
* **git merge branch_name** - влить в **текущую** ветвь ветку с именем branch_name
* **git branch -d branch_name** - удалить ветвь с именем branch_name

![avatar](https://epicris.ru/wp-content/uploads/2020/11/promokod-geekbrains.jpg)


## Первые шаги

1. Делаем fork репозитория, в которой потом хотим сделать pull request. Ищем кнопку Fork на странице репозитория <https://git@github.com:gulden-geekbrains/version_control.git>
2. Выполняем команду клонирования из своей fork-копии
```sh
git clone git@github.com:*YOURE_GITHUB*/version_control.git
```
3. Создаем новую ветку и вносим необходимые изменения в файл
```sh
git checkout -b updatereadme
vim README.md
git add README.md
git commit -m "Добавили инструкцию как создать pull request"
```
4. Делаем push  
```sh
git push --set-upstream origin updatereadme
```
5. Переходим на свою страницу репозитория. Выбираем ветку **updatereadme** и жмем кнопку **Compare & pull request**

## Заметки

Что бы сделать push от другого пользователя необходимо выполнить команду
```sh
GIT_SSH_COMMAND='ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes' git push git@github.com:gulden-geekbrains/version_control.git
```

вместо *user-private-key* подставьте свой ключ

Можно прописать настройки для подсоединения по ssh
```sh
git config remote.origin.url git@github.com:gitusername/reponame
git config core.sshCommand "ssh -i ~/.ssh/user-private-key -o IdentitiesOnly=yes"
```
# Как подружить git с github под Windows 10

Вот видео инструкция https://youtu.be/E8cIjbJMEpE


