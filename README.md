# Containerisation_Django_REST_MySQL_API
Containerising a Django, REST, MySQL API application.

```
docker-compose up --build -d
```

```
docker-compose exec web python3 manage.py createsuperuser
```

```
docker-compose exec web python3 manage.py makemigrations
docker-compose exec web python3 manage.py migrate
```

```
docker-compose exec db mysql -u django_admin -p # django_admin set in docker-compose
```

```
http://localhost:8888/admin
```

```
docker volume ls
docker volume inspect mysql_data
```

```
docker-compose exec db mysqldump -u django_admin -p countriesdb > backup.sql
docker-compose exec -T db mysql -u django_admin -p countriesdb < backup.sql
```
