# 2. Casos de Teste - Adequação Funcional

Esta seção detalha os Casos de Teste (CTs) projetados para coletar os dados das métricas de Adequação Funcional (AF) definidas na Fase 2.

---

### CT-AF-01: Verificação de Completude de Tarefas Essenciais
* **Métrica Associada:** M1.1 (% Completude Tarefas Essenciais)
* **Objetivo:** Verificar se o fluxo principal do usuário (Educador e Aluno) pode ser completado sem impedimentos funcionais.
* **Pré-condições:** Acesso a duas contas de usuário (1 Educador, 1 Aluno).
* **Passos de Execução:**
    1.  [Educador] Fazer login e navegar para o "Painel do Criador".
    2.  [Educador] Criar uma nova "Exploration" (lição).
    3.  [Educador] Adicionar uma interação de "Múltipla Escolha".
    4.  [Educador] Publicar a lição.
    5.  [Aluno] Fazer login e navegar para o "Painel do Aprendiz".
    6.  [Aluno] Encontrar e iniciar a lição criada no passo 4.
    7.  [Aluno] Responder à questão e concluir a lição.
    8.  [Aluno] Verificar se a lição aparece como concluída no painel.
* **Resultado Esperado:** Todas as 8 etapas são concluídas com sucesso. A lição é criada, publicada, respondida e marcada como concluída.

---

### CT-AF-02: Verificação de Precisão do Feedback
* **Métrica Associada:** M2.1 (% Precisão Feedback)
* **Objetivo:** Avaliar a precisão do feedback para diferentes tipos de interação e respostas.
* **Pré-condições:** Uma lição de teste com 3 tipos de resposta (correta, incorreta-específica, incorreta-padrão) está disponível.
* **Passos de Execução:**
    1.  [Aluno] Acessar a lição de teste de feedback.
    2.  Submeter a resposta "Correta".
    3.  Submeter a resposta "Incorreta Específica".
    4.  Submeter uma resposta "Incorreta Padrão".
* **Resultado Esperado:** O feedback exibido em cada passo corresponde 100% ao feedback esperado para o tipo de resposta fornecida.

---

### CT-AF-03: Verificação de Integridade e Recuperação de Dados
* **Métrica Associada:** M2.2 (% Integridade e Recuperação Dados)
* **Objetivo:** Verificar se o progresso do aluno e os rascunhos do educador são salvos e recuperados corretamente após uma interrupção.
* **Passos de Execução (Aluno):**
    1.  [Aluno] Iniciar uma lição longa (múltiplas etapas).
    2.  Completar 50% da lição.
    3.  Fechar abruptamente o navegador/app.
    4.  Reabrir e fazer login. Tentar resumir a lição.
* **Passos de Execução (Educador):**
    1.  [Educador] Criar uma nova lição e escrever 3 parágrafos de texto.
    2.  Esperar o salvamento automático do rascunho.
    3.  Fechar abruptamente o navegador.
    4.  Reabrir e fazer login. Acessar o "Painel do Criador" e abrir o rascunho.
* **Resultado Esperado:** O progresso do aluno é retomado do ponto de parada. O rascunho do educador é recuperado integralmente.

---

### CT-AF-04: Verificação de Precisão de Notificações
* **Métrica Associada:** M2.3 (% Precisão Notificações)
* **Objetivo:** Avaliar a correção das notificações geradas pela plataforma.
* **Passos de Execução:**
    1.  Identificar um evento gatilho (ex: Educador atribui uma lição).
    2.  Executar a ação que dispara o evento.
    3.  Monitorar o canal de notificação (painel ou e-mail).
    4.  Verificar se a notificação chega, se o conteúdo está correto e estimar o tempo de entrega.
* **Resultado Esperado:** As notificações são entregues de forma correta e dentro do tempo limite definido na hipótese (95% de precisão).

---

### CT-AF-05: Verificação de Eficiência da Busca
* **Métrica Associada:** M3.1 (% Buscas Bem-sucedidas)
* **Objetivo:** Avaliar a relevância dos resultados da busca na biblioteca.
* **Passos de Execução:**
    1.  Executar 3 buscas com termos comuns (ex: "matemática", "frações", "história").
    2.  Analisar os 5 primeiros resultados de cada busca e classificar sua relevância.
* **Resultado Esperado:** A maioria dos resultados (conforme hipótese de 85%) é classificada como relevante.

---

### CT-AF-06: Avaliação Qualitativa (Likert)
* **Métrica Associada:** M3.2 (Média Adequação Funcionalidades)
* **Objetivo:** Coletar a percepção de adequação dos usuários (equipe) após a execução dos testes.
* **Passos de Execução:**
    1.  Criar um questionário (Google Forms) com a pergunta: "Em uma escala de 1 a 5, quão adequadas são as funcionalidades do Oppia para ensino e aprendizado?".
    2.  Após a conclusão dos CTs, cada avaliador deve preencher o formulário.
* **Resultado Esperado:** Os dados (notas de 1 a 5) são coletados para cálculo da média.

---

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor |
| :---: | :---: | :--- | :--- | :--- |
| `1.0` | 16/11/2025 | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff) | |