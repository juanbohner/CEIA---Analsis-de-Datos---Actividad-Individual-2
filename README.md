# Análisis de Datos - Actividad Individual 2 (CEIA - FIUBA)
## Análisis Exploratorio de Datos (EDA) en Pingüinos del Archipiélago Palmer

**Alumno:** Juan Ignacio Bohner  
**Especialización:** Carrera de Especialización en Inteligencia Artificial (CEIA) - Facultad de Ingeniería, Universidad de Buenos Aires (FIUBA)  
**Materia:** Análisis de Datos  
**Dataset:** `penguins_lter.csv` (Palmer Station Antarctica LTER)  

---

## 🎯 Objetivos y Alcance del EDA
1. **Contexto Geográfico Real:** Localización precisa de las colonias reproductivas y de la estación Palmer mediante proyección sobre imagen satelital real de alta resolución (NASA / USGS / Esri).
2. **Integridad y Datos Faltantes:** Evaluación sistemática de completitud y nulidad con la biblioteca `missingno` (mecanismo MCAR en medidas morfológicas).
3. **Distribución Poblacional y Segregación Insular:** Análisis de composición y anidamiento por especie (*Adelie*, *Gentoo*, *Chinstrap*) e isla (*Torgersen*, *Dream*, *Biscoe*).
4. **Análisis Probabilístico de Variables Continuas:** Histogramas, curvas KDE, medidas de tendencia central, dispersión y forma (Media, Varianza, Std, Asimetría y Curtosis), tanto a nivel global como desagregado por especie.
5. **Contraste de Hipótesis de Normalidad (Shapiro-Wilk):** Evaluación formal con $\alpha = 0.05$ de la compatibilidad gaussiana de las variables condicionales a la especie.
6. **Detección y Estudio de Outliers (Criterio IQR de Tukey):** Identificación de la "paradoja de escala" entre el análisis global (0 outliers) y el análisis condicional (9 outliers biológicos válidos).
7. **Paradoja de Simpson y Dimorfismo Sexual:** Inversión de correlación en la morfología del culmen ($r = -0.24$ global vs. $r > +0.39$ intra-especie), alometría aleta-peso y análisis multivariado de correlación (Pearson y Spearman).

---

## 📁 Estructura del Repositorio
```text
.
├── actividad_Ind_2.ipynb     # Notebook interactivo completamente ejecutado con visualizaciones
├── penguins_lter.csv         # Dataset original de campo (Palmer Station LTER)
├── img/
│   ├── satelite_palmer_real.png # Fotografía satelital real de la Isla Anvers
│   └── mapa_anvers_palmer.png   # Mapa topográfico esquemático complementario
└── README.md                 # Documentación y síntesis del trabajo
```

---

## 🚀 Requisitos e Instalación
Para ejecutar el notebook localmente, se recomienda Python 3.10+ y las siguientes librerías:

```bash
pip install numpy pandas matplotlib seaborn scipy missingno Pillow
```
