# Teoria Elementar dos Conjuntos
## Conjuntos
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
- Descrição de conjuntos por:
    - Listagem de elementos: 
        - $\mathrm X = \{ 1, 2, 3, 4, 5, 6 \}$  
        - Python code:  
        ```python
        X = {1, 2, 3, 4, 5, 6}
        ```
    - Listagem de elementos com acréscimo de reticências para omitir sequência óbvia: 
        - $\mathrm X = \{ 1, 2, 3, ..., 6 \}$  
        - Python code:  
        ```python
        X = set(range(1,7))
        ```
    - Indicação de regras de pertencimento para seus elementos:
        - $\mathrm X = \{ x\ :\ x\ é\ um\ inteiro\ positivo\ não\ nulo\ menor\ que\ 7 \}$
        - $\mathrm X = \{ x\ |\ x\ é\ um\ inteiro\ positivo\ não\ nulo\ menor\ que\ 7 \}$  
        - Python code:  
        ```python
        X = {element for element in range(1,7)}
        X = {element for element in range(1,7) if element < 7}
        X = {element + 0 for element in range(1,7) if element < 7}
        ```  
## Definição Ingênua de Conjunto
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ P(x)\ \}$ é um conjunto.
    - Tendo considerado:
        - x um objeto,
        - $\mathbb R$ o conjunto Universo ao qual o elemento x perctence.
        - e $\mathrm P(x)$ uma propriedade verdadeira que descreve o elemento $\mathrm x$;  
    - Sendo esta a definição de conjunto, também são válidas as afirmações:
        1. Se $\mathrm x$ satisfaz a propriedade $\mathrm P(x)$, isto é, se $\mathrm P(x)$ é uma proposição verdadeira, escrevemos $\mathrm x\ \in X$ e dizemos que x pertence a X. 
        2. Se $\mathrm x$ não satisfaz a propriedade $\mathrm P(x)$, isto é, se $\mathrm P(x)$ é uma proposição falsa, escrevemos $\mathrm x\ \notin X$ e dizemos que x não pertence a X.

### Exemplo de descrição de conjunto:
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ x^2\ -\ 2x\ -\ 3\ =\ 0 \}$
- Quais elementos forma o conjunto X? 
- Avalio a propriedade: $\mathrm x^2\ -\ 2x\ -\ 3\ =\ 0$  
` - Devido fórmula de Bhaskara:  $\mathrm x\ =\ \frac{-\ b\ \pm \sqrt[2]{b^2 - 4 a c}}{2\ a}$, os valores possíveis de x são -1 e 3.  `
- Logo, $\mathrm X\ =\ \{-1,\ 3\}$.  [Q.E.D] quod erat demonstrandum

## Definição de Inclusão
- Sejam X e Y conjuntos. 
- Dizemos que X está contido em Y e escrevemos $\mathrm X \subset Y$, se todo elemento de X é um elemento de Y. Caso X não esteja contido em Y, escrevemos $\mathrm X \not\subset Y$.
- Dizer que X não está contido em Y significa que existe pelo menos um elemento de X que não é elemento de Y.

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
    - Planejamento terminado.

## Definição da Intersecção
- Sejam X e Y conjuntos definidos em um mesmo universo U.
- Definimos A intersecção de X e Y como o conjunto $\mathrm X\ \cap Y\ =\ \{x \in U\ |\ x \in X\ e\ x \in Y \}$

## Definição da Reunião
- Sejam X e Y conjuntos definidos em um mesmo universo U.
- Definimos A reunição de X e Y como o conjunto $\mathrm X\ \cup Y\ =\ \{x \in U\ |\ x \in X\ ou\ x \in Y \}$

## Definição de Complementar de um conjunto em relação a outro conjunto
- Sejam:
    - X e Y conjuntos definidos em um mesmo universo U.
    - $\mathrm X \subset Y$
- Definimos o complementar de X em relação a Y como o conjunto $\mathrm Y\ \setminus X\ =\ \{x \in U\ |\ x \in Y\ e\ x \not\in X \}$
    - Deve-se ter atenção na ordem. Se lê complemetar de X em relação a Y, mas usa-se a notação  $\mathrm Y\ \setminus X$.

## Definição de Complementar de um conjunto
- Seja X um conjuntos definido em um universo U.
- Definimos o complementar de X como o conjunto $\mathrm X^c =\ \{x \in U\ |\ x \not\in X \}$

## Cardinalidade de Conjuntos
- Quantidade de elementos que pertencem a um conjunto.
- Símbolo:
	- $ \text{card(A)} $
	- $ o(A) $
	- $ n(A) $
		- sendo:
			- $ A $ := um conjunto qualquer