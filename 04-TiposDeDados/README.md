## Desafio 4

**Python** – dinamicamente tipada

x = 10     	# x é inteiro
x = "dez"  	# Agora x é string – permitido
print(x + 5)   # Erro em tempo de execução: TypeError

**Comentários:**
- Python permite reatribuir variáveis com tipos diferentes.
- Erros de tipo só aparecem durante a execução.
- Forte tipagem: não permite, por exemplo, somar string com número sem conversão.

**Java** – estaticamente e fortemente tipada

int x = 10;
x = "dez"; 	// Erro de compilação: tipos incompatíveis
System.out.println(x + 5);  // Funciona, imprime 15

**Comentários:**
- Tipos são verificados na compilação.
- O tipo de x é declarado explicitamente.
- Trocar de tipo exige casting ou outro tipo de variável.
- Forte: não faz coerções automáticas como JavaScript faria.

**TypeScript** – estaticamente tipada com suporte a inferência

let x = 10; 	// Inferido como número
x = "dez";  	// Erro de compilação: tipo 'string' não é atribuível a 'number'
console.log(x + 5);  // Funciona se x for número

**Comentários:**
- Tipos são verificados em tempo de compilação.
- Tipagem é estática, mas pode ser inferida.
- Você pode optar por não tipar (usando any), o que torna o código mais flexível, porém menos seguro.

