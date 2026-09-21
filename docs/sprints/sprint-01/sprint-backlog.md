## 1. Registro de Usuario - Admin.
2
 
3
- Features: Crear formulario donde se defina su tipo de rol (Usuario - Admin).
4
 
5
- Tareas:
6
 
7
### 1. Frontend (UI / Interfas de Usuario)
8
 
9
- A. Diseño e implementación de la vista HTML/CSS: Crear la estructura del formulario de registro con campos (Nombre, Correo, Contraseña, Confirmar contraseña, Selección de Rol).
10
 
11
- B. Lógica de validación en cliente (JS):
12
 
13
- Validar campos obligatorios y formato de correo electrónico.
14
 
15
- Validar longitud mínima y coincidencia de contraseña.
16
 
17
- Capturar el valor seleccionado del rol (USER / ADMIN).
18
 
19
- C. Integración con API: Consumir el endpoint de registro mediante fetch o axios enviando el payload JSON.
20
 
21
- D. Manejo de estados de interfaz:
22
 
23
- Deshabilitar el botón de envío mientras se procesa la solicitud (estado loading).
24
 
25
- Mostrar notificaciones de éxito o mensajes de error según la respuesta del backend.
26
 
27
### 2. Backend (Lógica de Negocio y Seguridad)
28
 
29
- A. Creación del DTO / Modelo de entrada: Definir la estructura del objeto de transferencia de datos con las validaciones básicas (Campos @NotNull, @Email, @NotBlank, etc.).
30
 
31
- B. Definición de Enum/Entidad de Roles: Crear/verificar el enumerado de roles (USER, ADMIN) en la arquitectura del servidor.
32
 
33
- C. Implementación del Endpoint / Controlador: Crear la ruta POST /api/users/register.
34
 
35
- D. Lógica de Servicio y Encriptación:
36
 
37
- Encriptar la contraseña del nuevo usuario antes de guardarla (usando Bcrypt/Argon2).
38
 
39
- Asignar el rol enviado y guardar la entidad en la base de datos.
40
 
41
- E. Seguridad del Endpoint: Restringir el acceso a la ruta para que únicamente usuarios con el rol ADMIN (mediante token JWT o sesión activa) puedan crear cuentas con priviliegios.
42
 
43
### 3. Base de Datos
44
 
45
- Verificación/Ajuste de Tablas: Asegurar que las tablas de usuarios y roles (o la columna role) soporten correctamente los valores permitidos y sus relaciones.
46
 
47
### 4. Calidad y Pruebas (QA / Testing)
48
 
49
- A. Pruebas unitarias/integración backend:
50
 
51
- Test de registro exitoso con rol USER y ADMIN.
52
 
53
- Test de intento de registro con correo duplicado o campos inválidos.
54
 
55
- Test de autorización (verificar que un usuario no autenticado o con rol USER no pueda llamar al endpoint).
56
 
57
- B. Pruebas de interfaz (Frontend): Probar el flujo completo en pantalla y verificar la correcta visualización de mensajes de éxito/error.