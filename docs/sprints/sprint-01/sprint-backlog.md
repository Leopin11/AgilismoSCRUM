1. Registro de Usuario - Admin.

Features: Crear formulario donde se defina su tipo de rol (Usuario - Admin).

Tareas:

1. Frontend (UI / Interfas de Usuario): 

A. Diseño e implementación de la vista HTML/CSS: Crear la estructura del formulario de registro con campos (Nombre, Correo, Contraseña, Confirmar contraseña, Selección de Rol).

B. Lógica de validación en cliente (JS):

    * Validar campos obligatorios y formato de correo electrónico.

    * Validar longitud mínima y coincidencia de contraseña.

    * Capturar el valor seleccionado del rol (USER / ADMIN).

C. Integración con API: Consumir el endpoint de registro mediante fetch o axios enviando el payload JSON.

C. Manejo de estados de interfaz:

    * Deshabilitar el botón de envío mientras se procesa la solicitud (estado loading).

    * Mostrar notificaciones de éxito o mensajes de error según la respuesta del backend.

2. Backend (Lógica de Negocio y Seguridad)

A. Creación del DTO / Modelo de entrada: Definir la estructura del objeto de transferencia de datos con las validaciones básicas (Campos @NotNull, @Email, @NotBlank, etc.).

B. Definición de Enum/Entidad de Roles: Crear/verificar el enumerado de roles (USER, ADMIN) en la arquitectura del servidor.

C. Implementación del Endpoint / Controlador: Crear la ruta POST /api/users/register.

D. Lógica de Servicio y Encriptación:

    * Encriptar la contraseña del nuevo usuario antes de guardarla (usando Bcrypt/Argon2).

    * Asignar el rol enviado y guardar la entidad en la base de datos.

E. Seguridad del Endpoint: Restringir el acceso a la ruta para que únicamente usuarios con el rol ADMIN (mediante token JWT o sesión activa) puedan crear cuentas con priviliegios.

3. Base de Datos
 Verificación/Ajuste de Tablas: Asegurar que las tablas de usuarios y roles (o la columna role) soporten correctamente los valores permitidos y sus relaciones.

4. Calidad y Pruebas (QA / Testing)

A. Pruebas unitarias/integración backend:

    * Test de registro exitoso con rol USER y ADMIN.

    * Test de intento de registro con correo duplicado o campos inválidos.

    * Test de autorización (verificar que un usuario no autenticado o con rol USER no pueda llamar al endpoint).

B. Pruebas de interfaz (Frontend): Probar el flujo completo en pantalla y verificar la correcta visualización de mensajes de éxito/error.