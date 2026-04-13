# TDD Check · paquete listo para Netlify

## Archivos incluidos
- index.html
- manifest.json
- sw.js
- icon-192.png
- icon-512.png
- netlify.toml
- _redirects
- _headers

## Subida a GitHub
1. Crea un repositorio nuevo o usa uno vacío.
2. Sube todos los archivos de esta carpeta a la raíz del repo.
3. Verifica que `index.html` quede en la raíz.

## Conexión con Netlify
1. En Netlify, pulsa **Add new site** → **Import an existing project**.
2. Conecta GitHub y selecciona el repo.
3. Build command: dejar vacío.
4. Publish directory: `.`
5. Deploy.

## Google Drive
La app ya trae la integración de Google Drive en navegador.
Tras desplegarla, añade en Google Cloud Console:
- `https://TU-SITIO.netlify.app`
- y tu dominio personalizado, si lo usas
como **Authorized JavaScript origins** del cliente OAuth.

## OneDrive personal
Se ha añadido integración con **OneDrive personal** usando Microsoft Graph.
Para que funcione:
1. Crea un registro de app en Microsoft Entra.
2. Marca la app como **Single-page application (SPA)**.
3. Añade como Redirect URI tu URL de Netlify, por ejemplo `https://TU-SITIO.netlify.app/`.
4. Permite **cuentas personales de Microsoft**.
5. Concede el scope delegado `Files.ReadWrite.AppFolder`.
6. Copia el **Client ID** y pégalo dentro de la app en **Config → Cloud · OneDrive**.

La copia se guarda en la carpeta privada de la app dentro de OneDrive.

## Galería fotográfica
Ahora el anexo fotográfico permite:
- eliminar fotos
- editar el título o descripción
- editar el texto del análisis IA / observaciones


Actualización v3:
- Añadida carga de imágenes desde galería/fototeca/archivos, además de la cámara.
- En las fotos de checklist se distinguen accesos directos a Cámara y Galería.
