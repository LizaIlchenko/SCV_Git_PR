# Репозиторий для **pull request**
* В своём аккаунте на GitHub создать копию репозитория **"AndreyBulgakov19/SCV_Git_PR"** с помощью кнопки **"Fork"**.
---
* Клонировать копию репозитория на локальный компьютер.
---
* Создать новую ветку.
---
* Добавить файл с инструкцией в новую ветку.
---
* Дополнить инструкцию разделами по работе с удалёнными репозиториями, pull request.
---
* Зафиксировать изменения (коммиты).
---
* Отправить изменения на GitHub.
---
* На сайте GitHub выполнить **Pull request**.
---
# Работа с удалёнными репозиториями
## 1. Команда **git clone**
Копировать внешний репозиторий на свой ПК можно командой git clone. Команда `git clone` составная: она не только загружает все изменения, но и пытается слить 
все ветки на локальном компьютере и в удаленном репозитории.
## 2. Команда **git pull**
Команда позволяющая скачать все из текущего репозитория и автоматически
сделать merge с нашей версией `git pull`.
## 3. Команда **git push**
Отправить свою версию репозитория во внешний репозиторий поможет команда `git
push`. При первом её использовании нужна авторизация. Эта команда позволяет отправить нашу версию репозитория на внешний репозиторий. Требует авторизации на внешнем репозитории.
# Как настроить совместную работу
* Создать аккаунт на GitHub.com
* Создать локальный репозиторий
* “Подружить” ваш локальный и удалённый репозитории. GitHub при создании нового репозитория подскажет, как это можно сделать
* Отправить (push) ваш локальный репозиторий в удалённый (на GitHub), при этом возможно, вам нужно будет авторизоваться на удалённом репозитории
* Провести изменения “с другого компьютера”
* Выкачать (pull) актуальное состояние из удалённого репозитория
# Работа с **pull request**
В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают команду `pull request`. Предлагать изменения на GitHub нужно в отдельной ветке. Сначала пользователь копирует репозиторий на свой компьютер, делает fork репозитория, затем клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет изменения командой push в свой аккаунт на GitHub и даёт команду pull request. 
## Как сделать pull request
* Делаем  (ответвление) репозитория fork
* Делаем `git clone` версии репозитория СВОЕЙ
* Создаем новую ветку и в НЕЕ вносим свои изменения
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой GitHub
* На сайте GitHub нажимаем кнопку pull request
# Просмотр удалённых репозиториев
Для того, чтобы просмотреть список настроенных удалённых репозиториев, вы можете запустить команду `git remote`. Она выведет названия доступных удалённых репозиториев. Если вы клонировали репозиторий, то увидите как минимум `origin` — имя по умолчанию, которое Git даёт серверу, с которого производилось клонирование.
```
$ git clone https://github.com/schacon/ticgit
Cloning into 'ticgit'...
remote: Reusing existing pack: 1857, done.
remote: Total 1857 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (1857/1857), 374.35 KiB | 268.00 KiB/s, done.
Resolving deltas: 100% (772/772), done.
Checking connectivity... done.
$ cd ticgit
$ git remote
origin
```
Вы можете также указать ключ `-v`, чтобы просмотреть адреса для чтения и записи, привязанные к репозиторию.
```
$ git remote -v
origin	https://github.com/schacon/ticgit (fetch)
origin	https://github.com/schacon/ticgit (push)
```
Для того, чтобы добавить удалённый репозиторий и присвоить ему имя (shortname), просто выполните команду `git remote add <shortname> <url>`:
```
$ git remote
origin
$ git remote add pb https://github.com/paulboone/ticgit
$ git remote -v
```