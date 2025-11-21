# 2. Casos de Teste - Adequação Funcional

Esta seção tem o propósito de detalhar os Casos de Teste (CTs) projetados para realizar a execução da avaliação relacionada à característica de Adequação Funcional (AF). Cada CT é associado a uma das métricas anteriormente definidas na Fase 2, na qual essas estão atreladas a uma Questão que serve como base do plano de medição.

---

### CT-AF-01: Verificação de Completude de Tarefas Essenciais - *Educador*
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

### CT-AF-02: Verificação de Completude de Tarefas Essenciais - *Aluno*
* **Métrica Associada:** M1.1 (% Completude Tarefas Essenciais)
* **Objetivo:** Verificar se o fluxo principal do Aluno pode ser completado sem impedimentos funcionais.
* **Pré-condições:** Acesso a uma conta de Aluno. Uma lição publicada disponível na plataforma.
* **Passos de Execução:**
    1.  Fazer login e navegar para o "Painel do Aprendiz".
    2.  Selecionar uma lição disponível.
    3.  Avançar a lição e responder as questões até finalizar a lição.
    4.  Verificar se a lição no Painel do Aprendiz consta como concluída.
* **Resultado Esperado:** Todas as 4 etapas são concluídas com sucesso. A lição é respondida e marcada como concluída.

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

### CT-AF-04: Verificação de Integridade e Recuperação de Dados - *Aluno*
* **Métrica Associada:** M2.2 (% Integridade e Recuperação Dados)
* **Objetivo:** Verificar se o progresso do aluno é salvo e recuperado corretamente após uma interrupção.
* **Pré-condições:** Acesso a uma conta de Aluno. Uma lição longa (múltiplas etapas) disponível na plataforma.
* **Passos de Execução:**
    1.  Iniciar uma lição longa (múltiplas etapas).
    2.  Verificar no Painel do Aprendiz se a lição consta como iniciada.
    3.  Completar 50% da lição.
    4.  Fechar abruptamente o navegador/app.
    5.  Reabrir e fazer login.
    6.  Verificar se a lição salvou o ponto de controle.
* **Resultado Esperado:** O progresso do aluno é retomado do ponto de parada.

---

### CT-AF-05: Verificação de Integridade e Recuperação de Dados - *Educador*
* **Métrica Associada:** M2.2 (% Integridade e Recuperação Dados)
* **Objetivo:** Verificar se os rascunhos do educador são salvos e recuperados corretamente após uma interrupção.
* **Pré-condições:** Acesso a uma conta de Educador.
* **Passos de Execução:**
    1.  Fazer login e navegar para o "Painel do Criador".
    2.  Criar uma nova Exploração (lição).
    3.  Adicionar um texto de introdução e a pergunta clicando no ícone de lápis e depois salvar clicando em "Save Content".
    4.  Fechar abruptamente o navegador.
    5.  Reabrir e fazer login. Acessar o "Painel do Criador" e abrir o rascunho.
* **Resultado Esperado:** O rascunho do educador é recuperado integralmente.

---

### CT-AF-06: Verificação de Precisão de Notificações - *Educador & Aluno*
* **Métrica Associada:** M2.3 (% Precisão Notificações)
* **Objetivo:** Avaliar a correção e a pontualidade das notificações geradas pela plataforma após um evento gatilho que conecta os perfis Educador e Aluno.
* **Pré-condições:**
    * Existência de duas contas de teste: `Conta_Educador` e `Conta_Aluno`.
    * A `Conta_Educador` possui uma lição publicada (criada no CT-AF-01).
    * A plataforma deve possuir uma funcionalidade de "Atribuir" ou "Recomendar" lição (se não possuir, o teste deve ser adaptado para outro evento, como "feedback em lição").
* **Passos de Execução:**
    1.  **[Perfil Educador]:** Fazer login como `Conta_Educador`.
    2.  Navegar até o "Painel do Criador" e selecionar a lição publicada.
    3.  Localizar e utilizar a funcionalidade de "Atribuir" (ou "Recomendar") a lição para o usuário `Conta_Aluno`.
    4.  Registrar o horário exato da ação (H:MM:SS) para medir a pontualidade.
    5.  **[Perfil Aluno]:** Fazer login como `Conta_Aluno`.
    6.  Monitorar os canais de notificação definidos (ex: Painel do Aprendiz, ícone de notificação no topo, e-mail da conta) por 5 minutos (conforme hipótese da M2.3).
* **Resultado Esperado:**
    1.  A notificação é recebida pelo `Conta_Aluno` dentro do tempo limite definido na hipótese (5 minutos).
    2.  O conteúdo da notificação está funcionalmente correto (menciona a lição correta e o educador correto).
    3.  Se houver um link na notificação, ele direciona o aluno para o local esperado (a lição).
* ***Nota de Teste:*** *Caso a funcionalidade "Atribuir Lição" não seja encontrada, este CT deve ser marcado como "Não Aplicável (N/A)" e a métrica M2.3 deve ser reavaliada com base em outro evento gatilho.*

---

### CT-AF-07: Verificação de Eficiência da Busca
* **Métrica Associada:** M3.1 (% Buscas Bem-sucedidas)
* **Objetivo:** Avaliar objetivamente a relevância dos resultados da busca na biblioteca, conforme a hipótese da M3.1 (85% de relevância).
* **Pré-condições:**
    * Acesso à biblioteca pública de lições (sem necessidade de login).
    * **Definição de Relevância (Obrigatória):** Um resultado nos "top 5" é considerado "Relevante" se o título ou a descrição da lição contiver o termo de busca exato ou um sinônimo claro e direto.
* **Passos de Execução:**

    **Teste de Relevância:** Definir 3 termos de busca com alta expectativa de resultados (ex: "Math", "History", "Physics").
   
    1. Para cada termo, executar a busca.
    2. Analisar os 5 primeiros resultados.
    3. Classificar cada um como "Relevante" ou "Não Relevante" (conforme a Definição de Relevância).
    4. Registrar a contagem (ex: 4/5 relevantes para "Math").

    **Teste de Robustez (Erro de Digitação):** Definir 1 termo com erro de digitação comum (ex: "Programacao" sem til ou "Phisics").

    1. Executar a busca.
    2. Verificar se a plataforma sugere a correção ("Você quis dizer: ...?") ou se retorna resultados relevantes mesmo com o erro.

    **Teste de Feedback (Termo Inválido):** Definir 1 termo aleatório/inválido (ex: "asdfqwerzxcv").

    1. Executar a busca.
    2. Verificar se a plataforma exibe uma mensagem clara de "Nenhum resultado encontrado".

* **Resultado Esperado:**
    1.  O total de resultados relevantes (dos 15 analisados no Passo 1) atinge a hipótese da M3.1 (ex: 13/15 = 86.7%, que é ≥ 85%).
    2.  O teste do Passo 2 (Robustez) retorna sugestões úteis ou resultados relevantes.
    3.  O teste do Passo 3 (Feedback) exibe uma mensagem clara de "nenhum resultado".

---

### CT-AF-08: Avaliação Qualitativa (Likert) - *Equipe de Avaliação*
* **Métrica Associada:** M3.2 (Média Adequação Funcionalidades)
* **Objetivo:** Coletar a percepção de adequação da equipe de avaliação, *segmentada por perfil de uso*, após a execução dos testes.
* **Pré-condições:**
    * Toda a equipe de avaliação [N=X membros] deve ter concluído os CTs anteriores (CT-AF-01 a CT-AF-07), de acordo com o seu perfil.
* **Passos de Execução:**
    1.  Criar um questionário (Google Forms) e distribuí-lo aos [N] avaliadores.
    2.  O formulário deve usar a escala Likert (1=Totalmente Inadequado, 5=Totalmente Adequado) e ser dividido nas seguintes seções:

    **Formulário de Percepção (M3.2)**

    **Seção 1: Perfil EDUCADOR (Apropriação Funcional)**
    *(Baseado na experiência dos testes CT-AF-01 e CT-AF-05)*

    * **Q1.1:** Quão adequado é o processo de **configurar as interações** da lição (ex: Múltipla Escolha, Inserção de Texto)?
    * **Q1.2:** Quão adequado e flexível é o processo de **definir os feedbacks** para respostas corretas, incorretas e padrões?
    * **Q1.3:** Quão adequado é o processo de **gerenciar o fluxo** da lição (ex: criar e ligar novos cartões de conteúdo)?
    * **Q1.4:** Quão confiável e adequado foi o processo de **Salvar e Recuperar Rascunhos** (CT-AF-05)?
    * **Q1.5:** Quão adequadas são as funções para **publicar** e gerenciar o estado final de uma lição (de rascunho para pública)?

    **Seção 2: Perfil ALUNO (Apropriação Funcional)**
    *(Baseado na experiência dos testes CT-AF-02, CT-AF-03, CT-AF-04 e CT-AF-07)*

    * **Q2.1:** Quão adequadas são as funções para **encontrar e iniciar** uma lição (via Painel do Aprendiz ou Busca na Biblioteca)?
    * **Q2.2:** Quão adequado é o **fluxo de navegação e resposta** durante uma lição (avançar, responder, ver o progresso)?
    * **Q2.3:** Quão claro, útil e adequado foi o **Feedback recebido** (correto/incorreto) durante a lição (CT-AF-03)?
    * **Q2.4:** Quão confiável e adequada foi a **recuperação do seu progresso** após uma interrupção (CT-AF-04)?
    * **Q2.5:** Quão clara foi a **conclusão** da lição e a sua respectiva marcação no Painel do Aprendiz (CT-AF-02)?

    3.  Coletar as [N] respostas.
* **Resultado Esperado:**
    1.  Os dados (notas de 1 a 5 para as 10 perguntas) são coletados de todos os [N] avaliadores.
    2.  Os dados estão claramente segmentados por Perfil (Educador/Aluno), prontos para o cálculo da média (M3.2) na Fase 4.


## Histórico de Versões

| Versão |    Data    | Descrição                                                 | Autor                                                       | Revisor                                                     |
| :----: | :--------: | :-------------------------------------------------------- | :---------------------------------------------------------- | :---------------------------------------------------------- |
| `1.0`  | 16/11/2025 | Criação da estrutura inicial da página                    | [Brunno Fernandes](https://github.com/brunnoff)             | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) |
| `1.1`  | 17/11/2025 | Criação do CT-AF-01 - 05                                  | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7)   |
| `1.2`  | 17/11/2025 | Criação dos CTs 06, 07, 08 e adição de perfis nos títulos | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7)   | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) |