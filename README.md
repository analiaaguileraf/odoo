Proceso de configuración Odoo 16.

-VISTA ADM LOGIN:
Usuario: analiaaguilera@gmail.com
pass: 6qtz-et7g-irmx

-VISTA USUARIO LOGIN:
Usuario: analiaaguilerag@gmail.com
pass: prueba123

Paso 1.
Descargar odoo version 16.

Paso 2.
Creamos un archivo launch.json en visual studio code, tiene la función de personalizar la forma en la que se ve el panel de depuración del debugger o debug console.

Paso 3.
Nos dirigimos al archivo odoo.conf en donde se guardará el numero de proceso del servicio de Odoo.

Paso 4.
Ejecutamos.

Paso 5.
Nos vamos al navegador y escribimos nuestro http://localhost:8069/web/login.

Paso 6.
Configuramos los modelos básicos de:
Producto: Todos los productos cuentan con un nivel de stock mínimo y  un proveedor preferido.
Proveedor: Creamos un modelo básico de proveedor que incluye nombre, datos de contacto y plazos de pago.

Paso 7.
Seguimiento de existencias:
  En el módulo inventario programamos para verificar los niveles de stock diariamente o de baja demanda.
   Obs. Esto se ejecuta automáticamente a las 00:00 hs. todos los días o bien puede ser de manera manual en** operaciones - ejecutar planificador** para que genere una orden de compra y así proceder a el reabastecimiento del stock.
   
Paso 8.
Creación de Orden de Compra:
Automaticamente se genera una orden de compra para productos que se encuentren por debajo del nivel mínimo de inventario. Esta orden incluye detalles como proveedor, artículo, cantidad requerida para alcanzar un nivel establecido y fecha de entrega prevista.

Paso 9.
Aprobación de Orden de Compra:
  Creamos un flujo de trabajo de aprobación simple en el que cualquier orden de compra generada le notifique a un gerente para su revisión y aprobación.
  En la VISTA ADM:
  Seleccionamos un monto mínimo para la aprobación de compra.
  En la VISTA COMPRADOR (usuario):
  Creamos manualmente la orden de compra y enviamos la solicitud de aprobación por correo electrónico.
  En la VISTA ADM:
  Visualizamos la solicitud de aprobación de la orden de compra para su ejecución.
GRACIAS :)
End
