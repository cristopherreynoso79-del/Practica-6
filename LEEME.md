# Práctica 6 · Entornos virtuales y VS Code

**Alumno:** Cristopher Cortés · **Equipo:** A1 · **Ejecución:** 17 de noviembre de 2026

## Resultado
El cuaderno está ejecutado, contiene las imágenes y las tres respuestas finales. Se ejecutó mediante un kernel de Jupyter usando Python 3.13.0 en `.venv`. La ejecución desde la interfaz de VS Code no se ha verificado.

| Medición | Resultado |
|---|---:|
| Primera carga de MobileNetV2 | 6.00 s |
| Segunda carga | 0.33 s |
| Predicción del coche de muestra, incluida descarga | 0.74 s |
| Predicción de Grogus | 0.10 s |

El modelo no reconoció a Grogus: predijo `wooden spoon` con 7.6 %. El cuaderno explica las limitaciones de este resultado.

## Reproducir
En Git Bash, dentro de `practica-6`:

```bash
python -m venv .venv
source .venv/Scripts/activate
which python
python -m pip install -r requirements.txt
code .
```

Abrir `demo.ipynb`, seleccionar **Select Kernel → Python Environments → .venv**, ejecutar **Run All** y guardar. Las extensiones Python y Jupyter de Microsoft son necesarias en VS Code. Si no aparece el kernel, seleccionar el intérprete `.venv/Scripts/python.exe`.

## Archivos
- `demo.ipynb`: código, salidas reales, imágenes y respuestas.
- `mi-foto.jpg`: foto de Grogus.
- `requirements.txt`: versiones reales de las cuatro dependencias principales.
- `.gitignore`: excluye el entorno y temporales.

Se comprobó que las dependencias instaladas no tienen conflictos (`pip check`). El entorno virtual no se incluye en el paquete de entrega.

## Publicación y entrega
La entrega en Moodle es la liga a esta carpeta del portafolio:
https://github.com/cristopherreynoso79-del/portafolio-herramientas-ia/tree/main/practica-6

La existencia de esta liga en el documento no confirma que los archivos estén publicados. La publicación requiere una sesión de GitHub con permiso de escritura.
