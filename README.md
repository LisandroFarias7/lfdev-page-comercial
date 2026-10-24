# LF Dev — Página comercial

Sitio de una sola página de **LF Dev**: sistemas a medida para negocios de Venado Tuerto y la región (tienda online, control de stock, turnos y agenda).

- `index.html` — todo el sitio (HTML + CSS + JS embebido, sin dependencias).
- `assets/demo-tienda.jpg` — captura real del catálogo de la demo.
- `assets/demo-producto.jpg` — ficha de producto con talle y stock.
- `assets/demo-carrito.jpg` — carrito con el checkout.
- `assets/og.jpg` — imagen para compartir el link (1200×630).
- `assets/apple-touch-icon.png` — ícono para iOS (180×180).
- `brand/` — opciones de logo en SVG y una hoja de muestra (`brand/index.html`, con `noindex`).
- `favicon.svg` — ícono del sitio (badge LF, opción C).

## Configuración

Antes de publicar cambios, revisar el bloque `CONFIG` al inicio de `index.html`:

```js
const CONFIG = {
  whatsapp: "5493462226572",
  email: "lisandrofarias29@gmail.com",
  demo: "https://demo-web-ooz8.onrender.com",
  ciudad: "Venado Tuerto"
};
```

> Todos los botones de demo ("Ver la demo", "Abrir la tienda demo", las tres capturas
> y "Ver la demo" del cierre) toman el valor de `CONFIG.demo`. Si cambia la URL de Render,
> se cambia ahí.

## Precios

| Plan | Inversión | Alcance |
|---|---|---|
| Esencial | USD 300 | 1 módulo (tienda, stock o turnos) |
| Completo | USD 500 | 2-3 módulos integrados |
| Premium | USD 800 | sistema a medida |

Pago en 3 tramos (40 / 40 / 20). Mantenimiento opcional desde USD 35/mes.

## Idioma y precios

- El sitio está en español por defecto y tiene un botón **EN/ES** en el header. La elección
  se guarda en `localStorage` y también se puede forzar con `?lang=en` (útil para mandar
  el link en inglés).
- Los precios se muestran en USD y, debajo, el equivalente en pesos.
- La cotización se toma de `https://dolarapi.com/v1/dolares/oficial` al cargar la página.
  Si la API no responde, usa `CONFIG.usdArs` (hoy 1550). Actualizalo si cambia mucho.
- Para traducir textos nuevos: agregá la frase en español como clave dentro del objeto
  `EN` del último `<script>` de `index.html`, y su versión en inglés como valor.

## Logo

**Elegidas:** B para el sitio (versión oscura en el header) y C como badge/favicon.

| Archivo | Uso |
|---|---|
| `logo-b-oscuro.svg` | Fondo oscuro (el que usa el sitio) |
| `logo-b-duotono-claro.svg` | Fondo claro (documentos, propuestas) |
| `logo-c-badge.svg` | Badge / favicon / redes |
| `logo-a-verde-oscuro.svg` | Alternativa verde sólido |
| `logo-d-degradado.svg` | Alternativa degradado |
| `logo-e-apilado.svg` | Alternativa apilada |
| `mark.svg` | Monograma suelto, hereda color con `currentColor` |

Para cambiar el logo del sitio, editar el `<svg>` del header en `index.html` (el bloque `.logo`).

## Dominio

El sitio responde en **https://lfdev.com.ar** a través de Cloudflare y se actualiza al pushear a `main`.

Si se publica con GitHub Pages en su lugar:

1. Agregar `CNAME` con el contenido `lfdev.com.ar`.
2. Apuntar el DNS a GitHub Pages (A `185.199.108-111.153`, CNAME `www` → `lisandrofarias7.github.io`).
3. Settings → Pages → Custom domain → *Enforce HTTPS*.
