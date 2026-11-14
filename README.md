# Facebook Comments Analyzer

Aplicación web en un único archivo HTML para obtener, analizar, copiar y exportar los comentarios de publicaciones de Facebook.

## Características

- **Tres formas de obtener comentarios**
  - **Conectar con Facebook** (Graph API + inicio de sesión): para páginas que administras; fechas exactas, reacciones y respuestas.
  - **Extractor de navegador** (marcador *Facebook Comments Analyzer*): para cualquier publicación visible con tu sesión.
  - **Importar** JSON o CSV.
- **Vista de conversación** como en Facebook, con respuestas anidadas, o **vista de tabla** con todos los campos.
- **Análisis**: actividad en el tiempo y por hora, autores más activos, sentimiento estimado, palabras, emojis, hashtags y menciones.
- **Búsqueda y filtros** por texto, autor, tipo, sentimiento, preguntas, reacciones y adjuntos.
- **Copiar y exportar** a Excel (.xlsx), CSV, JSON, texto, Markdown o informe HTML.
- Diseño Material 3, responsive, tema claro/oscuro, tutorial de inicio y centro de ayuda integrados.
- Todo se procesa en el navegador: no hay servidor.

## Uso

**En línea (HTTPS):** <https://arlizheredia.github.io/comments-facebook-analyzer/>

También puedes abrir `index.html` directamente en el navegador. La primera vez se muestra un tutorial con los pasos para empezar.

Para **Conectar con Facebook**, la página debe servirse por `https://` (la versión publicada ya lo cumple; agrega `arlizheredia.github.io` a los dominios permitidos de tu app de Facebook) o por `http://localhost`:

```bash
python3 -m http.server 8000
# abre http://localhost:8000
```

Además necesitas el **App ID** de una app de Facebook con los permisos `pages_show_list`, `pages_read_engagement` y `pages_read_user_content`. La guía completa está en la sección **Ayuda** de la aplicación.

## Limitaciones

- El extractor de navegador requiere un ordenador; la versión móvil de Facebook no lo admite.
- Las fechas obtenidas con el extractor son aproximadas, porque Facebook muestra tiempos relativos (“2 h”, “3 sem”).
- El sentimiento se estima con un diccionario de palabras y emojis; es orientativo.
