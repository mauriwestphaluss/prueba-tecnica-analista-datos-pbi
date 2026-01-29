# 📘 Instrucciones de la Prueba Técnica – Analista de Datos (Power BI)

## 🧭 Descripción General

Esta prueba consiste en revisar, diagnosticar y corregir un artefacto de visualización desarrollado en **Power BI (formato PBIP)** que presenta errores funcionales y problemas de visualización reportados por un usuario final.  
El objetivo es aplicar criterios de análisis, DAX, modelo semántico, diseño visual y buenas prácticas de desarrollo en un entorno de analítica corporativa.

El repositorio incluye:

- Proyecto Power BI en formato PBIP  
- Datos base en la carpeta `data/`  
- Recursos visuales en la carpeta `resources/`  
- README del artefacto de visualización  

Tu tarea será refaccionar el informe, corregir los problemas descritos y migrarlo al nuevo look & feel.

---

## 🧩 1. Clonar o Descargar el Repositorio

Puedes:

- Clonar el repositorio desde GitHub, **o**
- Descargar el archivo ZIP

Asegúrate de mantener íntegra la estructura PBIP del proyecto.

---

## 🐞 2. Errores Reportados por el Usuario

El usuario ha enviado un ticket indicando los siguientes problemas:

### **1. “Problemas con el Año, solo necesito ver los últimos 5 periodos.”**
- Revisar la tabla calendario  
- Validar relaciones y jerarquías  
- Revisar si las medidas responden correctamente al filtro temporal  
- Ajustar DAX en caso necesario  

### **2. “El cálculo del año anterior en el gráfico de barras no funciona.”**
- Ajustar la medida para que el gráfico muestre correctamente el valor del año anterior  

---

## 🎨 3. Migración a Nuevo Look & Feel

Debe realizarse una actualización visual siguiendo la maqueta proporcionada.

### Pasos:

1. Revisar el archivo:  
   **`resources/referente.png`**

2. Crear una página nueva llamada:  
   **`Version UI`**

3. Simplificar la visualización existente en “Versión 1”

4. Rediseñar la nueva página para aproximarse al look & feel indicado en la maqueta

Se Valorara:

- Organización  
- Consistencia visual  
- Coherencia del layout  
- Claridad en la presentación de KPIs  

---

## 🔄 4. Guardar y Entregar el Artefacto

Una vez finalizados los ajustes:

- Guardar el informe en formato **PBIP**
- Verificar que los cambios estén reflejados en:
  - `model.bim` (modelo semántico)
  - `report.json` (visualizaciones)
- Entregar a través de una de las siguientes opciones:

### **Opción A — Repositorio personal**
Subir el proyecto completo a GitHub/Bitbucket y compartir el enlace.

### **Opción B — Enviar ZIP**
Comprimir el proyecto completo (manteniendo la estructura PBIP) y enviarlo por correo.

---

## 📌 Requisitos y Restricciones

- No convertir el proyecto PBIP en un archivo PBIX   
- Mantener la estructura original del repositorio  

---

## ✔ Criterios Evaluados

- Diagnóstico y corrección de medidas DAX  
- Comprensión del modelo semántico  
- Resolución de los errores reportados  
- Calidad y coherencia del diseño migrado  
- Orden y estructura del proyecto PBIP  
- Capacidad de documentar cambios realizados (Revisar README) 

---

## 📬 Resultado Esperado

El resultado esperado es un proyecto PBIP **funcional** que incluya:

- Medidas corregidas  
- Visualizaciones actualizadas  
- Nueva interfaz “Version UI”   
- Proyecto completo listo para versionamiento o despliegue