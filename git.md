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






