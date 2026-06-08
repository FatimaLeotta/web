# Fátima Leotta — Sitio web

Sitio estático listo para publicar. Incluye el Home + las 3 landings
(Founders, RRHH y Profesionales) en un solo `index.html`.

```
index.html     → todo el sitio (Home + 3 landings) con las imágenes,
                 fuentes y logos YA incrustados dentro del archivo
styles.css     → todos los estilos (fuentes Sentient + DM Sans ya incrustadas)
vercel.json    → configuración de Vercel (sitio estático, sin build)
```

No hay carpeta de imágenes: todas las fotos y logos están embebidos dentro
del `index.html`, así que no se pueden "perder" al subir el repo. No hay
paso de compilación. React y los videos de YouTube se cargan por CDN, así
que la primera carga necesita internet.

---

## Subir a GitHub

1. Creá un repositorio nuevo en https://github.com/new (por ej. `fatima-leotta-web`).
2. **Importante:** subí el *contenido* de esta carpeta, no la carpeta entera.
   El `index.html` tiene que quedar en la raíz del repositorio.
   - Opción fácil (web): en el repo nuevo → **Add file → Upload files** →
     arrastrá `index.html`, `styles.css`, `vercel.json` y `README.md`.
     → **Commit changes**.
   - Opción terminal:
     ```bash
     cd publicar
     git init
     git add .
     git commit -m "Sitio Fátima Leotta"
     git branch -M main
     git remote add origin https://github.com/TU-USUARIO/fatima-leotta-web.git
     git push -u origin main
     ```

> Este paquete pesa ~7 MB, muy por debajo del límite de 25 MB de GitHub.
> (El error anterior era porque se subía el proyecto completo con archivos
> de trabajo. Acá va sólo lo necesario para publicar.)

## Deployar en Vercel

1. Entrá a https://vercel.com y hacé login con tu cuenta de GitHub.
2. **Add New… → Project** → elegí el repositorio que acabás de subir.
3. Framework Preset: **Other** (no hace falta build command ni output dir).
4. **Deploy**. En segundos tenés una URL pública (`https://tu-proyecto.vercel.app`).
5. Para tu dominio: **Settings → Domains** y agregá `fatima-leotta.com`.

Cada vez que actualices el repo en GitHub, Vercel redeploya automáticamente.
