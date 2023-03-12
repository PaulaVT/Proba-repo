# Comandos en GIT
## Práctica 1 e 2: creación, conexión e actualización de repositorios git

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
git config --global color.ui auto
```
>Serve para poder cambiar a cor da interfaz de usuario.

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
---
12. Creamos o repositorio Libro.
13. Creamos o arquivo índice e engadímolo ao repositorio.
14. Realizamos un commit e comprobamos o estado do respositorio.
15. Modificamos índice e mostramos os cambios respecto da última versión.
16. Facemos un commit dos cambios e logo cambiamos a mensaxe do commit.
17. Finalmente volvemos mostrar os cambios no repositorio.

## Práctica 3: Historial de Cambios
-------------------------------------------------------------------------
###Comandos empregados:

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

1. Clonamos o repositorio Libro de: https://github.com/asalber/libro-git
2. Dentro do mesmo creamos a carpeta capítulos e un ficheiro chamado capitulo1.
3. Engadimolo ao repositorio e facemos un commit.
4. Mostramos os cambios.
5. Creamos o ficheiro capitulo2.txt co contido indicado, engadimolo ao repositorio e facemos un commit
6. Mostramos as diferencias entre a versión actual e dúas versións antes.
7. Creamos o ficheiro capitulo3.txt co contido indicado, engadímolo ao repositorio e facemos un commit
8. Mostramos as diferencias entre a primeira e a última versión do repositorio.
9. Engadimos ao final do ficheiro indice.txt a liña "Capítulo 5: Conceptos avanzados"
10. Engadímolo ao repositorio e facemos un commit.
11. Mostramos quen fixo os cambios no ficheiro indice.txt


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

1. Creamos a rama bibliografía.
2. 
1. Creamos unha nova rama nuevaRama.
2. Facemos un commit para avanzar coa rama main.
3. Facemos un checkout para apuntar á rama nuevaRama. 
4. Facemos un commit para avanzar coa rama nuevaRama.
5. Ahora temos dous commits diferentes, e a cada un apunta unha rama diferente.
6. Facemos un checkout main.
7. Facemos un marge nuevaRama para combinar as ramas, crearase un novo commit.
8. Borramos nuevaRama con branch -d.
9. Creamos unha nova rama con branch nuevaRama2.
10. Facemos o proceso anterior para separar as dúas ramas que temos agora mesmo.
11. Nunha rama editamos un ficheiro, e na outra editamos o mismo ficheiro, pero de forma diferente.
12. Colocamonos na rama main con checkout.
13. Facemos o commit -a -m ""Mensaxe", daranos un error porque o ficheiro que editamos de diferente forma nas duas ramas non o pode combinar.
14. Daremoslle á opción de combinar todo e engadirá todo o contido dos dous arquivos.




## Práctica 6: Repositorios remotos
-------------------------------------------------------------------------
###Comandos empregados

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
7. Finalmente comprobamos que p push e todos os cambios están ben feitos vendo todos os commits do proxecto.

