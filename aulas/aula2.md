### Retomado do problema dos carros:
  * Existem 48 rodas e 20 farois em estoque, a fabrica pode fazer carros ou tricilos calcule qual é o jeito de utilizar todas rodas e todos farois para fazer carros ou triciclos:
    * Equações resultantes;
      * *x = numero de carros*;
      * *y = n de triciclos*;
      * **4 * x + 3 * y = 48**;
      * **2 * x + y = 20**;

      * Resultado => __x = 6__ e __y = 8__;
### Possiveis Soluções de um Sistema: 
  * Em um sistema pode haver 3 desfechos:
    - Soluções infinitas;
    - Sem solução;
    - Uma solução;
### Solução:
  - Quando existem mais equações do que variáveis, a solução vai estar over definida, n sei escreve isso em português, e quando tem menos existem infintas soluções;
  - As equações de um sistema de equação pode ser representada a partir de matrizes:
      
      |4 3| * |x| = |48|

      |2 1|   |y|   |20|

      * A   *  v  =  b
      * multiplicando por A^-1 nos dois lado temos que:
      * A^-1 * A * v = A^-1 * b
      * A^-1 * A = I (matriz identidade) => simplificando temos que:
      * v = A^-1 * b

  * Assim temos que v que é a matriz das variaveis vai ser igual a uma matiz numerica, resultado da multiplicação, dessa forma temos o valor de cada variavel que satisfaz o sistema;
### Representação Geométrica:
  * É possível representar um sistema de equações em uma forma geometrica:
    - A forma definida pela equação de __n__ variaveis vai ter __n - 1 dimensões__;
    - A __intersecção__ das __formas geometricas__ definidas pelas equações vai ser a __solução__;
    __Exemplo__:
        - Em um sistema de 2 variaveis e 2 equações, cada equação vai ser representada em uma reta, e o ponto em que elas se cruzam vai ser a solução, caso as retas sejam paralelas não haverá solução;
        - Em um sistema de 3 variaveis e 3 equações, teremos 3 planos, cada dupla de planos vai se interceptar em uma reta, e onde as 3 retas se interceptarem, ou na instersecção entre os 3 planos, teremos a solução caso, uma reta ou plano sejam paralelos não havera solução;

### Eliminação Gaussiana:
 * __Exemplo 1: Solução Única__:
    <span> | <span> | <span> |
    --- | --- | --- | 
    | 4 | 3 | 48 |
    | 2 | 1 | 20 | 

    * Da matriz acima para debaixo a primeira linha foi multiplicada por 1/4

    <span> | <span> | <span> |
    --- | --- | --- | 
    | 1 | 3/4 | 12 |
    | 2 | 1 | 20 | 

    * Aqui a primeira linha foi multiplicada por -2 e somada a linha de baixo

    <span> | <span> | <span> |
    --- | --- | --- | 
    | 1 | 3/4 | 12 |
    | (2 - 1*2) | (1 - (3/4 * 2)) | (20 - 2 *12) | 


    <span> | <span> | <span> |
    --- | --- | --- | 
    | 1 | 3/4 | 12 |
    | 0 | -1/2 | -4 | 

    * Agora multiplicamos a linha 2 por -2:

    <span> | <span> | <span> |
    --- | --- | --- | 
    | 1 | 3/4 | 12 |
    | 0 | 1 | 8 |

    * Por ultimo multiplicamos a linha 2 por -3/4 e somamos a linha 1:

    <span> | <span> | <span> |
    --- | --- | --- | 
    | 1 | 0 | 6 |
    | 0 | 1 | 8 |

    * Operações que podem até mudar a forma geométrica mas a solução do sistema continua a mesma dessa forma é possível simplificar uma matriz;
    Exemplo de operações gaussianas:
      - Troca de linhas de lugar;
          - Não muda nd na representação geometrica;
      - Multiplicação de uma linha e somada com outra;
          - Multiplicação não pode ser por 0;
          - Rotaciona a forma geometrica em torna da intersecção entre as duas;
      - Multiplicação de uma linha por um valor;
          - Multiplicação não pode ser por 0;
          - Não muda nd na representação geometrica;

    * Refazendo o problema com a nova equação temos que:
    
    <span> | <span> | 
    --- | --- |
    | 1 | 0 |
    | 0 | 1 |

    *

    <span> |
    --- |
    x |
    y |

    =

    <span> |
    --- |
    6 |
    8 |

    * Assim sendo temos 2 novas equações:
        * 1 * x + 0 * y = 6
        * 0 * x + 1 * y = 8;
      * Pela segunda equação ja temos que y = 8, substituindo temos que x = 6;

  * __Exemplo 2: Soluções Infinitas:__:
    * Agora vamos ao caso que tem infitas soluções:

    <span> | <span> | <span> |
    --- | --- | --- | 
    | 4 | 2 | 40 |
    | 2 | 1 | 20 | 

    * Nesse caso após as operações de gauss teremos que:

    <span> | <span> | <span> |
    --- | --- | --- | 
    |4 | 2 |20|
    |0 | 0 | 0|

    * Transformando em equação:
      - 4 * x + 2 * y = 40;
      - 0 * x + 0 * y = 0; => tautologia;

    * Dessa forma temos que temos apenas uma reta que restringi a solução assim sendo temos infinitas soluções, definida pela reta y = (40 - 2x)/4;

  * __Exemplo 3: Nenhuma solução__:
    * Agora vamos ao caso que não tem solução:

    <span> | <span> | <span> |
    --- | --- | --- | 
    | 4 | 2 | 48 |
    | 2 | 1 | 20 | 
    
    * Nesse caso após as operações de gauss teremos que:

    <span> | <span> | <span> |
    --- | --- | --- | 
    | 4 | 2 | 48 |
    | 0 | 0 | -4 | 

    * Transformando em equação:
      - 4 * x + 2 * y = 40;
      - 0 * x + 0 * y = -4; => Contradição;

    * Como chegamos em uma contradição em uma das equações e a solução deve ser verdade para todas equações temos que o sistema não tem equação;