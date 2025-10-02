# 5. Seleção e Priorização de Características

Nesta etapa definimos as características de qualidade com base nos objetivos da avaliação e no público-alvo do Oppia[^1]. Seguindo os critérios da norma SQuaRE (ISO/IEC 25010)[^2], a priorização utilizou uma **matriz Impacto x Risco** (escala 1–5): impacto mede o quanto cada característica sustenta o valor educacional do produto, por sua vez, risco combina a probabilidade de falha e gravidante para estudantes, educadores e a equipe envolvida. A matriz pode ser observada logo abaixo, na Tabela 1.

<div class="center">

  <p class="figure-title"><strong>Tabela 1:</strong> Matriz Impacto x Risco</p>

  <table>
    <thead>
      <tr>
        <th style="text-align: left;">Característica</th>
        <th style="text-align: center;">Impacto (1–5)</th>
        <th style="text-align: center;">Risco (1–5)</th>
        <th style="text-align: center;">Prioridade = I×R</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="text-align: left;"><strong>Adequação Funcional</strong></td>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;"><strong>20</strong></td>
      </tr>
      <tr>
        <td style="text-align: left;"><strong>Portabilidade</strong></td>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;"><strong>15</strong></td>
      </tr>
      <tr>
        <td style="text-align: left;">Confiabilidade</td>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">12</td>
      </tr>
      <tr>
        <td style="text-align: left;">Eficiência de Desempenho</td>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">9</td>
      </tr>
      <tr>
        <td style="text-align: left;">Segurança</td>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">6</td>
      </tr>
      <tr>
        <td style="text-align: left;">Manutenibilidade</td>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">4</td>
      </tr>
      <tr>
        <td style="text-align: left;">Compatibilidade</td>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">4</td>
      </tr>
    </tbody>
  </table>

  <p class="figure-source">Fonte: Autoria de <a href="https://github.com/mandicrz" target="_blank">Amanda Cruz</a></p>

</div>

Logo, foram priorizadas **duas características** principais:  

1. **Adequação Funcional**  
      * ***Justificativa:*** fundamental para verificar se o Oppia entrega as funcionalidades pedagógicas previstas, caso isso não ocorra, melhora em outras dimensões tem um efeito limitado.

2. **Portabilidade**  
      * ***Justificativa:*** essencial para garantir acesso em diferentes contextos (web e Android, diferentes redes e dispositivos), ponto importante para a inclusão digital e os ODS citados no projeto.

Considerando os ***trade-offs***, colocar a Adequação Funcional no topo amplia o trabalho de modelagem das explorações e exige testes ponta a ponta mais rigorosos, custo maior agora para evitar risco educacional depois. Dar prioridade alta à Portabilidade pede execução consistente, com variações de dispositivos e navegadores, isso pode adicionar camadas e pressionar o desempenho em aparelhos de entrada.

Mantemos, ainda assim, as duas prioridades iniciais, porque entregam valor direto: o produto faz o que promete e chega a quem precisa e caso surja pressão de prazo ou performance, a regra é reduzir escopo funcional ou adiar suportes secundários (por exemplo, versões antigas do Android ou navegadores pouco utilizados) antes de ceder em qualidade. Depois, foco em Confiabilidade para estabilizar e em Eficiência de Desempenho para otimizar, sem comprometer o que já foi assegurado.

## Histórico de Versões
| Versão |    Data    | Descrição                                | Autor                                           |                           Revisor                           |
| :----: | :--------: | :--------------------------------------- | :---------------------------------------------- | :---------------------------------------------------------: |
| `1.0`  | 28/09/2025 | Criação da estrutura inicial da página   | [Brunno Fernandes](https://github.com/brunnoff) |         [Amanda Cruz](https://github.com/mandicrz)          |
| `1.1`  | 29/09/2025 | Elaboração da priorização e documentação | [Amanda Cruz](https://github.com/mandicrz)      | [Pedro Lucas Dourado](https://github.com/pedrolucasdourado) && [Brunno Fernandes](https://github.com/brunnoff) |

## Referências

[^1]: OPPIA FOUNDATION. *Oppia GitHub repository*. Disponível em: <https://github.com/oppia/oppia>. Acesso em: 29 set. 2025.
[^2]: ISO/IEC 25000 SQuaRE series Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE). Disponível em: https://committee.iso.org/sites/jtc1sc7/home/projects/flagship-standards/iso-25000-square-series.html. Acesso em: 29 set. 2025.
