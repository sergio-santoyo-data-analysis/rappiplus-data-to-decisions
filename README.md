# RappiPlus — De Datos a Decisiones de Negocio

**Autor:** Sergio Alberto Santoyo Ambriz — Certificado de Analista de Datos, TripleTen (2026)
**Stack:** Python (Pandas, NumPy) · SQL (CTEs, Joins) · Power BI / Tableau · Estadística

Proyecto capstone del Certificado de Analista de Datos. Evalúa el desempeño del servicio RappiPlus combinando pedidos, catálogo, marketing, eventos de usuario (SQL) y un experimento A/B, para responder preguntas de negocio sobre rentabilidad, comportamiento de usuario, retención y validación de cambios de producto.

## Preguntas de negocio

- ¿Es rentable el negocio?
- ¿En qué punto del funnel se pierden más usuarios?
- ¿Los usuarios regresan después de registrarse?
- ¿La nueva UI de checkout mejora la conversión?

## Metodología

1. Limpieza y validación de calidad de datos en Python
2. Cálculo de KPIs de rentabilidad (revenue, costo, profit, margen)
3. Construcción del funnel de conversión con SQL
4. Retención por cohortes (semana 1–3)
5. Prueba de hipótesis (chi-cuadrado) sobre el experimento A/B del checkout
6. Dashboard ejecutivo en Power BI / Tableau

## Resultados clave

- **Revenue de $51.95M** con **margen de 11.47%** — negocio rentable
- **Conversión general del 80.04%**; mayor fuga (**12.29%**) entre "iniciar checkout" y "agregar método de pago"
- **Retención estable de ~42%** durante 3 semanas — se recomendaron estrategias de activación temprana
- El cambio de UI (**+0.60% en conversión**) **no fue estadísticamente significativo** (p = 0.43), evitando una decisión de negocio basada en una señal falsa

## Visualizaciones

![Funnel de conversión](images/funnel_conversion.png)
![Retención por cohortes](images/retencion_cohortes.png)
![Experimento A/B checkout](images/test_ab_checkout.png)

## Estructura del repositorio

```
├── data/
│   ├── orders_clean.csv
│   ├── catalog_clean.csv
│   └── marketing_clean.csv
├── images/
│   ├── dashboard_overview.png
│   ├── funnel_conversion.png
│   ├── retencion_cohortes.png
│   └── test_ab_checkout.png
├── S12_Estudiante_Proyecto_Final.ipynb                         # Notebook completo del análisis
├── Proyecto_RappiPlus_de_datos_a_decisiones_de_negocio.xlsx    # Datos consolidados
├── Proyecto_final_Sergio_santoyo.pbix                           # Dashboard interactivo (Power BI)
└── README.md
```

> ⚠️ Nota de seguridad: la celda de conexión SQL del notebook tenía originalmente una contraseña de la base de datos de práctica de TripleTen escrita en texto plano. Fue removida y reemplazada por variables de entorno antes de subir este repo — nunca subas credenciales reales a un repositorio público. Los pasos 3-5 (funnel, retención, experimento A/B) requieren acceso a esa base de datos para ejecutarse; los pasos 1-2 (calidad de datos y rentabilidad) son completamente reproducibles con los CSVs incluidos en `data/`.

## Contacto

[LinkedIn](https://www.linkedin.com/in/sergio-alberto-santoyo-ambriz-12b458179) · sergio.santoyo.ambriz@gmail.com
