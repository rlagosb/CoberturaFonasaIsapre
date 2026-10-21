### Diccionario de Datos: `FACT_BENEFICIARIOS_COMUNAS` 📊

* **`Sexo`**: Identificador numérico del sexo de la población/beneficiario (por ejemplo, `1` para Hombres, `2` para Mujeres, o códigos adicionales/especiales de limpieza).
* **`RangoEdad10`**: Intervalos de edad agrupados en rangos de 10 años (por ejemplo, `[0, 10)`, `[10, 20)`, etc.).
* **`Comuna2024`**: Código único de la comuna homologado a la división político-administrativa vigente al año 2024 (incluyendo la corrección e integración de comunas de la Región de Ñuble).
* **`Año`**: Año correspondiente al registro de la población y los beneficiarios (rango temporal cubierto de 2002 a 2024).
* **`Tramo`**: Categorización de la cobertura o previsión de salud. Incluye los tramos de Fonasa (`A`, `B`, `C`, `D`) y la letra `I` designada para representar a los beneficiarios de Isapre.
* **`Poblacion`**: Cantidad total de personas proyectadas o registradas por el INE para la combinación específica de Comuna, Sexo, Edad y Año.
* **`Beneficiarios`**: Cantidad de personas afiliadas efectivamente al sistema de salud (Fonasa o Isapre) asociadas a ese segmento específico.

### **Descripción de las Columnas del DataFrame `Proyección_2010_2024`**

* **`Año`**: Año correspondiente a la observación o proyección (rango temporal consolidado de 2010 a 2024).
* **`Region`**: Código identificador numérico de la región de Chile en la que se ubica la comuna.
* **`Comuna`**: Código identificador único de la comuna correspondiente a la observación.
* **`Tramo`**: Nivel de cobertura de Fonasa (Tramos A, B, C, D) o Isapre, que caracteriza el estrato previsional/socioeconómico de los beneficiarios.
* **`Sexo`**: Identificador de sexo de la población (por ejemplo, `1` para hombres y `2` para mujeres, según la codificación original).
* **`RangoEdad10`**: Intervalo etario agrupado en bloques de 10 años (por ejemplo, `[0, 10)`, `[10, 20)`, etc.) utilizado para la estimación.
* **`Beneficiarios`**: Cantidad de beneficiarios proyectada (para 2010-2015) o real (para 2016-2024), redondeada al entero más cercano.

### **Descripción de las Columnas del DataFrame `DW_POBLACION_COMUNAS`**

* **`Sexo`**: Código identificador de sexo.
* **`Edad`**: Edad en años individuales.
* **`Comuna`**: Código de la comuna del registro de población.
* **`Año`**: Año de la estimación o censo de población.
* **`Poblacion`**: Cantidad total estimada o censada de personas que pertenecen a la combinación específica de comuna, año, sexo y edad.
* **`RangoEdad10`**: Rango de edad de 10 años obtenido mediante el cruce con el dataframe `edad`.

### Diccionario de Dimensiones 📂

#### 1. DataFrame: `DIM_EDAD` 🎂
* **`Edad`**: Edad de la persona en años individuales.
* **`RangoEdad5`**: Agrupación de edad en intervalos de 5 años.
* **`RangoEdad10`**: Agrupación de edad en intervalos de 10 años (utilizados para el análisis agregado).

#### 2. DataFrame: `DIM_SEXO` 👥
* **`Sexo`**: Código numérico de identificación del sexo (ej. `1` para Hombre, `2` para Mujer).
* **`GlosaSexo`**: Descripción textual correspondiente al identificador numérico (ej. "Hombre", "Mujer").

#### 3. DataFrame: `DIM_COMUNA` 🗺️
* **`Comuna`**: Código territorial histórico o identificador numérico único de la comuna.
* **`GlosaComuna`**: Nombre oficial de la comuna.
* **`Provincia`**: Código identificador de la provincia a la que pertenece la comuna.
* **`Region`**: Código identificador de la región a la que pertenece la comuna.
* **`Region13`**: Región homogeneizada bajo la estructura previa a las nuevas divisiones regionales (para mantener coherencia histórica con datos de 2002).
