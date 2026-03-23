# 🛡️ Risk-Sentinel: MLOps & Model Audit Framework

Este repositorio contiene la unidad de vigilancia avanzada diseñada para auditar y monitorear el desempeño del **Motor de Riesgo v2.0**. Su objetivo es detectar degradaciones en la población (**Data Drift**) y fallas en la estabilidad del modelo antes de que impacten la rentabilidad de la cartera crediticia.

---

## 🚨 Caso de Estudio: Detección de Crisis (Marzo 2026)
Durante la auditoría del primer trimestre de 2026, el sistema activó una **Alerta Roja** al detectar una inestabilidad poblacional crítica que invalidó el comportamiento histórico del modelo de entrenamiento.

### 1. Inestabilidad Poblacional (PSI)
El indicador **Population Stability Index (PSI)** registró un valor de **1.8628** en la variable de ingresos para la cosecha de marzo.
* **Umbral de Alerta:** > 0.25 (Inestabilidad Crítica).
* **Diagnóstico:** Existe un cambio estructural en el perfil socioeconómico de los solicitantes, lo que genera un "Data Drift" masivo que el modelo original no está diseñado para procesar bajo los parámetros actuales.

### 2. Análisis de Vintages (Cosechas)
La auditoría de maduración de mora revela una degradación acelerada en la calidad de la originación reciente:
* **Cosechas Estables (Mes 1 y 2):** Mantienen una curva de mora controlada con una maduración cercana al **6%**.
* **Cosecha Crítica (Mes 3 - Línea Roja):** Presenta una pendiente de mora agresiva, alcanzando el **14.5%** en solo 6 meses, confirmando la toxicidad de la cosecha detectada previamente por el PSI.

<img width="865" height="479" alt="image" src="https://github.com/user-attachments/assets/a3c2dc5d-159b-4eac-9210-b1b51e4f28b2" />

---

## 🛠️ Capacidades de Monitoreo (MLOps)
El motor `RiskSentinel` implementa herramientas esenciales para un Data Scientist Mid-Level:
* **Auditoría de Estabilidad:** Cálculo de PSI para detectar desviaciones en variables críticas.
* **Vintage Analysis:** Seguimiento del comportamiento de pago por mes de otorgamiento para identificar "cosechas tóxicas".
* **Gobernanza de Modelos:** Comparación estadística continua entre el dataset de Referencia (Entrenamiento) y Producción.

## 📉 Acciones de Mitigación Recomendadas
Basado en los hallazgos de este Sentinel, se proponen las siguientes acciones de gobernanza:
1. **Recalibración de Emergencia:** Ajustar el punto de corte (Cut-off) de **0.27 a 0.15** para reducir la exposición al riesgo.
2. **Cierre de Grifos:** Restricción temporal de crédito para segmentos con PSI > 0.50 hasta estabilización macroeconómica.

---

## 🔗 Ecosistema de Riesgo MX
Este proyecto es la unidad de vigilancia del ecosistema:
1. **[Macro-Risk-Supervision-Engine-MX](https://github.com/TU_USUARIO/Macro-Risk-Supervision-Engine-MX):** El núcleo de decisión y entrenamiento v2.0.
2. **Risk-Sentinel-MLOps-MX (Este Repositorio):** El guardián encargado de la salud y estabilidad del modelo en producción.
