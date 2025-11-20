# 2. Casos de Teste - Adequação Funcional

Esta seção tem o propósito de detalhar os Casos de Teste (CTs) projetados para realizar a execução da avaliação relacionada à característica de Adequação Funcional (AF). Cada CT é associado a uma das métricas anteriormente definidas na Fase 2, na qual essas estão atreladas a uma Questão que serve como base do plano de medição.

---

### CT-AF-01: Verificação de Completude de Tarefas Essenciais - *Educador*
* **Métrica Associada:** M1.1 (% Completude Tarefas Essenciais)
* **Objetivo:** Verificar se o fluxo principal do Educador pode ser completado sem impedimentos funcionais, considerando a interface híbrida (Português/Inglês).
* **Pré-condições:** Acesso a uma conta de Educador.
* **Passos de Execução:**
    1.  Fazer login e navegar para o "**Painel de Criador**".
    2.  Clicar no botão verde "**+ CRIAR EXPLORAÇÃO**".
    3.  No editor (em inglês), clicar no card "Introduction" para editar, adicionar conteúdo e salvar.
    4.  Clicar no botão "**+ ADD INTERACTION**" na seção Interaction.
    5.  No modal "Choose Interaction", selecionar "**Multiple Choice**".
    6.  No modal "Customize Interaction", preencher as opções de resposta e clicar em "**Save Interaction**".
    7.  Clicar no botão "**ADD RESPONSE**" ou abrir a resposta criada.
    8.  No modal "Add Response", configurar o campo "**And afterwards, directs the learner to ...**" selecionando "**A New Card Called...**" e digitando "END" (ou outro nome).
    9.  Marcar a checkbox "**The answers in this group are correct**" e clicar em "**Save Response**".
    10. Na visão geral ("Exploration Overview"), clicar no novo card criado ("END").
    11. Adicionar a interação "**End Exploration**".
    12. Clicar no botão "**Save Draft**" no topo direito. No modal "**Add Some Details**", preencher Título, Objetivo, Categoria e Idioma, e clicar em "**Save Changes**".
* **Resultado Esperado:** Todas as etapas são concluídas com sucesso. A lição é salva, os cards são conectados corretamente no grafo de visão geral e os metadados são registrados.

---

### CT-AF-02: Verificação de Completude de Tarefas Essenciais - *Aluno*
* **Métrica Associada:** M1.1 (% Completude Tarefas Essenciais)
* **Objetivo:** Verificar se o fluxo principal do Aluno pode ser completado sem impedimentos funcionais.
* **Pré-condições:** Acesso a uma conta de Aluno. Uma lição publicada disponível na plataforma.
* **Passos de Execução:**
    1.  Fazer login e acessar o "Painel do aprendiz".
    2.  No menu lateral, clicar em "Aulas da comunidade" (ou selecionar uma lição em "Início").
    3.  Escolher uma lição, avançar o conteúdo e responder às interações até a conclusão.
    4.  Retornar ao Painel e verificar no menu "Progresso" ou "Concluídas" se a lição foi contabilizada.
* **Resultado Esperado:** Todas as etapas são concluídas com sucesso. A lição é respondida e marcada como concluída no histórico do aluno.

---

### CT-AF-03: Verificação de Precisão do Feedback
* **Métrica Associada:** M2.1 (% Precisão Feedback)
* **Objetivo:** Avaliar a precisão do feedback para diferentes tipos de interação e respostas.
* **Pré-condições:** Uma lição de teste configurada com regra de resposta específica.
* **Passos de Execução:**
    1.  [Aluno] Acessar a lição de teste de feedback disponibilizada.
    2.  Responder propositalmente com uma opção configurada como "Incorreta".
    3.  Verificar se o feedback configurado no campo "**Oppia tells the learner...**" (visto no editor) é exibido.
    4.  Responder com a resposta "Correta".
* **Resultado Esperado:** O feedback visual e textual corresponde exatamente à configuração realizada no modal "Add Response" do editor.

---

### CT-AF-04: Verificação de Integridade e Recuperação de Dados - *Aluno*
* **Métrica Associada:** M2.2 (% Integridade e Recuperação Dados)
* **Objetivo:** Verificar se o progresso do aluno é salvo e recuperado corretamente na seção "Continuar de onde você parou".
* **Pré-condições:** Acesso a uma conta de Aluno. Lição longa disponível.
* **Passos de Execução:**
    1.  Iniciar uma lição longa.
    2.  Completar parcialmente a lição.
    3.  Fechar abruptamente o navegador.
    4.  Reabrir e fazer login.
    5.  No menu "Início", verificar a seção **"Continuar de onde você parou"**.
    6.  Clicar na lição e verificar o ponto de retorno.
* **Resultado Esperado:** A lição aparece na seção de continuidade e o progresso é retomado do ponto exato de parada.

---

### CT-AF-05: Verificação de Integridade e Recuperação de Dados - *Educador*
* **Métrica Associada:** M2.2 (% Integridade e Recuperação Dados)
* **Objetivo:** Verificar se os rascunhos do educador são salvos e recuperados corretamente.
* **Pré-condições:** Acesso a uma conta de Educador.
* **Passos de Execução:**
    1.  Fazer login e navegar para o "**Painel de Criador**".
    2.  Criar ou editar uma exploração.
    3.  Realizar uma alteração (ex: Adicionar uma interação).
    4.  Clicar no botão verde "**Save Draft**" no canto superior direito.
    5.  Fechar abruptamente o navegador ou sair sem publicar.
    6.  Reabrir, fazer login e acessar o "Painel de Criador".
* **Resultado Esperado:** O rascunho da exploração aparece na lista e, ao abrir, contém as últimas alterações salvas (Version History deve refletir o estado).

---

### CT-AF-06: Verificação da Funcionalidade de Pré-visualização - *Educador*
* **Métrica Associada:** M1.1 (% Completude Tarefas Essenciais)
* **Objetivo:** Verificar se o modo de pré-visualização reflete fielmente o comportamento da lição configurada, permitindo ao educador validar o conteúdo sem precisar publicar.
* **Pré-condições:** Acesso a uma conta de Educador com uma exploração em rascunho contendo pelo menos uma interação.
* **Passos de Execução:**
    1.  No "Exploration Editor", localizar e clicar no ícone de **"Play" (Preview)** na barra de navegação superior (ao lado do ícone de lápis).
    2.  Verificar se a interface muda para o modo de visualização do aluno.
    3.  Interagir com o card apresentado (ex: selecionar uma opção de "Multiple Choice" e enviar).
    4.  Confirmar se o feedback e o redirecionamento ocorrem conforme configurado no editor.
    5.  Clicar no ícone de **"Lápis" (Editor)** na barra superior para retornar ao modo de edição.
* **Resultado Esperado:**
    1.  O modo de pré-visualização é ativado instantaneamente.
    2.  A interação comporta-se exatamente como configurado (feedback e transição de cards).
    3.  É possível retornar ao modo de edição sem perda de dados.

---

### CT-AF-07: Verificação de Eficiência da Busca
* **Métrica Associada:** M3.1 (% Buscas Bem-sucedidas)
* **Objetivo:** Avaliar a relevância dos resultados da busca.
* **Passos de Execução:**
    1.  Usar a barra de busca "Sobre o que você está curioso?".
    2.  Testar termos exatos ("Math"), termos com erro ("Fisica") e termos inválidos.
* **Resultado Esperado:** Resultados coerentes com a categoria pesquisada (ex: cards de Matemática para a busca "Math").

---

### CT-AF-08: Avaliação Qualitativa (Likert) - *Equipe de Avaliação*
* **Métrica Associada:** M3.2 (Média Adequação Funcionalidades)
* **Objetivo:** Coletar a percepção subjetiva da equipe sobre a adequação, clareza e facilidade de uso das funcionalidades críticas testadas nos casos anteriores.
* **Passos de Execução:**
    1.  Distribuir um formulário eletrônico (ex: Google Forms) para os membros da equipe que executaram os testes.
    2.  Solicitar que avaliem os itens abaixo usando uma **Escala Likert de 1 a 5** (1 = Totalmente Inadequado/Difícil, 5 = Totalmente Adequado/Fácil).
    
    **Perfil EDUCADOR (Foco no Editor e Criação):**

    * **Q1:** Quão intuitivo foi o uso do modal **"Choose Interaction"** para selecionar o tipo de atividade (ex: Múltipla Escolha)?
    * **Q2:** Quão claro é o processo de configurar o redirecionamento de fluxo (criar novos cards/cenários) dentro da janela **"Add Response"**?
    * **Q3:** O quanto a ferramenta de **Pré-visualização (Ícone Play)** refletiu fielmente o comportamento final da lição?
    * **Q4:** Quão adequado é o processo de salvamento (**"Save Draft"**), considerando a exigência de preencher metadados (Título/Objetivo) a cada versão?
    * **Q5:** O quanto a **interface híbrida** (Painel em Português vs. Editor em Inglês) impactou a fluidez da criação da lição?

    **Perfil ALUNO (Foco no Aprendizado e Navegação):**

    * **Q6:** Quão fácil foi localizar novas lições utilizando a seção **"Aulas da comunidade"** ou a barra de busca?
    * **Q7:** Quão eficaz foi a seção **"Continuar de onde você parou"** para retomar uma lição interrompida?
    * **Q8:** Quão claro e útil foi o **feedback visual/textual** apresentado ao errar uma questão propositalmente?
    * **Q9:** Quão intuitiva é a navegação entre as abas do painel (**Início, Metas, Progresso**)?
    * **Q10:** Quão adequada é a visualização do seu histórico de conquistas e lições concluídas?

    3.  Compilar as respostas e calcular a média aritmética para a métrica M3.2.
* **Resultado Esperado:** Média de satisfação calculada e comentários qualitativos sobre os pontos de dor (ex: barreira linguística no editor).

## Histórico de Versões

| Versão |    Data    | Descrição                              | Autor                                                       | Revisor                                                     |
| :----: | :--------: | :------------------------------------- | :---------------------------------------------------------- | :---------------------------------------------------------- |
| `1.0`  | 16/11/2025 | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff)             | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) |
| `1.1`  | 17/11/2025 | Criação do CT-AF-01 e CT-AF-02         | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) |[Bianca Patrocínio](https://github.com/BiancaPatrocinio7) |
| `1.2`  | 17/11/2025 | Criação dos CTs 06, 07, 08             | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) ||
| `1.3`  | 20/11/2025 | Ajuste dos CTs de Aluno.  Atualização dos CTs de Educador conforme terminologia em Inglês do Editor.Substituição do CT-AF-06 (Notificações) por Teste de Pré-visualização                | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) ||
