# Introdução

Desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas - DIO. Usa-se o SageMaker Canvas [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/) para criar previsões de estoque baseadas em Machine Learning (ML).

Com essa poderosa ferramenta de ML Low Code pode-se:

. Prever a rotatividade de clientes

. Planejar o inventário com eficiência

. Otimizar o preço e a receita

. Melhorar as entregas dentro do prazo

. Classificar texto ou imagens com base em categorias personalizadas

. Identificar objetos e texto em imagens

. Extrair informações de documentos

# Descrição

Criou-se uma conta na AWS, após criou-se um domínio/ usuário no SageMaker Canvas.
Criou-se um modelo de anlálise preditiva de dados, através do dataset "canvas-sample-retail-eletronics-forecasting.csv", para prever a demanda de produtos. Através da target column DEMAND e no Configure model, em Times series configuration, escolheu-se item_id. Clicou-se em Quick build, utilizando 20.000 registros recomendados pelo SageMaker Canvas dos 45.000 registros do dataset, para o treinamento da máquina.

Gerou-se métricas Avg .wQL (Média da Perda Quantil Ponderada), MAPE (Erro percentual absoluto médio), WAPE (Erro Percentual Médio Ponderado), RMSE (Erro Quadrático Médio Raiz), MASE (Erro Médio Escalado Absoluto), os índices devem estar mais próximos de zero para melhor precisão da análise preditiva.

Feita a seleção do dataset (select), construção do modelo (build), gerou a análise de dados (analyze), podendo ser feita a predição de demanda de cada produto do dataset escolhido. 

Para refinar a contrução do modelo, foi criado um arquivo CSV ('sales_data.csv')através de AI, Gemini da Google, com o seguinte prompt: "Atue como um cientista de dados e crie um dataset em formato CSV com no mínimo 500 registros. Gostaria que esse arquivo refletisse o histórico de vendas de produtos com as seguintes colunas: ID_PRODUTO (numerico incremental), DIA (iniciando em 31/12/2023), FLAG_PROMOCAO, QUANTIDADE_ESTOQUE. Nesse sentido, garanta que haja uma diversidade interessante de produtos (pelo menos 25 IDs diferentes por dia) para um sistema de gerenciamento inteligente de estoque. Além disso, garanta que cada produto tenha uma quantidade inicial em estoque que vá decrescendo de maneira variável dia a dia (se tudo for vendido manter o estoque zerado). Na prática, usarei este dataset para treinar um modelo de machine learning", que foi usada para treinar e refinar o modelo. 

# Conclusão

O Amazon SageMaker Canvas é uma ferramenta poderosa que simplifica o processo de criação e implantação de modelos preditivos, especialmente para analistas de negócios e profissionais que desejam aproveitar o machine learning sem a necessidade de conhecimento técnico profundo, ele democratiza o machine learning, permitindo a tomada de decisões informadas com base em análises preditivas. 
