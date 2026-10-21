# Base de Datos Multidimensional: Cobertura Fonasa e Isapre a nivel comunal (2010–2024)

Este repositorio contiene los datos, *scripts* y proyecciones asociados al artículo científico: **"[Inserta aquí el título final del artículo]"**.

## 📄 Resumen
Este proyecto reconstruye y valida un conjunto de datos unificado de la población beneficiaria del sistema de salud chileno (Fonasa e Isapre) entre 2010 y 2024. Mediante técnicas de *back-casting* (modelos de regresión de Poisson con efectos aleatorios espaciales), se imputaron los datos faltantes del periodo 2010-2015, logrando una base con alta granularidad a nivel de comuna, año, sexo, rango etario y tramo de ingreso.

## 📂 Estructura del Repositorio
* **`1_Data_Multidimensional/`**: Contiene los conjuntos de datos limpios y el diccionario de variables.
* **`2_Notebooks/`**: *Scripts* en Python y R utilizados para análisis descriptivo  reportados en el artículo.
* **`3_Proyecciones/`**: Base de datos final consolidada con las retropolaciones 2010-2024 y resultados del análisis de sensibilidad.

## ⚙️ Reproducibilidad
Para reproducir este análisis en tu máquina local:
1. Clona este repositorio: `git clone https://github.com/tu-usuario/nombre-del-repo.git`
2. Ejecuta los notebooks en el orden numerado dentro de la carpeta 2_Notebooks.

## 📊 Uso de los datos
Los investigadores pueden utilizar la base consolidada ubicada en 3_Proyecciones/base_consolidada_2010_2024.csv como covariable o proxy del nivel socioeconómico y de protección financiera poblacional a nivel comunal.

## 📜 Licencia

Este repositorio y su contenido (código, datos y proyecciones) están bajo la licencia **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**.

### Condiciones de uso:
- **Atribución (Attribution):** Debes otorgar el crédito correspondiente citando el estudio original e incluir un enlace a la publicación oficial.
- **No Comercial (Non-Commercial):** No está permitido el uso de este material (base de datos o código) con fines comerciales.
