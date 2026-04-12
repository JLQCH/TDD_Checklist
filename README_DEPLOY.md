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

## Importante si usas Google Drive dentro de la app
La app incluye autenticación OAuth de Google en el navegador. Tras desplegarla, añade en Google Cloud Console:
- el dominio `https://TU-SITIO.netlify.app`
- y tu dominio personalizado, si lo usas
como **Authorized JavaScript origins** del cliente OAuth.

Sin eso, el despliegue puede completarse pero el login con Google Drive fallará en tiempo de ejecución.
