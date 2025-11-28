# 3. Casos de Teste - Portabilidade

Esta seção detalha os Casos de Teste (CTs) projetados para coletar os dados das métricas de Portabilidade (P) definidas na Fase 2.

---

## **CT-P-01: Verificação de Adaptabilidade (Hardware, Software e Resoluções)**

**Métricas Associadas:**

* M1.1 – Adaptabilidade ao Hardware
* M1.2 – Adaptabilidade ao Software
* M1.3 – Responsividade por Resolução

**Objetivo:**
Medir a capacidade da plataforma Oppia de operar corretamente em diferentes dispositivos, sistemas operacionais, navegadores e resoluções de tela.

**Passos de Execução:**

1. Definir uma lista de funcionalidades-chave (A) a serem avaliadas (ex.: criar conta, abrir lição, editar exploração, navegar entre páginas).
2. Definir os ambientes de teste (B), incluindo:

   * Dispositivos (desktop, notebook, tablet, smartphone)
   * Navegadores (Chrome, Firefox, Edge, Safari)
   * Sistemas Operacionais (Windows, Linux, Android, iOS)
   * Resoluções (480p, 720p, 1080p, 1440p, 4K)
3. Executar cada funcionalidade A em todos os ambientes definidos.
4. Registrar em cada teste se houve funcionamento:

   * Sem falhas funcionais
   * Sem falhas de layout/responsividade
5. Calcular a métrica X = A / B para cada combinação de ambiente.

**Resultado Esperado:**
A métrica X deve ser gerada para todos os ambientes testados, indicando o percentual de compatibilidade e adaptação.

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


