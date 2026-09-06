# Portafolio — Maykel Chapman / Nexora Labs

Sitio estático de una sola página. Sin build step, sin dependencias — es
HTML y CSS puros, así que sirve en cualquier hosting.

## Estructura

```
index.html    Contenido y estructura de la página
styles.css    Todos los estilos
robots.txt    Permite indexado por buscadores
```

## Cómo probarlo localmente

```bash
python3 -m http.server 8000
```

Abre `http://localhost:8000`.

## Cómo publicarlo con dominio propio

Cualquiera de estas opciones funciona sin modificar el código:

### Opción A — Netlify (recomendada, gratis, deploy en segundos)
1. Crea cuenta en [netlify.com](https://netlify.com)
2. Arrastra esta carpeta a la zona de "Deploy" del dashboard, o conecta
   este repositorio de GitHub para que se actualice solo con cada push
3. En **Domain settings** agrega tu dominio comprado y sigue las
   instrucciones de DNS que te da Netlify (apuntar un registro A o CNAME)

### Opción B — Vercel
1. Crea cuenta en [vercel.com](https://vercel.com)
2. Importa este repositorio de GitHub
3. Framework preset: "Other" (no necesita build)
4. Agrega tu dominio en **Settings → Domains**

### Opción C — GitHub Pages (gratis, ya en el mismo repo)
1. En este repositorio: **Settings → Pages**
2. Source: rama `main`, carpeta `/ (root)`
3. En **Settings → Pages → Custom domain** escribe tu dominio comprado
4. En tu proveedor de dominio agrega un registro CNAME apuntando a
   `<tu-usuario>.github.io`

### Opción D — Hosting tradicional (cPanel, etc.)
Sube `index.html`, `styles.css` y `robots.txt` a la carpeta pública
(`public_html` o `www`) por FTP o el administrador de archivos. No
requiere configuración adicional.

## Actualizar el contenido

Todo el texto y los mockups de cada app viven directamente en
`index.html`, sección por sección (`<section class="project" id="...">`).
Los colores de cada mockup usan directamente los hex de cada app, así
que para agregar una app nueva basta con duplicar una sección y
cambiar textos, colores y el link de GitHub.
