# Risk Matrix

| ID | Riesgo | Impacto | Probabilidad | Nivel | Justificación |
|---|---|---|---|---|---|
| **R1** | **Inconsistencia de Inventario:** Se permiten finalizar compras de productos sin stock disponible en tiempo real. | 5 | 3 | **15** | Afecta directamente los ingresos y genera una crisis de confianza legal con el cliente. |
| **R2** | **Registro Duplicado/Incompleto:** Se permite crear cuentas con correos repetidos o campos obligatorios vacíos. | 4 | 4 | **16** | Corrompe la integridad de la base de datos y genera una carga excesiva para el soporte técnico. |
| **R3** | **Fallo en Carrito:** El sistema no agrega ciertos productos o se vacía inesperadamente al navegar. | 5 | 3 | **15** | Impacto crítico en la conversión, el usuario abandona la compra si el carrito falla. |
| **R4** | **Error de Validación de Password:** El sistema permite crear cuentas aunque las contraseñas no coincidan en el formulario. | 4 | 2 | **8** | Genera problemas de acceso inmediatos y una percepción de baja calidad en el sistema. |
| **R5** | **Fallo en Registro de Existente:** El sistema se bloquea o da error 500 al intentar registrar un usuario que ya existe. | 3 | 3 | **9** | Indica falta en las validaciones y puede interrumpir la navegación del usuario. |

