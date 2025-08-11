# 📊 Informe Diario Multidimensional de Seguridad

**Versión:** 3.1  
**Autor:** Unidad de Seguridad SMA  
**Confidencialidad:** ALTO  
**Última actualización:** {{FECHA_ACTUAL}} {{HORA_ACTUAL}}  

---

## 📌 Descripción
Sistema de monitoreo integral para **orden público, movilidad, clima y riesgos**.  
Su objetivo es proporcionar una **visión completa y en tiempo real** para apoyar la toma de decisiones estratégicas en entornos críticos.

---

## 🎯 Objetivos
- Recopilar y clasificar noticias relevantes de fuentes oficiales y medios de comunicación.
- Monitorear condiciones meteorológicas en zonas estratégicas.
- Evaluar el estado de las vías y detectar bloqueos o paros en tiempo real.
- Calcular matriz de riesgos automática combinando probabilidad e impacto.
- Generar salidas automáticas en **PDF**, **Excel** y **JSON**.
- Integrar datos en un **Dashboard Power BI** con KPIs y mapas dinámicos.

---

## 🗂 Estructura del JSON

### 1. `metadata`
Información general:
- Versión, tipo, descripción, autor, zona horaria, nivel de confidencialidad.

### 2. `variables_globales`
Fechas, horas y rangos de consulta reutilizables.

### 3. `configuracion_dinamica`
Rangos e intervalos de actualización automática.

### 4. `dimensiones_analisis`
1. **Recopilación de Noticias**  
   - Categorías, fuentes, filtros, clasificación de criticidad.  
2. **Gráficos Estadísticos**  
   - Tendencias, mapa de calor, distribución horaria.  
3. **Dashboard Power BI**  
   - Conexión con dataset y widgets configurables.  
4. **Matriz de Riesgos**  
   - Probabilidad × impacto → nivel de riesgo.  
5. **Análisis Meteorológico**  
   - API OpenWeather, ubicaciones estratégicas, alertas.  
6. **Estado de Vías**  
   - Fuentes de tráfico y métricas viales.  
7. **Monitoreo de Bloqueos**  
   - Palabras clave, nivel de confianza y zonas de vigilancia.  

### 5. `salidas_automaticas`
Formatos y canales de distribución.

### 6. `auditoria`
Historial de ejecuciones y validaciones.

### 7. `validaciones`
Control de fechas, duplicados y uso de fuentes offline.

---

## 📊 Diagrama de Flujo del Sistema

```mermaid
flowchart TD
    A[Inicio del Proceso] --> B[Recopilación de Noticias]
    A --> C[Consulta Meteorológica]
    A --> D[Estado de Vías]
    
    B --> E[Matriz de Riesgos]
    C --> E
    D --> E

    E --> F[Generación de Gráficos]
    F --> G[Dashboard Power BI]
    E --> H[Alertas Automáticas]
    
    H --> I[Distribución: Email / SharePoint / Teams]
    G --> I
    
    I --> J[Fin del Proceso]

