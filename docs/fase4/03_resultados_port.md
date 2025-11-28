# 3. Resultados - Portabilidade

Esta seção apresenta os resultados consolidados da execução dos Casos de Teste de Portabilidade (CT-P) e a análise comparativa com as hipóteses de aceitação definidas na Fase 2.

## 3.1. Tabela de Execução (Resumo)

| ID do Teste | Título do Teste | Status | Observação |
| :--- | :--- | :---: | :--- |
| CT-P-01 | Verificação de Adaptabilidade | Passou | Todas métricas tiveram sucesso|
| CT-P-02 | Verificação de Instalabilidade | Falhou | Métrica 2.1 não teve sucesso|
| CT-P-03 | Verificação de Coexistência |Passou | Todas métricas tiveram sucesso |
| CT-P-04 | Verificação de Substituibilidade | Falhou | Nenhuma métrica teve sucesso |

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

* **Q1: Adaptabilidade:** [Descreva aqui a análise. O software passou nos testes de adaptabilidade (M1.1 e M1.2)? Ocorreram falhas de layout no mobile ou em navegadores diferentes?]
* **Q2: Instalabilidade:** [Descreva aqui a análise. O esforço (M2.1) e a flexibilidade (M2.2) atenderam às hipóteses?]
* **Q3: Coexistência:** [Descreva aqui a análise. O Oppia funcionou bem (M3.1 e M3.2) enquanto outros apps estavam rodando?]
* **Q4: Substituibilidade:** [Descreva aqui a análise. A sincronização de progresso entre Web e App funcionou (M4.2)? As funcionalidades são consistentes (M4.1)?]

---

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor |
| :---: | :---: | :--- | :--- | :--- |
| `1.0` | 16/11/2025 | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff) | [Othavio Bolzan](https://github.com/bolzanMGB)|
| `2.0` | 28/11/2025 | Preenchimento dos resultados | [[Othavio Bolzan](https://github.com/bolzanMGB)| |