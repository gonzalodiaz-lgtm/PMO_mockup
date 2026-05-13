# PMO_mockup

Mockups HTML estáticos del **Portal PMO — Polpaico** para compartir por enlace.

## Contenido

| Archivo | Descripción |
|--------|-------------|
| `index.html` | Página de entrada con enlaces a los dos mockups |
| `mockup-resumen.html` | Vista tipo tablero / resumen |
| `mockup-proyectos.html` | Vista listado de proyectos |

En **Resumen** y **Proyectos**, la barra superior enlaza entre ambas páginas. Cada HTML incluye un script que fija `<base href>` según la URL real (GitHub Pages con o sin barra final, `file://` en Windows, etc.) para que los enlaces relativos no se rompan.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub y sube esta carpeta (o haz push si ya tienes el repo clonado).
2. En el repo: **Settings** → **Pages** (menú izquierdo).
3. En **Build and deployment** → **Source**, elige **Deploy from a branch**.
4. Rama: normalmente **`main`** (o `master`). Carpeta: **`/ (root)`**.
5. Guarda. En uno o dos minutos el sitio quedará en:

   `https://<tu-usuario>.github.io/<nombre-del-repo>/`

   La URL principal abrirá `index.html` automáticamente.

### Notas

- El archivo **`.nojekyll`** evita que GitHub trate el sitio como proyecto Jekyll y altere archivos estáticos.
- Si el repositorio es **privado**, comprueba en la documentación de GitHub si tu plan permite Pages en repos privados (en cuentas gratuitas a veces el sitio es público aunque el repo sea privado).

## Probar en local

Desde esta carpeta, con Python:

```bash
python -m http.server 8080
```

Abre `http://localhost:8080/`.
