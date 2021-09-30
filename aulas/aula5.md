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
    
    * C₁₁ = -4

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
  ### Cálculo do determinante através de redução por linhas:
  #### Teoremas:
  * __Teorema 1__:
    * Seja A uma matriz de tamanho n x n. Se A possui uma _linha ou uma coluna de zeros_ o determinante é 0;
    * Pode ser percebido através do cálculo dos cofatores se linha i só tem 0 teremos:
      * __det(A)__: 0 * Cᵢ₁ + 0 * Cᵢ₂ + ... + 0 * Cᵢₙ;
  * __Teorema 2__:
    * Se uma matriz A de tamanho n x n, det(A) = det(Aᵀ);
  * __Teorema 3__:
    * Dada uma matriz A de n x n:
      * Se B é a matriz obtida pela multiplicação de uma única linha (ou coluna) de A por um escalar k, então: __det(B) = k*det(A)__;
      * Se B é a matriz obtida pela permutação de duas linhas (ou colunas) da matriz A, então: __det(B) = -det(A)__;
      * Se B é a matriz obtida quando um múltiplo de uma linha (ou coluna) de A é somada a outra linha (ou coluna), então: __det(B) = det(A)__;
    * Dada uma matriz E de n x n:
      * Se E é a matriz obtida pela multiplicação de uma única linha (ou coluna) de In por um escalar k, então: __det(E) = k__;
      * Se E é a matriz obtida pela permutação de duas linhas (ou colunas) da matriz In, então: __det(E) = -1__;
      * Se E é a matriz obtida quando um múltiplo de uma linha (ou coluna) de I é somada a outra linha (ou coluna), então: __det(B) = 1__;
  * __Teorema 3:__
    * Seja A uma matriz n x n, se duas linhas ou colunas 
#### Cálculo:
  * Reduzir a matriz ao formato triangular superior, através de operações elementares por linhas;
  * Calcular o determinante da matriz triangular superior;
  * Relacionar este determinante ao da matriz original;
  * __Exemplo__:
    * det(A) = 

    <span> | <span> | <span> |
    --- | --- | --- | 
    0 | 1 | 5
    3 |-6 | 9
    2 | 6 | -1

    * Trocamos a linha 1 com a 2 e ficamos com:

    <span> | <span> | <span> |
    --- | --- | --- | 
    3 |-6 | 9
    0 | 1 | 5
    2 | 6 | -1

    * Pelo teorema temos q o determinante dessa nova matriz é *-1 * det(A) = det(B)*;
      * *-det(B) = det(A)*;

    <span> | <span> | <span> |
    --- | --- | --- | 
    1 |-2 | 3
    0 | 1 | 5
    2 | 6 | -1

    * Agora multiplicamos a linha 1 por 1/3, dessa forma o determinante dessa nova matriz é *1/3 * det(A) = -det(B)*;
      * *det(A) = det(B) * -3*;

    <span> | <span> | <span> |
    --- | --- | --- | 
    1 |-2 | 3
    0 | 1 | 5
    0 | 10 | -5

    * Multiplicamos a linha 1 por -2 e somamos a linha 3, dessa forma não mudamos o determinante, *det(A) = det(B) * -3*;

    <span> | <span> | <span> |
    --- | --- | --- | 
    1 |-2 | 3
    0 | 1 | 5
    0 | 0 | -55

    * Multiplicamos a linha 2 por -10 e somamos a linha 3, dessa forma não mudamos o determinante, *det(A) = det(B) * -3*;

    * Agora calculamos o determinante dessa nova matriz, __det(B) = -55 * -3 = 165 = det(A)__;