# Casa Inteligente

Proyecto web para visualización y monitoreo de una "casa inteligente". Contiene las vistas, estilos y recursos estáticos necesarios para un panel de control (dashboard), interfaz de inicio de sesión y páginas de registro/monitoreo.

## Qué incluye

- **Interfaz de usuario:** archivos HTML en la carpeta `templates` (`dashboard.html`, `login.html`, `record.html`).
- **Estilos:** CSS en la carpeta `css` (`dashboard.css`, `login.css`).
- **Recursos:** imágenes en `images/`, videos en `video/`, y otros recursos estáticos en `static/`.
- **Código cliente:** carpeta `js/` para scripts de frontend.
- **Módulos de monitoreo:** carpeta `monitoreo/` para recursos relacionados con la captura o visualización de datos de sensores.

## Objetivo

Proveer una interfaz sencilla para:

- Iniciar sesión y autenticar usuarios (interfaz de `login.html`).
- Visualizar el estado y métricas de la casa (panel en `dashboard.html`).
- Revisar y reproducir registros o grabaciones (`record.html` y `video/`).
- Servir como base para integrar lógica backend (por ejemplo, una API en Flask o Node) que alimente las vistas con datos en tiempo real.

## Estructura del repositorio

- `templates/` — Plantillas HTML.
- `css/` — Hojas de estilo.
- `js/` — Scripts cliente.
- `images/` — Imágenes del proyecto.
- `video/` — Grabaciones o recursos de video.
- `monitoreo/` — Código o datos relacionados con el monitoreo.
- `static/` — Recursos estáticos adicionales.

## Cómo probar (modo estático)

Si sólo quieres abrir y revisar las páginas estáticas localmente, puedes abrir los archivos HTML con el navegador o iniciar un servidor HTTP simple:

```powershell
# Desde la raíz del proyecto (Windows PowerShell)
cd "c:\Users\crist\OneDrive\Escritorio\Nueva carpeta\casa_inteligente"
python -m http.server 8000
# Abrir en el navegador: http://localhost:8000/templates/dashboard.html
```

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



Proyecto localizado en `c:/Users/crist/OneDrive/Escritorio/Nueva carpeta/casa_inteligente`.
Para dudas o ayuda, responde en el repositorio o contacta al autor del proyecto.
