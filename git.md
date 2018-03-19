# How to en git

## comandos basicos

```git init``` _Inicializa el repositorio_   
```git status``` _Muestra el estado del reposito_   
```git log``` _Muestra la actividad realizada en el repositorio_   
```git add . ``` _Agrega todas las modificaciones y archivos nuevos al stage_    
```git commit -m "mensaje" ``` _guarda un momento del stage_    
```git push``` _sube el commit al repositorio_  
```git --version``` _muestra la versión actual de git_  
```git help``` _muestra la ayuda de git_  
```git help {comando}``` _muestra la ayuda completa de un comando en particular_  

## Primeros pasos

1. Identificarse en la computadora local

    ```git config --global user.name "Gabriel"```  
    ```git config --global user.email "nnnnnn@nnnn.nn"```

    * Mostrar el contenido de las variables globales

        ```git config --global -e ```

2. Creacion de alias

    * alias para git log  
       ```git config --global alias.lg  "log --oneline --decorate --all --graph"```  

    * alias para status  
        ```git config --global alias.s "status -s -b"```  

    [Video curso git - Alias Lecture](https://www.udemy.com/git-github/learn/v4/t/lecture/7306470)  


## Ver repositorios remotos

```git remote -v```

## Usar Tags

Un tag hace referencia a un commit y a todo el estado del proyecto en ese commit:

* Crear un tag

``git tag V1.0.0``

* Ver los tags

``git tag``

* Borrar tags

``git tag -d V1.0.0``

* Crear tags asociados al commit actual con una descripcion

``git tag -a v1.0.0 -m "Version 1.0.0"``

* Crear tags asociados a un commit espacifico con una descripcion

``git tag -a v0.1.0 345d7de -m "Versión alfa"``

* Crear un tag que abre una consoloa para agregar un mensaje mas elaborado

``git tag -a v0.1.0 345d7de``

* Mostrar la información de un tag

``git show v1.0.0``

* Subir todos Tags al repositorio

``git push --tags``
