# **P1-Comandos-de-Docker**

## **1. Descargar y comprobar que una imagen está en tu equipo**
Para descargar una imagen utilizaremos el comando `docker pull {Nombre de la imagen}`, en este caso se utiliza la imagen de nginx.  
Para comprobar que una imagen está en el equipo, se utiliza el comando `docker images`.

## 2. Crear un contenedor sin nombre, ¿queda arrancado?, ¿cómo obtienes el nombre?
Para arrancar un contenedor sin nombre utilizamos el comando `docker run -d nginx`.  
Sí, queda arrancado ya que Docker le asigna un nombre aleatorio automáticamente.  
Para conocer el nombre, se puede ver con el comando `docker ps -a` y revisar la columna de los nombres de los contenedores. También puede verse en Visual Studio Code al colocar el cursor sobre el contenedor.

## 3. Crear un contenedor con el nombre 'u1', ¿cómo accedes a él?
Para crear el contenedor utilizamos el comando `docker run -d --name u1 nginx`.  
Para acceder a él, podemos utilizar el comando `docker exec -it u1 /bin/bash` o hacer clic derecho sobre el contenedor y seleccionar **Attach Shell**.

## 4. Comprobar su IP y hacer ping a google.com
Para comprobar su IP utilizamos el comando `ifconfig` y para hacer ping, `ping google.com`.  
Si no tenemos estas utilidades, debemos instalarlas con los comandos `apt update`, `apt install -y iputils-ping` y `apt install -y net-tools`.

## 5. Crear un contenedor con el nombre 'bono', ¿puedes hacer ping entre los contenedores?
Para crear el contenedor utilizamos el comando `docker run -d --name bono nginx`.  
Si faltan las utilidades, debemos instalarlas con `apt update`, `apt install -y iputils-ping` y `apt install -y net-tools`.  
Para hacer ping entre los contenedores utilizamos el comando `ping {IP del otro contenedor}`, estos se comunican si están en la misma red.

## 6. ¿Qué pasa con el contenedor si cierras las terminales?
Si cerramos las terminales, los contenedores seguirán en segundo plano. Para comprobarlo, podemos utilizar el comando `docker ps`.

## 7. ¿Cuánto espacio en disco ocupaste? Usa Docker para calcularlo
Para ver cuánto espacio en disco hemos utilizado, ejecutamos el comando `docker system df`. En este caso, se han utilizado aproximadamente 458.6 MB.

## 8. ¿Cuánta RAM ocupan los contenedores? Crea varios para calcularlo
Para ver cuánta RAM ocupan los contenedores, utilizamos el comando `docker stats` con contenedores en ejecución. En este caso, dos contenedores están utilizando alrededor de 0.1% de la memoria RAM.

## 9. ¿Cómo clonaste el repositorio?
Para clonar un repositorio utilizamos el comando `git clone {DirecciónDelRepositorio}`.

## 10. ¿Cómo añadiste el archivo readme2.md?
Para añadir el archivo `readme2.md`, primero lo creamos con el comando `echo "Texto" > readme2.md`, dentro del directorio del repositorio.  
Para añadirlo, utilizamos el comando `git add -A readme2.md`.

## 11. Pasos a seguir para subir el archivo que estás editando y el archivo readme2.md
Después de realizar el paso anterior, utilizamos el comando `git commit -m "Texto para saber qué se actualizó"`.  
Finalmente, utilizamos el comando `git push` para subir los cambios al repositorio. Como solo hay una rama, no es necesario especificar a qué rama enviarlos.

## 12. ¿Cómo comprobarías que existen diferencias entre tu repositorio local y el remoto?
Para ver las diferencias entre el repositorio local y el remoto, utilizamos el comando `git diff origin/main`.

---

Si se desea ver de una forma gráfica, este documento se puede acompañar con el siguiente [enlace a Google Docs](https://docs.google.com/document/d/1n1eWJ78NX0vyJ95x-zQEwg3JVdBDc_Ndeg7THFZmB7Q/edit?usp=sharing)
, donde se encuentran imágenes del proceso en orden:  
