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
PG-2025-[carnet]
```

**Ejemplo:** Para un estudiante con carnet `12345`, el repositorio asignado sería:
```
PG-2025-12345
```

Este nombre no puede modificarse. El estudiante debe realizar un fork de este repositorio y trabajar sobre esa copia, manteniendo siempre el nombre original.

---

## 1. Estructura de Carpetas del Proyecto

El proyecto **debe** seguir exactamente esta estructura:

```
/Proyecto-Graduacion-2025-[carnet]
│
├── /demo
│   └── demo.mp4                 # Video demostrativo del proyecto
│
├── /docs
│   └── informe_final.pdf        # Informe final del equipo
│
├── /src
│   ├── .env.example             # Ejemplo de variables de entorno
│   ├── package.json             # Dependencias del proyecto
│   └── [archivos de código]     # Código fuente
│
└── README.md                    # Descripción del proyecto
```

### Descripción de cada carpeta

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

## Demo
El video demostrativo se encuentra en [`/demo/demo.mp4`](demo/demo.mp4)

## Documentación
El informe final del proyecto está disponible en [`/docs/informe_final.pdf`](docs/informe_final.pdf)

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
| Demo | Sí | Referencia al video en `/demo/demo.mp4` |
| Documentación | Sí | Enlace al informe en `/docs/informe_final.pdf` |
| Tecnologías | Sí | Lista de herramientas y frameworks utilizados |
| Requisitos previos | Sí | Software necesario para ejecutar el proyecto |

---

## 3. Especificaciones de los Archivos

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