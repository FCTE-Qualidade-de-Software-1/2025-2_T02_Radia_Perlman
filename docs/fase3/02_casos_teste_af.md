# 2. Casos de Teste - Adequação Funcional

Esta seção tem o propósito de detalhar os Casos de Teste (CTs) projetados para realizar a execução da avaliação relacionada à característica de Adequação Funcional (AF). Cada CT é associado a uma das métricas anteriormente definidas na Fase 2, na qual essas estão atreladas a uma Questão que serve como base do plano de medição.


---

### CT-AF-01: Verificação de Completude de Tarefas Essenciais - Educador
* **Métrica Associada:** M1.1 (% Completude Tarefas Essenciais)
* **Objetivo:** Verificar se o fluxo principal do Educador pode ser completado sem impedimentos funcionais.
* **Pré-condições:** Acesso a uma conta de Educador.
* **Passos de Execução:**
    1.  Fazer login e navegar para o "Painel do Criador".
    2.  Criar uma nova Exploração (lição).
    3.  Adicionar um texto de introdução e a pergunta clicando no ícone de lápis e depois salvar clicando em "Save Content".
    4.  Adicionar uma interação de "Multiple Choice" (Múltipla Escolha).
    5.  Adicionar 4 opções de resposta e clicar em "Save Interaction".
    6.  Selecionar uma resposta correta, adicionar texto de resposta do Oppia, no campo "And afterwards, directs the learner to ..." alterar de "(try again)" para "A New Card Called...", adicionar nome do novo card, marcar a caixa "The answers in this group are correct", salvar no botão "Save".
    7.  Alterar o componente "All other answers", adicionar texto de resposta do Oppia clicando em "Save Feedback".
    8.  Em "Exploration Overview" selecionar o novo card criado.
    9.  Adicionar uma interação "End Exploration".
    10. Salvar a lição.
    11. Publicar a lição.
* **Resultado Esperado:** Todas as 11 etapas são concluídas com sucesso. A lição é criada e publicada.

---

### CT-AF-02: Verificação de Completude de Tarefas Essenciais - Aluno
* **Métrica Associada:** M1.1 (% Completude Tarefas Essenciais)
* **Objetivo:** Verificar se o fluxo principal do Aluno pode ser completado sem impedimentos funcionais.
* **Pré-condições:** Acesso a uma conta de Aluno. Uma lição publicada disponível na plataforma.
* **Passos de Execução:**
    1.  Fazer login e navegar para o "Painel do Aprendiz".
    2.  Selecionar uma lição disponível.
    3.  Avançar a lição e responder as questões até atingir um ponto de controle.
    4.  Verificar no Painel do Aprendiz se a lição consta como iniciada.
    5.  Verificar se a lição salvou o ponto de controle.
    6.  Finalizar a lição        .
    7.  Verificar se a lição no Painel do Aprendiz consta como concluída.
* **Resultado Esperado:** Todas as 6 etapas são concluídas com sucesso. A lição é respondida e marcada como concluída.

---

### CT-AF-03: Verificação de Precisão do Feedback
* **Métrica Associada:** M2.1 (% Precisão Feedback)
* **Objetivo:** Avaliar a precisão do feedback para diferentes tipos de interação e respostas.
* **Pré-condições:** Uma lição de teste com 3 tipos de resposta (correta, incorreta-específica, incorreta-padrão) está disponível.
* **Passos de Execução:**
    1.  [Aluno] Acessar a lição de teste de feedback disponibilizada.
    2.  Responder com todas as respostas "Incorreta" disponíveis.
    3.  Responder com a resposta "Correta".
* **Resultado Esperado:** Independente da resposta escolhida o usuário deve receber um feedback detalhando se a resposta estava incorreta e correta.

---

### CT-AF-04: Verificação de Integridade e Recuperação de Dados
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

### CT-AF-05: Verificação de Precisão de Notificações
* **Métrica Associada:** M2.3 (% Precisão Notificações)
* **Objetivo:** Avaliar a correção das notificações geradas pela plataforma.
* **Passos de Execução:**
    1.  Identificar um evento gatilho (ex: Educador atribui uma lição).
    2.  Executar a ação que dispara o evento.
    3.  Monitorar o canal de notificação (painel ou e-mail).
    4.  Verificar se a notificação chega, se o conteúdo está correto e estimar o tempo de entrega.
* **Resultado Esperado:** As notificações são entregues de forma correta e dentro do tempo limite definido na hipótese (95% de precisão).

---

### CT-AF-06: Verificação de Eficiência da Busca
* **Métrica Associada:** M3.1 (% Buscas Bem-sucedidas)
* **Objetivo:** Avaliar a relevância dos resultados da busca na biblioteca.
* **Passos de Execução:**
    1.  Executar 3 buscas com termos comuns (ex: "matemática", "frações", "história").
    2.  Analisar os 5 primeiros resultados de cada busca e classificar sua relevância.
* **Resultado Esperado:** A maioria dos resultados (conforme hipótese de 85%) é classificada como relevante.

---

### CT-AF-07: Avaliação Qualitativa (Likert)
* **Métrica Associada:** M3.2 (Média Adequação Funcionalidades)
* **Objetivo:** Coletar a percepção de adequação dos usuários (equipe) após a execução dos testes.
* **Passos de Execução:**
    1.  Criar um questionário (Google Forms) com a pergunta: "Em uma escala de 1 a 5, quão adequadas são as funcionalidades do Oppia para ensino e aprendizado?".
    2.  Após a conclusão dos CTs, cada avaliador deve preencher o formulário.
* **Resultado Esperado:** Os dados (notas de 1 a 5) são coletados para cálculo da média.

---

## Histórico de Versões

| Versão |    Data    | Descrição                              | Autor                                                       | Revisor                                                     |
| :----: | :--------: | :------------------------------------- | :---------------------------------------------------------- | :---------------------------------------------------------- |
| `1.0`  | 16/11/2025 | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff)             | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) |
| `1.1`  | 17/11/2025 | Criação do CT-AF-01 e CT-AF-02         | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) |                                                             |