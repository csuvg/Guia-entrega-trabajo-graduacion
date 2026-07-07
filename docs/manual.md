# Manual de Instrucciones para Entrega de Proyectos

[← Volver al inicio](../README.md)

---

## Introducción

Este manual contiene las instrucciones para la correcta entrega del proyecto de graduación. Se detallan la estructura de carpetas requerida, el formato del archivo README y las especificaciones técnicas de cada entregable.

Es fundamental seguir cada indicación para asegurar que la entrega sea aceptada sin observaciones.

---

## 0. Convención de Nombres

Cada estudiante tiene asignado un repositorio con un nombre único basado en su número de carnet. El formato es el siguiente:
```
PG-2026-[carnet]
```

**Ejemplo:** Para un estudiante con carnet `12345`, el repositorio asignado sería:
```
PG-2026-12345
```

Este nombre no puede modificarse. El estudiante debe realizar un fork de este repositorio y trabajar sobre esa copia, manteniendo siempre el nombre original.

---

## 1. Estructura de Carpetas del Proyecto

El proyecto **debe** seguir exactamente esta estructura:

```
/PG-2026-[carnet]
│
├── /capturas
│   ├── captura-01.jpg           # Captura del sistema 1
│   ├── captura-02.jpg           # Captura del sistema 2
│   ├── ...                      # (mínimo 10 capturas)
│   └── captura-10.jpg           # Captura del sistema 10
│
├── /demo
│   └── demo.mp4                 # Video demostrativo del proyecto
│
├── /docs
│   ├── informe_final.pdf        # Informe final del equipo
│   └── consentimiento_firmado.pdf  # Consentimiento de uso de foto y video FIRMADO (OBLIGATORIO)
│
├── /src
│   ├── .env.example             # Ejemplo de variables de entorno
│   ├── package.json             # Dependencias del proyecto
│   └── [archivos de código]     # Código fuente
│
└── README.md                    # Descripción del proyecto
```

### Descripción de cada carpeta

#### `/capturas`
Contiene las capturas de pantalla del software en funcionamiento.

- **Archivos**: `captura-01.jpg`, `captura-02.jpg`, ... (numeradas de forma consecutiva)
- **Cantidad**: **mínimo 10 capturas**
- **Contenido**: Deben mostrar las pantallas y funcionalidades principales del sistema (login, vistas clave, flujos de uso, resultados, etc.)
- **Formato**: JPG o PNG, legibles y a buena resolución

#### `/demo`
Contiene el video demostrativo del proyecto.

- **Archivo**: `demo.mp4`
- **Duración recomendada**: 3-5 minutos
- **Contenido**: Demostración funcional del proyecto en ejecución
- **Formato**: MP4 (H.264 recomendado para compatibilidad)

#### `/docs`
Contiene la documentación formal del proyecto.

- **Archivo**: `informe_final.pdf`
- **Contenido**: Resumen ejecutivo, objetivos, metodología, resultados y conclusiones
- **Formato**: PDF (debe ser legible y no estar protegido)

- **Archivo**: `consentimiento_firmado.pdf` — ⚠️ **OBLIGATORIO**
- **Contenido**: El documento [Consentimiento de Uso de Foto y Video](Consentimiento-Uso-de-foto-y-Video.pdf) **firmado** por el estudiante
- **Formato**: PDF legible con la firma visible
- **Nota**: Descarga la plantilla del consentimiento, fírmala (a mano o de forma digital) y sube el PDF firmado a esta carpeta. **Sin este documento firmado la entrega NO será aceptada.**

#### `/src`
Contiene todo el código fuente del proyecto.

- **`.env.example`**: Archivo de ejemplo con las variables de entorno necesarias. **No incluir credenciales reales**, solo los nombres de las variables.
  
  ```env
  DATABASE_URL=url_de_base_de_datos
  API_KEY=api_key
  SECRET_KEY=secret_key
  ```

- **`package.json`**: Si el proyecto usa Node.js, incluir este archivo con todas las dependencias.

- **Código fuente**: Todos los archivos necesarios para ejecutar el proyecto.

---

## 2. Formato del archivo README.md

El archivo `README.md` es la carta de presentación del proyecto. Debe estar en la **raíz del repositorio** y contener las siguientes secciones:

### Plantilla recomendada

```markdown
# [Nombre del Proyecto]

## Descripción
[Breve descripción del proyecto: qué problema resuelve y cómo funciona]

## Tecnologías Utilizadas
- [Tecnología 1]
- [Tecnología 2]
- [Tecnología 3]

## Requisitos Previos
- [Requisito 1, ej: Node.js v18+]
- [Requisito 2, ej: PostgreSQL 14+]

## Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/usuario/repositorio.git
   cd repositorio
   ```

2. Instalar dependencias:
   ```bash
   npm install
   ```

3. Configurar variables de entorno:
   ```bash
   cp src/.env.example src/.env
   # Editar .env con las configuraciones correspondientes
   ```

4. Ejecutar el proyecto:
   ```bash
   npm start
   ```

## Capturas
Las capturas de pantalla del sistema se encuentran en [`/capturas`](capturas/) (mínimo 10)

## Demo
El video demostrativo se encuentra en [`/demo/demo.mp4`](demo/demo.mp4)

## Documentación
El informe final del proyecto está disponible en [`/docs/informe_final.pdf`](docs/informe_final.pdf)

El consentimiento de uso de foto y video firmado se encuentra en [`/docs/consentimiento_firmado.pdf`](docs/consentimiento_firmado.pdf)

## Autores
- [Nombre del estudiante] - [Carnet]

## Licencia
[Tipo de licencia, ej: MIT]
```

### Requisitos del README

| Elemento | Obligatorio | Descripción |
|----------|-------------|-------------|
| Descripción | Sí | Explicación clara del propósito del proyecto |
| Instalación | Sí | Pasos detallados para configurar y ejecutar |
| Capturas | Sí | Referencia a las capturas en `/capturas` (mínimo 10) |
| Demo | Sí | Referencia al video en `/demo/demo.mp4` |
| Documentación | Sí | Enlace al informe en `/docs/informe_final.pdf` |
| Consentimiento firmado | Sí | Enlace al consentimiento firmado en `/docs/consentimiento_firmado.pdf` |
| Tecnologías | Sí | Lista de herramientas y frameworks utilizados |
| Requisitos previos | Sí | Software necesario para ejecutar el proyecto |

---

## 3. Especificaciones de los Archivos

### Capturas de Pantalla (`/capturas`)

| Aspecto | Especificación |
|---------|----------------|
| Cantidad | **Mínimo 10 capturas** |
| Formato | JPG o PNG |
| Nombres | `captura-01`, `captura-02`, ... (consecutivos) |
| Resolución | Legibles, sin recortes que oculten información relevante |
| Contenido | Pantallas y funcionalidades principales del sistema |

**Recomendaciones para las capturas:**
1. Mostrar las vistas más importantes del sistema
2. Incluir los flujos de uso principales (registro, inicio de sesión, operaciones clave)
3. Evitar exponer datos sensibles o credenciales reales
4. Numerarlas en el orden lógico de uso del sistema

### Video Demo (`demo.mp4`)

| Aspecto | Especificación |
|---------|----------------|
| Formato | MP4 (codec H.264) |
| Duración | 3-5 minutos |
| Resolución | Mínimo 720p (1280x720) |
| Tamaño máximo | 100 MB |
| Audio | Incluir narración explicativa |

**Contenido del video:**
1. Introducción breve del proyecto
2. Demostración de las funcionalidades principales
3. Casos de uso en acción
4. Conclusión

### Informe Final (`informe_final.pdf`)

El informe debe incluir:
- Portada con información del proyecto y autores
- Índice
- Resumen ejecutivo
- Introducción y objetivos
- Marco teórico
- Metodología
- Desarrollo y resultados
- Conclusiones
- Referencias bibliográficas
- Anexos (si aplica)

### Consentimiento de Uso de Foto y Video (`consentimiento_firmado.pdf`) — ⚠️ OBLIGATORIO

Este documento es de **entrega obligatoria**. La entrega **no será aceptada** si falta o no está firmado.

| Aspecto | Especificación |
|---------|----------------|
| Origen | Plantilla [`Consentimiento-Uso-de-foto-y-Video.pdf`](Consentimiento-Uso-de-foto-y-Video.pdf) provista en esta guía |
| Firma | **Obligatoria** (a mano o digital), claramente visible |
| Formato | PDF legible, sin protección de contraseña |
| Ubicación | `/docs/consentimiento_firmado.pdf` en tu repositorio |

**Pasos:**
1. Descarga la plantilla del consentimiento desde esta guía
2. Complétala con tus datos y **fírmala**
3. Guarda el PDF firmado como `consentimiento_firmado.pdf`
4. Súbelo a la carpeta `/docs` de tu repositorio

---

## 4. Buenas Prácticas

### Código
- Código limpio y bien comentado
- Nombres de variables descriptivos
- Sin credenciales hardcodeadas
- `.gitignore` configurado correctamente

### Repositorio
- Commits descriptivos
- Sin archivos innecesarios (node_modules, .env, etc.)
- Estructura de carpetas respetada

### Documentación
- README claro y completo
- Instrucciones reproducibles
- Enlaces funcionando correctamente

---

## Siguiente Paso

Una vez estructurado el proyecto correctamente, verificar que todo esté en orden usando el [Checklist de Entrega](checklist.md).

---

[← Volver al inicio](../README.md) | [Checklist →](checklist.md)