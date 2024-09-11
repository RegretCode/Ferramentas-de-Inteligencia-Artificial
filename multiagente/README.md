# Simulação de Propagação de Doença com Intervenções - NetLogo

## Descrição do Projeto

Este projeto simula a propagação de uma doença contagiosa em uma população, considerando fatores externos como a eficácia das máscaras, a taxa de vacinação, o tempo de recuperação da doença e a taxa de mortalidade. O objetivo é analisar como esses fatores influenciam o número de pessoas infectadas, recuperadas e mortas ao longo do tempo.

## 1. Hipótese

A hipótese central é que a propagação de uma doença pode ser controlada através de intervenções, como o uso de máscaras e vacinação. A simulação busca explorar como esses fatores, em conjunto com a taxa de recuperação e mortalidade, influenciam a dinâmica de infecção e recuperação na população ao longo do tempo.

## 2. Implementação

A simulação foi realizada utilizando o ambiente de modelagem NetLogo, com os seguintes passos de implementação:

- **Inicialização da População**: Criação de 2140 agentes, cada um com atributos específicos como o tipo de máscara usada (com diferentes níveis de eficácia) e se foi ou não vacinado.
- **Infecção Inicial**: 10% da população (214 agentes) foi inicialmente infectada. A infecção se propaga com uma chance de 28% a cada "tick" (unidade de tempo).
- **Propagação da Doença**: A cada tick, os agentes infectados podem infectar agentes saudáveis próximos, considerando a eficácia de máscaras e vacinas.
- **Recuperação e Mortalidade**: Após 15 dias, os agentes podem se recuperar ou morrer, dependendo de uma taxa de mortalidade predefinida. Agentes recuperados adquirem imunidade temporária.
- **Vacinação Gradual**: A cada 10 ticks, 10% dos agentes não vacinados recebem uma vacina. Diferentes vacinas foram usadas, cada uma com diferentes níveis de eficácia.

## 3. Resultados

Os resultados da simulação mostram claramente a dinâmica da propagação da doença e o impacto das intervenções:

- **Disseminação Rápida**: Devido à alta chance de infecção (28%), o número de infectados aumentou rapidamente no início da simulação, atingindo um pico antes de começar a declinar à medida que os agentes se recuperavam ou morriam.
- **Imunidade Coletiva**: A recuperação de muitos indivíduos levou a uma queda no número de novos casos após o pico inicial, mostrando a importância da imunidade coletiva.
- **Mortalidade**: A taxa de mortalidade foi significativa, especialmente entre os não vacinados. O impacto acumulado das mortes é claramente observado no gráfico gerado pela simulação.
- **Vacinação**: A vacinação, mesmo sendo aplicada de forma gradual, reduziu a propagação da doença e o número de mortes. No entanto, o impacto da vacinação só foi percebido significativamente após um tempo devido à sua introdução gradual.

## 4. Conclusão

A simulação reforça a importância de intervenções como o uso de máscaras e a vacinação no controle de uma pandemia. A vacinação rápida e abrangente foi especialmente eficaz em reduzir as taxas de infecção e mortalidade. Os gráficos gerados durante a simulação ilustram o impacto dessas intervenções, destacando como essas estratégias podem ajudar a mitigar os efeitos de uma doença contagiosa na população.

## 5. Ferramentas Utilizadas

- **NetLogo**: Ambiente de simulação utilizado para modelagem de agentes.
- **Gráficos e Estatísticas**: Gerados automaticamente pela simulação para acompanhar a evolução dos agentes ao longo do tempo.

