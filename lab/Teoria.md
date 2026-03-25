# **Laboratorio de Programación y Lenguajes**

## **Introducción a HTML, CSS y Bootstrap**

1. **HTML (HyperText Markup Language)**
Es el lenguaje de marcado que permite definir la **estructura** y el **contenido** de una página web (párrafos, títulos, tablas, imágenes y enlaces).
\
    **Estructura Básica y Elementos**
    * **Anatomía de un elemento:** Se compone generalmente de un **tag de apertura**, el **contenido** y un **tag de cierre**. Existen excepciones como `<img>` que no requieren cierre.

    * **Componentes del documento:**
        * `<!DOCTYPE html>`: Identifica el tipo de documento.
        * `<html>`: Raíz del documento.
        * `<head>`: Contiene metadata e información para el navegador que no se muestra al usuario.
        * `<body>`: Contiene todo lo que es visible para el usuario.
    * **Jerarquía (Árbol HTML):** Los elementos se organizan en una estructura de **padres**, **hijos** y **hermanos**.
####

2. **CSS (Cascading Style Sheets)**
Lenguaje encargado de controlar la **apariencia** y los estilos de la página (color, tipografía, alineación, fondos y espaciado).
\
**Reglas y Selectores**
    * **Conjunto de reglas:** Una declaración de estilo incluye un **selector**, una **propiedad** y un **valor** (ej. `h1 {color: #CC9900;}`).
    * **Tipos de selectores:**
        * **De elemento:** Afecta a todos los tags del mismo tipo (ej. `p`, `h1`).
        * **De identificador (#):** Usa la propiedad `id` para un elemento único.
        * **De clase (.):** Usa la propiedad `class` para aplicar estilos a múltiples elementos.
    * **Unidades y Colores:** Soporta unidades absolutas (`px`, `cm`) y relativas (`em`, `%`, `vh/vw`). Los colores se definen por nombre literal, RGB o Hexadecimal.
    * **Stylesheets:** Los estilos se guardan en archivos `.css` externos que se vinculan en el `<head>` del HTML mediante el tag `<link>`.
####
3. **DevTools**
Herramienta clave integrada en los navegadores (F12 en Chrome) que permite a los desarrolladores inspeccionar y depurar elementos, red, consola y fuentes de una web.
####
4. **Bootstrap**
Es un **framework frontend** que simplifica el diseño web mediante CSS ya estructurado. Permite adaptar las páginas a distintos tamaños de pantalla (Responsive Design) sin necesidad de ser un experto en CSS plano.
\
**Sistema de Grillas (Grids)**
Bootstrap utiliza una cuadrícula basada en **contenedores**, **filas** (`row`) y **columnas** (`col`).
    * **Breakpoints:** Define puntos de corte según el ancho de pantalla:
        * `xs`: < 768px (teléfonos).
        * `sm`: ≥ 768px (tablets).
        * `md`: ≥ 992px (notebooks pequeñas).
        * `lg`: ≥ 1200px (monitores grandes).
    * **Dimensionamiento:** El ancho se divide en columnas (ej. `col-sm-4` ocupa un tercio del ancho total disponible en una fila).