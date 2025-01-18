# Relações Binárias

## Pertencimento de um Elemento em um Conjunto
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ x^2\ -\ 2x\ -\ 3\ =\ 0 \}$
- Elemento "-1" pertence ao conjunto X.
    - Dizemos: $\mathrm -1 \in X $  
- Pergunta feita em script:
    - O elemento "x" pertence a um conjunto "y"?
    - Python:  
    ```python
    y = {-1, 3}
    x = -1
    w = 4
    x_pertece_a_y  = x in y  # True
    w_pertece_a_y  = w in y  # False
    ```  

## Não Pertencimento de um Elemento em um Conjunto
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ x^2\ -\ 2x\ -\ 3\ =\ 0 \}$
- Elemento "-8" não pertence ao conjunto X.
    - Dizemos: $\mathrm -8 \not\in X $  
- Pergunta feita em script:
    - O elemento "-8" não pertence a um conjunto "y"?
    - Python:  
    ```python
    y = {1, 3}
    x = -8
    w = 3
    x_nao_pertece_a_y  = x not in y # True
    w_nao_pertece_a_y  = w not in y # False
    ```  

## Inclusão de um Conjunto em outro Conjunto
- Sejam X e Y conjuntos. 
- Dizemos que X está contido em Y e escrevemos $\mathrm X \subset Y$, se todo elemento de X é um elemento de Y. Caso X não esteja contido em Y, escrevemos $\mathrm X \not\subset Y$.
- Dizer que X não está contido em Y significa que existe pelo menos um elemento de X que não é elemento de Y.
- Possui 3 propriedades matemáticas:
    - Propriedade reflexiva:
        - $ A \ \subset \ A $
    - Propriedade antisimétrica:
        - $ A \ \subset \ B \ e \ B \ \subset \ A \to A = B $
    - Propriedade transitiva:
        - $ A \ \subset \ B \ e \ B \ \subset \ C \to A \ \subset \ C $
- Pergunta feita em script:
    - Todos elementos de um conjunto estão dentro de outro conjunto?
    - Python:  
    ```python
    a = {1, 3}
    b = set(range(1,7))
    c = set(range(1,3))
    a_eh_subset_of_b = a.issubset(b) # True
    a_eh_subset_of_c = a.issubset(c) # False
    ```  

## Igualdade entre Conjuntos
- Sejam X e Y dois conjuntos que estão contidos em um mesmo conjunto universo. Dizemos que X é igual a Y caso $\mathrm X \subset Y$ e $\mathrm Y \subset X$. Neste caso escrevemos $\mathrm X = Y$.
    - X é igual a Y se e somente se estes conjuntos possuem os mesmos elementos.
    - Por definição, para demonstrar que um conjunto X é igual a um conjunto Y, devemos verificar as duas inclusões indicadas: $\mathrm X \subset Y$ e $\mathrm Y \subset X$.

### Como demostrar a igualdade de conjuntos?
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ x^2\ -\ 2x\ -\ 3\ =\ 0 \}$
- $\mathrm Y = \{-2, 1\}$
- Demostre que X = Y.
- Planejamento da demostração:
    - Primeiro: Qual a definição da igualdade?
        - Deve-se indicar na demonstração a definição de igualdade.
        - Por definição, para que X = Y, deve ser válida a hipótese $\mathrm X \subset Y$ e a hipótese $\mathrm Y \subset X$.
    - Então, dividimos a demostração em duas verificações de inclusão. As duas devem ser verdadeiras.
        - Para verificar cada relação de inclusão, por sua vez, devemos verificar a relação de pertencimento de cada elemento, do conjunto que está supostamente contido, no conjunto que supostamente contém o outro conjunto.
        - Para o conjunto X, usaremos Bhaskara para, a partir da regra de formação do conjunto, identificar os elementos deste conjunto.
        - Verificamos os pertencimentos dos elementos, para cada relação de "estar contido", depois de ter definido seus elementos.
        - Se as duas relações de "estar contido" tiverem valor booleano verdadeiro, a relação de igualdade será verdadeira.
    - Planejamento terminado.
    ```python
    a = {1, 3}
    b = set(range(1,4))
    a_eh_subset_of_b = a.issubset(b)
    b_eh_subset_of_a = b.issubset(a) # or A.issuperset(B)
    a_equal_b = a_eh_subset_of_b and b_eh_subset_of_a # True
    c = {1, 3}
    d = set(range(1,7))
    c_eh_subset_of_d = c.issubset(d)
    d_eh_subset_of_c = d.issubset(c) # or C.issuperset(d)
    c_equal_d = c_eh_subset_of_d and d_eh_subset_of_c # False
    ```  

## Intersecção entre Conjuntos
- Sejam X e Y conjuntos definidos em um mesmo universo U.
- Definimos a Intersecção de X e Y como o conjunto $ I = \mathrm X\ \cap Y\ =\ \{i \in U\ |\ i \in X\ e\ i \in Y \}$
- Pergunta: Qual a intersecção entre dois conjuntos?
    ```python
    a = {1, 3}
    b = set(range(1,7))   
    intersection = a.intersection(b) # elements common to a and b
    intersection = a & b             # elements common to a and b
    ```  

## Reunião entre Conjuntos
- Sejam X e Y conjuntos definidos em um mesmo universo U.
- Definimos a Reunião de X e Y como o conjunto $ R = \mathrm X\ \cup Y\ =\ \{r \in U\ |\ r \in X\ ou\ r \in Y \}$
- Pergunta: Qual a união entre dois conjuntos?
    ```python
    a = {1, 3}
    b = set(range(1,7))
    reunion = a.union(b) # elements from both a and b
    reunion = a | b      # elements from both a and b
    ```  

## Complementar de um conjunto em relação a outro conjunto
- Também denominado como **diferença de um conjunto em relação a outro conjunto**.
- Sejam:
    - X e Y conjuntos definidos em um mesmo universo U.
    - $\mathrm X \subset Y$
- Definimos o complementar de X em relação a Y como o conjunto:
    - $C = \mathrm Y\ \setminus X\ =\ \{c \in U\ |\ c \in Y\ e\ c \not\in X \}$
    - Deve-se ter atenção na ordem. Se lê complementar de X em relação a Y, mas usa-se a notação  $\mathrm Y\ \setminus X$.
        - Pode-se também ler da esquerda para direita com o nome do operador:$ \mathrm Y\ menos\ \mathrm X $.
- Pergunta: Qual o complementar de um conjunto v em relação ao conjunto w?
    ```python
    v = {1, 3}
    w = set(range(1,7))
    complementar_de_v_em_relacao_a_w = w.difference(v) # elements in a but not in b
    complementar_de_v_em_relacao_a_w = w - v           # elements in a but not in b
    w_minus_v = w - v
    diferenca_de_v_em_relacao_a_w = w - v
    ```  

## Complementar em relação ao Conjunto Universo
- Não é necessário indicar o nome do conjunto universo.
- Sejam:
    - X um conjunto definido em um universo U.
    - $\mathrm X \subset U$
- Definimos o complementar de X em relação a U como o conjunto:
    - $\mathrm X^c =\ \{c \in U\ |\ c \not\in X \}$
- Pergunta: Qual o complementar de um conjunto v?
    ```python
    v = {1, 3}
    u = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
    complementar_de_v_em_relacao_a_u = w.difference(u) # elements in u but not in w
    ```  

## Diferença Simétrica entre 2 conjuntos
- Seja A e B conjuntos definidos em um universo U.
- A diferença simétrica de A e B é um conjunto que contém os elementos que pertencem a A ou a B, mas não a ambos.
    - A diferença simétrica não usa o conceito do operador "menos". 
    - A diferença simétrica usa o conceitos do elementos pertencer a apenas um dos conjutnso mas não aos dois.
    - No diagrama de Venn, a diferença simétrica representa o conjunto que possue os elementos que não se encontram na interseção dos conjuntos, mas que pertencem a exclusivamente a um conjunto ou ao outro conjunto.
    - Definimos a Diferença Simétrica entre A e B como o conjunto $\mathrm A\ \varDelta \ \mathrm B\ =\ \{ \ \{A \cup B\} \setminus \{A \cap B\} \ \}$
    ```python
    a = {1, 3}
    b = set(range(1,7))
    symmetric_difference = b.symmetric_difference(a) # elements in either s or t but not both
    ```  

## Produto Cartesiano entre dois Conjuntos
- Seja A e B conjuntos definidos em um universo U.
- O produto cartesiano de  $A \ \times \ B$ é o conjunto de todos os pares ordenados (a, b) , onde  $a \in A \ e \ b \in B $.
- Definição: 
    - $ A \times B = \{(a, b) \mid a \in A \text{ e } b \in B\} $
- Para identificar os pares ordenados, deve considerar a formação de pares, pegando para cada elemento de A na primeira posição, todos os elementos de B na segunda posição.

## Adição de Elementos em um Conjunto
- Seja A e B conjuntos definidos em um universo U.
- Seja B = \{c, d, e\}
- Se temos um conjunto A e queremos criar um novo conjunto X que contém todos os elementos de A e mais os elemento(s) c, d, e, executamos a operação:
    - $ X = A \cup \{c, d, e\} $
        - Onde  c, e, e são o elemento que queremos adicionar.
    ```python
    a = {1, 3}
    b = {4}
    a.update(b) # {1, 3, 4}
    print(a)
    a = {1, 3}
    a |= b # {1, 3, 4}
    print(a)
    a = {1, 3}
    a.add(4) # {1, 3, 4}
    print(a)
    ```

## Subração de Elementos de um Conjunto
- Seja A e B conjuntos definidos em um universo U.
- Seja B = \{c, d, e\}
- Se temos um conjunto A e queremos criar um novo conjunto X que contém todos os elementos de A mas sem os elemento(s) c, d, e, executamos a operação:
    - $ X = A \ \setminus \{c, d, e\} $
        - Onde  c, e, e são o elemento que queremos remover.
    ```python
    a = {1, 3}
    b = {3}
    a.symmetric_difference_update(b)
    print(a) # {1}
    a = {1, 3}
    a -= b
    print(a) # {1}
    a = {1, 3}
    a.discard(3)
    print(a) # {1}
    a = {1, 3}
    a.remove(3) # raises KeyError if not present
    print(a) # {1}
    a = {1, 3}
    ```
