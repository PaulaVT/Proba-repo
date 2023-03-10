# Comandos en GIT
## Práctica 1: creación, conexión e actualización de repositorios git

### Comandos empregados

```bash
git init
```
>Con este comando crearase un novo repositorio de Git. Serve tanto para crear un respositorio valeiro como para converter un proxecto xa existente nun repositorio de Git.

```bash
git config --global user.name "nome de usuario"
```
>Con este comando configurase o nome de usuario do repositorio

```bash
git config --global user.email contade@correo
```
>Serve para indicarlle a Git cal vai a ser o correo electrónico para todos os repositorios locais.
Tamén se pode empregar --local user.email para poder empregar diferentes contas.

```bash
git config --list
```
>Con este comando podemos comprobar todas as propiedades de Git configuradas.

```bash
git add .
```
>Sirve para engadir o proxecto ao Staging Area (que é o lugar onde se atopan os datos do proxecto e os seus cambios)

```bash
git status
```
>Este comnando mostra o estado do directorio de traballo, permite ver os cambios que se prepararon e os que nosm, así como os arquivos Git nos que non se vai a realizar seguimento. 

```bash
git commit
```
>Garda o contido actual do índice en un novo commit.

```bash
git commit -m "mensaxe"
```
>sirve para poñer unha mensaxe ao commit

```bash
git log --online --graph --decorate --all
```
>sirve para ver o historial completo

```bash
git branch -M main
```
>Cambia a rama do repositorio a Main forzando o cambio

```bash
git remote add origin dirección repositorio github
```
>A súa utilidade é a e conectar o repositorio local, ou de traballo ao repositorio remoto.

```bash
git push -u origin main
```
>Empregase para poder subir o contido de dito repositorio de traballo ao repositorio remoto.

```bash
git pull --all
```
>Serve para descargar o contido do repositorio remoto ao de traballo.

-----------------------------------------------------------------------------------


-----------------------------------------------------------------------------
### PASOS A SEGUIR NA PRÁCTICA

1. Inicializar repo local co comando `git init`.
2. Configurar o nome de usuario con `git config --global user.name "nome"`
3. Configurar a conta de correo con `git config --global user.email correo`
4. `git config --list`
5. Crear o contido, neste caso os arquivos index.html e engadilos empregando o comando `git add .`
6. Realizamos un commit coa mensaxe "Creación do proxecto".
7. Cambiamonos de rama a main empregando `git branch -M main`.
8. Conectamos o noso repositorio de traballo co repositorio remoto a través de `git remote add origin direccionDoRepo`.
9. Subimos o contido creado no repositorio local ao repositorio en liña empregando `git push`
10. Creamos o arquivo README.md
11. Baixamos eses arquivos do repositorio en liña ao local con `git pull --all`



## Práctica 2: Historial de Cambios
-------------------------------------------------------------------------

```bash
git diff
```
>Serve para mostrar as diferencias entre o directorio de traballo actual (é dicir, os cambios que aínda non foron confirmados) e o último commit.

```bash
git diff HEAD~2..HEAD
```
>Serve para comparar as diferencas entre o estado actual do repositorio e o estado do mesmo dous commits atrás.

```bash
git clone dirección
```
>Empregase para clonar un repositorio.

```bash
git annotate documento.extension
```
>Empregase para saber quen ou quenes foron os que modificaron os arquivos e en que commit o fixeron.

```bash
git reset --hard 5 1º caracteres del commit
```
>sirve para descartar todos os cambios que non se gardaron e volver ao estado anterior, ben sexa nun commit específico ou nun estado anterior do HEAD.


```bash
git remote remove repositorio
```
>Utilizamolo para eliminar un repositorio remoto do  repo local.


-----------------------------------------------------------------------------
### PASOS A SEGUIR NA PRÁCTICA

1. Creamos o repositorio de Libro.
2. Configurar o nome de usuario con `git config --global user.name "nome"`
3. Configurar a conta de correo con `git config --global user.email correo`
4. `git config --list`
5. Crear o contido, neste caso os arquivos index.html e engadilos empregando o comando `git add .`
6. Realizamos un commit coa mensaxe "Creación do proxecto".
7. Cambiamonos de rama a main empregando `git branch -M main`.
8. Conectamos o noso repositorio de traballo co repositorio remoto a través de `git remote add origin direccionDoRepo`.
9. Subimos o contido creado no repositorio local ao repositorio en liña empregando `git push`
10. Creamos o arquivo README.md
11. Baixamos eses arquivos do repositorio en liña ao local con `git pull --all`



## Práctica 4: Desfacer cambios
-------------------------------------------------------------------------
```bash
git remote remove repositorio
```
>Utilizamolo para eliminar un repositorio remoto do  repo local.

## Práctica 5: Ramas
-------------------------------------------------------------------------
```bash
git branch nomeRama
```
>Utilizamolo para crear una nova rama.

```bash
git branch -av
```
>Empregase para mostrar todas as ramas que existen tanto localmente como no repositorio remoto.

```bash
git checkout nomeRama
```
>Serve para cambiar de rama.

```bash
git merge nomeRama
```
>Serve fusionar a rama que desexemos coa rama na que estemos nese momento. É importante ter en conta que, en algúns casos, pode haber conflitos de fusión que deben resolverse manualmente.

```bash
git branch -d nomeRama
```
>Utilizamolo para eliminar unha rama unha vez feito o merge e sempre que non conteña novos cambios.


-----------------------------------------------------------------------------
### PASOS A SEGUIR NA PRÁCTICA

1. Creamos a rama bibliografía e mostramos as ramas do repo.
2. Logo creamos capitulo4.txt




## Práctica 6: Repositorios remotos
-------------------------------------------------------------------------
```bash
git remote add nomeRepo urlRepo
```
>Empregase para agregar un novo repo remoto ao repo local a través da dirección url 

```bash
git remote -v
```
> Emprégase para mostrar un listado dos repositorios remotos configurados no repo local e as direccións web de cada un deles.

```bash
git push nomeRepo nomeRama
```
>Usámolo para enviar os cambios nunha rama en específico ao repositorio remoto.

```bash
git checkout -b rama
```
>Utilizamolo para eliminar un repositorio remoto do  repo local.

```bash
git commit -am "mensaxe"
```
>Utilizamolo para eliminar un repositorio remoto do  repo local.

-----------------------------------------------------------------------------
### PASOS A SEGUIR NA PRÁCTICA

1. Creamos un novo repositorio en Github e engadímolo no repo local a través de `git clone url`.
2. Comprobamos que esté todo ben facendo un `git remote -v` e vendo todos os repositorios remotos.
3. Agora facemos o mesmo, pero clonando o repositorio de outro usuario.
4. Dentro del engadimos un ficheiro de autores e con nome de usuario e correo electrónico.
5. Engadimos os cambios a zona de intercambio temporal con `git add.` e facemos un commit avisando a través dunha mensaxe dos mesmos.
6. Subimos os cambios ao repositorio remoto con un `git push`.
7. TODO O DO FORK

