# 3. Descrição do Produto de Software

O Oppia é uma plataforma educacional interativa de código aberto, voltada para estudantes, professores e criadores de conteúdo. Seu objetivo principal é facilitar o aprendizado ativo e personalizado por meio de lições interativas chamadas “explorações”, que se adaptam às respostas e ao ritmo de cada usuário.

O sistema permite também que usuários criem conteúdo educacional, adicionando perguntas, explicações e multimídia, tornando-o uma ferramenta tanto de consumo quanto de produção de conhecimento. O Oppia funciona em navegadores web e em aplicativo Android, permitindo acesso online e offline.

A seguir, apresenta-se uma descrição detalhada do produto, organizada em tabela, abrangendo tipo, funcionalidades, usuários, ambiente de uso e outros aspectos relevantes para a avaliação de qualidade do software:


<p align="center"> Tabela 1 - Descrição Detalhada do Produto Oppia </a> </p>


| Item | Descrição |
|------|-----------|
| Nome | Oppia |
| Tipo | Plataforma educacional interativa (Web e Mobile), código aberto, disponível para múltiplos usuários e sem fins lucrativos|
| Repositório | [https://github.com/oppia/oppia](https://github.com/oppia/oppia) |
| Backend | Python (Django) |
| Banco de Dados | MariaDB / MySQL |
| Plataforma | Navegadores web (desktop e mobile), App Android |
| Público-alvo | Estudantes, professores/educadores e voluntários criadores de conteúdo educacional |
| Principais funções | 1. Navegar e acessar explorações<br>2. Responder perguntas interativas e receber feedback<br>3. Criar e editar explorações<br>4. Gerenciar conta, objetivos e progresso do usuário<br>5. Visualizar estatísticas de desempenho |
| Principais tarefas | Aprendizado interativo e personalizado; <br> Criação e publicação de conteúdo educativo; <br> Monitoramento do progresso do aluno |
| Janelas de interação | Login/cadastro; <br> Dashboard do usuário; Tela de exploração; <br> Editor de explorações; <br> Visualização de estatísticas |
| Ambiente de uso | Escolas, cursos online e ambientes de aprendizagem individuais; <br> Acesso via internet (web) ou app móvel (Android) |
| Nível de conhecimento em informática | Básico a intermediário (navegação e uso do app) |
| Nível de conhecimento no domínio | Não é necessário conhecimento técnico; |
| Componentes para avaliação | Interface de exploração; editor de autoria; gestão de usuários e progresso |
| Massa de dados disponível | Explorações dpúblicas e conteúdo educacional já existentes na plataforma |
| Requisitos de hardware/software | Navegador moderno ou Android 7.0+; <br> Conexão com internet (uso offline via app disponível)

<p align="center"><b>Fonte: </b>Autoria de <a href="https://github.com/bolzanMGB">Othavio Bolzan</a></p>


## 3.1 Classificação do Tipo de Produto

A classificação de produtos de software é importante para entender seu escopo, forma de distribuição e complexidade, além de auxiliar na definição dos critérios de avaliação de qualidade.
Existem diversas formas de classificar software, considerando domínio de aplicação, modelo de negócio, características construtivas e disponibilidade de dados.

Entre as classificações mais conhecidas estão:

- **Pressman (2002):** define categorias como software básico, comercial, científico/engenharia, embarcado, de computador pessoal e inteligência artificial.

- **IEEE 1062 (1998):** classifica produtos em COTS (Commercial Off-The-Shelf), MOTS (Modified Off-The-Shelf) e CUSTOMIZADO/FD (Fully Developed), considerando o nível de customização, manutenção, prazo de entrega e adequação ao uso do software.

- **Categorias práticas:** utilizadas em premiações ou avaliações, como educação, saúde, varejo, indústria, entre outras, destacando o domínio de aplicação do software.

A seguir, apresentamos a classificação do Oppia segundo essas abordagens:


<p align="center"> Tabela 2 - Classificação do Produto Oppia </a> </p>

| Critério | Classificação | Justificativa |
|----------|---------------|---------------|
| Segundo Pressman (2002) | **Software Comercial** | Produto padronizado e completo, disponível para um público amplo, com funcionalidades definidas; mesmo sendo de organização sem fins lucrativos, sua natureza funcional se enquadra nesta categoria. |
| Segundo IEEE 1062 (1998) | **COTS (Commercial Off-The-Shelf Software)** | Produto pronto, utilizado por diversos usuários, sem desenvolvimento específico para cliente; avaliação pode ser feita com critérios gerais de qualidade. |
| Categoria prática | **Educação e entretenimento** | Plataforma voltada à disseminação de conhecimento e criação de conteúdo educativo interativo; público-alvo: estudantes, professores e criadores de conteúdo. |

<p align="center"><b>Fonte: </b>Autoria de <a href="https://github.com/bolzanMGB">Othavio Bolzan</a></p>

## 3.2 Estrutura do Software
O Oppia apresenta:  
- **Módulos principais:** criação de lições interativas, ferramentas de edição, sistema de progressão de aprendizagem.  
- **Interfaces:** interface web responsiva (desktop e mobile).  
- **Dependências técnicas:** backend em **Python**, frontend em **AngularJS**, hospedagem no **Google App Engine**.  
- **Diagrama sugerido:** *(inserir aqui figura representando a arquitetura em alto nível: usuário → frontend → backend → banco de dados)*.

### 3.3 Referências
> RAMOS, Cristiane Soares. Processo de Avaliação de
Produto de Software. 2025. Disponível em: https://aprender3.unb.br/pluginfile.php/3230274/mod_resource/content/1/2025-2%20PROC%20AVAL%20PRODUTO.pdf.Acesso em: 29 set. 2025.

> Guerra, Ana Cervigni; Colombo, Regina Maria Thienne. Qualidade de produto de software. Disponível em: https://www.academia.edu/8349754/Qualidade_de_Produto_de_Software.Acesso em: 29 set. 2025.

### 3.4 Histórico de Versão

| Versão | Data       | Descrição                                    | Autor                                          | Revisor |
| :----: | ---------- | -------------------------------------------- | ---------------------------------------------- | ------- |
|  `1.0` | 28/09/2025 | Criação da estrutura do Documento            | [Brunno Fernandes](https://github.com/brunnoff) |         |
|  `1.1` | 29/09/2025 | Elaboração da Descrição  e Classificação do Tipo de Produto          | [Othavio Bolzan](https://github.com/bolzanMGB) | [Brunno Fernandes](https://github.com/brunnoff)        |

