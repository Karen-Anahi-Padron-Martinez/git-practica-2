# 📘 Preguntas y Respuestas sobre Git

---

## Pregunta 1
**¿Qué sucede cuando hacemos un `git add`?**

## Respuesta
Cuando ejecutamos `git add`, estamos moviendo los cambios del **directorio de trabajo** al **área de preparación (staging area)**. Esto le indica a Git qué archivos o cambios queremos incluir en el próximo commit. Los archivos quedan "listos para ser confirmados", pero aún no se ha guardado ningún commit.

---

## Pregunta 2
**¿Qué sucede cuando hacemos un `git commit`? ¿Dónde está ese commit?**

## Respuesta
Al ejecutar `git commit`, Git toma todos los cambios que estaban en el área de staging y crea una **instantánea permanente** del estado del proyecto, guardándola en el **repositorio local** (la carpeta `.git`). Ese commit solo existe en nuestra máquina, identificado por un hash único (SHA-1). No ha salido aún de nuestro equipo.

---

## Pregunta 3
**¿Por qué al hacer `git commit` todavía no está disponible ese commit en el repositorio remoto?**

## Respuesta
Porque `git commit` únicamente guarda los cambios en el **repositorio local**. Git es un sistema de control de versiones distribuido: cada desarrollador tiene su propia copia completa del repositorio. Para que los cambios lleguen al servidor remoto (por ejemplo, GitHub), es necesario realizar un paso adicional de sincronización explícita.

---

## Pregunta 4
**¿Qué hay que hacer para que veamos este commit en nuestro repositorio remoto de GitHub?**

## Respuesta
Hay que ejecutar el comando:

```bash
git push origin <nombre-de-la-rama>
```

Este comando **sube (empuja)** los commits locales al repositorio remoto. Por ejemplo, `git push origin main` envía los cambios de la rama `main` local al repositorio en GitHub, haciéndolos visibles para todos.

---

## Pregunta 5
**¿Qué diferencia hay entre hacer un fork o crear una nueva rama?**

## Respuesta

| Concepto | Fork | Nueva Rama |
|----------|------|------------|
| **Qué es** | Copia completa del repositorio en tu cuenta de GitHub | Una línea de desarrollo paralela dentro del mismo repositorio |
| **Dónde se crea** | En GitHub, como un repositorio independiente | En el repositorio actual (local o remoto) |
| **Uso típico** | Contribuir a proyectos ajenos sin tener permisos | Desarrollar funcionalidades o correcciones dentro del mismo proyecto |
| **Relación con el original** | Independiente; se sincroniza manualmente | Comparte el historial con el resto de ramas del repositorio |

En resumen: un **fork** es una copia de un repositorio externo; una **rama** es una bifurcación dentro de un mismo repositorio.

---

## Pregunta 6
**¿Qué comando se utiliza para crear una nueva rama sin cambiarte a ella?**

## Respuesta

```bash
git branch <nombre-de-la-rama>
```

Este comando crea la rama pero te mantiene en la rama actual. Si quisieras crearla y moverte a ella al mismo tiempo, usarías `git switch -c <nombre>` o `git checkout -b <nombre>`.

---

## Pregunta 7
**¿Cuál es la diferencia entre los comandos `git switch` y `git checkout` al trabajar con ramas?**

## Respuesta

- **`git checkout`** es un comando más antiguo y **multipropósito**: sirve para cambiar de rama, restaurar archivos, moverse a commits concretos, etc. Su amplitud lo hace algo confuso.
- **`git switch`** fue introducido en Git 2.23 con un propósito **más específico y claro**: únicamente para cambiar entre ramas o crear y cambiar a una nueva rama (`git switch -c <nombre>`).

Para trabajar con ramas, `git switch` es la opción moderna y recomendada por ser más intuitiva y menos propensa a errores.

---

## Pregunta 8
**¿Qué es una rama por defecto (como `main` o `master`) y por qué es importante?**

## Respuesta
La rama por defecto es la **rama principal del repositorio**, creada automáticamente al inicializarlo. Históricamente se llamaba `master`; actualmente GitHub usa `main` por defecto. Es importante porque:

- Representa el **estado estable y oficial** del proyecto.
- Es el punto de partida para crear otras ramas de trabajo.
- Suele ser la rama que se despliega en producción.
- Todas las demás ramas, al completarse, típicamente se fusionan aquí mediante Pull Requests.

---

## Pregunta 9
**¿Qué comando te permite ver la lista de todas las ramas locales de tu repositorio?**

## Respuesta

```bash
git branch
```

La rama activa aparece marcada con un asterisco (`*`). Para ver también las ramas remotas, se usa `git branch -a`; y solo las remotas con `git branch -r`.

---

## Pregunta 10
**En el contexto de Git, explica con tus propias palabras qué es una rama (branch) y cuál es su beneficio principal al trabajar en un proyecto de software.**

## Respuesta
Una **rama** es como una copia paralela del proyecto donde puedes trabajar de forma independiente sin afectar al código principal. Imagina que el proyecto es una línea del tiempo: una rama es una bifurcación donde puedes hacer cambios, probar ideas o corregir errores, y luego decidir si esos cambios se integran de vuelta o se descartan.

Su **beneficio principal** es el **aislamiento**: varios desarrolladores pueden trabajar simultáneamente en diferentes funcionalidades sin pisarse el trabajo, y el código principal (por ejemplo, `main`) permanece estable hasta que los cambios sean revisados y aprobados.

---

## Pregunta 11
**¿Qué ha pasado con el contenido de la carpeta `practica-taller-git`? ¿Por qué no la podemos ver en nuestro repositorio remoto de GitHub?**

## Respuesta
Lo más probable es que alguna de las siguientes situaciones haya ocurrido:

1. **No se hizo `git add`**: los archivos de la carpeta nunca fueron añadidos al área de staging, por lo que Git no los rastrea.
2. **No se hizo `git commit`**: los cambios se añadieron al staging pero nunca se confirmaron en el repositorio local.
3. **No se hizo `git push`**: los commits existen localmente pero nunca se subieron al repositorio remoto.
4. **La carpeta está en `.gitignore`**: Git está configurado para ignorar esa carpeta expresamente.
5. **La carpeta es un submódulo sin inicializar**: si contiene su propio `.git`, Git la trata como un submódulo y no sube su contenido automáticamente.

En cualquier caso, para que el contenido sea visible en GitHub es necesario haber completado los tres pasos: `git add` → `git commit` → `git push`.

---

