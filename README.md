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
|  1  |El número permitido de caracteres (1):kit_body = { "name": "a"}  |Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con       
                                                                         el campo "name" del cuerpo de la solicitud                                            | 
|  2  |El número permitido de caracteres (511):   |Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el   |
|     |kit_body = { "name":"El valor de prueba    |campo "name" del cuerpo de la solicitud                                               |
|     |para esta comprobación será inferior a"}   |                                                                                      |                     
|  3  |El número de caracteres es menor que la    |Código de respuesta: 400                                                              |
|     |cantidad permitida (0):                    |                                                                                      |
|     | kit_body = { "name": "" }                 |                                                                                      |
|  4  |El número de caracteres es mayor que la    |Código de respuesta: 400                                                              | 
|     |cantidad permitida (512):                  |                                                                                      |  
|     |kit_body = { "name":"El valor de prueba    |                                                                                      |
|     |para esta comprobación será inferior a” }  |                                                                                      |
|  5  |Se permiten caracteres especiales:         |Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el   | 
|     |kit_body = { "name": ""№%@"," }            |campo "name" del cuerpo de la solicitud                                               |
|  6  |Se permiten espacios:                      |Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el   | 
|     |kit_body = { "name": " A Aaa " }           |campo "name" del cuerpo de la solicitud                                               |
|  7  |Se permiten números:                       | Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el  |
|     |kit_body = { "name": "123" }               |campo "name" del cuerpo de la solicitud                                               |
|  8  |El parámetro no se pasa en la solicitud:   |Código de respuesta: 400                                                              |
|     |kit_body = { }                             |                                                                                      |
|  9  |Se ha pasado un tipo de parámetro diferente|Código de respuesta: 400                                                              |
|     |(número): kit_body = { "name": 123 }       |                                                                                      |
              
