# Автостопом по GIT (Windows version)

### Step 1. Регистрируемся на GitHub
[GutHub](https://github.com 'Просто добавь себя по-английски')
### Step 2. Устанавливаем терминал с Git на комп
[Git Bash](https://git-scm.com 'Качни, установи, расслабся')
### Step 3. Локальная движуха
1. Одноразовая настройка Git Bash
* Запускаем Git Bash и проверяем версию проги (чек на корректность установки, если всё ок - будут какие-то циферки, например "2.41.0.windows.3")
~~~bash
git version
~~~
* Регимся локально - имя и мыло, что слили при  регистрации на GitHub
~~~bash
git config --global user.name "твоё имя"
git config --global user.mail "твоя почта для спама (шутка, почти)"
~~~
* Проверяем правильность предыдущего ввода (там увидишь в строчках свои ник/мыло)
~~~bash
git config --list
~~~ 
2. Создаём папку для будущих Git-проектов (опционально)
~~~bash
cd /c/
mkdir FOR_ALL_GIT
~~~
3. Внутри созданной папки (опционально) или любом другом месте, создаём папку для конкретного Git-проекта и входим в неё
~~~bash
cd FOR_ALL_GIT
mkdir YP_1_readme
cd YP_1_readme
~~~
4. Инициализируем Git
~~~bash
git init
~~~
5. Бахнем добавлением и коммитом для фиксации
~~~bash
git add .
git commit -m 'Самый первый и тупой коммент'
~~~
6. Хотим приватность? Создаём ключи для шифрования!
~~~bash
ssh-keygen -t ed25519 -C "мыло (еще раз сестра, его мыло)"
~~~
### Step 4. Связываем узами комп и удалёнку
1. Создаём на GitHub новый репозиторий [New](https://github.com/new 'Название любое, приват/паблик как хошь, усё')
2. Клик по ~~кнопке~~ выпадающему меню **Code** и копируем во вкладке **SSH** путь типа "git@github.com:имя_твоё/название_твоё.git"
3. Меняем **master** на **main** (мы же любим Африку?)
~~~bash
git branch -M main
~~~
4. Вставляем этот путь в команду правым кликом и выбрав **вставить** (у меня Ctrl+Shift+V не пашут, но вдруг у вас пахать и сеять будут)
~~~bash
git remote add origin git@github.com:имя_твоё/название_твоё.git
~~~
5. Проверяем правильно ли мы всё сделали
~~~bash
git remote -v
~~~
6. Повяжем их вместе
~~~bash
git push -u origin main
~~~ 
### Step 5. Лепим горбатого
* На всё последущее есть:
~~~bash
git add .
git commit -m "Искромётный коммент"
git push
~~~
* Всегда перед всеми манипуляциями проверяем статус Git-a
~~~bash
git status
~~~
* Можно глянуть на GitHub и устроить себе день седьмой, ибо все **ok**, а если не, то читать курс [Яндекс.Практикум](https://practicum.yandex.ru/git-basics/?from=catalog 'Основы работы с Git')

### Step 6. Даже обезьяна жмёт кнопку. А что перед этим? Академические знания
1. О хэше  
Любую конечную последовательность данных можно представить в сокращенном уникальном выражении, не несущем информацию о контенте, но с помощью определённого алгоритма, однозначно идентифицирующего связь между данными и этой "сжатой" комбинаторикой. Итак, хэш - это уникальная краткая запись, полученная с помощью специального алгоритма и однозначно идентифицирующая массив данных независимо от платформы и количества повторов его получения. Любое изменение массива данных даже "атомарно" приводит к существенному изменению хэша.

2. О логе
~~~bash
git log
git log --oneline
~~~
Команда выводит детальный лог всех изменений, второй вариант сокращённая форма - выводит только комменты.
