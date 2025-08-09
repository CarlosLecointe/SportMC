# Tienda Online – Maquetación con Bootstrap 5 + Carga dinámica con Fetch

> **Autor:** Carlos Eduardo Hernández Lecointe – 1890-18-17646

Este proyecto implementa la **maquetación visual** (sin backend propio) de la página principal de una tienda online utilizando **Bootstrap 5.3**. Incluye:

- **Carousel** superior.
- **Navbar** con ícono de carrito y contador visual.
- **Layout responsivo** con **col-sm-3** (categorías) y **col-sm-9** (productos).
- **Cards de producto** y **grid** responsivo (1 por fila en móviles, 3 por fila en pantallas medianas o grandes).
- **Carga dinámica** de productos desde una **API pública** mediante **Fetch API**.
- **Footer** con el nombre y carné del autor.

---

## Estructura de carpetas

```
mi-tienda/
├─ index.html
├─ assets/
│  ├─ css/
│  │  └─ styles.css
│  └─ img/
│     └─ banner1.jpg
└─ README.md
```

> **Nota:** La carpeta `assets/img/` contiene `banner1.jpg` como imagen local para el carrusel. Puedes reemplazarla por otra de tu preferencia.

---

## Requisitos previos

- Navegador moderno (Chrome, Edge, Firefox). No necesitas servidor para ver el demo, basta con abrir `index.html`.
- Conexión a internet para cargar **Bootstrap** desde CDN y consumir la **API**.

---

## Cómo usar

1. Descarga el `.zip` y extrae en una carpeta local.
2. Abre `index.html` en el navegador.
3. Verás el **carousel**, el **menú de categorías** y los **productos** cargados dinámicamente desde la API.

---

## API utilizada

- **Endpoint:** `https://backcvbgtmdesa.azurewebsites.net/api/productos`

El script en `index.html` usa `fetch()` y maneja:
- Transformación a JSON.
- Renderizado dinámico con `forEach`.
- Presentación de **precio** y **precio de oferta** (cuando `EnOferta` es `true`), aplicando formato `toFixed(2)`.
- Imagen responsive con `img-fluid` y **fallback** a placeholder si hay error de carga.
- Botón **“Agregar al carrito”** que sólo incrementa el contador **visual**.
- Manejo de **errores** con `try/catch` y mensaje en pantalla.

---

## Responsividad (Bootstrap)

- **Móviles (sm):** `col-sm-12` → 1 producto por fila.
- **Medianas+ (md):** `col-md-4` → 3 productos por fila.

Clases clave:
- `container`, `row`, `col-sm-12`, `col-md-4`, `card`, `card-body`, `img-fluid`, `btn`, `mb-4`.

---

## Personalización

- Ajusta alturas del **carousel** y de las imágenes de **cards** en `assets/css/styles.css` (`.carousel-img`, `.card-img-top`).
- Cambia la **paleta** usando utilidades de Bootstrap o variables CSS propias.
- Sustituye imágenes por locales ubicándolas en `assets/img/` y actualizando los `src` en `index.html` si lo deseas.

---

## Pruebas en modo responsive

- Presiona **F12** → **Toggle device toolbar** para simular distintos dispositivos y verificar el grid.

---

## Créditos

- **Bootstrap 5.3** (CDN)
- **Bootstrap Icons** (CDN)
- Imágenes demo: `picsum.photos` y `placehold.co`

---

## Licencia

Proyecto educativo/ejercicio. Úsalo como base para prácticas y tareas universitarias.
