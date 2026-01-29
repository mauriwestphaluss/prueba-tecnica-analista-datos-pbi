# Informe de Ventas – Artefacto Power BI (PBIP)

## Versión del Artefacto
- **Versión:** v1.0.0  
- **Estado:** Con Errores  
- **Formato:** PBIP (Power BI Project)  

---

## 📘 Descripción General
Este repositorio contiene el artefacto de visualización **Caso_migración**, desarrollado utilizando el formato **Power BI Project (PBIP)** para asegurar trazabilidad, versionamiento y mantenibilidad adecuados en entornos de analítica gobernada.

El reporte implementa un modelo semántico con cálculos DAX, un conjunto de KPIs clave y visualizaciones que operan exclusivamente sobre los datos incluidos en `data/`.

---

## 📁 Estructura del Repositorio

```
/
├── data/
│   └── *.csv                     # Datos de origen utilizados por el modelo
│
├── report/
│   └── pbip/                     # Artefacto Power BI en formato PBIP
│       ├── model.bim             # Modelo semántico + medidas DAX
│       ├── report.json           # Visualizaciones del informe
│       ├── diagramLayout.json    # Diseño del diagrama del modelo
│       └── definition.pbir       # Metadatos del proyecto PBIP
│
├── docs/
│   └── documentación_adicional.md (acá va la documentacion de cambios)
│
├── .gitignore
├── LICENSE
└── README.md                     # Este archivo
```


## 📊 Modelo Semántico

El modelo semántico del artefacto, definido en `model.bim`, está compuesto por dos tablas principales:

**1. Hechos: FactArriendos**
Id_Arriendo [FactArriendos | Excel]
RUT (identificador del cliente) [FactArriendos | Excel]
Id_Pelicula (identificador de la película) [FactArriendos | Excel]
Fecha_Arriendo [FactArriendos | Excel]
Fecha_Devolución [FactArriendos | Excel]
Días Arriendo [FactArriendos | Excel]
Valor Arriendo Diario [FactArriendos | Excel]
Nombre Género, Nombre Categoría, Nombre Comuna (atributos redundantes informativos) [FactArriendos | Excel]


**2. Dimensión: DimClientes**
RUT (clave primaria) [DimClientes | Excel]
Paterno
Materno
Nombre
Dirección
Comuna
Tipo Cliente

**3. Dimensión: DimPeliculas**
Id_Pelicula (clave primaria) [DimPeliculas | Excel]
Nombre Pelicula
Nombre Género
Año
Protagonistas
Director

**4. Dimensión de fechas (DimDate)**
(La genera el desarrollador en Power Query o DAX en base al archivo Calendario.txt de la carpeta resources).
Se emplea para:

Time Intelligence
Cálculo de YTD / MTD / QTD
**Relación activa con Fecha_Arriendo**
Relación inactiva con Fecha_Devolución

---

## 🔐 Seguridad y Gobernanza (RLS)

El artefacto incorpora un rol de seguridad a nivel de filas:

### **Rol:** `GENERO_NORMAL`
- Restringe el acceso a los registros de la tabla *Datos* según el campo `Nombre Género`.

---

## 🔧 Tecnologías y Estándares Utilizados

- **Power BI – PBIP (Power BI Project Format)**  
- **Git / Bitbucket** para versionamiento y control de cambios  
- **Modelo Semántico Tabular**  
- **Lenguaje DAX**  
- **Estándares de visualización institucionales**  
- **Buenas prácticas de repositorios Git**  

---

## 📄 Changelog

### **v1.0.0**
- Publicación inicial del artefacto  
- Implementación del modelo semántico  
- Inclusión de tres medidas DAX  
- Incorporación de rol de seguridad RLS  
- Estructura completa PBIP  