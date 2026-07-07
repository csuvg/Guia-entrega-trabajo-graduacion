# Proyecto de Graduación 2026

Este documento es la guía oficial para la entrega de proyectos de graduación del ciclo 2026. Aquí se listan los requisitos, la estructura esperada y los pasos necesarios para completar la entrega obligatoria para optar al título.

Es importante revisar cada sección con atención y verificar que el proyecto cumpla con todos los puntos indicados. Los proyectos que no cumplan con los requisitos deberán ser corregidos antes de ser aceptados.

---

## Proceso de Entrega

El proceso de entrega consta de cuatro pasos:

1. Realizar un **Fork** del repositorio asignado según el número de carnet
2. Estructurar el proyecto siguiendo el formato establecido en esta guía
3. Cargar todos los archivos requeridos en el repositorio
4. Crear un **Pull Request** para formalizar la entrega
5. Esperar que se haga el merge al branch.

---

## Documentación Disponible

| Documento | Descripción |
|-----------|-------------|
| [📖 Manual de Instrucciones](docs/manual.md) | Guía completa con la estructura de carpetas y formato del README |
| [✅ Checklist de Entrega](docs/checklist.md) | Lista de verificación obligatoria antes de entregar |
| [🔀 Guía de Git y Pull Request](docs/guia-git.md) | Paso a paso para fork, commit y pull request |
| [✍️ Consentimiento de Uso de Foto y Video](docs/Consentimiento-Uso-de-foto-y-Video.pdf) | Documento **obligatorio** que debes firmar y subir a tu carpeta `/docs` |

---

## Estructura de Archivos

El repositorio debe organizarse siguiendo estrictamente la siguiente estructura de directorios:

```
/PG-2026-[carnet]
│
├── /capturas                  # Capturas de pantalla del software (mínimo 10)
│   └── captura-1.jpg         # Captura del sistema 1
│   └── captura-2.jpg         # Captura del sistema 2
│   └── ...   
│   └── captura-n.jpg         # Captura del sistema n (mínimo 10)
│
├── /demo
│   └── demo.mp4              # Video demostrativo del proyecto
│
├── /docs
│   └── informe_final.pdf     # Informe final del proyecto
│   └── consentimiento_firmado.pdf  # Consentimiento de uso de foto y video FIRMADO (OBLIGATORIO)
│
├── /src
│   ├── .env.example          # Archivo de ejemplo para variables de entorno
│   ├── package.json          # Archivo de dependencias (según corresponda)
│   └── [código fuente]       # Archivos del código fuente del proyecto
│
└── README.md                 # Archivo de descripción e instrucciones
```

---

## Requisitos y Consideraciones Importantes

- El checklist de verificación debe completarse al **100%** sin excepción
- La carpeta `/capturas` debe contener **al menos 10 capturas de pantalla** del software en funcionamiento
- ⚠️ Es **OBLIGATORIO** firmar el [Consentimiento de Uso de Foto y Video](docs/Consentimiento-Uso-de-foto-y-Video.pdf) y subirlo firmado a `/docs/consentimiento_firmado.pdf`. **Sin este documento firmado la entrega NO será aceptada**
- El Pull Request debe crearse **antes** de la fecha y hora límite establecidas
- Los proyectos que no cumplan con la totalidad de los requisitos deberán ser corregidos antes de su aceptación formal
- No se aceptarán entregas posteriores a la fecha límite bajo ninguna circunstancia

---

## Soporte Técnico

En caso de presentar dudas o dificultades técnicas durante el proceso de entrega, se recomienda:

1. Consultar la [Guía de Git y Pull Request](docs/guia-git.md) para resolver problemas relacionados con el control de versiones
2. Revisar la sección de [Preguntas Frecuentes](docs/faq.md) donde se abordan las consultas más comunes
3. Contactar al asesor o profesor asignado si el problema persiste

---

## Referencias Adicionales

- [Documentación oficial de Git](https://git-scm.com/doc)
- [GitHub Docs - Fork a repo](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
- [GitHub Docs - Creating a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
