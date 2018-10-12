# Docker Compose + Rails
Criar arquivos:
* Dockerfile
* docker-compose.yml
* Gemfile
* Gemfile.lock(vazio)

```
$ docker-compose run web rails new . --force --database=postgresql
$ sudo chown -R $USER:$USER .
$ docker-compose build
```
Sempre que o Gemfile for alterado, devemos executar o comando **$ docker-compose build**.

Atualizar arquivo config/database.yml para:
```
default: &default
  adapter: postgresql
  encoding: unicode
  host: db
  username: postgres
  password:
  pool: 5

development:
  <<: *default
  database: myapp_development


test:
  <<: *default
  database: myapp_test
```
Para iniciar nossas instâncias do docker:
```
$ docker-compose up
```
Para criar o banco de dados:
```
$ docker-compose run web rake db:create
```
