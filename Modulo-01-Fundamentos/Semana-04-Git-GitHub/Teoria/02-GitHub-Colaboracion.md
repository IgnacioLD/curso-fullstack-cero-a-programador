# GitHub y Colaboración

> **Trabajo en equipo con Git**

---

## Índice

- [[#¿Qué es GitHub?]]
- [[#Crear Cuenta y Configurar]]
- [[#Repositorios Remotos]]
- [[#Pull Requests]]
- [[#Issues]]
- [[#Colaboración en Equipo]]
- [[#GitHub Pages]]

---

## ¿Qué es GitHub?

**GitHub** es una plataforma web que:
- Aloja repositorios Git
- Facilita colaboración
- Proporciona herramientas de gestión de proyectos
- Funciona como portfolio para desarrolladores

**Alternativas**:
- GitLab
- Bitbucket
- Gitea (self-hosted)

---

## Crear Cuenta y Configurar

### Registro

1. Ve a [github.com](https://github.com)
2. Click "Sign up"
3. Elige username (será tu URL: github.com/username)
4. Email y contraseña
5. Verificar email

### SSH Keys (Recomendado)

**¿Por qué SSH?**
- No pedir contraseña cada vez
- Más seguro que HTTPS
- Estándar en la industria

**Generar clave**:
```bash
# Generar par de claves
ssh-keygen -t ed25519 -C "tu@email.com"

# Enter para ubicación default
# Enter para sin passphrase (o pon una)

# Ver clave pública
cat ~/.ssh/id_ed25519.pub
```

**Añadir a GitHub**:
1. GitHub → Settings → SSH and GPG keys
2. New SSH key
3. Copiar contenido de `id_ed25519.pub`
4. Pegar y guardar

**Probar**:
```bash
ssh -T git@github.com
# Should see: Hi username! You've successfully authenticated...
```

---

## Repositorios Remotos

### Crear Repositorio en GitHub

**Desde web**:
1. Click "+" → New repository
2. Nombre del repo
3. Descripción (opcional)
4. Public o Private
5. NO inicializar con README (si ya tienes código local)
6. Create repository

### Conectar Repo Local con GitHub

**Opción 1: Repo local existente**:
```bash
# En tu proyecto local
git remote add origin git@github.com:usuario/repo.git

# Verificar
git remote -v

# Subir por primera vez
git push -u origin main
```

**Opción 2: Clonar de GitHub**:
```bash
git clone git@github.com:usuario/repo.git
cd repo
# Listo para trabajar
```

### Comandos Remote

```bash
# Ver remotos
git remote -v

# Añadir remoto
git remote add nombre URL

# Cambiar URL de remoto
git remote set-url origin NUEVA_URL

# Eliminar remoto
git remote remove nombre
```

---

## Push y Pull

### Push (Subir cambios)

```bash
# Primera vez (establece upstream)
git push -u origin main

# Después solo
git push

# Forzar (cuidado)
git push --force
```

### Pull (Descargar cambios)

```bash
# Descargar y fusionar cambios
git pull

# Equivale a:
git fetch  # Descargar
git merge  # Fusionar
```

### Fetch (Solo descargar)

```bash
# Descargar sin fusionar
git fetch origin

# Ver ramas remotas
git branch -r
```

---

## Workflow con GitHub

### Flujo Típico

```bash
# 1. Clonar o pull para estar actualizado
git pull

# 2. Crear branch para feature
git checkout -b feature/nueva-funcionalidad

# 3. Hacer cambios y commits
git add .
git commit -m "Implementé nueva funcionalidad"

# 4. Subir branch a GitHub
git push -u origin feature/nueva-funcionalidad

# 5. Crear Pull Request en GitHub

# 6. Después de aprobación, fusionar en main

# 7. Actualizar local
git checkout main
git pull

# 8. Eliminar branch local
git branch -d feature/nueva-funcionalidad
```

---

## Pull Requests (PRs)

### ¿Qué es un PR?

**Definición**: Propuesta de cambios que otros pueden revisar antes de fusionar

**Workflow**:
1. Creas branch
2. Haces cambios
3. Subes branch a GitHub
4. Abres Pull Request
5. Otros revisan código
6. Haces ajustes si necesario
7. Se aprueba y fusiona

### Crear PR

**Desde GitHub**:
1. Push tu branch
2. GitHub mostrará "Compare & pull request"
3. O: Pull requests → New pull request
4. Selecciona base (main) y compare (tu-branch)
5. Título y descripción
6. Create pull request

**Buena descripción de PR**:
```markdown
## ¿Qué hace este PR?
Añade validación de email en el formulario de registro

## ¿Por qué es necesario?
Usuarios podían registrarse con emails inválidos

## ¿Cómo se probó?
- Probé con emails válidos e inválidos
- Todos los tests pasan

## Capturas de pantalla
[si aplica]
```

### Code Review

**Revisar PR de otro**:
1. Ve al PR en GitHub
2. Tab "Files changed"
3. Hover sobre línea → click "+"
4. Comentar
5. Submit review: Approve / Request changes / Comment

**Responder a comentarios**:
1. Hacer cambios en tu branch local
2. Commit y push
3. PR se actualiza automáticamente

---

## Issues

### ¿Qué son?

**Issues** = Sistema de tracking de tareas, bugs, mejoras

**Usar para**:
- Reportar bugs
- Proponer features
- Hacer preguntas
- Organizar trabajo

### Crear Issue

1. Tab "Issues" → New issue
2. Título descriptivo
3. Descripción con detalles
4. Labels (bug, enhancement, etc.)
5. Assign a persona
6. Submit

**Buen issue de bug**:
```markdown
## Descripción
El botón de submit no funciona en Safari

## Pasos para reproducir
1. Abrir página en Safari
2. Llenar formulario
3. Click en Submit
4. No pasa nada

## Comportamiento esperado
Debería enviar el formulario

## Screenshots
[captura]

## Entorno
- OS: macOS 14.0
- Browser: Safari 17
```

### Cerrar Issues

**Desde commit**:
```bash
git commit -m "Corregí validación. Closes #42"
```

**Desde PR**:
```markdown
Este PR cierra #42 y #43
```

---

## Colaboración en Equipo

### Roles

**Owner**: Creador del repo, control total
**Collaborator**: Acceso push directo
**Contributor**: Puede hacer PRs, no push directo

### Añadir Colaboradores

1. Repo → Settings → Collaborators
2. Add people
3. Buscar por username
4. Invitar

### Forking

**Fork** = Copia de un repo a tu cuenta

**Workflow de contribución**:
```bash
# 1. Fork en GitHub (botón Fork)

# 2. Clonar TU fork
git clone git@github.com:tu-usuario/repo.git

# 3. Añadir upstream (repo original)
git remote add upstream git@github.com:original/repo.git

# 4. Crear branch
git checkout -b fix-bug

# 5. Hacer cambios y commit
git commit -m "Corregí bug X"

# 6. Push a TU fork
git push origin fix-bug

# 7. Abrir PR desde TU fork al repo original
```

**Mantener fork actualizado**:
```bash
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

---

## README.md

### Importancia

**README** = Primera impresión de tu proyecto

**Debe incluir**:
- Qué hace el proyecto
- Cómo instalarlo
- Cómo usarlo
- Cómo contribuir
- Licencia

### Template Básico

```markdown
# Nombre del Proyecto

Breve descripción de qué hace

## Instalación

```bash
git clone https://github.com/usuario/proyecto.git
cd proyecto
make
```

## Uso

```bash
./programa argumentos
```

## Características

- Feature 1
- Feature 2
- Feature 3

## Contribuir

1. Fork el proyecto
2. Crea tu branch (`git checkout -b feature/nueva`)
3. Commit cambios (`git commit -m 'Añadí feature'`)
4. Push al branch (`git push origin feature/nueva`)
5. Abre Pull Request

## Licencia

MIT License - ver archivo LICENSE
```

---

## GitHub Pages

### ¿Qué es?

Hosting gratis de sitios estáticos desde tu repo

**Usos**:
- Portfolio personal
- Documentación de proyecto
- Landing page

### Activar

1. Repo → Settings → Pages
2. Source: main branch
3. Save
4. Sitio disponible en: `username.github.io/repo`

**Para sitio personal** (`username.github.io`):
1. Crear repo con nombre EXACTO: `username.github.io`
2. Push `index.html`
3. Visita `https://username.github.io`

---

## .github Folder

### Workflows Comunes

**Pull Request Template**:
```
.github/pull_request_template.md
```

**Issue Templates**:
```
.github/ISSUE_TEMPLATE/
├── bug_report.md
└── feature_request.md
```

**GitHub Actions** (CI/CD):
```
.github/workflows/
└── tests.yml
```

---

## Buenas Prácticas

### Commits

- Mensajes descriptivos
- Commits atómicos (un cambio lógico)
- Present tense: "Add feature" no "Added feature"

### Branches

- Nombres descriptivos: `feature/login`, `fix/bug-123`
- Mantén main siempre funcional
- Borra branches después de merge

### Pull Requests

- Un PR = una feature/fix
- Descripción clara
- Tests pasan antes de PR
- Responde a comentarios rápido

### Issues

- Busca duplicados antes de crear
- Sé específico
- Incluye pasos para reproducir (bugs)

---

## Recursos

### Documentación
- [GitHub Docs](https://docs.github.com/)
- [GitHub Skills](https://skills.github.com/) - Tutoriales interactivos
- [GitHub Guides](https://guides.github.com/)

### Learning
- [Lab GitHub](https://lab.github.com/)
- [First Contributions](https://github.com/firstcontributions/first-contributions)

### Enlaces Internos
- [[01-Introduccion-Git|Introducción a Git]]
- [[../Ejercicios/README|Ejercicios]]
- [[../Proyectos/README|Proyectos]]

---

## Checklist de Proyecto GitHub

Para cada proyecto:

- [ ] README.md completo
- [ ] .gitignore apropiado
- [ ] LICENSE file
- [ ] Descripción y tags en repo
- [ ] Al menos 1 release/tag
- [ ] Issues para TODOs
- [ ] Commits con mensajes claros
- [ ] Branches con nombres descriptivos

---

#github #colaboracion #pull-requests #open-source
