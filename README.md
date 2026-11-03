# Warehouse Inventory — Multi Scanner v4

Actualización de v3 con análisis de fotografía, selección de imagen, lectura múltiple de códigos si BarcodeDetector está disponible, OCR local condicional (TextDetector, no disponible en muchos navegadores), validación manual, ejemplos de 8 etiquetas y selección del origen de Quantity.

## Funciones conservadas
- Registro local de cajas por SKU 150xxxxx y CARTON ID único Cxxxxxxxx.
- Guardar, historial, ruta de exportación donde esté soportada, CSV/JSON, importación de respaldos, catálogo de productos.
- PWA y archivos precargados para uso offline después de instalar mediante HTTPS.

## Limitaciones
- Safari iOS y algunos navegadores Android no soportan BarcodeDetector o TextDetector; la cámara puede abrirse sin decodificar automáticamente.
- No se ha integrado un OCR universal ni se ha verificado qué valor codifica el código de barras bajo QUANTITY. Nunca se interpreta automáticamente como cantidad sin verificación.
- Los ocho registros de muestra son datos de prueba, no inventario guardado.
- Cada teléfono almacena su propia base local; exporta respaldos y evita limpiar datos del navegador.
- Requiere HTTPS para acceso a cámara. No ha sido probado en dispositivos físicos.

## Instalación
Subir los archivos de esta carpeta a GitHub Pages o a otro hosting HTTPS. Abrir en Safari/Chrome, permitir cámara y usar Tomar foto o Elegir imagen. Confirmar todos los campos antes de guardar.


## Cambios v5
- Eliminar una caja individual desde el historial, con confirmación y recálculo.
- Abrir respaldo JSON y combinar registros sin duplicar CARTON ID.
- Exportar TXT, Excel XLSX (Registro y Resumen), PDF mediante impresión del navegador.
- Guardar datos localmente, exportar CSV/JSON y elegir carpeta donde el navegador lo permita.
- PDF usa Imprimir/Guardar como PDF; no genera un PDF binario directamente.
- Se recomienda probar los botones en Safari iOS y Chrome Android antes de uso operativo.


## v6 corregida
Reportes mensuales y trimestrales, CSV/XLSX/TXT y vista PDF imprimible. Corregido HTML de scripts y caché del service worker.
