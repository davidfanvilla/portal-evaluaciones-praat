# Portal de evaluaciones PRAAT

## Contenido

- `index.html`: portal completo y editable. La portada contiene tres opciones: evaluación de vuelo del alumno, supervisión del instructor en simulador y observación de buenas prácticas del instructor en teoría.
- `praat-logo.jpg`: logotipo mostrado en la portada.

El tablero agrupa las evaluaciones de teoría y simulador por el campo **Instructor evaluado**. Cuando el mismo instructor tiene ambas modalidades, aparecen juntas en su ficha con resultados, historial y gráficas de barras por sección. La evaluación de vuelo mide el desempeño del alumno y se conserva como registro separado; no se mezcla con el puntaje del instructor.

## Editar el portal

Abre `index.html` en un editor de texto. El HTML, CSS y JavaScript están en un solo archivo. Puedes cambiar títulos, campos, criterios, secciones, escalas, colores y cálculos directamente. Los criterios de las evaluaciones se transcribieron de los formatos entregados; los porcentajes ponderados de teoría siguen los pesos indicados en la guía. En los formatos de vuelo y simulador el portal presenta porcentajes descriptivos S ÷ (S+T), pues sus documentos no definen ponderación oficial. En la supervisión de simulador se mantienen las marcas originales sin reinterpretar la diferencia entre S/T y S/E que muestra el formato.

## Registros y privacidad

Las evaluaciones se guardan en el navegador y dispositivo donde se capturan. GitHub Pages publica el formulario, pero no recibe los registros ni los sincroniza entre dispositivos. Usa **Descargar respaldo JSON** para conservarlos o trasladarlos y **Importar respaldo JSON** para recuperarlos. La guía anterior permanece en su repositorio independiente; este portal también intenta importar una sola vez los registros previos que existan en ese mismo navegador.

Para publicar estáticamente, conserva `praat-logo.jpg` junto a `index.html`. El archivo se puede abrir directamente o editar y volver a publicar en GitHub Pages.

