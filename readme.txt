POSTMAN: 
BUSCAR PERSONA: 
curl --location 'http://localhost:5000/personas/buscar' \
--header 'Content-Type: application/json' \
--data '{
"dni": "37124931"
}'
AGREGAR PERSONA: 
curl --location 'http://localhost:5000/personas' \
--header 'Content-Type: application/json' \
--data-raw '{
    "nombre": "Susanita",
    "apellido": "Sanchez",
    "email": "susanitasanchezx@gmail.com",
    "dni": "34567890"
}'
MODIFICAR PERSONAS:
curl --location --request PUT 'http://localhost:5000/personas' \
--header 'Content-Type: application/json' \
--data-raw '{
    "dni": "37124931",
    "nombre": "Edith",
    "apellido": "Nuñez",
    "email": "edithnunex@gmail.com@example.com"
}'
BORRAR PERSONA:
curl --location --request DELETE 'http://localhost:5000/personas/334456678' \
--header 'Content-Type: application/json' \
--data ''
curl --location 'http://localhost:5000/personas' \
--header 'Content-Type: application/json' \
--data ''
OBTENER PERSONA: 
curl --location --request GET 'http://localhost:5000/personas' \
--header 'Content-Type: application/json' \
--data '{
"dni": "37124931"
}'

----------------------------------------------------------------------------------------------------------------
CREACIÓN BASE DE DATOS EN DBEAVER:
Crear nueva base de datos, llamada persona
dentro de persona se crea una tabla llamada persona
se genera la primer columna llamada id, que se autoincremente, en contraints se le asigna a la columna a id la primary key
se crean las demás columnas, en mi caso, nombre, apellido, dni e email
