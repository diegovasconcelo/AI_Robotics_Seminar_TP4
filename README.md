# TP4 · Predicción de Spending Score

Análisis educativo de 200 clientes: estimación del Spending Score a partir de género, edad e ingreso anual.

## Archivos
- `TP4.ipynb`: análisis completo con salidas y gráficos guardados para lectura desde GitHub.
- `Mall_Customers.csv`: datos del ejercicio.
- `requirements.txt`: versiones de las bibliotecas utilizadas, más JupyterLab.

## Ejecutar localmente
Desde esta carpeta, con Python 3.11 o superior:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m jupyterlab
```

Abrir `TP4.ipynb` y ejecutar todas las celdas en orden. El CSV debe permanecer junto al notebook. En Colab, subir notebook y CSV al entorno. La ejecución fue comprobada en el entorno indicado en la última celda; los tiempos pueden variar entre equipos.

## Método y resultados
Reparto 120/40/40, escalado ajustado solo en entrenamiento, comparación de media y regresión lineal con redes de 8 y 4 neuronas. Selección neuronal por MAE de validación; prueba reservada durante la selección en este análisis. No se reajustan modelos después de la evaluación final.

| Modelo | MAE test | RMSE test | R² test |
|---|---:|---:|---:|
| Media | 18.67 | 23.57 | -0.126 |
| Regresión lineal | 17.99 | 22.13 | 0.007 |
| Red 4 neuronas | 17.59 | 21.62 | 0.053 |

La mejora es pequeña y existen errores individuales elevados. No se demuestra utilidad para decidir campañas sobre clientes específicos ni superioridad general de la red.

## Datos y referencias
Dataset: [Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python), usuario vjchoudhary7. CSV proporcionado para el ejercicio; no se atribuye autoría de los datos. Consultar las condiciones de uso en su fuente.
Material académico: consigna TP4, AP1_Complemento.ipynb y TP1-DiegoVasconcelo.pdf (perfiles). Los documentos académicos no están incluidos en este paquete.
