# 🏗️ Análisis de Licitaciones Públicas y Concentración de Proveedores (Singapur, 2015–2021)

## 📌 1. Situación (Contexto y Problema)
En los procesos de contratación pública de Singapur (periodo histórico 2015–2021), la falta de visibilidad sobre la estacionalidad de los montos adjudicados, la alta volatilidad interanual y la concentración de proveedores generan riesgos de sobrecostos e ineficiencias operativas. El objetivo de este proyecto fue analizar un dataset histórico de contrataciones para identificar patrones de gasto, evaluar la concentración de mercado y optimizar la toma de decisiones estratégicas.

---

## ⚙️ 2. Acción (Enfoque Técnico y Stack Utilizado)
El proyecto se desarrolló bajo un flujo analítico *end-to-end* integrando tres pilares tecnológicos:
* **Extracción y Limpieza (Python / Pandas):** Procesamiento inicial de 32,756 registros, aplicando filtros defensivos de integridad para descartar datos sin montos o fechas válidas, obteniendo una muestra analítica confiable de **12,298 contratos**.
* **Modelado y Consultas (SQL / SQLite):** Estructuración de una base de datos local y ejecución de consultas analíticas utilizando funciones de ventana (`LAG`, `OVER`) y agregaciones para calcular variaciones interanuales.
* **Modelado y Visualización (Power BI):** Diseño de un modelo relacional en estrella (*Star Schema*) conectando una tabla calendario personalizada con la tabla de hechos, implementando medidas avanzadas en DAX para *Time Intelligence* (YoY) y análisis trimestral.

---

## ❓ 3. Preguntas de Negocio Abordadas
1. **Evolución Interanual y Estacionalidad:** ¿Cuál ha sido la tendencia YoY del presupuesto total adjudicado y existe estacionalidad en la ejecución a lo largo del año?
2. **Análisis de Competitividad y Proveedores:** ¿Qué proveedores muestran mayor concentración de mercado y dominan el presupuesto de infraestructura?
3. **Distribución por Entidades:** ¿Cuáles son las agencias u organismos públicos que ejecutan los mayores presupuestos licitados?

---

## 📈 4. Resultados y Conclusiones (Hallazgos Clave)
* **Volumen e Impacto Financiero:** Se analizaron exitosamente 12,298 registros limpios que representan un volumen acumulado de **\$38.490 M** en adjudicaciones públicas.
* **Evolución y Volatilidad YoY:** El presupuesto muestra alta volatilidad plurianual, registrando crecimientos significativos de **+132,94% YoY (2017)** y **+43,87% YoY (2019)**, alternados con contracciones marcadas en 2016, 2018 y 2020.
* **Estacionalidad Trimestral:** El análisis temporal demuestra que el **Q3 (Tercer Trimestre)** concentra la mayor ejecución presupuestaria con más de **\$14 mil millones**, marcando el periodo pico de mayor dinamismo.
* **Concentración de Mercado:** Los contratistas dominantes son **WOH HUP (PRIVATE) LIMITED** (\$2.209 M) y **SHANGHAI TUNNEL ENGINEERING CO** (\$1.402 M), acaparando una porción crítica del presupuesto.
* **Principales Entidades:** Las agencias líderes en ejecución presupuestaria son la **Land Transport Authority** (\$9.83 mil millones), **Public Utilities Board** (\$6.21 mil millones) y la **Housing and Development Board** (\$4.89 mil millones).

---

## 💡 5. Recomendaciones Estratégicas de Negocio
1. **Mitigación de Riesgo Presupuestario:** Ante la alta volatilidad interanual, implementar cláusulas de ajuste dinámico por inflación en contratos plurianuales para amortiguar los picos de gasto.
2. **Diversificación de Proveedores:** Promover mayor competitividad en los pliegos de licitación para reducir la dependencia en los Top contratistas dominantes.
3. **Estrategia Comercial (Pricing):** Alinear la postulación de ofertas y recursos operativos con las ventanas de mayor dinamismo identificadas en el Q3.

---
🛠️ **Habilidades técnicas utilizadas:** Python (Pandas), SQL (SQLite), Power BI (DAX, Star Schema), Time Intelligence, Análisis Financiero.
