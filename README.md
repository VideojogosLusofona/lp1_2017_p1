<!--
1º Projeto de Linguagens de Programação I 2017/2018 (c) by Nuno Fachada

1º Projeto de Linguagens de Programação I 2017/2018 is licensed under a
Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.

You should have received a copy of the license along with this
work. If not, see <http://creativecommons.org/licenses/by-nc-sa/4.0/>.
-->

# 1º Projeto de Linguagens de Programação I 2017/2018

## Descrição do problema

Os alunos devem implementar o jogo [Simplexity] para dois jogadores em C#.

### O jogo Simplexity

O jogo [Simplexity] é semelhante ao [4-em-linha], mas com uma variação: além de
**cor**, as peças têm também **forma**. O [Simplexity] é jogado em turnos, e em
cada turno o jogador coloca uma peça numa das 7 colunas do tabuleiro de jogo. A
peça cai na vertical até atingir a base da coluna ou uma peça já colocada na
coluna. Um jogador vence quando 4 peças da sua **cor** ou da sua **forma** são
colocadas em linha (na vertical, horizontal ou diagonal). Se ocorrer uma
situação em que existam 4 peças em linha da mesma cor e 4 peças em linha da
mesma forma, a forma sobrepõem-se à cor para efeitos de vitória. O jogo termina
num empate após todas as peças terem sido colocadas em jogo sem que exista uma
situação de vitória.

A [Tabela 1](#tab1) mostra as condições de vitória para cada jogador, bem como
as peças alocadas inicialmente a cada um. Em caso de dúvida pode consultas as
[regras do Simplexity] ou contactar o docente.

<a name="tab1"></a>

**Tabela 1** - Condições de vitória (cor e forma) e peças alocadas inicialmente
a cada jogador.

| Jogador | Vitória de cor | Vitória de forma | Peças iniciais                             |
|---------|----------------|------------------|--------------------------------------------|
| 1       | Branco         | Cilindro         | 11 cubos brancos, 10 cilindros brancos     |
| 2       | Vermelho       | Cubo             | 11 cubos vermelhos, 10 cilindros vermelhos |

### Modo de funcionamento

O jogo começa automaticamente, entrando no seguinte ciclo (_game loop_):

1. Mostrar tabuleiro (ver secção <a href="#visualize">Visualização do jogo</a>)
2. Solicitar jogada ao jogador atual (jogador 1 é o primeiro a jogar)
3. Verificar se existe uma condição de vitória
   * Em caso afirmativo, terminar o jogo e indicar o vencedor
   * Em caso negativo:
      * Se ainda existirem peças para jogar, voltar ao ponto 1, alternando o
        jogador
      * Caso contrário, terminar jogo em empate.

No ponto 2, é solicitado ao jogador: a) a peça a jogar (cubo ou cilindro); e,
b) a coluna onde colocar a peça. Antes de solicitar a jogada, deve ser dada a
indicação de quantas peças de cada tipo o jogador ainda tem para jogar. Após o
jogador ter inserido uma jogada, o jogo deve verificar se: a) o jogador ainda
tem peças do tipo indicado; e, b) a coluna do tabuleiro ainda tem espaço para
mais peças (máximo 7 peças por coluna). Se alguma destas verificações falhar, o
jogador deve repetir a jogada.

No ponto 3, o tabuleiro deve ser analisado de modo a determinar se existe uma
das condições de vitória descritas na secção anterior.

<a name="visualize"></a>

### Visualização do jogo

A visualização do jogo deve feita em modo de texto. A [Figura 1](#fig1) mostra
uma possível implementação da visualização do jogo (lado direito), com os
caracteres `R` e `r` indicando peças vermelhas cúbicas e cilíndricas,
respetivamente, e os caracteres `W` e `w` representando peças brancas cúbicas
e cilíndricas, respetivamente.

<a name="fig1"></a>

![visualize](https://user-images.githubusercontent.com/3018963/38045647-463cb488-32b5-11e8-9c98-70c6cc42a16f.png)

**Figura 1** - Possível implementação da visualização em modo de texto (lado
esquerdo) e situação de jogo equivalente (lado direito).

### Organização do projeto e estrutura de classes

O projeto deve estar devidamente organizado, fazendo uso de classes e
enumerações. Cada classe/enumeração deve ser colocada num ficheiro com o mesmo
nome. Por exemplo, uma classe chamada classe `Player` deve ser colocada no
ficheiro `Player.cs`. A estrutura de classes deve ser bem pensada e organizada
de uma forma lógica, e [cada classe deve ter uma responsabilidade específica e
bem definida][SRP].

O exercício proposto no capítulo 20 do livro da disciplina [\[1\]](#ref1)
constitui um bom ponto de partida para desenhar uma estrutura de classes
adequada para este projeto.

<a name="objetivos"></a>

## Objetivos e critério de avaliação

Este projeto tem os seguintes objetivos:

* **O1** Jogo deve funcionar como especificado.
* **O2** Programa deve estar organizado numa estrutura de classes bem pensada.
  O código deve estar devidamente comentado e indentado<sup>[1](#fn1)</sup>.
* **O3** Projeto deve estar adequadamente comentado e documentado. Documentação
  do projeto deve ser feita comentários de documentação XML, e a documentação
  (gerada com [Doxygen], [Sandcastle] ou ferramenta similar) deve estar
  incluída no ZIP do projeto (mas não integrada no repositório Git).
* **O4** Repositório Git deve refletir um bom uso desta ferramenta, com
  _commits_ por parte de todos os elementos do grupo, com mensagens de _commit_
  que sigam as melhores práticas para o efeito (como indicado
  [aqui](https://chris.beams.io/posts/git-commit/),
  [aqui](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53),
  [aqui](https://github.com/erlang/otp/wiki/writing-good-commit-messages) e
  [aqui](https://stackoverflow.com/questions/2290016/git-commit-messages-50-72-formatting)).
* **O5** Documentação do projeto deve ser feita comentários de documentação
  XML, e a documentação (gerada com [Doxygen], [Sandcastle] ou ferramenta
  similar) deve estar incluída no ZIP do projeto.
* **O6** Relatório bem estruturado.

O projeto, que tem um peso de 4 valores na nota final da disciplina, será
avaliado de uma forma qualitativa. Isto significa que todos os objetivos têm de
ser totalmente (ou pelo menos parcialmente) cumpridos. A cada objetivo, O1 a
O6, será atribuída uma nota entre 0 e 1. A nota final do projeto será dada pela
seguinte fórmula:

_N = 4 x O1 x O2 x O3 x O4 x O5 x O6_

Isto significa que se os alunos ignorarem completamente um dos objetivos, a
nota final será zero.

## Entrega

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
UTF-8<sup>[2](#fn2)</sup>.

## Extensões opcionais

<a name="extensoesop"></a>

* Inteligência artificial

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
resultar em reprovação à disciplina, reprovaç.dropbox.attrão de ano ou mesmo
suspensão temporária ou definitiva da ULHT<sup>[3](#fn3)</sup>.

## Notas

<sup><a name="fn1">1</a></sup> Este item inclui vários aspetos: 1) projeto
devidamente organizado, com uma estrutura de classes lógica na qual [cada
classe tem uma responsabilidade específica e bem definida][SRP]; 2) código bem
indentado; 3) não é incluído código "morto", que não faz nada, como por exemplo
variáveis ou métodos nunca usados; 4) as soluções desenvolvidas são
[simples][KISS] e/ou eficientes; 5) código compila e executa sem erros e/ou
_warnings_; 6) código não acede a zonas inválidas da memória, como por exemplo
índices fora dos limites de um _array_.

<sup><a name="fn2">2</a></sup> Este pormenor é especialmente importante em
Windows pois regra geral a codificação UTF-8 não é usada por omissão. Em todo o
caso, e dependendo do editor usado, a codificação UTF-8 pode ser selecionada na
janela de "Save as"/"Guardar como", ou então nas preferências do editor.

<sup><a name="fn3">3</a></sup> Texto adaptado da disciplina de [Algoritmos e
Estruturas de Dados][aed] do [Instituto Superior Técnico][ist].

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
[regras do Simplexity]:https://john.cs.olemiss.edu/~dwilkins/CSCI531/fall12/Simplexity_rules.pdf
[Simplexity]:https://boardgamegeek.com/boardgame/55810/simplexity
[KISS]:https://en.wikipedia.org/wiki/KISS_principle
[4-em-linha]:https://en.wikipedia.org/wiki/Connect_Four
