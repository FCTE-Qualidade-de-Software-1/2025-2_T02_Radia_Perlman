# 4. Conclusão da Avaliação de Qualidade da Plataforma Oppia

Esta seção consolida os resultados da avaliação de qualidade da plataforma [Oppia](https://www.oppia.org/), realizada através da execução do plano GQM (Goal-Question-Metric) estabelecido nas fases anteriores. A avaliação focou em duas características críticas para a viabilidade de um projeto piloto educacional: **[Adequação Funcional](../fase2/02_adequacao_funcional.md)** e **[Portabilidade](../fase2/03_portabilidade.md)**.

## 4.1. Visão Geral da Avaliação

A **Fase 4** representou a execução prática do processo de avaliação, onde foram coletadas métricas quantitativas e qualitativas (via formulários e testes de campo):

- **Adequação Funcional:** 5 métricas avaliadas (M1.1, M2.1, M2.2, M3.1, M3.2).
- **Portabilidade:** 9 métricas avaliadas (M1.1, M1.2, M1.3, M2.1, M2.2, M3.1, M3.2, M4.1, M4.2).

Cada métrica foi coletada seguindo os procedimentos auditáveis definidos na Fase 3, com evidências armazenadas nas [planilhas de coleta](../fase4/01_dados_brutos.md) e [pastas de evidências multimídia](../fase4/01_dados_brutos.md).

---

## 4.2. Rastreabilidade e Resultados Consolidados

As tabelas abaixo apresentam a rastreabilidade completa entre as Questões definidas no GQM (Fase 2), as Métricas e o Veredito final baseado nas hipóteses de aceitação.

### 4.2.1. Adequação Funcional

*Detalhes completos na página de [Resultados de Adequação Funcional](./02_resultados_af.md).*

| Questão | Métrica | Resultado | Hipótese (Meta) | Classificação |
| :--- | :--- | :---: | :---: | :--- |
| **Q1: Completude** (Cobre tarefas essenciais?) | M1.1: % Completude de Tarefas | **100%** | 98% | <span style="color:green">**Excelente**</span> |
| **Q2: Correção** (Resultados corretos?) | M2.1: Precisão do Feedback | **100%** | 100% | <span style="color:green">**Excelente**</span> |
| | M2.2: Integridade de Dados | **100%*** | 99.5% | <span style="color:orange">**Bom (com restrição)**</span> |
| **Q3: Apropriação** (Facilita o aprendizado?) | M3.1: Eficiência da Busca | **50%** | 85% | <span style="color:red">**Insatisfatório**</span> |
| | M3.2: Satisfação (Likert) | **3.9** | 4.0 | <span style="color:orange">**Regular**</span> |

*\*Nota: A integridade dos dados pedagógicos foi mantida, mas houve falha na persistência da configuração de idioma.*

**Veredito Parcial:** A Adequação Funcional é **ACEITÁVEL COM RESSALVAS**. A parte pedagógica (criar e responder) é perfeita, mas a experiência de descoberta de conteúdo (Busca) e a satisfação do usuário (devido à interface híbrida Inglês/Português) baixaram a qualidade geral.

### 4.2.2. Portabilidade

*Detalhes completos na página de [Resultados de Portabilidade](./03_resultados_port.md).*

| Questão | Métrica | Resultado | Hipótese (Meta) | Classificação |
| :--- | :--- | :---: | :---: | :--- |
| **Q1: Adaptabilidade** (Funciona em diferentes ambientes?) | M1.1: Hardware (Web Mobile) | **0,7** | 0,7 | <span style="color:orange">**No Limite**</span> |
| | M1.2: Software (Browsers) | **0,8** | 0,7 | <span style="color:green">**Satisfatório**</span> |
| | M1.3: Responsividade | **0,8** | 0,7 | <span style="color:green">**Satisfatório**</span> |
| **Q2: Instalabilidade** (Fácil de instalar?) | M2.1: Esforço de Instalação | **0,47** | ≤ 0,40 | <span style="color:red">**Insatisfatório**</span> |
| | M2.2: Flexibilidade | **0,25** | 0,2-0,4 | <span style="color:green">**Satisfatório**</span> |
| **Q3: Coexistência** (Convive com outros softwares?) | M3.1: Disponibilidade | **0,81** | 0,7 | <span style="color:green">**Satisfatório**</span> |
| | M3.2: Restrições/Erros | **0,02** | ≤ 0,3 | <span style="color:green">**Excelente**</span> |
| **Q4: Substituibilidade** (Migração fácil?) | M4.1: Consistência Funcional | **0,82** | 0,9 | <span style="color:red">**Insatisfatório**</span> |
| | M4.2: Facilidade Migração | **0,5** | 0,9 | <span style="color:red">**Crítico**</span> |

**Veredito Parcial:** A Portabilidade é **INSTÁVEL**. Enquanto a plataforma funciona perfeitamente na convivência com outros softwares e uso em Desktop, ela falha criticamente na migração entre dispositivos (Sincronização Android quebrada) e na instalação local automatizada.

---

## 4.3. Síntese dos Resultados e Relação entre Características

A avaliação revelou uma "dualidade" na qualidade do Oppia: ele é tecnicamente sólido para **uso em laboratório (Desktop)**, mas frágil para **uso pessoal (Mobile)**.

### 4.3.1. Panorama Geral (Pontos Fortes x Fracos)

| Característica | O que funcionou bem? | O que falhou? |
| :--- | :--- | :--- |
| **Adequação Funcional** | **Mecanismo de Ensino:** A criação de lições e o feedback automático funcionam perfeitamente. | **Busca e Idioma:** O motor de busca mistura idiomas e falha 50% das vezes. A interface mistura Inglês/Português. |
| **Portabilidade** | **Coexistência:** Roda leve junto com Youtube/Spotify. **Desktop:** Funciona bem em Chrome/Firefox/Linux. | **Ecossistema Mobile:** App Android nativo com bug de login; Web no iOS com layout quebrado. |

### 4.3.2. Relação de Dependência (Causa e Efeito)

A aplicação do GQM permitiu identificar como a falha em uma característica afeta diretamente a outra:

1.  **Portabilidade bloqueando a Adequação:** As falhas de layout detectadas no iOS (M1.1 - Portabilidade) impediram fisicamente que o usuário clicasse nos botões para avançar a lição. Isso causou uma **falha de completude funcional** para esse perfil de usuário. Sem portabilidade, a função pedagógica não é entregue.
2.  **Instalabilidade dificultando a Substituibilidade:** A dificuldade de instalação local (M2.1 Reprovada) força o usuário a migrar para o Mobile. Porém, ao tentar migrar (M4.2), ele encontra falhas de sincronização no Android, ficando "preso" sem opções viáveis de estudo offline.

---

## 4.4. Recomendações e Plano de Ação

Com base nos dados, a equipe recomenda as seguintes correções para viabilizar o projeto piloto na rede municipal.

### Prioridade Crítica (Imediato)
1.  **Corrigir Login no App Android:** O bug que inicia o app em modo "Admin/Debug" impede o login e a sincronização de progresso (M4.2). Isso inutiliza o app para alunos.
2.  **Corrigir Layout Web no iOS:** Ajustar o CSS para que botões de navegação não fiquem inacessíveis em telas pequenas (Safari/iPhone), garantindo acesso aos alunos que possuem esses dispositivos.

### Prioridade Alta (Curto Prazo)
3.  **Tradução Completa da Interface (i18n):** Traduzir modais de criação e botões do sistema. A mistura de idiomas foi a principal queixa qualitativa dos professores (M3.2).
4.  **Otimização da Busca:** Ajustar o algoritmo para que termos em português retornem lições em português. A taxa de sucesso atual (50%) frustra o aluno.

### Prioridade Média (Médio Prazo)
5.  **Automação da Instalação Local:** Criar scripts ou instaladores (.exe) para Windows/Mac, reduzindo o esforço manual (M2.1) e facilitando a vida dos técnicos dos laboratórios de informática.

---

## 4.5. Conclusão Final

O software **Oppia** apresenta uma base tecnológica promissora e uma proposta pedagógica sólida. Entretanto, no estado atual, o sistema possui barreiras de entrada que conflitam com a realidade heterogênea de uma rede pública de ensino.

**Veredito para o Projeto Piloto:**
* **APROVADO** para uso controlado em **Laboratórios de Informática** (Desktops e Chromebooks), onde a portabilidade e instalação não são barreiras.
* **REPROVADO** para o modelo **"Traga seu próprio dispositivo" (BYOD)**, devido às falhas críticas no ecossistema mobile (Android e iOS).

A recomendação da equipe é iniciar o piloto apenas nos laboratórios e aguardar as correções de Prioridade Crítica antes de expandir o acesso para os dispositivos pessoais dos alunos.

---

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor |
| :---: | :---: | :--- | :--- | :--- |
| `1.0` | 16/11/2025 | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff) | |
| `2.0` | 29/11/2025 | Consolidação final dos resultados com tabelas de rastreabilidade e veredito | [Brunno Fernandes](https://github.com/brunnoff) |   [Bianca Patrocínio](https://github.com/BiancaPatrocinio7)  |