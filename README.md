Proyecto Banco Acme (JavaScript)
Este repositorio contiene la solución al caso práctico del Banco Acme, una plataforma web para la autogestión de cuentas bancarias de los clientes. Ha sido construida completamente en HTML, Vanilla CSS y Vanilla JS, sin dependencias de frameworks externos.

Funcionalidades Completadas
Inicio de Sesión:
Validación de credenciales locales.
Redirección funcional tras iniciar sesión correctamente.
Registro de Usuario:
Formulario completo con validaciones nativas y explícitas.
Asignación de número de cuenta automatizado y fecha de creación al registrarse.
Recuperación de Contraseña:
Verificación de identidad estricta y cambio de credenciales de seguridad desde las interfaces del cliente.
Dashboard y Resumen de Cuenta:
Panel informativo principal. Permite la visualización global del saldo actual, número de cuenta y fecha de apertura presentados en un diseño de Cards UI.
Manejo de Transacciones:
Consignación Electrónica: Suma valor al saldo final y registra contablemente en los repositorios del navegador de forma segura.
Retiros de Dinero: Resta valor al saldo (incluye bloqueos por insuficiencia de fondos frente a montos irreales).
Pago de Servicios Públicos: Permite elegir e iterar sobre los tipos de servicios integrados disminuyendo el balance y generando una referencia alfanumérica única.
Historial Operativo:
Visualización ordenada descendente (Nuevas a antiguas) de las últimas 10 transacciones.
Incluye formato de moneda local y distinciones por colores según la entrada/salida del capital de la cuenta.
Certificado Bancario:
Documento dinámico del certificado con los datos en vivo para su expedición inmediata mediante utilidades de impresión nativa.
Comprobantes y Alertas de Transacción:
Al generarse una operación (sea esta exitosa o errónea), se ejecutan notificaciones estilo "Toast" estéticas que retroalimentan al usuario.
Todo movimiento genera en pantalla un recibo/voucher con detalles estructurados (fecha, titular, valores) listos para guardarse en PDF o ser impresos.
Persistencia de Datos:
Utilización de la JSON Data Store Architecture adaptada para los motores integrados del navegador (localStorage), satisfaciendo de este modo el principal pilar del requisito de la evaluación técnica.
Guía de Despliegue y Ejecución
Clonar el repositorio completo dentro de sus gestores locales.
Servir el archivo inicial (index.html) por medio de un host local (Recomendado utilizar "Live Server" desde Visual Studio Code).
Paso 1, Nuevo Registro: Obligatorio como un primer paso, dirigirse desde el formulario principal al menú inferior de "Crear cuenta", rellenar los datos fielmente.
Paso 2, Iniciar Sesión: Ingresar el tipo de documento exacto y la identificación y la contraseña utilizada.
Iniciar la evaluación navegando por el entorno del Dashboard interactivo. (Es necesario primero realizar una consignación de fondos exitosa y posterior testear los métodos abstractos de retiros y pagos).
Características Técnicas Aplicadas
Vanilla ES Modules: Uso adecuado de prácticas modernas de Clean Code que particionan el sistema en módulos reusables (js/storage.js, js/auth.js, etc.).
Patrones de Diseño UI Contemporáneos: Implementación de Grids escalables y estilización unificada que prescinde de frameworks voluminosos obteniendo alto rendimiento y Responsive Design total.
Glassmorphism Theme Style: Implementación y despliegue del estilo visual Glassmorphism lo que brinda elegancia, modernismo y credibilidad acorde al nivel institucional de "Banco Acme".
Autores: Andrés Felipe Guerra | Camilo Andrés Garcia
