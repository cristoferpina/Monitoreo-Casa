<div align="center">

<sub>CRISTOFER PIÑA · DESARROLLO DE SOFTWARE</sub>

# Casa inteligente

**El hogar, desde un panel de control.**

Interfaces para consultar el estado de una casa inteligente y explorar sus registros de monitoreo.

<img alt="HTML" src="https://img.shields.io/badge/HTML-0F172A?style=for-the-badge" />
<img alt="CSS" src="https://img.shields.io/badge/CSS-1D4ED8?style=for-the-badge" />
<img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-0F766E?style=for-the-badge" />

[Código fuente](https://github.com/cristoferpina/Monitoreo-Casa) &nbsp; / &nbsp; [Incidencias](https://github.com/cristoferpina/Monitoreo-Casa/issues) &nbsp; / &nbsp; [Perfil](https://github.com/cristoferpina)

</div>

## Una mirada al proyecto

| Qué encontrarás | Por qué explorarlo |
| --- | --- |
| El hogar, desde un panel de control. | Interfaces para consultar el estado de una casa inteligente y explorar sus registros de monitoreo. |
| Trabajo de desarrollo | Diseño de un dashboard, pantallas de acceso y organización de recursos de una interfaz web. |

**[Explora las pantallas y recursos →](casa_inteligente/)**



---

[Qué incluye](#seccion-1) · [Objetivo](#seccion-2) · [Estructura del repositorio](#seccion-3) · [Cómo probar (modo estático)](#seccion-4) · [Uso con backend (opcional)](#seccion-5)

---

Proyecto web para visualización y monitoreo de una "casa inteligente". Contiene las vistas, estilos y recursos estáticos necesarios para un panel de control (dashboard), interfaz de inicio de sesión y páginas de registro/monitoreo.

<a id="seccion-1"></a>

## Qué incluye

- **Interfaz de usuario:** archivos HTML en la carpeta `templates` (`dashboard.html`, `login.html`, `record.html`).
- **Estilos:** CSS en la carpeta `css` (`dashboard.css`, `login.css`).
- **Recursos:** imágenes en `images/`, videos en `video/`, y otros recursos estáticos en `static/`.
- **Código cliente:** carpeta `js/` para scripts de frontend.
- **Módulos de monitoreo:** carpeta `monitoreo/` para recursos relacionados con la captura o visualización de datos de sensores.

<a id="seccion-2"></a>

## Objetivo

Proveer una interfaz sencilla para:

- Iniciar sesión y autenticar usuarios (interfaz de `login.html`).
- Visualizar el estado y métricas de la casa (panel en `dashboard.html`).
- Revisar y reproducir registros o grabaciones (`record.html` y `video/`).
- Servir como base para integrar lógica backend (por ejemplo, una API en Flask o Node) que alimente las vistas con datos en tiempo real.

<a id="seccion-3"></a>

## Estructura del repositorio

- `templates/` — Plantillas HTML.
- `css/` — Hojas de estilo.
- `js/` — Scripts cliente.
- `images/` — Imágenes del proyecto.
- `video/` — Grabaciones o recursos de video.
- `monitoreo/` — Código o datos relacionados con el monitoreo.
- `static/` — Recursos estáticos adicionales.

<a id="seccion-4"></a>

## Cómo probar (modo estático)

Si sólo quieres abrir y revisar las páginas estáticas localmente, puedes abrir los archivos HTML con el navegador o iniciar un servidor HTTP simple:

```powershell
# Desde la raíz del proyecto (Windows PowerShell)
cd casa_inteligente
python -m http.server 8000
# Abrir en el navegador: http://localhost:8000/templates/dashboard.html
```

<a id="seccion-5"></a>

## Uso con backend (opcional)

Para integrar con un servidor (por ejemplo Flask o Express):

- Crear un pequeño backend que sirva las plantillas y exponga endpoints para datos de sensores.
- Asegurar rutas estáticas para `css/`, `js/`, `images/` y `video/`.

Ejemplo mínimo con Flask (esquema):

```python
from flask import Flask, render_template
app = Flask(__name__)

@app.route('/')
def dashboard():
    return render_template('dashboard.html')

if __name__ == '__main__':
    app.run(debug=True)
```

---

<div align="center">
<sub>Desarrollado por <a href="https://github.com/cristoferpina">Cristofer Piña</a></sub>
</div>
