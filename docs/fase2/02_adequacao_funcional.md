## 2. Característica: Adequação Funcional

A Adequação Funcional é avaliada para garantir que o Oppia cumpra suas promessas como ferramenta de ensino, entregando as funcionalidades de forma completa, correta e apropriada aos seus objetivos. Esta página detalha o GQM para esta característica.

## 2.1 Objetivo de Medição de Adequação Funcional

<p align="center"> Tabela 1: Formalização do Objetivo de Medição (GQM) para Adequação Funcional </a> </p>


|        Dimensão           |                   Descrição                     |
| ------------------------- | ----------------------------------------------- |
| Analisar a      | Plataforma Oppia (Interface Web e App Mobile).                       |
| Com o propósito de                 | Avaliar se as funcionalidades essenciais de criação e aprendizado atendem aos requisitos de forma eficaz.     |
| Com respeito a | Adequação Funcional                               | 
| Perspectiva de Avaliação  | Educadores (criadores de conteúdo) e Estudantes (usuários finais).                             |
| Contexto                  | Projeto acadêmico da disciplina de Qualidade de Software.       |

<font size="3"><p style="text-align: center">Fonte: Autoria própria (2025)</p></font>

## Questões e Métricas

### Q1. Quanto à **Completude Funcional**, o "Painel do Criador" oferece todas as ferramentas essenciais para que um educador crie e publique uma lição interativa (exploração)?

  * **Métrica:** Percentual de completude de tarefas de criação = (Nº de tarefas essenciais de criação concluídas com sucesso / Nº total de tarefas essenciais de criação) \* 100.

### Q2. Quanto à **Correção Funcional**, o progresso do estudante no "Painel do Aprendiz" é salvo e recuperado corretamente entre diferentes sessões de uso?

  * **Métrica:** Taxa de sucesso no salvamento de progresso = (Nº de testes de salvamento e recuperação de progresso bem-sucedidos / Nº total de testes executados) \* 100.

### Q3. Quanto à **Correção Funcional**, o sistema fornece feedback imediato e correto com base nas respostas (certas ou erradas) fornecidas pelo estudante?

  * **Métrica:** Taxa de precisão do feedback = (Nº de feedbacks correspondentes à resposta do aluno / Nº total de feedbacks avaliados) \* 100.

### Q4. Quanto à **Apropriação Funcional**, as funcionalidades disponíveis para os estudantes (navegar, responder, ver progresso) são adequadas para atingir o objetivo de aprendizado interativo?

  * **Métrica:** (Qualitativa) Avaliação da adequação das funcionalidades do "Painel do Aprendiz" em relação aos cenários de uso definidos para os estudantes.

### Q5. Quanto à **Completude Funcional**, a documentação de instalação da plataforma Oppia contém todos os passos necessários para uma configuração bem-sucedida do ambiente?

  * **Métrica:** Taxa de sucesso na instalação via documentação = (Nº de instalações bem-sucedidas seguindo o guia / Nº total de tentativas de instalação) \* 100.

### Q6. Quanto à **Correção Funcional**, o sistema mantém a integridade dos dados quando múltiplos criadores editam explorações simultaneamente ou quando ocorrem falhas de conexão?

  * **Métrica:** Taxa de integridade de dados = (Nº de operações de edição concorrentes ou sob falha que preservaram os dados corretamente / Nº total de operações testadas) \* 100.

### Q7. Quanto à **Correção Funcional**, o sistema de notificações e alertas (ex: submissões de estudantes, atualizações de lições) entrega as mensagens de forma precisa e no momento adequado?

  * **Métrica:** Taxa de precisão de notificações = (Nº de notificações entregues corretamente e no tempo esperado / Nº total de eventos que deveriam gerar notificações) \* 100.

### Q8. Quanto à **Apropriação Funcional**, o sistema de busca e filtros permite que estudantes e educadores encontrem explorações relevantes de forma eficiente usando critérios como tópico, nível de dificuldade e idioma?

  * **Métrica (Quantitativa):** Taxa de sucesso na busca = (Nº de buscas que retornaram resultados relevantes nos primeiros 5 resultados / Nº total de buscas executadas) \* 100.
  * **Métrica (Qualitativa):** Avaliação da adequação dos filtros disponíveis em relação aos cenários de uso definidos (análise heurística dos critérios de busca disponíveis vs. necessidades documentadas).
-----

## Referências Bibliográficas

> SOUZA, Fernando Mauro de et al. **Uso do GQM para Avaliar Documentos de Utilização de Framework**. Anais do III Workshop de Qualidade de Software. v. 1, p. 75-82, 2008.
>
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. **ISO/IEC 25010:2011**. *Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models*. Genebra: ISO, 2011.

## Histórico de Versões

| Versão | Data       | Descrição                               | Autor                                                     | Revisor                                                   |
| :----: | ---------- | --------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `1.0`  | 14/10/2025 | Criação da estrutura inicial da página  | [Brunno Fernandes](https://github.com/brunnoff)           | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) |
| `1.1`  | 14/10/2025 | Adicionando tabela, questões e métricas | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) | [Pedro Lucas Dourado](https://github.com/lucasdray)       |
| `2.0`  | 14/10/2025 | Adição de 3 novas questões (Q6-Q8)      | [Pedro Lucas Dourado](https://github.com/lucasdray)       |                                                           |

