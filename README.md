# Grupo Vertex — Área de Seguridad

Sitio estático universitario creado con HTML, CSS y JavaScript Vanilla. No requiere instalación ni servidor para abrirlo localmente.

## Estructura

```
.
├── index.html                 # Página principal
├── pages/                     # Las ocho páginas académicas independientes
├── css/
│   ├── tokens.css             # Colores, tipografía, espacios y tamaños globales
│   ├── components/            # Navegación, botones, tarjetas, secciones y footer
│   └── pages/home.css         # Estilos exclusivos de inicio
├── js/
│   ├── components.js          # Menú, pie y secciones centralizados
│   ├── navigation.js          # Drawer móvil y comportamiento del menú
│   ├── animations.js          # Animaciones accesibles de entrada
│   └── main.js                # Tarjetas de inicio y recursos de video
└── assets/images/             # Imágenes futuras, organizadas por sección
```

## Abrir localmente

Abre `index.html` en un navegador. Para una previsualización más parecida a producción, usa una extensión de servidor local (por ejemplo, Live Server en VS Code).

## Imágenes

Usa WebP para fotografías y SVG para logos, símbolos y diagramas vectoriales. Las carpetas ya existen y pueden permanecer vacías.

- `assets/images/logo/vertex-security.svg`: logo/símbolo oficial (opcional; la interfaz usa un ícono temporal elegante).
- `assets/images/home/hero-seguridad.webp`: imagen del hero, recomendada 1400 × 1000 px, horizontal.
- `assets/images/home/grupo-vertex.webp`: imagen de apoyo para la sección Grupo Vertex, recomendada 1600 × 900 px, horizontal.

El diseño no produce imágenes rotas si estos archivos aún no están. Al incorporar una imagen, añade el elemento `<img>` correspondiente en `index.html` y conserva `object-fit: cover`.

## Personalización

- Cambia colores, espacios y tipografías desde `css/tokens.css`.
- Agrega o edita secciones solo en el arreglo `SITE_SECTIONS` de `js/components.js`: navegación, footer y tarjetas se actualizan desde allí.
- Para una página nueva, crea su HTML en `pages/`, añade su entrada a `SITE_SECTIONS` y conserva `data-page` con el mismo `id`.
- Para habilitar videos, reemplaza los datos de ejemplo en `js/main.js` por objetos con `youtubeId`; mantén la carga bajo interacción para no cargar YouTube al abrir la página.

## Publicación

El sitio funciona directamente en GitHub Pages, Netlify o Vercel:

1. Sube estos archivos al repositorio.
2. En GitHub Pages, selecciona **Settings → Pages → Deploy from a branch** y usa la rama `main` y la carpeta raíz (`/`).
3. Al no requerir compilación, no se necesita comando de build.
