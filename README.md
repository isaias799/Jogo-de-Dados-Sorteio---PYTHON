# Jogo-de-Dados-Sorteio---PYTHON

from random import  randint
from time import sleep
from operator import itemgetter
jogo = {'jogador1':randint(1,6),#AQUI É O  DICIONÁRIO...
        'jogador2':randint(1,6),
        'jogador3':randint(1,6),
        'jogador4':randint(1,6)}

ranking = list()#NESTA LINHA SERÁ SORTEADO OS NUMEROS DE 0 A 6...
print('  == VALORES SORTEADOS ==')
for k, v in jogo.items():#aQUI SERÁ LISTADO OS NÚMEROS SORTEADOS ENTRE JOGADORES
    print(f'{k} tirou {v} no dado.')
    sleep(1)
ranking = sorted(jogo.items(), key=itemgetter(1), reverse=True)
print('-=-'* 15)
print('  == RANKING DOS JOGADORES ==')
for i, v in enumerate(ranking):#AQUI SERÁ ENUMERADO OS VALORES DE 1 A 6
    print(f'{i+1}º lugar: {v[0]} com {v[1]}.')
    sleep(1)#ATRASO DE 1 SEGUNDO
