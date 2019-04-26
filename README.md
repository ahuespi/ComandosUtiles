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
* Ponerle un nombre al repo e crearlo sin un archivo README.md
* Luego tirar estos comandos en consola:
```
 echo "# ComandosUtiles" >> README.md

git init

git add README.md

git commit -m "first commit"

 git remote add origin git@github.com:nombreDeUsuarioDeGithub/nombreDelRepoQueCrearon.git

git push -u origin master

```