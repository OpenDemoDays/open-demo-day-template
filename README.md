# Open Demo Days Workshop Template

Plantilla estática y bilingüe para crear workshops. El sitio contiene texto de ayuda y ejemplos que puedes reemplazar. No necesitas instalar dependencias ni compilar.

## Personalizar el workshop

1. Edita `index.html`.
2. Busca `CHANGEME` y reemplaza cada marcador: título, enlaces y nombres de entorno.
3. Edita los textos de ejemplo en el arreglo `steps`. Mantén las etiquetas HTML para conservar títulos, listas, bloques de código y avisos.
4. Si cambias texto visible, actualiza las variantes en español e inglés cuando corresponda.
5. Guarda los cambios en `main`; GitHub Pages desplegará la página automáticamente.

## Agregar una sección

1. En `index.html`, localiza `const steps = [` y copia un objeto de sección.
2. Pégalo antes del `];` que cierra el arreglo.
3. Cambia `id` por un identificador único sin espacios, por ejemplo `troubleshooting`.
4. Completa `title`, `group`, `summary` y `html`.
5. Para mostrar una tarjeta en la portada, agrega también un elemento con el mismo `id` al arreglo `cards`.
6. Guarda y comprueba la sección en el menú, el índice de contenido y los botones anterior/siguiente. Estos elementos se generan automáticamente desde `steps`.

Ejemplo:

```js
{
  id: "troubleshooting",
  title: "Diagnóstico",
  group: "Módulo 2",
  summary: "Describe brevemente esta sección.",
  html: "<h2>Instrucciones</h2><p>Escribe aquí el contenido.</p>"
}
```

## Ejemplos de contenido

Texto con título y párrafo:

```html
<h2>Título del tema</h2>
<p>Escribe aquí una explicación breve.</p>
```

Lista de pasos:

```html
<ol><li>Primer paso</li><li>Segundo paso</li></ol>
```

Comandos: dentro de `html`, usa `<pre><code>...</code></pre>` y separa las líneas con `<br>`. En el código JavaScript, usa `<br>` en vez de saltos de línea literales dentro de una cadena.

```html
<pre><code>oc get pods -n CHANGEME_NAMESPACE<br>oc describe pod CHANGEME_POD</code></pre>
```

Imagen: guarda el archivo en el repositorio, por ejemplo `images/diagrama.png`, y usa la clase responsiva:

```html
<img class="content-image" src="images/diagrama.png" alt="Descripción del diagrama">
```

La clase `content-image` conserva la proporción para que la imagen no se corte. Para diagramas SVG, mantén el atributo `viewBox`.

## Publicar

GitHub Pages se publica desde `main` y `/(root)`. Confirma el estado en **Settings → Pages** y en **Actions → pages build and deployment**. La página raíz usa español; `?lang=en` muestra inglés.

## Enlaces

- [Workshop publicado](https://opendemodays.github.io/open-demo-day-template/)
- [Workshop de referencia: Unified Workload Migration with KubeVirt](https://psehgaft.github.io/UnifiedWorkloadMigration-Kubevirt/)
