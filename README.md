🎬 NFLX Insight: Netflix Stock Analysis

Um dashboard interativo de análise financeira construído com Power BI para examinar 4 anos de dados históricos da Netflix (NFLX). Este projeto foi desenvolvido para transformar a volatilidade bruta do mercado de ações em uma narrativa clara de tendências e volumes. Foquei intensamente na robustez do backend (DAX e Modelagem) e na precisão dos dados financeiros.

## 📦 Tecnologias

- **Power BI Desktop**
- **Power Query (M Language)**
- **DAX (Data Analysis Expressions)**
- **Modelagem Star Schema**
- **Figma** (Design de Background)

## 🦄 Features

Aqui está o que você pode analisar no NFLX Insight:

- **Análise de Tendência Inteligente:** Compare o preço de fechamento ajustado com Médias Móveis de 30 e 90 dias para identificar pontos de reversão.
- **KPIs Dinâmicos de Performance:** Cartões de indicadores que calculam em tempo real o Retorno Total, Variação Percentual e Volume Acumulado com base no período selecionado.
- **Monitoramento de Volatilidade:** Um gráfico dedicado a mostrar a amplitude (High vs Low) média diária por ano, ajudando a identificar períodos de incerteza no mercado.
- **Sazonalidade de Volume:** Identifique quais meses do ano historicamente apresentam maior liquidez e interesse de negociação.
- **Navegação Temporal:** Filtros customizados que permitem navegar entre 2018 e 2022 com precisão diária.

## 🎯 Atalhos de Interação:

Aumente a velocidade de análise com estas funções nativas:
- **Multi-seleção:** Segure `Ctrl` e clique em diferentes anos ou meses nos gráficos para comparar períodos específicos.
- **Foco de Detalhe:** Passe o mouse (Tooltip) sobre os pontos das linhas para ver os valores exatos de abertura, máxima e mínima de um dia específico.
- **Reset de Filtros:** Clique em um espaço vazio de qualquer gráfico para limpar as seleções e voltar à visão geral.

## 👩🏽‍🍳 The Process 

Comecei pelo **Power Query**, garantindo que os dados financeiros fossem tipados como "Número Decimal Fixo". Isso é crítico em projetos de BI para evitar erros de arredondamento comuns em cálculos de moedas e ativos.

O próximo passo foi a **Modelagem**. Em vez de usar a tabela original de forma isolada, criei uma tabela dimensão `dCalendario` via DAX. Isso me permitiu criar um relacionamento **1:N (Star Schema)**, que é a base para qualquer análise de *Time Intelligence* performática.

Para as métricas, desenvolvi uma série de **medidas DAX**. Foquei em criar medidas explícitas (em vez de usar colunas implícitas) para garantir que cálculos como a Média Móvel fossem dinâmicos e precisos independente do filtro aplicado.

Na etapa final, cuidei do **Storytelling**. Utilizei a identidade visual da Netflix (Vermelho sobre fundo escuro) não apenas por estética, mas como uma ferramenta de UI/UX para guiar o olhar do usuário primeiro para os KPIs de fechamento e depois para as tendências de longo prazo.

Documentar cada etapa, desde a limpeza até a criação do heatmap de retornos, me fez perceber que o entendimento completo de um projeto de dados só vem quando conseguimos explicar a lógica por trás de cada visual.

## 📚 O que eu aprendi

Durante este projeto, aprofundei habilidades técnicas que melhoraram meu pensamento lógico aplicado a finanças:

- **Cálculos de Média Móvel:** Aprender a usar as funções `DATESINPERIOD` e `LASTDATE` para criar tendências suaves foi um divisor de águas para análise de séries temporais.
- **Contexto de Filtro vs Contexto de Linha:** Entender como a função `CALCULATE` manipula os filtros para comparar o preço atual com o preço do ano anterior (YoY).
- **Tipagem de Dados Financeiros:** A importância da precisão decimal fixa para evitar inconsistências em grandes volumes de dados.
- **Ordenação Customizada:** Resolver o problema clássico de ordenação de meses (alfabética vs cronológica) usando colunas de índice no Power Query.

## 💭 Como pode ser melhorado?

- Adicionar uma conexão via API para atualizar os dados da Netflix em tempo real.
- Implementar análise de "What-if" para simular retornos baseados em diferentes valores de investimento inicial.
- Incluir indicadores técnicos avançados como RSI (Relative Strength Index) ou Bandas de Bollinger.
- Adicionar uma aba de comparação direta com o índice S&P 500 para análise de benchmark.

## 🚦 Executando o Projeto

Para visualizar o dashboard no seu ambiente local:
1. Clone o repositório ou baixe o arquivo `.pbix`.
2. Certifique-se de ter o **Power BI Desktop** instalado.
3. Abra o arquivo `NFLX_Insight.pbix`.
4. Se os dados não carregarem, vá em `Transformar Dados > Configurações da Fonte de Dados` e aponte para o arquivo `NFLX.csv` na pasta `/Data` deste repositório.

## 🍿 Video / Dashboard em Ação

![Netflix Dashboard Preview](https://github.com/user-attachments/assets/65598b09-c594-448b-9009-9984b48a2eac)

