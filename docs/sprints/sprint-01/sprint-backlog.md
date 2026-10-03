# SPRINT BACKLOG
## Proyecto: MapPal
## Sprint 1 - Fundación de la Plataforma
### Duración: 2 semanas
 
---
 
# Objetivo del Sprint
 
Construir la base funcional de la plataforma MapPal mediante la implementación del sistema de usuarios, perfiles, reputación comunitaria y canales de interacción iniciales.
 
---
 
# Incremento Esperado
 
Al finalizar el Sprint, un usuario podrá:
 
- Registrarse en la plataforma.
- Configurar su perfil.
- Establecer idioma y residencia activa.
- Visualizar su reputación inicial (Karma).
- Acceder a canales comunitarios.
- Crear publicaciones dentro de una ciudad o barrio.
 
---
 
# Backlog del Sprint
 
## 1. Gestión de Usuarios Globales
 
### Feature: Registro de Usuario
 
#### Tareas Backend
 
- Crear entidad Persona.
- Crear repositorio PersonaRepository.
- Crear servicio PersonService.
- Crear DTO de registro.
- Crear endpoint POST /register.
- Validar identificador único.
- Calcular edad automáticamente.
 
#### Tareas Frontend
 
- Diseñar formulario de registro.
- Implementar validaciones de formulario.
- Consumir API de registro.
- Mostrar mensajes de éxito y error.
 
#### Criterios de Aceptación
 
- El usuario puede registrarse correctamente.
- El identificador es único.
- La edad se calcula automáticamente.
 
---
 
## 2. Gestión de Perfil
 
### Feature: Perfil de Usuario
 
#### Tareas Backend
 
- Crear entidad Perfil.
- Crear servicio de actualización de perfil.
- Crear endpoint PUT /profile.
 
#### Tareas Frontend
 
- Diseñar página de perfil.
- Mostrar información de usuario.
- Permitir actualización de datos.
 
#### Criterios de Aceptación
 
- El usuario puede visualizar su perfil.
- El usuario puede editar su información.
 
---
 
## 3. Configuración Regional
 
### Feature: Residencia Activa e Idioma
 
#### Tareas Backend
 
- Crear catálogo de idiomas.
- Registrar residencia activa.
- Persistir configuración regional.
 
#### Tareas Frontend
 
- Selector de idioma.
- Selector de residencia activa.
 
#### Criterios de Aceptación
 
- El usuario puede cambiar idioma.
- El usuario puede establecer ciudad de residencia.
 
---
 
## 4. Sistema de Reputación
 
### Feature: Karma Inicial
 
#### Tareas Backend
 
- Crear atributo karma.
- Inicializar karma al registrarse.
- Crear lógica de actualización futura.
 
#### Tareas Frontend
 
- Mostrar karma en perfil.
- Mostrar nivel de confianza.
 
#### Criterios de Aceptación
 
- Todo usuario inicia con karma.
- El karma es visible desde el perfil.
 
---
 
## 5. Canales Comunitarios
 
### Feature: Gestión de Canales
 
#### Tareas Backend
 
- Crear entidad Canal.
- Crear entidad Ciudad.
- Crear entidad Barrio.
- Implementar consultas por destino.
 
#### Tareas Frontend
 
- Crear listado de canales.
- Crear pantalla de exploración.
 
#### Criterios de Aceptación
 
- El usuario puede consultar canales.
- Los canales se organizan por destino.
 
---
 
## 6. Publicaciones Comunitarias
 
### Feature: Publicaciones
 
#### Tareas Backend
 
- Crear entidad Publicacion.
- Crear endpoint de creación.
- Registrar ubicación GPS.
 
#### Tareas Frontend
 
- Crear formulario de publicación.
- Adjuntar imágenes.
- Mostrar publicaciones.
 
#### Criterios de Aceptación
 
- El usuario puede publicar contenido.
- La publicación queda asociada al canal.
 
---
 
# Definición de Terminado (DoD)
 
- Código implementado.
- Compilación exitosa.
- Pruebas unitarias aprobadas.
- API documentada.
- Frontend integrado con Backend.
- Validaciones funcionando.
- Revisión por el equipo realizada.
 
---
 
# Entregables
 
- Módulo de usuarios.
- Gestión de perfiles.
- Configuración regional.
- Sistema inicial de reputación.
- Canales comunitarios.
- Publicaciones básicas.