### 🧠 ¿Por qué es importante?

Imagina que tienes una tabla con los datos de estudiantes y cursos, y cada vez que un estudiante se inscribe en un nuevo curso, tienes que volver a escribir su nombre, su dirección, etc. Esto no solo **duplica datos**, sino que hace más probable que **cometas errores**. Si cambias la dirección en un lugar pero no en otro, ya tienes una inconsistencia. ¡Y eso es un gran problema!

#### ✅ **Primera Forma Normal (1FN)**:

- Cada columna debe contener **valores atómicos**, es decir, indivisibles.
    
- No debe haber **repeticiones** ni **listas de valores** en una sola celda.
    

**Ejemplo malo (no normalizado):**

|Estudiante|Cursos|
|---|---|
|Ana|Matemáticas, Bio|
|Juan|Química|

→ Aquí la columna "Cursos" contiene **más de un valor**.

**Ejemplo en 1FN:**

|Estudiante|Curso|
|---|---|
|Ana|Matemáticas|
|Ana|Biología|
|Juan|Química|

---

#### ✅ **Segunda Forma Normal (2FN)**:

- Debe cumplir **1FN**.
    
- Y además, **todas las columnas no clave** deben depender **completamente de la clave primaria** (no solo de una parte de ella si es compuesta).
    

→ Aquí se eliminan **dependencias parciales**.

---

#### ✅ **Tercera Forma Normal (3FN)**:

- Cumple **2FN**.
    
- No debe haber **dependencias transitivas**, es decir, columnas que dependen de **otras columnas no clave** en lugar de la clave primaria.