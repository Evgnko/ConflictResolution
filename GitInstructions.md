# Инструкция по Git
## Полное руководство на этом сайте

[![N|Solid](https://git-scm.com/images/logo@2x.png)](https://git-scm.com/docs)


Git это распределённая система управления версиями.

### Приемущества git
- Ведение истории разработки проекта
- Возможность просмотреть и откатить изменения
- Удобный просмотр изменений
- Удобно вести совместную рарзработку

## Некоторые команды
### Первичная настройка
- git config --global user.name = "My Name"
> Установка никнейма, под которым будут оставляться коммиты
- git config --global user.email = myemail@mail.com
> Установка почты, от которой будут оставляться коммиты

### Основные команды
- git init
> Инициализация локального репозитория в текущей папке
- git clone https://github.com/USERNAME/REPO.git
> Клонирование из указанного репозитория
> Если репозиторий приватный, то программа запросит Username и Password
> Username это ваш ник на GitHub
> Password это токен, который нужно сгенирироват следующим образом
[![N|Solid](https://miro.medium.com/max/1400/1*SSRjtoQ0H2X3SBPOiJ5rZw.jpeg)](https://docs.github.com/ru/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
- git remote add origin https://github.com/USERNAME/REPO.git
> Git связывает удаленный URL-адрес с именем. Удаленный репозиторий по умолчанию обычно называется origin
> Данная команда связывает имя origin с URL-адресом https://github.com/USERNAME/REPO.git
- git add .
> Добавление всех файлов в состояние ожидания
- git status
> Проверка состояния
- git commit -m "Название коммита"
> Добавление коммита с названием
- git push origin --all
> Отправление всех веток в удалённый репозиторий

## Что такое .gitignore?

> Это специальный файл, в котором
> прописываются файлы и папки,
> которые будут игнорироваться при
> добавлении в git. Обычно это файлы 
> конфигурации, а также другие
>  временные файлы и папки. 

## Работа с Github

### 1. Создание ветки
> Для добавления ветки через GitHub - зайдите в репозиторий.
> Во вкладке Code нажмите на ветку (в данном случае main) и нажмите View all branches
![N|Solid](https://sun9-west.userapi.com/sun9-2/s/v1/ig2/Dhh4Xf7-wbUHfiX1RzVZGSV5oN7KsUwcVfStJwfjsIAk2iN5K1BNcGMPn5mLILm2n_57iKcbVljLf9LryY9hVaLC.jpg?size=1280x766&quality=96&type=album)

> Нажмите зелёную кнопку New branch
![N|Solid](https://sun9-north.userapi.com/sun9-88/s/v1/ig2/XHHzHCx4-Kwso68LiEKAdG7c_t5MGIe_GXpUeuNyyXHyFOpK0uilz2OKZXYosJtwVwFuL2ZSceQZsPzhPapchcTy.jpg?size=1280x766&quality=96&type=album)

> Введите имя ветки и нажмите Create branch
![N|Solid](https://sun9-east.userapi.com/sun9-20/s/v1/ig2/OAdiaPhDn6bqzH8Ff0ID8F62YZjALBrUF5_o58isANivUDrFO3L4rDoWtKp_rTFODli-xbzEBR6BlH5z4R_woKVC.jpg?size=902x580&quality=96&type=album)

### 2. Создание конфликта

> Для создания конфликта был использован этот файл. Чтобы вызвать конфликт достаточно поменять строчки инструкции местами (в ветке main сделать коммит с новой инструкцией, а в ветке conflict взять эту новую инструкцию и поменять некоторые строки местами)
> Пример файла в ветке main (обратите внимение на номер строки) ![N|Solid](https://sun9-east.userapi.com/sun9-33/s/v1/ig2/9dDJhOBuS7Nh-2zkorEdx7zQuckH4-q8z1WOH7IsMLDA49wP-RnIE_ypsiw7l00gKFwNp1fLIVJes3LGbY9Vv0r7.jpg?size=1280x515&quality=96&type=album)
> Пример файла в ветке conflict (обратите внимение на номер строки)
![N|Solid](https://sun9-west.userapi.com/sun9-8/s/v1/ig2/Rt6EkTnxMunof4pHaoeEqJn9YwiuDsT32XppilUXIc4B0qkyl6mqNbLcX1nmYtHEdvv8CIQ5P-BKQgUBFIkJeO8p.jpg?size=1280x622&quality=96&type=album)

> Теперь пытаемся соеденить ветки
> Для этого надо перейти во вкладку Pull requests и нажать New Pull requests ![N|Solid](https://sun9-east.userapi.com/sun9-29/s/v1/ig2/BAxVEz-53Ob-hdhqeydzf9LqzotMzWlv3C3i_x6A2nPTXt0bMGiANjUYnIBhPbVNnndHbithXtyUFoNlleujyYFg.jpg?size=1280x339&quality=96&type=album)

> В compare выбираем какую ветку хотим включить в ветку main
> Видим "Can’t automatically merge." что говорит о существующем конфликте
![N|Solid](https://sun9-east.userapi.com/sun9-42/s/v1/ig2/0V82IW_ucLwB6RdV8IWSeVq1al4H2qBIfnVme-2gTqPNmIhFzSlpF-jXqqjjJyPX0KvxpY3Ju42MKQ45kacIyqgp.jpg?size=1280x483&quality=96&type=album)

### 2. Разрешение конфликта

> Не отчаиваемся и нажимаем Create pull request
![N|Solid](https://sun9-east.userapi.com/sun9-42/s/v1/ig2/0V82IW_ucLwB6RdV8IWSeVq1al4H2qBIfnVme-2gTqPNmIhFzSlpF-jXqqjjJyPX0KvxpY3Ju42MKQ45kacIyqgp.jpg?size=1280x483&quality=96&type=album)
> Тут также нажимаем Create pull request
![N|Solid](https://sun9-north.userapi.com/sun9-78/s/v1/ig2/PaKwkXlQONZ7u9dI7fpoNOjM9xxnv834c8KloqCjiZalCAN2apfcnxsk-xGBz4q0jC3RJCOVV7UIDDXlYyAPuX3s.jpg?size=1280x756&quality=96&type=album)

> Попадаем на страницу "запроса на вытягивание"
> Тут другие разработчики могут комментировать данные предложенные изменения, а создатель репозитория решает приминять ли данное изменение в указанную ветку
![N|Solid](https://sun9-west.userapi.com/sun9-68/s/v1/ig2/eQpdn6gLlPAF_EaGlq1ur_QtGgefq1732mRVVI4vru9XZUI476TSBHnOYazbBip8pMZhC8kIG35q4b8BdkvWM9jF.jpg?size=1280x762&quality=96&type=album)
![N|Solid](https://sun9-west.userapi.com/sun9-71/s/v1/ig2/TpCIMJc1NSlJKsj54ZKFDhoZxbFlw-vUBzGAMBJ40-bFvg2t-teEyNK12hjq6u5VXkAd3o8QLg4S-u3op8jc7GpY.jpg?size=1280x762&quality=96&type=album)
> Тут нам нужно нажать на кнопку Resolve conflicts
> И в открывшемся редакторе вставляем нашу инструкцию (этот файл) 
