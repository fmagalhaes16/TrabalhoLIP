## Desafio 6

**Python**

- PASSAGEM POR VALOR:

def modificar_valor(x):
	print(f"Antes da modificação: x = {x}")
	x = x + 10
	print(f"Depois da modificação: x = {x}")
    a = 5

modificar_valor(a)
print(f"Valor de 'a' fora da função: {a}")

- PASSAGEM POR REFERÊNCIA:

def modificar_lista(lst):
	print(f"Antes da modificação: {lst}")
	lst.append(99)
	print(f"Depois da modificação: {lst}")

minha_lista = [1, 2, 3]
modificar_lista(minha_lista)
print(f"Lista fora da função: {minha_lista}")

**C**

- PASSAGEM POR VALOR:

#include <stdio.h>

void modificarValor(int x) {
	printf("Antes: x = %d\n", x);
	x = x + 10;
	printf("Depois: x = %d\n", x);
}
int main() {
	int a = 5;
	modificarValor(a);
	printf("Valor de 'a' fora da função: %d\n", a);
	return 0;
}

- PASSAGEM POR REFERÊNCIA: 

#include <stdio.h>

void modificarReferencia(int *x) {
	printf("Antes: *x = %d\n", *x);
	*x = *x + 10;
	printf("Depois: *x = %d\n", *x);
}

int main() {
	int a = 5;
	modificarReferencia(&a);
	printf("Valor de 'a' fora da função: %d\n", a);
	return 0;
}

