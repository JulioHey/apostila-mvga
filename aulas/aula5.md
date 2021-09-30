## Determinantes:
  * Função que associa um número real a uma matriz;
  * f(A) = x;
  * _det(A_;
  * Determinantes podem ser usados para resolver sistemas de equações lineares, ou para obter a inversa de uma matriz;
  ### Algumas definições. Seja A uma matriz quadrada de tamanho n * n;
  * Menor da entrada *aᵢⱼ*:
    * *Mᵢⱼ* = det(A sem a linha i e coluna j);
  * Cofator da entrada *aᵢⱼ*;
    * *cᵢⱼ* = (-1)ᶦ⁺ʲ * *Mᵢⱼ*;
    * *cᵢⱼ* > 0 se i + j = par e *cᵢⱼ* < 0 se i + j = impar;
  * __EXEMPLO__:

    * *A* =

      <span> | <span> | <span> |
      --- | --- | --- | 
      3 | 1 | -4
      2 | __5__ | __6__
      1 | __4__ | __8__

    * Para sabermos *M₁₁* de *A* = 

      <span> | <span> |
      --- | --- | 
      5 | 6
      4 | 8

      * = (*5 * 8*) - (*4 * 6*) = __16__

      * *c₁₁ = (-1)¹⁺¹ * M₁₁ = M₁₁ = __16__*;

    * Para sabermos *M₃₂* de *A* = 

      <span> | <span> |
      --- | --- | 
      3 | -4
      2 | 6

      * = (*2 * -4*) - (*3 * 6*) = __26__

      * *c₃₂ = (-1)³⁺² * M₃₂ = -M₃₂ = __-26__*
  ### Determinante de uma matriz de tamanho 1x1:

  * A = [a₁₁];
  * Seu determinante det(A) é definido como:
    * *det(A)* = **a₁₁**;
  ### Definição Geral:
  * __det(A)__: a₁ⱼ * C₁ⱼ + a₂ⱼ * C₂ⱼ + ... + aₙⱼ * Cₙⱼ;
    * Expansão de cofatores ao longo da coluna *j*;
  * __det(A)__: aᵢ₁ * Cᵢ₁ + aᵢ₂ * Cᵢ₂ + ... + aᵢₙ * Cᵢₙ;
    * Expansão de cofatores ao longo da linha *i*;
  * A partir dessa fórmula é possível calcular o matriz de uma matriz A de forma recursiva através dos cofatores;

  * __Exemplo 1__:

    * *A* = 

    <span> | <span> |
    --- | --- | 
    a | b
    c | d

    * *det(A) = a * C₁₁ + b * C₁₂*;
    * *C₁₁ = (-1)¹⁺¹ * M₁₁ = 1 * |d| = __d__*;
    * *C₁₂ = (-1)¹⁺² * M₁₂ = -1 * |c| = __-c__*;
      * Assim sendo:
    * __det(A)__ = __a * d - b * c__;
  * __Exemplo 2__:

    * *A* =

    <span> | <span> | <span> |
    --- | --- | --- | 
    3 | 1 | 0
    -2 |-4 | 3
    5 | 4 | -2

    * *det(A) = 3 * C₁₁ + 1 *C₁₂ + 0 * C₁₃*;
    
    * C₁₁ = 4

      <span> | <span> |
      --- | --- | 
      -4 | 3 |
      4 | -2 |

    * C₁₂ = -11

      <span> | <span> |
      --- | --- | 
      -2 | 3 |
      5 | -2 |

    * *3 * -4 - 1 * -11 = __1__*;
  * __Importante__: sempre escolher a linha ou coluna que tem o maior número de 0 possíveis;
  ### Definição:
  * Para qualquer matriz triangular:
    * O determinante será igual a multiplicação dos valores da diagonal;