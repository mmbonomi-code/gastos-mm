# Instrucciones de instalación — Gastos M&M

## Archivos entregados
- `Code.gs` — Backend (Google Apps Script)
- `index.html` — La app (PWA)
- `manifest.json` — Hace que la app sea instalable en el teléfono

---

## PASO 1: Configurar Google Sheets

1. Abrí Google Sheets: https://sheets.google.com
2. Creá una nueva planilla y llamala "Gastos M&M"
3. Abrí: **Extensiones → Apps Script**
4. Borrá todo el contenido del editor
5. Pegá el contenido de `Code.gs`
6. Guardá (Ctrl+S o ⌘+S)
7. En el selector de funciones, elegí **setup**
8. Hacé clic en ▶ (Ejecutar)
   - Va a pedir permisos — aceptalos
   - Deberías ver "Setup completado"

---

## PASO 2: Publicar el script como Web App

1. Clic en **Implementar → Nueva implementación**
2. Tipo: **Aplicación web**
3. Configuración:
   - Ejecutar como: **Yo**
   - Quién tiene acceso: **Cualquier persona**
4. Clic en **Implementar**
5. **Copiá la URL** que aparece (empieza con `https://script.google.com/macros/s/...`)
   
⚠️ Guardá esta URL, la vas a necesitar en el siguiente paso.

---

## PASO 3: Subir la app a GitHub Pages (gratis)

1. Creá una cuenta en https://github.com (si no tenés)
2. Creá un nuevo repositorio público (ej: `gastos-mm`)
3. Subí los 3 archivos: `index.html`, `manifest.json`
   - (Para `manifest.json`, actualizá `"start_url": "/gastos-mm/index.html"` con el nombre de tu repo)
4. Activá GitHub Pages:
   - Settings → Pages → Source: **main branch / root**
5. Tu app va a estar disponible en:
   `https://TU_USUARIO.github.io/gastos-mm`

---

## PASO 4: Conectar la app con la planilla

1. Abrí la URL de la app desde Chrome en el teléfono
2. Va a aparecer la pantalla de configuración
3. Pegá la URL del Apps Script del Paso 2
4. Clic en **Conectar**

---

## PASO 5: Instalar en el teléfono

### Android (Chrome)
1. Abrí la URL de la app en Chrome
2. Menú (⋮) → **Agregar a pantalla de inicio**
3. Listo — aparece el ícono como una app nativa

### iPhone (Safari)
1. Abrí la URL en Safari (no Chrome)
2. Clic en el botón compartir (cuadrado con flecha)
3. **Agregar a pantalla de inicio**
4. Listo

---

## PASO 6: Editar categorías y medios de pago

Para agregar o quitar categorías o medios de pago:
1. Abrí la planilla de Google Sheets
2. Ir a la pestaña **Categorías** o **Medios de Pago**
3. Editá la lista directamente
4. La app los carga en tiempo real — no hace falta tocar código

---

## Datos en la planilla

Todos los gastos quedan guardados en la pestaña **Gastos** con estas columnas:
`ID | Fecha | Descripción | Monto | Categoría | Medio de Pago | Quién Pagó | Timestamp`

Podés filtrar, ordenar y generar gráficos directamente en Sheets si querés análisis más avanzados.
