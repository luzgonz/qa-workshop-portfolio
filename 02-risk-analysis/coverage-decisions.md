# Coverage Decisions

## Riesgos que se probarán primero

- Inconsistencia en el registro de nuevos usuarios (R2): El sistema permite crear múltiples cuentas con el mismo correo electrónico o con campos obligatorios vacíos.
- Inconsistencia de Inventario: El sistema permite finalizar la compra de productos que no tienen stock disponible en tiempo real.

## ¿Por qué esos riesgos son prioridad?

Estos riesgos son prioridad porque afectan la integridad de los datos y la viabilidad del negocio. Permitir registros duplicados o incompletos genera una base de datos corrupta y problemas de acceso para los usuarios. Por otro lado, la falta de control en el inventario provoca ventas de productos inexistentes, lo que deriva en devoluciones manuales, pérdida de confianza del cliente y una gestión logística ineficiente.

## Qué se probará menos o quedará fuera por ahora

- Detalles estéticos y diseño visual: Alineación de elementos, fuentes y colores que no afecten la funcionalidad.
- Pruebas de carga y rendimiento extremo: Comportamiento del sitio ante miles de usuarios concurrentes.
- Compatibilidad con navegadores obsoletos: Soporte para versiones de software que ya no son estándar

## Justificación de exclusiones

Estas exclusiones son razonables porque no bloquean el flujo principal de compra. Se prioriza garantizar la funcionalidad crítica y la integridad de los datos sobre la estética o el rendimiento masivo en esta fase inicial.
