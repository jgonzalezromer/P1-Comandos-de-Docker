# P1-Comandos-de-Docker

## 1. Descargar e comprobar que unha imaxe está no teu equipo
Para descargar unha imaxe utilizaremos o comando `docker pull {Nome da imaxe}`, neste caso úsase a imaxe de nginx.  
Para comprobar que unha imaxe está no equipo, utilízase o comando `docker images`.

## 2. Crear un contedor sen nome, ¿queda arrancado?, ¿como obtés o nome?
Para arrancar un contedor sen nome utilizamos o comando `docker run -d nginx`.  
Si, queda arrancado xa que Docker asígnalle un nome aleatorio automaticamente.  
Para coñecer o nome, pódese ver co comando `docker ps -a` e revisar a columna dos nomes dos contedores. Tamén pode verse en Visual Studio Code ao colocar o cursor sobre o contedor.

## 3. Crear un contedor co nome 'u1', ¿como accedes a el?
Para crear o contedor utilizamos o comando `docker run -d --name u1 nginx`.  
Para acceder a el, podemos utilizar o comando `docker exec -it u1 /bin/bash` ou facer clic dereito sobre o contedor e seleccionar **Attach Shell**.

## 4. Comprobar a súa IP e facer ping a google.com
Para comprobar a súa IP utilizamos o comando `ifconfig` e para facer ping, `ping google.com`.  
Se non temos estas utilidades, debemos instalalas cos comandos `apt update`, `apt install -y iputils-ping` e `apt install -y net-tools`.

## 5. Crear un contedor co nome 'bono', ¿podes facer ping entre os contedores?
Para crear o contedor utilizamos o comando `docker run -d --name bono nginx`.  
Se faltan as utilidades, debemos instalalas con `apt update`, `apt install -y iputils-ping` e `apt install -y net-tools`.  
Para facer ping entre os contedores utilizamos o comando `ping {IP do outro contedor}`, estes comunícanse se están na mesma rede.

## 6. ¿Que pasa co contedor se pechas as terminais?
Se pechamos as terminais, os contedores seguirán en segundo plano. Para comprobalo, podemos utilizar o comando `docker ps`.

## 7. ¿Canto espazo en disco ocupaches? Usa Docker para calculalo
Para ver canto espazo en disco utilizamos, executamos o comando `docker system df`. Neste caso, utilizáronse aproximadamente 458.6 MB.

## 8. ¿Canta RAM ocupan os contedores? Crea varios para calculalo
Para ver canta RAM ocupan os contedores, utilizamos o comando `docker stats` con contedores en execución. Neste caso, dous contedores están utilizando ao redor do 0.1% da memoria RAM.

## 9. ¿Como clonaches o repositorio?
Para clonar un repositorio utilizamos o comando `git clone {DirecciónDoRepositorio}`.

## 10. ¿Como engadiches o ficheiro readme2.md?
Para engadir o ficheiro `readme2.md`, primeiro creámolo co comando `echo "Texto" > readme2.md`, dentro do directorio do repositorio.  
Para engadilo, utilizamos o comando `git add -A readme2.md`.

## 11. Pasos a seguir para subir o ficheiro que estás a editar e o ficheiro readme2.md
Despois de realizar o paso anterior, utilizamos o comando `git commit -m "Texto para saber que se actualizou"`.  
Finalmente, utilizamos o comando `git push` para subir os cambios ao repositorio. Como só hai unha rama, non é necesario especificar a cal rama envialos.

## 12. ¿Como comprobarías que existen diferenzas entre o teu repositorio local e o remoto?
Para ver as diferenzas entre o repositorio local e o remoto, utilizamos o comando `git diff origin/main`.

---

Se se desexa ver dunha forma gráfica, este documento pódese acompañar co seguinte [enlace a Google Docs](https://docs.google.com/document/d/1n1eWJ78NX0vyJ95x-zQEwg3JVdBDc_Ndeg7THFZmB7Q/edit?usp=sharing), onde se atopan imaxes do proceso en orde.

