# Ejercicio 1 — Primer repositorio local en Git

En este ejercicio trabajarás completamente en tu computador local para comprender el flujo básico de Git y su modelo interno:

**Working Directory → Staging Area (Index) → Commit (HEAD)**

Aprenderás no solo los comandos, sino qué ocurre internamente en el repositorio.

---

## 1️⃣ Crear una carpeta para el proyecto

### Concepto

Un repositorio Git vive dentro de un directorio del sistema de archivos (o una carpeta)

### Comando

```bash windows
mkdir quijote-git
cd quijote-git
```

> **Qué ocurre ?**  Solo estás creando una carpeta normal. Aún no es un repositorio Git.


## 2️⃣ Inicializar el repositorio

### Concepto

Un repositorio se crea con `git init`. Esto genera la estructura interna que Git necesita para funcionar.

```bash windows
git init
```

> **Qué ocurre internamente ?**  Git crea un directorio oculto llamado .quijote-git/

```
.quijote-git/
└── .git/
```

Dentro de .git/ se almacenan:  

* Objetos (blobs, trees, commits)
* Referencias (branches)
* HEAD
* Configuración

Ahora la carpeta está bajo control de versiones.

## 3️⃣ Mostrar las ramas (y crear main si no existe)

### Comando para ver ramas

```bash
git branch
```

Dependiendo de la configuración:

* Puede existir main
* Puede existir master
* Puede no haber commits todavía (rama sin historial)

Si no existe main, crearla

```bash
git branch -M main
```

Verifica nuevamente:

```bash
git branch
```

El * indica la rama actual (HEAD apunta a ella).

## 4️⃣ Crear un archivo con un extracto de Don Quijote

### Concepto

El archivo primero vive en el Working Directory. Git aún no lo rastrea.

a) Crea un archivo llamado quijote.txt

b) editar el archivo y agrega el siguiente texto.

```
En un lugar de la Mancha, de cuyo nombre no quiero acordarme,
no ha mucho tiempo que vivía un hidalgo de los de lanza en astillero,
adarga antigua, rocín flaco y galgo corredor.
```
c) Guardar el archivo

## 5️⃣ Ver el estado del repositorio

