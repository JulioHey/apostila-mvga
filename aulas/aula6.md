## Propriedades dos Determinantes:
  * Sejam A e B matrizes de tamanho n x n, e k um escalar:
    * det(kA) = k^n * det(A);
    * det(A + B) != det(A) + det(B);
  * Quando A, B e C diferem em apenas 1 linha (ou coluna) e a linha em questão em C é definida pela soma das respectivas linhas (ou coluna) de A e B, temos que:
    * det(C) = det(A) + det(B);
    * __EXEMPLO__:

    * A =

      <span> | <span> | <span> | 
      --- | --- | --- |
      __1__ | __2__ | __3__
      __4__ | __5__ | __6__
      2 | 2 | 3

    * B =
  
      <span> | <span> | <span> | 
      --- | --- | --- |
      __1__ | __2__ | __3__
      __4__ | __5__ | __6__
      4 | 5 | 6

    * C =
  
      <span> | <span> | <span> | 
      --- | --- | --- |
      __1__ | __2__ | __3__
      __4__ | __5__ | __6__
      6 | 7 | 9
  
  * __Teorema:__
    * Uma matriz quadrada A é inversivel se e somente se det(A) != 0;
    * __Consequencia__ se uma matriz tem duas linhas ou colunas proporcionais, ela não é inversivel;
  * __Teoremas__:
    * det(A * B) = det(A) * det(B);
    * Consequência:
      * det(A * A^-1) = det(I);
      * det(I) = det(A) * det(A^-1);
      * 1 = det(A) * det(A^-1);
      * det(A^-1) = 1 / det(A);
## Matriz de cofatores e adjunta:
  * Seja A uma matriz n x n, e Cᵢⱼ de aᵢⱼ. A matriz de cofatores de A é definida como sendo a adjunta:

      <span> | <span> | <span> | <span> | 
      --- | --- | --- | --- |
      C₁₁ | C₁₂ | ... | C₁ₙ |
      C₂₁ | C₂₂ | ... | C₂ₙ |
      ... | ... | ... | ... |
      Cₙ₁ | Cₙ₂ | ... | Cₙₙ |
    
  * A inversa de A pode ser escrita como sendo:
    * A^⁻1 = 1/det(A) * adj(A);
  * __Regra de Cramer__:
    * Seja A * x = b um sistema de n equações e n incógnitas tal que det de A != 0. A solução única do sistema é:
      * x₁ = det(A₁)/det(A);
      * x₂ = det(A₂)/det(A);
      * ...
      * xₙ = det(Aₙ)/det(A);
    * Sendo Aⱼ a matriz obtida pela substituição da coluna j pelo vetor coluna b;
### Teorema das afirmações equivalentes:
  * Dada A um matriz n x n, as seguintes afirmações são equivalentes:
    * A é inversível;
    * Ax = 0 tem somente solução trivial;
    * A forma escalonada reduzido por linhas de A é In;
    * A pode ser expressa como um produto de matrizes elementares;
    * A * x = b tem exatamente uma solução com cada matriz b de tamanho n x 1;
    * det(A) != 0; 
## Testes de Colinearidade:
  * Se temos três pontos:
    * P₁ = (x₁, y₁);
    * P₂ = (x₂, y₂);
    * P₃ = (x₃, y₃);
  * Podemos testar se são paralelos através do determinante da matriz:
    * _A =_

      <span> | <span> | <span> | 
      --- | --- | --- |
      __x₁__ | __x₁__ | __x₃__
      __y₁__ | __y₂__ | __y₃__
      1 | 1 | 1
    
    * se det(A) = 0 então são colineares;
    * como y pode ser escrito como um _y = ax + b_, temos que A =

      <span> | <span> | <span> | 
      --- | --- | --- |
      __x₁__ | __x₁__ | __x₃__
      __ax₁ + b__ | __ax₂ + b__ | __ax₃ + b__
      1 | 1 | 1
    
    * Dessa forma fica provado o porque de quando os pontos são colineares eles o determinante da matriz é 0;
    * Pois multiplicando a linha 3 por b e tirando da 2;

      <span> | <span> | <span> | 
      --- | --- | --- |
      __x₁__ | __x₁__ | __x₃__
      __ax₁__ | __ax₂__ | __ax₃__
      1 | 1 | 1

    * Dividindo a linha 2 por _a_;

      <span> | <span> | <span> | 
      --- | --- | --- |
      __x₁__ | __x₁__ | __x₃__
      __x₁__ | __x₂__ | __x₃__
      1 | 1 | 1

    * Como duas linhas são iguais -> det é 0;
  * No espaço tridimensional teriamos:
    * P₁ = (x₁, y₁, z₁);
    * P₂ = (x₂, y₂, z₂);
    * P₃ = (x₃, y₃, z₃);
    * P₄ = (x₄, y₄, z₄);
  * E agora teriamos um teste de coplanaridade, se P₄ está contido no plano definido por P₁ P₂ P₃;
    
