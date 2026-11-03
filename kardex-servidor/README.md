# PRAAT · alojamiento externo del piloto

Preparación para Render: un servicio 0.5c-512mb (US$7/mes) y disco persistente de 1 GB (US$0.25/mes). Base estimada US$7.25/mes antes de impuestos o consumos adicionales; confirmar precio en la pantalla de contratación. El alta del servicio genera cargos: no ejecutar sin aprobación del propietario. Este paquete no contrata ni publica por sí mismo.

El servicio es para pruebas controladas; no es una validación de capacidad para 3,000 alumnos simultáneos. SQLite usa un solo servicio con disco persistente. Antes de operación institucional se deben definir recuperación del administrador, copias de seguridad consistentes de SQLite fuera del servidor, monitoreo y el dimensionamiento correspondiente. Los reinicios y despliegues pueden interrumpir brevemente un servicio con disco.

## Activación
1. Crear o abrir una cuenta de Render del propietario y conectar el repositorio autorizado.
2. Crear un Blueprint desde el repositorio y elegir el archivo kardex-servidor/render.yaml. Revisar y aprobar la cotización antes de crear recursos.
3. Render asigna su dirección HTTPS e informa RENDER_EXTERNAL_URL automáticamente. El servidor se niega a iniciar en producción si no conoce su origen HTTPS o falta la clave de activación.
4. Copiar PRIVADAMENTE PRAAT_SETUP_TOKEN desde las variables del servicio e introducirlo en la pantalla inicial junto con el ID y contraseña que el propietario elija. Nunca enviar esa clave por chat ni compartirla con el compañero.
5. Entrar como administrador. En Sincronización, importar por el formulario privado la copia JSON validada de Drive. Los datos reales no forman parte de esta imagen ni del repositorio público.
6. En Acceso de colaboradores, crear un ID y una clave temporal individual para el compañero. Ese acceso es solo de consulta y exige cambio de clave al entrar; no necesita correo ni ChatGPT. El propietario puede suspender o restablecer su acceso.
7. Para alumnos, usar Cuentas y accesos. Cada cuenta se vincula a un solo expediente y solo consulta sus propios registros. Verificar la identidad antes de asignarla.

No copiar la base del piloto local por archivos mientras el servidor esté activo: contiene información personal y sesiones. Esta imagen inicia vacía y permite importar la copia aprobada después del inicio de sesión. Las contraseñas y sesiones locales no se trasladan automáticamente.

## Fuentes
Drive y Zoho siguen pendientes de credenciales de lector autorizadas. Configurar PRAAT_GOOGLE_CREDENTIALS_FILE y PRAAT_ZOHO_CREDENTIALS_FILE como rutas de archivos secretos del servidor, y el archivo /var/data/praat/sync-config.json con los libros y el mapeo del reporte. Se usa solo lectura en ambos proveedores. No incluir secretos en Git, en render.yaml ni en el HTML.

Los cambios de la ficha en Drive pueden suspender automáticamente una cuenta cuando cambia el nombre para que se revise la identidad. Una actualización fallida conserva la última copia válida.

## Seguridad del piloto
HTTPS obligatorio detrás del proxy, cookies Secure/HttpOnly/SameSite, código privado para crear al primer administrador, contraseñas con hash, bloqueo tras 3 fallos, comprobación de permisos en cada petición, protección de escrituras con origen y CSRF, revocación al suspender/restablecer y ningún padrón incluido en archivos públicos.

La variable PRAAT_PUBLIC_ORIGIN permite fijar una dirección propia HTTPS si se usa otro proveedor. Se requiere un proxy que preserve Host y establezca X-Forwarded-Proto=https. En Render, RENDER_EXTERNAL_URL define la dirección de acceso por defecto. La comprobación /healthz no expone datos.

Las pruebas automáticas comprueban los controles de aplicación con datos ficticios. La imagen Docker no se construyó en esta computadora porque Docker no está instalado; el proveedor deberá construirla y se validará el servicio publicado antes de entregar accesos reales.

