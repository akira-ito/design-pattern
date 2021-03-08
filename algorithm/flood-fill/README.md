# Flood Fill

Algoritmo para acessar uma área com o mesmo valor em uma matrix 2D. As direções vizinhas podem serem acessadas de 4 posições (N, S, W, E) ou 8 posições (N, S, W, E, NW, NE, SW, SE). Dado a posição inicial da linha e coluna, o seu valor será trocado com o novo valor escolhido, ao termino será retornada uma nova matrix com os valores acessadas.
É muito utilizada no software Paint para pintar areas de mesma cor e tambem para descobrir qual das ilhas é maior em uma matrix.

## Soluções
- Recursividade;
- BFS (Breadth First Search).

## Exemplo
Trocar por H na posição da linha 0 e coluna 3. 
> Line = 0, Column = 0, Target = O, Value = H, N = 5, M = 4;

    [
        [   X   X   O   O   ]
        [   X   X   X   O   ]
        [   X   X   X   O   ]
        [   O   O   X   O   ]
        [   O   O   O   O   ]
    ]

Resultado:

    [
        [   X   X   H   H   ]
        [   X   X   X   H   ]
        [   X   X   X   H   ]
        [   H   H   X   H   ]
        [   H   H   H   H   ]
    ]

## Complexidade
    O(NxM): Linha(N) por Coluna(M)
