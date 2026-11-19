# Desarrollo de la práctica 6

Cristopher Cortés · Equipo A1 · 17 de noviembre de 2026

## 1. Entornos virtuales
Un entorno virtual aísla las bibliotecas de cada proyecto. Permite que dos proyectos utilicen versiones diferentes sin reemplazar la instalación del otro. Se crea con `python -m venv .venv`; en Git Bash para Windows se activa con `source .venv/Scripts/activate` y se sale con `deactivate`. Cada terminal necesita activar su entorno. La ruta de `sys.executable` del cuaderno es la evidencia del intérprete utilizado.

## 2. Dependencias y receta
`pip` instala bibliotecas y sus dependencias. PyTorch realiza los cálculos del modelo; Transformers carga y ejecuta MobileNetV2; Pillow trabaja con las imágenes; ipykernel conecta Python con Jupyter. `requirements.txt` registra las versiones principales realmente instaladas. Fijar solo estas cuatro no fija todas las dependencias indirectas.

En Git Bash puede generarse con:

```bash
python -m pip freeze | grep -i -E '^(torch|transformers|pillow|ipykernel)==' > requirements.txt
```

## 3. Cuaderno y resultados
Los dos cuadernos se ejecutaron mediante kernels de Jupyter con sus respectivos entornos virtuales. Se guardaron sus salidas e imágenes. Las tres preguntas del cuaderno individual están respondidas. La selección y ejecución desde la interfaz de VS Code queda por verificar; los archivos están preparados para abrirse en ella.

La primera carga de MobileNetV2 tardó 6.00 s y la segunda 0.33 s. La foto de Grogus obtuvo como primera categoría `wooden spoon` (7.6 %), una clasificación incorrecta. La tortuga pequeña, el peluche grande y el fondo pueden dificultar la tarea; no puede demostrarse la causa exacta con una sola imagen.

## 4. Git y entrega
Se deben versionar `demo.ipynb`, `mi-foto.jpg`, `requirements.txt` y las reglas de exclusión; `.venv` no se sube. Se comprobó que la regla `.venv/` excluye el intérprete del entorno. En la raíz del portafolio, conservar el `.gitignore` existente y añadir esa regla si falta. Usar `>>` para añadir sin borrar las reglas anteriores.

```bash
git status --short
git add .gitignore practica-6
git diff --cached --name-only
git commit -m "Completa practica 6: modelo local y resultados"
git push
```

La entrega en Moodle consiste en la liga a `practica-6` en GitHub. La publicación está pendiente de acceso de escritura; no debe confundirse el archivo local terminado con una entrega ya realizada.

## 5. Modelo del equipo A1
Se preparó una implementación complementaria porque el ZIP recibido no contiene el kit oficial. El clasificador se cargó en 0.986 s y procesó el coche de muestra en 0.397 s. Predijo `Volkswagen Bug 1967` con 48.36 %. Los pesos estaban descargados previamente; ese tiempo de descarga no forma parte de la carga medida. Los resultados del equipo se entregan por separado y no se publicaron en su repositorio.

## 6. Problemas comunes
Si falta `torch`, comprobar el kernel antes de reinstalar. Si no aparece `.venv`, seleccionar manualmente `.venv/Scripts/python.exe`. Si `source` falla en PowerShell, usar Git Bash. Si Git muestra archivos del entorno, revisar `.gitignore`; una regla nueva no elimina archivos ya versionados. Los avisos de Hugging Face por uso sin token y por caché sin enlaces simbólicos no impidieron esta ejecución.

## 7. Estado final
Completado localmente: entornos, dependencias, recetas, ambos cuadernos ejecutados, foto de Grogus, respuestas y resultados A1. Pendiente: verificación visual en VS Code, publicación autenticada en GitHub y entrega de la liga en Moodle. No se cerraron sesiones ni se borraron credenciales del usuario.
