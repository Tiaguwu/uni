# Unidad 1 - Conceptos básicos de Concurrencia (CBC)

1. **Fundamentos: El Modelo de Ejecución**
Para entender la concurrencia, debemos separar el **programa** (estático) del **proceso** (dinámico).
    * **Definición Formal de Proceso (Andrews):** Un proceso es una unidad de ejecución que tiene su propio **Contador de Programa (PC)**,  una **Pila (Stack)** para variables locales y acceso a un **Espacio de Direccionamiento (memoria)**.
    * **Concurrencia vs. Paralelismo:**
        * **Concurrencia:** Es una propiedad del software. Dos tareas son concurrentes si sus periodos de ejecución se solapan en el tiempo. No requiere necesariamente dos CPUs.
        * **Paralelismo:** Es una propiedad del hardware. Requiere múltiples procesadores ejecutando instrucciones en el mismo instante de tiempo ($t$).
####
2. **Gestión de Procesos y Estados (Stallings)**
El Sistema Operativo debe engañar a los procesos para que crean que tienen la CPU para ellos solos. Para esto, utiliza el **Bloque de Control de Proceso (PCB)**.
**El Modelo de 5 Estados**
    1. **Nuevo (New):** El proceso se está creando pero no ha sido admitido en el pool de procesos ejecutables.
    2. **Listo (Ready):** El proceso está en memoria principal y espera que el Dispatcher lo elija.
    3. **Ejecución (Running):** El proceso posee la CPU.
    4. **Bloqueado (Blocked/Waiting):** El proceso no puede seguir hasta que ocurra un evento (ej. E/S, una señal de sincronización).
    5. **Terminado (Exit):** El proceso finalizó y el SO libera sus recursos.
####
3. **La Naturaleza de la Interacción**
Los procesos no viven aislados. Interactúan de dos formas principales según Andrews:
    * **Competencia:** Compiten por recursos físicos (CPU, memoria, impresora). No saben de la existencia de los otros.
    * **Cooperación:** Trabajan juntos para resolver un problema (ej. un pipeline de datos). Aquí es donde la sincronización es crítica.

    **El Problema del No-Determinismo**
Debido a que el SO puede interrumpir un proceso en cualquier instrucción (preemption), el orden de ejecución es aleatorio. Esto genera:
    * **Intercalación (Interleaving):** El orden relativo de las instrucciones de diferentes procesos es variable.
    * **Efectos Colaterales:** Si dos procesos comparten una variable `global_x`, el resultado de `global_x++` no es atómico. En lenguaje de máquina, esto son 3 pasos: `LOAD`, `INCREMENT`, `STORE`. Si un proceso es interrumpido entre el `LOAD` y el `STORE`, el dato final será erróneo.
####
4. **Propiedades de Seguridad y Vitalidad (Safety & Liveness)**
En sistemas secuenciales, usamos post-condiciones. En concurrentes, usamos **Invariantes**.
\
    **Propiedades de Seguridad (Safety)**
Aseguran que el programa **nunca** entre en un estado "malo".
    * **Exclusión Mutua:** Es la propiedad de seguridad más famosa. Evita que dos procesos estén en su **Sección Crítica** (la parte del código que toca recursos compartidos) simultáneamente.

    **Propiedades de Vitalidad (Liveness)**
Aseguran que el programa **eventualmente** progrese.
    * **Ausencia de Deadlock (Interbloqueo):** Situación donde el Proceso A espera al B, y el B espera al A, quedando ambos congelados.
    * **Ausencia de Starvation (Inanición):** Un proceso nunca logra acceder al recurso porque otros siempre le "ganan" el turno.
####
5. **El Concepto de Atomicidad y Acciones Especiales**
Andrews clasifica las acciones según su visibilidad:
    * **Acciones Atómicas Especiales:** Operaciones que el hardware garantiza que son indivisibles (ej. leer una palabra de memoria alineada).
    * **Sentencia `await`:** Una construcción teórica para expresar que un proceso debe esperar a que una condición sea verdadera antes de ejecutar una acción atómica.
####
6. **Sincronización: La Solución**
Para controlar el caos del no-determinismo, usamos dos tipos de sincronización:
    * **Sincronización por Exclusión Mutua:** Para proteger variables compartidas.
    * **Sincronización por Condición:** Para coordinar el progreso (ej. un proceso "Productor" debe avisar al "Consumidor" que el dato ya está listo).