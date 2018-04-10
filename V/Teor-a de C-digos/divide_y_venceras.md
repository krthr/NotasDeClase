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
- Acorta y vencerás
- Recorta y serás vencido
