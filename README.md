# 📦 Control de Inventarios y Pedidos (Compatible con ERP Marino11)

Aplicación web progresiva (**PWA**) diseñada específicamente para la gestión de inventarios y control de stock en entornos de obrador, panadería, pastelería y tienda. Funciona **100% offline**, permitiendo realizar recuentos sin conexión a internet y exportar los resultados con el formato exacto requerido por el **ERP Marino11**.

---

## 🚀 Características Principales

* **Modo 100% Offline**: Almacenamiento seguro en el navegador mediante `LocalStorage` para operar en zonas del almacén sin cobertura Wi-Fi.
* **Carga de Datos Maestros mediante Excel**: 
  * Importación del **Máster de Artículos** (soporta búsqueda avanzada por Nombre/Abreviación, Código de Artículo y **Código Antiguo**).
  * Importación del **Máster de Almacenes**.
* **Conteo Rápido y Consolidación Inteligente**: 
  * Validación estricta de lotes y fechas de vencimiento.
  * **Consolidación automática**: Si se escanea o añade un artículo con el mismo lote y la misma fecha de caducidad, la aplicación suma las cantidades automáticamente en una sola línea en lugar de duplicarlas.
* **Historial y Edición de Inventarios**: Permite guardar las sesiones de conteo, consultarlas, compartirlas o volver a editarlas para corregir o añadir más artículos.
* **Exportación a Excel (Plantilla Marino11)**: Genera ficheros `.xlsx` con las columnas exactas del ERP, incluyendo el stock por lote, la caducidad formateada, el **responsable** y la **fecha/hora exacta del inventario**.

---

## 📂 Estructura del Proyecto

El proyecto está compuesto por tres archivos principales listos para desplegarse en cualquier servidor estático o utilizarse como PWA:

```text
📁 InventarioMarino11/
 ├── 📄 inventario_app.html   # Interfaz principal, lógica de negocio y motor de Excel (SheetJS)
 ├── 📄 manifest.json         # Archivo de configuración de la Progressive Web App (PWA)
 └── 📄 sw.js                 # Service Worker para la caché y funcionamiento sin conexión
