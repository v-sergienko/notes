# Записная книжка

[TOC]

## Создание рабочей учётной записи

Все деяствия выполняются из-под отдельной учётной записи, например - sscadm

    sudo useradd -c "SSC Administrator" -m sscadm
    passwd sscadm

Принципиально нет необходимости для устнаовки пароля для учётной записи sscadm,
так как в большинстве случаев для её использования будет применяться конструкция

    sudo su - sscadm

Для удоства настраивается sudo для учётной записи

    echo "sscadm ALL = (ALL) NOPASSWD:ALL" | sudo tee /etc/sudoers.d/sscadm
    sudo chmod 0640 /etc/sudoers.d/sscadm
