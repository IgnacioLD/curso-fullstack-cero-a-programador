# Introducción a Git y Control de Versiones

> **Semana 4 - Módulo 1: Fundamentos**
> **Duración**: 6-8 horas de estudio
> **Prerequisitos**: Conocimientos básicos de terminal

---

## Índice

- [[#Objetivos de Aprendizaje]]
- [[#¿Qué es Control de Versiones?]]
- [[#Git: Conceptos Fundamentales]]
- [[#Comandos Básicos]]
- [[#Workflow Típico]]
- [[#Branches (Ramas)]]
- [[#Recursos Adicionales]]

---

## Objetivos de Aprendizaje

Al finalizar:

- Entender qué es control de versiones y por qué es esencial
- Configurar Git en tu máquina
- Crear y gestionar repositorios locales
- Hacer commits efectivos
- Trabajar con branches
- Colaborar usando GitHub
- Resolver conflictos básicos

---

## ¿Qué es Control de Versiones?

### El Problema

**Sin control de versiones**:
```
proyecto.c
proyecto_v2.c
proyecto_v2_final.c
proyecto_v2_final_AHORA_SI.c
proyecto_v2_final_AHORA_SI_corregido.c
```

**Problemas**:
- No sabes qué cambió entre versiones
- Difícil colaborar con otros
- Imposible volver atrás fácilmente
- Archivos duplicados por todas partes

### La Solución: Control de Versiones

**Con Git**:
```
proyecto/
├── .git/         (historial completo)
└── proyecto.c    (versión actual)
```

**Ventajas**:
- Historial completo de cambios
- Volver a cualquier versión anterior
- Colaboración sin conflictos
- Backup automático
- Branches para experimentar

---

## Git vs GitHub

**Git**:
- Software de control de versiones
- Local en tu computadora
- Creado por Linus Torvalds (2005)
- Gratis y open source

**GitHub**:
- Plataforma web para alojar repositorios Git
- Permite colaboración
- Features adicionales: issues, pull requests, CI/CD
- Similar: GitLab, Bitbucket

**Analogía**:
- Git = Microsoft Word
- GitHub = Google Drive (para compartir documentos)

---

## Conceptos Fundamentales

### Repository (Repositorio)

**Definición**: Carpeta con historial Git

```bash
mi-proyecto/
├── .git/           # Base de datos Git (no tocar)
├── src/
│   └── main.c
└── README.md
```

### Commit

**Definición**: Snapshot (instantánea) de tu proyecto en un momento específico

**Analogía**: Punto de guardado en un videojuego

```
Commit 1: "Agregué función main"
    ↓
Commit 2: "Añadí validación de entrada"
    ↓
Commit 3: "Corregí bug en loop"
```

### Working Directory, Staging Area, Repository

```
Working Directory  →  Staging Area  →  Repository
(tus archivos)        (preparados)      (guardados)

    modificas      →    git add    →   git commit
```

**Workflow**:
1. **Working Directory**: Modificas archivos
2. **Staging Area**: Seleccionas qué cambios guardar (`git add`)
3. **Repository**: Guardas permanentemente (`git commit`)

---

## Instalación y Configuración

### Instalar Git

**Linux (Debian/Ubuntu)**:
```bash
sudo apt-get update
sudo apt-get install git
```

**macOS**:
```bash
# Con Homebrew
brew install git

# O al usar por primera vez
git --version  # Instala Xcode Command Line Tools
```

**Windows**:
- Descargar de [git-scm.com](https://git-scm.com/)
- Instalar Git Bash

### Configuración Inicial

**Identidad** (obligatorio):
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

**Editor por defecto**:
```bash
# Usar nano
git config --global core.editor "nano"

# O vim
git config --global core.editor "vim"

# O VS Code
git config --global core.editor "code --wait"
```

**Verificar configuración**:
```bash
git config --list
git config user.name
git config user.email
```

---

## Comandos Básicos

### Crear Repositorio

**Opción 1: Nuevo proyecto**:
```bash
mkdir mi-proyecto
cd mi-proyecto
git init
```

**Opción 2: Clonar existente**:
```bash
git clone https://github.com/usuario/repo.git
cd repo
```

### Ver Estado

```bash
git status
```

**Output típico**:
```
On branch main
Changes not staged for commit:
  modified:   archivo.c

Untracked files:
  nuevo.c
```

### Añadir Archivos (Staging)

```bash
# Añadir archivo específico
git add archivo.c

# Añadir varios
git add archivo1.c archivo2.c

# Añadir todos los modificados
git add .

# Añadir por extensión
git add *.c
```

### Hacer Commit

```bash
# Con mensaje inline
git commit -m "Mensaje descriptivo del cambio"

# Abre editor para mensaje largo
git commit

# Add + commit en uno (solo tracked files)
git commit -am "Mensaje"
```

**Buenos mensajes de commit**:
```
✓ "Añadí validación de email en formulario"
✓ "Corregí bug de división por cero en calc()"
✓ "Actualicé README con instrucciones de instalación"

✗ "cambios"
✗ "fix"
✗ "asdfasdf"
```

### Ver Historial

```bash
# Log completo
git log

# Log compacto
git log --oneline

# Con gráfico
git log --oneline --graph

# Últimos N commits
git log -n 5
```

### Ver Cambios

```bash
# Cambios no staged
git diff

# Cambios staged
git diff --staged

# Cambios en archivo específico
git diff archivo.c
```

---

## Workflow Típico

### Flujo Diario

```bash
# 1. Ver estado actual
git status

# 2. Hacer cambios en archivos
nano programa.c

# 3. Ver qué cambió
git diff

# 4. Añadir a staging
git add programa.c

# 5. Hacer commit
git commit -m "Añadí función de validación"

# 6. Repetir 2-5 según necesites
```

### Ejemplo Completo

```bash
# Crear proyecto
mkdir calculadora
cd calculadora
git init

# Crear archivo
echo '#include <stdio.h>' > main.c
echo 'int main(void) { return 0; }' >> main.c

# Primer commit
git add main.c
git commit -m "Estructura básica del programa"

# Modificar
echo 'printf("Calculadora\\n");' >> main.c

# Ver cambios
git diff

# Segundo commit
git add main.c
git commit -m "Añadí mensaje de bienvenida"

# Ver historial
git log --oneline
```

---

## Deshacer Cambios

### Antes de Staging

```bash
# Descartar cambios en archivo
git checkout -- archivo.c

# Descartar todos los cambios
git checkout -- .
```

### Quitar de Staging

```bash
# Quitar archivo de staging (cambios se mantienen)
git reset archivo.c

# Quitar todo de staging
git reset
```

### Modificar Último Commit

```bash
# Cambiar mensaje del último commit
git commit --amend -m "Nuevo mensaje"

# Añadir archivo olvidado al último commit
git add archivo_olvidado.c
git commit --amend --no-edit
```

### Volver a Commit Anterior

```bash
# Ver historial
git log --oneline

# Volver a commit específico (mantiene cambios)
git reset --soft COMMIT_HASH

# Volver y descartar cambios (peligroso)
git reset --hard COMMIT_HASH
```

---

## Branches (Ramas)

### ¿Qué son?

**Definición**: Líneas paralelas de desarrollo

**Analogía**: Universos paralelos donde experimentas sin afectar la versión principal

```
main:     A---B---C---D
                   \
feature:            E---F
```

### Comandos de Branches

```bash
# Ver branches
git branch

# Crear branch
git branch feature-login

# Cambiar a branch
git checkout feature-login
# O (Git 2.23+)
git switch feature-login

# Crear y cambiar en uno
git checkout -b feature-nueva

# Ver branches con último commit
git branch -v

# Eliminar branch
git branch -d feature-vieja
```

### Merge (Fusionar)

```bash
# Desde branch main
git checkout main

# Fusionar feature-login en main
git merge feature-login
```

**Tipos de merge**:

**Fast-forward** (simple):
```
main:    A---B---C
              \
feature:       D---E

Después:
main:    A---B---C---D---E
```

**3-way merge** (con commit de merge):
```
main:    A---B---C---F
              \     /
feature:       D---E

Después:
main:    A---B---C---F---M
              \     /   /
feature:       D---E---
```

---

## .gitignore

### ¿Para Qué?

Archivos que Git debe ignorar:
- Binarios compilados
- Archivos de configuración local
- Dependencias
- Archivos temporales

### Crear .gitignore

```bash
# Crear archivo
nano .gitignore
```

**Contenido típico para C**:
```
# Ejecutables
*.exe
*.out
a.out

# Objetos
*.o
*.so

# Editor
.vscode/
*.swp

# Sistema
.DS_Store
Thumbs.db

# Build
build/
dist/
```

**Para Python**:
```
__pycache__/
*.pyc
venv/
.env
```

---

## Recursos Adicionales

### Documentación
- [Git Official Docs](https://git-scm.com/doc)
- [Git Handbook - GitHub](https://guides.github.com/introduction/git-handbook/)
- [Pro Git Book](https://git-scm.com/book/en/v2) - Gratis online

### Tutoriales Interactivos
- [Learn Git Branching](https://learngitbranching.js.org/) - Visualización interactiva
- [Git-it](https://github.com/jlord/git-it-electron) - Tutorial desktop

### Cheat Sheets
- [GitHub Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Atlassian Git Cheat Sheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)

### Enlaces Internos
- [[02-GitHub-Colaboracion|GitHub y Colaboración]]
- [[../Ejercicios/README|Ejercicios de Git]]
- [[../Proyectos/README|Proyectos]]

---

## Autoevaluación

- [ ] ¿Entiendes la diferencia entre Git y GitHub?
- [ ] ¿Sabes crear un repositorio local?
- [ ] ¿Puedes hacer commits con mensajes descriptivos?
- [ ] ¿Entiendes staging area vs working directory?
- [ ] ¿Sabes crear y cambiar entre branches?
- [ ] ¿Puedes ver el historial de cambios?

---

## Comandos de Referencia Rápida

```bash
# Configuración
git config --global user.name "Nombre"
git config --global user.email "email@example.com"

# Crear/Clonar
git init
git clone URL

# Básicos
git status
git add archivo
git commit -m "mensaje"
git log --oneline

# Branches
git branch nombre
git checkout nombre
git merge nombre

# Ver cambios
git diff
git diff --staged
```

---

**Próximo**: [[02-GitHub-Colaboracion|GitHub y Colaboración]]

---

#git #control-versiones #fundamentos #semana4
