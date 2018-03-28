<!--
1º Projeto de Linguagens de Programação I 2017/2018 (c) by Nuno Fachada

1º Projeto de Linguagens de Programação I 2017/2018 is licensed under a
Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.

You should have received a copy of the license along with this
work. If not, see <http://creativecommons.org/licenses/by-nc-sa/4.0/>.
-->

# 1º Projeto de Linguagens de Programação I 2017/2018

_Este documento está em construção e sujeito a alterações_

## Descrição do problema

Descrever problema

## Modo de funcionamento

Explicar como programa deve funcionar

## Visualização do jogo

Explicar visualização do jogo

## Objetivos, critério de avaliação e entrega

<a name="objetivos"></a>

### Objetivos

* Jogo deve funcionar como especificado.
* Código deve estar devidamente comentado e indentado.
* Documentação do projeto deve ser feita comentários de documentação XML, e a
  documentação (gerada com [Doxygen], [Sandcastle] ou ferramenta similar) deve
  estar incluída no ZIP do projeto.
* Programa deve estar organizado numa estrutura de classes bem pensada, onde
  [cada classe tem uma responsabilidade específica e bem definida][SRP].

### Critério de avaliação

O projeto, que tem um peso de 10 valores na nota final da disciplina, será
avaliado segundo os critérios indicados na [Tabela 1](#tabela1).

<a name="tabela1"></a>

**Tabela 1** - Critérios de avaliação.

| Critério                                               | Peso      |
|--------------------------------------------------------|-----------|
| Funcionamento segundo especificações                   | ?,? val.  |
| Qualidade do código e das soluções<sup>[6](#fn6)</sup> | ?,? val.  |
| Comentários e documentação XML                         | ?,? val.  |
| Relatório                                              | ?,? val.  |
| Uso adequado de Git                                    | ?,? val.  |
| Organização do projecto e estrutura de classes         | ?,? val.  |

### Entrega

O projeto deve ser entregue via Moodle até às 23h de 22 de abril de 2018.
Deve ser submetido um ficheiro `zip` com os seguintes conteúdos:

* Solução completa (Visual Studio 2017, Visual Studio Code ou Visual Studio
  Mac), contendo adicionalmente e obrigatoriamente:
  * Pasta escondida `.git` contendo o repositório Git local do projeto.
  * Documentação gerada com [Doxygen], [Sandcastle] ou ferramenta similar.
  * Ficheiro `README.md` contendo o relatório do projeto em formato [Markdown]
    organizado da seguinte forma:
    * Título do projeto.
    * Nome dos autores (primeiro e último) e respetivos números de aluno.
    * Descrição da solução:
      * Arquitetura da solução, com breve explicação de como o programa foi
        estruturado.
      * Um diagrama UML explicando a estrutura de classes.
      * Um fluxograma explicando o _game loop_.
      * Estruturas de dados: grelha de jogo, outras estruturas auxiliares
        relevantes.
      * Algoritmos: verificação de situação vencedora.
    * Conclusões e matéria aprendida.
    * Indicação de quem fez o quê no projeto
    * Deve estar em conformidade com os _commits_ no git
    * Referências:
      * Incluindo trocas de ideias com colegas, código aberto reutilizado e
        bibliotecas de terceiros utilizadas. Devem ser o mais detalhados
        possível.
    * **Nota:** o relatório deve ser simples e breve, com informação mínima e
      suficiente para que seja possível ter uma boa ideia do que foi feito.

**Atenção**: Todos os ficheiros do projeto devem ser gravados em codificação
UTF-8<sup>[5](#fn5)</sup>.

## Extensões opcionais

<a name="extensoesop"></a>

* Inteligência artificial
* [Unity]

## Honestidade académica

Nesta disciplina, espera-se que cada aluno siga os mais altos padrões de
honestidade académica. Isto significa que cada ideia que não seja do
aluno deve ser claramente indicada, com devida referência ao respectivo
autor. O não cumprimento desta regra constitui plágio.

O plágio inclui a utilização de ideias, código ou conjuntos de soluções
de outros alunos ou indivíduos, ou quaisquer outras fontes para além
dos textos de apoio à disciplina, sem dar o respectivo crédito a essas
fontes. Os alunos são encorajados a discutir os problemas com outros
alunos e devem mencionar essa discussão quando submetem os projetos.
Essa menção **não** influenciará a nota. Os alunos não deverão, no
entanto, copiar códigos, documentação e relatórios de outros alunos, ou dar os
seus próprios códigos, documentação e relatórios a outros em qualquer
circunstância. De facto, não devem sequer deixar códigos, documentação e
relatórios em computadores de uso partilhado.

Nesta disciplina, a desonestidade académica é considerada fraude, com
todas as consequências legais que daí advêm. Qualquer fraude terá como
consequência imediata a anulação dos projetos de todos os alunos envolvidos
(incluindo os que possibilitaram a ocorrência). Qualquer suspeita de
desonestidade académica será relatada aos órgãos superiores da escola
para possível instauração de um processo disciplinar. Este poderá
resultar em reprovação à disciplina, reprovação de ano ou mesmo
suspensão temporária ou definitiva da ULHT<sup>[12](#fn12)</sup>.

## Notas

<sup><a name="fn1">1</a></sup> Temporário

## Referências

* <a name="ref1">\[1\]</a> Whitaker, R. B. (2016). The C# Player's Guide
  (3rd Edition). Starbound Software.
* <a name="ref2">\[2\]</a> Brain Bender Games (2009). Simplexity Game Rules.
  Discovery Bay Games.
* <a name="ref3">\[3\]</a> Simplexity. (2009) Retrieved from
  https://boardgamegeek.com/boardgame/55810/simplexity

## Licenças

Este enunciado é disponibilizados através da licença [CC BY-NC-SA 4.0].

## Metadados

* Autor: [Nuno Fachada]
* Curso:  [Licenciatura em Videojogos][lamv]
* Instituição: [Universidade Lusófona de Humanidades e Tecnologias][ULHT]

[GPLv3]:https://www.gnu.org/licenses/gpl-3.0.en.html
[CC BY-NC-SA 4.0]:https://creativecommons.org/licenses/by-nc-sa/4.0/
[lamv]:https://www.ulusofona.pt/licenciatura/videojogos
[Nuno Fachada]:https://github.com/fakenmc
[ULHT]:https://www.ulusofona.pt/
[aed]:https://fenix.tecnico.ulisboa.pt/disciplinas/AED-2/2009-2010/2-semestre/honestidade-academica
[ist]:https://tecnico.ulisboa.pt/pt/
[Markdown]:https://guides.github.com/features/mastering-markdown/
[Doxygen]:https://www.stack.nl/~dimitri/doxygen/
[Sandcastle]:https://github.com/EWSoftware/SHFB
[SRP]:https://en.wikipedia.org/wiki/Single_responsibility_principle
[Unity]:https://unity3d.com
