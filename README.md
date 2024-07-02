# Шпаргалка по git-у

## Установка Git

Windows - [Ссылка для установки git](https://git-scm.com/download/win) 

Linux - все стоит по-умолчанию

Проверить установку git можно с помощью команды
```shell
git -v
```

## Создание SSH-ключей для GitHub и других похожих сервисов

#### Генерация ключа
```shell
ssh-keygen -t ed25519 -C "Электронная почта, к которой привязан сервис"
```

#### Вывод в консоль публичного ключа
```shell
cat ~/.ssh/id_ed25519.pub
```

## Настройка пользователя git

```shell
git config --global user.name "Имя пользователя"
git config --global user.email "Почта"
```

## Создание репозитория

```shell
mkdir "Папка с проектом"
cd "Папка с проектом"
git init
git remote add origin "Ссылка на репозиторий"
```

## Создание коммитов

#### Добавление всех файлов из корневого каталога и его подкаталогов
```shell
git add --all
```

#### Создание коммита
```shell
git commit -m "Содержание коммита"
```

Если под windows при создании коммита забыть добавить флаг -m и текст с содержанием коммита, то откроется ~~vim~~ и вы от туда
<span style="color: red; font-size: large; font-weight: bold;">НЕ ВЫБЕРЕТЕСЬ НИКОГДА</span> (esc, :w, :q)

## Толкание коммита на удаленный сервер

#### Первый раз
```shell
git push -u origin "Название главной ветки (обычно master или main)"
```
#### Все последующие
```shell
git push
```

## Просто полезные команды

#### Статус git
```shell
git status
```

#### Вывести историю коммитов в виде графа
```shell
git log --graph --all
```

#### Вывести все коммиты (в том числе, те которые были в ветках без названия) 
```shell
git reflog
```

#### Помогите!!!
```shell
git help
```