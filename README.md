# Gestión de Sistemas de Base de Datos para Actividades Específicas

Este repositorio contiene el código en Python, utilizando SQLAlchemy, para modelar sistemas de bases de datos destinados a gestionar diversas actividades. Cada sección cumple con los requisitos específicos y abarca todas las entidades, atributos y relaciones necesarios. 

## Requisitos de la Actividad

1. **Preparación de recetas de cocina**
2. **Gestión de partidos de una liga de fútbol en una temporada**
3. **Reserva de habitaciones en un hotel**
4. **Matrícula de estudiantes en una institución educativa**
5. **Simulación del funcionamiento de una red social**

---

## Descripción de los Sistemas Modelados

### 1. Preparación de Recetas de Cocina

Este sistema permite gestionar recetas de cocina, incluyendo ingredientes y pasos de preparación.

- **Entidades**: 
  - `Receta`: nombre, tiempo de preparación, dificultad, instrucciones.
  - `Ingrediente`: nombre, cantidad, unidad.
  - `Paso`: descripción, orden.
- **Relaciones**:
  - Una receta puede tener múltiples ingredientes y pasos.
  
### 2. Liga de Fútbol - Partidos de una Temporada

Este sistema almacena y gestiona información sobre los equipos, partidos, estadios y temporadas.

- **Entidades**:
  - `Equipo`: nombre, ciudad.
  - `Temporada`: año.
  - `Estadio`: nombre, capacidad, ciudad.
  - `Partido`: fecha, equipo local y visitante, estadio, temporada, marcador.
- **Relaciones**:
  - Un partido tiene un equipo local, un equipo visitante, y pertenece a una temporada y estadio específicos.

### 3. Reserva de Habitación en un Hotel

Este modelo permite gestionar reservas de hotel y la información de clientes y habitaciones.

- **Entidades**:
  - `Cliente`: nombre, apellido, teléfono, email.
  - `Habitacion`: número, tipo, capacidad, precio por noche.
  - `Reserva`: cliente, habitación, fecha de entrada y salida, estado.
- **Relaciones**:
  - Cada reserva está asociada a un cliente y una habitación.

### 4. Matrícula de Estudiantes

Este sistema facilita la gestión de la matrícula de estudiantes, profesores, materias y grados académicos.

- **Entidades**:
  - `Estudiante`: nombre, apellido, grado.
  - `Profesor`: nombre, apellido, teléfono, email.
  - `Materia`: nombre, profesor.
  - `Grado`: nivel, sección.
- **Relaciones**:
  - Cada materia es impartida por un profesor y pertenece a un grado.
  - Los estudiantes están inscritos en grados específicos.

### 5. Simulación de Red Social

Este modelo representa una red social básica donde los usuarios pueden agregar contactos, organizarlos en grupos y bloquear usuarios.

- **Entidades**:
  - `Usuario`: nombre, apellido, dirección, teléfono, email, contraseña, foto, es celebridad.
  - `Contacto`: usuario, contacto, comentario.
  - `Grupo`: nombre, usuario.
  - `Bloqueo`: usuario, bloqueado.
- **Relaciones**:
  - Un usuario puede tener múltiples contactos, los cuales pueden organizarse en grupos y bloquear a otros usuarios.

---

## Requisitos para Ejecución

1. **Python** 3.8 o superior.
2. **SQLAlchemy** para modelar la base de datos:
   ```bash
   pip install sqlalchemy
