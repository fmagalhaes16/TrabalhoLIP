## Desafio 13 


import os
from pathlib import Path
from datetime import datetime, timedelta

PASTA_LOGS = Path("/caminho/para/logs") 
DIAS_LIMITE = 7 

def limpar_logs_antigos(pasta_logs, dias_limite):
	agora = datetime.now()
	limite = agora - timedelta(days=dias_limite)

	if not pasta_logs.exists():
    	print(f" A pasta {pasta_logs} não existe.")
    	return

	arquivos_removidos = 0

	for arquivo in pasta_logs.glob("*.log"):
    	modificado_em = datetime.fromtimestamp(arquivo.stat().st_mtime)
    	if modificado_em < limite:
        	print(f"Removendo: {arquivo} (última modificação: {modificado_em})")
        	arquivo.unlink()
        	arquivos_removidos += 1

	print(f"Total de arquivos removidos: {arquivos_removidos}")

if __name__ == "__main__":
	limpar_logs_antigos(PASTA_LOGS, DIAS_LIMITE)

