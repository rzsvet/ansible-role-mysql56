# Ansible role for install mysql 5.6

## Требования

Список поддерживаемых семейств linux:
*Alpine (Only install mysql)
*CentOs (Install, Startup, Setup user with password)

## Переменные

### Описание

mysql_default_password - пароль, который установиться пользователю root при установке

### Значения по-умолчанию

```YAML
---
mysql_default_password: "root"
```

## Установка

Добавить в файл requirements.yml
```
- src: https://github.com/rzsvet/ansible-role-mysql56.git
```
Перед выполнением запустить
```
ansible-galaxy install -r requirements.yml
```

## Применение

Данная роль используется установки mysql и настроке пароля, который находится в переменной mysql_default_password, для пользователя root
Для сохранности ключей их лучше вего прописать в group_vars в переменных mysql_default_password

## Примечание

Данная роль тестовая и врядли пригодится для использования в реальных проектах. Старайтесь не использовать сторонние роли, чтобы случайно не загрузить вредный код.
