# clickhouse-docker-compose
This GitHub repository offers a Docker Compose configuration for easy deployment and management of ClickHouse clusters.

# Проект ClickHouse Docker Compose

## Введение

Этот проект представляет собой простой способ развертывания ClickHouse с использованием Docker Compose. Он включает в себя конфигурацию для двух пользователей: `admin` (с правами администратора) и `user_ro` (только для чтения).

## Использование

1. Клонируйте этот репозиторий на свой локальный компьютер.
2. Замените `admin_password` и `user_ro_password` на свои собственные пароли в файле `users.xml`.
3. Запустите `docker-compose up` в каталоге с файлами `docker-compose.yml` и `users.xml`.

После этого ClickHouse будет доступен на порту 8123. Вы можете подключиться к нему с помощью библиотеки `clickhouse_connect`, указав хост `localhost` и порт `8123`.

## Безопасность

По умолчанию этот пример предоставляет доступ к ClickHouse из любого IP-адреса, что может быть небезопасно. Вы должны настроить сети в соответствии с вашими требованиями безопасности.

## Лицензия

Этот проект распространяется под лицензией MIT.
