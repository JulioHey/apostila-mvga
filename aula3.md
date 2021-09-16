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
