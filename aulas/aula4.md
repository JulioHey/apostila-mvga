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

* __Teorema (afirmações equivalentes)__:

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
      * Multiplicando uma a uma em ambos lados:
    * A^-1 = In * (Ek ... * (E2 * E1));
    * __IMPORTANTE__: A ordem é importante, sempre multiplicando primeiro por E1, depois E2 e assim por diante;

    * Podemos representar todas as operações elementares em uma matriz A para chegarmos a Identidade :
      * ((E1 * E2) * E3) ... * Ek;
      * Que é __EXATAMENTE IGUAL__ a __A^-1__;