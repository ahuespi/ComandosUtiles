# Comandos Utiles


## **Composer**

* ### Instalar Composer en la carpeta del proyecto (NO GLOBAL)

En la consola, tiene que escribir lo siguiente:

```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

php -r "if (hash_file('sha384', 'composer-setup.php') === '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

php composer-setup.php

php -r "unlink('composer-setup.php');"
```

## **PHP UNIT**

Requisitos:
* Tenes instalado Composer en la carpeta donde voy a iniciar PHP UNIT

``` php composer.phar require phpunit/phpunit ```


## **GIT HUB**

#### Configurar los datos de su cuenta
```
git config --global user.email "emaildegithub@chachara.com"
git config --global user.name "NombreDeUsuarioDeGitHub"
```
#### Si es un proyecto propio:
* Ir a Github -> New
* Ponerle un nombre al repo y crearlo sin un archivo README.md
* Luego tirar estos comandos en consola:
```
echo "# ComandosUtiles" >> README.md

git init

git add README.md

git commit -m "first commit"

git remote add origin git@github.com:nombreDeUsuarioDeGithub/nombreDelRepoQueCrearon.git

git push -u origin master
```

---

## Pasos utiles para el dia del examen:


* **git checkout master** --> (Te situas en tu branch master)

* **git pull upstream master** --> (Traes todos los archivos actualizados del repositorio externo)

* **git push origin master** --> (Envias todos esos archivos actualizados a tu branch master)

### **Si todavia no tenes un branch para trabajar:**

* **git branch nombreDelNuevoBranch** --> (Creas el nuevo branch)
* **git checkout nombreDelNuevoBranch** --> (Te situas en el nuevo branch)
* **git merge master** --> (Actualizas el nuevo branch con lo que se actualizó en tu master en el punto 3 anterior)

### **Si ya tenes un branch donde trabajaste:**

* **git status** --> (Para ver si falta algo por commitear)

Si no hay nada para commitear:

* **git checkout nombreDelNuevoBranch** --> (Te situas en el nuevo branch)
* **git merge master** --> (Actualizas el nuevo branch con lo que se actualizó en tu master en el punto 3 anterior)

Si hay algo en rojo que indica que todavia no se agregó para commitear:

* **git add nombreDelArchivo** --> (Agregar el archivo para commitear)
* **git commit** --> (Commitear los archivos agregados)
* **git merge master** --> (Actualizas el nuevo branch con lo que se actualizó en tu master en el punto 3 anterior)


[Ver el nombre del branch actual en la terminal](https://www.leaseweb.com/labs/2013/08)
[Ver el nombre del branch actual en la terminal - 2 ](https://www.shellhacks.com/show-git-branch-terminal-command-prompt/)


## RABBITMQ EN DOCKER

Instalar Docker y su Interfaz Grafica
```
docker run -d --hostname my-rabbit --name RabbitMQ -p 8080:15672 -p 5672:5672 rabbitmq:3-management
```

https://www.youtube.com/watch?v=R8pMwciZ95U&t