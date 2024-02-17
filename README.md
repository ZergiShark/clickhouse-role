Role Name
Роль для установки clickhouse.

Компоненты:
clickhouse-client
clickhouse-server
clickhouse-common-static

Создаётся таблица для логов
Создаётся пользователь для записи в БД
Конфигурируется clickhouse-server для работы внешних подключений
Requirements
Role Variables
Переменные для установки кредов default/main.yml:

clickhouse_user: user
clickhouse_password: password
Переменные для установки необходимых пакетов и конфигурационных файлов clickhouse vars/main.yml

```
clickhouse_version: "22.10.4.23"
clickhouse_packages:
  - clickhouse-client
  - clickhouse-server
  - clickhouse-common-static
clickhouse_config_path: /etc/clickhouse-server/config.xml
clickhouse_users_path: /etc/clickhouse-server/users.xml
```
Dependencies
A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
hosts: clickhouse
roles:
  - role: clickhouse-role
License
MIT

Author Information
