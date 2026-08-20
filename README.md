# Economía del Conocimiento — TIC y Robótica, Salta
### Sitio estático con los tableros del Componente 1 (Programa AR-L1386, BID)

Este sitio contiene 3 páginas HTML autocontenidas (sin backend, sin build,
sin dependencias que instalar — Chart.js se carga desde un CDN):

- `index.html` — página de inicio con enlaces a los dos tableros.
- `contexto.html` — tablero del Diagnóstico de Contexto (Entregable 2).
- `indice.html` — tablero del Índice IA-EdC (Entregable 3A).

---

## Opción 1: Subir por drag & drop (la más rápida, sin instalar nada)

1. Andá a **https://vercel.com** y creá una cuenta (podés usar GitHub, Google o email).
2. Andá a **https://vercel.com/new**.
3. Buscá la opción "Deploy without Git" / arrastrá la carpeta `sitio/` completa
   (con los 3 archivos .html adentro) directo al navegador.
4. Vercel detecta automáticamente que es un sitio estático y lo publica.
5. En 30-60 segundos te da una URL pública (algo como `tu-proyecto.vercel.app`).

## Opción 2: Vercel CLI (si tenés Node.js instalado)

```bash
npm install -g vercel     # solo la primera vez
cd sitio
vercel                    # sigue las instrucciones en pantalla (login + deploy)
vercel --prod             # para publicar la versión definitiva
```

## Opción 3: Conectado a GitHub (recomendado si vas a seguir iterando)

1. Creá un repositorio en GitHub y subí la carpeta `sitio/` (los 3 .html).
2. En **https://vercel.com/new**, elegí "Import Git Repository" y seleccioná ese repo.
3. Dejá la configuración por defecto (Framework Preset: "Other", sin build command).
4. Cada vez que hagas `git push`, Vercel vuelve a publicar el sitio automáticamente.

---

## Notas

- No hace falta ningún archivo de configuración (`vercel.json`) — al ser HTML
  estático puro, Vercel lo sirve tal cual.
- Si querés un dominio propio (ej. `edc-salta.com`), se agrega desde el panel
  del proyecto en Vercel → Settings → Domains, una vez desplegado.
- Los datos de los gráficos están **embebidos directamente en el HTML**
  (no se leen de ninguna base de datos externa), así que el sitio funciona
  igual de rápido sin necesitar backend ni configurar variables de entorno.
- Si en el futuro actualizás los datos, solo hay que reemplazar el archivo
  `.html` correspondiente y volver a desplegar (drag & drop de nuevo, o
  `git push` si usás la Opción 3).
