## Inversa de uma Matriz

* Na aritmética dos números reais, cada número não nulo tem um inverso que multiplicado por ele resulta em 1;
* Como o 1 nas matrizes é In;
* Temos que a matriz inversa de A, A^-1, é uma matriz tal que:

  * A * A^-1 = I

* Nem sempre é possível obter uma matriz inversa, caso seja possível dizemos que A é __inversível__ (__não singular__), caso não seja inversível temos que A é __não inversível__ (__singular__);
* Se A^-1 existe ela é unica, não existem outras matrizes que satisfaçam essa condição;

### Exemplo da aplicação da inversa:

  * 4x + 3y = 48
  * 2x + y = 20
  * A =

    <span> | <span> 
    --- | ---  
    4 | 3  
    2 | 1  

  * v =

    <span>|
    ---|   
    x|
    y|

  * b =

    <span>|
    ---|   
    48|
    20|

    * A * v = b
    * A⁻1 * A * v = b * A^-1
    * I * v = b * A^-1
    * v = A^-1 * b

* Ao final chegamos em uma comparação de escalares com variáveis assim chegando ao resultado;

### Como sabemos se uma matriz é inversível;

* Para uma matriz ser inversível ela deve ser quadrada;

### Teorema (inversa do produto):

* Se A e B são matrizes inversíveis e de mesmo tamanho;

  * (A * B)^-1 = A^-1 * B^-1;
  * Isso seria tipo comutação entre inversão e multiplicação?

### Teorema (inversa da transposta):

* Se uma matriz inversível A, então A^T também é inversível;

  * (A^T)^-1 = (A^-1)^T;

## Encontrando a inversa de uma matriz:

* Operações elementares sobre linhas:
  * Multiplicação por uma constante não nula c;
  * Troca de duas linhas;
  * Soma de (c vezes uma linha) a (outra linha);

* A e B são __equivalentes por linha__ se uma pode ser obtida a partir da outra através de operações elementares por linha;

### __Matriz Elementar__: 
matriz obtida a partir de I efetuando-se uma única operação elementar sobre linhas;

  * __Ex:__

    * M = 

    <span> | <span> 
    --- | ---  
    1 | 0  
    0 | -3  

    * Nessa matriz multiplicamos a última linha por -3;

    * T = 

    <span> | <span> 
    --- | ---  
    0 | 1  
    1 | 0  

    * Nessa matriz trocamos as linhas de ordem;

    * S =

    <span> | <span> 
    --- | ---  
    1 | 2  
    0 | 1  
    
    * Nessa matriz multiplicamos por 2 a segunda linha e somamos a primeira;

  * Exemplo de uso:

    * A = 

    <span> | <span> 
    --- | ---  
    a | b  
    c | d

    * A * M =

    <span> | <span> 
    --- | ---  
    a | b  
    -3c | -3d

    * Isso significa que quando você pega uma matriz elementar e multiplica ela por uma matriz qualquer o resultado é a mesma coisa que aplicar a operação elementar sobre a matriz a qualquer;

    * A * T =

    <span> | <span> 
    --- | ---  
    c | d
    a | b  

    * A * S =

    <span> | <span> 
    --- | ---  
    c + 2a | d + 2b
    a | b  

### __Teorema (afirmações equivalentes)__:

  * Dada uma matriz A nxn, as seguintes afirmações são equivalentes, isso é se uma é falsa todas são, e se todas são verdadeiras todas são;

    * A é inversível;
    * Ax = 0 tem somente a solução trivial;
    * A forma escalonada reduzido por linhas de A é In;
    * A pode ser expressa como um produto de matrizes elementares;

* A partir do último teorema:

  * Seja A uma matriz inversível de tamanho n x n:
    * Ek ... * (E2 * (E1 * A)) = In;
      * Multiplicando os dois lados da igualdade por todas matrizes elementares invertidas;
    * A = ((In * Ek^-1) ... * E2^-1) * E1^-1;
      * Utilizando a propriedade:
        * A = B * C * D
        * A⁻1 = D⁻1 * C^⁻1 * B^-1
    * A^-1 = In * (Ek ... * (E2 * E1));
    * __IMPORTANTE__: A ordem é importante, sempre multiplicando primeiro por E1, depois E2 e assim por diante;

    * Podemos representar todas as operações elementares em uma matriz A para chegarmos a Identidade :
      * ((E1 * E2) * E3) ... * Ek;
      * Que é __EXATAMENTE IGUAL__ a __A^-1__;

  * Você deve criar uma matriz estendida com [A | I], e fazer operações de forma que a antiga matriz A, vire a identidade, e oq antigamente era a matriz identidade agora é a inversa de A;

    * A ==> [A | I] ==> [I | A^-1]

  * __EX:__

    <span> | <span> | <span> 
    --- | --- | --- 
    1 | 2 | 3 
    2 | 5 | 3 
    1 | 0 | 8 

    <span> | <span> | <span> | <span> | <span> | <span>
    --- | --- | --- | --- | --- | ---
    1 | 2 | 3 | 1 | 0 | 0
    2 | 5 | 3 | 0 | 1 | 0
    1 | 0 | 8 | 0 | 0 | 1

    * Multiplicando linha 1 por -2 e somando a linha 2;

    <span> | <span> | <span> | <span> | <span> | <span>
    --- | --- | --- | --- | --- | ---
    1 | 2 | 3 | 1 | 0 | 0
    __0__ |__1__|__-3__| __-2__ | 1 | 0
    1 | 0 | 8 | 0 | 0 | 1

    * Multiplicando linha 1 por -1 e somando a linha 3;

    <span> | <span> | <span> | <span> | <span> | <span>
    --- | --- | --- | --- | --- | ---
    1 | 2 | 3 | 1 | 0 | 0
    0 | 1 | -3 | -2 | 1 | 0
    __0__ | __-2__ |__5__|__-1__| 0 | 1

    * Multiplicando linha 2 por 2 e somando a linha 3;

    <span> | <span> | <span> | <span> |<span> | <span>
    --- | --- | --- | --- | --- | ---
    1 | 2 | 3 | 1 | 0 | 0
    0 | 1 | -3 | -2 | 1 | 0
    0 | 0 |__-1__|__-5__|__2__| 1

    * Multiplicando linha 3 por -1;

    <span> | <span> | <span> | <span> |<span> | <span>
    --- | --- | --- | --- | --- | ---
    1 | 2 | 3 | 1 | 0 | 0
    0 | 1 | -3 | -2 | 1 | 0
    0 | 0 |__1__|__5__|__-2__| __-1__

    * Multiplicando linha 3 por 3 e somando a linha 2;

    <span> | <span> | <span> | <span> |<span> | <span>
    --- | --- | --- | --- | --- | ---
    1 | 2 | 3 | 1 | 0 | 0
    0 | 1 | __0__ |__13__|__-5__|__-3__
    0 | 0 | 1 | 5 | -2 |  -1 

    * Multiplicando linha 3 por -3 e somando a linha 1;

    <span> | <span> | <span> | <span> |<span> | <span>
    --- | --- | --- | --- | --- | ---
    1 | 2 | __0__ | __-14__ | __6__ | __3__
    0 | 1 |  0  | 13 | -5 | -3 
    0 | 0 | 1 | 5 | -2 |  -1 

    * Multiplicando linha 2 por -2 e somando a linha 1;

    <span> | <span> | <span> | <span> |<span> | <span>
    --- | --- | --- | --- | --- | ---
    1 | __0__ | 0 |__-40__|__-16__|__9__
    0 | 1 |  0  | 13 | -5 | -3 
    0 | 0 | 1 | 5 | -2 |  -1 

    * Dessa forma temos q a inversa da matriz inicial é:

    <span> | <span> | <span> 
    --- | --- | --- 
    -40 | -16 | 9 
    13 | -5 | -3 
    5| -2 | -1 

### Matrizes especiais:
  * __Matrizes diagonais__:
    * Apenas a diagonal é diferente de 0;
  * __Matrizes triangulares__:
    * Quando elementos acima da diagonal = 0 -> _Triangular Superior_;
    * Quando elementos acima da diagonal = 0 -> _Triangular Inferior_;
  * __Matrizes simétricas__:
    * Se A é simétrica então transposta de A = A;