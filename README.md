# Optimización de Compras en Supermercados con Algoritmos Genéticos

## Descripción General

Este proyecto utiliza **algoritmos genéticos** para optimizar el proceso de compra en supermercados. El objetivo es minimizar el costo total de las compras, considerando tanto los precios de los productos como los gastos de transporte entre diferentes tiendas. El algoritmo emplea cromosomas que representan soluciones posibles y aplica técnicas de **selección**, **mutación** y **cruce** para mejorar la eficiencia de las compras.

---

## Características Principales

- **Optimización del costo total**: Minimiza el costo de las compras, considerando tanto los precios de los productos como los costos de transporte.
- **Algoritmo Genético**: Se utilizan técnicas de selección, cruce y mutación para encontrar la mejor solución.
- **Flexibilidad**: Puede manejar diversos tamaños de problemas (pequeños, medianos y grandes).
- **Resultados medibles**: Se evalúan las soluciones con métricas como **ENP**, **MAE** y **MSE**.

---

## Funcionalidades

1. **Generación de cromosomas**: Representación de soluciones como cromosomas (diccionarios de tiendas con productos y precios).
2. **Mutación de cromosomas**: Implementación de dos métodos de mutación: *swap* y *scramble*.
3. **Evaluación de fitness**: Cálculo del costo total, incluyendo productos y transporte.
4. **Optimización**: Generación de la siguiente generación a través de selección, cruce y mutación.
5. **Registro de resultados**: Los mejores resultados se guardan en formato **JSON** para análisis posterior.

---

## Estructura del Proyecto

- **Códigos fuente**: Archivos Python con las implementaciones de los métodos y clases que definen el algoritmo genético.
- **Datos de entrada**: Archivos `catalogo.xlsx` y `grafo.xlsx` que contienen información sobre los productos, tiendas y distancias entre ellas.
- **Métricas de rendimiento**: Evaluación de resultados mediante métricas de error como **ENP**, **MAE** y **MSE**.
- **Resultados**: Archivos `.json` y `.txt` que contienen las soluciones optimizadas y los registros de ejecución.

---

## Requisitos

- **Python 3.x**
- Librerías necesarias:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `scipy`
  - Entre otras...

---

## Uso

### 1. Configuración Inicial

Asegúrate de tener los archivos `catalogo.xlsx` y `grafo.xlsx` con los datos correctos.

Configura el entorno con las dependencias necesarias usando `pip` o `conda`.

```bash
pip install pandas numpy matplotlib scipy
```

---

### 2. Ejecutar el Algoritmo

Ejecuta el archivo principal que contiene el ciclo de optimización (run.py).

```bash
python run.py
```

Los resultados se guardarán automáticamente en archivos de registro y en formato JSON.

---

### 3. Revisión de Resultados

Los archivos de salida contienen las soluciones optimizadas, las métricas de error y los costos totales calculados.

---

### Diagrama de Flujo

```plaintext
    +--------------------+
    | Selección de Parámetros |
    +--------------------+
              |
              v
    +--------------------+
    | Cargar Datos (catalogo.xlsx, grafo.xlsx) |
    +--------------------+
              |
              v
    +--------------------+
    | Inicializar Población GA |
    +--------------------+
              |
              v
    +--------------------+
    | Evaluar Fitness de Cromosomas |
    +--------------------+
              |
              v
    +--------------------+
    | Selección, Crossover y Mutación |
    +--------------------+
              |
              v
    +--------------------+
    | Generar Nueva Generación |
    +--------------------+
              |
              v
    +--------------------+
    | Almacenar Mejor Solución |
    +--------------------+
```

---

### Resultados

El algoritmo genético ha demostrado ser una solución efectiva para reducir costos, proporcionando un balance entre precios de productos y costos de transporte. La configuración "hard_uniform_swap" ha mostrado los mejores resultados en términos de minimizar el error de predicción (ENP, MAE, MSE).

---

### Conclusiones

Este proyecto demuestra cómo los algoritmos genéticos pueden ser una herramienta poderosa para la optimización de compras, aplicando inteligencia artificial para mejorar tanto los costos de los productos como el gasto en transporte. Esto ofrece un valor real tanto a consumidores como minoristas.
