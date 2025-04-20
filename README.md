# Filtro sobre Imágenes
Aplicación de modelos de redes neuronales recurrentes (RNN) para el Diplomado de Ciencias de Datos Primavera 2025.


## Base de datos
El repocitorio de imagnes usado se puede econtran en la pagina [Radiografías de tórax (COVID-19 vs. normal vs. neumonía).](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database)


## Filtros

Los filtros que se conciderarón, son Filtro de bordes, ecualización del histograma y Wavelets (PyWavelets),  ya que son especialmente adecuada para el análisis de imágenes médicas,
debido a sus propiedades para resaltar características críticas. 

**Filtro de Bordes** (Sobel, Canny, Prewitt): Destaca los bordes y contornos de estructuras anatómicas. Útil para identificar opacidades irregulares y
líquido o consolidaciones en el tejido pulmonar. Reduce el ruido, Sobel o Canny suavizan la imagen antes de detectar bordes, eliminando artefactos.

**Ecualización del Histograma**: Mejora el contraste en imágenes donde las diferencias entre tejidos son sutiles. Las radiografías suelen tener bajo contraste. 
La ecualización estira el histograma para distinguir mejor las zonas sanas (negro/gris oscuro) vs zonas afectadas (gris claro/blanco). 
Es útil cuando hay variaciones en la exposición de las imágenes.

**Wavelets (PyWavelets)**: Analizar la imagen en múltiples escalas y orientaciones (texturas finas/ásperas). Las wavelets descomponen la imagen en aproximación (cA) que es un componente general (útil para estructuras grandes) y
detalles (cH, cV, cD) que son bordes horizontales, verticales y diagonales (ideales para patrones locales).


A travez de la plataforma de Google Colap se implementa el modelo para [Radiografía de tórax](https://colab.research.google.com/drive/1SxEEdETGpusYROC02qqLCQR73UUrSR0x?usp=sharing)





####  creado por Krystian Rodriguez Santos
