# 3. Resultados - Portabilidade

Esta seção apresenta os resultados consolidados da execução dos Casos de Teste de Portabilidade (CT-P) e a análise comparativa com as hipóteses de aceitação definidas na Fase 2.

## 3.1. Tabela de Execução (Resumo)

| ID do Teste | Título do Teste | Status | Observação |
| :--- | :--- | :---: | :--- |
| CT-P-01 | Verificação de Adaptabilidade | Passou | Todas métricas tiveram sucesso|
| CT-P-02 | Verificação de Instalabilidade | Falhou | Métrica 2.1 não teve sucesso|
| CT-P-03 | Verificação de Coexistência |Passou | Todas métricas tiveram sucesso |
| CT-P-04 | Verificação de Substituibilidade | Falhou | Nenhuma métrica teve sucessoObservação |

## 3.2. Análise Detalhada das Métricas

| Métrica | Resultado Medido | Nível de Aceitação | Aprovado? |
| :--- | :--- | :--- | :---: |
| **M1.1: Adaptabilidade Hardware** | X = 0,7 | ≥ 0,7 | Sim |
| **M1.2: Adaptabilidade Software** | X = 0,8 | ≥ 0,7 | Sim |
| **M1.3: Adaptabilidade Software** | X = 0,8 | ≥ 0,7 | Sim |
| **M2.1: Esforço Instalar** | X = 0,473 | ≤ 0,4 | Não |
| **M2.2: Flexibilidade Instalação**| X = 0,25| 0,2 ≤ X ≤ 0,4 | Sim |
| **M3.1: Disponibilidade Coexist.** | X = 0,8175 | ≥ 0,7 | Sim |
| **M3.2: Coexistência Apresentada**| X = 0,02 | ≤ 0,3 | Sim |
| **M4.1: Consistência Funcional** | X = 0,82 | ≥ 0,9 | Não |
| **M4.2: Facilidade Migração** | X = 0,5 | ≥ 0,9 | Não |

## 3.3. Discussão dos Resultados

* **Q1: Adaptabilidade:** A plataforma foi aprovada globalmente nas métricas, demonstrando alta solidez em ambientes Desktop (Windows e Linux) com navegadores baseados em Chromium (Brave, Opera, Chrome) e resoluções acima de 1024px. Entretanto, as evidências apontam uma falha crítica de usabilidade no ecossistema Apple móvel (iOS/Safari), onde botões tornam-se "não clicáveis" e o layout quebra em resoluções pequenas (365px). A aprovação nas métricas gerais (M1.1 e M1.3) ocorreu devido à compensação pelo excelente desempenho do App Nativo Android, que funcionou perfeitamente em 1080px, mascarando a deficiência da versão Web Mobile.


* **Q2: Instalabilidade:** A métrica de Esforço de Instalação (M2.1) não atingiu o critério de aceitação, resultando em reprovação do teste. A análise revelou que, embora a instalação no Linux seja fluída e automatizada, os ambientes Windows e Mac exigem excessiva configuração manual prévia, o que baixou a média global de automação para 0,473. Já a Flexibilidade (M2.2) foi aprovada, confirmando que a arquitetura de "ambiente hermético" do Oppia restringe variações propositalmente para garantir estabilidade.


* **Q3: Coexistência:** A coexistência entre aplicativos mostrou bom desempenho geral: todas as plataformas conseguiram manter o sistema funcionando sem falhas críticas, garantindo aprovação nas métricas M3.1 e M3.2. Apesar de Linux e iOS apresentarem pequenos atrasos e aquecimento, e de Android e Windows terem sido mais estáveis, o sistema demonstrou capacidade consistente de operar junto a outros apps, com instabilidades apenas pontuais.


* **Q4: Substituibilidade:** A migração entre ambientes foi o ponto mais problemático, resultando em reprovação nas métricas M4.1 e M4.2. Embora a migração entre navegadores desktop tenha funcionado perfeitamente, tanto Android quanto iOS apresentaram falhas que impediram a continuidade do estudo: no Android, o aplicativo inicia em modo Admin/Debug sem opção de login, bloqueando totalmente a sincronização de progresso; no iOS, apesar de parte do progresso ser reconhecida, a interface quebrada impede o uso normal das lições. Assim, a migração só foi plenamente bem-sucedida em ambientes desktop, mostrando baixa consistência e falta de suporte adequado em dispositivos móveis.

---

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor |
| :---: | :---: | :--- | :--- | :--- |
| `1.0` | 16/11/2025 | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff) | [Othavio Bolzan](https://github.com/bolzanMGB)|
| `2.0` | 28/11/2025 | Preenchimento dos resultados | [Othavio Bolzan](https://github.com/bolzanMGB)| [Douglas Marinho](https://github.com/M4RINH0) |