## Домашнее задание 12

1. Запретить всем пользователям, кроме группы admin логин в выходные

Написан скрипт test_login.sh, проверяющий день недели и присутствие пользователя в группе admin. Этот скрипт прописан в /etc/pam.d/sshd для модуля pam_exec.so

2. Дать конкретному пользователю права работать с докером и возможность рестартить сервис docker

Права работать с докером - пользователь включен в группу docker.
Возможность рестартить сервис docker - написано правило 51-docker.rules для polkit, размещено в /etc/polkit-1/rules.d


Оба файла, test_login.sh и 51-docker.rules копируются на машину вагрантом с помощью provision file, затем скриптом script.sh перемещаются в нужное место.
script.sh также создает пользователей, добавляет их в группы, устанавливает docker.