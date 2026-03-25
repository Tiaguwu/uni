# Ingeniería de Software II
## Introducción 

1. **Fundamentos y Conceptos Clave**
    * **Definición (Pressman):** Incluye instrucciones (programas), estructuras de datos que permiten manipular información y documentos que describen la construcción y uso.
    * **Definición (Sommerville):** Programas de computadora y su documentación asociada.

    * **Tipos de Productos:**
        * **Genéricos:** Desarrollados para un mercado amplio y diversos clientes.
        * **A medida:** Desarrollados específicamente para un cliente y sus necesidades particulares.

    * **Importancia y Costos:** El software es el "alma mater" de los sistemas modernos (transporte, salud, industria). Económicamente, tiene una particularidad: **cuesta más mantener el software que desarrollarlo**.
        * **Primera Ley del Software (Nathan Myhrvold):** "El software es un gas. Se expande hasta llenar todo el recipiente que lo contiene".
#####
2. **Ingeniería de Software (IS)**
    Es una **disciplina de la ingeniería** que abarca todos los aspectos de la producción, desde la especificación inicial hasta el mantenimiento.
    * **Enfoque:** Sistemático, disciplinado y cuantificable.
    * **Diferencias clave:**
        * vs. Ciencias de la Computación: Estas se centran en teorías y fundamentos; la IS se enfoca en los problemas prácticos del desarrollo.
        * vs. Ingeniería de Sistemas: La IS es solo una parte de la Ingeniería de Sistemas, la cual incluye hardware y procesos generales.

    **Disciplinas que la integran**
    La IS se divide en aspectos de **Desarrollo** (requerimientos, diseño, construcción, pruebas) y de **Administración** (gestión de configuración, procesos, calidad).
#####
3. **Procesos y Métodos**  
    * **Proceso de Software:** Conjunto de actividades (Especificación, Desarrollo, Validación y Evolución) para crear o evolucionar software.
    * **Modelo de Proceso:** Representación simplificada de un proceso (ej. Cascada, Evolutivo, Basado en componentes).
    * **Métodos de IS:** Enfoques estructurados para obtener calidad a costo razonable (ej. Métodos estructurados de De Marco o métodos Orientados a Objetos).
####
4. **El Documento de Requerimientos (SRS)**
Un software bien diseñado debe ser **mantenible**, **seguro**, **eficiente** y **amigable**. Para lograrlo, la Especificación de Requerimientos de Software (SRS) debe cumplir atributos críticos:

| Atributo      | Descripción |
|:--------------|--------------|
| Correcto | Si los requerimientos escritos son los que el software realmente debe cumplir. | |
| No ambiguo | Cada requerimiento tiene una sola interpretación posible. |
| Completo | Incluye todas las funcionalidades, respuestas a entradas y unidades de medida. |
| Consistente | No existen contradicciones entre los requerimientos. |
| Verificable | Existe un método cuantificable para comprobar si se cumple (evitar frases como "debe funcionar bien") |
| Modificable | Su estructura permite cambios fáciles y consistentes (índices, sin redundancias). |
| Rastreable | Se conoce el origen del requerimiento (hacia atrás) y su impacto en el diseño (hacia adelante). |

5. **Aplicaciones y Retos Actuales**
La IS se aplica en diversos ámbitos:
    * **Sistemas:** SOs, compiladores.
    * **Tiempo Real:** Control de aviones, clima.
    * **Empotrados:** Software en ROM para hardware específico
    * **IA:** Algoritmos declarativos, reconocimiento de patrones.

    **Retos fundamentales:** La heterogeneidad de los sistemas, la herencia (sistemas antiguos que deben seguir funcionando) y la presión por reducir los plazos de entrega.