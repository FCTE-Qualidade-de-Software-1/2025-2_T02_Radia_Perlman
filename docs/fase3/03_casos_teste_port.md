# 3. Casos de Teste (Portabilidade)

Esta seção detalha os Casos de Teste (CTs) projetados para coletar os dados das métricas de Portabilidade (P) definidas na Fase 2.

---

### CT-P-01: Verificação de Adaptabilidade (Hardware e Software)
* **Métricas Associadas:** M1.1 (Adaptabilidade Hardware), M1.2 (Adaptabilidade Software)
* **Objetivo:** Medir a capacidade da plataforma de se adaptar a diferentes ambientes de hardware (desktop vs. mobile) e software (navegadores).
* **Passos de Execução:**
    1.  Definir um conjunto de "componentes" (funcionalidades-chave) a serem testados (ex: `CT-AF-01`).
    2.  Definir os ambientes de teste (B) (ex: Chrome, Firefox, Simulação Mobile).
    3.  Executar o `CT-AF-01` em todos os ambientes.
    4.  Registrar o número de componentes (A) que funcionaram sem falhas (funcionais ou de layout) em cada ambiente.
    5.  Calcular a métrica X = A / B para cada ambiente.
* **Resultado Esperado:** O cálculo da métrica X é concluído para todos os ambientes testados.

---

### CT-P-02: Verificação de Instalabilidade
* **Métricas Associadas:** M2.1 (Esforço), M2.2 (Flexibilidade)
* **Objetivo:** Medir o esforço e a flexibilidade para "instalar" o Oppia (registrar-se na web e instalar o app mobile).
* **Passos de Execução (Web - Esforço M2.1):**
    1.  Cronometrar o tempo e contar os passos (B) para um novo usuário se registrar na plataforma web.
    2.  Contar quantos desses passos são automáticos (A).
* **Passos de Execução (Web - Flexibilidade M2.2):**
    1.  Contar o número total de operações (B) durante o registro.
    2.  Contar quantas operações permitem customização (A) (ex: adicionar foto, definir interesses).
* **Passos de Execução (Mobile App):**
    1.  Repetir os passos acima para o processo de instalação do App pela Google Play Store e primeiro login.
* **Resultado Esperado:** Os dados A e B são coletados para o cálculo das métricas M2.1 e M2.2.

---

### CT-P-03: Verificação de Coexistência
* **Métricas Associadas:** M3.1 (Disponibilidade), M3.2 (Apresentada)
* **Objetivo:** Verificar se o Oppia funciona corretamente ao compartilhar recursos com outros aplicativos.
* **Passos de Execução (Desktop):**
    1.  Definir o ambiente de produção (B) (ex: B=2, Spotify e YouTube).
    2.  Iniciar o `CT-AF-01` no Chrome.
    3.  Simultaneamente, executar um vídeo em alta definição no YouTube e tocar música no Spotify.
    4.  Contar o número de produtos (A) com os quais o Oppia coexistiu (M3.1).
    5.  Executar por um tempo (T) (ex: T=1 hora) e contar o número de erros/travamentos (A) (M3.2).
* **Passos de Execução (Mobile):**
    1.  Repetir os passos acima no ambiente mobile.
* **Resultado Esperado:** Os dados A, B e T são coletados.

---

### CT-P-04: Verificação de Substituibilidade
* **Métricas Associadas:** M4.1 (Consistência), M4.2 (Facilidade de Migração)
* **Objetivo:** Avaliar a consistência de funcionalidades e a migração de dados entre as plataformas Web e App.
* **Passos de Execução:**
    1.  [Web] Fazer 50% de progresso em uma lição.
    2.  [App Mobile] Fazer login com a mesma conta.
    3.  Verificar se o progresso foi sincronizado (Passou/Falhou). Este resultado alimenta a M4.2.
    4.  [App Mobile] Identificar 10 funcionalidades-chave (B=10) da versão Web.
    5.  Verificar quantas (A) estão presentes e produzem resultados semelhantes no App (M4.1).
* **Resultado Esperado:** Os dados para A e B (M4.1) e o resultado da sincronização (M4.2) são coletados.

---

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor |
| :---: | :---: | :--- | :--- | :--- |
| `1.0` | [dd/mm/aaaa] | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff) | |