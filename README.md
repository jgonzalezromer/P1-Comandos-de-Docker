# P1-Comandos-de-Docker



## 1. Descargar e comprobar que unha imaxe está no teu equipo.
# Para descargar unha imaxe utilizaremos o comando "docker pull {Nome da imaxe}", neste caso utilizei a imaxe de nginx.
# Para comprobar que unha imaxe está no meu equipo utilizarei o comando "docker images".

## 2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?
# Para arrincar un contenedor sen nome utilizamos o comando "docker run -d nginx".
# Si queda arrincado xa que docker ponlle un nome aleatorio de forma automática.
# Para poder saber o seu nome poderemos velo co comando "docker ps -a" e fixarnos na columna dos nomes dos contenedores, por defecto esta a dereita de todo. Tamén poderemos velo se estamos utilizando Visual Studio Code poñendo o rato encima do contendor.

## 3. Crea un contenedor coo nome 'u1', cómo accedes a el?
# Para crear o contenedor utilizamos o comnado "docker run -d --name u1 nginx".
# Para acceder a él poderemos utilizar o comando "docker exec -it u1 /bin/bash" ou dandolle click dereito encima do contendor e clicando en Attach Shell.

## 4. Comproba a súa ip e fai ping a google.com
# Para comprobar a sua ip utilizamos o comando "ifconfig" e para facer ping "ping google.com".
# Se temos o problema que non temos estas utilidades deberemolas descargar cos comandos "apt update", "apt install -y iputils-ping" e "apt install -y net-tools".

# 5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?
# Para crear o contenedor utilizamos o comando "docker run -d --name bono nginx".
# Se temos o problema que non temos estas utilidades deberemolas descargar cos comandos "apt update", "apt install -y iputils-ping" e "apt install -y net-tools".
# Para facer o ping entre os contenedores utilizaremos o comando "ping {IP do outro contenedor}", estos se comunican sempre e cando estan na mesma rede.


# 6. Se pechas as terminales, qué pasa coo contenedor?
# Se pechamos as terminales estas seguiran en segundo plano para comprobalo podemos utilizar o comando "docker ps".

# 7. Cánta memoria no disco duro ocupaches? usa docker para calculalo
# Para ver cánta memoria do disco duro utilizamos pondremos o comando "docker system df". Neste caso eu agora mesmo utilizei sobre 458.6 mb.

# 8. Cánta RAM ocupan os contenedores? Crea varios para calculalo
# Para ver canta RAM ocupan os contenedores teremos que por o comando "docker stats" tendo contenedores iniciados. Neste caso estarián utilizando dous contenedores ao redor de 0.1% de memoria RAM.

# 9. Cómo fixeches para clonar o repositorio
# Para clonar un repositorio utilizamos o comando "git clone {DireccionDoRepositorio}"

# 10. Cómo engades o arquivo readme2.md
# Para engadir o arquico readme2.md primeiro teremos que crealo eu neste caso o fixen co comando "echo "Texto" > readme2.md", isto dentro do directorio do repositorio que terá o mesmo nome.
# Para engadilo utilizamos o comando "git add -A readme2.md"

# 11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md
# Despois de facer o do apartado 10 utilizaremos o comando "git commit -m "Texto para saber en que se actualizou""
# Por último utilizaremos o comando "git push" para subir os cambios ao repositorio, como so temos un non temos porque expecificar a que rama mandalo.

# 12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.
# Para ver as diferenzas entre o repositorio local e remoto utilizamos o comando "git diff origin/main"




# Se se quere ver de unha forma gráfica podese acompañar este documento xunto co seguinte docs onde atopamos imaxes do proceso en orden.
# https://docs.google.com/document/d/1n1eWJ78NX0vyJ95x-zQEwg3JVdBDc_Ndeg7THFZmB7Q/edit?usp=sharing
