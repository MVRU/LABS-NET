# Unidad 1: Plataforma y Entorno de Desarrollo

## Capítulo 1: Plataforma

### Plataforma .NET

#### Introducción
La plataforma .NET es un conjunto de tecnologías diseñadas por Microsoft para el desarrollo y ejecución de software, independientemente del lenguaje de programación, modelo de objetos, sistema operativo, infraestructura de hardware y dispositivos. Está compuesta por un entorno de trabajo denominado .NET Framework, un conjunto de lenguajes .NET y herramientas de programación que permiten el desarrollo de aplicaciones robustas, seguras y de alto rendimiento para diversos entornos.

#### Cuerpo
##### 1. Plataforma de Desarrollo .NET y su Funcionamiento
- **Problemas que resuelve:**
  - Independencia del hardware, lenguaje de programación y dispositivos.
- **Beneficios:**
  - Modelo de programación coherente e independiente del lenguaje.
  - Interoperabilidad entre tecnologías.
  - Fácil migración desde tecnologías existentes.
  - Soporte completo de tecnologías de Internet independientes de la plataforma (HTTP, XML, SOAP).

##### 2. Entorno de Trabajo .NET Framework y su Funcionamiento
- **Componentes:**
  - Common Language Runtime (CLR)
  - Base Class Library (BCL)
- **Evolución de versiones:**
  - .NET Framework 1.0 a 4.8
  - .NET Core y .NET 5.0

##### 3. Motor de Ejecución CLR (Common Language Runtime) y su Funcionamiento
- **Componentes y servicios en tiempo de ejecución:**
  - Recolección de basura (garbage collector)
  - Otros servicios

##### 4. Arquitectura de Compilación y Ejecución
- Proceso de compilación Just-In-Time (JIT)

##### 5. Sistema de Tipos Comunes CTS (Common Type System)
- **Categorías:**
  - Tipos por Valor
  - Tipos por Referencia

##### 6. Biblioteca de Clases Base BCL (Base Class Library)
- Organización y evolución de la BCL

##### 7. Espacio de Nombres (Namespaces)
- Organización y uso en el desarrollo

##### 8. Código Administrado o Interpretado
- Código en Lenguaje Intermedio CIL o MSIL

##### 9. Ensamblados, Manifiestos y Metadatos
- Definición y uso en .NET

##### 10. Especificación Común de Lenguajes CLS (Common Language Specification)
- Reglas y estándares para lenguajes compatibles

##### 11. Infraestructura Común del Lenguaje CLI (Common Language Infrastructure)
- Estandarización y licenciamiento (Norma ECMA-335 ISO/IEC 23271)

##### 12. Soporte a Múltiples Lenguajes
- Compatibilidad con diversos lenguajes de programación

#### Plataforma de Desarrollo .NET
##### Características Principales
- **Entorno de trabajo:** .NET Framework y .NET Core
- **Lenguajes y herramientas de desarrollo:** soporte para múltiples lenguajes y herramientas dentro del entorno de Visual Studio .NET

#### Entorno de Trabajo .NET Framework y .NET Core
- **Definición de Framework:** Estructura conceptual y tecnológica de soporte para proyectos de software.
- **Evolución:**
  - Primera versión estable de .NET Framework en 2002
  - .NET Core en 2014, evolucionando a .NET 5.0 en 2020

##### Evolución de Versiones de .NET Framework
- **Versiones y características:**
  - **4.8:** Visual Studio 2019, mejoras en seguridad y rendimiento.
  - **4.7:** Visual Studio 2017, mejoras en criptografía y soporte para DPI alto.
  - **4.6:** Visual Studio 2015, nuevo compilador JIT para 64 bits.
  - **4.5.2 y anteriores:** mejoras en rendimiento, compatibilidad y nuevas API.

#### Componentes Principales
##### Common Language Runtime (CLR)
- Motor de ejecución que gestiona la ejecución de aplicaciones .NET.

##### Base Class Library (BCL)
- Librería de clases que proporciona funcionalidades básicas y avanzadas para el desarrollo de aplicaciones.

#### .NET Core
- **Características:**
  - **Multiplataforma:** Compatible con Windows, macOS y Linux.
  - **Código Abierto:** Disponible en GitHub, con licencias MIT y Apache 2.
  - **Coherente en varias arquitecturas:** x64, x86, ARM.
  - **Compatible con .NET Framework, Xamarin y Mono**.
  - **Modularidad:** Publicado a través de NuGet en paquetes más pequeños.
  - **Desarrollo flexible:** Implementación basada en framework o autocontenida.


## Capítulo 2: Entorno de Desarrollo

### Introducción

Un Entorno de Desarrollo Integrado (IDE) es una aplicación que proporciona un conjunto de herramientas y servicios integrados para facilitar y optimizar el desarrollo de software. Los ejemplos incluyen Visual Studio .NET, Sharp Develop, Mono Develop, Eclipse y NetBeans. Nos enfocaremos en Visual Studio .NET, su evolución, características y herramientas.

### Entorno de Desarrollo Integrado Visual Studio .NET

#### Historia de Versiones

- **Visual Studio 2002 y 2003:** Primera versión de Visual Studio .NET, versiones 7.0 y 7.1, relacionadas con .NET Framework 1.0 y 1.1.
- **Visual Studio 2005:** Versión 8.0, basada en .NET Framework 2.0, con soporte posterior para 3.0.
- **Visual Studio 2008:** Versión 9.0, lanzada para utilizar .NET Framework 3.5.
- **Visual Studio 2010:** Versión 10.0, soporta .NET Framework 4.0 e incluye el nuevo lenguaje F#.
- **Visual Studio 2012:** Versión 11.0, soporta .NET Framework 4.5, no soporta Windows XP.
- **Visual Studio Online:** Introducción de Visual Studio Online, con ediciones Basic, Professional y Advanced.
- **Visual Studio 2013:** Versión 12.0, soporta .NET Framework 4.5.1, incorpora Git y Blend.
- **Visual Studio 2015:** Versión 14, soporta .NET Framework 4.6, incluye Python y ASP.NET 5.0.
- **Visual Studio 2017:** Versión 15, soporta .NET Framework 4.7 y .NET Core 1.0, 1.1 y 2.0, integración con Xamarin y Azure.

#### Componentes del IDE Visual Studio

El entorno de desarrollo integra elementos como:

- Menús
- Barras de herramientas
- Interfaces
- Editores gráficos y de código

Las herramientas están orientadas a tareas de Diseño, Codificación, Compilación, Depuración, Implementación, y Trabajo en equipo.

#### Soluciones y Proyectos

##### Soluciones

- Contienen los elementos necesarios para crear una aplicación.
- Incluyen uno o más proyectos, archivos y metadatos.
- Archivos de definición: .sln y .suo.

##### Proyectos

- Administran de forma lógica, compilan y depuran los elementos de la aplicación.
- Resultados: ejecutable (.exe), biblioteca de vínculos dinámicos (.dll) o módulo.
- Proporcionan plantillas predefinidas para varios tipos de proyectos.

##### Proyectos y Plantillas

- Generan nuevos proyectos basados en datos proporcionados por el usuario.
- Plantillas organizadas por Categorías y Subcategorías.

#### Diferencias entre Web Sites y Web Applications

- **Web Sites:** No requiere proyecto, compila dinámicamente.
- **Web Applications:** Requiere proyecto, compila antes de ejecutar.

#### Opciones del IDE

- Personalización del IDE para ajustarlo a las necesidades del desarrollador.

#### Utilidades y Facilidades del IDE VS.Net

##### Depuración (Debugging)

- **Start debugging: (F5)** Inicia la depuración.
- **Start without debugging (Ctrl+F5):** Inicia sin depuración.

##### Refactorización (Refactoring)

- Modificación del código sin cambiar su comportamiento externo.

##### Fragmentos de Código (Snippets)

- Plantillas de código reutilizables.

##### Métodos Abreviados de Teclado

- Atajos para agilizar el desarrollo.

##### Galería de Productos y Extensiones para Visual Studio

- Extensiones y herramientas adicionales.

##### Administrador de Librerías de Terceros “NuGet”

- Gestión de paquetes y librerías.