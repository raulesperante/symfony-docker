# 🐳 Docker + PHP 7.4 + MySQL + Nginx + Symfony 5 Boilerplate

## Description

This is a complete stack for running Symfony 5 into Docker containers using docker-compose tool.

It is composed by 4 containers:

- `nginx`, acting as the webserver.
- `nginx-proxy`, the reverse proxy
- `php`, the PHP-FPM container with the 7.4 PHPversion.
- `db` which is the MySQL database container with a **MySQL 8.0** image.

## Installation

1. 😀 Clone this rep.

2. Run `docker-compose up -d`

3. The 4 containers are deployed


4. Install symfony

```
cd symfony-docker
docker run --rm -it -v "$(pwd)":/app composer composer create-project symfony/website-skeleton symfony
```

5. Use this value for the DATABASE_URL environment variable of Symfony:

```
DATABASE_URL=mysql://app_user:helloworld@db:3306/app_db?serverVersion=5.7
```

You could change the name, user and password of the database in the `env` file at the root of the project.

## Add fake domain

```
sudo nano /etc/hosts
Add this line:
127.0.0.1 proyecto-symfony.com.devel
```

