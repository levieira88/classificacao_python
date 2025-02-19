# Previsão de usuários com alta chance de deixar Streaming
Utilize um modelo de classificação para mapear qual o perfil de usuários tem mais chance de deixar uma plataforma de streaming.

## Contexto

Você trabalha em uma plataforma de streaming e a diretoria está preocupada com o alto índice de usuários cancelando as suas assinaturas. Eles acreditam que é possível prever se um usuário tem mais chance de deixar a plataforma antes que isso aconteça, e com base nessa informação tomar ações para reduzir o churn.

Seu objetivo é criar um modelo de classificação capaz de prever se um usuário tem mais chance de cancelar a sua assinatura na plataforma ou não. Para isso, a empresa forneceu uma base de dados em csv contendo dados sobre as contas dos clientes.

### Sobre os dados

Os dados fornecidos possuem informações sobre as contas dos clientes na plataforma de streaming, divididos entre contas Basic, Standard e Premium, onde cada uma oferece uma gama maior de serviços que a anterior.

## Como começar?

Desenvolva um modelo de classificação que seja capaz de prever se o cliente irá cancelar o serviço ou não, levando em consideração o seu perfil no streaming.

Teste com mais de um tipo de modelo para encontrar o que possuir a melhor performance em comparação com um baseline. Utilize gráficos e visualizações para auxiliar e enriquecer a sua análise.

Não se esqueça de documentar cada etapa, justificando as escolhas realizadas. É essencial informar os insights obtidos e como o serviço de streaming pode se beneficiar do uso do seu modelo para resolver o problema de negócio. Boa sorte!

# 🎯 Etapas de Desenvolvimento

## **Etapa 01) Análise exploratória dos dados (Data Understanding)**

1. Carregue a base de dados;
2. Realize uma descrição estatística dos dados;
3. Verifique os tipos de dados
4. Verifique a quantidade de valores faltantes

<aside>
💡 
  
  **Dica:** Utilize as funções .info(), .isna().sum(), faça algumas plotagens para entender a distribuição dos dados.

</aside>

## Etapa 02) Tratamento dos Dados (Data Preparation)

1. Substituir valores “NaN” por 0 Colunas → Time_on_platform, Num_streaming_services, Churned, Avg_rating, Devices_connected
2. Dropar linhas nulas nas colunas Gender, Subscription_type e Age
3. Transformando valores churned 0 e 1 por No e Yes
4. Transformando valores floats em valores inteiros

<aside>
💡 
  
  **Dica:** Utilize as funções fillna(), dropna, replace, astype(int)

</aside>

## Etapa 03) Modelagem dos Dados - Regressão Logística

1. Definir variáveis X e y para o modelo
2. Realizar o .fit do modelo
3. Separar em train e test
4. Realizar a modelagem
5. Plotar matrix confusão
6. Printar métricas

<aside>
💡 
  
  **Dica:** Utilize as funções LabelEncoder, .fit, .transform, get_dummies, MinMaxScaler, train_test_split, predict, assign, ConfusionMatrixDisplay

</aside>

## Etapa 04) Modelagem dos Dados - Tunning

1. Realizar o pré-processamento das variáveis categóricas com `LabelEncoder` ou `get_dummies`.
2. Dividir os dados em treino e teste utilizando `train_test_split`.
3. Treinar o modelo com a função `.fit`.
4. Realizar as predições com `.predict`.
5. Adicionar as previsões ao DataFrame original utilizando `.assign`.
6. Avaliar o modelo plotando a matriz de confusão com `ConfusionMatrixDisplay`.

<aside>
💡

  **Dica:** Utilize as funções `LabelEncoder`, `.fit`, `.transform`, `get_dummies`, `MinMaxScaler`, `train_test_split`, `.predict`, `.assign`, e `ConfusionMatrixDisplay` para garantir um processo de modelagem eficaz.

</aside>

## Etapa 05) Modelagem dos Dados - Random Forest

1. Realizar a montagem do grid search
2. Realizar o .fit do modelo
3. Realizar o Tunning
4. Realizar a modelagem
5. Plotar matrix confusão
6. Printar métricas

<aside>
💡 
  
  **Dica:** Utilize as funções grid_search.best_estimator_.get_params(), fit, assign, ConfusionMatrixDisplay

</aside>
