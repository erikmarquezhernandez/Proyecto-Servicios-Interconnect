# **Pronóstico de cancelación de clientes y estrategias de retención**  

## **Situación**  
Interconnect, un operador de telecomunicaciones, enfrenta una alta tasa de cancelación de clientes. Para mitigar esta problemática, la empresa busca un sistema que identifique a los clientes con mayor probabilidad de cancelar, permitiendo así ofrecer códigos promocionales y planes especiales que fomenten la retención.  

## **Tarea**  
Desarrollar un modelo de Machine Learning capaz de predecir qué clientes tienen mayor probabilidad de cancelar su servicio, con el fin de implementar estrategias de retención más efectivas.  

## **Acción**  
1. **Análisis exploratorio de datos (EDA)**:  
   - Se integraron múltiples bases de datos con información de clientes, contratos y servicios.  
   - Se transformaron variables categóricas y se detectaron patrones en los datos, como la influencia del tipo de contrato y método de pago en la cancelación.  

2. **Creación y evaluación de modelos**:  
   - Se probaron varios algoritmos: Árbol de Decisión, Bosques Aleatorios, Regresión Logística, Boosting y Redes Neuronales.  
   - Se optimizaron hiperparámetros con GridSearchCV.  
   - La métrica principal fue **AUC-ROC**, obteniendo un valor de **0.85** con LightGBM, el modelo con mejor desempeño.  

3. **Optimización de la estrategia de retención**:  
   - Se identificó un subconjunto de clientes con alta probabilidad de cancelar.  
   - Se definió una estrategia de promoción dirigida para estos clientes.  

## **Resultado**  
- La empresa tiene en promedio **5174 clientes activos y 467 cancelaciones cada mes**, con una tasa de cancelación del **8.29%**.  
- El modelo identificó **694 clientes como cancelaciones**, de los cuales **467 (67.3%) realmente lo estaban**.  
- Si el equipo de marketing ofrece promociones a estos clientes y **el 20% de ellos las acepta**, **93 clientes podrían ser retenidos cada mes**.  
- Esto representaría una **reducción de la tasa de cancelación del 19.91%**, bajando del **8.29% al 6.63%**, con un impacto significativo en la retención y los ingresos de la empresa.  

