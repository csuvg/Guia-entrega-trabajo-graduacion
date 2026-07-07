# 🔀 Guía de Git y Pull Request

[← Volver al inicio](../README.md)

---

## Introducción

Esta guía te llevará paso a paso por el proceso de fork, clonación, commits y creación del Pull Request para entregar tu proyecto de graduación.

---

## Paso 1: Hacer Fork del Repositorio

El fork crea una copia del repositorio asignado en tu cuenta personal de GitHub.

### Instrucciones

1. **Accede al repositorio asignado**
   
   Tu repositorio tiene el formato:
   ```
   https://github.com/[profesor]/PG-2026-[tu-carnet]
   ```

2. **Haz clic en "Fork"**
   
   Busca el botón **Fork** en la esquina superior derecha de la página.

   ![Fork Button](https://docs.github.com/assets/images/help/repository/fork_button.png)

3. **Confirma la creación**
   
   GitHub creará una copia en tu cuenta:
   ```
   https://github.com/[tu-usuario]/PG-2026-[tu-carnet]
   ```

---

## Paso 2: Clonar tu Fork

Descarga el repositorio a tu computadora para trabajar localmente.

### Usando HTTPS

```bash
git clone https://github.com/[tu-usuario]/PG-2026-[tu-carnet].git
cd PG-2026-[tu-carnet]
```

### Usando SSH (si tienes llaves configuradas)

```bash
git clone git@github.com:[tu-usuario]/PG-2026-[tu-carnet].git
cd PG-2026-[tu-carnet]
```

---

## Paso 3: Crear la Estructura del Proyecto

Crea las carpetas requeridas:

```bash
# Crear estructura de carpetas
mkdir -p capturas demo docs src

# Verificar estructura
ls -la
```

Tu estructura debe verse así:
```
PG-2026-[carnet]/
├── capturas/
├── demo/
├── docs/
├── src/
└── README.md
```

---

## Paso 4: Agregar tus Archivos

### Copiar archivos a las carpetas correspondientes

```bash
# Copiar capturas de pantalla (mínimo 10)
cp /ruta/a/tus/capturas/*.jpg capturas/

# Copiar video demo
cp /ruta/a/tu/demo.mp4 demo/

# Copiar informe
cp /ruta/a/tu/informe_final.pdf docs/

# Copiar consentimiento FIRMADO (OBLIGATORIO)
cp /ruta/a/tu/consentimiento_firmado.pdf docs/

# Copiar código fuente
cp -r /ruta/a/tu/codigo/* src/
```

> ⚠️ **OBLIGATORIO**: El archivo `consentimiento_firmado.pdf` es el documento *Consentimiento de Uso de Foto y Video* **firmado**. Descarga la plantilla desde la guía, fírmala y súbela a `/docs`. **Sin este documento firmado la entrega NO será aceptada.**

### Crear archivo .env.example

```bash
# Crear archivo de ejemplo de variables de entorno
cat > src/.env.example << EOF
# Database
DATABASE_URL=your_database_url

# API Keys
API_KEY=your_api_key
SECRET_KEY=your_secret_key

# Other configs
PORT=3000
EOF
```

### Crear/Editar README.md

Crea tu README.md en la raíz del proyecto siguiendo la [plantilla del manual](manual.md#plantilla-recomendada).

---

## Paso 5: Configurar .gitignore

Crea un archivo `.gitignore` para excluir archivos innecesarios:

```bash
cat > .gitignore << EOF
# Dependencies
node_modules/
vendor/
__pycache__/
*.pyc

# Environment
.env
.env.local
.env.*.local

# IDE
.idea/
.vscode/
*.swp
*.swo

# OS
.DS_Store
Thumbs.db

# Build
dist/
build/
*.log

# Temporary
tmp/
temp/
EOF
```

---

## Paso 6: Hacer Commits

### Ver estado de los archivos

```bash
git status
```

### Agregar archivos al staging

```bash
# Agregar todos los archivos
git add .

# O agregar archivos específicos
git add README.md
git add capturas/
git add demo/demo.mp4
git add docs/informe_final.pdf
git add docs/consentimiento_firmado.pdf
git add src/
```

### Crear commits

Es recomendable hacer commits organizados:

```bash
# Commit de estructura inicial
git add README.md .gitignore
git commit -m "Agregar README y configuración inicial"

# Commit de documentación
git add docs/informe_final.pdf
git commit -m "Agregar informe final del proyecto"

# Commit del consentimiento firmado (OBLIGATORIO)
git add docs/consentimiento_firmado.pdf
git commit -m "Agregar consentimiento de uso de foto y video firmado"

# Commit de capturas
git add capturas/
git commit -m "Agregar capturas de pantalla del sistema"

# Commit de demo
git add demo/demo.mp4
git commit -m "Agregar video demostrativo"

# Commit de código fuente
git add src/
git commit -m "Agregar código fuente del proyecto"
```

### Commits atómicos (alternativa rápida)

Si prefieres un solo commit:

```bash
git add .
git commit -m "Entrega final del proyecto de graduación"
```

---

## Paso 7: Subir Cambios (Push)

Envía tus commits a tu fork en GitHub:

```bash
git push origin main
```

> **Nota**: Si tu branch principal se llama `master`, usa:
> ```bash
> git push origin master
> ```

### Si es tu primer push

Puede que necesites configurar el upstream:

```bash
git push -u origin main
```

---

## Paso 8: Crear Pull Request

El Pull Request es la forma oficial de entregar tu proyecto.

### Instrucciones

1. **Ve a tu fork en GitHub**
   ```
   https://github.com/[tu-usuario]/PG-2026-[tu-carnet]
   ```

2. **Haz clic en "Contribute"** y luego **"Open pull request"**
   
   O ve directamente a la pestaña **Pull requests** → **New pull request**

3. **Verifica la dirección del PR**
   
   - **Base repository**: `[profesor]/PG-2026-[tu-carnet]` (el original)
   - **Base branch**: `main`
   - **Head repository**: `[tu-usuario]/PG-2026-[tu-carnet]` (tu fork)
   - **Compare branch**: `main`

4. **Completa el formulario**
   
   **Título**:
   ```
   Entrega Final - [Tu Nombre] - [Carnet]
   ```
   
   **Descripción**:
   ```markdown
   ## Entrega de Proyecto de Graduación
   
   - **Estudiante**: [Tu nombre completo]
   - **Carnet**: [Tu carnet]
   - **Proyecto**: [Nombre del proyecto]
   
   ### Contenido incluido
   - [x] Capturas de pantalla (capturas/ — mínimo 10)
   - [x] Video demo (demo/demo.mp4)
   - [x] Informe final (docs/informe_final.pdf)
   - [x] Consentimiento de uso de foto y video FIRMADO (docs/consentimiento_firmado.pdf)
   - [x] Código fuente (src/)
   - [x] README.md con instrucciones
   
   ### Checklist completado
   He verificado todos los puntos del checklist de entrega.
   ```

5. **Haz clic en "Create pull request"**

---

## Verificar tu Pull Request

Después de crear el PR:

1. **Confirma que aparece** en el repositorio original
2. **Revisa los archivos** en la pestaña "Files changed"
3. **Verifica que no haya conflictos**

---

## Solución de Problemas Comunes

### Error: "Permission denied"

```bash
# Verificar configuración de git
git config --list

# Configurar usuario si es necesario
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

### Error: "Repository not found"

Verifica que:
- El URL del repositorio es correcto
- Ya hiciste fork del repositorio
- Estás usando tu usuario en el URL

### Archivos muy grandes

Si `demo.mp4` es muy grande (>100MB), considera:
- Comprimir el video
- Usar [Git LFS](https://git-lfs.github.com/)

```bash
# Instalar Git LFS
git lfs install
git lfs track "*.mp4"
git add .gitattributes
```

### Conflictos en el Pull Request

Si hay conflictos:

```bash
# Agregar el repositorio original como upstream
git remote add upstream https://github.com/[profesor]/PG-2026-[tu-carnet].git

# Obtener cambios
git fetch upstream

# Merge con main del upstream
git merge upstream/main

# Resolver conflictos manualmente, luego:
git add .
git commit -m "Resolver conflictos"
git push origin main
```

---

## Resumen de Comandos

```bash
# 1. Clonar
git clone https://github.com/[tu-usuario]/PG-2026-[carnet].git
cd PG-2026-[carnet]

# 2. Crear estructura
mkdir -p demo docs src

# 3. Agregar archivos
# (copiar tus archivos a las carpetas)

# 4. Commit
git add .
git commit -m "Entrega final del proyecto"

# 5. Push
git push origin main

# 6. Crear Pull Request en GitHub (interfaz web)
```

---

## ¿Necesitas más ayuda?

- [Documentación oficial de Git](https://git-scm.com/doc)
- [GitHub Docs - Forking](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
- [GitHub Docs - Pull Requests](https://docs.github.com/en/pull-requests)

---

[← Checklist](checklist.md) | [Volver al inicio](../README.md) | [FAQ →](faq.md)