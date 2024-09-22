# Riesgo Relativo en lookerstudio

Ficha Técnica: Proyecto de Análisis de Datos

Título del Proyecto: Riesgo Relativo en Looker Studio

Objetivo:
Realizar una prueba de hipótesis, utilizando una técnica de analisis de datos de segmentación y riesgo relativo.

Equipo:
Trabajo Individual.

Herramientas y Tecnologías:
- Python
- Google Colab
- Google BigQuery.
- Looker Studio.
- Google Slides.

Procesamiento y análisis:
- limpieza de datos
- exploración de datos
- consultas SQL
- Técnicas de Análisis de datos
- Técnicas de Machine Learning
  
Resultados y Conclusiones:
Se probo la hipótesis mediante insights concluidos por gráficos y técnicas de análisis.

Calculo de Riesgo Relativo:
```sql
 COUNTIF(loan_status = 'Mal Pagador') / COUNT(*) AS risk_of_default,
```
Segmentacion de Tipo de Cliente:

```sql
  CASE 
    WHEN more_90_days_overdue > 0 THEN 'Mal Pagador'
    WHEN number_times_delayed_payment_loan_30_59_days > 2 THEN 'Mal Pagador'
    WHEN number_times_delayed_payment_loan_60_89_days > 1 THEN 'Mal Pagador'
    WHEN debt_ratio > 0.4 THEN 'Mal Pagador'
    ELSE 'Buen Pagador'
  END AS loan_status
```


Dashboard

![Dashboard](dashboard.png)


Limitaciones/Próximos Pasos:

Enlaces de interés:
[google slides](https://docs.google.com/presentation/d/1eBlx9hKla9FAeFiUN3BKeECJP97DlD57f0p1xYaDhSE/edit?usp=sharing)
[informe en looker studio](https://lookerstudio.google.com/reporting/58ab40fa-c933-4253-8695-886ee40f4b21)
[google colab](https://colab.research.google.com/drive/1Fte-_pmgMSEDIb4N1X3mWFMpx6021qYp?usp=sharing)
