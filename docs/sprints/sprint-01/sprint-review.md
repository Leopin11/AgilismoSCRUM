# Sprint Review - Registro de Usuario Admin
2
 
3
## Objetivo del Sprint
4
Implementar la funcionalidad de registro de usuarios con asignación de roles (USER y ADMIN) controlada por permisos de administrador.
5
 
6
## Funcionalidades Completadas
7
 
8
### Frontend
9
 
10
- Se desarrolló el formulario de registro con los campos:
11
- Nombre
12
- Correo electrónico
13
- Contraseña
14
- Confirmar contraseña
15
- Rol (USER / ADMIN)
16
 
17
- Se implementaron validaciones en cliente:
18
- Campos obligatorios.
19
- Formato de correo electrónico.
20
- Longitud mínima de contraseña.
21
- Confirmación de contraseña.
22
 
23
- Se integró el formulario con el endpoint de registro mediante consumo de API REST.
24
 
25
- Se implementó manejo de estados:
26
- Botón deshabilitado durante el envío.
27
- Mensajes de éxito.
28
- Mensajes de error.
29
 
30
### Backend
31
 
32
- Se creó el DTO de registro con validaciones.
33
- Se implementó el enum de roles USER y ADMIN.
34
- Se desarrolló el endpoint:
35
 
36
```http
37
POST /api/users/register