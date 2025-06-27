# Prediccion-Cuotas-Apuestas-Deportivas
Proyecto académico que utiliza aprendizaje automático para predecir cuotas deportivas (victoria local, empate o visitante) con el fin de maximizar la rentabilidad de casas de apuestas. Implementado en Python.

---

### **Estructura del Repositorio**  
```
├── src                             # Código fuente modular (demanda, clasificación, recomendación)
│   ├── 01_EDA.ipynb                # Análisis exploratorio
│   ├── 02_Preprocesamiento.ipynb
│   └── 03_Modelos.ipynb            # Entrenamiento y evaluación
│
├── docs/                           # Documentación
│   ├── Anteproyecto.pdf            # Archivo original
│   └── Memoria_Final.md            # Informe detallado
│
├── LICENSE                         # Licencia del proyecto
├── README.md                       # Descripción del proyecto
├── requirements.txt                # Dependencias (Python)
```

---

## Objetivo  
Desarrollar un sistema que prediga cuotas deportivas (victoria local, empate, visitante) utilizando modelos de ML, ajustando un margen de rentabilidad para casas de apuestas.


## Dataset  
Datos históricos de la Premier League (1993-2023) con resultados y cuotas de Bet365. Fuente: [Kaggle](https://www.kaggle.com/datasets/louischen7/football-results-and-betting-odds-data-of-epl).


## Métodos  
- Regresión lineal multisalida  
- Random Forest, XGBoost  
- Ajuste de overround  

## Requisitos  
- Python ≥ 3.10
- TensorFlow ≥ 2.12
- Bibliotecas: `pandas`, `scikit-learn`, `matplotlib`, `seaborn`, `XGBoost`  

## Uso  
1. Clonar repositorio:  
   ```bash
   git clone https://github.com/tu-usuario/Prediccion-Cuotas-Apuestas-Deportivas.git
   ```  
2. Instalar dependencias:  
   ```bash
   pip install -r requirements.txt
   ```  
3. Ejecutar notebooks en orden (`01_EDA.ipynb`, `02_Preprocesamiento.ipynb`, `03_Modelos.ipynb`.).  

## Autores  
- Mariana Valencia Cubillos  
- Leonard David Vivas Dallos  
- Tomás Escobar Rivera  