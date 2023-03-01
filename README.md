# Comandos en GIT
## Práctica 1: creación e conexión de repositorios git

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
>Cambia a rama do repositorio a Main

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
2. Configurar o nome de usuario con `git config --global user.name "nome"
3. Configurar a conta de correo con `git config --global user.email correo
4. `git config --list
5. Crear o contido, neste caso os arquivos index.html e engadilos empregando o comando `git add .`
6. Realizamos un commit coa mensaxe "Creación do proxecto".
7. Cambiamonos de rama a main empregando `git branch -M main`.
8. Conectamos o noso repositorio de traballo co repositorio remoto a través de `git remote add origin direccionDoRepo`.
9. Subimos o contido creado no repositorio local ao repositorio en liña empregando git push
10. Creamos o arquivo README.md
11. Baixamos eses arquivos do repositorio en liña ao local con `git pull --all`




-------------------------------------------------------------------------
```bash
git clone
```
>Empregase para copiar un repositorio.


```bash
git reset --hard oquesea
```
>sirve para


```bash
git remote -v
```
>sirve para
```bash
git remote add nome link
```
>sirve para
```bash
git remote remove origin
```
>sirve para

