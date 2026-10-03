# SPRINT REVIEW
## Proyecto: MapPal
## Sprint 1 - Fundación de la Plataforma
 
---
 
# Objetivo del Sprint
 
Construir la base funcional de la plataforma MapPal mediante la implementación de usuarios, perfiles, reputación inicial y canales comunitarios.
 
---
 
# Resumen Ejecutivo
 
Durante este Sprint se implementaron los componentes fundamentales necesarios para iniciar la interacción entre usuarios y la plataforma.
 
Se logró establecer la estructura base sobre la cual se desarrollarán los módulos de inteligencia territorial, alertas comunitarias, accesibilidad, reservas y pagos.
 
---
 
# Funcionalidades Completadas
 
## Gestión de Usuarios
 
### Completado
 
- Registro de usuarios.
- Validación de identificador único.
- Registro de datos personales.
- Configuración de residencia activa.
- Configuración de idioma preferido.
 
### Resultado
 
Los usuarios pueden crear una cuenta y almacenar su información personal correctamente.
 
---
 
## Gestión de Perfil
 
### Completado
 
- Visualización de perfil.
- Actualización de datos personales.
- Persistencia de cambios.
 
### Resultado
 
Los usuarios pueden administrar su información desde el perfil personal.
 
---
 
## Sistema de Reputación
 
### Completado
 
- Creación del atributo Karma.
- Inicialización automática del Karma.
- Visualización del nivel de confianza.
 
### Resultado
 
Todos los usuarios registrados cuentan con un indicador base de reputación.
 
---
 
## Canales Comunitarios
 
### Completado
 
- Creación de entidades Canal, Ciudad y Barrio.
- Asociación de canales por destino.
- Consulta de canales disponibles.
 
### Resultado
 
La plataforma permite explorar espacios de conversación organizados geográficamente.
 
---
 
## Publicaciones Comunitarias
 
### Completado
 
- Creación de publicaciones.
- Asociación a un canal.
- Registro de ubicación GPS.
- Carga de imágenes.
 
### Resultado
 
Los usuarios pueden compartir información relacionada con cada destino.
 
---
 
# Evidencia Funcional
 
### Flujo de Usuario Validado
 
1. Registro en la plataforma.
2. Configuración de perfil.
3. Selección de idioma.
4. Selección de residencia activa.
5. Acceso a canales comunitarios.
6. Creación de publicación.
7. Visualización de contenido publicado.
 
---
 
# Resultados de Pruebas
 
## Backend
 
✅ Registro exitoso de usuarios.
 
✅ Persistencia de perfiles.
 
✅ Consulta de canales.
 
✅ Creación de publicaciones.
 
✅ Asociación correcta entre entidades.
 
---
 
## Frontend
 
✅ Formularios funcionales.
 
✅ Validaciones visuales.
 
✅ Navegación entre módulos.
 
✅ Consumo correcto de API REST.
 
✅ Mensajes de éxito y error.
 
---
 
# Aspectos Pendientes
 
Las siguientes funcionalidades fueron identificadas para próximos Sprints:
 
- Sistema de alertas comunitarias.
- Sistema de accesibilidad universal.
- Registro de prestadores locales.
- Sistema de insignias.
- Motor de reservas.
- Procesamiento de pagos.
- Exploración avanzada de destinos.
 
---
 
# Retroalimentación Obtenida
 
## Aspectos Positivos
 
- La estructura del sistema es escalable.
- La experiencia de registro es sencilla.
- La navegación entre canales es intuitiva.
 
## Oportunidades de Mejora
 
- Incorporar filtros de búsqueda.
- Mejorar el sistema de reputación.
- Implementar notificaciones en tiempo real.
 
---
 
# Estado del Sprint
 
✅ Sprint completado exitosamente.
 
✅ Objetivo alcanzado.
 
✅ Incremento potencialmente desplegable.
 
---
 
# Próximo Sprint
 
## Objetivo
 
Implementar el sistema de inteligencia territorial y alertas comunitarias mediante:
 
- Gestión de alertas georreferenciadas.
- Validación comunitaria.
- Mapas interactivos.
- Protocolos de seguridad.
- Primeras métricas de confiabilidad.
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
