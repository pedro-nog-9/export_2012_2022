# export_2012_2022

## Análise da série temporal das exportações brasileiras mês a mês de 2012 a 2022

Fonte: https://www.gov.br/produtividade-e-comercio-exterior/pt-br/assuntos/comercio-exterior/estatisticas/base-de-dados-bruta

## Leitura e decomposição dos dados tratados

O arquivo 'serie_2012_2022.csv' foi compilado de todas as exportações do período disponível separadamente por ano no portal do ministério da aconomia. A decomposição se deu nas tabelas: 'Aumento', 'Aceleração' e 'Média Móvel' e a soma acumulada dos meses em cada ano em US$ Bilhões.

![1](https://user-images.githubusercontent.com/127139232/229600072-57fa5a9d-6493-49df-a79e-f607d223d7ef.png)

## Análise dos meses

O DataFrame a seguir mostra o desempenho médio de cada mês através da função .groupby() em ordem decresente do valor médio exportado por mês. Percebe-se que os meses com a maior média são os meses do meio do ano, enquanto os meses do início e do fim do ano apresentam os menores desempenhos

![2](https://user-images.githubusercontent.com/127139232/229600210-1444c15e-ee7f-45fa-a796-7ea1cd77d5ad.png)

## Gráficos da Série Temporal em Meses x US$ Bilhões

Para ficar mais evidente, o gráfico de desempenho mensal no intervalo 2012-2022:

![3](https://user-images.githubusercontent.com/127139232/229600281-e5fa1279-bd5c-4ac9-830d-4d503bd5d4d0.png)

Para uma melhor visualiazação, o gráfico com ruído suavizado pela média móvel de 3 meses:

![4](https://user-images.githubusercontent.com/127139232/229600324-c0a07aea-fffe-4963-864f-360c13f8661c.png)

Autocorrelação:

![5](https://user-images.githubusercontent.com/127139232/229600374-d0392640-3529-417a-bba1-8f1bf583030a.png)

# Conclusão

É esperado que séries temporais de teor econômico/financeiro apresentem alguma sazonalidade, em alguns casos, porém, a visualização não é tão nítida como nesse caso das exportações e é preciso fazer uma análise mais complexa com a transformada de fourier, que chamamos de análise espectral. Nesse caso mostrado acima, a explicação está no período de safra e entresafra das commodities agrículas brasileiras, que compõe a maior parte dos produtos exportados.

