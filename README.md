### <center>Ejercicio Cronjob </center>

Para poder construir este proyecto damos a:
```sh
docker build -t cronjob .
```
Para correr la imagen construida especificamos 
<strong>(-d) Ejecutar contenedor en segundo plano e imprimir ID de contenedor </strong>
```sh
docker run -itd cronjob
```
Al tener esto se generará el ID tal como se especifica arriba debido al comando que se agregó

Lo que se tendría que hacer ahora es comprobar que está corriendo...
```sh
docker ps
```
 Tomamos su ID y corremos
```sh
docker exec -it [ID] bash
```
Nos encontramos ya en Ubuntu, corramos el CRON
```sh
tail -f /var/log/cron.log
```
Hecho esto veremos desde nuestra terminal en ubuntu cómo se va generando un texto línea por línea en un lapso de un minuto

Guía: https://www.markdownguide.org/basic-syntax/

Ante todo recordar cuáles son los comandos para pushear por primera vez un repositorio...
https://www.atlassian.com/git/tutorials/using-branches
```sh
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin [URL_REPOSITORY]
git push -u origin main
```
