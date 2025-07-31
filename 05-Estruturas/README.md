## Desafio 5

**Jogo de Adivinhação com Dicas**

O usuário tem que adivinhar um número de 0 a 100, ele irá receber dicas se o número está mais alto ou mais baixo, o usuário terá um número limitado de tentativas.
```
import random
print(" Bem-vindo ao Jogo da Adivinhação!")
print("Tente adivinhar o número secreto entre 1 e 100.")
numero_secreto = random.randint(1, 100)
tentativas_restantes = 7
while tentativas_restantes > 0:
	try:
    	chute = int(input(f"\nVocê tem {tentativas_restantes} tentativa(s). Digite seu palpite: "))
    	if chute < 1 or chute > 100:
        	print(" Por favor, digite um número entre 1 e 100.")
        	continue 
        	if chute == numero_secreto:
        	print("Parabéns! Você acertou o número!")
        	break 
    	elif chute < numero_secreto:
        	print("Dica: O número secreto é MAIOR.")
    	else:
        	print("Dica: O número secreto é MENOR.")
    	tentativas_restantes -= 1
	except ValueError:
    	print("Entrada inválida! Digite apenas números inteiros.")
if tentativas_restantes == 0:
	print("\n Fim de jogo! O número secreto era {numero_secreto}. Tente novamente!")
´´´
