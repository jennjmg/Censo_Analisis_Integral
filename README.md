# 📊 Análisis del Censo – Ejercicios de Excel
Este proyecto recopila y analiza un conjunto de datos del censo, explorando indicadores socioeconómicos clave mediante Excel. El objetivo es comprender la distribución de ingresos, el endeudamiento y las características demográficas de la población, aplicando fórmulas, pivots y gráficos para obtener insights claros y visuales.

## 📝 Ejercicio 1 – Preparación y Cálculos Iniciales
Consultas y fórmulas realizadas en el sheet Censo:
* Columna “Es Ingeniero/a?”: Detecta si la profesión es ingeniero usando =IF(D2="Ingeniero"; "SI"; "NO"). Permite segmentar la población por profesión técnica.
* Columna “Cumple Condiciones Familiares y Salario”: =IF(AND(F2>3;G2>30000); "Cumple"; "No Cumple") identifica familias con más de 3 integrantes y salario mayor a 30k.
* Columna “Código”: Se asigna un código numérico a cada nacionalidad usando =VLOOKUP(E2;País!A:B;2;FALSE) para facilitar filtros y agrupamientos.
* Columna “Salario per capita”: Calcula el ingreso por persona en la familia: =G2/F2.
* Columna “¿Gana más que la deuda?”: =IF(G2>-H2;"SI";"NO") indica si los ingresos superan las deudas.
* Columna “Categoría Salarial”: =IF(G2<10000;"Bajo (<10k)";
   IF(G2<30000;"Medio (10k-30k)";
   IF(G2<60000;"Alto (30k-60k)";
   "Muy Alto (>60k)"))) Categoriza los salarios en 4 rangos 

## 📊 Ejercicios 2 – Exploración de Datos con Pivots
* Ejercicio 2.1: Pivot para explorar salarios según profesión (sumas, conteos, máximos, mínimos y promedios).
* Ejercicio 2.2-2.3: Pivot por año y mes de nacimiento para analizar la distribución temporal de los nombres y salarios. Esto permite ver tendencias demográficas y patrones de edad en los ingresos.
* Ejercicio 2.4-2.5: Pivot con filtros de integrantes de familia, nacionalidad y profesión; valores como promedio de salario.
* Ejercicio 2.6: Pivot mostrando proporción de salario por profesión (%).
* Ejercicio 2.7-2.8: Pivot con nacionalidad en columnas y profesión en filas; valores sumados y formato condicional para resaltar máximos y mínimos. Filtros interactivos por profesión, integrantes y año de nacimiento.
* Ejercicio 2.9: Pivot con nacionalidad y profesión en filas y suma de salario en valores.

## 📈 Ejercicios 3 – Gráficos
* Ejercicio 3.1-3.3: Histogramas y scatter plots para visualizar distribución de salarios y relación con deuda.
* Ejercicio 3.4: Pie chart basado en “¿Gana más que la deuda?” para analizar la proporción de la población financieramente estable.
* Ejercicio 3.5-3.6: PivotCharts de evolución anual de salarios (promedio, mínimo y máximo).
* Ejercicio 3.7: PivotChart con promedio de salario y promedio de integrantes por año.

## 🧠 Conclusión
* Desigualdad Salarial: La mayoría de la población se concentra en rangos bajos mientras una minoría concentra altos ingresos (regla 80/20).
* Relación Ingresos vs. Deuda: A mayor ingreso, mayor deuda; reflejo del acceso al crédito y del poder adquisitivo.
* Vulnerabilidad Financiera: Una proporción significativa de la población tiene deuda superior a sus ingresos.
* Crecimiento Salarial y Estructura Familiar: A lo largo de los años, los ingresos promedio muestran una tendencia ascendente; el tamaño familiar permanece relativamente estable.
* Visualización Integral: Los gráficos y pivots permiten ver patrones por país, profesión, año de nacimiento y tamaño familiar, ofreciendo una visión completa de la dinámica socioeconómica.

En resumen, este análisis del censo ofrece insights clave sobre distribución de ingresos, endeudamiento y composición familiar, sirviendo como base para decisiones estratégicas, estudios de mercado o políticas públicas.
