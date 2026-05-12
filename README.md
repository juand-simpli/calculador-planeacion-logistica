# Calculador de Planeación Logística — SimpliRoute

Herramienta web ligera para dimensionar operaciones de última milla a partir de cuatro variables clave: **número de visitas**, **número de vehículos**, **jornada laboral** y **rapidez de entrega** (visitas por hora-vehículo). Selecciona la variable a calcular y la herramienta resuelve el resto.

Pensada para definir con criterio los inputs de planeación que se cargan en [SimpliRoute](https://simpliroute.com/).

---

## Contenido del repositorio

```
.
├── index.html                          # Punto de entrada de la herramienta
├── Logo_positivo_ES_1.png              # Logo SimpliRoute (positivo, ES)
└── README.md                           # Este archivo
```

`index.html` es 100% autocontenido: solo necesita estar en la misma carpeta que `Logo_positivo_ES_1.png`. Sin dependencias de Node, build, ni framework.

---

## Vista previa local

Cualquiera de estas tres opciones funciona:

**Opción A — Doble clic** sobre `index.html`. Se abre directo en el navegador.

**Opción B — Servidor local con Python** (recomendado, evita restricciones de CORS):

```bash
cd ruta/a/la/carpeta
python -m http.server 8000
```

Luego abre <http://localhost:8000> en tu navegador.

**Opción C — Servidor local con Node:**

```bash
npx serve
```

---

## Publicar en internet

### Opción 1 · GitHub Pages (recomendada si quieres versionar y mantener)

1. Crea un repositorio nuevo en GitHub, por ejemplo `calculador-planeacion-logistica`.
2. Sube los tres archivos (`index.html`, `Logo_positivo_ES_1.png`, `README.md`) a la rama `main`:

   ```bash
   git init
   git add .
   git commit -m "Versión inicial del calculador"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/calculador-planeacion-logistica.git
   git push -u origin main
   ```

3. En GitHub → **Settings → Pages**, selecciona:
   - Source: `Deploy from a branch`
   - Branch: `main` / carpeta `/ (root)`
4. Guarda y espera ~1 minuto. La URL queda en:

   ```
   https://TU_USUARIO.github.io/calculador-planeacion-logistica/
   ```

Cada `git push` que hagas se publica automáticamente.

### Opción 2 · Netlify Drop (la más rápida, sin Git)

1. Comprime los tres archivos en un `.zip` (o arrastra la carpeta completa).
2. Ve a <https://app.netlify.com/drop>.
3. Arrastra y suelta. Listo: en 30 segundos tienes URL pública con HTTPS.
4. Desde el panel puedes cambiar el subdominio (`xxx.netlify.app`) o conectar uno propio.

### Opción 3 · Cloudflare Pages

1. Crea cuenta gratuita en <https://pages.cloudflare.com/>.
2. **Create a project → Direct Upload** (o conecta tu repo de GitHub).
3. Sube la carpeta. URL queda en `xxx.pages.dev`.

Cloudflare ofrece el CDN más rápido del mercado, ancho de banda ilimitado y 500 builds gratis al mes.

### Opción 4 · Vercel

1. Crea cuenta en <https://vercel.com/>.
2. **Add New → Project → Import** (conecta GitHub) o usa `vercel deploy` desde CLI.
3. URL queda en `xxx.vercel.app`.

---

## Dominio propio (opcional)

Si quieres usar un subdominio corporativo, todas las opciones soportan dominio custom gratis:

| Plataforma | Configuración |
|---|---|
| GitHub Pages | Añadir archivo `CNAME` con el dominio + configurar registros DNS tipo `CNAME` apuntando a `TU_USUARIO.github.io` |
| Netlify / Vercel / Cloudflare Pages | Panel del proyecto → "Domains" → añadir dominio → seguir las instrucciones DNS |

Sugerencia: `calculador.simplit-solutions.com` o `herramientas.simplit-solutions.com`.

---

## Mantenimiento

Para actualizar la herramienta:

1. Edita `index.html`.
2. Si publicas en GitHub Pages: `git add . && git commit -m "Cambio X" && git push`.
3. Si publicas en Netlify/Vercel/Cloudflare: vuelve a arrastrar la carpeta o haz push al repo conectado.

Los cambios se reflejan en menos de un minuto.

---

## Créditos

- Marca, paleta y logo: [SimpliRoute](https://simpliroute.com/)
- Herramienta desarrollada en **2026**.

© 2026
