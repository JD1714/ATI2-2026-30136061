# CineConnect - Red Social de Reseñas y Recomendaciones

Plataforma comunitaria interactiva orientada a la crítica, discusión de películas y series de televisión.

---

## 1. Identificación y Entorno del Reto

* **Asignatura:** Aplicación de Tecnologías de Información 2 (ATI2)
* **Entregable:** Reto 2
* **Entorno de Desarrollo:** IntelliJ IDEA
* **Control de Versiones:** Git & GitHub
* **Rama de Trabajo:** `reto2`

---

## 2. Registro de Sincronización y Configuración

* **Estado de Sincronización:** Repositorio local configurado y vinculado mediante upstream (`origin/reto2`).
* **Verificación de Herramientas:** Integración de Git activa en IntelliJ IDEA, seguimiento de ramas locales y remotas, y documentación del proyecto versionada bajo estándares de la asignatura.

---

## 3. Políticas de Manejo de Ramas y Versiones

### 3.1. Modelo de Ramas (Git Flow Adaptado)
* **`main`**: Rama principal de producción y entrega de versiones estables. Solo recibe cambios mediante Pull Requests validados tras revisión.
* **`develop`**: Rama base de integración continua donde convergen las características previas a cada corte evaluativo.
* **Ramas de soporte y características:**
  * `feature/<nombre-modulo>`: Creación de componentes específicos (e.g., `feature/perfil-usuario`, `feature/top5-rankings`).
  * `fix/<nombre-incidencia>`: Correcciones y ajustes durante el desarrollo.
  * `reto2`: Rama designada para el desarrollo y entrega formal del Reto 2.

### 3.2. Convención de Commits (Conventional Commits)
Se emplea el estándar de prefijos semánticos para mantener un historial trazable:
* `feat:` Incorporación de nuevas funciones en la aplicación.
* `fix:` Corrección de errores o bugs.
* `docs:` Modificaciones exclusivas de documentación (README, diagramas, actas).
* `refactor:` Reestructuración interna de código sin impacto funcional.
* `chore:` Tareas de configuración, scripts o ajustes de dependencias.

### 3.3. Esquema de Versionado
Se aplica **Semantic Versioning (SemVer)** bajo el formato `vX.Y.Z`:
* **X (Major):** Hitos evaluativos mayores o cambios estructurales incompatibles.
* **Y (Minor):** Nuevas funcionalidades o entregas de retos específicos.
* **Z (Patch):** Correcciones menores de interfaz, estilos o documentación.
* **Versión actual:** `v0.2.0` (Corte correspondiente a Reto 2).

---

## 4. Propuesta de Proyecto ATI2

### 4.1. Título
**CineConnect: Plataforma Social de Crítica Cinematográfica y Curaduría de Top 5**

### 4.2. Descripción y Justificación
En la actualidad, los espectadores disponen de una amplia oferta de contenidos audiovisuales distribuidos en múltiples plataformas de streaming, lo que a menudo dificulta el filtrado y descubrimiento de producciones de calidad.

**CineConnect** surge como una red social especializada donde los usuarios no solo califican producciones de forma aislada, sino que construyen una identidad cinéfila basada en la discusión comunitaria. El elemento diferenciador es su sistema modular de curaduría: perfiles con rankings fijos de **"Top 5 Películas"** y **"Top 5 Series"**, reseñas con soporte de etiquetas por género, y un muro de interacción para debatir puntos de vista con amigos y la comunidad.

### 4.3. Objetivos
* **Objetivo General:**
  * Desarrollar una aplicación web orientada a la interacción social en torno al cine y las series, facilitando la publicación de reseñas analíticas y la exhibición de listas personalizadas de favoritos.
* **Objetivos Específicos:**
  1. Diseñar un módulo de gestión de perfiles de usuario que integre un selector interactivo para rankear su "Top 5" permanente de series y películas con orden de preferencia (1 al 5).
  2. Implementar un sistema de publicación y lectura de reseñas comunitarias con valoración cuantitativa (estrellas o puntuación base 10) y comentarios.
  3. Integrar un feed dinámico que permita descubrir reseñas recientes, seguir a otros usuarios y explorar recomendaciones basadas en los gustos comunes.
  4. Configurar una arquitectura desacoplada que garantice persistencia de datos segura y un flujo continuo de versionado en Git.

### 4.4. Alcance y Limitaciones
* **Alcance:**
  * Registro, login y autenticación de usuarios.
  * Panel de perfil personalizable con el widget visual del "Top 5" (películas y series).
  * Muro / Feed con reseñas, opción de dar "Me gusta" y sección de comentarios.
  * Búsqueda y filtrado de títulos por categoría, género y puntuación media.
* **Limitaciones:**
  * En esta primera fase no se incluye reproducción de video ni almacenamiento de archivos pesados (streaming).
  * No se implementará mensajería instantánea privada (chat 1 a 1) en las entregas iniciales.

### 4.5. Arquitectura y Stack Tecnológico Propuesto
* **Frontend:** Interfaz web modular y reactiva construida con componentes reutilizables (HTML5, CSS3/Tailwind, JavaScript/TypeScript).
* **Backend / Lógica:** API REST encargada del manejo de lógica de negocio, validaciones y autenticación.
* **Persistencia:** Base de datos relacional para el modelado de entidades (Usuarios, Producciones, Reseñas, Rankings Top 5).
* **Control y Despliegue:** Control de versiones con Git/GitHub, entorno IntelliJ IDEA y configuración de despliegue continuo.