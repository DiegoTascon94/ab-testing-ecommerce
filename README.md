# 🚗 Análisis Interactivo de Mercado: Vehículos Usados en EE. UU.

## 🎯 Contexto del Negocio
El mercado de vehículos usados es altamente dinámico y está influenciado por múltiples factores interconectados. Para los concesionarios y compradores, entender cómo variables como el kilometraje, el año y la condición afectan el precio es crucial para tomar decisiones de inversión acertadas. Este proyecto nace de la necesidad de transformar un conjunto de datos plano en una herramienta de exploración visual en tiempo real.

## 🚀 Objetivo del Proyecto
Desarrollar y desplegar una **aplicación web interactiva** que facilite el Análisis Exploratorio de Datos (EDA), permitiendo a los usuarios identificar patrones de precios y tendencias de inventario de forma dinámica.

## 📊 Alcance del Análisis
* **Datos:** Conjunto de datos de anuncios de venta de vehículos en EE. UU.
* **Procesamiento:** Limpieza exhaustiva de valores ausentes en kilometraje, cilindros y modelos, asegurando la integridad de las visualizaciones.
* **Interactividad:** Implementación de filtros dinámicos que permiten segmentar el mercado por tipo de vehículo, marca y condición.

## 💡 Principales Insights (EDA)
* **Depreciación Crítica:** Se identificó la curva de correlación negativa entre el kilometraje y el precio, detectando los puntos de mayor pérdida de valor.
* **Segmentación por Transmisión:** El volumen de vehículos automáticos domina el mercado, influyendo en la liquidez de los anuncios.
* **Tiempo de Venta:** Análisis del periodo de publicación para identificar qué tipos de vehículos rotan más rápido en el inventario.

## 🛠️ Enfoque Analítico y Funcionalidad
La solución no es solo un reporte estático, sino una **WebApp funcional**:
* **Visualización Dinámica:** Uso de histogramas y gráficos de dispersión interactivos que responden a la entrada del usuario.
* **Ingeniería de Datos:** Creación de un dataset optimizado (`vehicles_clean.csv`) para mejorar el tiempo de respuesta de la aplicación.

## 📈 Métricas y Resultados
* **Accesibilidad:** Disponibilidad del análisis al 100% vía web mediante la nube.
* **Eficiencia Visual:** Reducción del tiempo de interpretación de datos mediante la centralización de KPIs en un dashboard único.

## 🧠 Impacto en Decisiones de Negocio
* **Estrategia de Precios:** Permite a los vendedores ajustar precios competitivos basados en la distribución real del mercado.
* **Optimización de Inventario:** Identificación de las marcas y modelos con mayor presencia y precio promedio para diversificar el stock.

## 💻 Tecnologías y Herramientas
* **Dashboard:** Streamlit (Framework de despliegue).
* **Visualización:** Plotly Express (Gráficos interactivos), Seaborn, Matplotlib.
* **Manipulación de Datos:** Pandas, NumPy.
* **Cloud:** Render (Hosting de la aplicación).

## 🌍 Aplicación Desplegada
La herramienta está disponible para uso público en el siguiente enlace:
👉 [**Visualizador de Mercado - Vehículos Usados**](https://sprint-7-psv8.onrender.com)

---

## 📂 Estructura del Repositorio
```text
├── notebooks/
│   └── EDA.ipynb          # Análisis exploratorio y limpieza de datos
├── app.py                 # Aplicación principal (Streamlit)
├── requirements.txt       # Dependencias del proyecto
├── vehicles_us.csv        # Dataset original (crudo)
├── vehicles_clean.csv     # Dataset procesado para la App
├── .gitignore             # Archivos excluidos de Git
└── README.md              # Documentación profesional
```

## ▶️ Cómo Ejecutar la App (Local)

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/DiegoTascon94/nombre-del-repo.git](https://github.com/DiegoTascon94/nombre-del-repo.git)
   ```
2. **Instalar dependencias:**
   pip install -r requirements.txt

3. **Lanzar la aplicación:**
   streamlit run app.py

## 📝 Conclusiones
Este proyecto demuestra la capacidad de cerrar la brecha entre el análisis técnico en notebooks y la entrega de valor al usuario final. La interactividad de la App permite que personas sin conocimientos técnicos puedan extraer conclusiones valiosas del mercado de vehículos de forma autónoma.

## 🔮 Próximos Pasos / Mejoras Futuras
* **Modelo Predictivo:** Integrar un estimador de precios basado en Machine Learning para predecir el valor de un auto según sus características (Kilometraje, Año, Marca).
* **Filtros Geográficos:** Implementar mapas interactivos si se dispone de datos de ubicación por estado, permitiendo un análisis regional del mercado.   
