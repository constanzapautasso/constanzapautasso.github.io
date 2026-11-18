# Constanza Pautasso | Portfolio y CV digital

Sitio personal de **Constanza Pautasso**, desarrolladora web freelance (Córdoba, Argentina).

Sitio estático hecho con HTML5, CSS3 y JavaScript sin frameworks ni dependencias. Funciona en GitHub Pages sin backend ni servicios pagos.

## Contenido

- Inicio con presentación, foto, descarga del CV y contacto
- Sobre mí
- Formación académica
- Habilidades
- Experiencia
- Proyectos destacados
- Servicios para emprendimientos
- Contacto (email, WhatsApp y LinkedIn)

## Estructura

```
.
├── index.html              Página principal
├── 404.html                Página de error de GitHub Pages
├── site.webmanifest        Datos para instalar el sitio en el celular
├── robots.txt              Indicaciones para buscadores
├── sitemap.xml             Mapa del sitio para buscadores
├── .nojekyll               Le indica a GitHub Pages que publique los archivos tal cual
└── assets/
    ├── css/styles.css      Estilos
    ├── js/main.js          Menú, navegación, animaciones y copiar email
    ├── cv/CV-Constanza-Pautasso.pdf
    ├── img/                Foto, imagen para redes (og-image) y, a futuro, proyectos
    ├── icons/              Favicon e íconos de la app
    └── fonts/              Tipografías Bricolage Grotesque e Instrument Sans (licencia SIL OFL)
```

## Publicar en GitHub Pages

### 1. Crear el repositorio

1. Creá una cuenta en [github.com](https://github.com) si todavía no tenés.
2. Creá un repositorio nuevo **público** con el nombre exacto `TU-USUARIO.github.io` (reemplazando `TU-USUARIO` por tu nombre de usuario de GitHub). Con ese nombre, la web queda en `https://TU-USUARIO.github.io/`.

### 2. Subir los archivos

**Desde el navegador (sin instalar nada):**

1. En el repositorio, entrá a **Add file → Upload files**.
2. Arrastrá **todo el contenido** de esta carpeta (no la carpeta en sí). `index.html` tiene que quedar en la raíz del repositorio.
3. Hacé clic en **Commit changes**.

> El archivo `.nojekyll` empieza con punto y puede quedar oculto en tu computadora. Si no lo ves, no pasa nada: el sitio funciona igual.

**Con Git (opcional):**

```bash
git init
git add .
git commit -m "Primera versión del portfolio"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/TU-USUARIO.github.io.git
git push -u origin main
```

### 3. Activar GitHub Pages

1. En el repositorio, entrá a **Settings → Pages**.
2. En **Source** elegí **Deploy from a branch**.
3. En **Branch** elegí `main` y la carpeta `/ (root)`. Guardá.
4. En uno o dos minutos la web queda publicada en `https://TU-USUARIO.github.io/`.

### 4. Completar tu dirección en el sitio

Buscá el texto `TU-USUARIO` y reemplazalo por tu usuario de GitHub en estos archivos:

- `index.html` (enlace canónico e imagen para redes)
- `robots.txt`
- `sitemap.xml`

Esto hace que la vista previa al compartir el enlace en WhatsApp o LinkedIn muestre la imagen correcta.

> Si preferís publicar en un repositorio con otro nombre (por ejemplo `portfolio`), la dirección será `https://TU-USUARIO.github.io/portfolio/`. En ese caso actualizá también esa dirección en los tres archivos, y en `404.html` cambiá las rutas que empiezan con `/` por `/portfolio/`.

## Cómo actualizar el contenido

Todos los textos están en `index.html`. Cada sección está marcada con un comentario, por ejemplo `<!-- ============ PROYECTOS ============ -->`.

### Activar el botón de GitHub

Hay dos bloques preparados y ocultos con el atributo `hidden` (uno en el inicio y otro en contacto). Para mostrarlos:

1. Reemplazá `https://github.com/TU-USUARIO` por la dirección de tu perfil.
2. Borrá la palabra `hidden` de esas dos líneas `<li ... hidden>`.

### Agregar imágenes, tecnologías o enlaces a un proyecto

Dentro de cada proyecto hay un comentario con las instrucciones. Resumen:

- **Imagen:** guardala en `assets/img/proyectos/` (formato `.webp` o `.jpg`, proporción 16:9, unos 1200 × 675 px) y reemplazá el bloque `<div class="project-cover ...">` por una etiqueta `<img class="project-cover" ...>`.
- **Tecnologías:** completá la lista `<ul class="chips chips-sm">` y borrá `hidden`.
- **Enlaces a GitHub o demo:** completá las direcciones en `.project-links` y borrá `hidden`.

### Agregar un proyecto nuevo

Al final de la sección de proyectos hay una plantilla comentada. Copiala, quitá los signos `<!--` y `-->` y completala.

### Actualizar el CV

Reemplazá `assets/cv/CV-Constanza-Pautasso.pdf` por la versión nueva, con el mismo nombre de archivo.

### Cambiar la foto

Reemplazá `assets/img/constanza-pautasso.jpg` y `assets/img/constanza-pautasso.webp`. La foto actual mide 414 × 452 px; conviene mantener una proporción parecida.

## Probar en tu computadora

Abrí `index.html` con doble clic, o levantá un servidor local desde la carpeta:

```bash
python3 -m http.server 8000
```

y entrá a `http://localhost:8000`.

## Características técnicas

- Diseño responsive para computadora, tablet y celular
- Menú móvil accesible con teclado (se cierra con Escape)
- Resaltado de la sección activa en el menú
- Animaciones al desplazarse, desactivadas si el sistema pide reducir el movimiento
- SEO básico: título, descripción, Open Graph, datos estructurados (schema.org), sitemap y robots
- Accesibilidad: enlace para saltar al contenido, foco visible, textos alternativos y contraste AA
- Tipografías alojadas en el repositorio, sin depender de servicios externos
- Sin dependencias ni proceso de compilación

---

© 2026 Constanza Pautasso
