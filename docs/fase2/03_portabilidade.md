A Portabilidade é avaliada para verificar se o Oppia pode, de fato, chegar aonde mais se precisa dele, funcionando em diferentes ambientes.


## 3.1 Objetivo de Medição de Adequação Funcional

<p align="center"> Tabela 1: Formalização do Objetivo de Medição (GQM) para Portabilidade </a> </p>


|        Dimensão           |                   Descrição                     |
| ------------------------- | ----------------------------------------------- |
| Analisar a      | Plataforma Oppia (Interface Web e App Mobile).                       |
| Com o propósito de                 |     Avaliar a capacidade do Oppia de ser portado, instalado, adaptado e executado em diferentes ambientes |
| Com respeito a | Portabilidade                              | 
| Perspectiva de Avaliação  | Educadores (criadores de conteúdo) e Estudantes (usuários finais).                             |
| Contexto                  | Projeto acadêmico da disciplina de Qualidade de Software.       |

<font size="3"><p style="text-align: center">Fonte: Autoria própria (2025)</p></font>



## 3.2 Questões e Métricas

Abaixo estão propostas questões relacionadas às subcaracterísticas de Portabilidade, cada uma acompanhada de métricas operacionais e fórmulas.

### Q1 — Adaptabilidade

**Pergunta:** Em que grau o Oppia adapta-se automaticamente ou com baixo esforço a diferentes navegadores web, tamanhos de tela e condições de rede?

**Métrica 1.1 — Taxa de Sucesso de Renderização Responsiva**

- **Fórmula:** % renderização correta = (Nº de cenários com UI renderizada sem distorções / Nº total de cenários testados) × 100

- **Cenários:** combinações de navegadores (Chrome, Firefox, Edge, Safari), larguras de tela (desktop, tablet, mobile) e resolução.

- **Aceitação:** ≥ 95% para navegadores suportados.

**Métrica 1.2 — Taxa de Funcionamento em Condições de Rede Degradada**

- **Fórmula:** % funcionalidades críticas funcionando = (Nº de funcionalidades críticas disponíveis offline / Nº total de funcionalidades críticas definidas) × 100.

- **Cenários:** continuação de exploração salvo localmente, acesso a lições baixadas, sincronização posterior.

- **Aceitação:** ≥ 80% de limitações conhecidas do app.

---

### Q2 — Instalabilidade

**Pergunta:** Quão fácil é instalar e configurar o Oppia nas plataformas alvo?

**Métrica 2.1 — Taxa de Sucesso de Instalação via Documentação**

* **Fórmula:** % instalações bem-sucedidas = (Nº de instalações concluídas seguindo o guia / Nº total de tentativas) × 100.

* **Ambientes de teste:** Linux (Ubuntu), Windows, Android (versões suportadas).

* **Aceitação:** ≥ 90% em ambientes suportados documentados.

**Métrica 2.2 — Tempo Médio de Instalação**

* **Fórmula:** tempo médio (minutos) desde o início até o término da instalação/configuração funcional.
* **Aceitação:**  ≤ 4 minutos em servidor padrão.


---

### Q3 — Coexistência

**Pergunta:** O Oppia opera corretamente quando compartilhando recursos com outras aplicações no mesmo ambiente (mesmo servidor, mesmas bibliotecas, múltiplos apps no dispositivo)?

**Métrica 3.1 — Taxa de Operação em Ambiente Compartilhado**

* **Fórmula:** % de cenários de coexistência bem-sucedidos = (Nº de cenários onde Oppia funcionou sem impacto / Nº total de cenários testados) × 100.
* **Aceitação:** ≥ 90% nos cenários documentados.

**Métrica 3.2 — Incidência de Conflitos de Dependência**

* **Fórmula:** Nº total de conflitos (bibliotecas, versões de runtime) detectados por ciclo de teste.
- **Aceitação:** ≤ 1 conflito crítico por ciclo de teste.
---

### Q4 — Substituibilidade

**Pergunta:** Como é o esforço e o impacto ao substituir componentes do Oppia (ex.: provedor de banco de dados ou serviço de armazenamento)?

**Métrica 4.1 — Tempo Médio para Substituição de Componente**

* **Fórmula:** tempo médio (horas) desde a decisão de substituição até restabelecimento funcional.
* **Aceitação:** 4-5 horas.

**Métrica 4.2 — Percentual de Funcionalidades Afetadas Após Substituição**

* **Fórmula:** % funcionalidades impactadas = (Nº funcionalidades que sofreram regressão / Nº funcionalidades testadas após substituição) × 100.
* **Aceitação:** regressões ≤ 5% para substituições suportadas.

---

## Referências Bibliográficas

> SOUZA, Fernando Mauro de et al. **Uso do GQM para Avaliar Documentos de Utilização de Framework**. Anais do III Workshop de Qualidade de Software. v. 1, p. 75-82, 2008.
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. **ISO/IEC 25010:2011**. *Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models*. Genebra: ISO, 2011.

---

## Histórico de Versões

| Versão | Data       | Descrição                                           | Autor                                           | Revisor |
| :----: | ---------- | --------------------------------------------------- | ----------------------------------------------- | ------- |
|  `1.0` | 14/10/2025 | Criação da estrutura inicial da página              | [Brunno Fernandes](https://github.com/brunnoff) | [Bianca Patrocínio](https://github.com/BiancaPatrocinio7) |
|  `1.1` | 14/10/2025 | Adicionando tabela base      |  [Bianca Patrocínio](https://github.com/BiancaPatrocinio7)  |  [Othavio Bolzan](https://github.com/bolzanMGB)   |

|  `1.2` | 14/10/2025 | Adicionando métricas     |  [Othavio Bolzan](https://github.com/bolzanMGB)  |    |

