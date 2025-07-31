## Desafio 7


def fatorial(n):
	if n == 0:
    	return 1
	else:
    	return n * fatorial(n - 1)

print(fatorial(3))

A função fatorial(n) chama a si mesma com n - 1, até que n == 0. A cada chamada, a execução atual é pausada e empilhada até que a base da recursão seja alcançada. Depois, o retorno acontece de cima para baixo (desempilhando), na imagem mostra como acontece.

