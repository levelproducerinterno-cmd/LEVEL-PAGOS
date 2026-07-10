# Level Quincena

Genera la imagen del "video del mes" (con miniatura automática de YouTube) y los mensajes personalizados de pago quincenal para el equipo, con botón directo para abrir WhatsApp.

## Cómo subirlo a GitHub + Vercel (igual que tus otros sistemas Level)

1. Crea un repo nuevo en GitHub, por ejemplo `LEVEL-QUINCENA` (bajo tu mismo usuario/organización `levelproducerinterno-cmd`).
2. Sube el archivo `index.html` de este zip a la raíz del repo.
3. Entra a [vercel.com](https://vercel.com), dale "Add New... → Project", elige el repo `LEVEL-QUINCENA`.
4. Vercel detecta automáticamente que es un sitio estático — no necesita Build Command ni Framework Preset. Dale "Deploy".
5. En unos segundos te da una URL tipo `level-quincena.vercel.app`.

## Notas importantes

- El logo y el fondo con textura están incrustados en base64 dentro del `index.html` — no dependen de archivos externos, salvo las fuentes de Google Fonts y la librería html2canvas (cargada por CDN).
- La miniatura de YouTube se obtiene a través de un proxy público (images.weserv.nl) para evitar problemas de CORS al generar la imagen; si YouTube o el proxy cambian su comportamiento en el futuro, avísame para ajustarlo.
- **Guardado del equipo:** el sistema intenta guardar tu lista de nombres y teléfonos automáticamente. Si notas que no se guarda entre visitas (una vez desplegado fuera de Claude), usa el botón "respaldo manual" dentro de la tarjeta "Equipo" para copiar tu lista como texto y guardarla en algún lugar (notas, Drive, etc.) — así la puedes restaurar pegándola de vuelta en un segundo.
- Los links de WhatsApp usan el formato `wa.me/<código de país><número>`, por ejemplo `521XXXXXXXXXX` para México. Asegúrate de guardar los teléfonos del equipo con el código de país incluido, sin espacios ni guiones.
