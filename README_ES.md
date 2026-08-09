# GIROFAC — Plataforma ERP Web Integral

GIROFAC es una plataforma ERP web orientada a la gestión integral de negocio bajo una arquitectura modular y escalable. El proyecto se adopta inicialmente bajo un entorno de desarrollo local basado en la pila **LAMP/XAMPP** (Linux/Windows, Apache, MariaDB/MySQL, PHP 8.x), diseñado con patrones de desarrollo desconectados que garantizan una transición inmediata hacia infraestructuras en la nube (VPS, PaaS o entornos contenedorizados) sin refactorización del código fuente.

La interfaz se basa en principios **Mobile-First** y diseño adaptativo (*responsive*), garantizando la accesibilidad desde cualquier dispositivo y aplicando un control de acceso basado en roles (**RBAC**) que adapta la experiencia de usuario y la visibilidad de los módulos en tiempo real.

**01/07/2026: En proceso de desarrollo**
---

## Módulos del Sistema

### 1. Sistema, Configuración y Control de Acceso
* **Configuración Empresarial y Fiscal:** Centraliza datos fiscales, entornos multiidioma (CA, ES, EN), impuestos (IVA/IRPF) y series de facturación correlativa.
* **Sistema de Autenticación y Roles (RBAC):** Evalúa en tiempo real la matriz de permisos para habilitar o restringir acciones CRUD según el rol.
* **Registro de Auditoría y Trazabilidad:** Logging centralizado para operaciones críticas (accesos, datos sensibles y transacciones financieras).

### 2. Gestión Comercial y CRM
* **Gestión Unificada de Clientes:** Histórico fiscal y operativo para una visión de 360° de la relación comercial.
* **Ciclo de Negociación y Conversión Directa:** Elaboración de presupuestos y conversión automática a factura o proyecto operativo.
* **Contratos Recurrentes y Suscripciones:** Soporte para facturación periódica programada.
* **Validación y Firma Electrónica:** Captura de firma digital en dispositivos móviles con registro de trazabilidad (IP, fecha y hora).

### 3. Operaciones, Proyectos y Soporte Técnico
* **Planificación y Gestión de Proyectos (PM):** Organización en proyectos/tareas con hitos temporalizados y asignación de personal.
* **Control de Tiempo y Partes de Horas:** Imputación de horas facturables y no facturables con cálculo de rentabilidad en tiempo real.
* **Gestión de Incidencias y Tickets:** Soporte a clientes integrado directamente con los partes de horas del proyecto.
* **Gestión del Conocimiento:** Biblioteca técnica interna para documentación y procedimientos.
* **Flujo de Facturación por Horas:** Consolidación automática de horas pendientes en facturas de cliente (`Cliente` ➔ `Proyecto` ➔ `Partes de Horas`).

### 4. Contabilidad y Gestión Financiera
* **Facturación Directa y Derivada:** Emisión y recepción de facturas cumpliendo la normativa fiscal y series correlativas.
* **Gestión de Gastos Operativos y de Personal:** Clasificación de gastos con imputación directa a proyectos.
* **Conciliación Bancaria Automática:** Emparejamiento de extractos bancarios con facturas pendientes y liquidaciones.
* **Informes y Registros Fiscales:** Libros de registro y cálculos preliminares para liquidaciones de IVA e IRPF.

### 5. Logística, Inventario y Gestión de Proveedores
* **Gestión de Proveedores y Catálogo:** Datos de compra, listas de precios y parámetros financieros (coste vs. PVP) vía SKU.
* **Control de Inventario en Tiempo Real:** Alertas automáticas por stock mínimo.
* **Automatización de Movimientos de Stock:** Descuento e incremento automático de unidades según facturas de venta u órdenes de compra.

### 6. Recursos Humanos, Control Horario y Gestión de Personal
* **Control Horario y Fichajes:** Registro diario de la jornada (entradas, salidas y pausas) para el cumplimiento laboral.
* **Planificación y Ausencias:** Gestión de cuadrantes, turnos, vacaciones y bajas médicas.
* **Imputación Coste-Hora y Analítica:** Enlace del coste/hora empleado con partes de horas para determinar el margen real del proyecto.

### 7. Marketing, Comunicación y Agenda Corporativa
* **Marketing por Correo:** Creación y envío masivo con plantillas dinámicas.
* **Gestión de Marketing Social:** Planificación editorial mediante calendario interactivo.
* **Agenda Unificada:** Citas comerciales, hitos de proyectos y acciones de marketing en una sola interfaz.
* **Segmentación Dinámica:** Filtro de audiencias a partir de los datos del CRM.

---

## Arquitectura Global de Datos e Integración

El valor diferencial de GIROFAC radica en la **interconexión nativa** de todos sus módulos operativos, eliminando los silos de información:
1. El ciclo de **CRM** transforma opciones de éxito en proyectos (**Operaciones**) o facturas.
2. La actividad de **Operaciones** calcula el coste en tiempo real basándose en **RRHH** y deriva horas a **Finanzas**.
3. La compra/venta mantiene sincronizados el **Inventario** y el flujo de caja, finalizando en la **Conciliación Bancaria**.
