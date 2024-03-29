# psql
Заметки для PostgreSQL

Статья - https://telegra.ph/Ispolzuem-PostgreSQL-bystro-i-legko-07-31

Канал: https://t.me/dev_survival

# Базовое управление
[Для Ubuntu видео установка](https://www.youtube.com/watch?v=kWUW3sMK0Mk)

Входим как пользователь ` postgres ` - ` sudo -i -u <username> ` 

Для выхода - ` exit `


### Входим в управление postgres -  `psql`

> Просмотр баз данных - `\l`

> Вывести список всех таблиц в текущей базе - `\dt`

> Подключиться к базе данных - `\c <db_name>`

> Выход из управления postgres - `\q`

> Список пользователей - `\du`

### Чтобы что-то делать с базами данных, нужно быть в нужном пользователе:

> Создание баз данных - `createdb <db_name>`
 
> Удаление базы - `drop <namdb>`


### Изменение пароля пользователя :

> ` alter user <username> with password '<password>'; `


### Создать нового пользователя:

> ` create user <usernmae> with password '<password>'; `


### Удаление пользователя:

> ` drop user <username>; `

---

### Выдать права пользователю:

> ` alter user <username> with <role>; `
	
```
ROLE допустимые параметры:

   | SUPERUSER         | NOSUPERUSER

   | CREATEDB          | NOCREATEDB

   | CREATEROLE        | NOCREATEROLE

   | INHERIT           | NOINHERIT

   | LOGIN             | NOLOGIN

   | REPLICATION       | NOREPLICATION

   | BYPASSRLS         | NOBYPASSRLS

   | PASSWORD 'пароль' | PASSWORD NULL

   | CONNECTION LIMIT предел_подключений
   | VALID UNTIL 'timestamp'
```

### Передать права на базу данных:

> ` ALTER <TABLE | DATABASE> <name> OWNER TO <user> `
