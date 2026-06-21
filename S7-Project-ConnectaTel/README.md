# Análisis de Datos ConnectaTel

El objetivo de este proyecto es identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas dentro de la compañía, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.

---

## 📊 Datasets Utilizados

El análisis se alimenta de tres fuentes de datos principales:

* **`plans.csv`**: Detalle de los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
* **`users_latam.csv`**: Información demográfica y contractual de los clientes (edad, ciudad, fecha de registro, plan contratado).
* **`usage.csv`**: Detalle de uso real del servicio, especificando llamadas (duración) y mensajes (longitud).

---

## 🔄 Flujo General del Proyecto

| Paso | Acción | Resultado para el Negocio |
| :--- | :--- | :--- |
| **1. Cargar y explorar** | Cargar y explorar `plans`, `users_latam`, `usage`. | Visión clara de la estructura y tipos de columna de cada dataset. |
| **2. Identificación de problemas de calidad** | Contar nulos, detectar sentinels y revisar fechas fuera de rango. | Lista priorizada de problemas de calidad que pueden sesgar decisiones. |
| **3. Limpieza básica** | Reemplazar sentinels, convertir fechas, imputar o marcar NA según reglas de negocio. | Datos consistentes y listos para análisis estadístico confiable. |
| **4. Summary statistics** | Revisar las medidas clave en variables categóricas y numéricas. | Medidas clave (media, mediana, percentiles) que muestran el comportamiento típico y extremo. |
| **5. Visualización & outliers** | Creación de histogramas y boxplots enfocados. | Visualización de sesgos, patrones de usuarios o datos atípicos. |
| **6. Segmentación** | Crear segmentaciones basadas en reglas claras; visualizar proporciones con countplots. | Segmentos accionables que permiten diseñar ofertas, campañas y migraciones de plan. |
| **7. Insight ejecutivo** | Redactar conclusiones y recomendaciones comerciales basadas en los pasos anteriores. | Responder a las preguntas del negocio y proponer acciones concretas. |
| **8. Publicación** | Subir el notebook + README a GitHub. | Entrega reproducible para revisión y ejecución por *stakeholders*. |

---

## 🚀 Cómo Ejecutar el Notebook

Puedes ejecutar este análisis de manera local o directamente en la nube. Elige la opción que prefieras:

### Opción A: Ejecutar en Google Colab (Recomendada)
1. Ve a [Google Colab](https://colab.research.google.com/).
2. Haz clic en la pestaña **File** (Archivo) > **Upload notebook** (Subir cuaderno).
3. Selecciona el archivo `notebook.ipynb` de este repositorio.
4. Sube los archivos `.csv` de la sección de datasets a la sección de archivos de Colab (icono de carpeta en la barra lateral izquierda).
5. Ejecuta las celdas en orden de arriba hacia abajo (`Ctrl + F9` ejecuta todo).

### Opción B: Ejecutar Localmente (Jupyter Notebook / VS Code)
1. Asegúrate de tener instalado Python (versión 3.9 o superior) junto con las librerías necesarias:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

Inicia el servidor de Jupyter en tu terminal:

```bash
jupyter notebook
```
Abre el archivo notebook.ipynb desde la interfaz del navegador y ejecuta las celdas secuencialmente.

