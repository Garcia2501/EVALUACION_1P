# Universidad [TECNICA DE AMBATO]  
## Facultad de [INGENIERIA ELECTRONICA E INDUSTRIAL]  
### Carrera de [SOFTWARE]  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Manolo Jose Garcia Amores
**Fecha:** 8 de abril del 2026

---

# Evaluación Práctica de Git y GitHub

## Instrucciones Generales

- Cada pregunta debe ser respondida directamente en este archivo **(README.md)** debajo del enunciado correspondiente. 
- Es importante que se coloque capturas de pantalla como evidencia de la parte práctica. Se recomienda crear una carpeta `images/` para almacenar las capturas de pantalla.
- Cada respuesta debe ir acompañada de uno o más **commits**, según se indique en cada pregunta.
- Cuando se indique, deberán realizarse acciones prácticas dentro del repositorio (como creación de archivos, ramas, resolución de conflictos, etc.).
- Cada pregunta debe estar **etiquetada con un tag**, únicamente en el commit final correspondiente, con el formato: `"Pregunta 1"`, `"Pregunta 2"`, etc.

---

## Pregunta 1 (1 punto)

**Explicar la diferencia entre los siguientes conceptos/comandos en Git y GitHub:**

- `git clone` Copia un repositorio remoto a un directorio local para trabajar en él.  
- `fork`  Crea una copia de un repositorio en tu propia cuenta de GitHub (nivel servidor).
- `git pull` Actualiza tu repositorio local con los últimos cambios del servidor remoto.

### Parte práctica:

- Realizar un **fork** de este repositorio en la cuenta personal de GitHub del estudiante.
- Luego, realizar un **clone** del fork en el equipo local.
- En este README, describir el proceso seguido:
  - ¿Cómo se realizó el fork?
  - ¿Cómo se realizó el clone del fork?
  - ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?
- Realizar en la rama `main` todo lo que corresponde a esta pregunta.

**📝 Respuesta:**

- `git clone` Copia un repositorio remoto a un directorio local para trabajar en él.   
- `fork`  Crea una copia de un repositorio en tu propia cuenta de GitHub (nivel servidor).
- `git pull` Actualiza tu repositorio local con los últimos cambios del servidor remoto.



**Respuesta:**

* **¿Cómo se realizó el fork?**
  Se accedió al repositorio original de `santiagojara/EVALUACION_1P` en GitHub y se presionó el botón "Fork" ubicado en la esquina superior derecha, seleccionando mi cuenta personal `Garcia2501` como destino para crear la copia independiente.

  Aquí presento la evidencia de la configuración de mis repositorios remotos, lo cual demuestra que realicé el **fork** correctamente a mi cuenta personal y que estoy trabajando sobre ese clone.

![Verificación de Remotos](images/evidencia_fork.png)

* **¿Cómo se realizó el clone del fork?**
  Una vez creado el fork en mi perfil, copié la URL de mi repositorio (`https://github.com/Garcia2501/EVALUACION_1P.git`) y en la Git Bash utilicé el comando `git clone` seguido de dicha URL para descargar los archivos localmente en mi WorkSpace.

* **¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original?**
  Se utilizó el comando `git remote -v` en la terminal. La salida confirmó que el remoto denominado `origin` apunta a mi usuario (`Garcia2501`) y no al repositorio del docente, asegurando que tengo permisos de escritura sobre este repositorio.

![Evidencia de Configuración](images/evidencia_fork.png)

También se ha creado la estructura de carpetas requerida por el examen.

![Estructura del Proyecto](images/estructura.png)


---

## Pregunta 2 (1 punto)

**Configurar un archivo `.gitignore` para que ignore:**

- Todos los archivos con extensión `.log`.
- Una carpeta llamada `temp/`.
- Todos los archivos `.md` y `.txt`de la carpeta `doc/`. (Probar agregando un archivo `prueba.md` y un archivo `prueba.txt` dentro de la carpeta y fuera de la carpeta.)

### Requisitos:

1. Realizar un **primer commit** que incluya únicamente el archivo `.gitignore` con las reglas de exclusión definidas.
2. Realizar un **segundo commit** que incluya las creación de los archivos de prueba.
2. Realizar un **tercer commit** donde se explique en este README la función del archivo `.gitignore` y se muestre evidencia de que los archivos y carpetas indicadas no están siendo rastreadas por Git.

**Importante:**  
- Solo el **tercer commit** debe llevar el **tag `"Pregunta 2"`**.

**📝 Respuesta:**

**Respuesta:**

El archivo `.gitignore` es una herramienta esencial en Git que permite filtrar qué archivos o directorios no deben ser rastreados ni subidos al repositorio remoto. Esto ayuda a mantener el proyecto limpio de archivos temporales, configuraciones locales o logs de errores.

#### 1. Configuración inicial
Se creó el archivo `.gitignore` en la raíz del proyecto con las siguientes reglas:
- `*.log`: Ignora todos los archivos con extensión de registro.
- `temp/`: Excluye la carpeta completa de archivos temporales.
- `doc/*.md` y `doc/*.txt`: Filtra archivos de texto y markdown específicamente dentro de la carpeta doc.

![Configuración de Gitignore](images/evidencia_p2_config.png) 
![Contenido del Gitignore](images/evidencia2_p2_config.png)

#### 2. Validación de exclusiones
Para probar las reglas, se crearon archivos que coinciden con los patrones (como `error.log` y carpetas `temp/`). Al ejecutar `git status`, se verificó que Git ignora estos elementos y solo detecta aquellos permitidos, como `archivo_valido.txt`.
Con esto se demuetsra la validacion del archivo .gitignore

![Prueba de archivos ignorados](images/evidencia_p2_creacionarchivos.png)(
  ![Resultado del Git status](images/evidencia_p2_status.png)

---

## Pregunta 3 (2 puntos)

**Utilizar Git Flow para desarrollar una nueva funcionalidad llamada `ingresar-encabezado`.**

### Requisitos:

- Inicializar el repositorio con Git Flow, utilizando las ramas por defecto: `main` y `develop`.
- Crear una rama de tipo `feature` con el nombre `ingresar-encabezado`.
- En dicha rama, **completar con los datos personales del estudiante** el encabezado que ya se encuentra al inicio de este archivo `README.md`.
- Realizar al menos un commit durante el desarrollo.
- Finalizar el hotfix siguiendo el flujo de trabajo establecido por Git Flow.

### En la sección de respuesta, se debe incluir:

- Los **comandos exactos** utilizados desde la inicialización de Git Flow hasta el cierre de la rama.
- Una descripción del **proceso seguido**, indicando el propósito de cada paso.
- Una reflexión sobre las **ventajas de aplicar Git Flow**, especialmente en contextos colaborativos o proyectos de larga duración.

**Importante:**

- Deben realizarse varios commits durante esta pregunta.
- **Solo el commit final** debe llevar el **tag `"Pregunta 3"`**.
- El flujo debe respetar la estructura de Git Flow con las ramas `develop` y `main`.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 3 -->

---

## Pregunta 4 (2 puntos)

**Trabajo con Issues y Pull Requests**

### Parte teórica:

- ¿Qué es un Pull Request y cuál es su función dentro de un flujo de trabajo colaborativo con Git y GitHub?
- ¿Por qué es importante revisar un Pull Request antes de fusionarlo con la rama principal?
- ¿Qué tipo de observaciones o validaciones se suelen realizar durante la revisión de un Pull Request?

### Parte práctica:

- Trabajar en la rama `develop`, ya existente desde la configuración de Git Flow.
- Realizar los cambios necesarios en este archivo `README.md` para responder las preguntas.
- Realizar un **commit** con los cambios de la primera pregunta y subirlo a la rama `develop` del repositorio remoto.
- Crear un **pull request** desde `develop` hacia `main` en GitHub, con el nombre `"Pregunta 4 - Apellido Nombre"`.
- Crear comentarios solicitando: 1. que se agregue la respuesta de la segunda pregunta y luego agregando la respuesta con el respectivo commit; y 2. el mismo procedimiento para la tercera pregunta.
- **Aprobar** el pull request para que se haga el merge respectivo hacia `main`.

### En la sección de respuesta, se debe incluir:

- Un resumen del procedimiento realizado con las respectivas preguntas y capturas.
- El número y enlace al pull request.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 4 -->

---

## Pregunta 5 (2 puntos)

**Resolver conflictos entre ramas y realizar un Pull Request**

### Requisitos:

- Crear dos ramas llamadas `ramaA` y `ramaB`, ambas a partir de la rama `develop`.
- En `ramaA`, crear un archivo llamado `archivoA.txt` con el contenido:  
  `Contenido A`
- En `ramaB`, crear un archivo con el mismo nombre (`archivoA.txt`), pero con el contenido:  
  `Contenido B`
- Intentar fusionar `ramaB` sobre `ramaA`, lo cual debe generar un conflicto.
- Resolver el conflicto combinando ambos contenidos.
- Realizar el merge de `ramaA` hacia `develop`.
- Crear un **pull request** desde `develop` hacia `main`.
- Una vez completado lo anterior, eliminar las ramas `ramaA` y `ramaB`.

### En la sección de respuesta, se debe incluir:

- El procedimiento completo:
  - Cómo se crearon las ramas.
  - Cómo se generó y resolvió el conflicto.
  - Cómo se realizó el merge hacia `develop`.
  - Cómo se eliminaron las ramas al finalizar.
- El enlace al pull request.
- Una breve explicación de qué es un conflicto en Git y por qué ocurrió en este caso.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 5 -->

---

## Pregunta 6 (2 puntos)

**Realizar limpieza, explicar versionamiento semántico y enviar cambios al repositorio original**

### Requisitos:

- Trabajar en la rama `develop` del fork del repositorio.
- Eliminar los archivos `archivoA.txt` y `archivoB.txt` creados en preguntas anteriores.
- Realizar un merge desde `develop` hacia `main` en el repositorio local.
- Enviar los cambios de la rama `main` local a la rama `develop` del repositorio remoto (fork). Recuerde incluir todos los tags creados (6 tags).
- Finalmente, crear un **pull request** desde la rama `develop` del fork hacia la rama `main` del repositorio original (del cual se realizó el fork en la Pregunta 1). El titulo del pull request debe ser `"NOMBRE APELLIDOS"`, en la descripción colocar el link de su repositorio de GitHub.

### En la sección de respuesta, se debe incluir:

- Una explicación del proceso realizado paso a paso.
- Una explicación del **versionamiento semántico**, indicando:
  - En qué consiste.
  - Sus tres componentes (MAJOR, MINOR, PATCH).
- Si hace falta agregar alguna evidencia adicional, agregue un tag adicional que sea `Version Final`.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 6 -->
