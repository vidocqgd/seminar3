# **Инструкция по использованию системы контроля версий Git**

![Эблема Гит](git.jpg)

## Что такое Git

Программа Git это - распределённая система управления версиями.

## Инициализация репозитория

Чтобы инициализировать (создать) новый репозиторий нужно ввести в терминале команду:

    git init

## Проверка состояния репозитория

Чтобы проверить состояние репозитория нужно ввести команду

    git status

## Добавление изменений в индекс

Чтобы добавить изменение в индекс следующего коммита нужно ввести команду:

    git add <filename>

## Фиксация изменений

Чтобы зафиксировать изменения (добавленные ранее к отслеживанию) необходимо использовать команду:

    git commit

Чтобы ввести краткое сообщение в процессе создания коммита необходимо использовать эту же команду с дополнительной опцией:

    git commit -m "сообщение"
    
## Просмотр истории коммитов

Чтобы просмотреть историю изменений (коммитов) применяется команда:

    git log

Для отображения лога в кратком виде (один коммит-одна строка) используется та же команда с добавлением опции:

    git log --oneline

Для отображения всех коммитов (вне зависимости от того на какой из них мы переключены) используется команда:

    git log --all

## Переключение между версиями

Чтобы переключиться на другую (ранее сохраненную) версию репозитория используется команда:

    git checkout <hash>

hash - это идентификатор коммита, показываемый в логе.

## Просмотр различий между коммитами

Для просмотра различий между текущим состояния репозитория и последним закоммиченным используется команда:

    git diff
Для просмотра различных версий репозитория используется команда:

    git diff <hash1> <hash2>

## Ветвление

Ветки в гит нужны для того, чтобы разделять код

### Создание новой ветки

Чтобы создать новую ветку используется команда

    git branch <имя ветки>

### Просмотр всех веток

Чтобы посмотреть какие ветки существуют и на какой мы находимся используется команда

    git branch

### Переключение между ветками

Чтобы переключиться на другую ветку используется команда

    git checkout <имя ветки>

### Слияние веток

Чтобы влить одну ветку в другую необходимо, находясь в целевой ветке, выполнить команду

    git merge <имя вливаемой ветки>

### Удаление ветки

Чтобы удалить ветку, которая больше не нужна используется команда

    git branch -d <имя ветки>

### Конфликты при слиянии

Если одна и та же строка в разных версиях записана по-разному возникает конфликт. Чистый Гит автоматически сохраняет оба изменения, далее требуется вручную внести нужные правки и сделать коммит.

VSCode дает возможность выбрать сохраняемое изменение (входящее, сущетсвующее или оба)

## Удаленные репозиториии

Удаленные репозитории это оч полезная штука
