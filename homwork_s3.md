# Мое руководство по Git
## Установка Git
1. Скачиваем установочный файл с официального сайта Git - git-scm.com
2. Открываем терминал и проверяем установлен ли у нас Git, для этого можно ввести команду:
    - git version
3. Далее вводим две команды, чтобы создать "пользователя":
    - git config --global user.name "enter your name"
    - git config --global user.email "enter your email"
## Создание репозитория
1. Создаем папку проекта на своем ПК
2. В терминале вводим команды:
    - cd <path_to_the_project>
    - git init (создает репозиторий в папке нашего проекта)
3. Создаем новый файл в своем проекте, и чтобы Git его отслеживал вводим команду:
    - git add <file.name>
4. Создаем commit:
    - git commit -m "comment" (создает сохраненную версию проекта в репозитории)
## Список команд в Git:
- git --version - проверка текущей установленной версии Git
- git init - инициализирует репозиторий (в папке с проектом создается скрытая папка .git)
- git status - текущее состояние Git (есть ли новые изменения или новые файлы)
- git add <file.name> - добавляет файл в репозиторий (имя файла полностью писать необязательно, достаточно ввести первую букву в нужном регистре и нажать "Tab", имя заполнится автоматически)
- git commit -m "comment" - команда, фиксирует (сохраняет) текущее состояние файла (у каждого commit есть hash (уникальный id) и комментарий; с помощью id мы можем перемещаться к более старым изменениям и наоборот)
- git log - журнал изменений
- git checkout - перемещение между commit'ами и между ветками файла (для перемещения по commit'ам необходимо добавить первые 4 символа commit'а, для перемещения между ветками, необходимо добавить название ветки)
- git diff - показывает разницу между текущем файлом и сохраненным 
- git branch - вывести все ветки 
- git branch <branch_name> - создать новую ветку
- git log --graph - вывод лога с движением веток
## Инструкция для синхронизации работы с Github.com:
- создать аккуаунт
- создать локальный репозиторий (на своем ПК и т.п.)
- синхронизировать локальный и удаленный репозитории. Github предоставит подсказки
    Команды для размещения репозитория в интернете:
    - git remote add origin <ссылка с github с именем репозитория>
    - git branch -M master
    - git push -u origin master (команда отправляет локальный репозиторий в удаленный)
- git pull (команда для скачивания удаленного репозитория и синхронизации с локальным)
## Инструкция для работы с чужим проектом через github:
- на github делаем fork интересующего нас репозитория (проекта)
- git clone (команда для клонирования репозитрия на наш локальный компьютер)
- создаем файл в репозитории README.***
- git branch _имя ветки_ (команда для создания ветки, в которой будем производить изменения)
- git push (команда для отправки репозитория с изменениями в свой аккаунт на github)
- на github появляется возможность отправить изменения владельцу репозитория, в который мы хотели бы внести свои изменения (pull request)
