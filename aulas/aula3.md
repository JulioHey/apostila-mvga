# MVGA

## Matriz

__Definição__:
* Agrupamento retangular de números(entradas);
* tamanho: número de linhas, número de colunas;
* Seja uma matriz arbitrária de tamanho M x N;

L/C   |   1  |  2   | ... | N
--- | --- |---  | --- |---
__1__ | a11 | a12 | ... | a1n
__2__ | a21 | a22 | ... | a2n
__...__ | ... | ... | ... | ...
__M__ | am1 | am2 | ... | amn

### Notações
* Notações mais compactas: A = [aij]m x n ou simplesmente [aij];
* Vetores linhas (1 x n) e vetores colunas (n x 1);
#### Ex:
Podemos representar um ponto através de um vetor;
### Padrão de Notação:
- A -> matriz sempre letra maiúscula;
- aij -> elemento da matriz A (letra minúscula + índices);
- __b__ vetor linha ou coluna (letra minúscula em negrito);

* Uma matriz A com n linhas e n colunas é denominada uma matriz quadrada de ordem n. Os elementos da forma aii constituem a diagonal principal;

## Aritmética de matrizes:

Para os exemplos a seguir vamos considerar as matrizes A e B tal que:
* A:

L/C   |   1  |  2  
--- | --- |---  
__1__ | a11 | a12 
__2__ | a21 | a22 
* B:

L/C   |   1  |  2  
--- | --- |---  
__1__ | b11 | b12 
__2__ | b21 | b22 

Dadas duas matrizes A e B de mesmo tamanho:
* A e B são consideradas iguais se aij = bij;
* A + B = [aij + bij]
#### Ex:
A+B:

L/C   |   1  |  2  
--- | --- |---  
__1__ | a11 + b11 | a12 + b12 
__2__ | a21 + b21 | a22 + b22 

* A - B = [aij - bij]
#### Ex:
A-B:

L/C   |   1  |  2  
--- | --- |---  
__1__ | a11 - b11 | a12 - b12 
__2__ | a21 - b21 | a22 - b22 

Multiplicação por números escalares:
* c * A = [c*aij]
#### Ex:
L/C   |   1  |  2  
--- | --- |---  
__1__ | c * a11 | c * a12 
__2__ | c * a21 | c * a22 

### Produtos de Matrizes:
* A (m x p), B (p x n);
* Número de colunas da matriz A deve ser igual ao número de colunas da matriz B;
* A * B = [cij]mn, onde cij = Somatória de aix * bxj;
#### Ex:
A =

L/C   |   1  |  2  | 3
--- | --- |--- |---  
__1__ | 1 | 2 | 3
__2__ | 4 | 5 | 6

B =

L/C   |   1  |  2  
--- | --- |---  
__1__ | 1 | 2
__2__ | 3 | 4
__3__ | 5 | 6

C =
* Primeiro passo:

L/C   |   1  |  2  
--- | --- |---  
__1__ | (a11 * b11) + (a12 * b21) + (a13 * b31) | (a11 * b12) + (a12 * b22) + (a13 * b32)
__2__ | (a21 * b11) + (a22 * b21) + (a23 * b31) | (a21 * b12) + (a22 * b22) + (a23 * b32)

* Segundo passo:

L/C   |   1  |  2  
--- | --- |---  
__1__ | (1) + (6) + (15) | (2) + (8) + (18)
__2__ | (4) + (15) + (30) | (8) + (20) + (36)

* Terceiro passo:

L/C   |   1  |  2  
--- | --- |---  
__1__ | 22 | 28
__2__ | 49 | 64

* Resultado de uma multiplicação de matrizes A (m x p), B (p x n) será uma matriz C (m x n);

### Voltando...
* A multiplicação matricial é uma operação conveniente para representação de um sistema linear de equações lineares:

 <span> | <span>|
--- |---  |
4 | 3 |
2 | 1|

Multiplicado

<span> |
--- | 
x | 
y |

=

<span> |
--- | 
48 | 
20 |

* É exatamente igual a:

4x + 3y = 48

2x + y = 20

## Operações sem análogas em aritmética:

### Transposição:
* Matrizes transpostas é basicamente trocar as linhas por colunas dessa forma;
* B sendo transposta de A teremos que:
* Se A (i x j) e B (j * i);
* A transposta de uma matriz A pode ser representada por A^t;

#### Ex:
A: 

 <span> | <span>|
--- |---  |
4 | 3 |
2 | 1|

B ou A^t:

 <span> | <span>|
--- |---  |
4 | 2 |
3 | 1 |

* Se A é uma matriz quadrada: A^T é obtida refletindo as entradas em torno da diagonal principal;

### Traço:
* Soma das entradas na diagonal principal;
* tr (A (m x n)) = Somatória aii

## Propriedades:
* A + B = B + A;
* A + (B + C) = (A + B) + C;
* A * (B * C) = (A * B) * C;

É importante prestar atenção que como na multiplicação o gasto computacional muda a partir da ordem das multiplicações, apesar de A * (B * C) = (A * B) * C, como (B * C) e (A * B), tem tamanhos diferentes é legal prestar atenção para diminuir o gasto computacional;
* A * (B + C) = (A * B) + (A * C);
* (B + C) * A = (B * C) + (C * A);

Nas distributiva da esquerda e na direita sempre vale a pena somar antes, no quesito computacional e na mão também né;

* a * (B + C) = a * B + a * C;
Todas propriedades que valem para soma também valem pra subtração;

## ATENÇÃO:

A * B != B * A
* a multiplicação pode estar definida para A * B, mas não para B * A;
* O tamanho das matrizes resultas pode ser diferente;
* O resultado das entradas pode ser diferente;

No caso de A * B == B * A, então falamos que A e B __comutam__;

## Outras Propriedades:

* Propriedades envolvendo matrizes nulas (todas as entradas iguais a zero):

- A + 0 = 0 + A = A;
- A - 0 = A
- A - A = 0
- 0 * A = 0;
- Se c * A = 0, então c = 0 ou A = 0;

Escrito com MD: (c * A = 0) -> (c = 0) v (A = 0)

* Outras propriedades de números que __não__ se aplicam a matrizes:

- Se a * b = a * c, e a != 0 então b = c;

Escrito com MD: (a * b = a * c) E (a != 0) -> (c = b)

__Não__ se aplicam a matrizes;

- Se ab = 0, então a = 0 ou b = 0;

Escrito com MD: (a * b = 0) -> (a = 0) v (b = 0)

__Não__ se aplicam a matrizes;


## Matriz Identidade:

* Matriz quadrada com entradas iguais a 1 na diagonal principal:

I = [ipq], onde ipq 1 se p = q, 0 caso contrário;

* Matriz análoga ao 1 na aritmética;

A * In = Im * A = A;

I =

<span>   |   <span>   |  <span>    | <span>  | <span> 
--- | --- |---  | --- |---
__1__ | 0 | 0 | 0 | 0
0 | __1__ | 0 | 0 | 0
0 | 0 | __1__ | 0 | 0
0 | 0 | 0 | __1__ | 0
0 | 0 | 0 | 0 | __1__

### Utilizando matrizes identidade e eliminação gaussiana para resolução de sistemas;

Voltando a resolução de sistemas lineares, o nosso objetivo ao aplicar eliminação gaussiana é chegar em uma matriz identidade de modo a facilitar a resolução do sistema;

<span> | <span> | <span>
--- | --- | --- 
4 | 3 | 48 
2 | 1 | 20 

Primeiro devemos fazer o primeiro pivô que será a entrada na linha 1 e coluna 1, virar 1;

Multiplicando por 1/4 a primeira linha temos:

<span> | <span> | <span>
--- | --- | --- 
1 | 3/4 | 12 
2 | 1 | 20 

Após isso devemos fazer o valor imediatamente abaixo = 0;

Multiplicando por -2 a primeira linha, e a somando com a segunda linha temos:

<span> | <span> | <span>
--- | --- | --- 
1 | 3/4 | 12 
0 | -1/2 | -4 

Agora passamos para o próximo pivo, que é linha = coluna = 2, queremos que ele seja = 1;

Multiplicando por -2 a segunda linha, temos que:

<span> | <span> | <span>
--- | --- | --- 
1 | 3/4 | 12 
0 | 1 | 8 

O ultimo passo é zerar todo resto da matriz fora da diagonal, que nesse caso é linha 1, coluna 2;

O último passo é multiplicar a segunda linha por -3/4 e soma-la a primeira:

<span> | <span> | <span>
--- | --- | --- 
__1__ | __0__ | 6 
__0__ | __1__ | 8 

As duas primeiras colunas forma uma matriz identidade então fica bem mais fácil de resolver o sistema de equação;

Chegamos em x = 6 e y = 8;

### Casos especiais da forma escalonada:
* Se R é a forma escalonada reduzida por linhas de uma matriz A (n x n);
#### ou R tem um linha de zeros;

Nesse caso podemos ter duas saidas:
* Infinitas soluções no caso da linha zerada termina com 0;

<span> | <span> | <span>
--- | --- | --- 
__0__ | __0__ | __0__ 
0 | 1 | 8 

* Sem solução no caso da linha zerada não terminar com 0;

<span> | <span> | <span>
--- | --- | --- 
__0__ | __0__ | __4__ 
0 | 1 | 8 

#### ou R é a matriz identidade In;

<span> | <span> | <span>
--- | --- | --- 
__1__ | __0__ | 6 
__0__ | __1__ | 8 

* Solução única;


## Inversa de uma Matriz

* Na aritmética dos números reais, cada número não nulo tem um inverso que multiplicado por ele resulta em 1;
* Como o 1 nas matrizes é In;
* Temos que a matriz inversa de A, A^-1, é uma matriz tal que:

A * A^-1 = I

* Nem sempre é possível obter uma matriz inversa, caso seja possível dizemos que A é __inversível__ (__não singular__), caso não seja inversível temos que A é __não inversível__ (__singular__);
* Se A^-1 existe ela é unica, não existem outras matrizes que satisfaçam essa condição;

### Exemplo da aplicação da inversa:

4x + 3y = 48

2x + y = 20

A =

<span> | <span> 
--- | ---  
4 | 3  
2 | 1  

v =

<span>|
---|   
x|
y|

b =

<span>|
---|   
48|
20|

A * v = b

A⁻1 * A * v = b * A^-1

I * v = b * A^-1

v = A^-1 * b

Ao final chegamos em uma comparação de escalares com variáveis assim chegando ao resultado;

### Como sabemos se uma matriz é inversível;

* Para uma matriz ser inversível ela deve ser quadrada;