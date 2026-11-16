# Catálogo Cuero Barra — reglas para el proyecto

Catálogo web estático (HTML + CSS + JavaScript sin frameworks ni dependencias), publicado con GitHub Pages desde `main`.

## Estructura
- `index.html` — diseño (CSS en `<style>`), estructura de la página y lógica (JS al final: filtros, búsqueda, ficha/modal, WhatsApp, envíos).
- `data.js` — **datos editables**: `WA_NUMBER`, orden de categorías, íconos, colores, distritos/costos de envío y la lista `productos`.
- `manifest.webmanifest` — datos de la app instalable (PWA).

## Producto (en `data.js`)
`{code, name, cat, price, priceOld?, liquidacion?, medidas, emoji, colores[], tiktok, img}`
- `code` es el identificador (búsqueda, enlace `?p=CODIGO`, mensajes de WhatsApp). Debe ser único.
- `priceOld` > `price` o `liquidacion:true` → aparece en Liquidación con descuento.
- `img`: una sola imagen principal (URL de barraleather.com/wp-content/uploads).

## Reglas obligatorias
- No cambiar precios, códigos, categorías ni el número/enlaces de WhatsApp sin autorización expresa.
- No eliminar productos ni funcionalidades.
- No agregar dependencias ni pasos de compilación.
- Trabajar en una rama y pedir aprobación antes de fusionar a `main` (fusionar = publicar).
- Logos oficiales: `cuero-barra-logo-blanco.webp` en fondos oscuros (header, footer); `cuero-barra-logo-negro.webp` en fondos claros. No aplicarles filtros CSS ni deformarlos.

## Verificación antes de publicar
Abrir `index.html` en el navegador (escritorio y celular): sin errores en consola, 145+ productos, filtros, búsqueda por código, ficha (`?p=MV01`), botones de WhatsApp y calculadora de envío.
