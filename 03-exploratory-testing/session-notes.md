# Sesión 1

## Charter
Explorar la gestión del carrito de compras y la manipulación de cantidades para verificar la precisión del cálculo de subtotales y la validación de campos.

## ÁREAS
Web App / Catálogo de Productos / Módulo de Carrito de Compras.

## INICIO
18/04/2026 - 08:30 a 09:00 hs

## TESTER
Luz González

## DESGLOSE DE TAREAS
* Configuración y navegación inicial: 10%
* Ejecución de pruebas (inputs y cálculos): 70%
* Registro de observaciones y fallos: 20%

## ARCHIVOS DE DATOS
Categoría: Fish (EST-1 Large Angelfish) y Dogs (EST-6 Male Adult Bulldog).

## NOTAS DE PRUEBA
* Se exploró la adición de diferentes mascotas al carrito y se validó la redirección.
* Al cambiar la cantidad a un número mayor y presionar "Update Cart", el subtotal se calculó correctamente.
* Se probó la manipulación del campo "Quantity" ingresando datos anómalos (letras, valores negativos, vacíos).
* Se aprendió que la aplicación confía en el input del usuario sin validaciones previas en el frontend.

## LISTA DE RIESGOS 
* Riesgo de Lógica de Negocio: Alteración de precios a favor del cliente mediante la manipulación de cantidades.
* Riesgo de Estabilidad: Posibilidad de que un usuario colapse su propia sesión al enviar datos no procesables.

## DEFECTOS (BUGS) 
* BUG-01: Ingresar una cantidad negativa (ej. -5) y actualizar el carrito genera un subtotal negativo, restando dinero del costo total.
* BUG-02: Dejar el campo "Quantity" en blanco o ingresar letras provoca una caída de la página con error de servidor (HTTP Status 500 - java.lang.NumberFormatException).

## INCIDENTES (ISSUES) 
* ¿Existe un control de stock real en el backend o el inventario es infinito? Pude agregar 10,000 unidades sin restricción.

---

# Sesión 2

## Charter
Explorar el flujo de autenticación, creación de cuenta nueva ("Register Now!") y gestión del perfil.

## ÁREAS
Módulo de Autenticación (Sign In) / Formulario de Registro de Usuario / Mi Perfil.

## INICIO
18/04/2026 - 09:00 a 09:30 hs

## TESTER
Luz González

## DESGLOSE DE TAREAS
* Ejecución de pruebas en formulario: 60%
* Pruebas de sesión (login/logout): 20%
* Documentación: 20%

## ARCHIVOS DE DATOS
User ID: testuser2026, Password: 1, Email: correofalso (sin arroba ni dominio).

## NOTAS DE PRUEBA
* Se probó usar contraseñas cortas y formatos de correo electrónico inválidos.
* Al guardar la cuenta, el sistema crea el usuario sin validaciones estrictas y redirige al catálogo.
* Se aprendió que el formulario de "Language Preference" guarda los datos, pero no altera la interfaz gráfica.

## LISTA DE RIESGOS 
* Riesgo de Seguridad: Creación de cuentas con contraseñas extremadamente débiles, facilitando ataques.
* Riesgo de Calidad de Datos: Base de datos propensa a llenarse de correos inválidos, afectando futuras comunicaciones.

## DEFECTOS (BUGS) 
* BUG-03: El campo "Email" permite guardar cadenas de texto sin el símbolo "@" ni dominio válido.
* BUG-04: La contraseña acepta 1 solo carácter, sin validación de seguridad mínima.

## INCIDENTES (ISSUES) 
* Si se intenta registrar un "User ID" ya existente, falta claridad sobre cómo el sistema maneja el error.
* La opción "Enable MyList" en el perfil no parece habilitar ninguna funcionalidad visible.