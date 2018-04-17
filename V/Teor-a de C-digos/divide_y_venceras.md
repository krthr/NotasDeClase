# MODELAJE DE LA SOLUCIÓN DE UN PROBLEMA

MODELOS -> SOLUCIÓN PROBLEMAS TRATABLES COMPUTACIONALMENTE

Mundo real > Problemas > Teoría de algoritmos > Tipos (A1, A2, ..., Ak), Algoritmo optimal* Aj* > Lenguaje de probamación Pj > Paradgisma de programación > Solución programa (?) > Modelar el programa en términos de herramientas

# Métodos generales → Solución de problemas
- Dividir y Conquistar
- Técnias heurísticas y de aproximación
- Teoría de Grafos
- Técnicas de Retroceso (Backtracking)
- Programación Dinámica

## Método de Divir y Conquistar
1. **Dividir** el problema $$P_c$$ en subproblemas
2. **Conquistar** las soluciones de los subproblemas (Recursivamente)
3. **Combinar** las soluciones de los subproblemas para lograr la solución del $$P_c$$

### Modelo matemático genérico para la solución de problemas por D&V
$$T(n) = aT(\frac{n}{b}) + cn^k$$

$$n$$: Número de datos
$$cn^k$$: Trabajo adicional
$$b$$: Número de veces que se dividen los datos
$$a$$: Número de veces que se repite la división

#### Tipos de Ecuaciones de Recurrencia de Dive and Conquer
- Divide y vencerás
$$T(n) = T(\frac{n}{b}) + cn^k$$
- Acorta y vencerás
$$T(n)= T(n - d) + cn^k$$
- Recorta y serás vencido
$$T(n) = aT(n - d) + cn^k$$


    Func: DivideVenceras(x)
        Si (x es suficientemente simple) Entonces
            retornar solucionSimple(x)
        SiNo
            Descomponer x en x_1, ..., x_k
            Para i = 1, k, i++
                y_i = DivideVenceras(x)
            FinPara
            
            retornar combinar(y_i), para obtener una sol y de x
        FinSi
        retornar y
    Fin

$$x_1, ..., x_k$$: Son los subprobelmas en los cuales se dividió el probl. principal, todos con las mismas caract.
$$y_1, ..., y_k$$, Son las soluciones a los subproblemas obtenidos