# Trama Urbana
## Del prompt a la publicación

**Proyecto Final · IA: Entretejiendo Imaginación y Algoritmos**  
**Autor:** Lucca Vilas · **Fecha:** 19 de septiembre de 2026

[**Abrir la notebook final**](Trama_Urbana_Final.ipynb) · [**Ejecutar en Google Colab**](https://colab.research.google.com/github/LuccaVilas/trama-urbana-fast-prompting/blob/main/Trama_Urbana_Final.ipynb) · [Guía para explicar el proyecto](final/GUIA_DEL_PROYECTO.md)

## Resumen
Trama Urbana es una prueba de concepto para preparar contenido de Instagram de un emprendimiento ficticio de ropa. Combina generación de texto para redactar publicaciones y generación de imágenes para crear fondos conceptuales con una identidad visual común. El objetivo es facilitar la preparación de borradores cuando hay poco tiempo y recursos limitados.

El proyecto compara tres configuraciones de prompts y aplica la variante con contexto a una campaña de tres publicaciones. Conserva las respuestas originales, registra las correcciones editoriales y utiliza una notebook para validar, mostrar y exportar los resultados. La generación se hace en herramientas externas y se incorpora manualmente; ejecutar la notebook reproduce el análisis de resultados reales sin claves API ni nuevas consultas a modelos.

## Campaña final
| Presentación de marca | Presentación de remera | Idea de combinación |
|---|---|---|
| ![Fondo de marca](final/imagenes/01_marca.png) | ![Fondo para remera](final/imagenes/02_remera.png) | ![Fondo para combinación](final/imagenes/03_combinacion.png) |
| 59 palabras | 61 palabras | 64 palabras |

Los PNG son **fondos conceptuales generados con IA**, no fotografías del catálogo. Los textos completos, hashtags y prompts aparecen junto a las imágenes en la notebook. Para convertir las piezas en anuncios de productos reales se incorporarían fotografías auténticas y la aprobación del responsable de la marca.

## Problema, solución y viabilidad
Un pequeño emprendimiento debe redactar, diseñar y revisar publicaciones con recursos limitados. La solución propuesta obtiene borradores coherentes con la marca a partir de una ficha y restricciones explícitas. Se trabaja con remeras y buzos básicos y una remera de referencia negra, lisa y de manga corta; no se inventan precios, telas o condiciones comerciales.

Se necesitan una computadora, Internet, acceso a herramientas generativas y Jupyter o Colab. No se entrena un modelo. El alcance se limita a tres borradores, sin publicación automática, atención de mensajes ni medición de ventas. La planificación estima 6–8 horas; no se afirma un ahorro de tiempo medido.

## Objetivos y metodología
1. Comparar prompts básicos, con contexto y con ejemplos.
2. Preparar tres textos con hashtags y prompts visuales en una consulta final.
3. Generar tres fondos y revisar su coherencia.
4. Conservar evidencia original y documentar dos ajustes editoriales.
5. Evaluar y exportar los resultados mediante una notebook en funcionamiento.

Se aplican zero-shot, rol y contexto, restricciones, few-shot con dos ejemplos, formato JSON, agrupación de tareas y funciones reutilizables. La agrupación no es el servicio Batch API. La evaluación se hace con Python para evitar consultas adicionales. La notebook explica y justifica cada técnica.

## Cómo ejecutar
1. Abrir el enlace de **Google Colab** de arriba.
2. Mantener `MODO = "REGISTRO"`.
3. Elegir **Entorno de ejecución → Ejecutar todas**.
4. Revisar las tablas, las tres imágenes y el mensaje de validación completada.

La notebook descarga los recursos públicos desde una versión fija del repositorio si no están presentes; esas descargas no son llamadas a IA. Al finalizar genera `salidas_final/` con JSON, CSV, PNG y una galería HTML local. La notebook contiene salidas guardadas para poder corregirla directamente desde GitHub.

Para una respuesta nueva, copiar el prompt de la notebook en ChatGPT, pegar su JSON en `RESPUESTA_MANUAL` y seleccionar `IMPORTAR`. Se evalúa sin aplicar las correcciones del registro anterior. Las imágenes que se muestran en ese modo están rotuladas como referencias anteriores; para una campaña visual nueva deben ejecutarse los nuevos prompts en una herramienta de imagen.

Para usar Jupyter local: instalar `requirements.txt`, abrir `Trama_Urbana_Final.ipynb` y ejecutar en orden. No hace falta instalar dependencias adicionales en Colab para el modo de registro.

## Resultados y conclusiones
- Tres publicaciones revisadas de **59, 61 y 64 palabras**, con hashtags y llamada a mensaje privado.
- Tres imágenes reales generadas de **1254 × 1254 píxeles**, con sus prompts exactos.
- Tres comparaciones históricas del TP 2 y una consulta final de texto para completar la campaña.
- Cinco controles formales aprobados por publicación y verificación de integridad de las imágenes.
- Dos cambios editoriales documentados: una historia no confirmada de la marca y una frase sobre disponibilidad.

La variante con contexto fue seleccionada por su adecuación al caso. Los ejemplos adicionales no mostraron una ventaja clara en la pequeña muestra del TP 2. El resultado resuelve la preparación de borradores dentro del alcance; no demuestra superioridad general, eficacia publicitaria ni eliminación de errores.

La imagen de marca agrega cielo, agua y una roca no pedidos expresamente. Se acepta como fondo conceptual y se documenta esa desviación. La revisión visual no se reemplaza por la comprobación de dimensiones.

## Recursos y costos
En el experimento final se hizo **una consulta de texto y tres generaciones de imagen**, sin comprar saldo API adicional. Los accesos utilizados no permiten atribuir un importe o contar tokens; no se presupone gratuidad universal. Reejecutar el modo REGISTRO hace cero consultas a modelos. El conteo del experimento excluye la asistencia para programar y documentar el trabajo.

## Verificación de la notebook
Se ejecutaron sus **ocho celdas de código con un kernel Jupyter real**, tanto con recursos locales como desde una carpeta vacía descargando los recursos públicos. Ambos recorridos terminaron sin errores y mostraron tres imágenes. Se probaron JSON inválido, claves duplicadas, IDs repetidos y envolturas Markdown.

[Informe local](final/resultados/verificacion_local.json) · [Informe con descarga de recursos](final/resultados/verificacion_remota.json) · [Evaluación exportada](final/resultados/evaluacion.json)

La segunda verificación reproduce el recorrido de descarga que usa Colab, pero no se presenta como una ejecución realizada dentro del servicio Colab.

## Dónde está cada requisito
| Requisito | Ubicación |
|---|---|
| Título y resumen | Inicio de la notebook y de este README |
| Problema, solución y viabilidad | Notebook, sección 1 |
| Objetivos | Sección 2 |
| Metodología y técnicas | Sección 3 |
| Código, prompts y evidencias | Sección 4; `final/datos/` y `final/prompts/` |
| Texto e imagen | Sección 5; `final/imagenes/` |
| Resultados y recursos | Secciones 6 y 7 |
| Conclusiones y límites | Sección 8 |
| Referencias | Sección 9 |

## Archivos y antecedentes
- `Trama_Urbana_Final.ipynb`: entrega principal ejecutada.
- `final/datos/`: respuestas originales, revisión editorial, comparación del TP 2 y procedencia.
- `final/prompts/`: prompt de campaña y tres prompts de imagen utilizados.
- `final/imagenes/`: PNG originales generados.
- `final/resultados/`: exportaciones e informes de ejecución.
- `Trama_Urbana_TP2.ipynb`: antecedente conservado; la entrada principal es la notebook final.

No se recibió una devolución del TP 2. No se incluyeron los extras de audio o interfaz interactiva, que son optativos. La galería es un archivo de revisión, no un sitio publicado.

## Referencias y asistencia
- [OpenAI: Ingeniería de prompts](https://developers.openai.com/es-419/api/docs/guides/prompt-engineering).
- [Jupyter: ejecución con nbclient](https://nbclient.readthedocs.io/en/latest/client.html).
- Consigna del Proyecto Final proporcionada por el curso.

Se utilizó asistencia de IA para redacción, código, generación y revisión. Los textos se generaron en ChatGPT web y las imágenes con el generador integrado `image_gen`. No se expusieron identificadores exactos de modelo; no se inventan. Trama Urbana es ficticia y no se utilizaron datos de clientes.
