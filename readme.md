## Домашнее задание 1

Установлены Vagrant, Packer и VirtualBox
Сделан форк репозитория dmitry-lyutenko/manual_kernel_update и затем склонирован на рабочую машину.

Заапущена виртуалка из содержащегося в репозитории Vagrantfile.

Внутри виртуалки: подключен репозитория elrepo, скачано и установлено последнее ядро kernel-ml.

В конфиг образа Packer centos.json внесена строка "headless" : "true", затем создан образ centos 7.7 с ядром 5.12.0. Этот образ импортирован в Vagrant и запущен.

Заведен аккаунт на Vagrant Cloud, загружен полученный образ centos.

Все изменения запушены в github.

Адрес образа в Vagrant Cloud - https://app.vagrantup.com/hataldir/boxes/centos-7-5
Репозиторий в github - https://github.com/hataldir/manual_kernel_update