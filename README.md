# my-proyecto-millonario

## Trabajo diario a través de git

## Indice

- [Commit inicial](#commitinicial)
- [Push inicial](#pushinicial)
- [Ignorar archivos](#ignorararchivos)
- [Añadir fichero 1.txt](#añadirfichero)
- [Ejercicio 5](#ejercicio5)
- [Ejercicio 6](#ejercicio6)
- [Ejercicio 7](#ejercicio7)
- [Ejercicio 8](#ejercicio8)
- [Ejercicio 9](#ejercicio9)

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



>Pregunta: Si ejecutado las acciones add y commit, que realiza cada una sobre el/los ficheros. Justifica tu respuesta en el fichero README.md.

- 