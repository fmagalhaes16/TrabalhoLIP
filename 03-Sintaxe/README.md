## Desafio 3

**Mini-Gramática da Linguagem Luni (simplificada)**

**Alfabeto e Caracteres Permitidos:**
Letras: a - z | A - Z
Dígitos: 0 - 9
Símbolos Especiais: +, -, *, /, =, :, ;, (, ), {, }, “
Espaços e quebras de linhas são usados para separar tokens

**Categorias Gramaticais:**
  Categoria        Exemplos                         Padrão/Descrição

  IDENT            sol, raio                 Pode conter n° depois da 1° letra
  NUM               124, 3.3                       Inteiros ou Decimais 
  STR               “claro”                    Cadeias de textos entre aspas
  KEYWORD          se, entao                       Palavras reservadas
  OP                +, =, *                  Op. Aritméticos ou de Atribuição
  DELIM             (, ), {                      Delimitadores Sintáticos 
  END                 ;                             Final de Comando

**Palavras Chaves da Linguagem Luni:**

SE - condiconal;
ENTAO - consequência;
MOSTRAR - imprime um valor;
FAZER - início de bloco;
FIM - fim de bloco;
ENQUANTO - laço de repetição.

**Estrutura de Comando:**

programa ::= comando+
comando  ::= atribuicao | condicional | repeticao | exibicao

atribuicao ::= IDENT "=" expressao ";"
condicional ::= "se" expressao "entao" comando
repeticao ::= "enquanto" expressao "fazer" bloco "fim"
exibicao ::= "mostrar" expressao ";"

expressao ::= NUM | STR | IDENT | expressao OP expressao
bloco ::= "{" comando+ "}"

**Exemplo:**

- Luni: 
luz = 10;
- CSS: 
[IDENT('luz'), OP('='), NUM('10'), END(';')]

