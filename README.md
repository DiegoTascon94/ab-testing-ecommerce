# 🧪 Análisis Experimental A/B Test para E-commerce

## 📌 Contexto del Negocio
En el entorno competitivo del comercio electrónico, cada cambio en la interfaz o en el sistema de recomendaciones representa una apuesta de negocio. Implementar modificaciones sin validación estadística puede resultar en pérdidas significativas de conversión o ticket promedio. Este proyecto responde a la necesidad de tomar decisiones basadas en evidencia cuantitativa antes de un despliegue masivo.

## 🎯 Objetivo del Proyecto
Evaluar mediante un experimento A/B controlado si los cambios implementados en la interfaz y el sistema de recomendaciones de un e-commerce producen mejoras estadísticamente significativas en las métricas clave de negocio:
- Validar el impacto sobre la **tasa de conversión**.
- Medir el efecto sobre el **ticket promedio** por transacción.
- Garantizar la **integridad del experimento** antes de interpretar resultados.
- Emitir una **recomendación estratégica** sustentada en evidencia cuantitativa.

## 🔍 Alcance del Análisis
- **Nivel de análisis:** Usuario individual por grupo experimental (Control vs. Tratamiento).
- **Datos incluidos:** Registro de eventos de sesión, conversiones y valor transaccional por grupo.
- **Supuestos:** Se asume asignación aleatoria correcta de usuarios a cada grupo y ausencia de contaminación entre variantes.

## 📊 Principales Insights del Análisis (EDA)
- **Verificación de Integridad:** Se auditó la distribución de usuarios entre grupos para confirmar la ausencia de sesgos en la asignación experimental.
- **Detección de Anomalías:** Se identificaron y trataron registros duplicados y sesiones con comportamiento atípico que podrían inflar artificialmente las métricas.
- **Distribución de Conversiones:** Análisis de la tasa de conversión por cohorte temporal para identificar posibles efectos de novedad o fatiga en el grupo de tratamiento.
- **Análisis de Varianza:** Evaluación de la dispersión del ticket promedio entre grupos para seleccionar la prueba estadística más adecuada.

## 🤖 Enfoque Analítico y Modelo
Se implementó un pipeline estadístico completo de validación experimental:

- **Verificación de integridad del experimento:** Control de tamaño de muestra y distribución entre grupos.
- **Limpieza y control de sesgos:** Eliminación de registros contaminados o mal asignados.
- **Pruebas estadísticas aplicadas:**
  - **Test Z** — Comparación de proporciones de conversión entre grupos.
  - **T-Test** — Comparación de medias del ticket promedio.
  - **Comparación de proporciones** — Evaluación de diferencias en métricas binarias clave.
- **Control de errores:** Evaluación del tamaño del efecto y control de falsos positivos (error Tipo I).
- **Interpretación estratégica:** Traducción de los resultados estadísticos a recomendaciones de negocio accionables.

## 📈 Métricas y Resultados
- **Tasa de Conversión:** Comparación estadística entre grupo control y tratamiento con nivel de significancia definido.
- **Ticket Promedio:** Evaluación del impacto económico por transacción entre variantes.
- **Tamaño del Efecto:** Cuantificación de la magnitud práctica del cambio, más allá de la significancia estadística.
- **Conclusión:** Los resultados estadísticos validaron que los cambios en el embudo **no afectaron negativamente la conversión**, mitigando riesgos financieros antes del despliegue total.

## 💼 Impacto en Decisiones de Negocio
- **Mitigación de Riesgo:** La validación previa al despliegue evita impactos negativos en métricas de ingresos a escala completa.
- **Cultura Data-Driven:** Establece un framework replicable para evaluar futuras iteraciones de producto con rigor estadístico.
- **Optimización de Producto:** Los hallazgos proveen una base sólida para priorizar el roadmap de mejoras de la interfaz con respaldo cuantitativo.

## 🛠️ Tecnologías y Herramientas Utilizadas
- **Lenguaje:** Python 3.x
- **Librerías:** Pandas, NumPy, SciPy (Stats), Matplotlib, Seaborn
- **Métodos estadísticos:** Z-Test, T-Test, Comparación de proporciones, Análisis de tamaño de efecto
- **Entorno de trabajo:** Jupyter Notebook, GitHub

## 📂 Estructura del Repositorio
```
├── data/
│   └── ab_test_data.csv          # Dataset del experimento A/B
├── notebook/
│   └── ab_testing_ecommerce.ipynb  # Notebook principal del análisis
├── README.md                       # Documentación del proyecto
└── requirements.txt                # Dependencias del entorno
```

## ▶️ Cómo Ejecutar el Proyecto
1. Clonar el repositorio:
   ```
   git clone https://github.com/DiegoTascon94/ab-testing-ecommerce.git
   ```
2. Instalar dependencias:
   ```
   pip install -r requirements.txt
   ```
3. Abrir el análisis: Navegar a `/notebook` y ejecutar `ab_testing_ecommerce.ipynb`.

## 📝 Conclusiones
Este proyecto demuestra que la toma de decisiones sobre cambios de producto no puede depender de la intuición. La aplicación de un framework experimental riguroso — que incluye verificación de integridad, control de sesgos y pruebas estadísticas múltiples — permite separar el ruido del efecto real, protegiendo los ingresos del negocio y sustentando cada decisión con evidencia cuantitativa.

## 🔮 Próximos Pasos / Mejoras Futuras
- **Test Multivariante (MVT):** Extender el análisis para evaluar múltiples variantes simultáneamente y optimizar la velocidad de iteración.
- **Segmentación de Resultados:** Desagregar el impacto del experimento por segmento de usuario (nuevo vs. recurrente, dispositivo, fuente de tráfico) para identificar efectos heterogéneos.
- **Automatización del Framework:** Desarrollar un pipeline reutilizable que estandarice la evaluación estadística de futuros experimentos A/B en la organización. 
