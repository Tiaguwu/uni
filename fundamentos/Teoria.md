# FundamentoFundamentos Teóricos de Informática

## Clase 1 - Fundamentos de la Informática

1. **Introducción y Conceptos Generales**
    * **Teoría de la Computación:** Es el estudio matemático de las computadoras.
    * **Autómatas:** En lugar de computadoras físicas, se describen dispositivos generales denominados máquinas o autómatas.
    * **Propósito:** Cada autómata se diseña para un fin específico y reconoce datos de entrada codificados como cadenas de símbolos.
    * **Lenguajes Formales:** Son sistemas matemáticos que difieren del lenguaje natural. Su estudio abarca conjuntos de cadenas y los mecanismos para generarlas o reconocerlas.

2. **Definiciones de Base (Alfabetos y Cadenas)**
    * **Alfabeto ($\Sigma$):** Conjunto finito y no vacío de símbolos.
        * Los elementos se llaman letras o símbolos.
        * $\sigma \in \Sigma$ denota que $\sigma$ es un símbolo del alfabeto.
    * **Palabra (Cadena):** Secuencia finita de símbolos de un alfabeto.
        * **Cadena vacía ($\lambda$):** No tiene símbolos, su longitud es $|\lambda| = 0$ y pertenece a cualquier alfabeto.
        * **Igualdad:** Dos palabras $w$ y $z$ son iguales si tienen la misma longitud y los mismos símbolos en la misma posición.
    * **Longitud ($|w|$):** Es el número de símbolos que tiene la cadena.

3. **Operaciones sobre Cadenas**
    * **Concatenación ($w.z$):** Añadir la palabra $z$ a continuación de la cadena $w$.
        * $\lambda$ es el elemento neutro: $\lambda.w = w$.
    * **Potencia ($w^n$):** Notación para reducir la concatenación repetida.
        * $w^0 = \lambda$.
        * $w^n = w.w^{n-1}$ para $n > 0$.
    * **Prefijo y Sufijo:** Si $z = xy$, entonces $x$ es prefijo de $z$ e $y$ es sufijo de $z$.
    * **Inversa o Reversa ($w^R$):** Cadena formada por los mismos símbolos pero en orden inverso.
        * Propiedad: $(x^R)^R = x$.
    
4. **Definiciones y Operaciones sobre Lenguajes**
    * **Lenguaje:** Cualquier subconjunto de $\Sigma^*$ (el lenguaje universal).
    * **Lenguaje Vacío ($\emptyset$):** No contiene ninguna cadena. Es distinto al lenguaje que contiene la cadena vacía $\{\lambda\}$.
    * **Sublenguaje:** $A \subseteq B$ si todas las cadenas de $A$ pertenecen a $B$.
    * **Igualdad de Lenguajes:** $A = B$ si y solo si $A \subseteq B$ y $B \subseteq A$.

    ##### Operaciones Conjuntistas
    *  **Unión ($A \cup B$):** Palabras que pertenecen al menos a uno de los dos lenguajes. Es conmutativa, asociativa e idempotente ($L \cup L = L$).
    * **Intersección ($A \cap B$):** Palabras que pertenecen a $A$ y $B$ simultáneamente.
    * **Diferencia ($A - B$):** Palabras que están en $A$ pero no en $B$.
    * **Complemento ($\bar{L}$):** Definido como $\Sigma^* - L$.

    ##### Operaciones Específicas de Lenguajes
    * **Concatenación ($A.B$):** Todas las cadenas formadas por $w.x$ donde $w \in A$ y $x \in B$.
        * No es conmutativa ($A.B \neq B.A$)
        * Es distributiva respecto a la unión: $A.(B \cup C) = (A.B) \cup (A.C)$.
    * **Potencia de Lenguaje ($L^n$):**
        * $L^0 = \{\lambda\}$.
        * $L^n = L.L^{n-1}$.
    * **Reflejo ($L^R$):** Lenguaje que contiene las palabras inversas de $L$.
        * Teorema: $(A.B)^R = B^R.A^R$.

5. **Clausuras**
    * **Clausura de Kleene ($L^*$):** Unión de todas las potencias posibles de $L$, incluyendo $L^0$.
        * $L^* = \bigcup_{i=0}^{\infty} L^i$. Siempre contiene a $\lambda$.
    * **Clausura Positiva ($L^+$):** Unión de todas las potencias excepto la vacía.
        * $L^+ = \bigcup_{i=1}^{\infty} L^i$.
        * Relaciones: $L^* = L^+ \cup \{\lambda\}$ y $L^+ = L^*.L = L.L^*$.
