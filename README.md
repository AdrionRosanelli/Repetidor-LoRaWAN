# Repetidor-LoRaWAN
Simulador de um repetidor em uma rede LoRaWAN baseado no trabalho de [1].

## Procedimentos para execução

"""
 SYNOPSIS:
 
    ./LoRaWAN.py <nodes> <avgsend> <datasize> <collision> <randomseed>
 
 DESCRIPTION:
 
    nodes:
        number of nodes to simulate
    avgsend:
        average sending interval in seconds
    datasize:
        Size of data that each device sends in bytes
    collision:
        0   simplified check. Two packets collide when they arrive at the same time, on the same frequency and SF
        1   considers the capture effect
        2   consider the Non-orthognality SFs effect and capture effect
    randomseed:
        random seed
 
 OUTPUT:
    The result of every simulation run will be appended to a file named expX.dat,
    whereby X is the experiment number. The file contains a space separated table
    of values for nodes, collisions, transmissions and total energy spent. The
    data file can be easily plotted using e.g. gnuplot.
"""
 
Essa descrição é valida para todas as versões dos códigos. Onde o código deve ser executado com seus parametros:
 
      ./LoRaWAN.py <nodes> <avgsend> <datasize> <collision> <randomseed>
  
EXEMPLO: pode-se executar o código com o seguinte comando:
 
        " run LoRaWAN_v3.py 100 300 200 2 10 "  
 
  Para rodar a versão 3 da simulação com 100 nós, 300 segundos de intervalo de envio, 200 bytes de dados, colisão considerando não-ortogonalidade dos SFs
 e o efeito de captura, e com uma semente aleatória igual a 10.  

[1] ABDELFADEEL, K. Q. et al. FREE - Fine-Grained Scheduling for Reliable and Energy-Efficient Data Collection in LoRaWAN.IEEE Internet of Things Journal, IEEE, v. 7, n. 1, p. 669–683,2020.
