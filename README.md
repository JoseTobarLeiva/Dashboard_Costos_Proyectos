# 📊 Dashboard de Costos y Proyectos

Este proyecto muestra un **Dashboard Interactivo** desarrollado en **Power BI**, se realizo con el objetivo de analizar:
- Movimientos de materiales en distintos proyectos.
- Comparativa entre cantidades ingresadas y salidas.
- Análisis de gasto de materiales por proyecto y SKU.
- Detección de incongruencia en los materiales usados para los proyectos.
- Tener un registro de todos los materiales utilizados en los diferentes proyectos.


---


## 🛠️ Herramientas Utilizadas
- **Power BI** Para visualización y modelado
- **DAX** para cálculos personalizados.
- **Power Query** para limpieza y transformación de datos.
- **Excel** para integración de información.
- **Odoo* Para recopilar los datos para analizar.


---


## Formulas DAX utilizadas
- Para calcular el coste de cada material se tuvo que conectar dos tablas una con el costo del material y otra con el total de movimientos por proyectos
"precio del material = SUMX(Movimientos,Movimientos[Realizado] * RELATED(Stock[Coste]))"
- Para hacer visible la fecha del proyecto tanto inicial como final se tuvieron que utilizar formulas
" Fecha Final por Proyecto = CALCULATE([Fecha Final],
  (FILTER(Movimientos,Movimientos[Entrada/Salida]="Salida"))) "

" Fecha Inicial por Proyecto = CALCULATE([Fecha Inicial],
  (FILTER(Movimientos,Movimientos[Entrada/Salida]="Salida")))"
---


## 📷 Capturas de pantalla


![Dashboard](https://github.com/user-attachments/assets/52bc2c54-2c11-49a3-9b4d-48bc7eea5858)

- Se puede visualizar todos los los materiales utilizados en el proyecto S00253 donde tiene la cantidad total del costo de materiales, ademas de tener una tabla con los productos - Costo total - Cantidad utilizada en el proyecto - Unidad de medida del material. 
- El proyecto tiene filtros para ver los materiales utilizados por categoria (Adhesivo, electrico, gasfiteria, terminaciones, etc), ademas de poder cambiar entre proyectos desde el primero hasta el ultimo ingresado al sistema Odoo.

![Dashboard_Categoria](https://github.com/user-attachments/assets/6a436ceb-c8e6-463d-9d40-5d9d20a02294)


--


## 📌 Notas
- Por motivos de confidencialidad, no se incluyen los costos de materiales, el costo total del proyecto ni el archivo '.pbix' con información original
  
