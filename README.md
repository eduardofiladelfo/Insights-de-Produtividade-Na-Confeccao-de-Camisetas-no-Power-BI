# Dashboard-Insights-de-Produtividade-Na-Confeccao-de-Camisetas-no-Power-BI

 ### 🌍 Overview do Projeto

Este KPI foi criado com o intuito de promover insights sobre a produtividade geral por equipes de uma fábrica que produz camisetas entre julho de 2024 até junho de 2025. A análise abrange múltiplos aspectos sobre a produtividade, incluindo:

- O comparativo entre a produtividade ao longo do ano _versus_ a meta estabelecida  do período citado acima;

- Ranqueamento dos motivos pelos quais as metas não foram atingidas;

- Histórico diário detalhado das metas que não foram antingidas por equipe e justificativa;

- Detalhamento das peças produzidas por equipe ao longo do período por Work Orders.

https://github.com/user-attachments/assets/99069ff1-b705-41e3-9c95-16a398b79e38
  
### ✅ Perguntas de Negócio

O intuito desse relatório é responder às seguintes perguntas de negócio:

1. É possível visualizarmos a quantidade de peças que foram produzidas mensalmente ao longo do ano juntamente com a meta que foi estabelecida? 

2. É possível visualizarmos a variação percentual da produtividade em relação ao mês anterior? 

2. Quais são as falhas operacionais? Quais os problemas mais recorrentes?

3. Qual a produtividade diária das equipes em relação à meta? É possível visualizarmos também a diferença entre saldo programado e o realizado?

4. Quais as metas que não foram atingidas e qual a justificativa?

5. Qual a produtividade total por cada equipe? É possível visualizarmos também a diferença entre saldo programado e o realizado?

6. É possível visualizarmos As Work Orders separadas por equipes de forma detalhada de todo o período?

### 🗂️ Dataset

O conjunto de dados deste dataset tem autoria própria e está disponível [aqui](https://github.com/eduardofiladelfo/Insights-de-Produtividade-Na-Confeccao-de-Camisetas-no-Power-BI/tree/27aef06a1a2ac6f0ec28fab970ce6f7d8908fda0/bases).

### 🛠️ Ferramentas 

Power BI:  Importação dos arquivos em CSV e visualização dos dashboards.
Canva: Criação do design visual do indicador, permitindo uma apresentação mais clara dos insights obtidos na análise.

### 📝 Dados Utilizados
Para a anáise, foram utilizadas as seguintes tabelas: 

- fProducao: Registro histórico das peças que foram produzidas pelas equipes;
- fMeta: Metas estabelecidas para as equipes por meta diária;
- dEquipe: Tabela dimensão com as equipes que produzem as peças;
- dJustificativaMeta: Tabela dimensão com as justificativas de forma detalhada das metas que não foram atingidas; 
- dCalendario: Tabela dimensão com as datas do período;
- dWorkOrder: Tabela dimensão das Work Orders, suas fases (fase de confecção) e a quantidade de peças que serão produzidas;
- dCor: Tabela dimensão contendo as cores das camisetas; 
- dGrade: Tabela dimensão contendo os tamanhos das peças;
- dEquipe: Tabela dimensão com as equipes que realizam o processo de confecção;
- dProduto: Tabela dimensão com o nome dos produtos que são confeccionados; 
- dHcOperador: Tabela dimensão da relação de nome, matrícula e qual equipe o funcionário pertence;
- dUsuarioColetorOperador: Tabela dimensão com o id utilizado pelo operador ao acessar o coletor e sua matrícula.

### ⚙️ Estrutura do dashboard

#### Página Geral

Este relatório detalha as quantidades produzidas comparadas às metas definidas para cada dia, semana e mês, destacando também o ranking de falhas operacionais e o histórico das metas não alcançadas.

- Qtd peças mês x Meta Mês: Relação Quantidade de peças produzidas por mês versus meta estabelecida. É possível visualizar também o comparativo de peças produzidas MoM (month over month)

- Ranking de falhas operacionais: Gráfico ranqueado das falhas operacionais do período, com visualização do anual, mensal e semanal. Podendo também a filtragem por equipe.
 
- Qtd produzida x Meta Dia: Histórico da produtividade diária versus meta estabelecida com a visualização do saldo de pegas entregues em relação a meta, podendo ser positivo ou negativo. Podendo também a filtragem por equipe. 

- Histórico de Metas não Atingidas: Tabela com a relação de metas não atingidas por data, equipe, Justificativa da falha operacional e a porcentagem entregue no dia. 

- Produtividade por Equipe: Produtividade semanal da equipe, com a visualização do saldo de pegas entregues em relação a meta, podendo ser positivo ou negativo.

  <div align="center">
  
  ![Geral](imagens/Geral.jpg)
  
</div>

#### Página Por W.O

O relatório mostra de forma detalhada a produtividade da equipe dada sua Work Order, com a filtragem anual, mensal, semanal e diária. Também é possível a filtragem por equipe, sendo:

-	Work Order: Número da Work Order;
-	Nome: Nome do operador responsável pela confecção;
-	Equipe: Nome da Equipe que o operador pertence;
-	Grade: Tamanho da peça confeccionada;
-	Produto: Nome do produto confeccionado;
-	Cor: Cor do produto confeccionado;
-	Quantidade peças: Quantidade de peças entregues.

    <div align="center">
  
  ![PorWo](imagens/PorWo.jpg)
  
</div>

### 🕸️ Diagrama ER

ㅤ
    <div align="center">
  
  ![DiagramaER](imagens/DiagramaER.png)
  
</div>

### 🎯 Tratamento dos dados 
O tratamento dos dados foi realizado via Excel na extração dos dados, algumas linhas da coluna "QTDE" na tabela fProducao continham valores nulos, logo, foram removidas.
