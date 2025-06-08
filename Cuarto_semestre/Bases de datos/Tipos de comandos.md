## DQL
Lenguaje de consulta de datos
```MySQL
SELECT nombre, edad FROM estudiantes`
WHERE edad > 8
```

## DDL 
Lenguaje de definición de datos
```MySQL
CREATE TABLE estudiantes (id INT, nombre VARCHAR(50), edad INT);

ALTER TABLE estudiantes ADD columna_grado VARCHAR(10);

DROP TABLE estudiantes;
```

## DML
Leguaje de manipulación de los datos
```MySQL
INSERT INTO estudiantes (id, nombre, edad) VALUES (1, 'Juan', 20)

UPDATE estudiantes SET edad = 21 WHERE id = 1;

DETELE FROM estudiantes WHere id =1;
```

## DCL
Lenguaje de control de datos

Nos permite dar permisos a los diferentes usuarios que manejen la base de datos.

```MySQL
GRANT SELECT ON estudiantes TO usuario1

REVOKE SELECT ON estudiantes FROM usuario1
```

## TCL
Lenguaje de control de transacciones
```MySQL
COMMIT;
ROLLBACK;
SAVEPOINT puntoA;
```
