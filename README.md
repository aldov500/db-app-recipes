# db-app-recipes

# Crear un volumen local
docker volume create mysql-db-data
docker volume ls

# Crear el contenedor
$  docker run -d -p 33060:3306 --name mysql-db  -e MYSQL_ROOT_PASSWORD=secret --mount src=mysql-db-data,dst=/var/lib/mysql mysql

# Entrar al contenedor
docker exec -it mysql-db mysql -p

# Terminar el proceso
docker rm -f mysql-db

# Add to dbeaver
allowPublicKeyRetrieval=True
