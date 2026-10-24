# LF Dev — Página comercial

Sitio de una sola página de **LF Dev**: sistemas de turnos y tiendas online para negocios de Venado Tuerto y la región.

- `index.html` — todo el sitio (HTML + CSS + JS embebido, sin dependencias).
- Publicado con **GitHub Pages** desde la rama `main`, carpeta raíz.

## Configuración

Antes de publicar cambios, revisar el bloque `CONFIG` al inicio de `index.html`:

```js
const CONFIG = {
  whatsapp: "5493462226572",
  email: "lisandro@lfdev.com.ar",
  demoTurnos: "https://demo.lfdev.com.ar",
  demoTienda: "https://tienda.lfdev.com.ar",
  agenda: "",
  ciudad: "Venado Tuerto"
};
```

## Dominio propio

Para servir el sitio en `lfdev.com.ar`:

1. Agregar un archivo `CNAME` en la raíz con el contenido `lfdev.com.ar`.
2. En el DNS del dominio, apuntar a GitHub Pages:

| Tipo | Nombre | Valor |
|---|---|---|
| A | `@` | 185.199.108.153 |
| A | `@` | 185.199.109.153 |
| A | `@` | 185.199.110.153 |
| A | `@` | 185.199.111.153 |
| CNAME | `www` | `lisandrofarias7.github.io` |

3. En GitHub: Settings → Pages → Custom domain → `lfdev.com.ar` → tildar *Enforce HTTPS*.

> El archivo `CNAME` se agrega recién cuando el DNS está configurado. Si se agrega antes, la URL `github.io` redirige a un dominio que todavía no resuelve.
