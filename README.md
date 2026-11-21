# Hando Science — Registro Nacional de Trauma

Paquete de implementación web basado en el diseño de Figma **Hando-Web**, nodo `183:35`.

## Contenido

- `index.html` — estructura de la landing y sus contenidos.
- `style.css` — estilos de escritorio, tablet y móvil.
- `script.js` — gráficos ilustrativos, menú móvil y comportamiento del formulario.
- `assets/` — logos e íconos locales utilizados por la página.

## Cómo revisarlo

Abrir `index.html` en el navegador. Para una vista más parecida al entorno de producción, se puede servir esta carpeta con cualquier servidor web estático, por ejemplo `python3 -m http.server 8000`, y abrir `http://localhost:8000`.

No requiere instalación de librerías, compilación ni Tailwind. Las fuentes se cargan desde Google Fonts; si la política del sitio restringe recursos externos, deberán alojarse localmente o sustituirse por las fuentes ya aprobadas.

## Cómo integrarlo al sitio de Hando

1. Adaptar el contenido de `index.html` a la estructura y framework que utilice la web existente. Si se publica como página independiente, pueden conservarse los archivos tal cual dentro de una ruta, por ejemplo `/trauma/`.
2. Mantener juntos `index.html`, `style.css`, `script.js` y `assets/`, porque el HTML utiliza rutas relativas.
3. Revisar el menú superior: algunos enlaces están dirigidos a secciones de esta landing como demostración y deberán conectarse a las rutas reales de Hando, Calendar, Science, Equipo y Contacto.
4. Conectar el formulario `#signup-form` a un backend o servicio de recepción, incorporar validaciones del servidor, consentimiento y aviso de privacidad. Actualmente **no envía ni almacena datos**: solo muestra un aviso de demostración.
5. Sustituir cualquier contenido todavía marcado como pendiente en el diseño: periodicidad de los planes (`[al mes / al año]`), proveedor y región de almacenamiento, y documento PDF de seguridad. El enlace de descarga de seguridad es solo texto, no una descarga activa.
6. Revisar las afirmaciones legales, de seguridad, precios y resultados clínicos con los responsables de Hando antes de publicar en producción. Los datos de los dashboards están etiquetados como ficticios.
7. Conectar los enlaces de privacidad, términos y equipo a las páginas definitivas.

## Diseño de origen

https://www.figma.com/design/eK7GmrpkPjTLOB51SxbZpD/Hando-Web?node-id=183-35&m=dev

Este paquete es una implementación independiente HTML/CSS/JS. No modifica el sitio de producción ni incluye claves, credenciales o servicios de backend.
