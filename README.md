# Open Demo Days Workshop Template

Plantilla estática y bilingüe para crear workshops prácticos, inspirada en el workshop [Unified Workload Migration with KubeVirt](https://psehgaft.github.io/UnifiedWorkloadMigration-Kubevirt/).

## Qué incluye

- Navegación lateral con búsqueda y módulos del workshop.
- Tabla de contenidos contextual, navegación anterior/siguiente y selector de idioma.
- Diseño adaptable para escritorio y pantallas pequeñas.
- Imágenes y diagramas escalados dentro del contenido para conservar la proporción y evitar recortes.
- Versión en español por defecto e inglés con `?lang=en`.

## Personalizar

Edita `index.html` para cambiar el nombre del workshop, las secciones, los enlaces de presentación/materiales y el contenido de ejemplo. Busca `CHANGEME` para localizar los valores de configuración que debes reemplazar. Sustituye los diagramas de ejemplo por tus imágenes y conserva las clases de imagen existentes para que se adapten al ancho disponible sin cortarse.

## Publicar con GitHub Pages

1. Abre **Settings → Pages**.
2. En **Build and deployment**, elige **Deploy from a branch**.
3. Selecciona la rama `main` y la carpeta `/(root)`, y guarda.
4. Espera a que termine el despliegue. La página en español se sirve desde la raíz; añade `?lang=en` para inglés.

El sitio no requiere compilación ni dependencias: GitHub Pages publica directamente `index.html`.
