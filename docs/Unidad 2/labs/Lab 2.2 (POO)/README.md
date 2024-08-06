# Unidad 2 – Capítulo 2: Laboratorio POO

## 1. Clases y Herencia

### Objetivo
Escribir una aplicación que utilice clases y herencia. Crear una librería de clases.

### Pasos

1. **Crear Proyecto:**
     - En Visual Studio, crear una nueva aplicación de consola llamada `LabClases1`.
     - Agregar un nuevo proyecto a la solución llamado `Clases`, de tipo `Class Library`.

2. **Configurar Clase A:**
     - Renombrar el archivo `class1.cs` a `A.cs` y cambiar el nombre de la clase dentro del archivo.
     - Agregar `using System.Console;` para acceso rápido a elementos de la consola.
     - **Clase A debe tener:**
       - Property `NombreInstancia`.
       - **Dos constructores:**
         - Uno por defecto que asigne `NombreInstancia` como “Instancia sin nombre”.
         - Otro que permita pasar el nombre por parámetro.
       - Método `MostrarNombre` que devuelva el nombre de la instancia por consola.
       - Métodos `M1`, `M2` y `M3` que muestren un mensaje por consola al ser invocados.

3. **Configurar Clase B:**
     - Agregar un nuevo archivo `B.cs` para implementar la clase `B`, heredera de `A`.
     - **Clase B debe tener:**
       - Método `M4` que muestre el mensaje “Metodo del hijo Invocado”.
       - Constructor que pase por defecto "Instancia de B" al constructor de `A`.

4. **Compilar Clase:**
     - Compilar la clase y observar que se genera un assembly propio llamado `Clases`.

5. **Referenciar Clase en Proyecto Principal:**
     - En `Solution Explorer`, agregar una nueva referencia al proyecto `LabClases1`.
     - Desde el cuadro de diálogo, agregar referencia a `Clases`.

6. **Utilizar Clases en Program.cs:**
     - Definir `using Clases;`.
     - Crear instancias de `A` y `B`.
     - Llamar a todos los métodos de `A` y `B`.
     - Observar métodos disponibles y su comportamiento.

7. **Compilar y Ejecutar:**
     - Compilar y ejecutar la aplicación.
     - Cambiar accesibilidad de los miembros a `protected` y `private`, observar errores y analizarlos.

## 2. Métodos Virtuales y Ocultamiento

### Objetivo
Comprender el uso de modificadores `virtual`, `new` y `override`.

### Pasos

1. **Crear Proyecto:**
     - Crear una nueva aplicación de consola llamada `LabClases2`.
     - Agregar un proyecto `Clases` de tipo `Class Library`. Renombrar el archivo a `Clases.cs`.

2. **Implementar Código:**
     - Copiar el siguiente código:

       ```csharp
       namespace Clases 
       { 
           public class A 
           { 
               public void F() { Console.WriteLine("A.F"); } 
               public virtual void G() { Console.WriteLine("A.G"); } 
           } 
           public class B : A 
           { 
               new public void F() { Console.WriteLine("B.F"); } 
               public override void G() { Console.WriteLine("B.G"); } 
           } 
       }
       ```

3. **Compilar Librería:**
     - Compilar la librería y observar que no hay errores ni warnings.

4. **Referenciar Librería:**
     - Referenciar `Clases` en el proyecto principal de la solución.
     - Copiar el siguiente código dentro del `Main`:

       ```csharp
       B b = new B();
       A a = b;
       a.F();
       b.F();
       a.G();
       b.G();
       Console.ReadKey();
       ```

5. **Compilar y Ejecutar:**
     - Compilar y ejecutar el código. Analizar la salida por pantalla.

6. **Modificar Código:**
     - Eliminar el modificador `new` del método `F` en la clase `B`. Compilar y observar el warning.
     - Quitar el operador `override` de `B.G()`. Observar el warning y la salida al ejecutar la aplicación.

## 3. Visor de Clases y Diseñador de Clases

### Objetivo
Utilizar el diseñador de clases para crear una jerarquía de clases y visualizar componentes principales.

### Pasos

1. **Crear Proyecto:**
     - Crear un proyecto tipo `Class Library` llamado `Geometria` y la solución con el mismo nombre.
     - Renombrar la clase `Class1` a `Circulo`.

2. **Agregar Diagrama de Clases:**
     - Agregar un nuevo ítem del tipo `Class Diagram` llamado `DiagramaClases`.
     - Activar y visualizar `Class View` y `Tool Box`.

3. **Diseñar Clase:**
     - Arrastrar la clase `Circulo` al `Class Designer`.
     - Agregar campo `m_radio`, propiedad `Radio`, métodos `CalcularPerimetro` y `CalcularSuperficie` desde el menú de contexto.

4. **Implementar Clase Triangulo:**
     - Agregar código para implementar la propiedad `Radio` y métodos agregados en `Triangulo`.

5. **Desarrollar Jerarquía:**
     - Continuar desarrollando otras clases (`Triangulo`, `Poligono`, `Rectangulo`, `Cuadrado`) siguiendo los pasos anteriores.
     - Implementar miembros (campos, métodos y propiedades) de cada clase agregada.

## 4. Clase Persona

### Objetivo
Familiarizarse con el uso del diseñador de clases y reforzar conceptos de POO.

### Recomendaciones

1. **Declarar Clase Persona:**
     - Contener información: `Nombre`, `Apellido`, `Edad`, `DNI`.
     - Implementar:
       - Constructor que reciba información y proporcione un mensaje de creación.
       - Destructor que proporcione un mensaje de destrucción.
       - Propiedades para acceder a los atributos de la clase.
       - Método `GetFullName` que devuelva la concatenación de nombre y apellido.
       - Método `GetAge` para calcular la edad.

## 5. Adivine el Número

### Objetivo
Familiarizarse con el uso del diseñador de clases y reforzar conceptos de POO.

### Recomendaciones

1. **Crear Clases:**
     - Crear clases `Juego` y `Jugada` en archivos separados.
     - `Juego` debe tener método público `ComenzarJuego()`.
     - `Jugada` debe generar un número a adivinar en el constructor:

       ```csharp
       public Jugada(int maxNumero) 
       { 
           Random rnd = new Random(); 
           Numero = rnd.Next(maxNumero); 
       }
       ```

2. **Controlar Intentos:**
     - Atributo privado para cantidad de intentos, accesible por `Juego` a través de una propiedad.
     - Propiedad para saber si el número fue acertado.

3. **Manejo de Errores:**
     - Capturar errores y mostrar mensajes explicativos.

## 6. Adivine el Número con Ayuda

### Objetivo
Familiarizarse con el uso del diseñador de clases y reforzar conceptos de POO.

### Recomendaciones

1. **Implementar Nueva Clase:**
     - Crear clase `JugadaConAyuda`, heredera de `Jugada`.
     - Método `Comparar` debe brindar ayuda en función de un rango de distancia del número esperado.
     - Modificar la clase `Juego` solo para instanciar `JugadaConAyuda`.