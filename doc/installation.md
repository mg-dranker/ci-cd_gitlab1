## Установка Git

sudo apt update
sudo apt install git

## Установка Docker

1. Ообновить существующий список пакетов:

sudo apt update

2. Установить несколько необходимых пакетов, которые позволяют apt использовать пакеты через HTTPS:

sudo apt install apt-transport-https ca-certificates curl gnupg2 software-properties-common

3. Добавить ключ GPG для официального репозитория Docker в систему:

curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

4. Добавить репозиторий Docker в источники APT:

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"

5. Обновить базу данных пакетов и добавить в нее пакеты Docker из недавно добавленного репозитория:

sudo apt update

6. Убедиться, что установка будет выполняться из репозитория Docker, а не из репозитория Debian по умолчанию:

apt-cache policy docker-ce

7. Установить Docker:

sudo apt install docker-ce

8. Docker должен быть установлен, демон-процесс запущен, а для процесса активирован запуск при загрузке. Проверить, что он запущен:

sudo systemctl status docker

## Установка Docker Compose

1. Проверить текущий выпуск и при необходимости обновите его с помощью следующей команды:

sudo curl -L https://github.com/docker/compose/releases/download/1.25.3/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

2. Настроить разрешения:

sudo chmod +x /usr/local/bin/docker-compose

3. Проверить, что установка прошла успешно, с помощью проверки версии:

docker-compose --version










