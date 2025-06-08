Sistema que permite almacenar y registrar información.
## Tipos
- Relacionales (RBDMS)
- No relacionales (Bases de datos NoSQL)
### Base de datos relacional
A nivel de estructura está compuesta por tablas que tienen filas y columnas, las cuales representan atributos.

**Esquema rígido**
La estructura de las tablas debe definirse de antema y es rígido. los datos deben ajustarse a este esquema
**Relaciones**
Relaciones primarias y relaciones foráneas.

**Integridad**
Garantizan la consistencia y la integridad de los datos

Normalmente se utilizan en aplicaciones con datos bien estructurados y relaciones complejas, como sistemas financieros, ERP y gestión de inventarios

[[[Motor de Bases de datos]]]
- MySQL
- PostgreSQL
- Oracle
- Microsoft SQL server
- SQLite
## Bases de datos no relacionales
Se almacenan los datos en grafos, archivos JSon.

No necesariamente tienen relaciones explicitas entre las entidades.

Se escalan de manera horizontal

Son más adecuados para guardar datos no estructurados y pueden manejar grandes volúmenes de datos.

Aplicaciones con datos no estructurados o de rápido crecimiento como aplicaciones web, redes sociales, big data y sistemas de recomendación.

[[Motor de Bases de datos]]
- MongoDB
- Cassandra 
- Redis
- DynamoDB