# NORMALIZACIÓN DE BASE DE DATOS RELACIONALES.

Este concepto nos enfoca a las reglas que toda base de datos de tipo relacional debería seguir para ser lo más estructurada y organizada posible.

Una base de datos debe ser eficiente y en lo posible evitar la redundancia, siguiendo una serie de reglas denominadas **formas normales**.

## 1. Primera forma normal.
### ATOMICIDAD Y NO REDUNDANCIA.
Los valores almacenados en cada columna de la BD deben ser concretos y no deben ser divisibles, ejemplo:

__FORMA CORRECTA__ 
    
    | nombre  | apellidoP | apellidoM |
    | --------| --------  | --------  |
    | enoc    |  soto     | arenilla  |

__FORMA INCORRECTA__

    | nombres       | apellidos        | 
    | ------------  | ---------------  | 
    | enoc de jesus |  soto  Arenilla  |


**No Redundancia**: Los datos deben ser datos completos **NO** deben existir arreglos y/o datos divididos en una base de datos.
**EJEMPLO**
__FORMA CORRECTA__

    | Generos  |
    | -------- |
    | Drama    |
    | Aventura | 
    | Animacion| 

__FORMA INCORRECTA__

    | Genero 1  | Genero 2 | Genero 3 |
    | ------   | ------   | ------   |
    | Animacion | Drama    | Aventura |
  

 Para evitar lo anterior se deben agrupar valores en tablas individuales, las cuales deben estar relacionadas entre cada una.
 

 **Atomicidad de la información**: Se debe asegurar que toda transacción realizada se complete satisfactoriamente o se realice un rollback. 

 **transaccion**: En base de datos es un conjunto de operaciones que deben ser o ejecutarse todas correctamente de lo contrario un solo error encontrado debería revertir todas las operaciones para mantener la integridad lógica de los datos.

- Campo unico PK toda tabla existente debe tener una llave primaria que garantice la nonrepiticion de este campo en ninguna otra tabla de la base de datos, (el PK puede ser conformado por varias columnas).


