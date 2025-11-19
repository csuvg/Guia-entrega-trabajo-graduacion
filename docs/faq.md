# ❓ Preguntas Frecuentes (FAQ)

[← Volver al inicio](../README.md)

---

## General

### ¿Cuál es la fecha límite de entrega?
La fecha límite es **[FECHA POR DEFINIR]**. El Pull Request debe estar creado antes de esta fecha. Entregas tardías no serán aceptadas.

### ¿Puedo entregar antes de la fecha límite?
Sí, puedes crear tu Pull Request cuando tengas todo listo. De hecho, es recomendable entregar con anticipación para evitar problemas de último momento.

### ¿Qué pasa si mi proyecto está incompleto?
Los proyectos que no cumplan al 100% con el [checklist](checklist.md) deberán ser corregidos. Recibirás retroalimentación en el Pull Request sobre qué necesita corrección.

---

## Repositorio y Fork

### ¿Dónde encuentro mi repositorio asignado?
Tu repositorio tiene el formato:
```
https://github.com/[profesor]/Proyecto-Graduacion-2025-[tu-carnet]
```
Si no lo encuentras, contacta a tu profesor o asesor.

### ¿Puedo cambiar el nombre del repositorio?
No. El nombre del repositorio debe mantenerse exactamente como fue asignado.

### ¿Puedo hacer mi repositorio privado?
No. El fork debe permanecer público para que puedas crear el Pull Request correctamente.

### ¿Qué hago si ya tengo un fork anterior?
Si necesitas empezar de nuevo:
1. Elimina el fork anterior desde Settings → Delete repository
2. Crea un nuevo fork desde el repositorio original

---

## Archivos y Estructura

### ¿Puedo agregar carpetas adicionales?
Sí, puedes agregar carpetas extras si tu proyecto lo requiere, pero las carpetas obligatorias (`/demo`, `/docs`, `/src`) deben existir con los archivos requeridos.

### Mi proyecto no usa package.json, ¿qué hago?
Si tu proyecto no es de Node.js, no necesitas `package.json`. Sin embargo, incluye el archivo de dependencias correspondiente a tu tecnología (requirements.txt para Python, pom.xml para Java, etc.).

### ¿Qué formato debe tener el video demo?
- **Formato**: MP4 (H.264)
- **Resolución**: Mínimo 720p
- **Duración**: 3-5 minutos
- **Tamaño**: Máximo 100 MB

### Mi video es muy grande, ¿qué puedo hacer?

**Opción 1: Comprimir el video**
- Usa [HandBrake](https://handbrake.fr/) (gratis)
- Reduce la resolución a 720p
- Ajusta el bitrate

**Opción 2: Usar Git LFS**
```bash
git lfs install
git lfs track "*.mp4"
git add .gitattributes
git add demo/demo.mp4
git commit -m "Agregar video con LFS"
```

### ¿Puedo subir el video a YouTube/Drive en lugar de al repo?
No. El video debe estar en la carpeta `/demo` del repositorio. Esto asegura que la entrega esté completa y autocontenida.

---

## Git y Pull Request

### Nunca he usado Git, ¿por dónde empiezo?
1. Instala Git: [git-scm.com/downloads](https://git-scm.com/downloads)
2. Crea una cuenta en GitHub si no tienes
3. Sigue nuestra [Guía de Git](guia-git.md) paso a paso

### ¿Cómo sé si mi Pull Request fue creado correctamente?
1. Ve al repositorio **original** (no tu fork)
2. Haz clic en la pestaña "Pull requests"
3. Deberías ver tu PR en la lista

### ¿Puedo modificar mi entrega después de crear el Pull Request?
Sí. Cualquier commit que hagas a tu fork se reflejará automáticamente en el PR existente:
```bash
git add .
git commit -m "Correcciones finales"
git push origin main
```

### ¿Puedo cerrar y crear un nuevo Pull Request?
Sí, pero no es necesario. Es mejor actualizar el PR existente con nuevos commits.

### Me aparece un conflicto en el Pull Request, ¿qué hago?
Sigue estos pasos:
```bash
# Agregar el repositorio original
git remote add upstream https://github.com/[profesor]/Proyecto-Graduacion-2025-[carnet].git

# Obtener cambios
git fetch upstream
git merge upstream/main

# Si hay conflictos, resuélvelos y luego:
git add .
git commit -m "Resolver conflictos"
git push origin main
```

### Error "Permission denied (publickey)"
Esto significa que necesitas configurar SSH o usar HTTPS:

**Opción HTTPS (más fácil):**
```bash
git clone https://github.com/[tu-usuario]/tu-repo.git
```

**Opción SSH:**
1. Genera una llave: `ssh-keygen -t ed25519 -C "tu@email.com"`
2. Agrega la llave pública a GitHub: Settings → SSH Keys

---

## README y Documentación

### ¿Qué debe contener mi README?
Ver la [plantilla completa en el Manual](manual.md#plantilla-recomendada).

Mínimo obligatorio:
- Descripción del proyecto
- Tecnologías usadas
- Instrucciones de instalación
- Instrucciones de ejecución
- Referencias al demo e informe

### ¿En qué idioma debe estar el README?
Puede estar en español o inglés, pero debe ser consistente y profesional.

### ¿El informe tiene un formato específico?
Debe incluir las secciones listadas en el [checklist](checklist.md#informe-final-pdf). El formato visual (fuentes, márgenes, etc.) queda a tu criterio, pero debe ser profesional.

---

## Variables de Entorno

### ¿Qué es el archivo .env.example?
Es un archivo de ejemplo que muestra qué variables de entorno necesita tu proyecto para funcionar, **sin incluir los valores reales**.

### ¿Puedo subir mi archivo .env real?
**No, nunca.** El archivo `.env` con credenciales reales debe estar en `.gitignore`. Solo sube `.env.example` con valores de ejemplo.

Ejemplo correcto de `.env.example`:
```env
DATABASE_URL=postgresql://user:password@localhost:5432/mydb
API_KEY=your_api_key_here
SECRET_KEY=your_secret_key_here
```

---

## Problemas Técnicos

### Git no reconoce mis comandos
Verifica que Git está instalado:
```bash
git --version
```
Si no está instalado, descárgalo de [git-scm.com](https://git-scm.com/downloads).

### No puedo hacer push (rejected)
Probablemente necesitas hacer pull primero:
```bash
git pull origin main
# Resolver conflictos si los hay
git push origin main
```

### Mi terminal dice "fatal: not a git repository"
Asegúrate de estar en la carpeta correcta del proyecto:
```bash
cd ruta/a/tu/Proyecto-Graduacion-2025-[carnet]
```

### GitHub dice que mi archivo es muy grande
GitHub tiene un límite de 100 MB por archivo. Para archivos grandes usa Git LFS:
```bash
git lfs install
git lfs track "*.mp4"
git add .gitattributes
```

---

## Contacto y Soporte

### ¿A quién contacto si tengo problemas?
1. **Problemas técnicos con Git**: Revisa esta FAQ y la [Guía de Git](guia-git.md)
2. **Dudas sobre el contenido**: Contacta a tu asesor
3. **Problemas con el repositorio**: Contacta a tu profesor

### ¿Hay algún canal de comunicación?
[Agregar información de contacto, Slack, Discord, email, etc.]

---

## ¿No encontraste tu pregunta?

Contacta a tu asesor o profesor con:
- Descripción clara del problema
- Capturas de pantalla si aplica
- Mensajes de error completos

---

[← Guía Git](guia-git.md) | [Volver al inicio](../README.md)