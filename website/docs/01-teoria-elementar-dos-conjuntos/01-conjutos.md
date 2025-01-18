# Conjuntos

## Definição:
- Coleção de elementos.
- Cada elemento contido em um conjunto é uma única entidade (distinta das demais).
- Os elementos de um conjunto não possuem uma ordem específica.

## Conjuntos Numéricos: 
- Números naturais: 
    - $\mathbb N $
- Números inteiros:
    - $\mathbb Z $
- Números racionais:
    - $\mathbb Q $
- Números irracionais:
    - $\mathbb I $
- Números reais:
    - $\mathbb R $
- Números complexos:
    - $\mathbb C $

## Representação de Conjuntos:
- Listagem de elementos: 
    - $\mathrm X = \{ 1, 2, 3, 4, 5, 6 \}$  
    - Python:  
    ```python
    X = {1, 2, 3, 4, 5, 6}
    ```
- Listagem de elementos com acréscimo de reticências para omitir sequência óbvia: 
    - $\mathrm X = \{ 1, 2, 3, ..., 6 \}$  
    - Python:  
    ```python
    X = set(range(1,7))
    ```
- Indicação de regras de pertencimento para seus elementos:
    - $\mathrm X = \{ x\ :\ x\ é\ um\ inteiro\ positivo\ não\ nulo\ menor\ que\ 7 \}$
    - $\mathrm X = \{ x\ |\ x\ é\ um\ inteiro\ positivo\ não\ nulo\ menor\ que\ 7 \}$  
    - Python:  
    ```python
    X = {element for element in range(1,7)}
    X = {element for element in range(1,7) if element < 7}
    X = {element + 0 for element in range(1,7) if element < 7}
    ```  

## Definição Ingênua (não formal) de Conjunto
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ P(x)\ \}$ é um conjunto.
    - Tendo considerado:
        - x := um elemento.
        - $\mathbb R$ := o conjunto Universo ao qual o elemento x pertence.
        - e $\mathrm P(x)$ := uma propriedade que descreve o elemento $\mathrm x$ e tem valor booleano verdadeiro.
    - Sendo esta a definição de conjunto, também são válidas as afirmações:
        1. Se $\mathrm x$ satisfaz a propriedade $\mathrm P(x)$, isto é, se $\mathrm P(x)$ é uma proposição verdadeira, escrevemos $\mathrm x\ \in X$ e dizemos que x pertence a X. 
        2. Se $\mathrm x$ não satisfaz a propriedade $\mathrm P(x)$, isto é, se $\mathrm P(x)$ é uma proposição falsa, escrevemos $\mathrm x\ \notin X$ e dizemos que x não pertence a X.

### Exemplo de descrição de conjunto:
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ x^2\ -\ 2x\ -\ 3\ =\ 0 \}$
- Quais elementos formam o conjunto X? 
    - Avalio a propriedade: $\mathrm x^2\ -\ 2x\ -\ 3\ =\ 0$  
        - Devido fórmula de Bhaskara:  $\mathrm x\ =\ \frac{-\ b\ \pm \sqrt[2]{b^2 - 4 a c}}{2\ a}$, os valores possíveis de x são -1 e 3.
    - Logo, $\mathrm X\ =\ \{-1,\ 3\}$.  

## Definição de Pertencimento
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

## Definição de Não Pertencimento
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

## Definição de Inclusão
- Sejam X e Y conjuntos. 
- Dizemos que X está contido em Y e escrevemos $\mathrm X \subset Y$, se todo elemento de X é um elemento de Y. Caso X não esteja contido em Y, escrevemos $\mathrm X \not\subset Y$.
- Dizer que X não está contido em Y significa que existe pelo menos um elemento de X que não é elemento de Y.
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

## Definição de Igualdade
- Sejam X e Y dois conjuntos com o mesmo universo. Dizemos que X é igual a Y caso $\mathrm X \subset Y$ e $\mathrm Y \subset X$. Neste caso escrevemos $\mathrm X = Y$.
- X é igual a Y se e somente se estes conjuntos possuem os mesmos elementos.
- Por definição, para demonstrar que um conjunto X é igual a um conjunto Y, devemos verificar duas inclusões: $\mathrm X \subset Y$ e $\mathrm Y \subset X$.

## Como demostrar a igualdade de conjuntos?
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ x^2\ -\ 2x\ -\ 3\ =\ 0 \}$
- $\mathrm Y = \{-2, 1\}$
- Demostre que X = Y.
- Planejamento da demostração:
    - Primeiro: Qual a definição da igualdade?
        - Deve-se indicar na demonstração a definição de igualdade.
        - Por definição, para que X = Y, deve ser válida a hipótese $\mathrm X \subset Y$ e a hipótese $\mathrm Y \subset X$.
    - Então, dividimos a demostração em duas verificações de inclusão. As duas devem ser verdadeiras.
        - Para verificar cada relação de inclusão, por sua vez, devemos verificar a relação de pertencimento de cada elemento do conjunto que está supostamente contido, no conjunto que supostamente deve conter o outro conjunto.
        - Para o conjunto X, usaremos Bhaskara para, a partir da regra de formação do conjunto, identificar os elementos deste conjunto.
        - Verificamos os dois pertencimentos, depois de ter definido seus elementos.
    - Planejamento terminado.
        - A base da demostração é saber a definição matemática da igualdade. E saber que devemos verificar dois pertencimentos, devido esta definição.
    ```python
    a = {1, 3}
    b = set(range(1,7))
    a_eh_subset_of_b = a.issubset(b)
    b_eh_subset_of_a = b.issubset(a) # or A.issuperset(B)
    a_equal_b = a_eh_subset_of_b and b_eh_subset_of_a # False
    ```  

## Definição da Intersecção
- Sejam X e Y conjuntos definidos em um mesmo universo U.
- Definimos a Intersecção de X e Y como o conjunto $ I = \mathrm X\ \cap Y\ =\ \{i \in U\ |\ i \in X\ e\ i \in Y \}$
- Pergunta: Qual a intersecção entre dois conjuntos?
    ```python
    a = {1, 3}
    b = set(range(1,7))   
    intersection = a.intersection(b) # elements common to a and b
    intersection = a & b             # elements common to a and b
    ```  

## Definição da Reunião
- Sejam X e Y conjuntos definidos em um mesmo universo U.
- Definimos a Reunião de X e Y como o conjunto $ R = \mathrm X\ \cup Y\ =\ \{r \in U\ |\ r \in X\ ou\ r \in Y \}$
- Pergunta: Qual a união entre dois conjuntos?
    ```python
    a = {1, 3}
    b = set(range(1,7))
    reunion = a.union(b) # elements from both a and b
    reunion = a | b      # elements from both a and b
    ```  

## Definição de Complementar de um conjunto em relação a outro conjunto
- Sejam:
    - X e Y conjuntos definidos em um mesmo universo U.
    - $\mathrm X \subset Y$
- Definimos o complementar de X em relação a Y como o conjunto $C = \mathrm Y\ \setminus X\ =\ \{c \in U\ |\ c \in Y\ e\ c \not\in X \}$
    - Deve-se ter atenção na ordem. Se lê complementar de X em relação a Y, mas usa-se a notação  $\mathrm Y\ \setminus X$.
- Pergunta: Qual o complementar de um conjunto A em relação ao conjunto B?
    ```python
    v = {1, 3}
    w = set(range(1,7))
    complementar_de_v_em_relacao_a_w = w.difference(v) # elements in a but not in b
    complementar_de_v_em_relacao_a_w = w - v           # elements in a but not in b
    w_minus_v = w - v
    diferenca_de_v_em_relacao_a_w = w - v
    ```  

## Definição de Diferença Simétria entre 2 conjuntos
- Seja X um conjuntos definido em um universo U.
- Definimos o complementar de X como o conjunto $\mathrm X^c =\ \{c \in U\ |\ c \not\in X \}$
    ```python
    a = {1, 3}
    b = set(range(1,7))
    symmetric_difference = b.symmetric_difference(a) # elements in either s or t but not both
    ```  

## Definição de Diferença Simétrica de 2 conjunto
- Seja X um conjuntos definido em um universo U.
- Definimos o complementar de X como o conjunto $\mathrm X^c =\ \{c \in U\ |\ c \not\in X \}$
- Pergunta: Quais elementos existem em algum dos conjuntos, mas não existem nos dois ao mesmo tempo?
    ```python
    a = {1, 3}
    b = set(range(1,7))
    new_set = a.symmetric_difference(b) # {2, 4, 5, 6, 7 } # new set with elements in either s or t but not both
    ```  

## Cardinalidade de Conjuntos
- Quantidade de elementos que pertencem a um conjunto.
- Símbolo:
	- $ \text{card(A)} $
	- $ o(A) $
	- $ n(A) $
		- sendo:
			- $ A $ := um conjunto qualquer
    ```python
    a = {1, 3}
    cardinalidade_de_a = len(a) # 2
    ```  


```python
a = {1, 3}

s.update(t)

s |= t

return set s with elements added from t

s.intersection_update(t)

s &= t

return set s keeping only elements also found in t

s.difference_update(t)

s -= t

return set s after removing elements found in t

s.symmetric_difference_update(t)

s ^= t

return set s with elements from s or t but not both

s.add(x)

add element x to set s

s.remove(x)

remove x from set s; raises KeyError if not present

s.discard(x)

removes x from set s if present

s.pop()

remove and return an arbitrary element from s; raises KeyError if empty

```  
