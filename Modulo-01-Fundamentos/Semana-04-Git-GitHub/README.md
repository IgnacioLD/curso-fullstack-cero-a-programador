# Semana 04: Git & GitHub

**Módulo 1: Fundamentos Sólidos**

---

## Bienvenida

Esta semana aprendes la herramienta más importante para cualquier desarrollador: control de versiones con Git y colaboración con GitHub.

**Duración**: 5-7 días
**Horas totales**: 6-10 horas

---

## Contenido

### Teoría
1. [[Teoria/01-Introduccion-Git|Introducción a Git]]
2. [[Teoria/02-GitHub-Colaboracion|GitHub y Colaboración]]
3. [[Teoria/Slides-Clase-04-Git-GitHub|Slides de Clase]]

### Ejercicios
[[Ejercicios/README|Guía de Ejercicios]] - Práctica con comandos Git

### Proyectos
[[Proyectos/README|Portfolio en GitHub]] - Subir proyectos anteriores

---

## Objetivos

- [ ] Configurar Git localmente
- [ ] Crear y gestionar repos
- [ ] Hacer commits efectivos
- [ ] Trabajar con branches
- [ ] Crear cuenta GitHub
- [ ] Push/pull con remotes
- [ ] Hacer Pull Requests
- [ ] Crear portfolio público

---

## Setup

### Instalar Git

**macOS**:
```bash
brew install git
# o
xcode-select --install
```

**Linux**:
```bash
sudo apt install git
```

**Windows**:
Descargar de git-scm.com

### Configurar

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

---

## Comandos Esenciales

```bash
# Local
git init
git add .
git commit -m "mensaje"
git status
git log

# Branches
git branch nombre
git checkout nombre
git merge nombre

# Remote
git clone URL
git push origin main
git pull origin main
```

---

## Evaluación

**Ejercicios (30%)**:
- Practicar comandos básicos
- Crear repos locales
- Trabajar con branches

**Proyecto (60%)**:
- Portfolio en GitHub
- READMEs profesionales
- Commits organizados

**Participación (10%)**

---

## Recursos

- [Git Official](https://git-scm.com/)
- [GitHub Docs](https://docs.github.com/)
- [Learn Git Branching](https://learngitbranching.js.org/)

---

## Próxima Semana

**Semana 5: Teoría de Hardware**

Entender cómo funciona una computadora a bajo nivel.

---

#git #github #semana4 #control-versiones
