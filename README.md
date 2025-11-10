# Selección de Cuentas Bancarias para Jóvenes (Trabajo Multicriterio)

Este repositorio contiene un trabajo académico para la asignatura de Teoría de la Decisión. El objetivo es aplicar y comparar varios métodos de decisión multicriterio para resolver el problema: **"Selección del mejor banco para abrir una cuenta universitaria o joven"**.

## 1. Definición del Problema

El análisis se centra en evaluar 5 alternativas (bancos) basándose en una jerarquía de criterios.

* **Alternativas (Bancos):**
    * Santander
    * BBVA
    * CaixaBank
    * ING
    * Sabadell
* **Criterios:**
    El modelo se estructura en 3 criterios principales y 8 subcriterios:
    1.  **Condiciones Económicas** (Comisiones Cuenta, Comisiones Tarjeta, Comisiones Transferencias, Requisitos Vinculación)
    2.  **Servicios y Comodidad** (Banca Online App, Atención Cliente)
    3.  **Accesibilidad y Beneficios** (Cajeros Oficinas, Beneficios Jovenes)

## 2. Metodología Aplicada

El análisis compara las 5 alternativas aplicando las siguientes técnicas:

* **Proceso Analítico Jerárquico (AHP):** Se implementa de dos formas:
    * Utilizando el paquete `ahp` de R, cargando la estructura y las comparaciones pareadas desde `bancos.ahp`.
    * Replicando el análisis con las funciones R personalizadas de la asignatura (`teoriadecision_funciones_multicriterio.R`) para validar el proceso y analizar la consistencia.
* **Método ELECTRE I:** Se aplica este método de superación para identificar el núcleo de alternativas no dominadas, utilizando los pesos derivados del AHP.
* **Método PROMETHEE:** Se aplica este método para generar un ranking completo. Se implementa de dos formas:
    * Usando las funciones personalizadas de R.
    * Usando el software específico Visual PROMETHEE (para el cual se incluye el archivo `.vpg`).

## 3. Archivos del Repositorio
  * `cuentas_bancarias`: Documento principal que contiene todo el código R, el análisis detallado de cada método y la generación de tablas. Se ha incluido en versión Quarto, HTML y PDF.
  * `bancos.ahp`: Fichero de definición del modelo (YAML) que almacena la jerarquía AHP y todas las matrices de comparación por pares (juicios).
  * `teoriadecision_funciones_multicriterio.R`: Script de R con las funciones base para calcular AHP (variantes 1, 2 y 3), ELECTRE I, PROMETHEE (I y II) y métodos de homogeneización.
  * `teoriadecision_funciones_multicriterio_utiles.R`: Script de R con funciones auxiliares para formatear tablas de resultados (ELECTRE, PROMETHEE Windows) y análisis GAIA.
  * `teoriadecision_funciones_multicriterio_diagram.R`: Script de R con la función para generar el diagrama visual de la jerarquía AHP.
  * `visual_promethee_data_file.vpg`: Archivo de datos de ejemplo exportado para el software Visual PROMETHEE. Para facilitar la visualización de los resultados, se han incluido también capturas `.png` de la tabla de datos y las gráficas correspondientes a los rankings PROMETHEE I y II, además de la gráfica GAIA.
