# **TRABAJO PRÁCTICO Nº 1: Lenguajes Formales**

1. Sea Σ = {a, b} un alfabeto.
    1. $Σ^0$ = $\lambda$
    2. $Σ^1$ = {a, b}
    3. $Σ^2$ = {aa, ab, ba, bb}
    4. $Σ^*$ = {$\lambda$, a, b, aa, ab, ba, bb, ..}
    5. $Σ^+$ = {a, b, aa, ab, ba, bb, ..}
    6. $|Σ|$ = 2
    7. $|Σ^0|$ = 1
####
2. Sea x = abb una cadena.
    1. $x^0$ = $\lambda$
    2. $x^1$ = abb
    3. $x^2$ = abbabb
    4. $x^3$ = abbabbabb
    5. $Π_{k=0..3} x^k$ = $x^1.x^2.x^3$ = abbabbabbabbabbabb
    6. $x^r$ = bba
####
3. Sea V = { a, b} , W = { a, c} 
    1. aa ∈ V x W :heavy_check_mark:
    2. aba ∈ V x W x V :heavy_multiplication_x:
    3. aaa ∈ V x W x W :heavy_check_mark:
    4. aa$\lambda$ ∈ V x W x (W $\cup$ $\Lambda$) :heavy_check_mark:
    5. a$\lambda$ ∈ V x W :heavy_multiplication_x:
    6. a$\lambda$ ∈ V x (W $\cup$ $\Lambda$) :heavy_check_mark:
    7. a$\lambda$$\lambda$ ∈ V x (W $\cup$ $\Lambda$) x (W $\cup$ $\Lambda$) :heavy_check_mark:
    8. ac$\lambda$ ∈ V x W x $W^*$ :heavy_check_mark:

4. Dados $\Sigma$ = {a, b}, A = {a, c}
    1. $\Sigma$ $\cup$ A = {a, b, c}
    2. $\Sigma$ $\cap$ A = {a}
    3. $\Sigma$ . A = {aa, ac, ba, bc}
    4. $\Sigma$ . $A^+$ = {a. $A^+$, b. $A^+$}
    5. $\Sigma^+$ . A = {$\Sigma^+$. a, $\Sigma^+$ . c}
    6. $(\Sigma . A)^+$ = {aa, ac, ba, bc, aaaa, aaac, aaba, aabc, ...}
    7. $(\Sigma . A)^*$ = {$\lambda$, aa, ac, ba, bc, aaaa, aaac, aaba, aabc, ...}
    8. $\Sigma^* . A^*$ = {$\lambda$, a, b, c, aa, ac, ba, bc, ...}
    9. $\Sigma . \Lambda . A$ = {a$\lambda$a, a$\lambda$c, b$\lambda$a, b$\lambda$c}

5. Sean $L_1 $ = { $a^nb^k / 1 \le n \le 2k $} y $L_2$ = { $0^m1^n/$m impar y n par, ó m par y n impar}

    1. $a^3b^2$ ∈ $L_1$ :heavy_check_mark:
    2. a b ∈ $L_1$ :heavy_check_mark:
    3. $a^8b^4$ ∈ $L_1$ :heavy_check_mark:
    4. $a^{10}b^3$ ∈ $L_1$ :heavy_multiplication_x:
    5. $0^31^3$ ∈ $L_2$ :heavy_multiplication_x:
    6. $0^41^7$ ∈ $L_2$ :heavy_check_mark:
    7. $0^21^2$ ∈ $L_2$ :heavy_multiplication_x:
    8. $0^9$ ∈ $L_2$ :heavy_check_mark:
    9. $0^51^4$ ∈ $L_2$ :heavy_check_mark:
    10. $0^31^6a^2b^3$ ∈ $L_1.L_2$ :heavy_multiplication_x:
    11. $a^6b^50^41^7$ ∈ $L_1.L_2$ :heavy_check_mark:
    12. $0^21^9ab^3$ ∈ $L_2.L_1$ :heavy_check_mark:

6. 3 cadenas de distinta longitud que pertenezcan a cada uno de los siguientes lenguajes

    1. $L_1$ = {x / x ∈ {a, b}$^*$ y x contiene al menos 3 b's}
    = {bbb, bbbb, bbbbb}
    2. $L_2$ = {$a^kb^k$ / k $\ge$ 0} 
    = {$\lambda$, ab, aabb}
    3. $L_3$ = {$a^kb^k$ / k $\ge$ 1} 
    = {ab, aabb, aaabbb}
    4. $L_4$ = {$a^kb^j$ / k $\ge$ 0 ^ j $\ge$ 1} 
    = {$\lambda$b, $\lambda$bb, $\lambda$bbb}
    5. $L_5$ = {$a^kb^j$ / k $\ge$ 1 ^ j $\ge$ 0}
    = {a$\lambda$, aa$\lambda$, aaa$\lambda$}
    6. $L_6$ = {$a^kb^n$c^m / k $\neq$ n y n $\neq$ m y k, n, m $\ge$ 0}
    = {$\lambda$bcc, a$\lambda$cc, aab$\lambda$}
    7. $L_7$ = {x / x $\ge$ {a, b, c}$^*$ y x empieza y termina con distinta letra} 
    = {abc, cba, cab}
    8. $L_8$ = {$a^n(ac)^p(bab)^q$ / n $\ge$ 0, q = p+2, p $\ge$ 1} 
    = {$\lambda$acbabbabbab, aacbabbabbab, aaacbabbabbab}

7. Para cada uno de los siguientes conjuntos de cadenas, describa formalmente el lenguaje al que pertenecen y el alfabeto sobre el que está definido el lenguaje:

    1. $L_1$ = { ab, aab, aaab, aaaab, ...}
    = $a^k$b / k $\ge$ 1
    2. $L_2$ = { d, ddd, ddddd, ddddddd, ... }
    = $d^k$ / k es impar
    3. $L_3$ = { aa, aabbb, aaaabbb, aaaaaabbb, ..., aabbbbbb, aaaabbbbbb,
aaaaaabbbbbb, ... }
    =  $aa^kb^m$ / k es par y m es impar
    4. $L_4$ = {1011, 101011, 10101011, ..., 10111, 1010111, 101010111, ..., 101111, 10101111, ... }
    = $10^k1^m$ / k $\ge$ 1 ^ m $\ge$ 2
    5. $L_5$ = { ab, aabb, aaabbb, .....}
    = $a^kb^k$ / k $\ge$ 1
    6. $L_6$ = { aab, aaaabb, aaaaaabbb, ....}
    = $aa^kb^k$ / k $\ge$ 1
    7. $L_7$ = { aaabccc, aaaabcccc, aaaaabccccc, ....} crecimiento lineal
    = $a^kbc^k$ / k $\ge$ 3

8. Sean A y B alfabetos, A = { a, b, c} y B = { b, c, d}, y $L_1$, $L_2$ y  $L_3$ lenguajes
$L_1$ = {$a^ib^j$ / i $\ge$ 1, j $\ge$ 1}
$L_2$ = {$b^ic^j$ / i $\ge$ 1, j $\ge$ 1}
$L_3$ = = {$a^ib^jc^id^j$ / i $\ge$ 1, j $\ge$ 1}

    1. $L_1$ es un lenguaje sobre A. :heavy_check_mark:
    2. $L_2$ es un lenguaje sobre A $\cup$ B. :heavy_check_mark:
    3. $L_2$ es un lenguaje sobre A $\cap$ B. :heavy_check_mark:
    4. $L_3$ es un lenguaje sobre A $\cup$ B. :heavy_check_mark:
    5. $L_3$ es un lenguaje sobre A $\cap$ B. :heavy_multiplication_x:
    6. $L_1$ es un lenguaje sobre A - B. :heavy_multiplication_x:
    7. $L_1 \cup L_2$ es un lenguaje sobre A. :heavy_check_mark:
    8. $L_1 \cup L_2$ es un lenguaje sobre A $\cap$ B. :heavy_multiplication_x:
    9. $L_1$ - $L_2$ es un lenguaje sobre A. :heavy_check_mark: (PREGUNTAR)

#####
9. Sean $L_1$={λ}, $L_2$={aa, ab, bb}, $L_3$={ λ , aa, bb} y $L_4$=Ø, definidos sobre A={a,b}, obtener:

    1. $L_1 \cup L_2$ = {$\lambda$, aa, ab, bb}
    2. $L_1 \cup L_3$ = {$\lambda$, aa, bb}
    3. $L_1 \cup L_4$ = {$\lambda$}
    4. $L_1 \cap L_2$ = Ø
    5. $L_2 \cap L_3$ = {aa, bb}
    6. $L_3 \cap L_4$ = Ø
    7. $L_1 \cap L_4$ = Ø

10. Sean $L_1$ y $L_2$ los siguientes lenguajes: $L_1$ = { a } $L_2$ = { b }. Determine los conjuntos de cadenas que pertenecen a los siguientes lenguajes:
    1. $L_1^*$ = {$\lambda$, a, aa, aaa, aaaa, ...}
    2. ($L_1$ . $L_2$)$^*$ = {$\lambda$, ab, abab, ababab, ...}
    3. ($L_1 \cap L_2$)$^*$ = Ø / $\lambda$ (PREGUNTAR)
    4. $L_1^*$ . $L_2^*$ = {$\lambda . L_2$, a, ab, abb, abbb, ...}
    5. ($L_1 \cup L_2$)$^*$ = {$\lambda$, a, b, aa, ab, ba, bb, aaa, ...}
    6. ($L_1 \cup L_2$)$^*$ . $L_1$ . $L_2$ = {ab, aab, bab, aaab, abab, bbab, aaaab, ...}

11. Dados los siguientes lenguajes
$L_1$ = { $a^nb^mc^k$ / n, m, k $\ge$ 0 }
$L_2$ = { $a^ib^jc^i$ / i, j $\ge$ 1 }
L3 = { x / x ∈ {a, b}* y la cantidad de símbolos a es el doble que la cantidad de símbolos b}
Determine:

    1. $L_1 \cap L_2$ = { $a^ib^jc^i$ / i, j $\ge$ 1 }
    2. $L_1 \cup L_2$ = { $a^nb^mc^k$ / n, m, k $\ge$ 0 }
    3. $L_1 - L_2$ = {cadenas donde n $\neq$ k, o donde n, k o m = 0}
    4. $L_1 . L_2$ = { $a^nb^mc^ka^ib^jc^i$ / n, m, k $\ge$ 0 ^ i, j $\ge$ 1 }
    5. $\overline{L_1}$ = { $a^nb^mc^k$ / n, m, k $\ge$ 0 y tiene una inversion de orden}
    6. $L_1^R$ = { $c^kb^ma^n$ / n, m, k $\ge$ 0 }
    7.  $L_1^*$ = {a, b, c}*
    8.  $L_2^R$ = { $c^i,b^ja^i$ / i, j $\ge$ 1 }
    9. $L_3 \cap L_1$ = {$a^{2n}b^n$ / n $\ge$ 0}
    10. $L_3 \cup L_1$ = {$a^{2n}b^nc^k$ / k,n $\ge$ 0}

12. Describa si es posible, mediante un único conjunto las siguientes operaciones:
    1.  { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i $\neq$ s} $\cup$  { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i = s}
    = { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i = s}
    2. { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i $\neq$ s} $\cap$  { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i = s}
    = $\emptyset$ 
    3. { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i $\neq$ s} . { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i = s}
    =  {$a^kb^nd^{k+n}g^ih^sa^qb^wd^{q+w}g^eh^r$ / k, n $\ge$ 0 y i $\neq$ s ^ q, w $\ge$ 0 y e = r}
    4. { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i $\neq$ s} - { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i = s}
    = { $a^kb^nd^{k+n}g^ih^s$ / k, n $\ge$ 0 y i $\neq$ s}
    5. { $a^nb^{2k}$ / n, k $\ge$ 0} $\cup$ { $a^{2n+1}b^k$ / n, k $\ge$ 0}
    = 
    6. { $a^nb^{2k}$ / n, k $\ge$ 0} $\cap$ { $a^{2n+1}b^k$ / n, k $\ge$ 0}
    = 
    7. { $a^nb^{2k}$ / n, k $\ge$ 0} . { $a^{2n+1}b^k$ / n, k $\ge$ 0}
    = 
    8. { $a^nb^{2k}$ / n, k $\ge$ 0} - { $a^{2n+1}b^k$ / n, k $\ge$ 0}
    = 
    9. { $a^{3n}b^{2n}$ / n > 0} $\cup$ { $a^kb^j$ / k,j $\ge$ 0}
    =
    10. { $a^{3n}b^{2n}$ / n > 0} $\cap$ { $a^kb^j$ / k,j $\ge$ 0}
    =
    11. { $a^{3n}b^{2n}$ / n > 0} . { $a^kb^j$ / k,j $\ge$ 0}
    =
    12. { $a^{3n}b^{2n}$ / n > 0} - { $a^kb^j$ / k,j $\ge$ 0}
    =

