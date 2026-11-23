# QuickSurfaces · Assets

Todas las imágenes, logos, ilustraciones y PDFs de QuickSurfaces en un solo lugar.
Lo usan estas apps:
- la **web principal** (quicksurfaces);
- **Condo** (la app de comunidades como Siena Reserve);
- **Surfaces** (surfacesgama.com, el catálogo marca blanca para instaladores).

Lo que comparten va en `compartido/`. Lo que es solo de una app va en su carpeta.

```
quicksurfaces-assets/
├── compartido/                ← lo usan las dos apps (y el cotizador / catálogo)
│   ├── brand/                 logos SVG + PNG, ícono, logo de ficha técnica, fuente Poppins
│   ├── guides/                PDFs: instalación, limpieza, garantía
│   ├── products/<producto>/   foto del producto solo (tabla, moldura, rollo…)
│   ├── rooms/<producto>/      foto del producto instalado / ambiente
│   └── testimonials/          una foto por testimonio (los mismos en web y Condo)
├── web/                       ← solo la web principal
│   ├── site/                  hero, foto de pisos, foto de escaleras, sección de escaleras, teléfono Roomvo
│   ├── projects/<proyecto>/   01.webp (portada), 02.webp, 03.webp
│   └── illustrations/categories/   ilustraciones de las 6 categorías (SVG para Figma + PNG)
├── surfaces/                  ← solo la app Surfaces (sin marca QuickSurfaces)
│   ├── brand/                 logo de Surfaces (horizontal, vertical, ícono, ícono de app) en SVG + PNG
│   └── guides/                guías genéricas: instalación, limpieza y garantía (CPF)
└── condo/                     ← solo la app Condo
    ├── banners/               banner de entrada de cada comunidad
    ├── projects/<comunidad>/  fotos de trabajos hechos en esa comunidad
    ├── renders/<comunidad>/<modelo>/   vertical.webp, dollhouse-1er-piso.jpg, dollhouse-2do-piso.jpg
    ├── stairs/                fotos y diagrama del Square Step Nose
    └── illustrations/stairs/  ilustraciones SVG de las escaleras
```

## Productos: una sola foto para todas las apps

Las fotos de pisos, baseboards, molduras, etc. van **una sola vez** en `compartido/products` y `compartido/rooms`.
La base de datos central dice qué foto usa cada color. Condo solo muestra 3 colecciones de piso:
- Pulse Select (`spc-5.5mm-pulse-select`);
- XL Pulse (`spc-8.0mm-xl-pulse`);
- Pulse Shield XL (`spc-6.0mm-pulse-shield-xl`).

Esas 3 colecciones las usa también la web, así que no se duplican.

## Reglas para nombrar fotos

- **Todo en minúsculas, sin espacios ni acentos.** Usa guiones: `q-0115.webp`, no `Q 0115.WEBP`.
- **Formato:** `.webp` (si tienes JPG o PNG, súbelo igual y yo lo convierto).
- **Tamaño recomendado:** 2000 px por el lado más largo, menos de 400 KB.
- **Pisos y wall panels:** el archivo se llama como el **código del color** (`q-0115.webp`). El resto de productos se llama `main.webp`.
- **No cambies el nombre de las carpetas de productos:** el nombre es el ID del producto en la base de datos.
- **Comunidad o modelo nuevo en Condo:** crea su carpeta con el mismo formato, por ejemplo `condo/renders/<comunidad>/<modelo>/`.

## Qué falta

La lista **siempre al día** está en el admin: **Productos → Fotos**. Lee esta carpeta, muestra qué foto falta
(también de productos nuevos), cuáles están listas y, con **Vincular**, conecta cada foto con su producto y color.


Abre **`LISTA-DE-FOTOS.csv`** (en Excel o Google Sheets). Cada fila es una foto, con la app que la usa,
el producto, el color, el código y si **YA ESTÁ** o **FALTA**.

Las carpetas vacías tienen un archivo `.gitkeep` (para que GitHub las guarde). Cuando metas la foto, puedes borrarlo.

Si un producto ya no existe (lo borraste del panel), borra sus dos carpetas: la de `compartido/products/` y la de `compartido/rooms/`.

## ⚠️ No subir aquí

Este repositorio es **público** (para que las fotos se vean en las apps). Nunca subas precios,
el respaldo JSON, el Excel con precios ni ninguna llave o contraseña.
