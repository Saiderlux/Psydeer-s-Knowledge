## Componentes
Entidades: representación se un objeto en la base de datos. 
Existen las entidades concretas y hacen referencias a un objeto físico.
Entidades abstractas: Hacen referencia a algo no físico.

- Atributos simples: Aquellos que no se pueden dividir en más partes, una estatura
- Atributo compuesto: Se puede dividir en componentes, por ejemplo una dirección; podemos tener calle, ciudad, país, etc.
- Atributos monovalorados: Identificador único de la tabla (clave primaria
- Atributos multivalorados: Pueden tener más de un valor asociado
- Atributos derivados: Los que se pueden calcular o derivar de otros atributos, por ejemplo la edad calculada con la fecha de nacimiento y la fecha actual.

### Cardinalidad
La **cardinalidad** en bases de datos se refiere a la cantidad de instancias de una entidad que pueden estar relacionadas con instancias de otra entidad. Es un concepto clave del modelo entidad-relación, que se utiliza para definir cómo se vinculan los datos en un sistema.

- **Uno a Uno (1:1):** Cada registro en la primera entidad se relaciona con, a lo sumo, un único registro en la segunda entidad y viceversa. Por ejemplo, un pasaporte que corresponde a un único ciudadano.
    
- **Uno a Muchos (1:N) o Muchos a Uno (N:1):** Un registro de la entidad “uno” puede estar relacionado con múltiples registros en la entidad “muchos”. Por ejemplo, un cliente (uno) puede tener varias órdenes (muchos), aunque cada orden pertenece a un solo cliente.
    
- **Muchos a Muchos (N:M):** Múltiples registros de una entidad pueden estar relacionados con múltiples registros de otra entidad. Por ejemplo, en una base de datos de estudiantes y cursos, un estudiante puede inscribirse en varios cursos y a la vez cada curso puede tener varios estudiantes inscritos. Normalmente, este tipo de relaciones se modela mediante una tabla intermedia (o de unión) para gestionar la complejidad.

