import json

faturamento_diario = """
{
    "faturamento": [0, 22174.1664, 24537.6698, 0, 0, 26139.6134, 0, 0, 26742.6612, 0, 42889.2258, 0, 11191.4722, 0, 0, 0, 3847.4823, 3737.223, 0, 0, 24681.6818, 0, 0, 0, 45281.6436, 0, 0, 0, 58622.5897, 0]
}
"""

dados = json.loads(faturamento_diario)["faturamento"]

faturamento_filtrado = [dia for dia in dados if dia > 0]

menor_valor = min(faturamento_filtrado)
maior_valor = max(faturamento_filtrado)
media_mensal = sum(faturamento_filtrado) / len(faturamento_filtrado)

dias_acima_media = sum(1 for dia in faturamento_filtrado if dia > media_mensal)

print(f"Menor valor de faturamento: R$ {menor_valor:.2f}")
print(f"Maior valor de faturamento: R$ {maior_valor:.2f}")
print(f"Número de dias com faturamento acima da média: {dias_acima_media}")
