# my-proyecto-millonario

## Trabajo diario a través de git

## Indice

- [Commit inicial](#commitinicial)
- [Push inicial](#pushinicial)
- [Ignorar archivos](#ignorararchivos)
- [Añadir fichero 1.txt](#añadirfichero)
- [Crear el tag v0.1](#creartag)
- [Subir el tag v0.1](#subirtag)
- [Crear una rama v0.2](#crearrama)
- [Añadir fichero 2.txt](#añadirfichero)
- [Crear rama remota v0.2](#crearramaremota)
- [Merge directo](#mergedirecto)
- [Merge con conflicto](#mergeconflicto)
-  [Ignorar archivos](#ignorararchivos)
- [Añadir fichero 1.txt](#añadirfichero)
- [Crear el tag v0.1](#creartag)
- [Subir el tag v0.1](#subirtag)
- [Crear una rama v0.2](#crearrama)
- [Añadir fichero 2.txt](#añadirfichero)
- [Crear rama remota v0.2](#crearramaremota)

Clonamos el repositorio que acabamos de crear con el siguiente comando:

```code
  git clone https://github.com/eduglezexp/my-proyecto-millonario.git
```
- salida:

```code
  Clonando en 'my-proyecto-millonario'...
  remote: Enumerating objects: 3, done.
  remote: Counting objects: 100% (3/3), done.
  remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
  Recibiendo objetos: 100% (3/3), listo.
```

>Nota: Para entrar al directorio, usamos el comando __cd my-proyecto-millonario__

- salida:

```code 
  eduglezexp@eduglezexp-VirtualBox:~/my-proyecto-millonario$ 
```

>Nota: __ls -la__, con este comando muestro el contenido del directorio

- salida:

```code
  total 16
  drwxrwxr-x  3 eduglezexp eduglezexp 4096 oct 10 15:39 .
  drwxr-x--- 26 eduglezexp eduglezexp 4096 oct 10 15:39 ..
  drwxrwxr-x  8 eduglezexp eduglezexp 4096 oct 10 15:39 .git
  -rw-rw-r--  1 eduglezexp eduglezexp   24 oct 10 15:39 README.md
```

## Commit inicial <a name="commitinicial"></a>

- Añadir al README.md los comanddos utilizados hasta ahora y hacer un coomit inicial con el mensaje commit inicial.
  Para ello, usaremos los siguientes comandos:

```code
  git add .
  git commit -m "commit inicial"
```

- Para añadir lo hecho:

```code
  git add .
```
- salida:

```code
  Aunque no nos muestre nada en la terminal, se ha añadido lo hecho.
```

- Para comentarlo, usamos:

```code
  git commit -m "commit inicial"
```
- salida:

```code
  [main 4c71bb8] commit inicial
  1 file changed, 73 insertions(+), 1 deletion(-)
  rewrite README.md (100%)
```

## Push inicial <a name="pushinicial"></a>

- Subir los cambios al repositorio remoto.

```code
  git push origin master
```
>Pregunta: Si has clonado el repostorio es necesirio que parte del comando anterior puedo omitir.Justifica tu respuesta en el fichero README.md.

-

```code
  git push origin 
```

- salida:

```code
  Username for 'https://github.com': eduglezexp
  Password for 'https://eduglezexp@github.com': 
  Enumerando objetos: 5, listo.
  Contando objetos: 100% (5/5), listo.
  Compresión delta usando hasta 3 hilos
  Comprimiendo objetos: 100% (2/2), listo.
  Escribiendo objetos: 100% (3/3), 918 bytes | 918.00 KiB/s, listo.
  Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
  To https://github.com/eduglezexp/my-proyecto-millonario.git
  2bfe884..4c71bb8  main -> main
```

## Ignorar archivos <a name="ignorararchivos"></a>

- Crear en el repositorio local un fichero llamado privado.txt.

```code
  touch privado.txt
```

- salida:

```code
  Aunque no lo muestre la terminal, se ha creado un fichero en el repositorio local.
```

- Para crear en el repositorio local una carpeta llamada privada, usaremos el siguiente comando:

```code
  mkdir privada
```

- salida:

```code
  Aunque no lo muestre la terminal, se ha creado la carpeta en el repositorio local.
```

- Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git.

## Operaciones a realizar:

```code
  echo "privado.txt" >> .gitignore
  echo "/privada" >> .gitignore
  git add .
  git commit -m "añadido fichero .gitignore"
```
- salida:

```code
  eduglezexp@eduglezexp-VirtualBox:~/my-proyecto-millonario$ echo "privado.txt" >> .gitignore
  eduglezexp@eduglezexp-VirtualBox:~/my-proyecto-millonario$ echo "/privada" >> .gitignore
  eduglezexp@eduglezexp-VirtualBox:~/my-proyecto-millonario$ git add .
  eduglezexp@eduglezexp-VirtualBox:~/my-proyecto-millonario$ git commit -m "añadido fichero .gitignore"
  [main 4ec4bf8] añadido fichero .gitignore
  7 files changed, 115 insertions(+), 3 deletions(-)
  create mode 100644 .gitignore
  create mode 100644 .idea/.gitignore
  create mode 100644 .idea/misc.xml
  create mode 100644 .idea/modules.xml
  create mode 100644 .idea/my-proyecto-millonario.iml
  create mode 100644 .idea/vcs.xml
```

>Pregunta: el fichero y el directorio privado debe de subir al repositorio si se encuentra añadido al fichero .gitingnore. [Si/No]. Justifica tu respuesta en el fichero README.md.

-

## Añadir fichero 1.txt <a name="añadirfichero"></a>

- Añadir fichero 1.txt al repositorio local.

```code
  touch 1.txt
  git add .
  git commit -m "añadido 1.txt"
```

- salida:

```code
  [main ea185a2] añadido 1.txt
  2 files changed, 40 insertions(+), 2 deletions(-)
  create mode 100644 1.txt
```

>Pregunta: Si ejecutado las acciones add y commit, que realiza cada una sobre el/los ficheros. Justifica tu respuesta en el fichero README.md.

-

## Crear el tag v0.1 <a name="creartag"></a>

- Para crear un tag v0.1, usaremos el siguiente comando

```code
  git tag v0.1
```

- salida:

```code
  Aunque no se muestre en la terminal, se ha creado el tag v0.1 
```

## Subir el tag v0.1 <a name="subirtag"></a>

- Subir los cambios al repositorio remoto.

```code
  git push --tag origin master
```

- salida:

```code
  Total 0 (delta 0), reusados 0 (delta 0), pack-reusados 0
  To https://github.com/eduglezexp/my-proyecto-millonario.git
  * [new tag]         v0.1 -> v0.1
```

>Pregunta: ¿Qué es un tag sobre un repositorio git, en nuestro caso Github?. Justifica tu respuesta en el fichero README.md.

-

# Crear una rama v0.2 <a name="crearrama"></a>

- Crear una rama v0.2.

```code
  git branch v0.2
```

- salida:

```code

```

- Posiciona tu carpeta de trabajo en esta rama.

```code
  git checkout v0.2
```

- salida:

```code
  Cambiado a rama 'v0.2'
```

# Añadir fichero 2.txt <a name="añadirfichero"></a>

- Añadir un fichero 2.txt en la rama v0.2.

```code
  touch 2.txt
  git add .
  `git commit -m "añadido 2.txt"`
```

- salida:

```code
  [v0.2 b7f8785] añadido 2.txt
  2 files changed, 87 insertions(+), 6 deletions(-)
  create mode 100644 2.txt
```

>Pregunta: Cuando estamos trabajando con ramas, cual es su fin, y sentido en organizaciones pequeñas/medianas/grandes. Justifica tu respuesta en el fichero README.md.

# Crear rama remota v0.2 <a name="crearramaremota"></a>

- Subir los cambios al repositorio remoto.

```code
  git push origin v0.2
```

- salida:

```code 
  Username for 'https://github.com': eduglezexp
  Password for 'https://eduglezexp@github.com': 
  Enumerando objetos: 19, listo.
  Contando objetos: 100% (19/19), listo.
  Compresión delta usando hasta 3 hilos
  Comprimiendo objetos: 100% (14/14), listo.
  Escribiendo objetos: 100% (17/17), 3.67 KiB | 3.67 MiB/s, listo.
  Total 17 (delta 3), reusados 0 (delta 0), pack-reusados 0
  remote: Resolving deltas: 100% (3/3), done.
  remote: 
  remote: Create a pull request for 'v0.2' on GitHub by visiting:
  remote:      https://github.com/eduglezexp/my-proyecto-millonario/pull/new/v0.2
  remote: 
  To https://github.com/eduglezexp/my-proyecto-millonario.git
  * [new branch]      v0.2 -> v0.2
```

# Merge directo <a name="mergedirecto"></a>

- Posicionarse en la rama master/main según sea tu rama principal.

```code
  git checkout master
```

- salida:

```code
  Tu rama está adelantada a 'origin/main' por 2 commits.
  (usa "git push" para publicar tus commits locales)
```

- Hacer un merge de la rama v0.2 en la rama master/main.

```code 
  git merge v0.2 -m "merge v0.2 sin conflictos"
```

- ssalida:

```code
  Actualizando ea185a2..5b37d2e
  error: Los cambios locales de los siguientes archivos serán sobrescritos al fusionar:
	  README.md
  Por favor, confirma tus cambios o aguárdalos antes de fusionar.
  Abortando
```

>Pregunta: Se tendrían que producir conflictos en esta acción. [Si/No] Justifica tu respuesta en el fichero README.md.

# Merge con conflicto <a name="mergeconflicto"></a>

- En la rama maste/main poner Hola en el fichero 1.txt y hacer commit.

## Operaciones a realizar

```code
  git checkout master
  echo "Hola" >> 1.txt
  git add .
  git commit -m "hola en 1.txt"
```

- Cambiamos a la rama main:

```code
  git checkout master
```

- salida:

```code
  Ya en 'main'
  Tu rama está adelantada a 'origin/main' por 2 commits.
  (usa "git push" para publicar tus commits locales)
```

- Hacemos un commit con el mensaje: "hola en 1.txt"

```code
  git commit -m "hola en 1.txt"
```

- salida:

```code
  [main cbfb7ad] hola en 1.txt
  2 files changed, 193 insertions(+), 7 deletions(-)
```

- Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.

## Operaciones a realizar

```code
  git checkout v0.2
  echo "Adios" >> 1.txt
  git add .
  git commit -m "adios en 1.txt"
```

- Cambiamos a la rama v0.2:

```code
  git checkout v0.2
```

- salida:

```code
  Cambiado a rama 'v0.2'
```

- Hacemos un commit con el mensaje: "adios en 1.txt"

```code
  [v0.2 41c2cc9] adios en 1.txt
  2 files changed, 97 insertions(+), 2 deletions(-)
```

- Posicionarse de nuevo en la rama master/main y hacer un merge con la rama v0.2

```code
  git checkout master
  git merge v0.2
  vim 1.txt
  git add .
  git commit -m "arreglado merge en 1.txt"
```

- Cambiamos a la rama main:

```code
  Cambiado a rama 'main'
  Tu rama está adelantada a 'origin/main' por 4 commits.
  (usa "git push" para publicar tus commits locales)
```


