# Unidad 2 – Capítulo 3: Laboratorio 1

## 1. LINQ to Objects

### Objetivo
Familiarizarse con el uso de LINQ to Objects.

### Pasos

1. **Obtener Provincias por Inicial:**
     - **Crear Array de Provincias:**
       - Definir un array que incluya todas las provincias de Argentina.
     - **Filtrar con LINQ:**
       - Usar LINQ para obtener y mostrar por consola aquellas provincias que empiezan con la letra “S” o “T”.

2. **Filtrar Números Mayores a 20:**
     - **Crear Programa para Lista de Números:**
       - Aceptar una lista de números ingresados por el usuario.
       - Almacenar los números en un objeto de tipo `List<int>`.
     - **Filtrar con LINQ:**
       - Usar LINQ para mostrar por consola aquellos números que son mayores a 20.

3. **Obtener Código Postal de Ciudades:**
     - **Crear ArrayList de Ciudades:**
       - Definir un `ArrayList` que incluya al menos 10 ciudades de Argentina con nombre y código postal.
     - **Filtrar con LINQ:**
       - Usar LINQ para obtener y mostrar por consola el código postal de aquellas ciudades que incluyan dentro de su nombre una expresión de búsqueda de tres caracteres, sin respetar mayúsculas o minúsculas.
       - Ejemplo: Si se ingresa “ros” y el `ArrayList` incluye Rosario, mostrar el código postal de Rosario.

4. **Ordenar Lista de Empleados:**
     - **Definir Clase Empleado:**
       - Crear una clase `Empleado` con propiedades `Id` (int), `Nombre` (string), y `Sueldo` (decimal).
     - **Crear Programa para Lista de Empleados:**
       - Aceptar la entrada de empleados para darlos de alta en una `List<Empleado>`.
     - **Ordenar con LINQ:**
       - Usar LINQ para mostrar por consola la lista de empleados ordenada por la propiedad `Sueldo` de manera ascendente.
       - Usar LINQ para mostrar por consola la lista de empleados ordenada por la propiedad `Sueldo` de manera descendente.