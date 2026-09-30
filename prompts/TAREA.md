# Tarea: Mi prompt avanzado

## Tarea elegida
Diseñar las clases y el código en Java para un **Sistema de Registro de Notas de Estudiantes**.


## Version 1: prompt basico

```text
Crea un sistema de notas en Java con sus clases y código.
```

## Version 2

```text
Actúa como un Docente Universitario de Programación en Java. 
Diseña un sistema de notas de estudiantes. Explica primero tu razonamiento paso a paso sobre qué clases se necesitan y luego genera la clase Alumno con sus atributos (nombre, nota1, nota2), constructor, getters/setters y un método para calcular el promedio.
```
## Version 3 prompt final

```text
Actúa como un Docente Universitario de Programación en Java especialista en Orientación a Objetos.

Tu tarea es diseñar la clase Alumno para un sistema de notas escolar.

Sigue este proceso de pensamiento paso a paso:
1. Analiza los atributos mínimos necesarios para representar a un alumno y sus calificaciones.
2. Identifica las validaciones requeridas (ej. las notas deben estar entre 0 y 20).
3. Diseña el método para calcular el promedio final y determinar si aprueba (nota >= 13).

Aquí tienes un ejemplo de cómo debes estructurar los métodos de validación:
Ejemplo:
Input: setNota1(25)
Output: Error, la nota debe estar entre 0 y 20.

Genera la respuesta con la siguiente estructura:
- ### Análisis y Diseño
- ### Código Java de la clase Alumno
- ### Autocrítica del código generado (señala 2 posibles puntos de mejora)
```

## Tecnicas usadas en el prompt final

| Parte del Prompt Final | Técnica usada |
|---|---|
| `Actúa como un Docente Universitario...` | Role Prompting (Rol) |
| `Sigue este proceso de pensamiento paso a paso...` | Chain of Thought (Paso a paso) |
| `Ejemplo: Input: setNota1(25) -> Output: Error...` | Few-Shot (Dar un ejemplo) |
| `Genera la respuesta con la siguiente estructura...` | Prompt Estructurado (Formato) |
| `- ### Autocrítica del código generado...` | Autocrítica |

---

## Evaluacion del resultado

| Criterio de Evaluación | Cumplido (Sí / No) |
|---|---|
| ¿El rol ayudó a que la respuesta sea más clara? | **Sí** |
| ¿El código valida que las notas sean entre 0 y 20? | **Sí** |
| ¿La IA respetó el formato de respuesta solicitado? | **Sí** |
| ¿La autocrítica mostró cosas por mejorar en el código? | **Sí** |

---

## Por que elegi estas tecnicas

Elegí estas técnicas porque me ayudan a recibir una mejor respuesta de la IA sin que se olvide de las validaciones importantes. El rol de docente hace que me explique fácil, el paso a paso evita que se salte detalles como el rango de notas (0 a 20), el ejemplo le enseña cómo quiero la respuesta y la autocrítica me ayuda a ver qué fallas tiene el código.


- [Tarea: mi prompt avanzado](prompts/TAREA.md)