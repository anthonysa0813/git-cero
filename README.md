# Curso de git desde cero

-Existen tres estados de git:

1)Estado de proyecto
2)Estado de stagging o de preparación (git add <file> ó git add .)
3)Estado de repositorio local (git commit -m "some comment")

- Configuración de git: "git config --global user.email "contact@email.com""

- Para quitar del estado de stagging algún archivo: "git restores --staged <file>"
- Para ver los logs de mis commits: "git log"
- Para ver las diferencias entre logs: git diff code_log code_log
- Para ir hacia un commit especifico: "git checkout <some_code_commit_log>"
- Para regresar al principal: "git checkout master ó main"

## Git reset:

- "git reset <some_code_commmit_log> --hard": todo vuelve a ese estado
- "git reset <some_code_commmit_log> --soft": vuelve a ese estado pero lo que este en stagging, seguirá en ese estado.

## Git Log

- Para condensar los logs: "git log --oneline"
- Para ver algo de información: "git log --raw"
- Para ver los últimos 5 commits logs: "git log --oneline -n 5"
  -Para ver todos y con grafica las logs: "git log --oneline --all --graph --decorate"

## Ramas

- Para crear una rama: "git branch <name_branch>"
- Para listar las ramas existentes: "git branch"
- Para cambiarnos a otra rama: "git checkout <name_branch>" ó "git switch <name_branch>"
- Para fusionar las ramas: "git merge <name_branch>"
- Si queremos enviar un rama al repositorio de github: "git push -u origin <name_branch>"
- Para eliminar rama: "git branch -D <name_branch>"
- Si deseas crear una rama y cambiarte a esa rama: "git checkout -b <name_branch>"
- git show-branch --all

- gitk

## Git remote

- Para clonar un repositorio: "git clone <enlace_github>"
- Otra forma de trabajar con remotos: "git remote add origin <enla_https_github_project>"
- Para traernos los cambios y guardarlos en nuestra rama: "git pull origin <branch_name>"
- Para unir todos los cambios si el merge se rehusa : "git pull origin master --allow-unrelated-histories"

- Para saber a donde está apuntando nuestro repositorio si trabajamos con el flujo colaborativo: "git remote -v"
- Para traerme los cambios del repositorio: "git pull origin <branch>"
- Para eliminar una rama que este en el remote: "git push --delete origin <name_branch>"

## Llaves ssh

Generar una nueva llave SSH: (Cualquier sistema operativo)

- ssh-keygen -t rsa -b 4096 -C "youremail@example.com"

Comprobar proceso y agregarlo (Windows)

- eval $(ssh-agent -s)
- ssh-add ~/.ssh/id_rsa
  Comprobar proceso y agregarlo (Mac)

eval "$(ssh-agent -s)"
¿Usas macOS Sierra 10.12.2 o superior?
Haz lo siguiente:

cd ~/.ssh
Crea un archivo config…
Con Vim vim config
Con VSCode code config
Pega la siguiente configuración en el archivo…
Host \*
AddKeysToAgent yes
UseKeychain yes
IdentityFile ~/.ssh/id_rsa
Agrega tu llave

ssh-add -K ~/.ssh/id_rsa
🥳

## Alias

- alias arbolito="git log --all --decorate --graph"

## Tags

- Para crear un tag: "git tag -a v0.1 -m 'comentario de lo que se hizo en esta versión' <hash_log>"

- Para ver los tags cread: "git tag"
- Para enviar los tags a github: "git push origin --tags"
- Para eliminar un tag: "git tag -d <name_tag>"
- Para borrar la referencia del tag en github: "git push origin :refs/tags/<name_tag>

## Fork

- Los forks son como copias pero propias, una vez que hagamos fork a un repositorio viene a ser de nuestra propiedad, así el repositorio se haya eliminado.
- podremos hacer cambios sin tener que pedirle permiso a dueño del repositorio.

## Pull Request & Issues

- Pull request: Si deseamos contribuir con otros repositorios. significa que le estamos "solicitando un cambio" y este cambio se hará visible si el dueño del repositorio lo acepta.f5
- Issue: Es un comentario que le dejamos a un repositorio sobre algun bug, sugerencia, etc.
