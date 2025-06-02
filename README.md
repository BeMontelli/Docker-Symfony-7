# Symfony 7 / Docker
- Link inspiration : https://www.citizenz.info/article/symfony-7-avec-docker

## Docker Config Files
- compose.yml
- Dockerfile
- php.ini
- nginx.conf
- README.md

## Symfony Installation
- > symfony new --webapp app
- generate app/ folder with symfony 7 startup project

## Docker commands
- Start Docker
    - > docker-compose up -d
- Stop Docker
    - > docker-compose stop
- Delete containers
    - > docker-compose down

## Local URLs access
- Symfony : http://127.0.0.1:8080
- PhpMyAdmin : http://127.0.0.1:8081
- Mailpit : http://127.0.0.1:8025

## Troubleshootings access var/cache && var/log
- > docker-compose exec php chmod -R 777 var/cache
- > docker-compose exec php chmod -R 777 var/log