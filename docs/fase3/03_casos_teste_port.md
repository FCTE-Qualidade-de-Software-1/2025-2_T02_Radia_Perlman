# 3. Casos de Teste - Portabilidade

Esta seção detalha os Casos de Teste (CTs) projetados para coletar os dados das métricas de Portabilidade (P) definidas na Fase 2.

---

# **CT-P-01: Verificação de Adaptabilidade (Hardware, Software e Resoluções)**

**Métricas Associadas:**

* **M1.1 – Adaptabilidade ao Hardware**
* **M1.2 – Adaptabilidade ao Software**
* **M1.3 – Responsividade por Resolução**


**Objetivo**

Avaliar a capacidade da plataforma **Oppia** de funcionar corretamente em diferentes **dispositivos**, **softwares** (navegadores e sistemas operacionais) e **resoluções** de tela.

O teste é dividido em **três subgrupos independentes**, permitindo isolar cada dimensão da adaptabilidade:

1. **Adaptabilidade ao Software (M1.2):** navegador/SO variando, dispositivo fixo.
2. **Adaptabilidade ao Hardware (M1.1):** dispositivo variando, navegador/SO fixos.
3. **Responsividade por Resolução (M1.3):** resolução variando, dispositivo e navegador fixos.


**Passos de Execução**

- **a. Seleção das funcionalidades-chave (A):** As mesmas funcionalidades serão executadas em todos os ambientes para manter consistência.
Exemplos:

    * Criar conta
    * Abrir lição
    * Editar exploração
    * Navegar entre páginas
    * Visualizar histórico
    * Visualizar aba de perfil


- **b. Definição dos Ambientes de Teste (B):** Os ambientes são organizados em três grupos independentes:

    - **1. Adaptabilidade ao Software (M1.2):** Dispositivo fixo, navegadores/SO variam.
Exemplos: Chrome, Firefox, Edge, Safari. 
    - **2. Adaptabilidade ao Hardware (M1.1):** Navegador e SO fixos, dispositivos variam Exemplos: Desktop Linux, Destktop Windows, Smarphone IOS, Smartphone Android, Table e Ipad.
    - **3. Responsividade por Resolução (M1.3):** Dispositivo e navegador fixos, resoluções variam via DevTools. Exemplo: 480p, 720p, 1080p, 1440p, 4K.


**Execução dos Testes**

Para cada combinação de ambiente (software, hardware ou resolução):

- a. Executar todas as funcionalidades-chave (A).

- b. Registrar separadamente:

   * **Funcionamento funcional:** a funcionalidade completou a tarefa sem erros?
   * **Funcionamento visual/layout:** quebras de layout? textos sobrepostos? botões escondidos?

- c. Marcar o resultado em tabela (Passou/Falhou ou 1/0).


**Cálculo das Métricas**

Para cada conjunto de testes: **X = A / B**, onde:

* **A** = número de ambientes onde todas as funcionalidades funcionaram adequadamente
* **B** = número total de ambientes testados naquele grupo

Isso gera:

* **M1.1 (Hardware):** compatibilidade por dispositivos
* **M1.2 (Software):** compatibilidade por navegadores/SO
* **M1.3 (Resolução):** responsividade por tamanhos de tela


**Resultado Esperado**

O resultado deste caso de teste é a geração das três métricas (M1.1, M1.2, M1.3) representando o percentual de compatibilidade e adaptabilidade do Oppia em cada dimensão testada.


---

## **CT-P-02: Verificação de Instalabilidade**

**Métricas Associadas:**

* M2.1 – Esforço de Instalação
* M2.2 – Flexibilidade de Instalação

**Objetivo:**
Avaliar o esforço e a flexibilidade necessários para instalar e configurar o ambiente do Oppia localmente, considerando variações de ambiente e dependências.

**Passos de Execução (Esforço – M2.1):**

1. Cronometrar o tempo total para concluir a instalação/execução local do Oppia.
2. Contar o número total de passos necessários (B).
3. Contar quantos passos são automáticos ou realizados por ferramentas (A).

**Passos de Execução (Flexibilidade – M2.2):**

1. Registrar quantas operações ou configurações permitem variações (A), por exemplo:

   * Versões alternativas do Node
   * Alterações no Bazel
   * Variações de dependências Python
2. Comparar com o total de operações envolvidas no processo (B).

**Resultado Esperado:**
Coleta dos valores A e B para cálculo das métricas M2.1 e M2.2.

---

## **CT-P-03: Verificação de Coexistência**

**Métricas Associadas:**

* M3.1 – Disponibilidade de Coexistência
* M3.2 – Restrição/Avaria sob Coexistência

**Objetivo:**
Avaliar se o Oppia mantém estabilidade e funcionamento quando executado simultaneamente com outros softwares relevantes.

**Passos de Execução (Desktop):**

1. Definir um conjunto de aplicações concorrentes (B), como:

   * Aplicativos de streaming de áudio
   * Aplicativos de streaming de vídeo (HD/4K)
   * Extensões de navegador comuns 
   * Ferramentas de comunicação (chat, videoconferência)
   * Editores/IDE ou ferramentas de produtividade

2. Iniciar o Oppia e executar funcionalidades do CT-AF-01.
3. Registrar quantas aplicações estão rodando simultaneamente sem impactar o Oppia (A) → **M3.1**.
4. Durante um período T (ex.: 1 hora), contar erros, travamentos ou perda de responsividade → **M3.2**.

**Passos de Execução (Mobile):**

1. Repetir o teste executando o Oppia via navegador móvel com outros apps em segundo plano.

**Resultado Esperado:**
Coleta dos valores A, B e T para análise de coexistência e restrições.

---

## **CT-P-04: Verificação de Substituibilidade**

**Métricas Associadas:**

* M4.1 – Consistência de Funcionalidades
* M4.2 – Facilidade de Migração

**Objetivo:**
Avaliar a capacidade do Oppia de manter dados, progresso e consistência de funcionamento quando o usuário alterna entre dispositivos, navegadores ou sistemas operacionais.

**Passos de Execução:**

1. Em um dispositivo inicial, criar uma conta e fazer progresso parcial em uma exploração (ex.: 50%).
2. Acessar a mesma conta em outro ambiente diferente (ex.: mudar de Windows para Android, ou de Chrome para Safari).
3. Verificar se o progresso foi mantido e sincronizado corretamente → **M4.2 (Passou/Falhou)**.
4. Identificar 10 funcionalidades-chave na primeira plataforma (B = 10).
5. Verificar quantas dessas funcionalidades (A) estão disponíveis e funcionam de forma equivalente na plataforma secundária → **M4.1**.

**Resultado Esperado:**
Coleta dos valores para as métricas M4.1 (A/B) e M4.2 (Passou/Falhou).

---

# Histórico de Versões

| Versão |    Data    | Descrição                                                                                 | Autor                                           | Revisor |
| :----: | :--------: | :---------------------------------------------------------------------------------------- | :---------------------------------------------- | :------ |
|  `1.0` | 16/11/2025 | Criação da estrutura inicial da página                                                    | [Brunno Fernandes](https://github.com/brunnoff) |[Othavio Bolzan](https://github.com/bolzanMGB)|
|  `2.0` | 17/11/2025 | Atualização dos CTs para alinhar com nova Tabela de Portabilidade e revisões das métricas | [Douglas Marinho](https://github.com/M4RINH0)   | [Othavio Bolzan](https://github.com/bolzanMGB)    |
|  `2.1` | 24/11/2025 | Concertando pequenos  na formatação  | [Douglas Marinho](https://github.com/M4RINH0)   | [Othavio Bolzan](https://github.com/bolzanMGB)    |


