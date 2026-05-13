# Gestión básica de entorno Linux y administración de archivos

## 1. Estructura base del proyecto

### 1.1 Crea una carpera anomenada: workspace

```git
mkdir workspace
```

### 1.2 Dentro de ella, crea utilizando una sola instrucción:

frontend/

backend/

docs/ 

scripts/

backup/


- mover en el carpeta **workspace**
  
```git
cd workspace
```
- crear las carpetas

```git
mkdir frontend/ backend/ docs/ scripts/ backup/ 
```

## 2. Creación de archivos

### 2.1 Crea los siguientes archivos:

frontend/index.html

frontend/styles.css

backend/server.js

docs/README.md

scripts/deploy.sh

```git
touch frontend/index.html frontend/styles.css backend/server.js docs/README.md scripts/deploy.sh

```

## 3. Gestión de archivos

### 3.1 Copia: README.md

dentro de: backup/

```git
cp docs/README.md backup/
```

### 3.2 Renombra: server.js

a: app.js

```git
mv backend/server.js backend/app.js
```

### 3.3 Mueve: styles.css

a: docs/

```git
 mv frontend/styles.css docs/

```
- ejecutar 

```git
ls frontend/ docs/
```
resultado:
```
docs/:
README.md  styles.css

frontend/:
index.html
```

## 4 Permisos y seguridad

### 4.1 Asigna permisos: 

permisos actual:

```git
root@ed3da28a9a6d:/workspace# ls -l scripts/deploy.sh docs/README.md 
-rw-r--r-- 1 root root 0 May 13 14:51 docs/README.md
-rw-r--r-- 1 root root 0 May 13 14:51 scripts/deploy.sh
```

- **deploy.sh** - ejecutable solo para propietario

```git
chmod 744 scripts/deploy.sh 
```


- **README.md** - solo lectura para todos

```
chmod u-w docs/README.md
```


### 4.2 Verfica los permisos de todos los archivos:

## 5 Verificación final

```
root@ed3da28a9a6d:/workspace# ls -l docs/README.md scripts/deploy.sh 
-r--r--r-- 1 root root 0 May 13 14:51 docs/README.md
-rwxr--r-- 1 root root 0 May 13 14:51 scripts/deploy.sh
```

### 5.1 Muestra:

- estructura completa
  
```text
workspace/
├── backend/
│   └── app.js
├── frontend/
│   └── index.html
├── scripts/
│   └── deploy.sh
├── docs/
│   ├── README.md
│   └── styles.css
├── backup/
│   └── README.md

```

- ruta actural

```text
root@ed3da28a9a6d:/workspace# pwd
/workspace
```

- historia de comandos

```text
root@ed3da28a9a6d:/workspace# history
    1  ls
    2  mkdir workspace
    3  ls
    4  cd workspace
    5  mkdir frontend/ backend/ backup/ docs/ scripts/
    6  ls
    7  touch frontend/index.html
    8  ls frontend/
    9  touch frontend/styles.css
   10  touch backend/server.js docs/README.md scripts/deploy.sh
   11  ls backend/
   12  ls docs/ scripts/
   13  cp docs/README.md backup/
   14  ls docs/ back
   15  ls docs/ backup/
   16  mv backend/server.js backend/app.js
   17  ls backend/
   18  mv frontend/styles.css docs/
   19  ls frontend/ docs/
   20  ls -l scripts/deploy.sh docs/README.md 
   21  chmod 744 scripts/deploy.sh 
   22  ls -l scripts/
   23  chmod u-w docs/README.md 
   24  ls -l docs/
   25  ls -l docs/README.md scripts/deploy.sh 
   26  ls frontend/ backend/ backup/ scripts/ docs/
   27  pwd
   28  history
```