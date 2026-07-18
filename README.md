# Dashboard IoT - Monitoreo Ambiental

Dashboard web para la visualización de datos de sensores IoT (temperatura, humedad y presión), simulados con un nodo **ESP32 en Wokwi**. El diseño replica la estructura de un panel de gestión de referencia: barra lateral de navegación, barra superior, tarjetas de resumen, mapa de ubicación del nodo, tabla de lecturas y un panel lateral de detalles con mini gráficos históricos.

**Asignatura:** Aplicaciones Telemáticas Basadas en Web
**Carrera:** Ingeniería en Telemática - UTEQ (Universidad Técnica Estatal de Quevedo)

## Demo en vivo

`https://<tu-usuario>.github.io/<nombre-del-repositorio>/`

*(Reemplaza esta URL por la que te entregue GitHub Pages una vez publicado el repositorio — instrucciones abajo).*

## Tecnologías utilizadas

- **HTML5** semántico
- **CSS3** puro (variables CSS, Flexbox, CSS Grid, diseño responsive)
- **JavaScript** vanilla (filtro de tabla, menú móvil, mapa a pantalla completa)
- **[Leaflet.js](https://leafletjs.com/)** — mapa interactivo con la ubicación del nodo (tiles de OpenStreetMap, sin necesidad de API key)
- **[Chart.js](https://www.chartjs.org/)** — mini gráficos históricos de temperatura, humedad y presión

Ambas librerías se cargan por CDN, por lo que el sitio funciona directamente en GitHub Pages sin ningún paso de compilación (*build*).

## Funcionalidades

- Barra lateral de navegación con enlaces internos a cada sección del panel
- Tarjetas de resumen con el estado actual de los sensores (temperatura, humedad, presión, estado del dispositivo)
- Mapa interactivo con la ubicación del nodo ESP32 y botón de pantalla completa
- Tabla de lecturas IoT con buscador/filtro en tiempo real
- Panel lateral de detalles del nodo con mini gráficos históricos (24h)
- Sección de valores históricos (máximos, mínimos y última lectura)
- Sección de alertas con historial de eventos
- Diseño responsive (adaptado a pantallas móviles)

## Estructura del repositorio

```
├── index.html            → Página principal del dashboard
├── README.md             → Este archivo
└── stylesheet/
    └── styles.css        → Hoja de estilos del dashboard
```

El archivo `index.html` enlaza la hoja de estilos con una ruta relativa a la carpeta `stylesheet`:

```html
<link rel="stylesheet" href="stylesheet/styles.css">
```

Esto significa que cualquier cambio guardado en `stylesheet/styles.css` se refleja automáticamente al recargar `index.html` — no hace falta tocar el HTML para actualizar el estilo.

## Cómo ejecutarlo localmente

No requiere instalación. Basta con abrir `index.html` en el navegador, o servirlo con cualquier servidor estático (por ejemplo, la extensión "Live Server" de VS Code).

## Publicación en GitHub Pages

1. Crear un repositorio nuevo en GitHub (público).
2. Subir `index.html` y `README.md` en la raíz del repositorio.
3. Crear una carpeta llamada `stylesheet` y subir `styles.css` dentro de ella.
4. Ir a **Settings → Pages**, y en "Source" seleccionar la rama `main` y la carpeta `/ (root)`.
5. Guardar. GitHub generará la URL pública en unos minutos (`https://<tu-usuario>.github.io/<repositorio>/`).

## Autor

Estudiante de Ingeniería en Telemática - UTEQ
