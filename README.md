
### Setup Template Laravel 10 with docker 


#### Setup do Ambiente

1. Clone este repositório:
```bash
git clone https://github.com/zzeis/relogioponto.git
cd relogio-ponto
```


2.  Dentro do container app Instale as dependências do PHP e do front-end:

```bash
docker exec -it app(nome do seu container app) composer install
docker exec -it app(nome do seu container app)  npm install
```

3.  Gere a chave da aplicação Laravel(Dentro do container App):

```bash
docker exec -it app(nome do seu container app) php artisan key:generate
```

4. Rode as migrações para criar o banco de dados:

```bash
docker exec -it app(nome do seu containre app) php artisan migrate
```

5. Acesse o sistema no navegador:

-   URL: [http://localhost:8989](http://localhost:8989)

#### containers

    1 - mysql 8
    2 - app (laravel)
    3 - nginx
    4 - redis
    5 - worker para filas
    6 -

#### arquivos importantes 

    1 - dockerfile 
    2 - docker-compose 
    3 - .env.example
