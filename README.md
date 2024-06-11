# Hey, it's cool tips for `Git`
---
[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)
1. Используйте __Git__ для управления версиями проекта локально
2. Синхронизируйте локальные проекты с различными репозиториями, такими как __GitHub__
3. Работайте на проектом в команде

## Создание и подключение
##### Рассмотрим все шаги детально:
---
### На __windows__ локальные репозитория могут храниться тут:
```bash
cd ~/source/repos/
```
##### -🗂️ Тут обычно храняться все локальные репозитории __Git__
[![capture-20240610143550648.png](https://i.postimg.cc/pTZwfNYV/capture-20240610143550648.png)](https://postimg.cc/ftVqsrr1)

### Инициализация крутого репозитория
```bash
git init
```
##### - 🗺️ Команда выполняется непосредственно в начальной директории проекта

### 💾 Добавим файлы с изменениями, это как __ctrl+c__
```bash
git add [Название_файла | .]
```

### 🔗 Объеденим все изменения
```bash
git commit -m "Что объединяет изменения?"
```

### Поделимся актуальной версией с удалённым репозиторием
```bash
git push
```

#### ⚠️ Первое добавление на __GitHub__
>  Если на удалёном репозитории ещё пусто, тогда `git remote add origin [git@github.com:username/Имя_репозитория.git]`
>  Затем, `git push -u [master | main]`

# Статусы файлов
---

```mermaid
graph LR;
untracked -- "git add" --> staged;
modified -- "git add" --> staged;
staged -- "git commit" --> tracked;
```

```mermaid
mindmap
  root((Файл))
    Новый файл
      untracked
      ::icon(fa fa-book)
      Добавление
        git add "Название_файла"
    Изменённый файл
      modified
        git add "Название_файла"
            git commit -m "Что сделано?"
      tracked
        Старая версия файла
    Не изменённый файл
      tracked

```

# __HEAD__ && __HASH__
---

```mermaid
---
title: Хэширование
---
stateDiagram-v2
    [*] --> State1
    State1 --> [*]

    State1: Commit
    note right of State1
        Информация об изменениях: дата, автор, изменёния в файлах
    end note
    State1 --> State2: SHA-1
    note right of State2
        Хэш - идентификатор коммита, длинной 40 символов
    end note

```
**Author: a1ndreay**
