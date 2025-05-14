# Bootcamp-CDIA
Bootcamp CDIA



1.  **Planejamento Inicial:** Iniciei o projeto com o planejamento, criando uma lista geral de tarefas para organizar as atividades do desafio.
2.  **Definição dos Objetivos do Projeto:** Defini os objetivos do projeto, como desenvolver um sistema inteligente para classificar defeitos em chapas de aço, prever a classe do defeito com probabilidade, extrair insights e gerar visualizações.
3.  **Identificação das Necessidades da Empresa:** Identifiquei as necessidades da empresa, incluindo a automatização do controle de qualidade, detecção precoce e classificação precisa de defeitos, e a geração de informações para tomada de decisão.
4.  **Compreensão da Estrutura dos Dados:** Entendi os dados, analisando a estrutura e o significado de cada uma das 31 colunas (features) fornecidas.
5.  **Análise Exploratória Inicial:** Explorei estatísticas descritivas básicas, identificando outliers, valores ausentes e a necessidade de padronização em algumas colunas.
6.  **Verificação do Balanceamento e Consistência:** Verifiquei o balanceamento das classes de defeito e a consistência dos dados, notando a necessidade de padronizar representações de valores booleanos (ex: 'true', 'sim').
7.  **Pré-processamento e Limpeza de Dados:** Realizei o pré-processamento dos dados, tratando valores ausentes e removendo 418 linhas com dados faltantes.
8.  **Padronização e Criação de Novas Features:** Padronizei as colunas 'tipo_do_aço_A300' e 'tipo_do_aço_A400', criando a nova coluna 'tipo_de_aço' para unificar essa informação.
9.  **Tratamento de Dados Inconsistentes:** Removi valores inconsistentes, como espessuras negativas e coordenadas negativas (x_minimo, x_maximo, y_minimo, y_maximo), que não são fisicamente possíveis.
10. **Correção Adicional de Dados Numéricos:** Tratei também valores negativos em 'area_pixels', 'perimetro_x', 'perimetro_y' e 'comprimento_do_transportador'.
11. **Análise de Correlação:** Analisei a correlação entre as variáveis, identificando relações fortes, negativas, fracas e a ausência de correlação para 'peso_da_placa' devido a valores nulos.
12. **Modelagem Inicial (Baseline):** Para a modelagem inicial, selecionei e treinei um modelo de Regressão Logística como baseline.
13. **Engenharia de Features Baseada em Insights:** Na engenharia de features, utilizei insights da análise de correlação, como a criação da variável 'tipo_de_aço' e a observação da baixa preditividade linear das coordenadas.
14. **Segmentação dos Dados por Tipo de Aço:** Decidi separar os dados em DataFrames distintos para o aço A300 e A400, visando análises e modelagem específicas por tipo de produto.
15. **Exploração de Modelos Multirrótulo:** Explorei diferentes modelos de classificação multirrótulo, como Árvore de Decisão, Random Forest, Gradient Boosting e Algoritmo de Cadeias de Classificadores.
16. **Identificação do Desbalanceamento de Classes:** Identifiquei um desbalanceamento extremo de classes para algumas falhas no DataFrame do aço A300 (especialmente falha_3, falha_4, falha_5), representando um desafio para o treinamento dos modelos.
17. **Seleção do Modelo Final:** Selecionei o Algoritmo de Cadeias de Classificadores por apresentar o melhor desempenho entre os modelos multirrótulo testados.
18. **Consideração sobre Redes Neurais:** Considerei o uso de Redes Neurais (Keras) como uma possibilidade, embora não tenha sido o foco principal da modelagem final.
19. **Sugestão de Próximos Passos:** Sugeri, como próximo passo, a otimização de hiperparâmetros do modelo selecionado (e do Gradient Boosting) para potencializar os resultados, uma etapa que não foi realizada.
