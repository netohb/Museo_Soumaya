# Museo Soumaya — Comandos de Git

Guía paso a paso de los comandos de git que utilicé para subir el código al repositorio.

Primero tengo que decir que me ubiqué en la carpeta que tengo para la materia y ahí comencé desde cero el archivo .html donde copié la siguiente página: https://www.museo-soumaya.org/

Tengo en link del primer pull request: https://github.com/netohb/Museo_Soumaya/pull/1, ahora debo de explicar que solamente hay un PR porque tuve problemas con los pull request, como cree el repositorio vacío e hice los primeros commit en otra rama que no era la main, al intentar hacer un pull request no me dejaba comparar entre ramas, es decir, no existía la rama main, entonces con la ayuda de ChatGPT, puse los comandos siguientes en la terminal: 

```bash
git rev-list --max-parents=0 user/netohb/soumaya-page  #Obtén el primer commit (la raíz) de tu rama

git branch -f main <SHA_QUE_COPIASTE>  #Mueve main para que apunte a ese commit raíz

git push -u -f origin main  #Publica esa main en GitHub (forzando, para reemplazar la main huérfana)

```

Como pueden observar, ya había creado la rama main huérfana, pero precisamente por esto no me dejaba comparar entre ramas, al parecer esto surgió porque main y user/netohb/soumaya-page no compartían historia. Creé main con --orphan y GitHub no puede calcular el diff entre dos raíces diferentes, así que no te dejaba abrir el PR.

Lo arreglé con ayuda de ChatGPT dejando main apuntando a la raíz (primer commit) de mi rama de trabajo, para que sí existiera un ancestro común.


## Comandos utilizados

```bash
git clone https://github.com/netohb/Museo_Soumaya.git  # para clonar el repositorio

cd .\Museo_Soumaya\  # para entrar al repositorio

git checkout -b user/netohb/soumaya-page  # para crear una nueva rama en el repositorio

En esta parte en el tiempo, puse los archivos que ya tenía hechos en el repositorio

git status  # para verificar que estoy en la rama correcta e identifíque los archivos que añadí

git add /nombre de los archivos # aquí perfilé los archivos para un commit

git commit -m "mensaje del commit" # aquí hice commit de los archivos, para tomar una foto de mi trabajo en el tiempo

git push --set-upstream origin user/netohb/soumaya-page  # para subir los cambios a github en la rama específicada
