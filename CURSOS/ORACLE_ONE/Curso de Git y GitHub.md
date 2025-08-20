## ¿Qué es Git y GitHub?

- **Git**: Es un sistema de control de versiones distribuido. Sirve para llevar un registro de los cambios en tus archivos y proyectos a lo largo de la historia.
    
- **GitHub**: Es una plataforma de almacenamiento de código y una red social para desarrolladores. Utiliza Git para sus operaciones y permite alojar proyectos, colaborar con otros y gestionar el código de forma remota.
    

---

## Comandos básicos de Git

### Configuración inicial

- `git config --global user.name "Tu Nombre"`: Configura tu nombre de usuario para Git.
    
- `git config --global user.email "tu_email@ejemplo.com"`: Configura tu correo electrónico.
    

### Creación y clonación de repositorios

- `git init`: Inicializa un nuevo repositorio de Git en la carpeta actual.
    
- `git clone https://aws.amazon.com/es/what-is/repo/`: Clona (descarga) un repositorio existente de una plataforma como GitHub.
    

### Seguimiento de cambios

- `git status`: Muestra el estado de los archivos y los cambios que se han realizado.
    
- `git add [nombre del archivo]`: Prepara un archivo para el próximo commit. También se puede usar `git add .` para añadir todos los archivos modificados.
    
- `git commit -m "[mensaje]"` : Guarda los cambios que has añadido con `git add`. El mensaje (`-m`) describe los cambios realizados.
    

### Historial y diferencias

- `git diff`: Muestra las diferencias entre la versión actual y la última versión guardada.
    
- `git log`: Muestra el historial completo de los commits.
    

---

## Gestión de ramas (Branches)

Una rama es una línea de desarrollo independiente. Hacer todo en una sola rama (`main`) puede causar errores, por lo que es mejor trabajar en ramas separadas.

- `git branch`: Muestra las ramas que existen en tu repositorio.
    
- `git branch [nombre de la rama]`: Crea una nueva rama.
    
- `git switch [nombre de la rama]`: Te permite cambiar a una rama existente. Es la forma moderna y recomendada.
    
- `git checkout -b [nombre de la rama]`: Es el comando antiguo para crear y cambiar a una nueva rama simultáneamente.
    

---

## Fusión de ramas (Merge)

`Merge` es el proceso de mezclar los cambios de una rama en otra.

1. **Posicionarse en la rama principal:**
    
    Bash
    
```bash
git switch main
```
    
2. **Mezclar la otra rama:**
    
```bash
git merge [nombre de la otra rama]
 ```
    
- Git intentará fusionar los cambios. Si hay conflictos, deberás resolverlos manualmente en los archivos afectados.
        

---

## Colaboración y sincronización

- `git push origin [nombre de la rama]`: Sube los cambios de tu rama local al repositorio remoto en GitHub. Si mezclas la rama principal, deberás subir los cambios de `main`.
    
- `git pull`: Descarga y fusiona los cambios de la rama remota a tu rama local. Es el comando opuesto a `git push`.
    
- `git restore [nombre del archivo]`: Deshace los cambios locales en un archivo. También puede usarse para volver a un commit anterior.