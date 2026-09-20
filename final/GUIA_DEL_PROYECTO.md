# Cómo explicar Trama Urbana

## En un minuto
El proyecto aborda la dificultad de un emprendimiento de ropa para preparar contenido de Instagram con poco tiempo. Diseñé una POC que combina textos y fondos visuales generados con IA. Se compararon tres tipos de prompts y se eligió el que incluye contexto y restricciones. Para la campaña final se agruparon tres publicaciones en una consulta, se generaron sus fondos y se revisaron los resultados. La notebook comprueba requisitos, muestra las piezas y exporta los materiales.

## Qué significa cada parte
- **Prompt:** la instrucción enviada al modelo.
- **Texto a texto:** una instrucción produce textos para las publicaciones.
- **Texto a imagen:** una descripción produce un fondo visual.
- **Zero-shot:** se pide una tarea sin dar ejemplos de respuesta.
- **Few-shot:** se agregan algunos ejemplos; aquí se probaron dos.
- **Contexto y restricciones:** se indica la marca, público, producto y datos que no se deben inventar.
- **JSON:** formato que permite que Python lea los campos de forma ordenada.
- **POC:** una prueba acotada para comprobar que el procedimiento puede funcionar.

## Qué hace la notebook realmente
Construye el prompt, carga o importa respuestas, comprueba extensión y formato, presenta las tres imágenes y exporta resultados. En REGISTRO utiliza respuestas reales guardadas. No se conecta automáticamente con ChatGPT ni genera imágenes al ejecutarla.

Para obtener contenido nuevo, se copia el prompt en la herramienta, se obtiene una respuesta y se la importa. Ese paso manual está documentado; no hay que describirlo como una conexión API.

## Qué se encontró
En la comparación previa, todos los textos cumplían el formato. Sin embargo, el básico decía que la remera era cómoda sin tener ese dato. Por eso la puntuación automática no bastaba para elegir. El prompt con contexto fue una mejor base para este caso, aunque una muestra pequeña no demuestra que siempre sea superior.

En la campaña final hubo que corregir dos textos: uno inventaba una etapa inicial de la marca y otro podía sugerir stock. Se conservaron los originales y se registraron las correcciones. Los tres textos finales tienen 59, 61 y 64 palabras.

## Por qué hay espacios vacíos en las imágenes
Son fondos conceptuales con una paleta común. Permiten añadir fotos auténticas de productos, algo que queda fuera del caso ficticio. No se afirma que esos fondos muestren la ropa real del emprendimiento.

## Qué se optimizó
Se pidió la campaña de tres publicaciones en una consulta final de texto. Python revisa los resultados sin consultar otra vez a un modelo. No se midieron tokens, dinero ahorrado ni aumento de ventas.

## Qué conviene revisar antes de entregar
Abrir la notebook final desde el README, recorrer los resultados y comprobar que se entienden. El profesor recibe el enlace público del repositorio. Si pregunta por el uso de IA, explicar que se utilizó asistencia para el código, la redacción y la generación, tal como está declarado.
