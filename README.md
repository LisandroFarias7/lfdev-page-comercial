# LF Dev — Página comercial

Sitio de una sola página de **LF Dev**: tiendas online a medida para negocios de Venado Tuerto y la región.

- `index.html` — todo el sitio (HTML + CSS + JS embebido, sin dependencias).
- `assets/demo-tienda.jpg` — captura real de la tienda demo.
- `assets/og.jpg` — imagen para compartir el link (1200×630).
- `brand/` — opciones de logo en SVG y una hoja de muestra (`brand/index.html`, con `noindex`).
- `favicon.svg` — ícono del sitio (badge LF).

## Configuración

Antes de publicar cambios, revisar el bloque `CONFIG` al inicio de `index.html`:

```js
const CONFIG = {
  whatsapp: "5493462226572",
  email: "lisandro@lfdev.com.ar",
  demo: "https://tienda-demo.onrender.com",  // ← URL real de la demo
  ciudad: "Venado Tuerto"
};
```

> **Pendiente:** reemplazar `demo` por la URL real del servicio en Render. Todos los botones de demo
> ("Entrar a la demo", "Abrir la tienda demo", el banner y "Ver la demo") toman ese valor.

## Precios

| Plan | Inversión |
|---|---|
| Esencial | USD 300 |
| Completo | USD 500 |
| Premium | USD 800 |

Pago en 3 tramos (40 / 40 / 20). Mantenimiento opcional desde USD 35/mes.

## Logo

Las cinco opciones están en `brand/`:

| Archivo | Uso |
|---|---|
| `logo-a-verde-oscuro.svg` | Fondo oscuro (el que usa el sitio) |
| `logo-b-duotono-claro.svg` | Fondo claro, slate + verde |
| `logo-c-badge.svg` | Ícono de app / favicon / redes |
| `logo-d-degradado.svg` | Degradado verde |
| `logo-e-apilado.svg` | Apilado, el más parecido al logo anterior |
| `mark.svg` | Monograma suelto, hereda color con `currentColor` |

Para cambiar el logo del sitio, editar el `<svg>` del header en `index.html` (el bloque `.logo`).

## Dominio

El sitio responde en **https://lfdev.com.ar** a través de Cloudflare.

Si se publica con GitHub Pages en su lugar:

1. Agregar `CNAME` con el contenido `lfdev.com.ar`.
2. Apuntar el DNS a GitHub Pages (A `185.199.108-111.153`, CNAME `www` → `lisandrofarias7.github.io`).
3. Settings → Pages → Custom domain → *Enforce HTTPS*.
