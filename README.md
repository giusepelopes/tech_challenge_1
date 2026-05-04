# Análise de Experiência do Cliente e Impactos no NPS (E-commerce)
Este repositório contém uma análise exploratória de dados (EDA) focada em identificar os gargalos operacionais que afetam a satisfação do cliente (NPS) e a retenção em uma plataforma de e-commerce.

1. **Objetivo do Projeto**

    O principal objetivo deste projeto é investigar os fatores que geram detratores na base de clientes. A análise busca responder:

    * Qual o impacto real dos atrasos de entrega na percepção da marca?

    * Como o volume de reclamações e o tempo de resolução influenciam a nota de NPS?

    * Existe correlação entre falhas operacionais e a queda na taxa de recompra em 30 dias?

2. **Descrição da Base de Dados**

    A base de dados utilizada (desafio_nps_fase_1.csv) contém 2.500 registros únicos de pedidos. Os principais atributos incluem:

    * **Perfil do Cliente:** Idade, região e tempo de relacionamento (tenure).

    * **Métricas de Satisfação:** nps_score (variável alvo) e csat_internal_score.

    * **Operacional:** Valor do pedido, quantidade de itens, dias de atraso na entrega e número de tentativas de entrega.

    * **Suporte:** Contatos com o atendimento, contagem de reclamações e tempo de resolução em dias.

    * **Comportamental:** Indicador de recompra em 30 dias (repeat_purchase_30d).

3. **Metodologia Utilizada**

    A análise seguiu os seguintes passos técnicos:

    * **Tratamento e Engenharia de Dados:** Criação de variáveis categóricas para segmentar atrasos, tempo de casa e perfis de suporte para facilitar a visualização de padrões.

    * **Testes Estatísticos:**
    
        * Shapiro-Wilk: Aplicado para verificar a normalidade da distribuição do NPS.

        * Kruskal-Wallis: Utilizado para comparar se as variações de NPS por região eram estatisticamente significativas.

    * **Análise de Correlação:** Uso de matrizes de correlação e heatmaps para identificar os maiores "detratores" da nota.

    * **Análise de Cohort e Segmentação:** Cruzamento de CSAT vs NPS e impacto de atrasos na taxa de recompra.

4. **Como Reproduzir os Resultados**

    **Pré-requisitos**

    * Certifique-se de ter o Python 3.x instalado e as seguintes bibliotecas:

            pip install pandas numpy seaborn scipy plotly matplotlib

    **Jupyter Notebook:**

    * Clone este repositório
    * Abra o projeto no seu ambiente de execução Jupyter preferido
    * Execute o notebook t1_EDA.ipynb

    **Python Script:**
        
    * Clone este repositório
    * No terminal, navegue até o diretório tech_challenge_1/scripts
    * Execute o script principal:
            
            python t1_eda.py
