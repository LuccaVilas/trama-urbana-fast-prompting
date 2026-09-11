# Trama Urbana — Fast Prompting en Acción

POC académica de creación de contenido para un emprendimiento ficticio de ropa.

## Abrir la entrega
Abrí **[Trama_Urbana_TP2.ipynb](Trama_Urbana_TP2.ipynb)**. Contiene introducción, problema, solución, viabilidad, objetivos, metodología, técnicas, prompts, código, salidas, costos, imagen y conclusiones.

## Estado y transparencia
La notebook incluye una **demostración local ejecutada con ejemplos didácticos fijos**. No son resultados de un experimento API. La conexión a Responses está implementada, pero no se ejecutó contra el servicio porque no había clave configurada. No se afirma superioridad entre prompts ni ahorro medido. La imagen es una generación real de la Preentrega 1, incorporada dentro de la notebook.

## Uso sin costo
En Google Colab, usar Archivo → Subir notebook y seleccionar el archivo `.ipynb`; ejecutar las celdas en orden con `MODO = "DEMO"`. No hace consultas externas. También se puede usar Jupyter local con Python 3.10 o superior. Para instalar Jupyter local: `python -m pip install -r requirements.txt` y luego `jupyter notebook`.

## Ejecutar un experimento real
1. Cambiar `MODO = "API"` y completar `MODELO` con un identificador disponible en la cuenta.
2. Ejecutar en orden. La clave se solicita con entrada oculta; no guardarla en el código.
3. Se realizan hasta tres consultas; las respuestas completadas se guardan en `.cache_trama/`. No hay reintentos automáticos.
4. Revisar las respuestas y completar las tarifas del modelo si se desea estimar el costo. No se generan imágenes por API en esta notebook.
5. Guardar la notebook con las nuevas salidas y actualizar las conclusiones según lo observado antes de subirla a GitHub. Las conclusiones actuales corresponden al modo DEMO.

## Validación realizada
Todas las celdas de código se ejecutaron secuencialmente en Python 3.14, con salidas capturadas en la notebook. Se comprobaron los tres ejemplos y el manejo de JSON inválido/tipos incorrectos. No se dispuso de un kernel Jupyter instalado ni se verificó la API real. Se incorporó una imagen PNG como adjunto Markdown para evitar dependencias de archivos externos.

## Repositorio público
[Ver el repositorio](https://github.com/LuccaVilas/trama-urbana-fast-prompting) · [Abrir la notebook en Google Colab](https://colab.research.google.com/github/LuccaVilas/trama-urbana-fast-prompting/blob/main/Trama_Urbana_TP2.ipynb)

Para la entrega se comparte el enlace del repositorio. No publicar claves ni la carpeta de caché.

## Alcance pendiente
Para que la comparación sea empírica, falta ejecutar las tres variantes con un modelo real y actualizar el análisis. Si la evaluación del curso exige generación en vivo, el modo DEMO por sí solo no satisface ese punto.
