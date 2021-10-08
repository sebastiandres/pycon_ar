# HELP

## Crear el ambiente
conda create -n template

# Instalar librerías
Desde requirements:
source activate template
conda install --file requirements.txt

Uno a uno:
pip install rise
pip install pandas
(rise instala jupyter notebook & all, pandas instala numpy y matplotlib)

## Generar un pdf con las slides
Ejecutar
jupyter nbconvert --to slides template.ipynb --post serve

Abrir
http://127.0.0.1:8000/template.slides.html

Agregar "?print-pdf" al enlace
http://127.0.0.1:8000/template.slides.html?print-pdf

Puedes hacer los 2 al mismo tiempo, y ahora guardas como pdf (Ctrl/Cmmd+P):
jupyter nbconvert --to slides template.ipynb --post serve; open http://127.0.0.1:8000/template.slides.html?print-pdf

## Borrar el ambiente
conda deactivate
conda env remove -n template

## Mostrar todos los ambientes
conda env list

## Actualizar index.html
Reemplazar REPOSITORY por el nombre del repositorio.
Recordar activar github pages en la rama principal y directorio principal.
