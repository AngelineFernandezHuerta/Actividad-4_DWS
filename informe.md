# Informe de la actividad

Describe aquí los pasos realizados, comandos usados y pega capturas de pantalla.

## Objetivo

Completar la práctica de Git/GitHub creando el repositorio `DWeb`, gestionando archivos, ramas, merges, conflictos, tags y subiendo el trabajo a GitHub.

## Resumen de pasos realizados

1. Crear estructura local y archivos iniciales: `README.md`, `Hernan.txt` (renombrado después), `.gitignore`, `privado.txt`, carpeta `privada/`.
2. Inicializar repositorio Git y realizar commit inicial con mensaje: "Comenzamos con la creación de repositorio.".
3. Crear rama `Libro`, añadir `indice.txt` y `2.txt` en esa rama y commitear.
4. Volver a `master`, añadir `pagina.txt` (versión A) y commitear.
5. Modificar `pagina.txt` en `Libro` (versión B) y commitear; realizar merge en `master` provocando conflicto en `pagina.txt`.
6. Resolver conflicto manteniendo la versión final que incluye el capítulo 4 (Gestión de ramas), commitear la resolución.
7. Crear tag `Libro` y borrar la rama `Libro` localmente.
8. Añadir remoto `origin` y subir `master`, tags y crear/push de la rama remota `v0.2`.
9. Renombrar `Hernan.txt` a `Angeline.txt`, commitear y push.
10. Actualizar `README.md` con tu nombre y enlace al repo, añadir fila en la tabla de compañeros y subir cambios.

## Comandos principales ejecutados

Inicializar y commit inicial:

```
git init
git config user.name "Tu Nombre"
git config user.email "tuemail@example.com"
git add README.md Hernan.txt .gitignore
git commit -m "Comenzamos con la creación de repositorio."
```

Ramas, commits y conflicto:

```
git branch Libro
git checkout Libro
echo "Índice del proyecto" > indice.txt
echo "Contenido del archivo 2" > 2.txt
git add indice.txt 2.txt
git commit -m "Añadir indice.txt y 2.txt en rama Libro"
git checkout master
echo "(versión A)" > pagina.txt
git add pagina.txt
git commit -m "Añadir pagina.txt en master (versión A)"
git checkout Libro
echo "(versión B con Capítulo 4)" > pagina.txt
git add pagina.txt
git commit -m "Modificar pagina.txt en Libro (versión B)"
git checkout master
git merge Libro   # conflicto en pagina.txt
# Resolver conflicto: editar pagina.txt con la versión final y luego:
git add pagina.txt
git commit -m "Resolver conflicto en pagina.txt"
```

Remoto y push:

```
git remote add origin https://github.com/AngelineFernandezHuerta/Actividad-4_DWS.git
git push -u origin master
git push origin --tags
git checkout -b v0.2
git push -u origin v0.2
```

Renombrar archivo y actualizar README:

```
git mv Hernan.txt Angeline.txt
git commit -m "Renombrar Hernan.txt a Angeline.txt"
git push

# Actualizar README y push
git add README.md
git commit -m "Actualizar README: añadir autor y enlace al repo"
git push origin master
```

Comprobaciones y listados guardados localmente:

```
git branch --merged > merged_branches.txt
git branch --no-merged > no_merged_branches.txt
git log --graph --decorate --all --oneline > commits_overview.txt
```

## Archivos creados/importantes

- `README.md` (descripción, tabla compañeros, autor y enlace)
- `Hernan.txt` → renombrado a `Angeline.txt`
- `.gitignore` (ignorando `privado.txt` y `privada/`)
- `privado.txt`, `privada/.gitkeep`
- `indice.txt`, `2.txt` (en rama `Libro`)
- `pagina.txt` (archivo con conflicto resuelto)
- `merged_branches.txt`, `no_merged_branches.txt`, `commits_overview.txt`
- `informe.md` (este documento)

## Capturas y evidencias

Pega aquí capturas de pantalla de la interfaz de GitHub o del terminal que consideres necesarias. Ejemplos: historial de commits, lista de ramas, conflicto en `pagina.txt`, confirmación de push en GitHub.

## Cómo reproducir desde cero

1. Clonar el repo remoto:

```
git clone https://github.com/AngelineFernandezHuerta/Actividad-4_DWS.git
cd Actividad-4_DWS/DWeb
```

2. Revisar ramas y commits:

```
git branch -a
git log --graph --decorate --all --oneline
```

## Notas y siguientes pasos

- Invitar a `sandrallara` como colaborador mediante Settings → Collaborators en GitHub.
- Seguir y añadir estrellas a repositorios de compañeros desde la web de GitHub.
- Si deseas, puedo generar un PDF del informe o insertar capturas si me las facilitas.

---

Fecha de generación: 2026-05-15

