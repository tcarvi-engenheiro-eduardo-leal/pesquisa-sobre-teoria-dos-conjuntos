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

### Exemplo de descrição de Conjunto:
- $\mathrm X\ =\ \{x\ \in \mathbb R\ \mathrm |\ x^2\ -\ 2x\ -\ 3\ =\ 0 \}$
- Quais elementos formam o conjunto X? 
    - Avalio a propriedade: $\mathrm x^2\ -\ 2x\ -\ 3\ =\ 0$  
        - Devido fórmula de Bhaskara:  $\mathrm x\ =\ \frac{-\ b\ \pm \sqrt[2]{b^2 - 4 a c}}{2\ a}$, os valores possíveis de x são -1 e 3.
    - Logo, $\mathrm X\ =\ \{-1,\ 3\}$.  

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
