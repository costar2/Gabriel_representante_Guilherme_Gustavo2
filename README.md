# Gabriel_Guilherme_representante_Gustavo2

Monitoramento de consumo de Energia Sustentável
Este projeto visa monitorar e otimizar o consumo de energia limpa em uma comuinidade, verificando se as metas de consumo sustentável estão sendo cumpridas.

#funcionalidade

Entrada de dados de consumo diário

Verificação de cumprimento da meta de consumo

Cálculo de média, maior e menor consumo

Relatório de desempenho diário

#Como Executar

Ter o Python instalado
Executar o arquivo '.py' no terminal com o comando 'python nome_do_arquivo.py'
Programa para monitorar e otimizar o consumo de energia limpa
Definindo a meta diária de consumo sustentável
META_DIARIA = 150

Entrada de dados
n = int(input("Insira a quantidade de dias: ")) # Quantidade de dias dias_cumpriram_meta = 0 soma_consumo = 0 maior_consumo = None menor_consumo = None

for dia in range(1, n + 1): consumo = int(input(f"Insira o consumo do dia {dia}: "))

# Verificar se o dia cumpriu a meta
if consumo >= META_DIARIA:
    dias_cumpriram_meta += 1

# Atualizar soma para cálculo da média
soma_consumo += consumo

# Atualizar maior e menor consumo
if maior_consumo is None or consumo > maior_consumo:
    maior_consumo = consumo
if menor_consumo is None or consumo < menor_consumo:
    menor_consumo = consumo
Cálculo da média de consumo
media_consumo = soma_consumo / n

# Relatório de resultados
if dias_cumpriram_meta == n:
    print("Parabéns! Todos os dias cumpriram a meta de consumo sustentável.")
elif dias_cumpriram_meta == 0:
    print("Infelizmente, nenhum dia cumpriu a meta de consumo sustentável.")
else:
    dias_nao_cumpriram_meta = n - dias_cumpriram_meta
    print(f"{dias_cumpriram_meta} dias cumpriram a meta e {dias_nao_cumpriram_meta} dias não cumpriram a meta.")

print(f"A média de consumo foi de {media_consumo:.2f} kWh. "
      f"O maior consumo foi de {maior_consumo} kWh e o menor consumo foi de {menor_consumo} kWh.")
