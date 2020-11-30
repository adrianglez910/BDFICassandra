# BDFICassandra

Una vez en la carpeta BDFIcassandra ejecutar
```
docker-compose up -d
```
Para crear el Keyspace agile_data_science es necesario utilizar los siguientes comandos:
```
docker ps -a  
```
para comprobar el ID del contenedor de Cassandra
```
docker exec -it <contenedor-ID> cqlsh
```
y
```
CREATE KEYSPACE IF NOT EXISTS agile_data_science WITH REPLICATION = { 'class' : 'SimpleStrategy', 'replication_factor' : 1 };
```
para crear el keyspace. 

Volver a ejecutar 
```
docker-compose up -d --build spark-submit
```
para no tener errores.
Ir a la pagina web de la prediccion y esperar un poco antes de pulsar submit.
Abrir la consola de la pagina web y verificar que el json recibido es correcto.
