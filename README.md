# Catálogo de productos frikis de [www.mundofriki.es](https://www.mundofriki.es)

Catálogo abierto con los productos que aparecen en [www.mundofriki.es](https://www.mundofriki.es): libros, cómics, figuras, juegos y otros artículos del mundo friki disponibles en España.

El fichero se genera automáticamente desde la web y se actualiza cada día a las 18:00 (hora de España). En este repositorio solo se guarda la última versión.

## Fichero

| Fichero | Contenido |
|---|---|
| `Todos-los-productos-de-mundofriki-es.zip` | ZIP con un único CSV de todos los productos activos |

El CSV dentro del ZIP tiene estas características:

- Codificación **UTF-8 con BOM**, para que Excel muestre bien los acentos y la ñ al abrirlo con doble clic.
- Separador de campos: coma (`,`).
- Los textos que contienen comas van entre comillas dobles (`"`).
- La primera fila es la cabecera con el nombre de las columnas.

## Columnas

| Columna | Descripción | Ejemplo |
|---|---|---|
| `asin` | Código ASIN del producto en Amazon | `8417954732` |
| `ean` | Código de barras EAN-13 (puede estar vacío) | `9788417954734` |
| `isbn` | ISBN-10, solo en libros (puede estar vacío) | `8417954732` |
| `titulo` | Título del producto | `Historia De La Semana Santa De Sevilla para Niños` |
| `formato` | Formato o presentación | `Tapa blanda` |
| `categoria` | Categoría del producto en mundofriki.es | `Semana Santa` |
| `video_youtube` | Vídeo del producto en YouTube (puede estar vacío) | `https://www.youtube.com/watch?v=rZ9p5aXewaE` |
| `url` | Ficha del producto en mundofriki.es | `https://www.mundofriki.es/producto/8417954732/...` |

El catálogo no incluye precios, imágenes, valoraciones ni descripciones. Los precios y la disponibilidad cambian a diario; para consultarlos, visita la ficha del producto en la web.

## Cómo usarlo

### Con Excel

1. Descarga el ZIP y descomprímelo.
2. Abre el fichero CSV con doble clic.

### Con Python (pandas)

```python
import pandas as pd

productos = pd.read_csv("Todos-los-productos-de-mundofriki-es.zip", encoding="utf-8-sig")
print(productos.head())
```

`encoding="utf-8-sig"` hace que pandas ignore el BOM del principio del fichero.

## Licencia

Los datos se publican con licencia [Creative Commons Atribución 4.0 Internacional (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.es).

Puedes usarlos, copiarlos, modificarlos y redistribuirlos, también con fines comerciales, siempre que cites la fuente:

> Catálogo de productos de mundofriki.es — https://www.mundofriki.es

## Autor

© Roger Casadejús Pérez
