## Задача

* Создать виртуальную машину на vscale, cгенерировать случайный пароль с помощью terraform   пользователю root и выполнить  с помощью provisioner, сохранить всю информацию в локальный файл devs.txt при помощи Terraform

 - Файл должен быть такого содержания: <DNS имя машины> <ip машины> <пароль пользователя root

## Предпосылки

* Установить terraform
* Установить Go 1.13 (to build the provider plugin)
* Собрать плагин terraform для vscale

## Развертывание

* Конфигурируем main.tf
* Выносим описание variables  в отдельный файл variables.tf
* Описываем в фале outputs.tf выводимые значения
* Переменные объявляем в файле terraform.tfvars (В файле объявляем токен, имя образа, Id дата-центра,secret_key, access_key для AWS, регион для AWS)
* В файле terraform.tfvars.sample описано назначение переменных

## Проверяем подключение по ssh

*  ssh root@95.213.235.103
*  ssh root@46.161.54.112
*  cat ~/.ssh/authorized_keys (проверяем пробросились ли все ключи)


## Авторы

  - Sergey Babanin https://gitlab.rebrainme.com/babaninsergey

