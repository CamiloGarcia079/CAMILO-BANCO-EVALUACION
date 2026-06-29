# 🏦 Banco ACME — Plataforma de banca web

Plataforma web para la autogestión de cuentas bancarias, construida **completamente en HTML, CSS y JavaScript puro (Vanilla JS)**, sin frameworks. El cliente puede registrarse, iniciar sesión y operar su cuenta como en un banco real: consignar, retirar, transferir, pagar servicios, fijar metas de ahorro y consultar su historial, todo con persistencia en el navegador.

> Proyecto desarrollado en equipo junto a **Andrés Felipe Guerra**.

---

## ¿Qué hace?

Es una banca digital funcional de principio a fin:

- **Autenticación completa:** registro con validaciones, inicio de sesión y recuperación de contraseña. Al registrarse se asigna número de cuenta y fecha de apertura automáticamente.
- **Dashboard:** resumen del saldo, número de cuenta y fecha de apertura en un diseño de *cards*.
- **Transacciones:** consignaciones, retiros (con bloqueo por fondos insuficientes) y pago de servicios públicos con referencia única.
- **Transferencias** entre cuentas.
- **Metas de ahorro:** el usuario define objetivos y hace seguimiento.
- **Historial:** las últimas 10 operaciones, ordenadas de más reciente a más antigua, con formato de moneda y colores según entrada o salida de dinero.
- **Certificado bancario** dinámico, listo para imprimir.
- **Comprobantes y notificaciones:** cada operación genera un *voucher* imprimible y notificaciones tipo *toast*.
- **Tasas de cambio en vivo**, calculadas en segundo plano con un *Web Worker* para no bloquear la interfaz.

---

## 🛠️ Tecnologías

| Herramienta | Para qué se usa |
|-------------|-----------------|
| **HTML5** | Estructura de las vistas (login, registro, dashboard…) |
| **CSS3** | Diseño responsive con estilo *glassmorphism* |
| **JavaScript (Vanilla, ES Modules)** | Toda la lógica del banco, en módulos reusables |
| **Web Workers** | Cálculo de tasas de cambio sin congelar la interfaz |
| **localStorage** | Persistencia de usuarios, saldos y movimientos |

---

## 🧩 Arquitectura

El código está dividido en **módulos de JavaScript** con responsabilidades claras, en lugar de un solo archivo gigante:

```
js/
├── auth.js              → inicio de sesión
├── register.js          → registro de usuarios
├── forgot.js            → recuperación de contraseña
├── dashboard.js         → panel principal
├── storage.js           → persistencia en localStorage
├── ui.js                → lógica de interfaz y componentes
├── 1_export_csv.js      → exportar movimientos a CSV
├── 2_transferencias.js  → transferencias entre cuentas
├── 3_metas_ahorro.js    → metas de ahorro
├── 4_notificaciones.js  → notificaciones tipo toast
├── 5_web_worker.js      → integración del web worker
├── 6_clave_dinamica.js  → clave dinámica de seguridad
└── workers/exchangeWorker.js → cálculo de tasas en segundo plano
```

Separar la lógica en módulos hace el proyecto más fácil de mantener y de entender, aplicando buenas prácticas de *clean code*.

---

## 🚀 Cómo ejecutarlo

1. Clonar el repositorio.
2. Servir el `index.html` con un servidor local (recomendado **Live Server** de VS Code), ya que el proyecto usa ES Modules.
3. **Crear una cuenta** desde "Registrarse" y llenar los datos.
4. **Iniciar sesión** con el documento y la contraseña registrados.
5. Hacer una consignación y luego probar retiros, transferencias, pagos y metas de ahorro desde el dashboard.

---

## 📚 Destacados técnicos

- **JavaScript modular (ES Modules)** en vez de un único archivo, pensando en mantenibilidad.
- **Web Workers** para tareas en segundo plano sin afectar la fluidez.
- **Diseño responsive** con tema *glassmorphism*, sin frameworks.
- **Persistencia real** de datos entre sesiones con localStorage.

---

## 👤 Autores

**Camilo Andrés García Almeida** · **Andrés Felipe Guerra**
Estudiantes de Desarrollo de Software — Campuslands
[GitHub](https://github.com/CamiloGarcia079) · [LinkedIn](https://www.linkedin.com/in/camilo-garcia-7570693b7/)
