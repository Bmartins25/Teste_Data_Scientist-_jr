# Teste_Data_Scientist_jr

---

Assuma que se deseja prever a soma do número de diárias de carros a serem vendidas nos próximos 7 dias em cada agência, em função do preço médio a ser arbitrado para cada tipo de carro em cada agência.

 

Os dados históricos de vendas estão em um arquivo CSV (ou em uma tabela SQL) com as seguintes colunas e respectivos dados em cada linha, onde cada linha corresponde a uma venda:

 

- COD_AG: código da agência

- NUM_NOTA: número da nota fiscal

- DATA: data correspondente à venda

- COD_TIPO_CARRO: código do tipo de carro que foi alugado

- NUM_DIARIAS: número de diárias vendidas

- VALOR: valor total da nota fiscal


 ----

 

Note que:

 

Múltiplas vendas do mesmo tipo de carro podem ocorrer no mesmo dia e na mesma agência, cada uma com preço potencialmente diferente.

O preço unitário de uma diária em uma venda pode ser calculado pela divisão VALOR/NUM_DIARIAS.

A DATA pode ser assumida como um número inteiro entre 1 e 7000, onde esse número corresponde ao número de dias desde o início da operação da empresa.

Você pode assumir que há aluguel de todos os tipos de carros em todas as agências ao longo de todos os dias do histórico.

 ----
 

 Exercícios:

 

 Escreva o código (usando SQL; Python com Pandas ou Spark; ou R) correspondente à preparação do seguinte dataframe (ou tabela SQL) para a criação de um modelo preditivo:
 

 

- DATA_REF: data de referência (i.e. valores correspondem a 7 dias a partir dessa data)

- COD_AG: código da agência

- COD_TIPO_CARRO: código do tipo de carro

- PRECO_MEDIO: preço médio ponderado por número de diárias do tipo de carro no período de referência e na agência

- DELTA_PRECO_MEDIO: variação percentual do preço médio ponderado entre semana anterior (entre DATA_REF-7dias e DATA_REF-1 dia, incluindo os limites) e semana atual (entre DATA_REF e DATA_REF+6 dias, incluindo os limites)

- NUM_DIARIAS_SEMANA_ANTERIOR: número total de diárias vendidas na semana anterior (entre DATA_REF-7dias e DATA_REF-1 dia, incluindo os limites)

- NUM_DIARIAS_SEMANA: número total de diárias vendidas na semana atual (entre DATA_REF e DATA_REF+6 dias, incluindo os limites)


 
 Proponha conjunto de “features” adicionais que possam ajudar na previsão futura, a serem adicionadas no dataframe. Note que há uma infinidade de “features” que podem ser úteis ao se agregar as vendas por semana e ao se considerar o histórico.
 

 
 Explique como faria o treinamento e o teste do modelo.
