#Curso de git desde cero

-Existen tres estados de git:

1)Estado de proyecto
2)Estado de stagging o de preparación (git add <file> ó git add .)
3)Estado de repositorio local (git commit -m "some comment")

- Para quitar del estado de stagging algún archivo: "git restores --staged <file>"
- Para ver los logs de mis commits: "git log"
- Para ver las diferencias entre logs: git diff code_log code_log
- Para ir hacia un commit especifico: "git checkout <code_commit_log>"
- Para regresar al principal: "git checkout master ó main"

Git Log

- Para condensar los logs: "git log --oneline"
- Para ver algo de información: "git log --raw"
- Para ver los últimos 5 commits logs: "git log --oneline -n 5"
  -Para ver todos y con grafica las logs: "git log --oneline --all --graph --decorate"

Ramas

- Para crear una rama: "git branch <name_branch>"
- Para listar las ramas existentes: "git branch"
- Para cambiarnos a otra rama: "git checkout <name_branch>" ó "git switch <name_branch>"
- Para fusionar las ramas: "git merge <name_branch>"
- Si queremos enviar un rama al repositorio: "git push -u origin <name_branch>"
