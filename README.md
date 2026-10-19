# Calidad de datos FinTech — 50 registros en Excel

## Descripción

Mini proyecto de práctica de **limpieza, validación y documentación de calidad de datos** sobre 50 registros ficticios de pagos y productos financieros.

El objetivo es identificar inconsistencias en los datos, comprobar reglas básicas de calidad y documentar los casos que requieren confirmación, sin inventar ni reemplazar importes faltantes.

> **Aviso:** los registros son ficticios y se utilizan exclusivamente con fines de aprendizaje y portafolio. No representan transacciones ni clientes reales.

## Herramientas y funciones

- **Microsoft Excel** para la organización, limpieza y revisión de registros.
- **ESPACIOS** para quitar espacios adicionales en campos de texto.
- **SI** y **O** para aplicar reglas de validación.
- **CONTAR.SI** para calcular indicadores del reporte.
- Comprobaciones y documentación manual de hallazgos.

## Estructura del archivo

El libro `FinTech_Calidad_Datos_50_Portafolio.xlsx` contiene seis hojas:

| Hoja | Propósito |
| --- | --- |
| `Instrucciones` | Objetivo, pasos del ejercicio y fórmulas de referencia. |
| `Resumen` | Indicadores de calidad y comprobaciones de resultados. |
| `Pagos_50_Original` | Versión de referencia del ejercicio; conserva fórmulas y comprobaciones previas que no deben confundirse con la validación final. |
| `Pagos_50_Limpio` | Hoja principal de trabajo con limpieza de texto, validaciones y comprobación por registro. |
| `Hallazgos` | Registro de las cinco incidencias de monto y las acciones recomendadas. |
| `Solución` | Referencias y ejemplos de las fórmulas utilizadas. |

## Procedimiento

1. Revisar los campos capturados y crear columnas de texto limpio con `ESPACIOS`.
2. Validar el estatus contra cuatro valores permitidos: **Aprobada, Pendiente, Rechazada y Cancelada**.
3. Marcar como **Revisar** los montos vacíos o iguales a cero.
4. Comprobar cada registro mediante las columnas de calidad y comprobación.
5. Resumir los resultados con `CONTAR.SI` y documentar los casos que requieren seguimiento.

**Alcance de la limpieza:** `ESPACIOS` corrige espacios adicionales, pero no normaliza por sí sola el uso de mayúsculas y minúsculas. La revisión de estatus del ejercicio se realiza con las reglas documentadas en el archivo.

## Resultados

| Indicador | Resultado |
| --- | ---: |
| Registros analizados | 50 |
| Estatus válidos | 50 |
| Estatus por revisar | 0 |
| Montos válidos | 45 |
| Montos por revisar | 5 |
| Pagos con estatus `Cancelada` | 6 |

### Hallazgos de monto

Se documentaron **cinco registros que requieren confirmación**:

| Fila en `Pagos_50_Limpio` | Hallazgo | Acción recomendada |
| --- | --- | --- |
| 9 | Monto de $0.00 | Confirmar si el importe es válido para la operación. |
| 18 | Monto vacío | Solicitar el importe o confirmar si debe permanecer vacío. |
| 30 | Monto vacío | Solicitar el importe o confirmar si debe permanecer vacío. |
| 42 | Monto vacío | Solicitar el importe o confirmar si debe permanecer vacío. |
| 49 | Monto de $0.00 | Confirmar si el importe es válido para la operación. |

**Criterio aplicado:** los montos sospechosos se marcaron para revisión; no se sustituyeron por cifras supuestas.

## Aprendizajes demostrados

- Uso de fórmulas básicas de limpieza y validación en Excel.
- Detección de valores faltantes y montos en cero.
- Construcción de un resumen cuantitativo de calidad de datos.
- Registro de hallazgos con observaciones y acciones sugeridas.
- Separación entre una hoja de referencia, la hoja de trabajo y la documentación.

## Limitaciones y siguientes mejoras

Este es un **proyecto introductorio de práctica**, no una auditoría financiera ni un sistema automatizado de producción. La hoja `Pagos_50_Original` conserva comprobaciones de una etapa anterior; para interpretar los resultados finales deben consultarse `Pagos_50_Limpio`, `Resumen` y `Hallazgos`.

Como siguientes mejoras se pueden explorar la normalización explícita de mayúsculas/minúsculas, reglas adicionales de validación y un flujo reproducible con Power Query.

## Cómo revisar el proyecto

1. Descargar y abrir `FinTech_Calidad_Datos_50_Portafolio.xlsx` en Microsoft Excel.
2. Consultar `Instrucciones` para conocer el objetivo y las reglas.
3. Revisar los registros y validaciones en `Pagos_50_Limpio`.
4. Consultar `Resumen` para los indicadores y `Hallazgos` para los cinco casos señalados.
5. Revisar `Solución` para ver las fórmulas de ejemplo.

---

*Proyecto de aprendizaje y portafolio personal — limpieza y calidad de datos con Excel.*
