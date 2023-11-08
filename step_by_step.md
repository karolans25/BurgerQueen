# Integrate the backend and the frontend

## 1. Add the submodules

`git submodule add https://github.com/karolans25/DEV010-burger-queen-api backend`

`git submodule add https://github.com/karolans25/DEV010-burger-queen-api-client frontend`

## 2. How to be able to use the submodules of this repository (when it's cloned)

When you have added the submodules and your collaborators are going to clone it, they'll get the directories that contain submodules empty.

### First way:
So, it's necessary to get into each submodule directory and run the next two commands for each one:

`git submodule init`

`git submodule update`

### Second way:
Adding the `--recursive` arg in the cloning comand
`git clone --recursive git@github.com:karolans25/BurgerQueen.git`

## 3. How to update the submodules (frontend and backend)

### First way:
If you want to check new changes in the submodule you can access to the directory of the submodule and run `git fetch` and `git merge` in the upstream branch to update the local code.

`cd frontend`

`git fetch`

`git merge origin/main`

Now, if you come back to the principal project and run `git diff --submodule` you'll check that the submodule was updated and get the commit list added. 

Si hace “commit” en este punto, bloqueará el submódulo para que tenga el nuevo código cuando otras personas lo actualicen.

### Second way: 

There's another wat if you don't prefer looking for changes in each submodule and merge then manually in the subdirectory. If you run `git submodule update --remote`, Git will go and check an update everything by itself.

`git submodule update --remote frontend`

`git submodule update --remote backend`

[Git documentation for submodules](https://git-scm.com/book/es/v2/Herramientas-de-Git-Subm%C3%B3dulos) 
