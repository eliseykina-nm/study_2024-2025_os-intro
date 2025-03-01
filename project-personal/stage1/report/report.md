---
## Front matter
title: "Отчёт по индивидуальному проекту. Этап 1."
subtitle: "Архитектура компьютера и операционные системы"
author: "Елисейкина Надежда Михайловна НММбд-02-24"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

- Создать свой сайт (разместить на Github pages заготовки для персонального сайта)

# Задание

- Установить необходимое программное обеспечение.

- Скачать шаблон темы сайта.

- Разместить его на хостинге git.

- Установить параметр для URLs сайта.

- Разместить заготовку сайта на Github pages.

# Теоретическое введение

## Примеры использования git:

- Система контроля версий Git представляет собой набор программ командной строки. 
Доступ к ним можно получить из терминала посредством ввода команды git с различными опциями.

- Благодаря тому, что Git является распределённой системой контроля версий, резервную копию локального хранилища можно сделать простым копированием или архивацией.

## Основные команды git:

Например, в табл. @tbl:std-dir приведено краткое описание основных команд Git.

: Описание некоторых команд системы контроля версий Git {#tbl:std-dir}

| Команда | Описание команды                                                                  |
|--------------|-----------------------------------------------------------------------------------|
| git init     | Создание основного дерева репозитория  |
| git pull     | Получение обновлений(изменений текущего дерева из центрального репозитория |
| git push     | Отправка всех произведённых изменений локального дерева в центральный репозиторий |
| git status   | Просмотр списка изменённых файлов в текущей директории |
| git diff     | Просмотр текущих изменений  |
| git add .    | Добавление все изменённые и/или созданные файлы и/или каталоги |
| git rm имена_файлов | Удаление файлов и/или каталогов из индекса репозитория |
| git commit -am 'Описание коммита'| Сохранение всех добавленных изменений и всех изменённых файлов |
| git commit   | Сохранение добавленный изменений с внесением комментария через встроенный редактор |
| git checkout -b имя_ветки | Создание новой ветки, базирующейся на текущей | 
| git branch -d имя_ветки | Удаление локальной уже слитой с основным деревом ветки |
| git branch -D имя_ветки | Принудительное удаление локальной ветки |

Полный список команд можно посмотреть на официальном сайте: [Github.com](https://docs.github.com/en/get-started/using-github/github-command-palette)


# Выполнение лабораторной работы

Загружаем последнюю версию hugo :

![Загрузка нужной нам версии](image/01.png){#fig:001 width=70%}

Файл скачивается в папку *"Загрузки"* :

![Скачивание](image/02.png){#fig:002 width=70%}

По завершении скачивания извлекаем архив в ту же папку, в которой мы находимся:

![Извлечение](image/03.png){#fig:003 width=70%}

![Извлечение - выбор папки](image/04.png){#fig:004 width=70%}

![Проверка извлечения](image/05.png){#fig:005 width=70%}

После извлечения файла, нам его необходимо вырезать и вставить в папку */usr/local/bin*:

![Вырезание файла](image/06.png){#fig:006 width=70%}

![Перенос файла](image/07.png){#fig:007 width=70%}

Далее открываем наш github и создаем репозиторий на основе данного нам:

[Репозиторий](https://github.com/wowchemy/starter-hugo-academic)

![Создание репозитория](image/08.png){#fig:008 width=70%}

При создании даём ему имя blog:

![Создание репозитория](image/09.png){#fig:009 width=70%}

После клонируем данный репозиторий в путь */home/nmeliseykina/work*:

![Клонирование репозитория](image/10.png){#fig:010 width=70%}

![Проверка](image/11.png){#fig:011 width=70%}

Переходим в папку *blog* и запускаем *hugo*:

![Hugo](image/12.png){#fig:012 width=70%}

Так как выдало ошибку, доустановим модуль go из-под суперпользователя:

![Доустановка модуля "GO"](image/13.png){#fig:013 width=70%}

Возвращаемся в папку blog и запускаем *hugo*:

![HUGO](image/14.png){#fig:014 width=70%}

После установки необходимых модулей проверяем создание папок и файлов:

![Проверка](image/15.png){#fig:015 width=70%}

Удаляем каталог public:

![Удаляем public](image/16.png){#fig:016 width=70%}

Запускаем hugo server:

![Запуск hugo server](image/17.png){#fig:017 width=70%}

![Запуск hugo server](image/18.png){#fig:018 width=70%}

Открываем ссылку в браузере и видим сайт:

![Шаблон сайта](image/19.png){#fig:019 width=70%}

После проверки в браузере закроем сервер:

![Закрытие hugo server](image/20.png){#fig:020 width=70%}

Создание нового репозитория:

![Github](image/21.png){#fig:021 width=70%}

Название репозитория должно полностью совпадать с именем владельца + github.io:

![Создаем новый репозиторий](image/22.png){#fig:022 width=70%}

Возвращаемся в терминал, в папку work и клонируем туда наш репозиторий (свежесозданный):

![Клонирование репозитория](image/23.png){#fig:023 width=70%}

![Проверка](image/24.png){#fig:024 width=70%}

Переключаемся на ветку "main":

![Переключаемся на ветку "main"](image/25.png){#fig:025 width=70%}

Создаем пустой файл README.md, а затем коммитим все изменения и отправляет на github:

![Создание пустого файла и отправка изменений](image/26.png){#fig:026 width=70%}

![Проверка](image/27.png){#fig:027 width=70%}

Создаем ветку подмодуля, клонируя репозиторий с нашего Github:

![Создаем новую ветку](image/28.png){#fig:028 width=70%}

После выполнения запускаем hugo:

![HUGO](image/29.png){#fig:029 width=70%}

Проверим подключение каталога к репозиторию командой git remote -v:

![Проверка](image/30.png){#fig:030 width=70%}

Добавим изменения на github:

![Загружаем обновления](image/31.png){#fig:031 width=70%}

![Загружаем обновления](image/32.png){#fig:032 width=70%}

Проверка обновлений:

![Проверка github](image/33.png){#fig:033 width=70%}

Открываем наш сайт:

![Шаблон сайта готовый](image/34.png){#fig:034 width=70%}

# Выводы

В ходе данной работы я создала шаблон своего сайта, который в будущем буду дорабатывать, а также запрепила навыки работы с системой контроля версий Git.

# Список литературы{.unnumbered}

1. [Этапы реализации проекта](https://esystem.rudn.ru/mod/page/view.php?id=970806&forceview=1)

2. [Техническая реализация проекта](https://esystem.rudn.ru/mod/page/view.php?id=970807&forceview=1)

3. [Руководство по выполнению первого этапа индивидуального проекта](https://esystem.rudn.ru/mod/url/view.php?id=980904&forceview=1)

4. [Инструменты Git - Подмодули](https://git-scm.com/book/ru/v2/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D1%8B-Git-%D0%9F%D0%BE%D0%B4%D0%BC%D0%BE%D0%B4%D1%83%D0%BB%D0%B8)

::: {#refs}
:::
