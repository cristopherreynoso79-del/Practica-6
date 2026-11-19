# Resultados · Modelo A1

Modelo: `Jordo23/vehicle-classifier`. Ejecución local en CPU, 4 hilos, Python 3.13.0, Windows 11.

| Medición | Tiempo |
|---|---:|
| Consulta de archivo ya descargado | 0.0011 s |
| Carga de pesos y creación del modelo | 0.986 s |
| Preprocesamiento e inferencia | 0.397 s |

La descarga de los pesos se había realizado previamente; su duración no está incluida en estas mediciones.

| Predicción | Puntuación |
|---|---:|
| Volkswagen Bug 1967 | 48.36 % |
| Volkswagen Beetle Hatchback 2012 | 7.99 % |
| Volkswagen Beetle 1967 | 7.60 % |
| Volkswagen Beetle 1969 | 6.52 % |
| Volkswagen Bug 1968 | 5.58 % |

Se usó el coche de muestra público de Hugging Face. No se verificó el año real del vehículo y una sola imagen no permite medir exactitud. La salida es una estimación del modelo, no una identificación garantizada.

Este contenido está preparado para incorporarlo a la sección Resultados del README del equipo. No se hizo commit ni push en su repositorio.
