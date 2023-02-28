# Faturamento diario
import pandas as pd

tabela_vendas = pd.read_excel('dados.xlsx')
print(tabela_vendas)

nmin = min(tabela_vendas['valor'])
print(f'O menor valor de faturamento doi de {nmin}')

nmax = max(tabela_vendas['valor'])
print(f'O maior valor de faturamento foi de {nmax}')

media = sum(tabela_vendas['valor'])/ len(tabela_vendas['valor'])
print(f'A média de vendas foi de {media:.4f}')

c = 0
for lista in tabela_vendas['valor']:
    if lista > media:
        c+=1
print(f'O número de dias no mês em que o valor do faturamento diário foi superior à média mensal foi de {c} dias.')
