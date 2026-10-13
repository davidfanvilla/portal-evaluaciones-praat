# Portal de evaluaciones PRAAT

## Contenido

- `index.html`: portal completo y editable. La portada muestra tres formatos: evaluación de vuelo del alumno, supervisión del instructor en simulador y observación de buenas prácticas del instructor de teoría.
- `praat-logo.jpg`: logotipo de PRAAT.`n- `ejemplo-dashboard.html`: vista completa de demostración del dashboard con datos ficticios, sin persistencia.

El dashboard reúne teoría y simulador bajo el campo **Instructor evaluado** y muestra resultados y gráficas por sección. Solo presenta evaluaciones completas: todos los datos del formato y todas las calificaciones. En teoría, `N/O` cuenta como respuesta y se excluye del cálculo ponderado. Los borradores se pueden reanudar desde **Continuar borradores**. La evaluación del alumno se muestra aparte del resultado docente.

## Firmas y exportaciones

Las firmas se dibujan con dedo, lápiz táctil o mouse y se guardan dentro de la evaluación en ese dispositivo. **Respaldo completo JSON** conserva todos los datos y permite restaurarlos con **Importar respaldo JSON**. **Exportar CSV para Excel / Numbers** produce una tabla legible de indicadores, puntajes y observaciones. También se puede imprimir o guardar un formato individual como PDF desde el navegador.

## Editar el portal

Abre `index.html` en un editor de texto. El HTML, CSS y JavaScript están en un solo archivo. El bloque `EDITA AQUÍ LOS FORMATOS` contiene los títulos, campos e indicadores de vuelo y simulador. La variable `dimensions` contiene las diez dimensiones y criterios de teoría. Puedes modificar esos textos y estilos directamente.

Los porcentajes de teoría respetan la ponderación oficial de la guía. Vuelo y simulador usan la proporción descriptiva S ÷ (S+T), porque los formatos no proporcionan ponderaciones oficiales. En simulador se conservan las marcas que aparecen en la tabla, sin resolver la diferencia entre S/T y S/E que presenta el documento.

## Dónde se guardan los datos

GitHub Pages aloja los archivos públicos del portal, no las evaluaciones capturadas. Los registros permanecen en el almacenamiento local del navegador y perfil de cada dispositivo. No se sincronizan entre Windows, macOS, iPad, iPhone o Android. Exporta JSON con regularidad y transfiere el archivo para mover o conservar registros. Conserva `praat-logo.jpg` junto a `index.html` al editar o publicar.

