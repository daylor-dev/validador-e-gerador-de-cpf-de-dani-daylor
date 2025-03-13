# validador-e-gerador-de-cpf-de-dani-daylor
Criei um algoritmo que além de validar um cpf, também gera 100 cpfs diferentes. Código gerado com o VScode através da linguagem Python 
#gerar 100 CPFs


import random #importar biblioteca random que gera valores aleatórios

for _ in range(100):
    cpf_zeroanove = ''
    for n in range(9):            
        cpf_zeroanove += str(random.randint(0,9))




    contador_regressivo_1 = 10
    resultado_digito_1 = 0
    for digito in cpf_zeroanove: 
        resultado_digito_1 += int(digito) * contador_regressivo_1 
        contador_regressivo_1 -= 1

    digito_1 = (resultado_digito_1 * 10) % 11
    digito_1 = digito_1 if digito_1 <= 9 else 0 


    digito_1 = digito_1 if digito_1 <= 9 else 0 

    cpf_zeroadez = cpf_zeroanove + str(digito_1) #5263112483
    contador_regressivo_2 = 11

    resultado_digito_2 = 0 

    for digito in cpf_zeroadez:
        resultado_digito_2 += int(digito) * contador_regressivo_2
        contador_regressivo_2 -= 1
    digito_2 = (resultado_digito_2 * 10) % 11



    digito_2 = digito_2 if digito_2 <= 9 else 0 

    cpf_gerado =  f'{cpf_zeroanove}{digito_1}{digito_2}'
    print(cpf_gerado)
