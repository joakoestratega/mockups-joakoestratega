# Zona Traffickers · Feria EFFIX 2026

Landing de la convocatoria a la Zona Traffickers dentro de Feria EFFIX 2026,
del 16 al 18 de octubre de 2026 en Plaza Mayor, Medellín, con acceso exclusivo
al evento de inauguración el 15 de octubre.

Esta carpeta contiene la versión publicable de la landing para evaluación
pública antes del montaje definitivo en `feriaeffix.com/traffickers/`.

---

## Qué hay en esta carpeta

| Archivo | Qué es |
|---|---|
| `index.html` | Landing completa, autocontenida. Se sirve directamente al abrirla. |
| `video-juan-zona-traffickers.mp4` | Reel de Juan Carmona (Gerente de Feria EFFIX) presentando la zona. Formato vertical 9:16, 76 MB. |
| `README.md` | Este archivo. |
| `.gitignore` | Configuración para Git. |

La landing usa Google Fonts (Montserrat) y las imágenes oficiales de Feria EFFIX
desde su dominio. No requiere instalar nada para verla.

---

## Cómo subirla a GitHub y publicarla

### Paso 1. Crear el repositorio

1. Ingresa a [github.com](https://github.com) e inicia sesión.
2. Haz clic en el botón **+** arriba a la derecha y selecciona **New repository**.
3. Pon un nombre, por ejemplo `zona-traffickers-landing`.
4. Marca el repositorio como **Public** (necesario para que GitHub Pages funcione gratis).
5. **No** marques "Add a README file" (ya tenemos uno).
6. Haz clic en **Create repository**.

### Paso 2. Subir los archivos

**Opción A · Por la interfaz web (más fácil)**

1. En la página del repo recién creado, haz clic en **uploading an existing file**.
2. Arrastra los cuatro archivos de esta carpeta (`index.html`, `video-juan-zona-traffickers.mp4`, `README.md`, `.gitignore`).
3. Espera a que el video termine de subir (puede tardar uno a tres minutos según tu conexión).
4. En el campo de commit, escribe `Subo la landing inicial`.
5. Haz clic en **Commit changes**.

**Opción B · Con GitHub Desktop**

1. Descarga [GitHub Desktop](https://desktop.github.com/) si no lo tienes.
2. Clona el repositorio recién creado.
3. Copia los cuatro archivos a la carpeta clonada.
4. Desde GitHub Desktop, haz commit con un mensaje y push.

### Paso 3. Activar GitHub Pages

1. En el repositorio, haz clic en la pestaña **Settings**.
2. En el menú izquierdo, haz clic en **Pages**.
3. En la sección **Source**, selecciona:
   - Source: **Deploy from a branch**
   - Branch: **main** y carpeta **/ (root)**
4. Haz clic en **Save**.
5. Espera entre uno y tres minutos. Refresca la página.
6. Aparecerá un mensaje verde con la URL pública, algo como:
   ```
   https://[tu-usuario].github.io/zona-traffickers-landing/
   ```

Esa es la URL que puedes compartir para evaluación.

---

## Recomendaciones para la evaluación

1. **Probar el video.** El reel debe reproducirse al hacer clic en el botón
   de play. Si no carga, espera unos segundos por la primera reproducción
   (es normal con archivos grandes en GitHub Pages).

2. **Probar el banner fijo.** Al hacer scroll, la barra superior con el botón
   POSTULARME debe quedar visible siempre.

3. **Probar el responsive.** Abrir la URL desde celular para verificar que
   se vea bien en móvil. La pantalla del celular es donde más entran los
   traffickers a aplicar.

4. **Probar el formulario.** Los campos se ven, pero el botón ENVIAR no
   manda nada en esta versión (es solo réplica visual del formulario actual
   de Elementor). Cuando se monte en `feriaeffix.com/traffickers/`, se
   conecta el widget real con su lógica.

---

## Notas técnicas

- El HTML es standalone: no usa frameworks ni dependencias instaladas.
- El video pesa 76 MB. Está dentro del límite de GitHub (100 MB por archivo)
  y de GitHub Pages (1 GB por sitio, 100 GB de ancho de banda mensual).
- Para producción definitiva en `feriaeffix.com/traffickers/`, lo recomendable
  es subir el video a la biblioteca de medios de WordPress y reemplazar el
  `src` del `<source>` en el HTML por la URL de WordPress, o embeber
  directamente el reel desde Instagram.
- La paleta de colores y la tipografía heredan la identidad oficial de
  Feria EFFIX (azul `#194D7E`, gris violeta `#73708E`, Montserrat).

---

## Para actualizar la landing después

Cualquier cambio futuro al HTML, video o este README se sube al mismo
repositorio. GitHub Pages republica el sitio automáticamente entre uno y
cinco minutos después del push, sin volver a configurar nada.

---

**Coordina:** Joako Estratega para Feria EFFIX
**Canal oficial de comunicación:** Instagram [@feriaeffix](https://www.instagram.com/feriaeffix/)