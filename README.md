# CIM UC · Explorador de Innovación en Madera

Aplicación móvil Android (MVP académico) desarrollada para la asignatura **DSY1105 – Desarrollo de Aplicaciones Móviles** (Evaluación Parcial 2, Equipo G1).

## Integrantes

- [Martin Soto]
- [Enzo Rojas]

## Descripción del proyecto

Experiencia móvil para explorar, buscar y consultar contenidos ficticios del Centro UC de Innovación en Madera (CIM UC): proyectos, capacidades I+D, integrantes, publicaciones y actividades. Su elemento diferenciador es la **Ruta de Innovación**, que muestra la cadena *Proyecto → Capacidad I+D → Integrante → Oportunidad* y orienta al usuario hacia una oportunidad de colaboración (contacto simulado).

Todos los datos son ficticios y no se usa ningún sistema productivo ni credenciales reales.

## Funcionalidades implementadas

- Explorar catálogo por categorías (RF-01).
- Buscar por título o descripción (RF-02) y filtrar por tipo y área temática (RF-03).
- Ficha de detalle con título, descripción, año, estado y relaciones (RF-04).
- Ruta de Innovación y contenidos relacionados (RF-05).
- Consulta de oportunidad de colaboración (RF-06).
- Formulario de contacto simulado con validaciones por campo (RF-07).
- Historial de los últimos contenidos consultados en la sesión (RF-08).

## Estado de entrega

El código fuente está en esta carpeta. El ZIP recibido no incluye un repositorio Git ni los archivos `gradlew`, `gradlew.bat` y `gradle-wrapper.jar`; abre el proyecto desde Android Studio y sincroniza Gradle. Completa los nombres antes de entregar. La publicación en GitHub, la planificación en Trello y la carga/activación en AVA se realizan desde las cuentas del equipo y deben comprobarse por separado.

## Requisitos de la evaluación

| Requisito | Dónde está |
|---|---|
| Interfaz organizada y navegación clara | `ui/screens`, `ui/navigation` |
| Formularios validados con íconos y mensajes visuales | `ui/components/Componentes.kt` (`CampoValidado`), `ui/screens/contacto` |
| Validaciones manejadas desde lógica | `validacion/Validadores.kt`, `ContactoViewModel` |
| Animaciones funcionales | Transiciones de navegación, entrada escalonada de la Ruta, escala al presionar, mensajes de error y confirmación animados |
| Estructura modular, MVVM y persistencia local | `data/` (Room), `ui/screens/*/…ViewModel.kt` |
| Dos recursos nativos | Vibración (`recursos/VibradorHelper.kt`) y notificaciones locales con permiso en ejecución (`recursos/NotificacionHelper.kt`) |
| GitHub + Trello | Ver `GUIA_ENTREGA.md` |

## Arquitectura

MVVM con Jetpack Compose. Carpetas dentro de `app/src/main/java/cl/duoc/cimuc`:

```
data/        local (Room: entidades, DAO, base de datos, datos iniciales), model, repository
validacion/  reglas de validación
recursos/    acceso a recursos nativos (vibración, notificaciones)
ui/          theme, components, navigation, screens (inicio, busqueda, detalle, ruta, contacto)
```


