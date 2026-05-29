# git practica 2
Taller GIT. Práctica 2.
Guarda los comandos realizados, así como los resultados(capturas), integrarlo dentro del mismo repositorio

## Trabajar con un proyecto HTML y un repositorio local.
- Crea una carpeta practica-taller-git en tu pc.
- Inicializa el repositorio. 
 ![alt text](image.png)
- Crea el fichero index.html con un html simple.
- Comprueba que el repositorio a detectado el cambio. 
![alt text](image-1.png)
- Añade el fichero al stage. 
- Confirma los cambios. 
![alt text](image-2.png)
- Añade un fichero description.html y edita index.html.
- Comprueba que ha detectado el nuevo fichero y la modificación de index.
![alt text](image-3.png)
- Crea un fichero TODO.txt de tareas pendientes.
- Comprueba que git ha detectado el nuevo fichero. 
![alt text](image-4.png)
- Ignora el fichero TODO.txt ya que es donde anotaremos nuestras tareas personales y no debe formar parte del proyecto. Para ello crea un fichero .gitignore con la linea TODO.txt.
- Comprueba que ya no detecta el nuevo fichero TODO.txt (si que detectara el .gitignore claro). 
![alt text](image-5.png)
- Añade y confirma el .gitignore.
- Puedes continuar añadiendo ficheros html, css e imágenes para probar el repositorio.
![alt text](image-6.png)

## Haz un fork del repositorio creado para la práctica del taller:
- Entra en https://github.com/
- Accede a tu cuenta.
- Accede al repositorio del profesor https://github.com/lalobarri/git-practica-2.git
- Pulsa el botón fork (parte superior derecha) para crearte una copia del mismo en tu cuenta.
![alt text](image-7.png)
- Clona el repositorio en tu equipo *en otra carpeta diferente que la llamaremos 'git-practica-2'*. Quedará algo parecido a lo siguiente:
![alt text](image-8.png)
- Crea un nuevo fichero en el proyecto que se llame [tu-nombre-de-usuario].html
- Edita el fichero añadiendo como título tu nombre, algún texto y lo que desees en el.
- Añade el fichero al repositorio.

- Súbelo al repositorio remoto (github). 
![alt text](image-9.png)
- Crea una rama develop y cámbiate a ella.
![alt text](image-10.png)
- Realiza cambios en el proyecto, confírmalos y súbelos al repositorio remoto.
![alt text](image-11.png)
![alt text](image-12.png)
- Desde github crea un pull request de la rama develop a main.
- Fusiona la rama develop con en main. No deberías de tener ningún conflicto.
- Haz nuevos cambios en el proyecto siguiendo el flujo de trabajo git flow.
![alt text](image-13.png)
![alt text](image-14.png)
![alt text](image-15.png)

## Preguntas
Crea un nuevo fichero respuestas.md, contesta las siguientes preguntas y súbelo a tu repositorio remoto de github:

 1. ¿Qué sucede cuando hacemos un git add?
 2. ¿Qué sucede cuando hacemos un git commit? ¿Dónde está ese commit? 
 3. ¿Por qué al hacer git commit todavía no está disponible ese commit en el repositorio remoto?
 4. ¿Qué hay que hacer para que veamos este commit en nuestro repositorio remoto de github?
 5. ¿Qué diferencia hay entre hacer un fork o crear una nueva rama?
 6. ¿Qué comando se utiliza para crear una nueva rama sin cambiarte a ella?
 7. ¿Cuál es la diferencia entre los comandos git switch y git checkout al trabajar con ramas?
 8. ¿Qué es una rama por defecto (como main o master) y por qué es importante?
 9. ¿Qué comando te permite ver la lista de todas las ramas locales de tu repositorio?
 10. En el contexto de Git, explica con tus propias palabras qué es una rama (branch) y cuál es su beneficio principal al trabajar en un proyecto de software
 11. ¿Qué ha pasado con el contenido de la carpeta practica-taller-git? ¿Por qué no la podemos ver en nuestro repositorio remoto de github?


*Utilice un formato que permita distinguir entre sus preguntas y respuestas*
