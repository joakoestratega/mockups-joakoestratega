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
| `README.md` | Este archivo. |
| `.gitignore` | Configuración para Git. |

El reel del Gerente Juan Carmona se carga directamente desde Instagram a
través de un embed (URL pública del reel:
[instagram.com/p/DX0HDHLO8p4](https://www.instagram.com/p/DX0HDHLO8p4/)),
así que **no es necesario subir ningún video** al repositorio.

La landing usa Google Fonts (Montserrat) y las imágenes oficiales de Feria EFFIX
desde su dominio. No requiere instalar nada para verla.

---

## URL pública

Una vez activado GitHub Pages en este repositorio, la landing queda visible en:

```
https://joakoestratega.github.io/mockups-joakoestratega/landing-zona-traffickers/
```

Esa es la URL para compartir en evaluaciones internas.

---

## Cómo activar GitHub Pages (una sola vez)

1. En el repositorio `mockups-joakoestratega`, haz clic en la pestaña **Settings**.
2. En el menú izquierdo, haz clic en **Pages**.
3. En la sección **Source**, selecciona:
   - Source: **Deploy from a branch**
   - Branch: **main** y carpeta **/ (root)**
4. Haz clic en **Save**.
5. Espera entre uno y tres minutos. Refresca la página.
6. Aparecerá un mensaje verde con la URL pública del repo. La landing
   específica está en la subruta `/landing-zona-traffickers/`.

---

## Recomendaciones para la evaluación

1. **Probar el reel.** Debe cargar directo desde Instagram en la sección
   "Escucha al CEO de Feria EFFIX". Si Instagram cambia el video o el reel
   se borra, la sección queda vacía hasta que se actualice la URL.

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
- El reel se carga vía `iframe` desde Instagram (`/embed/`). Si la cuenta
  pone el reel privado o lo borra, hay que actualizar la URL en el HTML.
- La landing pesa menos de 50 KB (sin contar fuentes ni imágenes externas
  que se cargan desde feriaeffix.com).
- La paleta de colores y la tipografía heredan la identidad oficial de
  Feria EFFIX (azul `#194D7E`, gris violeta `#73708E`, Montserrat).

---

## Para actualizar la landing después

Cualquier cambio futuro al `index.html` o este README se sube al mismo
repositorio. GitHub Pages republica el sitio automáticamente entre uno y
cinco minutos después del push, sin volver a configurar nada.

---

**Coordina:** Joako Estratega para Feria EFFIX
**Canal oficial de comunicación:** Instagram [@feriaeffix](https://www.instagram.com/feriaeffix/)