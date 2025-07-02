# Análisis de Evasión de Clientes en Telecom X

## Propósito del Análisis
Este proyecto busca identificar los factores clave que contribuyen a la alta tasa de evasión de clientes (churn) en Telecom X. Mediante un análisis exhaustivo de datos históricos de clientes, nuestro objetivo es:

- Identificar patrones y características comunes entre clientes que abandonan el servicio
- Cuantificar el impacto económico de la evasión
- Desarrollar estrategias basadas en datos para reducir el churn en un 50-65%
- Priorizar iniciativas de retención con mayor potencial de ROI

![Distribución de Evasión](https://via.placeholder.com/400x250/3498db/ffffff?text=Gráfico+Evasores+vs+Leales)
*Distribución de clientes evasores (26.5%) vs leales (73.5%)*

## Estructura del Proyecto

```
telecom-x-churn-analysis/
├── data/
│   └── TelecomX_Data.json              # Datos originales de la API
├── notebooks/
│   └── Telecom_X_Churn_Analysis.ipynb  # Notebook de análisis completo
├── reports/
│   └── Executive_Summary.pdf           # Resumen ejecutivo para stakeholders
├── README.md                           # Este archivo
└── requirements.txt                    # Dependencias de Python
```

## Principales Hallazgos e Insights

### 1. Factores Críticos de Evasión
![Tasas de Evasión por Factor](https://via.placeholder.com/600x300/2c3e50/ffffff?text=Factores+de+Evasor)
```markdown
| Factor                | Tasa de Evasión | Impacto Relativo |
|-----------------------|-----------------|------------------|
| Contrato Mensual      | 43%             | 3.6x mayor riesgo |
| Servicio Fibra Óptica | 41%             | 2.5x mayor riesgo |
| <12 meses antigüedad  | 42%             | 60% mayor riesgo |
| 0 servicios adicionales | 41%          | 5.1x mayor riesgo |
```

**Insight clave:** Clientes nuevos con contratos mensuales y servicio de fibra óptica tienen 68% probabilidad de abandonar el servicio en los primeros 6 meses.

### 2. Relación Antigüedad vs Evasión
![Antigüedad vs Evasión](https://via.placeholder.com/400x250/e74c3c/ffffff?text=Antigüedad+vs+Evasor)
- **Punto crítico:** 12 meses de antigüedad
- Clientes con <12 meses: 42% tasa de evasión
- Clientes con >24 meses: 9% tasa de evasión
- **Recomendación:** Programas de retención focalizados en primer año

### 3. Impacto de Servicios Adicionales
![Servicios vs Evasión](https://via.placeholder.com/400x250/2ecc71/ffffff?text=Servicios+vs+Evasor)
```markdown
Cantidad Servicios | Tasa Evasión | Reducción vs 0 servicios
-------------------|--------------|-------------------------
0                  | 41%          | -
1                  | 28%          | -32%
2                  | 17%          | -59%
3+                 | 8%           | -80%
```

**Hallazgo clave:** Cada servicio adicional reduce el riesgo de evasión en aproximadamente 15%.

### 4. Zonas de Alto Riesgo
![Riesgo de Evasión](https://via.placeholder.com/500x300/f39c12/ffffff?text=Zonas+de+Riesgo)
- **Cuadrante crítico:** Clientes con <12 meses y facturación >$70
- Representan solo 18% de clientes pero 42% de evasores
- Potencial de retención: $930K/mes

## Instrucciones de Ejecución

### Prerrequisitos
- Python 3.8+
- Jupyter Notebook
- Librerías: pandas, numpy, matplotlib, seaborn

### Pasos para ejecutar el análisis:
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/telecom-x-churn-analysis.git
   cd telecom-x-churn-analysis
   ```

2. Crear entorno virtual (recomendado):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac)
   venv\Scripts\activate     # Windows
   ```

3. Instalar dependencias:
   ```bash
   pip install -r requirements.txt
   ```

4. Ejecutar Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

5. Abrir y ejecutar:
   ```
   notebooks/Telecom_X_Churn_Analysis.ipynb
   ```

### Configuración Alternativa con Google Colab
1. Subir el notebook a Google Drive
2. Abrir en [Google Colab](https://colab.research.google.com/)
3. Ejecutar todas las celdas (Runtime > Run all)
4. Los datos se cargarán automáticamente desde la API pública

## Recursos Adicionales
- [Diccionario de Datos](docs/DATA_DICTIONARY.md)
- [Presentación Ejecutiva](reports/Executive_Summary.pdf)
- [Repositorio de Datos](https://github.com/alura-cursos/challenge2-data-science-LATAM)

## Contacto
Para preguntas o colaboraciones:
- Nombre: Felipe Cancino
- Email: felcancino@email.com
