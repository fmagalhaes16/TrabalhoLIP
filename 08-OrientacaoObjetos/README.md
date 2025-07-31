## Desafio 8

class Transporte:
	def __init__(self, nome, capacidade):
    	self.nome = nome
    	self.capacidade = capacidade  # número de passageiros
	def mover(self):
    	print(f"{self.nome} está se movendo...")

	def info(self):
    	print(f"{self.nome} transporta até {self.capacidade} pessoas.")

class Terrestre(Transporte):
	def __init__(self, nome, capacidade, rodas):
    	super().__init__(nome, capacidade)
    	self.rodas = rodas

	def info(self):
    	super().info()
    	print(f"É um transporte terrestre com {self.rodas} rodas.")

class Aquatico(Transporte):
	def mover(self):
    	print(f"{self.nome} está navegando na água...")
class Aereo(Transporte):
	def mover(self):
    	print(f"{self.nome} está voando pelos céus...")

class Carro(Terrestre):
	def __init__(self, nome):
    	super().__init__(nome, capacidade=5, rodas=4)

class Moto(Terrestre):
	def __init__(self, nome):
    	super().__init__(nome, capacidade=2, rodas=2)

