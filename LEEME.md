# Portal de evaluaciones PRAAT

## Archivos

- `index.html`: página completa y editable. Contiene el diseño, los campos, los criterios, los cálculos y el gráfico.
- `praat-logo.jpg`: logotipo usado en el encabezado.

## Editar el formato

Abre `index.html` en un editor de texto. En el código busca `EDITA AQUÍ LOS FORMATOS`. El objeto `catalog` contiene los títulos, campos, criterios y secciones de cada evaluación. Puedes cambiar el texto directamente y guardar el archivo.

Los resultados actuales son descriptivos: calculan marcas `S` sobre las marcas `S` y `T` registradas. Los formatos de origen no proporcionan una ponderación oficial. En la supervisión de instructor, el encabezado de la tabla muestra `S / T`, mientras que la leyenda define `S / E`; el portal conserva las etiquetas originales y no les asigna una definición nueva.

## Datos de evaluación

Los registros se guardan localmente en el navegador del dispositivo. No se envían al sitio ni se sincronizan entre dispositivos. Usa **Descargar respaldo JSON** dentro de una evaluación para conservar o trasladar los registros.

El portal está construido con HTML, CSS y JavaScript sin instalación de paquetes. Se puede abrir `index.html` directamente o publicar la carpeta en un hosting estático. Para que el logotipo aparezca, conserva `praat-logo.jpg` junto a `index.html`.

