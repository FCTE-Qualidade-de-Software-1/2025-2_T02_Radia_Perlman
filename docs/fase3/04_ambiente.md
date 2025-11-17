# 4. Ferramentas e Ambiente de Avaliação

Esta seção descreve o ambiente de hardware, software e as ferramentas utilizadas na execução dos Casos de Teste definidos neste plano. O objetivo é garantir que a coleta dos dados ocorra em condições controladas, reproduzíveis e alinhadas às métricas estabelecidas.

## 4.1. Ambiente de Hardware

Os testes serão executados em notebooks pessoais dos membros da equipe e em dispositivos móveis físicos, conforme descrito:

* **Desktop / Notebook:**  
  Notebooks com os sistemas operacionais **Windows 11**, **Ubuntu 22.04 LTS** (ou versão equivalente) e **macOS Sonoma**, utilizados como ambiente primário para a execução dos testes funcionais e de portabilidade.

* **Mobile (iOS – Físico):**  
  Dispositivo **Apple iPhone**, executando a versão mais recente disponível do **iOS**, utilizado para testes reais de portabilidade, responsividade e comportamento no navegador Safari.

* **Mobile (Android – Físico):**  
  Dispositivo **Android**, executando a versão mais recente, utilizado nos testes de portabilidade, instalabilidade e sincronização pelo aplicativo Oppia.

## 4.2. Ambiente de Software

* **Navegador 1 (Principal):**  
  **Google Chrome** – versão estável mais recente (Windows, Ubuntu e macOS).

* **Navegador 2 (Secundário):**  
  **Mozilla Firefox** – versão estável mais recente (Windows, Ubuntu e macOS).

* **Navegador Mobile (iOS):**  
  **Safari** – versão mais recente disponível no dispositivo iOS utilizado nos testes.

* **Aplicativo Móvel:**  
  **Oppia Android App** – versão mais recente disponibilizada na **Google Play Store**.

* **Software de Produtividade:**  
  **Google Workspace** (Docs, Sheets) – utilizado para documentação, organização dos artefatos e registro dos resultados dos testes.

## 4.3. Ferramentas de Coleta e Auditoria

Para garantir rastreabilidade e conformidade com o requisito de **"Dados Auditáveis"**, serão utilizadas as seguintes ferramentas:

* **Registro de Resultados:**  
  **Google Sheets** – planilha centralizada para registro do status ("Passou/Falhou") e observações de cada Caso de Teste.

* **Gravação de Tela:**  
  **OBS Studio** – utilizado para gravação das execuções dos testes em desktop/notebook, servindo como evidência de falhas ou fluxos bem-sucedidos.

* **Captura de Tela:**  
  Ferramentas nativas dos sistemas operacionais **Windows**, **macOS**, **Ubuntu**, **Android** e **iOS**, utilizadas para capturar evidências de problemas visuais, inconsistências ou falhas de layout.

---

## Histórico de Versões

| Versão | Data | Descrição | Autor | Revisor |
| :---: | :---: | :--- | :--- | :--- |
| `1.0` | 16/11/2025 | Criação da estrutura inicial da página | [Brunno Fernandes](https://github.com/brunnoff) | |
| `1.1` | 17/11/2025 | Revisão do ambiente, inclusão de iPhone físico e Ubuntu | [Brunno Fernandes](https://github.com/brunnoff) | |