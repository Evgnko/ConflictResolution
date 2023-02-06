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

## Работа с Github

### 1. Создание ветки
> Для добавления ветки через GitHub - зайдите в репозиторий.
> Во вкладке Code нажмите на ветку (в данном случае main) и нажмите View all branches
![N|Solid](https://sun9-west.userapi.com/sun9-2/s/v1/ig2/Dhh4Xf7-wbUHfiX1RzVZGSV5oN7KsUwcVfStJwfjsIAk2iN5K1BNcGMPn5mLILm2n_57iKcbVljLf9LryY9hVaLC.jpg?size=1280x766&quality=96&type=album)

> Нажмите зелёную кнопку New branch
![N|Solid](https://sun9-north.userapi.com/sun9-88/s/v1/ig2/XHHzHCx4-Kwso68LiEKAdG7c_t5MGIe_GXpUeuNyyXHyFOpK0uilz2OKZXYosJtwVwFuL2ZSceQZsPzhPapchcTy.jpg?size=1280x766&quality=96&type=album)

> Введите имя ветки и нажмите Create branch
![N|Solid](https://sun9-east.userapi.com/sun9-20/s/v1/ig2/OAdiaPhDn6bqzH8Ff0ID8F62YZjALBrUF5_o58isANivUDrFO3L4rDoWtKp_rTFODli-xbzEBR6BlH5z4R_woKVC.jpg?size=902x580&quality=96&type=album)

## Что такое .gitignore?

> Это специальный файл, в котором
> прописываются файлы и папки,
> которые будут игнорироваться при
> добавлении в git. Обычно это файлы 
> конфигурации, а также другие
>  временные файлы и папки. 
