# Projeto de Microserviços
Projeto para o desenvolvimento de microserviços.

## Informações importantes
No mysql descrito no docker-compose, não consiguirá realizar *migrate* no comando `php artisan migrate`. Para contornar essa situação é necessário criar um usuário manualmente e conseder à ele as devidas permissões e também criar o database.

### Passos
- Acessar o container mysql pelo comando: ```docker exec -it your_container_name_or_id bash```
- Entrar como usuário root: ```mysql -u nome_usuario -p```
  Pressionar Enter no campo de senha.
- Criando usuário com o comando: ```CREATE USER 'nome_usuario'@'%' IDENTIFIED BY 'senha_usuario';```
- Criando tabela com o comando: ```CREATE DATABASE productapp;```
- Garantindo privilégios com o comando:```GRANT ALL PRIVILEGES on productapp.* to 'root'@'%' IDENTIFIED BY 'pswd';```

Pronto! Agora o comando `php artisan migrate` deve funcionar normalmente.

# Laravel
[Laravel](README.laravel.md)
