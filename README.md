# Trama Urbana — Fast Prompting en Acción

POC de generación de contenido para un emprendimiento ficticio de ropa. **Incluye tres respuestas reales obtenidas en ChatGPT web**, su evaluación con Python y una selección fundamentada de la variante con contexto.

[Abrir notebook en GitHub](Trama_Urbana_TP2.ipynb) · [Ejecutar en Google Colab](https://colab.research.google.com/github/LuccaVilas/trama-urbana-fast-prompting/blob/main/Trama_Urbana_TP2.ipynb)

## Introducción y propuesta
Los pequeños emprendimientos necesitan contenido de Instagram, pero disponen de poco tiempo para redactar y diseñar. Trama Urbana usa IA existente para preparar textos, hashtags y fondos conceptuales. El alcance final contempla tres publicaciones; esta POC compara tres prompts sobre una remera negra, lisa y de manga corta. No se entrena un modelo ni se automatiza la publicación en redes.

## Objetivos y metodología
Se comparan zero-shot, rol/contexto/restricciones y few-shot con dos ejemplos. Se mantiene el producto y formato JSON. Cada variante se envió una vez en una conversación nueva de ChatGPT web; las respuestas se conservaron sin edición. Python comprueba estructura, extensión, hashtags, marca y contacto. La revisión cualitativa examina información no confirmada.

## Resultados reales
| Variante | Caracteres del prompt | Palabras del texto | Comprobaciones |
|---|---:|---:|---:|
| A_basico | 611 | 60 | 5/5 |
| B_contexto | 869 | 56 | 5/5 |
| C_few_shot | 1296 | 56 | 5/5 |

B fue seleccionada porque no atribuye comodidad a la prenda ni inventa datos comerciales, y requiere menos instrucciones que C. A contiene el atributo no confirmado “cómoda”. El cumplimiento formal no equivale a veracidad. Una sola muestra no demuestra superioridad general.

## Cómo comprobarlo sin pagar una API
Abrir la notebook en Colab y ejecutar todas las celdas con `MODO = "REGISTRO"`. Se reanalizan las respuestas reales guardadas y se exportan los resultados. No pide claves. **Cero consultas nuevas significa reutilización de pruebas reales, no ejemplos inventados.**

Para repetir la generación, usar `MODO = "MANUAL"`: la notebook muestra un prompt, se envía en un chat nuevo de ChatGPT y se pega la respuesta original en la entrada de Python, finalizando con una línea `FIN`. Repetir para las tres variantes. La transferencia es manual y está explicitada; la notebook no controla el navegador. La evaluación detecta JSON incorrecto en vez de sustituirlo por ejemplos.

## Herramientas, viabilidad y costos
Python 3.10+, Jupyter o Colab, ChatGPT web. La preparación se estima en seis a ocho horas. El experimento realizado usó tres consultas web, cero consultas API y ninguna compra adicional de saldo API. No se conocen los tokens ni el costo imputable de suscripción. El modo REGISTRO no hace llamadas externas. La caché opcional evita solicitudes API repetidas.

El modo `API` se conserva como extensión opcional con clave y modelo propios; **no fue probado contra el servicio y no es la vía usada para esta POC**. No es necesario activarlo para repetir las pruebas manualmente. Para Jupyter local: `python -m pip install -r requirements.txt` y `jupyter notebook`.

## Archivos
- `Trama_Urbana_TP2.ipynb`: introducción, objetivos, metodología, código, prompts, respuestas, salidas, imagen y conclusiones.
- `experimento_real.json`: prompts y respuestas originales con procedencia.
- `comparacion.csv`: métricas calculadas.
- `resultados_ejecucion.json`: evaluación exportada de la ejecución registrada.
- `requirements.txt` y `.gitignore`: instalación local y exclusión de claves/caché.

## Validación y límites
Las seis celdas se ejecutaron secuencialmente en Python 3.14 y se guardaron sus salidas. Se verificaron los tres JSON, la entrada manual multilínea y el rechazo de JSON inválido. La versión previa había sido ejecutada por el autor en Colab; esta revisión fue ejecutada localmente, no en un kernel Colab.

La captura web se realizó el 10/09/2026 en Argentina con asistencia de navegador. La interfaz no expuso un identificador verificable del modelo: no se infiere a partir de la etiqueta ChatGPT Plus. La muestra es exploratoria; no demuestra causalidad ni aumento de ventas. La imagen de la Preentrega 1 está incorporada en la notebook. No se generaron nuevas imágenes en la comparación de texto.
