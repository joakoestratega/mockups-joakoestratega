# Cómo subir el mockup "ecuador" a GitHub sin dañar lo existente

## Qué vas a subir

Esta carpeta `ecuador/` contiene:

- `index.html` — la página (antes "Ecuador - Feria Effix 2026 MEJORADO.html", renombrada para que GitHub Pages la sirva como portada)
- `assets/` — toda la carpeta `Ecuador - Feria Effix 2026_files` renombrada (sin espacios en el nombre para evitar problemas de rutas)
- Todas las referencias dentro del HTML ya fueron actualizadas de `Ecuador - Feria Effix 2026_files/...` a `assets/...`

## Dónde va en el repo

El repo `mockups-joakoestratega` actualmente tiene:

```
mockups-joakoestratega/
└── feria-effix/
    └── digitalex/     ← mockup existente (NO tocar)
```

Tu nuevo mockup debe quedar así, al lado del que ya existe:

```
mockups-joakoestratega/
└── feria-effix/
    ├── digitalex/     ← existente, intacto
    └── ecuador/       ← NUEVO (lo que vas a subir)
        ├── index.html
        └── assets/
```

Una vez subido, la URL pública será:

```
https://joakoestratega.github.io/mockups-joakoestratega/feria-effix/ecuador/
```

---

## Opción A — Subir desde la web de GitHub (sin tocar consola)

Esta es la forma más segura de no dañar `digitalex/`, porque solo agregas archivos nuevos.

1. Entra al repo: https://github.com/joakoestratega/mockups-joakoestratega
2. Click en la carpeta `feria-effix/` para entrar.
3. Arriba a la derecha, click en **"Add file"** → **"Upload files"**.
4. **IMPORTANTE:** antes de soltar los archivos, en la barra de ruta que aparece arriba del área de upload, escribe `ecuador/` al final de la ruta actual. Debe quedar:
   ```
   mockups-joakoestratega / feria-effix / ecuador /
   ```
   Así GitHub creará la carpeta `ecuador` automáticamente al subir.
5. Arrastra desde tu explorador de Windows:
   - El archivo `index.html`
   - La carpeta completa `assets/`

   (GitHub preserva la estructura de carpetas al arrastrar.)
6. Abajo, en "Commit changes":
   - Título: `Add ecuador mockup`
   - Deja marcada la opción **"Commit directly to the `main` branch"**
7. Click en **"Commit changes"**.

Espera 1-2 minutos a que GitHub Pages actualice y entra a:
```
https://joakoestratega.github.io/mockups-joakoestratega/feria-effix/ecuador/
```

**Por qué esto NO daña `digitalex/`:** solo estás creando una carpeta nueva. GitHub hace un merge aditivo, no reemplaza nada existente.

---

## Opción B — Subir por Git (terminal)

Solo si ya tienes el repo clonado localmente.

```bash
# 1. Entra a tu copia local del repo
cd ruta/a/mockups-joakoestratega

# 2. Asegúrate de estar al día
git pull origin main

# 3. Copia la carpeta ecuador dentro de feria-effix/
#    (ajusta la ruta de origen a donde está esta carpeta en tu PC)
cp -r "/c/Users/JoaquínRojasPeña/Documents/CLAUDE CODE - JOAKO ESTRATEGA/JOAKO ESTRATEGA AGENTE/OUTPUT/GITHUB-PAGES/feria-effix/ecuador" feria-effix/

# 4. Verifica que digitalex sigue intacto
ls feria-effix/
# debe mostrar: digitalex  ecuador

# 5. Commit y push
git add feria-effix/ecuador
git commit -m "Add ecuador mockup"
git push origin main
```

---

## Verificación después de subir

1. Entra al repo en GitHub y confirma que ves DOS carpetas dentro de `feria-effix/`: `digitalex/` y `ecuador/`.
2. Abre la URL del nuevo mockup: `https://joakoestratega.github.io/mockups-joakoestratega/feria-effix/ecuador/`
3. Confirma que las imágenes, fuentes y estilos cargan bien (si algo se ve roto, probablemente quedó una referencia a `Ecuador - Feria Effix 2026_files` sin reemplazar; avísame).
4. Confirma que la URL anterior de digitalex sigue funcionando igual que antes.

---

## Notas

- El archivo `index.html` es más liviano que el original porque se eliminaron los prefijos largos de rutas. El contenido visual es idéntico.
- La carpeta `assets/` tiene 60 archivos (imágenes, CSS, JS, fuentes) que son todo lo que el HTML necesita para renderizar sin conexión.
- Si en el futuro quieres subir otra versión (ej: ecuador-v2), repite este mismo proceso con otra carpeta al lado. Nunca reemplaces en caliente una carpeta existente desde la web de GitHub sin antes eliminarla; es más seguro crear versiones nuevas.
