## Desafio 11

from functools import reduce

def achatar(lista):
	if not lista:
    	return []
	if isinstance(lista[0], list):
    	return achatar(lista[0]) + achatar(lista[1:])
	else:
    	return [lista[0]] + achatar(lista[1:])

def soma_pares(lista_aninhada):

	lista_achatada = achatar(lista_aninhada)
    
	pares = list(filter(lambda x: x % 2 == 0, lista_achatada))

	return reduce(lambda acc, x: acc + x, pares, 0)



exemplo = [1, [2, 3], [4, [5, 6, [7, 8]]], 9]
resultado = soma_pares(exemplo)
print("Soma dos números pares: {resultado}")

