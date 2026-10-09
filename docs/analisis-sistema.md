# Análisis del sistema

## Actores
- Administrador: gestiona usuarios, estudiantes, docentes y cursos.
- Docente: registra notas y asistencia de sus cursos.
- Estudiante: consulta sus cursos, notas y asistencia.

## Casos de uso principales
- CU-01 Iniciar sesión (todos)
- CU-02 Gestionar estudiantes: crear, editar, buscar, eliminar (Administrador)
- CU-03 Gestionar cursos (Administrador)
- CU-04 Matricular estudiante en curso (Administrador)
- CU-05 Registrar calificaciones (Docente)
- CU-06 Registrar asistencia (Docente)
- CU-07 Consultar calificaciones (Estudiante)
- CU-08 Generar reporte de notas (Administrador, Docente)

## Descripción de funcionalidades
- Gestión de estudiantes: registro con documento, nombre, correo y programa; no se permiten documentos duplicados.
- Gestión de cursos: cada curso tiene código, nombre, créditos y un docente asignado.
- Matrículas: un estudiante puede estar en varios cursos.
- Calificaciones: notas de 0.0 a 5.0 y cálculo del promedio por curso.
- Asistencia: registro por fecha (presente / ausente).
- Reportes: notas y promedio de un estudiante.

## Requerimientos funcionales
- RF-01 El sistema debe permitir iniciar sesión con usuario y contraseña.
- RF-02 El sistema debe permitir registrar, editar, buscar y eliminar estudiantes.
- RF-03 El sistema debe permitir crear cursos y asignarles un docente.
- RF-04 El sistema debe permitir matricular estudiantes en cursos.
- RF-05 El sistema debe permitir al docente registrar notas entre 0.0 y 5.0.
- RF-06 El sistema debe calcular el promedio de cada estudiante por curso.
- RF-07 El sistema debe permitir registrar asistencia por fecha.
- RF-08 El sistema debe permitir al estudiante consultar sus notas.

## Requerimientos no funcionales
- RNF-01 Usabilidad: interfaz sencilla en español.
- RNF-02 Seguridad: las contraseñas se guardan cifradas y cada rol solo ve lo que le corresponde.
- RNF-03 Rendimiento: las consultas responden en menos de 2 segundos.
- RNF-04 Mantenibilidad: código organizado por capas y versionado en Git.
- RNF-05 Portabilidad: funciona en Windows, Linux y macOS.

## Arquitectura del sistema
Arquitectura en 3 capas:
- Presentación: interfaz con la que interactúa el usuario.
- Lógica de negocio: reglas del sistema (validaciones, cálculo de promedios).
- Datos: almacenamiento en una base de datos SQLite.

Tecnologías propuestas: Python 3 y SQLite.