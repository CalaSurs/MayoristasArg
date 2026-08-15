# MayoristasARG

Landing page de MayoristasARG (mismo sitio y flujo de compra que el original, con branding propio).

## Marca

| Uso | Color | Hex |
| --- | --- | --- |
| Primario (botones, header, footer, fondos oscuros) | Azul Marino Sólido | `#1A365D` |
| Acento (badges, destacados, íconos, pasos, estrellas) | Naranja Vibrante | `#F97316` |
| Base | Blanco Puro | `#FFFFFF` |

Los colores están centralizados en las variables de `css/styles.css` (`--clay*` para el azul,
`--accent*` para el naranja). Cambiando esas variables cambia todo el sitio.

Imágenes de marca en `images/`, generadas a partir del logo original:

- `logo-full.png` — logo a color (header y páginas legales)
- `logo-full-white.png` — versión blanca con el acento naranja (footer)
- `favicon-32.png` / `favicon-180.png` / `favicon-512.png` — isotipo sobre fondo azul marino
- `og-image.jpg` — imagen para compartir en redes (1200x630)

## Datos de contacto y cobro

Ya están cargados en el sitio:

- **WhatsApp:** +54 9 3434 66-9310 (en `js/main.js`, `CONFIG.whatsappNumber`)
- **Email:** calamayoristasya@gmail.com (`index.html`, `privacidad.html`, `terminos.html`)
- **Instagram:** [@mayoristasargenti](https://www.instagram.com/mayoristasargenti)
- **TikTok:** [@mayoristasarg](https://www.tiktok.com/@mayoristasarg)
- **Transferencia:** Valentin Francisco Vergara Guarascio · CBU `0000076500000017215693` ·
  alias `Valen.guarascio` (en `js/main.js`, `CONFIG.transfer`; se incluyen en el mensaje de WhatsApp
  que se arma al confirmar el pedido)

## Antes de publicar

1. **Dominio.** Todo el sitio apunta a `mayoristasarg.com` (`CNAME`, `robots.txt`, `sitemap.xml`,
   canonical y Open Graph en los 3 HTML). Si el dominio final es otro, reemplazar esas ocurrencias.
2. **Google Analytics.** En `js/analytics.js`, reemplazar `G-XXXXXXXXXX` por el ID de medición del
   sitio nuevo. Mientras diga `XXXXXXXXXX` no se carga nada y el sitio funciona igual.
3. **Google Search Console.** En `index.html`, dentro del `<head>`, pegar el meta de verificación del
   dominio nuevo (hay un comentario marcando el lugar).
4. **Registro de pedidos (opcional).** En `js/orders.js`, pegar la URL de la Web App de Google Apps
   Script (`google-apps-script.gs`) para que cada pedido quede guardado en una planilla.
5. **`downloads/guia-reventa.pdf`.** Es el PDF del sitio original; si tiene marca adentro, reemplazarlo.

## Packs

El sitio vende 3 packs: **Pack 100** ($4.999), **Pack 500** ($14.999) y **Pack 1000** ($19.999).
Se editan en la sección `#precios` de `index.html` (los datos de cada botón `js-add-cart` —
`data-id`, `data-name`, `data-price`, `data-price-label` — son los que usa el carrito).
