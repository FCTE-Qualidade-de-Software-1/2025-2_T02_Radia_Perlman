# 1. Planejamento da Avaliação

## 1.1. Objetivo da Fase

Esta fase detalha o plano de execução para a coleta de dados da Fase 4. O objetivo é traduzir as métricas definidas no GQM (Fase 2) em um conjunto de Casos de Teste (CTs) auditáveis, garantindo que a avaliação seja sistemática e repetível.

Esta página centraliza o planejamento do projeto, incluindo a rastreabilidade entre as fases, o cronograma de execução e a divisão de tarefas da equipe.

## 1.2. Método de Avaliação 

Será adotada uma abordagem orientada pelo método GQM (Goal-Question-Metric).
A coleta de dados será realizada por meio de múltiplas fontes, incluindo: formulários, videochamadas com usuários para avaliar a navegação no Oppia, gravações de tela em diferentes dispositivos, ferramentas de análise estática, análise do histórico do repositório e inspeções manuais de código.

A tabela apresentada a seguir assegura que todas as métricas definidas na Fase 2 estão associadas a um ou mais Casos de Teste (CTs) documentados nesta etapa, garantindo assim a rastreabilidade completa entre os objetivos do GQM e os testes planejados.

<p align="center"> <b>Tabela 1 - Tabela Geral de Métricas</b> </p>

| Característica          | Questão                                                                       | Métrica                                                          | Ferramenta / Fonte de Dados       | Plano de Coleta                                                                                                                                     | ID Caso de Teste             |
| ----------------------- | ----------------------------------------------------------------------------- | ---------------------------------------------------------------- | --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| **Adequação Funcional** | **Q1.1 Completude Funcional: As funções cobrem todas as tarefas essenciais?** | **M1.1: Percentual de Completude das Tarefas Essenciais**        | Testes de Cenário, Requisitos     | 1. Calcular % = (tarefas concluídas / tarefas essenciais) × 100. Hipótese: 98%. Testado via cenários de uso.                                        | CT-AF-01, CT-AF-02, CT-AF-06 |
|                         | **Q1.2 Correção Funcional: As funções produzem resultados corretos?**         | **M2.1: Taxa de Precisão do Feedback de Aprendizado**            | Testes funcionais em questões     | 1. % = (feedbacks corretos / total) × 100. Hipótese: 100%.                                                                                          | CT-AF-03                     |
|                         |                                                                               | **M2.2: Taxa de Integridade e Recuperação de Dados**             | Testes de Estresse / Concorrência | 1. % = (operações de salvamento e recuperação bem-sucedidas / total) × 100. Hipótese: 99.5%.                                                        | CT-AF-04, CT-AF-05           |
|                         | **Q1.3 Apropriação Funcional: As funções facilitam o aprendizado?**           | **M3.1: Eficiência na Recuperação de Informação**                | Testes de Usabilidade             | 1. % = (buscas relevantes nas 5 primeiras / total). Hipótese: 85%.                                                                                  | CT-AF-07                     |
|                         |                                                                               | **M3.2: Adequação das Funcionalidades-Chave (Likert)**           | Questionários Likert              | Média ≥ 4.0/5. Escala aplicada a estudantes e educadores.                                                                                           | CT-AF-08                     |
| **Portabilidade**       | **Q2.1 Adaptabilidade: O sistema funciona em diferentes ambientes?**          | **M1.1: Adaptabilidade ao Hardware**                             | Análise estrutural                | 1. X = A/B. Aceitação ≥ 0.7.                                                                                                                        | CT-P-Q1-M1                   |
|                         |                                                                               | **M1.2: Adaptabilidade ao Software**                             | Análise estrutural                | 1. X = A/B. Aceitação ≥ 0.7.                                                                                                                        | CT-P-Q1-M2                   |
|                         | **Q2.2 Instalabilidade: O sistema pode ser instalado facilmente?**            | **M2.1: Esforço de Instalação**                                  | Processo de instalação            | 1. X = A/B. Aceitação: ≤ 0.4.                                                                                                                       | CT-P-Q2-M1                   |
|                         |                                                                               | **M2.2: Flexibilidade de Instalação**                            | Processo de instalação            | 1. X = A/B. Aceitação: 0.2 ≤ X ≤ 0.4.                                                                                                               | CT-P-Q2-M2                   |
|                         | **Q2.3 Coexistência: O sistema funciona bem com outros softwares?**           | **M3.1: Disponibilidade de Coexistência**                        | Ambiente de produção              | 1. X = A/B. Aceitação ≥ 0.7.                                                                                                                        | CT-P-Q3-M1                   |
|                         |                                                                               | **M3.2: Restrição/Avaria sob Coexistência**                      | Registros de Erro                 | 1. X = A/T. Aceitação: ≤ 0.3.                                                                                                                       | CT-P-Q3-M2                   |
|                         | **Q2.4 Substituibilidade: O sistema pode ser migrado ou substituído?**        | **M4.1: Consistência de Funcionalidades**                        | Testes de Migração                | 1. X = A/B. Aceitação ≥ 0.9.                                                                                                                        | CT-P-Q4-M1                   |
|                         |                                                                               | **M4.2: Facilidade de Migração**                                 | Testes de Migração                | 1. X = A/B. Aceitação ≥ 0.9.                                                                                                                        | CT-P-Q4-M2                   |


<p align="center"><b>Fonte: </b>Autoria de <a href="https://github.com/bolzanMGB">Othavio Bolzan</a></p>


## 1.3. Cronograma de Execução e Divisão de Tarefas

A seguir apresenta-se o cronograma detalhado das atividades previstas para as Fases 3 e 4, contemplando a configuração do ambiente, a coleta das métricas de Adequação Funcional e Portabilidade, a consolidação dos dados obtidos e a elaboração do relatório final. As datas foram distribuídas entre 19 e 30 de novembro de 2025, garantindo uma execução organizada, sequencial e alinhada aos objetivos definidos pelo método GQM.


<p align="center"> <b>Tabela 2 - Cronograma de Coleta e Avaliação</b> </p>

| **Fase** | **Etapa (Agrupada por Característica)** | **Métricas Coletadas**                                                                                                                                                                                                                                                                                                                 | **Responsáveis**                                                                                                                                               | **Início Previsto** | **Fim Previsto** |
| -------- | --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- | ---------------- |
| **Fase 3**    | Configuração do Ambiente                | Preparação dos formulários, ferramentas de gravação, dispositivos, Oppia, análise estática.                                                                                                                                                                                                                                            | Todos                                                                                                                                                          | **19/11/25**        | **20/11/25**     |
| **Fase 3**    | Coleta Adequação Funcional              | **M1.1** Completude de Tarefas <br> **M2.1** Precisão do Feedback <br> **M2.2** Integridade de Dados <br> **M2.3** Precisão de Notificação e Recuperação de Dados     <br>                         **M3.1** Recuperação de Informação <br> **M3.2** Adequação Funcional (Likert)                                             | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) <br> [Douglas Marinho](https://github.com/M4RINH0)                                                   | **21/11/25**        | **23/11/25**     |
| **Fase 3**    | Coleta Portabilidade                    | **M1.1** Adaptabilidade ao Hardware <br> **M1.2** Adaptabilidade ao Software <br> **M2.1** Esforço de Instalação <br> **M2.2** Flexibilidade de Instalação <br> **M3.1** Coexistência <br> **M3.2** Restrição sob Coexistência <br> **M4.1** Consistência em Migração <br> **M4.2** Facilidade de Migração | [Brunno Fernandes](https://github.com/brunnoff) <br> [Othavio Bolzan](https://github.com/bolzanMGB) <br> [Pedro Dourado](https://github.com/pedrolucasdourado) | **24/11/25**        | **26/11/25**     |
| **Fase 4**    | Consolidação dos Dados                  | Agrupamento e organização de gravações, formulários, análise estática, inspeções e dados do repositório.                                                                                                                                                                                                                               | Todos                                                                                                                                                          | **27/11/25**        | **28/11/25**     |
| **Fase 4**    | Análise e Relatório Final               | Aplicação do GQM, interpretação dos resultados das métricas e elaboração do relatório final.                                                                                                                                                                                                                                           | Todos                                                                                                                                                          | **29/11/25**        | **30/11/25**     |


<p align="center"><b>Fonte: </b>Autoria de <a href="https://github.com/bolzanMGB">Othavio Bolzan</a></p>

## 1.4. Fontes de Evidência e Rastreabilidade

Os seguintes documentos, artefatos e ferramentas do Oppia serão utilizados para garantir a rastreabilidade completa da avaliação, desde a definição das métricas até a verificação dos resultados.

<p align="center"> <b>Tabela 3 -  Fontes de Evidência </b> </p>


| **Fonte**                                | **Local / Ferramenta**                                                                                                                              | **Uso**                                                                                                               |
| ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Código-Fonte (Oppia)**                 | [Repositório oficial do Oppia (GitHub)](https://github.com/oppia/oppia)                                                                             | Base primária para métricas de análise estática, inspeções e verificação de implementações reais das funcionalidades. |
| **Histórico de Desenvolvimento**         | [Git Log, Pull Requests, Issues e Discussions (GitHub)](https://github.com/oppia/oppia)                                                             | Utilizado para métricas de processo e evolução (commits, issues, mudanças em funcionalidades).                        |
| **Ambiente de Execução** | [Plataforma Oppia Web](https://www.oppia.org/)                                                                                                | Fonte de métricas coletadas via testes funcionais, questionários, logs de execução e experimentação de usuários.      |
| **Definição da Avaliação**               | [Fase 2](https://fcte-qualidade-de-software-1.github.io/2025-2_T02_Radia_Perlman/fase2/01_plano_de_medicao_gqm/)                              | Formaliza cada métrica, métodos de coleta, questões e critérios de julgamento.                                        |
| **Dados Brutos Coletados**               | [Fase 4 ](https://fcte-qualidade-de-software-1.github.io/2025-2_T02_Radia_Perlman/fase4/01_dados_brutos/) | Armazena integralmente os dados coletados nos testes, formulários e análises.                                         |
| **Relatório Final**                      | [Documento Final da Avaliação](https://fcte-qualidade-de-software-1.github.io/2025-2_T02_Radia_Perlman/fase4/03_resultados_port/)                   | Consolida dados, julgamentos, discussão e conclusões.                                                                 |

<p align="center"><b>Fonte: </b>Autoria de <a href="https://github.com/bolzanMGB">Othavio Bolzan</a></p>



## Histórico de Versões

| Versão |    Data    | Descrição                                                                            | Autor                                                       | Revisor                                                   |
| :----: | :--------: | :----------------------------------------------------------------------------------- | :---------------------------------------------------------- | :-------------------------------------------------------- |
| `1.0`  | 16/11/2025 | Criação da estrutura inicial da página                                               | [Brunno Fernandes](https://github.com/brunnoff)             | [Othavio Bolzan](https://github.com/bolzanMGB)            |
| `2.0`  | 17/11/2025 | Elaboração das tabelas Método de Avaliação e Cronograma de Execução                  | [Othavio Bolzan](https://github.com/bolzanMGB)              | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) |
| `3.0`  | 20/11/2025 | Atualização da nomeclatura dos testes de adequação funcional, remoção da métrica 2.3 | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) |                                                           |