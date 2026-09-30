# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting. Herramienta de IA usada: (escribe aqui cual usaste)

##	Ejercicio	2:	Zero-shot, one-shot y few-shot

| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Sí/No) |
|---|---|---|---|
| **Zero-shot** |si |si |si |
| **One-shot** |si |si |no |
| **Few-shot** |si |si |no |


##	Ejercicio	3:	Chain of Thought

| Pedido | Respuesta de la IA | Muestra los pasos (Sí/No) | Correcta (Sí/No) |
|---|---|---|---|
| **Directo** |si |si |no |
| **Paso a paso** |si |si |si |

##	Ejercicio	4:	Role prompting

| Versión | Vocabulario (sencillo/técnico) | Usa ejemplos o código | A quién le sirve más |
|---|---|---|---|
| **A. Sin rol** |NO |NO |N.A|
| **B. Rol docente** |SI |NO |Docente |
| **C. Rol senior** |SI |NO |SENIOR |

##	Ejercicio	5:	Descomposicion

### Registro de Resultados: Pedido por Pasos vs. Pedido Único

* **Paso 1** la IA entregó una lista de 5 requisitos (gestión de productos, control de stock, alertas de stock mínimo, búsqueda y reportes, persistencia y usuarios) más una sugerencia de arquitectura por capas.
* **Paso 2** la IA entregó el diseño de 8 clases (Categoria, Proveedor, Producto, MovimientoStock, Usuario, Venta, DetalleVenta, AlertaStock) y 2 enumeraciones, con atributos y tipos de dato, además de las relaciones entre ellas.
* **Paso 3** la IA entregó el archivo Producto.java con atributos, constructor, getters y setters, validaciones y dos métodos de negocio (estaBajoMinimo() y calcularValorStock()).
* **Paso 4** la IA entregó 3 mejoras concretas sobre su propio código: métodos aumentarStock/reducirStock en lugar del setter, equals/hashCode sobre un campo mutable y un Builder para reemplazar el constructor de 11 parámetros.
**Comparación con el pedido de una sola vez:**
> al dividir la tarea en 4 pedidos, cada respuesta quedó alineada con los requisitos del paso anterior y pude corregir el rumbo entre pasos. En un único pedido ("diseña un inventario en Java con requisitos, clases y código") lo probable es obtener una respuesta más genérica y menos trazable, con código menos depurado y sin una revisión crítica.

##	Ejercicio	6:	Prompt estructurado y autocritica

###  Evaluar

| Qué revisar | Cumple (Sí / No) |
|-------------|------------------|
| ¿Tiene las 4 columnas pedidas? | Sí |
| ¿Incluye el bloqueo después de 3 intentos? | Sí |
| ¿Incluye casos con campos vacíos? | Sí |
| ¿Indica qué casos agregó en la autocrítica? | Sí |
| ¿Hay algún caso repetido o que no tenga sentido? | Sí (ver observación) |


### Guardar el prompt estructurado

```text
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>

--- Mensaje de autocritica ---
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @
o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```


- [Bitacora de tecnicas avanzadas](prompts/BITACORA.md)
