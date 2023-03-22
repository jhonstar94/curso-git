# Curso de _Git_ & _GitHut_
## Configuracion
```
git --version
git config --global user.name "Jhonatan"
git config --global user.email correo@gmail.com
git config --global user.ui true
git config --global init.defaultBranch main
git config --list
```
## Usar visual studio code como editor de git
```
git config --global core.editor "code --wait"
git config --global -e
```
## Hacer compatible Windows con Linux y Mac
```
git config --global core.autocrlf true
```
## Ver todas las opciones de la configuración en la terminal
```
git config -h
```
## Ver todas las opciones de la configuración en el navegador
```
git help config
```
# Inicializar  _Git_  en un directorio local
#### Crear Carpeta
```
mkdir carpeta
```
#### Dirigirse a la carpeta
```
cd carpeta
```
#### Crear Archivos
```
type nul > README.md
type nul > .gitignore
```
#### Iniciar Git por primera vez
```
git init
```
#### Abrir la configuración de Git en el Editor
```
code .
```
# Flujo Básico de Git
### agregar los cambios de un archivo al staged
```
git add archivo/directorio
```
### agregar todos los cambios de todos los archivos al staged
```
git add .
```
Los cambios son comprometidos en el repositorio, debes escribir el mensaje del cambio cuando se abra el archivo de configuración al terminar guarda y cierra el archivo para que los cambios tengan efecto
### Para agregar una modificación con título
```
git commit -m "mensaje descriptivo del cambio"
```
### Se agrega el origen remoto de tu repositorio de GitHub previamente creado en github.com
```
git remote add origin https://github.com/usuario/repositorio.git
```
### La primera vez que vinculamos el repositorio remoto con el local
```
git push -u origin master
```
### Para futuras actualizaciones, si no cambias de rama
```
git push
```
### Para descargar los cambios del repositorio remoto al local
```
git pull
```
### Para clonar un repositorio
```
git clone https://github.com/jhonstar94/curso-git.git
```
# Crear Ramas y trabajar en ellas
### crear rama
```
git branch nombre-rama
```

### cambiar de rama
```
git checkout nombre-rama
```

### crear una rama y cambiarte a ella
```
git checkout -b rama
```

### eliminar rama
```
git branch -d nombre-rama
```

### eliminar ramas remotas
```
git push origin --delete nombre-rama
```

### eliminar rama (forzado)
```
git branch -D nombre-rama
```

### listar todas las ramas del repositorio
```
git branch
```

### lista ramas no fusionadas a la rama actual
```
git branch --no-merged
```

### lista ramas fusionadas a la rama actual
```
git branch --merged
```

### rebasar ramas
```
git checkout rama-secundaria
git rebase rama-principal
```