# Social Comments Analyzer

Aplicación web en un único archivo HTML para obtener, analizar, copiar y exportar los comentarios de publicaciones de **Facebook** e **Instagram**.

## Características

- **Facebook e Instagram**: la red social se detecta automáticamente al pegar un enlace.
- **Tres formas de obtener comentarios**
  - **Conectar con la API** (inicio de sesión de Facebook): páginas de Facebook que administras y sus cuentas profesionales de Instagram vinculadas; fechas exactas, reacciones o me gusta y respuestas.
  - **Extractor de navegador** (marcador *Social Comments Analyzer*): para cualquier publicación visible con tu sesión. El mismo marcador funciona en Facebook e Instagram.
  - **Importar** JSON o CSV.
- **Vista de conversación** con el estilo de cada red y respuestas anidadas, o **vista de tabla** con todos los campos.
- **Análisis**: actividad en el tiempo y por hora, autores más activos, sentimiento estimado, palabras, emojis, hashtags y menciones.
- **Búsqueda y filtros** por texto, autor, tipo, sentimiento, preguntas, reacciones y adjuntos.
- **Copiar y exportar** a Excel (.xlsx), CSV, JSON, texto, Markdown o informe HTML, con la plataforma de cada comentario.
- Diseño Material 3, responsive, tema claro/oscuro, tutorial de inicio y centro de ayuda contextual.
- Todo se procesa en el navegador: no hay servidor.

## Uso

**En línea (HTTPS):** <https://arlizheredia.github.io/comments-facebook-analyzer/>

También puedes abrir `index.html` directamente en el navegador. La primera vez se muestra un tutorial con los pasos para empezar.

Para **conectar con la API**, la página debe servirse por `https://` (la versión publicada ya lo cumple; agrega `arlizheredia.github.io` a los dominios permitidos de tu app de Meta) o por `http://localhost`:

```bash
python3 -m http.server 8000
# abre http://localhost:8000
```

Necesitas el **App ID** de una app de Meta con estos permisos:

- Facebook: `pages_show_list`, `pages_read_engagement` y `pages_read_user_content`.
- Instagram (además de los anteriores): `instagram_basic` e `instagram_manage_comments`. La cuenta de Instagram debe ser profesional (Empresa o Creador) y estar vinculada a una página de Facebook que administres.

La guía completa está en la sección **Ayuda** de la aplicación.

## Limitaciones

- La API solo da acceso a publicaciones de páginas y cuentas que administras; para las demás se usa el extractor.
- El extractor de navegador requiere un ordenador; las versiones móviles de Facebook e Instagram no lo admiten.
- En Facebook, las fechas del extractor son aproximadas, porque la página muestra tiempos relativos (“2 h”, “3 sem”). En Instagram son exactas.
- Las condiciones de uso de Facebook e Instagram limitan la recogida automatizada de datos: usa el extractor de forma responsable.
- El sentimiento se estima con un diccionario de palabras y emojis; es orientativo.
