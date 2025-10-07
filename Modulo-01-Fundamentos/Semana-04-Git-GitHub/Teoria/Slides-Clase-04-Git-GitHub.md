---
theme: black
highlightTheme: monokai
transition: slide
---

# Semana 4: Git & GitHub

**Módulo 1: Fundamentos**

Control de Versiones Profesional

---

## ¿Por Qué Git?

**Sin Git**:
```
proyecto.c
proyecto_v2.c
proyecto_final.c
proyecto_final_AHORA_SI.c
proyecto_final_DEFINITIVO.c
```

**Con Git**:
```
proyecto/
└── proyecto.c (+ historial completo)
```

---

## Git vs GitHub

**Git**:
- Software de control de versiones
- Local en tu computadora
- Gratis y open source

**GitHub**:
- Plataforma web
- Aloja repositorios
- Colaboración
- Portfolio

---

## Conceptos Clave

**Repository**: Proyecto con historial
**Commit**: Snapshot del proyecto
**Branch**: Línea paralela de desarrollo
**Remote**: Versión en servidor (GitHub)

---

## Workflow Básico

```
Working    Staging     Repository
Directory  Area        (commits)

modificar → git add → git commit
```

---

## Comandos Esenciales

```bash
git init              # Crear repo
git status            # Ver estado
git add archivo       # Añadir a staging
git commit -m "msg"   # Guardar cambio
git log               # Ver historial
```

---

## Branches

```
main:     A---B---C
               \
feature:        D---E
```

```bash
git branch feature
git checkout feature
# trabajo...
git checkout main
git merge feature
```

---

## GitHub Setup

1. Crear cuenta en github.com
2. Generar SSH key
3. Añadir key a GitHub
4. ¡Listo!

---

## Push y Pull

```bash
# Subir cambios
git push origin main

# Descargar cambios
git pull origin main
```

---

## Pull Requests

1. Crear branch
2. Hacer cambios
3. Push a GitHub
4. Abrir PR
5. Code review
6. Merge

---

## Proyecto de la Semana

**Subir proyectos anteriores a GitHub**:
- Crear repos para proyectos C
- README para cada uno
- Commits organizados
- Portfolio público

---

#git #github #control-versiones
