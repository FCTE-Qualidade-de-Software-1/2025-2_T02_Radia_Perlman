# 2. Resultados - Adequação Funcional

Esta seção apresenta os resultados consolidados da execução dos Casos de Teste de Adequação Funcional (CT-AF) e a análise dos dados coletados via formulário de avaliação com **6 participantes** (2 perfis Educador e 4 perfis Aluno).

## 2.1. Tabela de Execução (Resumo)

A tabela abaixo resume os resultados da execução dos Casos de Teste.

| ID do Teste | Título do Teste | Status | Observação |
| :--- | :--- | :---: | :--- |
| **CT-AF-01** | Completude Tarefas Essenciais (Educador) | **Passou** | Tarefas concluídas, mas com dificuldade devido ao idioma (Inglês). |
| **CT-AF-02** | Completude Tarefas Essenciais (Aluno) | **Passou** | Fluxo fluído, sem bloqueios. |
| **CT-AF-03** | Verificação de Precisão do Feedback | **Passou** | O feedback foi considerado claro e preciso. |
| **CT-AF-04** | Integridade e Recup. de Dados | **Passou com Restrições** | Os dados são recuperados, mas o sistema perde a configuração de idioma (volta para Inglês). |
| **CT-AF-05** | Integridade e Recup. de Dados (Educador) | **Passou** | Rascunhos salvos corretamente. |
| **CT-AF-06** | Funcionalidade de Pré-visualização | **Passou** | Funcionalidade mais bem avaliada (5/5). |
| **CT-AF-07** | Eficiência da Busca | **Falhou** | Relatos de resultados imprecisos e mistura de idiomas. |
| **CT-AF-08** | Avaliação Qualitativa (Likert) | **Coletado** | Média geral: 3.9. |

## 2.2. Análise Detalhada das Métricas

A análise quantitativa revela que, embora a plataforma seja funcionalmente robusta (completude e integridade), a experiência é prejudicada pela usabilidade da busca e barreiras linguísticas.

| Métrica | Resultado Medido | Hipótese (Fase 2) | Aprovado? |
| :--- | :--- | :--- | :---: |
| **M1.1: % Completude Tarefas** | **100%** | 98% | **Sim** |
| **M2.1: % Precisão Feedback** | **100%** | 100% | **Sim** |
| **M2.2: % Integridade Dados** | **100%** | 99.5% | **Sim** |
| **M3.1: % Buscas Bem-sucedidas**| **50%** | 85% | **Não** |
| **M3.2: Média Adequação (Likert)** | **3.9 / 5.0** | 4.0 / 5.0 | **Não** |

## 2.3. Discussão dos Resultados

Abaixo discute-se os desvios encontrados, justificando as métricas reprovadas com base nos relatos qualitativos dos participantes.

* **Q1: Completude Funcional (M1.1):**
    A métrica foi aprovada (100%), pois todos os usuários conseguiram chegar ao final dos fluxos propostos. Contudo, para o perfil **Educador**, a eficiência foi impactada negativamente pela interface híbrida.
    * *Evidência:* Um participante relatou que a interface em inglês foi *"o único ponto que dificultou a usabilidade"*, recebendo nota média de **1.5** na questão específica sobre a interface híbrida.

* **Q2: Correção Funcional e Integridade (M2.1 e M2.2):**
    A recuperação de dados funciona (o progresso é salvo), mas foi identificado um defeito funcional na manutenção do estado da sessão:
    * *Defeito:* Ao utilizar a função "Continuar de onde você parou", o sistema recupera o progresso pedagógico, mas **reseta a preferência de idioma para o Inglês**.
    * *Relato do Usuário:* *"Apesar de retornar ao ponto de controle, retornou na língua Inglês... não vi a opção para retornar para a língua Português"*.
    * A pré-visualização (Preview) e o Salvamento (Save Draft) obtiveram pontuação máxima (5.0) em quase todos os testes.

* **Q3: Apropriação Funcional e Busca (M3.1 e M3.2):**
    As métricas M3.1 (Busca) e M3.2 (Satisfação Geral) **não atingiram a meta**.
    * **Falha na Busca:** Usuários relataram que a busca retorna lições em idiomas misturados e tem dificuldade com termos específicos (*"Não apareceram lições com o tema e o título esperado"*). Sugeriu-se mover a barra de pesquisa para o topo da página.
    * **Navegação Confusa:** A aba "Metas" e "Progresso" gerou confusão. Um usuário mencionou: *"Não entendi muito bem o propósito da aba de metas e ela não pareceu funcionar corretamente"*.
    * **Ponto Positivo (Histórico):** A visualização de conquistas foi elogiada como uma ferramenta de gamificação (*"transforma o estudo em um jogo onde cada conclusão é uma vitória"*).

---

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor |
| :---: | :---: | :--- | :--- | :--- |
| `1.0` | 16/11/2025 | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff) | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) |
| `1.1` | 24/11/2025 | Preenchimento dos Resultados da Fase 4 com dados de 6 participantes | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) | [Brunno Fernandes](https://github.com/brunnoff)|