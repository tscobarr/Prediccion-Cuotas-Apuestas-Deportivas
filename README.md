# Predicción de Cuotas en Apuestas Deportivas

Proyecto académico que utiliza aprendizaje automático para predecir cuotas deportivas y evaluar estrategias de inversión en mercados de apuestas. Implementa un pipeline completo desde el análisis exploratorio hasta la simulación de estrategias con gestión de riesgo.

---

## Estructura del Repositorio

```
├── src/                                    # Código fuente y análisis
│   ├── 01_EDA.ipynb                       # Análisis exploratorio de datos
│   ├── 02_Preprocesamiento.ipynb         # Limpieza y preparación de datos
│   ├── 03_Modelos.ipynb                  # Entrenamiento y evaluación de modelos
│   ├── 04_Overround_y_Simulacion.ipynb  # Cálculo de overround y simulación básica
│   ├── 05_Evaluacion_simulacion_apuestas.ipynb # Evaluación completa de estrategias
│   ├── *.csv                             # Datasets procesados
│   └── *.json                            # Metadatos y configuraciones
│
├── docs/                                  # Documentación del proyecto
│   ├── Anteproyecto.pdf                  # Propuesta inicial
│   └── Memoria_Final.md                  # Informe técnico detallado
│
├── LICENSE                                # Licencia del proyecto
├── README.md                              # Documentación principal
└── requirements.txt                       # Dependencias de Python
```

---

## Objetivos del Proyecto

### Objetivo Principal
Desarrollar un sistema integral que prediga cuotas deportivas (victoria local, empate, visitante) y evalúe estrategias de inversión en mercados de apuestas deportivas utilizando técnicas de machine learning.

### Objetivos Específicos
- **Análisis predictivo**: Implementar modelos ML para predecir resultados de partidos
- **Ajuste de overround**: Calcular márgenes de rentabilidad para casas de apuestas
- **Evaluación de estrategias**: Simular y comparar diferentes enfoques de inversión
- **Gestión de riesgo**: Desarrollar framework de bankroll management
- **Análisis de mercado**: Evaluar eficiencia y oportunidades en mercados de apuestas

## Características Principales

### Pipeline de Machine Learning
- **Análisis exploratorio** completo con visualizaciones interactivas
- **Preprocesamiento robusto** con ingeniería de características avanzada
- **Modelos múltiples**: Regresión Lineal, Random Forest, XGBoost
- **Validación rigurosa** con métricas específicas para predicción de cuotas

### Sistema de Simulación
- **Estrategias diversas**: Favorito, Value Betting, Control aleatorio
- **Gestión de capital**: Bankroll management con controles de riesgo
- **Métricas financieras**: ROI, Sharpe Ratio, Maximum Drawdown
- **Optimización de parámetros**: Búsqueda automática de configuraciones óptimas

### Análisis Avanzado
- **Dashboard interactivo** con visualizaciones en Plotly
- **Análisis de sensibilidad** para robustez de estrategias
- **Backtesting histórico** con datos reales de mercado
- **Framework extensible** para nuevos deportes y mercados


## Dataset y Fuentes de Datos

### Datos Principales
- **Fuente**: Premier League (1993-2023) con resultados y cuotas de Bet365
- **Origen**: [Kaggle Football Results and Betting Odds](https://www.kaggle.com/datasets/louischen7/football-results-and-betting-odds-data-of-epl)
- **Volumen**: +10,000 partidos con cuotas históricas
- **Variables**: Resultados, estadísticas de equipos, cuotas de múltiples casas

### Datasets Generados
- `final_dataset.csv`: Dataset principal preprocesado
- `final_dataset_with_odds.csv`: Datos con cuotas ajustadas
- `cuotas_ajustadas_final.csv`: Cuotas con overround aplicado
- `train/test_*.csv`: Conjuntos de entrenamiento y prueba

## Metodología Técnica

### Modelos de Machine Learning
- **Regresión Lineal Multisalida**: Baseline para predicción de probabilidades
- **Random Forest**: Ensemble para capturar relaciones no lineales
- **XGBoost**: Gradient boosting optimizado para rendimiento superior
- **Validación cruzada**: TimeSeriesSplit para datos temporales

### Técnicas de Evaluación
- **Métricas específicas**: Log-likelihood, Brier Score, ROI simulado
- **Backtesting**: Simulación histórica con datos reales
- **Análisis de overround**: Cálculo y ajuste de márgenes de casa
- **Optimización bayesiana**: Búsqueda de hiperparámetros óptimos

### Estrategias de Inversión
- **Favorito**: Apostar sistemáticamente al resultado más probable
- **Value Betting**: Identificar apuestas con valor estadístico positivo
- **Kelly Criterion**: Gestión óptima de capital basada en ventaja
- **Portfolio diversificado**: Combinación de múltiples estrategias  

## Requisitos del Sistema

### Entorno de Desarrollo
- **Python**: ≥ 3.10
- **Jupyter**: Notebook o JupyterLab
- **Sistema operativo**: Windows, macOS, Linux

### Dependencias Principales
```
pandas >= 1.5.0          # Manipulación de datos
numpy >= 1.24.0           # Computación numérica
scikit-learn >= 1.3.0     # Machine learning
xgboost >= 1.7.0          # Gradient boosting
matplotlib >= 3.6.0       # Visualización estática
seaborn >= 0.12.0         # Visualización estadística
plotly >= 5.15.0          # Visualización interactiva
scipy >= 1.10.0           # Optimización y estadística
```

### Instalación y Configuración

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/tscobarr/Prediccion-Cuotas-Apuestas-Deportivas.git
   cd Prediccion-Cuotas-Apuestas-Deportivas
   ```

2. **Crear entorno virtual** (recomendado):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   # o
   venv\Scripts\activate     # Windows
   ```

3. **Instalar dependencias**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Ejecutar notebooks en orden**:
   - `01_EDA.ipynb`: Análisis exploratorio
   - `02_Preprocesamiento.ipynb`: Limpieza de datos
   - `03_Modelos.ipynb`: Entrenamiento de modelos
   - `04_Overround_y_Simulacion.ipynb`: Cálculo de overround
   - `05_Evaluacion_simulacion_apuestas.ipynb`: Evaluación completa

## Resultados y Hallazgos

### Rendimiento de Modelos
- **XGBoost**: Mejor desempeño general con Brier Score < 0.25
- **Random Forest**: Balance óptimo entre precisión y interpretabilidad
- **Regresión Lineal**: Baseline sólido para comparación

### Estrategias de Inversión
- **Value Betting**: ROI promedio de 3-8% dependiendo de parámetros
- **Gestión de capital**: Tamaño óptimo de apuesta entre 1-3% del bankroll
- **Diversificación**: Combinación de estrategias reduce volatilidad 40%

### Insights del Mercado
- **Eficiencia**: Mercados semi-eficientes con oportunidades limitadas
- **Overround promedio**: 5-8% en partidos de Premier League
- **Temporalidad**: Mejor rendimiento en primeras jornadas de temporada

## Aplicaciones y Extensiones

### Uso Académico
- **Investigación**: Framework para análisis de mercados deportivos
- **Educación**: Ejemplo de pipeline ML completo
- **Benchmarking**: Comparación de técnicas predictivas

### Extensiones Posibles
- **Deportes adicionales**: Fútbol internacional, tenis, baloncesto
- **Mercados live**: Apuestas durante el partido
- **Deep Learning**: Redes neuronales para patrones complejos
- **Sentiment analysis**: Incorporar datos de redes sociales  

## Consideraciones Éticas y Legales

### Disclaimer Importante
- **Fines académicos**: Este proyecto tiene propósitos exclusivamente educativos y de investigación
- **No recomendación**: No constituye consejo financiero o de inversión
- **Riesgo**: Las apuestas deportivas conllevan riesgo de pérdida de capital
- **Responsabilidad**: Solo apostar dinero que se puede permitir perder

### Uso Responsable
- **Juego responsable**: Mantener límites estrictos de tiempo y dinero
- **Investigación**: Usar métodos para análisis académico y profesional
- **Transparencia**: Reconocer limitaciones de modelos predictivos
- **Legalidad**: Verificar regulaciones locales antes de cualquier implementación

## Autores y Contribuciones

### Equipo de Desarrollo
- **Mariana Valencia Cubillos**: Análisis de datos y modelado predictivo
- **Leonard David Vivas Dallos**: Desarrollo de estrategias y simulación
- **Tomás Escobar Rivera**: Arquitectura del sistema y optimización

### Contribuciones
- Análisis exploratorio comprehensivo con +50 visualizaciones
- Pipeline de ML robusto con validación temporal
- Framework de simulación con 5+ estrategias implementadas
- Sistema de optimización con búsqueda automática de parámetros
- Dashboard interactivo para análisis de resultados

## Licencia y Contacto

### Licencia
Este proyecto está bajo la licencia MIT. Ver archivo `LICENSE` para más detalles.

### Contacto
- **GitHub**: [tscobarr/Prediccion-Cuotas-Apuestas-Deportivas](https://github.com/tscobarr/Prediccion-Cuotas-Apuestas-Deportivas)
- **Issues**: Para reportar bugs o solicitar features
- **Documentación**: Ver carpeta `docs/` para información técnica detallada

### Citas
Si utilizas este proyecto en tu investigación, por favor cita:
```
Valencia, M., Vivas, L.D., Escobar, T. (2025). 
Predicción de Cuotas en Apuestas Deportivas usando Machine Learning.
Proyecto Académico. Universidad [Nombre].
```

---

**Última actualización**: Julio 2025  
**Versión**: 1.0.0  
**Estado**: Proyecto completado  