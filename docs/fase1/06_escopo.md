# 6. Escopo e Profundidade da Avaliação

A definição do escopo é fundamental para garantir que a avaliação seja focada e alinhada ao seu propósito. A análise se concentrará nas características de **Adequação Funcional** e **Portabilidade**, com base no modelo de qualidade da norma ISO/IEC 25010 [^1].

### 6.1. Justificativa da Escolha das Características
A seleção das características de qualidade a serem avaliadas foi uma decisão estratégica, baseada no propósito fundamental do software Oppia e no impacto direto sobre seus stakeholders.

* **Por que Adequação Funcional?**

    A Adequação Funcional vai além de apenas corrigir bugs; ela garante que o Oppia cumpra sua principal promessa: ser uma ferramenta de ensino eficaz e interativa. Para os **educadores**, isso se traduz em confiança de que suas lições podem ser criadas e gerenciadas sem problemas. Para os **estudantes**, significa uma jornada de aprendizado sem interrupções, onde o progresso é salvo corretamente e o feedback é útil. Por isso, avaliar se a plataforma funciona como esperado é o passo mais essencial.

* **Por que Portabilidade?**

    A missão do Oppia é democratizar o acesso à educação de qualidade, especialmente para comunidades com menos oportunidades [^2]. A Portabilidade é a característica de qualidade que materializa essa missão. Ela mede a capacidade do software de operar em diversos ambientes, diferentes sistemas operacionais, navegadores e, crucialmente, em dispositivos móveis com potencial de uso offline. Em um cenário global com grande diversidade tecnológica e acesso desigual à internet, a portabilidade não é apenas detalhe um técnico, mas um pilar para a **inclusão digital**. Avaliar a portabilidade é verificar se o Oppia pode, de fato, chegar aonde mais se precisa dele.

### 6.2. Objetos de Avaliação (O Quê Será Avaliado)
* **Interface de Criação de Conteúdo (Web):** Serão avaliadas as telas e ferramentas do "Painel do Criador", que é o ambiente onde os educadores criam e gerenciam as lições.
* **Interface de Aprendizagem (Web e App):** A análise cobrirá a jornada do estudante ao consumir e acompanhar o conteúdo no "Painel do Aprendiz", tanto na plataforma web quanto no aplicativo móvel.
* **Documentação de Instalação:** Também serão verificados os guias e o processo para colocar a plataforma em funcionamento.

<div class="figure">
  <p class="figure-title">Figura 1 – Painel de opções do Oppia</p>
  <img src="https://fcte-qualidade-de-software-1.github.io/2025-2_T02_Radia_Perlman/assets/images/painel.png" alt="Painel de opções do Oppia" width="250">
  <p class="figure-source">Fonte: <a href="https://www.oppia.org/" target="_blank">Print de tela (Bianca Patrocínio)</a></p>
</div>


### 6.3. Profundidade da Avaliação (Nível de Detalhe)
A avaliação terá uma **profundidade qualitativa**, com foco em verificar a existência e o funcionamento das principais funcionalidades em cenários de uso prático. A análise se concentrará em responder se as tarefas essenciais podem ser concluídas pelos públicos-alvo (estudantes e educadores) nos ambientes propostos.

---

### 6.4. Delimitação do Escopo e Fora do Escopo
* **Fora do Escopo Nesta Fase:**
    * **Desempenho, Segurança e Manutenibilidade:** Ficam de fora por exigirem uma análise técnica aprofundada que extrapola os recursos e o cronograma desta fase do projeto.
    * **Usabilidade:** Conforme as regras do trabalho, a avaliação não se aprofundará em aspectos subjetivos de "facilidade de uso", mas sim na disponibilidade e correção das funcionalidades.

### 6.5. Limites de Validade dos Resultados
Os resultados desta avaliação são válidos apenas para a versão específica do Oppia testada e devem ser vistos como **insights qualitativos** de uma amostra pequena, não representando estatisticamente toda a base de usuários da plataforma.

### 6.6. Avaliações Futuras (Plano de Cobertura Progressiva)
Este projeto é a primeira etapa de uma análise mais ampla. Os resultados servirão como base para avaliações futuras que poderão incluir testes de manutenibilidade, desempenho e uma auditoria de segurança completa, aprofundando a análise de qualidade de forma estruturada.

---

## Referências

[^1]: INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. **ISO/IEC 25010:2011**. *Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models*. Genebra: ISO, 2011.
[^2]: OPPIA FOUNDATION. **About Oppia**. Disponível em: <https://www.oppia.org/about>. Acesso em: 28 set. 2025.

---

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor |
| :---: | :---: | :--- | :--- | :--- |
| `1.0` | 28/09/2025 | Criação da estrutura inicial da página | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) | [Brunno Fernandes](https://github.com/brunnoff) |
| `1.1` | 29/09/2025 | Refinamento do escopo com público-alvo | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) | [Brunno Fernandes](https://github.com/brunnoff) |
| `2.0` | 29/09/2025 | Detalhamento do método com base na ISO 25010, incluindo métricas e cálculos |[Bianca Patrocínio](https://github.com/BiancaPatrocinio7) | [Brunno Fernandes](https://github.com/brunnoff) |
| `2.1` | 29/09/2025 | Inclusão do aplicativo móvel (Android) no escopo da avaliação |[Bianca Patrocínio](https://github.com/BiancaPatrocinio7) | [Brunno Fernandes](https://github.com/brunnoff) |
| `2.2` | 30/09/2025 | Removendo métricas e ajustando justificativa|[Bianca Patrocínio](https://github.com/BiancaPatrocinio7) | [Brunno Fernandes](https://github.com/brunnoff) |

---
