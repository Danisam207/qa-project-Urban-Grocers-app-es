# qa-project-Urban-Grocers-app-es

Contenido

1.	Descripcion
2.	Lista de comprobación
3.	Archivos del proyecto

Descripción

El objetico es comprobar que la aplicación Urban Grocers crea kits de productos. Hacer pruebas positivas y negativas para el campo “name” es la parte medular de
dicho proyecto tomado en cuenta la lista de comprobación que se nos ha proporcionado enfocando nuestra atención en los resultados esperados.

Lista de comprobación

| No. |               Description                 |                         ER                                                                                 | 
|-----|-------------------------------------------|-------------------------------------------------------------------------------------------------------------|
|  1  |El número permitido de caracteres (1):kit_body = { "name": "a"}  |Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud | 
|  2  |El número permitido de caracteres (511): kit_body = { "name":"El valor de prueba para esta comprobación será inferior a"}| Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud|
|  3  |El número de caracteres es menor que la cantidad permitida (0): kit_body = { "name": "" }|Código de respuesta: 400|
|  4  |El número de caracteres es mayor que la cantidad permitida (512): kit_body = { "name":"El valor de prueba para esta comprobación será inferior a” }|Código de respuesta: 400|
|  5  |Se permiten caracteres especiales: kit_body = { "name": ""№%@"," }|Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud|
|  6  |Se permiten espacios: kit_body = { "name": " A Aaa " }|Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud|
|  7  |Se permiten números: kit_body = { "name": "123" }|Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud|
|  8  |El parámetro no se pasa en la solicitud: kit_body = { }|Código de respuesta: 400|
|  9  |Se ha pasado un tipo de parámetro diferente (número): kit_body = { "name": 123 }|Código de respuesta: 400|


Archivos del Proyecto

  •	configuration.py: Este archivo contiene el URL y las rutas de solicitud.

  •	data.py: Este archivo contiene los cuerpos necesarios para las solicitudes.

  •	sender_stand_request.py: Este archivo contiene todas las solicitudes para POST para crear una cuenta de usuario y crear un kit.

  •	create_kit_name_kit_test.py: Este archivo contiene todos los tests.

  •	README.md: Este archivo incluye una descripción del proyecto.

  •	.gitignore: Incluye los archivos que no se deben subir a los repositorios.

Recursos

Paquetes instalados

1.	Pytest
2.	Paqueterias en paytest

Documentación

•	API docs Urban Groucers “ https://cnt-c9838ccb-d8db-4325-b370-53a0ed2bebcb.containerhub.tripleten-services.com/docs/”

Instrucciones

o Ejecutar las pruebas a traves de Paycharm: hacuendo uso de la terminal escribir pytest create_kit_name_kit_test.py

o Ejecutar todas las pruebas a traves de la interfaz de Paycharm haciendo clic en el triangulo verde de la parte superior.

Nota: asegurarse que se este ejecutando el archivo correcto, de lo contrario se debe seleccionar "current file" antes de ejecutar la prueba.

o Algunas pruebas devolveran un resultado "failed" la cual es normal ya que es un resultado esperado en algunas pruebas.


