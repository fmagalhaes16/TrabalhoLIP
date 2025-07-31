## Desafio 2

1. Compilador:
Traduz todo o código-fonte para código de máquina nativo, antes de executar o código.


- Exemplo: gcc (para C/C++) transforma um arquivo .c em um .exe no Windows.


- Vantagem: Alta performance.


- Desvantagem: Menor portabilidade.

2. Interpretador:
Lê e executa o código fonte linha por linha, em tempo real de execução.


- Exemplo: python ou bash.


- Vantagem: Fácil de testar e debugar.


- Desvantagem: Mais lento, pois interpreta toda vez.

3. Compilador para Bytecode + Máquina Virtual:
O código-fonte é compilado para bytecode, que é executado por uma máquina virtual (VM).


- Exemplo:


Java → javac gera .class → executado pela JVM.


C# → compilado para IL → executado pela .NET CLR.


- Vantagem: Portabilidade entre sistemas operacionais.


- Desvantagem: Pode ter overhead da VM.

