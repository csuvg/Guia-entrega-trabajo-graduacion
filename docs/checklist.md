# ✅ Checklist de Entrega

[← Volver al inicio](../README.md)

---

## Instrucciones

Este checklist **debe completarse al 100%** antes de crear el Pull Request. Cualquier proyecto que no cumpla con todos los puntos deberá corregirse antes de ser aceptado.

> 💡 **Tip**: Usa este checklist como guía final antes de entregar. Marca cada elemento conforme lo vayas verificando.

---

## 1. Estructura de Carpetas

### Carpeta `/capturas`
- [ ] La carpeta `/capturas` existe en la raíz del repositorio
- [ ] Contiene **al menos 10 capturas de pantalla** del software
- [ ] Las capturas están en formato JPG o PNG
- [ ] Las capturas son legibles y a buena resolución
- [ ] Las capturas muestran las funcionalidades principales del sistema
- [ ] Los archivos están numerados de forma consecutiva (`captura-01`, `captura-02`, ...)

### Carpeta `/demo`
- [ ] La carpeta `/demo` existe en la raíz del repositorio
- [ ] El archivo `demo.mp4` está presente dentro de `/demo`
- [ ] El video es reproducible y no está corrupto
- [ ] La duración del video es apropiada (3-5 minutos)

### Carpeta `/docs`
- [ ] La carpeta `/docs` existe en la raíz del repositorio
- [ ] El archivo `informe_final.pdf` está presente dentro de `/docs`
- [ ] El PDF es legible y no está protegido con contraseña
- [ ] El informe contiene todas las secciones requeridas
- [ ] ⚠️ El archivo `consentimiento_firmado.pdf` está presente dentro de `/docs` (**OBLIGATORIO**)
- [ ] El consentimiento está **firmado** y la firma es claramente visible
- [ ] El consentimiento es legible y no está protegido con contraseña

### Carpeta `/src`
- [ ] La carpeta `/src` existe en la raíz del repositorio
- [ ] El archivo `.env.example` está presente con las variables necesarias
- [ ] El archivo `.env.example` **NO contiene** credenciales reales
- [ ] El archivo `package.json` está presente (si aplica)
- [ ] Todo el código fuente está dentro de `/src`
- [ ] No hay archivos sensibles expuestos (.env real, credenciales, etc.)

---

## 2. Archivo README.md

### Ubicación y formato
- [ ] El archivo `README.md` está en la raíz del repositorio
- [ ] El archivo está en formato Markdown válido
- [ ] Se visualiza correctamente en GitHub

### Contenido obligatorio
- [ ] Contiene una descripción clara del proyecto
- [ ] Lista las tecnologías utilizadas
- [ ] Especifica los requisitos previos (software necesario)
- [ ] Incluye instrucciones de instalación paso a paso
- [ ] Las instrucciones de instalación son reproducibles
- [ ] Incluye instrucciones de ejecución
- [ ] Referencia las capturas en `/capturas` (mínimo 10)
- [ ] Referencia el video demo en `/demo/demo.mp4`
- [ ] Referencia el informe final en `/docs/informe_final.pdf`
- [ ] Referencia el consentimiento firmado en `/docs/consentimiento_firmado.pdf`
- [ ] Incluye información del autor(es) y carnet

### Calidad
- [ ] Los enlaces internos funcionan correctamente
- [ ] No hay errores ortográficos graves
- [ ] El formato es consistente y legible

---

## 3. Video Demo

### Aspectos técnicos
- [ ] Formato: MP4
- [ ] Resolución mínima: 720p
- [ ] Tamaño: menor a 100 MB
- [ ] Audio claro y audible

### Contenido
- [ ] Introducción del proyecto
- [ ] Demostración de funcionalidades principales
- [ ] Se muestran casos de uso reales
- [ ] Conclusión o cierre

---

## 4. Informe Final (PDF)

### Formato
- [ ] Archivo en formato PDF
- [ ] Legible en cualquier visor de PDF
- [ ] Sin restricciones de acceso

### Secciones requeridas
- [ ] Portada con título, autores y fecha
- [ ] Índice o tabla de contenidos
- [ ] Resumen ejecutivo
- [ ] Introducción y objetivos
- [ ] Marco teórico o antecedentes
- [ ] Metodología
- [ ] Desarrollo y resultados
- [ ] Conclusiones
- [ ] Referencias bibliográficas

---

## 5. Consentimiento de Uso de Foto y Video ⚠️ OBLIGATORIO

- [ ] Descargaste la plantilla del consentimiento provista en la guía
- [ ] El documento está **firmado** (firma visible)
- [ ] El archivo se llama `consentimiento_firmado.pdf`
- [ ] Está ubicado en la carpeta `/docs`
- [ ] El PDF es legible y no está protegido con contraseña

> ⚠️ **Sin este documento firmado la entrega NO será aceptada.**

---

## 6. Repositorio Git

### Configuración
- [ ] El repositorio es un fork del repositorio asignado
- [ ] El branch principal tiene todos los archivos
- [ ] El archivo `.gitignore` está configurado correctamente

### Archivos excluidos (NO deben estar en el repo)
- [ ] `node_modules/` no está en el repositorio
- [ ] `.env` (con credenciales reales) no está en el repositorio
- [ ] Archivos de caché o temporales no están incluidos
- [ ] Archivos de IDE (.idea, .vscode) no están incluidos

### Commits
- [ ] Los mensajes de commit son descriptivos
- [ ] El historial de commits es limpio

---

## 7. Pull Request

- [ ] El Pull Request está creado hacia el repositorio original
- [ ] El título del PR es descriptivo
- [ ] La descripción incluye información relevante
- [ ] El PR fue creado **antes** de la fecha límite

---

## Resumen de Verificación

| Sección | Elementos | Completado |
|---------|-----------|------------|
| Estructura de Carpetas | 23 | [ ] |
| README.md | 16 | [ ] |
| Video Demo | 8 | [ ] |
| Informe Final | 12 | [ ] |
| Consentimiento firmado | 5 | [ ] |
| Repositorio Git | 9 | [ ] |
| Pull Request | 4 | [ ] |
| **TOTAL** | **77** | [ ] |

---

## ⚠️ Importante

- **No se aceptarán entregas parciales**
- Todos los elementos deben estar completos
- Si tienes dudas, consulta el [Manual de Instrucciones](manual.md)
- Para problemas con Git, revisa la [Guía de Git](guia-git.md)

---

## ¿Todo listo?

Si completaste todos los puntos de este checklist, estás listo para crear tu Pull Request. Sigue los pasos en la [Guía de Git y Pull Request](guia-git.md).

---

[← Manual](manual.md) | [Volver al inicio](../README.md) | [Guía Git →](guia-git.md)