# Mockup CRO — Página oficial de boletas Feria EFFIX 2026 (precio full)

**Fecha:** 2026-06-09
**Archivo:** `index.html` (abrir en navegador, los assets están en `assets/`)
**Base visual:** réplica fiel de la página oficial de Feria EFFIX (misma estructura audiovisual, mismos colores, mismas imágenes). Solo se aplicaron los ajustes CRO acordados con Joako.

Este es el mockup para revisar y publicar. No es un borrador: el HTML es la landing oficial. Los `href` con placeholder se reemplazan por la URL real antes de subir (ver abajo).

---

## Ajustes aplicados (lo que se cambió respecto a la página actual)

1. **Gancho primario en texto (no en imagen).** Headline: *"La mejor feria de comercio electrónico del mundo"*. Subtítulo de dolor sencillo: *"En 3 días encuentras todo lo que tu negocio necesita para vender más por internet"*. Datos: 60.000 personas · +300 ponentes · +350 empresas · 16-17-18 oct · Plaza Mayor.
2. **Contador oculto.** No hay fecha autorizada de cambio de etapa ni de precio, así que se quitó todo contador regresivo.
3. **Precio General visible como argumento de valor.** Título de precios: *"3 días, +300 ponentes y +350 empresas por $201.300"*.
4. **Sección de dolor nueva** (estilo Digitalex), en el idioma del cliente.
5. **Sección "Lo que tu negocio busca, aquí está"**: IA, proveedores dropshipping, filmmakers, agencias de tráfico, contadores ecommerce, aliados.
6. **Prueba social sin cifras prohibidas.** Se eliminaron "150.000 acumulados", "95% vuelve" y la "historia de los 20.000 comentarios". Quedan solo datos que le sirven al comprador: +350 empresas, +300 ponentes, +160 conferencias, 5 ediciones, +50.000 por edición.
7. **Barra fija superior** con botón "Comprar mi entrada" (móvil y escritorio). Documentada como componente reutilizable en `SCRIPTS/componentes-web/barra-sticky-cta.md`.
8. **Botones con micro-animación** (latido) para que el ojo los encuentre.
9. **Jerarquía de botones: VIP domina.** El VIP es la tarjeta más grande y centrada (etiqueta "Recomendada"); General y Black quedan un poco más pequeños a los lados.
10. **VIP y Black ahora son 5 días** (jueves 15 al lunes 19 de octubre). General sigue siendo 3 días (16-18). Reflejado en tarjetas, tabla comparativa y FAQ. También se actualizó la base de datos del cliente (`06-contexto-ia.md` y `09-cliente-final.md`).
11. **Tabla comparativa** de los 3 tickets, a precio full (sin fila de oferta).
12. **FAQ reescritas para vender** (vencen objeciones de compra, no solo logística).
13. **Precios:** Pasaporte $201.300 · VIP $1.155.000 · Black $3.997.000.

---

## PENDIENTE antes de publicar (reemplazos)

- **Checkout por ticket.** Cada botón de compra debe ir al checkout directo de su entrada en latiquetera. Hoy los tres apuntan a la URL general del evento como placeholder. Buscar en el HTML los comentarios `<!-- REEMPLAZAR href ... -->`:
  - `data-ticket="general"` → checkout directo Pasaporte 3 días
  - `data-ticket="vip"` → checkout directo VIP
  - `data-ticket="black"` → checkout directo Black
- **Validar precio Black.** Se usó $3.997.000 (precio oficial documentado). Confirmar con el equipo si el vigente es ese o $4.000.000.
- **Pixel y tracking.** Este mockup no trae Meta Pixel / GTM / Clarity. Al montarlo en el sitio real, conservar los pixeles que ya tiene la página oficial.
- **Planimetría / testimonios.** Usan las imágenes de la base; reemplazar por las definitivas 2026 si las hay.

---

---

## Sección de ponentes (agregada tras auditoría)

Carrusel horizontal deslizable con los afiches verticales de ponentes confirmados (Juan ID, Alejandra Rincón, Felipe Vergara, Pamela Richter) más una tarjeta de cierre "+300 ponentes en total". Las imágenes están en `assets/ponente-*`.

**Cómo agregar más ponentes (para el equipo de desarrollo):** dentro de `<section class="ponentes">`, duplicar un bloque `<div class="ponente-card"><img src="assets/ponente-XXX.webp" ...></div>` por cada afiche nuevo y subir su imagen a `assets/`. El carrusel crece solo, sin tocar el CSS. Los afiches son verticales 4:5 y ya traen nombre y credenciales incrustados, así que no hay que escribir texto aparte. La tarjeta "+300" se mantiene siempre al final.

---

## Para el equipo de desarrollo

- Es una página estática: `index.html` + carpeta `assets/`. Se puede montar tal cual o portar el HTML/CSS al sitio actual (WordPress/Elementor).
- **Mantiene la misma identidad visual** de la página oficial (negro, dorado, tipografías, estilo de títulos).
- **Reemplazos obligatorios antes de publicar:** los 3 botones de compra (`data-ticket="general|vip|black"`) apuntan hoy a la URL general de La Tiquetera; cambiar cada `href` por el checkout directo de su ticket (ver comentarios `<!-- REEMPLAZAR href -->`). Completar los enlaces legales del footer (hoy en `#`).
- **Conservar los pixeles** (Meta, GTM, Clarity) de la página oficial al integrarla; este mockup no los trae.
- Quedó **CSS sin uso** de la versión anterior (`.countdown`, `.capsula-oferta-hero`, `.sello-digitalex-hero`); no afecta el render, pero se puede limpiar.

---

*Ver lista completa de recomendaciones CRO y razonamiento estratégico en el LOG-OPERATIVO de feria-effix.*
