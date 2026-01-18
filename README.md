![Logo](https://github.com/ClaudioRojasMon/Trayectorias_Academicas/blob/79b362cb03730b1e8f20d9116f9fc4cbfddd78fc/Original%20Logo.png)


# 📊 Trayectorias Académicas - Análisis Longitudinal

**Análisis longitudinal de rendimiento estudiantil en asignaturas troncales y su relación con resultados en pruebas estandarizadas (PSU/PDT)**

![R](https://img.shields.io/badge/R-276DC3?style=flat&logo=r&logoColor=white)
![RStudio](https://img.shields.io/badge/RStudio-75AADB?style=flat&logo=rstudio&logoColor=white)
![License](https://img.shields.io/badge/License-CC--BY-green)

---

## 📖 Sobre este proyecto

Este proyecto surge de una solicitud de una **Fundación Educacional** que necesitaba un análisis profundo de las trayectorias académicas de sus estudiantes para entender:

- 🎯 Patrones de rendimiento en asignaturas troncales a lo largo de la escolaridad
- 📈 Evolución del desempeño desde 1° Básico hasta IV° Medio
- 🔗 Relación entre rendimiento escolar y resultados en pruebas PSU/PDT
- 👥 Diferencias de rendimiento por género
- 📊 Identificación de ciclos críticos que requieren intervención

### 🎯 Problema abordado

La institución educativa enfrentaba:

- ❌ **Falta de visión longitudinal** - No había seguimiento integrado del rendimiento estudiantil a través de los años
- ❌ **Decisiones sin datos** - Las intervenciones pedagógicas no estaban respaldadas por análisis sistemático
- ❌ **Desconexión entre evaluaciones** - No se relacionaban las notas escolares con resultados en pruebas estandarizadas
- ❌ **Información fragmentada** - Los datos existían pero no estaban sistematizados ni analizados

### ✅ Solución entregada

Sistema completo de análisis que proporciona:

- 📊 **Visualizaciones comprensivas** - Más de 100 gráficos de distribución, tendencia y comparación
- 📈 **Análisis estadístico robusto** - Box plots, QQ plots, correlaciones por género y nivel
- 🔍 **Seguimiento por cohorte** - Trayectorias de generaciones 2016-2020
- 📋 **Reportes ejecutivos** - Presentaciones generadas automáticamente en múltiples formatos
- 💡 **Insights accionables** - Identificación de puntos críticos para intervención

---

## 📊 Metodología

### Fuentes de datos

| Fuente | Período | Contenido |
|--------|---------|-----------|
| **Actas de notas** | 2017-2020 | Promedios generales y por asignatura (1° Básico a IV° Medio) |
| **Resultados PSU/PDT** | 2017-2020 | Puntajes en pruebas de admisión universitaria |
| **Variables demográficas** | - | Género, curso, generación |

### Proceso de análisis

**Parte I: Construcción de dataset**

- Consolidación de 4 años de actas de notas
- Cálculo de promedios por estudiante en asignaturas troncales:
  - Lenguaje
  - Matemáticas
  - Historia y Ciencias Sociales
  - Ciencias Naturales (Biología, Física, Química)
  - Inglés
- Incorporación de variable género (F/M)
- Integración con resultados PSU/PDT

**Parte II: Visualización y análisis**

Dos tipos principales de gráficos:

1. **Gráficos de tendencia**
   - Puntos con línea de tendencia
   - Evolución del rendimiento por nivel y año
   
2. **Box plots (diagramas de caja)**
   - Distribución de notas/puntajes por nivel
   - Mediana (línea central)
   - Media (punto rojo)
   - Moda (punto naranja)
   - Valores atípicos (puntos verdes)
   - Permite identificar dispersión y casos extremos

**Parte III: Análisis comparativo**

- Comparaciones por género
- Comparaciones entre generaciones
- Correlaciones entre asignaturas
- Relación notas escolares vs PSU/PDT

---

## 🚀 Estructura del proyecto

```
Trayectorias_Academicas/
│
├── datos/                              # Datos del proyecto (no incluidos)
│   ├── Base de Datos 2018-2020 II.xlsx
│   ├── Base de PSU 2017-2020.xlsx
│   └── [archivos de datos sensibles]
│
├── Rendimiento_Academico.Rmd          # Script principal de análisis
│
├── outputs/                            # Resultados generados
│   ├── presentacion.html              # Presentación interactiva
│   ├── presentacion.pptx              # PowerPoint
│   └── graficos/                      # Gráficos individuales
│
├── README.md                          # Este archivo
└── LICENSE.md                         # Licencia Creative Commons
```

---

## 📈 Tipos de análisis incluidos

### 1. Análisis de Distribución

- **Histogramas** por asignatura, nivel y año
- **Box plots** para visualizar dispersión
- **QQ plots** para verificar normalidad de distribuciones

### 2. Análisis de Tendencias

- Evolución de promedios por nivel (1° Básico → IV° Medio)
- Tendencias por asignatura y año
- Comparaciones entre ciclos escolares

### 3. Análisis Comparativo

- Rendimiento por género en cada asignatura
- Comparación entre generaciones
- Evolución de cohortes específicas (2° básico 2017 → 6° básico 2020)

### 4. Análisis de Correlaciones

- Matriz de correlaciones entre asignaturas
- Correlaciones por género
- Relación entre rendimiento escolar y PSU/PDT

### 5. Análisis PSU/PDT

- Distribución de puntajes por año
- Comparación Lenguaje vs Matemáticas
- Relación con rendimiento en III° y IV° Medio

---

## 🛠️ Tecnologías utilizadas

### Lenguaje y entorno
- **R** - Análisis estadístico y visualización
- **RStudio** - IDE para desarrollo
- **R Markdown** - Documentación reproducible

### Librerías principales

```r
# Manipulación de datos
library(tidyverse)
library(readxl)

# Visualización
library(ggplot2)
library(ggthemes)
library(viridis)
library(gridExtra)

# Análisis estadístico
library(dlookr)
library(skimr)
library(modeest)

# Reportes
library(knitr)
library(kableExtra)
library(GGally)
```

---

## 💻 Cómo usar este proyecto

### Requisitos previos

```r
# R versión 4.0 o superior
# RStudio (recomendado)

# Instalar librerías necesarias
install.packages(c("tidyverse", "readxl", "ggplot2", "ggthemes", 
                   "gridExtra", "viridis", "knitr", "skimr", 
                   "dlookr", "modeest", "GGally", "kableExtra"))
```

### Ejecución del análisis

**Opción 1: Generar reporte completo**

1. Abre `Rendimiento_Academico.Rmd` en RStudio
2. Prepara tus datos en formato Excel según la estructura esperada
3. Actualiza las rutas de archivo en el chunk "ImportarDatos"
4. Haz clic en **Knit** → Selecciona formato de salida:
   - `HTML` - Presentación interactiva
   - `PowerPoint` - Para presentaciones ejecutivas
   - `PDF` - Documento estático

**Opción 2: Ejecutar análisis específicos**

```r
# Cargar librerías
source("setup.R")

# Importar datos
base_datos <- read_excel("datos/Base_de_Datos.xlsx")

# Análisis de distribución 2020
base_datos %>%
  filter(AÑO == 2020) %>%
  ggplot(aes(x = CURSO, y = PROMEDIO, group = CURSO)) +
  geom_boxplot(outlier.colour = "green") +
  stat_summary(fun = mean, geom = "point", shape = 18, 
               size = 3, color = "red")
```

### Adaptar a tus propios datos

**Formato esperado de datos:**

Tu archivo Excel debe contener las siguientes columnas:

| Columna | Tipo | Descripción |
|---------|------|-------------|
| AÑO | Numérico | Año escolar (2017, 2018, etc.) |
| CURSO | Numérico | Nivel (1-12, donde 1=1°Básico, 12=IV°Medio) |
| SEXO | Texto | "F" o "M" |
| PROMEDIO | Numérico | Promedio general (escala 1-7) |
| LENGUAJE | Numérico | Promedio en Lenguaje |
| MATEMATICAS | Numérico | Promedio en Matemáticas |
| HISTORIA | Numérico | Promedio en Historia |
| CIENCIAS | Numérico | Promedio en Ciencias |
| INGLÉS | Numérico | Promedio en Inglés |

---

## 📊 Ejemplos de insights obtenidos

### Hallazgos clave del análisis original

**🔴 Puntos críticos identificados:**

- **8° Básico** - Mayor dispersión en rendimiento de Lenguaje y Matemáticas
- **II° Medio** - Caída pronunciada en promedios generales
- **Transición 6°→7°** - Cambio significativo en distribución de notas

**📈 Tendencias observadas:**

- Promedios de Matemáticas consistentemente >5.5 en todos los niveles
- Historia muestra mayor variabilidad entre años
- Inglés mantiene tendencia estable en educación media

**👥 Diferencias por género:**

- Mujeres muestran mejor rendimiento en Lenguaje (todos los niveles)
- Hombres presentan mejor desempeño en Matemáticas (7° en adelante)
- Ciencias: rendimiento similar hasta III° Medio

**🎯 Correlación notas-PSU:**

- Fuerte correlación entre promedios de IV° Medio y puntajes PSU/PDT
- Lenguaje escolar predice mejor PSU Lenguaje que Matemáticas escolar PSU Matemáticas

---

## 📁 Entregables del proyecto

### Para el directorio de la fundación

- ✅ Presentación ejecutiva (PowerPoint)
- ✅ Reporte completo con todos los gráficos
- ✅ Datasets procesados
- ✅ Código fuente documentado

### Para el equipo directivo

- ✅ Dashboard interactivo (HTML)
- ✅ Análisis detallado por nivel y asignatura
- ✅ Recomendaciones basadas en datos

---

## 🎨 Ejemplos de visualizaciones

El proyecto genera más de **100 visualizaciones**, incluyendo:

### Distribuciones
- Box plots de promedios generales por nivel
- Distribución de notas por asignatura
- Histogramas por género y año

### Tendencias
- Evolución de promedios 1° Básico → IV° Medio
- Tendencias por asignatura (2017-2020)
- Comparación entre generaciones

### Comparaciones
- Rendimiento por género en cada asignatura
- Análisis por ciclo escolar
- PSU/PDT vs rendimiento escolar

### Correlaciones
- Matrices de correlación por género
- Relación entre asignaturas
- GGpairs con visualización multivariada

---

## 🔒 Consideraciones de privacidad

### Datos sensibles

⚠️ **IMPORTANTE:** Este repositorio **NO incluye los datos originales** porque contienen información sensible de estudiantes.

Si deseas usar este código:
- Prepara tus propios datos siguiendo el formato especificado
- Asegúrate de cumplir con leyes de protección de datos (Ley 19.628 en Chile)
- Anonimiza información personal antes de compartir resultados

### Buenas prácticas

✅ **Al usar este código, asegúrate de:**
- Obtener consentimiento informado para uso de datos
- Anonimizar identificadores personales
- Almacenar datos de forma segura
- Cumplir con regulaciones locales de privacidad

---

## 💡 Aplicaciones potenciales

Este tipo de análisis puede ser usado para:

### En instituciones educativas
- 📊 Monitoreo de calidad educativa
- 🎯 Identificación de estudiantes en riesgo
- 📈 Evaluación de impacto de intervenciones
- 🔍 Detección de brechas de género
- 📋 Reportes para sostenedores y autoridades

### En investigación educativa
- 📚 Estudios longitudinales de rendimiento
- 🔬 Análisis de factores asociados al éxito académico
- 📊 Validación de instrumentos de evaluación
- 🎓 Investigación sobre transiciones escolares críticas

### En consultoría
- 💼 Diagnósticos institucionales
- 📈 Planes de mejora basados en evidencia
- 🎯 Diseño de sistemas de monitoreo
- 📊 Capacitación en análisis de datos educativos

---

## 🤝 Contribuir

Aunque este proyecto específico está finalizado, puedes:

- 🐛 Reportar bugs en el código
- 💡 Sugerir mejoras en visualizaciones
- 📝 Compartir casos de uso
- 🔀 Hacer fork para adaptarlo a tu contexto

---

## 📝 Estado del proyecto

| Estado | Descripción |
|--------|-------------|
| ✅ **Finalizado** | Proyecto completado y entregado |
| 📅 **Fecha de entrega** | Febrero 2021 |
| 🎯 **Cliente** | Fundación Educacional (colegio particular pagado) |
| 📊 **Período analizado** | Generaciones 2016-2020 |
| 📈 **Alcance** | 1° Básico a IV° Medio (12 niveles) |

---

## 🙏 Créditos y agradecimientos

### Autor Principal

**Claudio Rojas Monsalves** - Director Académico y Analista de Datos

- Conceptualización del proyecto
- Análisis de datos y visualizaciones
- Generación de reportes ejecutivos
- Presentación a directorio y equipo directivo

### Contexto

Este proyecto fue realizado durante mi gestión como Director Académico, aplicando técnicas de data science al análisis educativo para tomar decisiones basadas en evidencia.

### Agradecimientos

- A la Fundación Educacional que confió en este enfoque basado en datos
- A la comunidad de R y tidyverse por sus excelentes herramientas
- A los desarrolladores de ggplot2 por hacer la visualización de datos accesible y poderosa

---

## 📜 Licencia

Este proyecto está bajo **Licencia Creative Commons BY** (Attribution).

Puedes:
- ✅ Usar el código para tus propios análisis
- ✅ Modificar y adaptar a tu contexto
- ✅ Distribuir y compartir

Debes:
- 📌 Dar crédito apropiado al autor original
- 📌 Indicar si realizaste cambios
- 📌 Incluir un link a la licencia

---

## 📧 Contacto

¿Preguntas sobre el proyecto? ¿Interesado en consultoría similar?

**Claudio Rojas Monsalves**  
📧 crojasmon@gmail.com  
💼 [LinkedIn](https://www.linkedin.com/in/claudio-rojas-monsalves)  
🐙 [GitHub](https://github.com/ClaudioRojasMon)

---

## 🔗 Proyectos relacionados

Si te interesó este proyecto, también revisa:

- [📖 analizador-lexile-chile](https://github.com/ClaudioRojasMon/analizador-lexile-chile) - Análisis de complejidad lectora
- [📊 paes-ranking-chile](https://github.com/ClaudioRojasMon/paes-ranking-chile) - Análisis de resultados PAES
- [📚 Apoyo](https://github.com/ClaudioRojasMon/Apoyo) - Jupyter Book de Python para educación media

---

💙 Desarrollado con pasión por la educación desde el sur de Chile 🇨🇱
