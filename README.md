# Museo Soumaya — Comandos de Git

Guía paso a paso de los comandos de git que utilicé para subir el código al repositorio.

Primero tengo que decir que me ubiqué en la carpeta que tengo para la materia y ahí comencé desde cero el archivo .html donde copié la siguiente página: https://www.museo-soumaya.org/

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
