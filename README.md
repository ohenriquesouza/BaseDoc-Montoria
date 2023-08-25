# README: Estrutura 🔎

<div style="display: inline-block;">
<img align="center" height="20px" width="60px" src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white"/> 
<img align="center" height="20px" width="80px" src="https://img.shields.io/badge/Made%20for-VSCode-1f425f.svg"/> 
<a href="https://github.com/ohenriquesouza">
<img align="center" height="20px" width="90px" src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat"/>
</a> 
</div>
<br/>
<br/>

# OBJETIVOS
<div align="justify">

<p>Foi proposto pelo professor {<b>nome professor</b>} na disciplina de {<b>nome disciplina</b>}, um trabalho no qual o objetivo era {<b>breve resumo sobre o trabalho</b>}, além disso, {🔎<b>completo, caso seja cabível a ocasião</b>}</p>

<p>Sendo assim, após a conclusão do projeto, temos aqui um algorítmo capaz de: {🔎<b>Aqui, vamos listar em tópicos, de maneira resumida, as principais características do seu algorítmo</b>}</br>
<b>- [✔️] Característica I;</br></b>
<b>- [✔️] Característica II;</br></b>
<b>- [✔️] Característica III;</br></b>
<b>- [✔️] Característica IV; </br></b>
</p>

<p>Vale informar aos que não conhecem, {🔎<b>Caso seu programa utilize de alguma biblioteca específica para realizar alguma tarefa citada nas características, vale uma breve explicação, como msotra o exemplo ➝➝</b>}[<i>que tanto o <i>Map</i> quanto o <i>Unordered_Map</i> são estruturas próprias da vasta linguagem C++, portanto, no site <i>Cplusplus</i> (vide referência), é possível encontrar todas informações sobre estrutura, contexto, implementação e funções associadas de ambos os mapas.</i>]</p>
<p>Após a apresentação do tema, bem como a demonstração da lógica, serão apresentados todos os resultados obtidos a partir dos testes feitos.</p>

# INTRODUÇÃO

<p>{🔎<b>Na introdução, é necessário contextualizar o tema, antes de apresentar funções específicas do seu código. Lembre-se: um bom README deve ser capaz de ser bem entendido por uma pessoa que não tem o mesmo conhecimento sobre a área que você, portanto, os assuntos relacionados devem ser brevemente explicados.</b>}</p>

<p><b>O que é uma árvore em programação?</b> Árvore é uma estrutura de dados que organiza seus elementos de forma hierárquica, onde existe um elemento que fica no topo da árvore, chamado de raiz e existem os elementos subordinados a ele, que são chamados de nós filhos. Cada nós filho pode conter zero, um ou mais de um nós filhos. Os nós filhos que não contém outros nós filhos são chamados de nós folha.</p>

<b>Características de uma Árvore</b>
<ul>
<li>Raiz: Toda arvore possui o nó raiz que é o nó inicial da árvore;</li>
<li>Grau: o número de filhos que um nó possui;</li>
<li>Nível (ou profundidade): a distância de um nó até a raiz;</li>
<li>Altura: o maior nível encontrado na árvore (altura de uma árvore com n nós pode variar de lg(n) até n-1);</li>
<li>Folha: o nó que não possui filho.</li>
</ul>

<p>A partir dessas características, foram a nós apresentadas três diferentes estruturas em Árvore: <i>Árvore de Pesquisa Binária</i>, <i>Árvore AVL</i> e <i>Árvore Red/Black</i>. Cada uma delas com suas características e peculiaridades, o que possibilita realizar a comparação entre elas e concluir com êxito o objetivo do trabalho.</p>
</hr>

# LÓGICA UTILIZADA

<p>{🔎<b>Nesta sessão, serão apresentadas as principais funções do seu algorítmo, bem como uma breve explicação sobre seus funcionamentos. Para isso, utilize imagens de PEQUENOS trechos do código, apenas para ficar mais claro a funcionalidade do que você quer mostrar.</b>}</br>
{<b>⚠️Lembre-se: PEQUENOS trechos! Se o leitor estivesse interessado em linhas de código, iria direto na pasta busca-las, portanto, NÃO abuse de códigos na documentação.</b>}</p>

<h2>⚙️ Estruturas: </h2>

<p>Como já citado anteriormente, o objetivo principal do trabalho não era implementar as estrutras e sim realizar testes visando compara-las. Por conta disso, não extenderemos muito sobre as funções principais de cada árvore, uma vez que não foram feitas pelo autor.</p>

<p>Uma das poucas alterações que se mostraram necessárias durante a codificação, foi a necessidade de adotar a mesma estrutura mostrada no livro para a criação das árvores para que a remoção na red/black fosse concluida. No código disponibilizado para uso, durante a criação da árvore, era atribuido <i>NULL</i> ou <i>nullptr</i> (C++) para certificar de que seria criado apenas a raiz. Já no livro, usa-se a palavra <i>nill</i> que diz respeito aos filhos do nó receberem ponteiros nulos. No começo pareceu confuso, mas após ler o passo a passo mostrado no livro, torna-se fácil entender esse ponto. Por isso, a função padrão <code>CreateTree()</code>, para a red/black, foi substituida por uma <code>initializeTreeRB()</code> na qual iguala a nulo todos os possíveis elementos envoltos à raiz.</p>
</br>

<div align="center">
<p>Imagem 1, mostrando uma função</p>ㅤ<br/>ㅤㅤㅤㅤㅤㅤㅤㅤㅤㅤ
<i>Figura 1: Função <code>initializeTreeRB()</code> modificada.</i>
</div>

</br>

<p>Continuação...</p>

<h2>🕗 Tempo: </h2>

<p>{🔎<b>Neste trabalho que usei como exemplo, foi pedido para que os resultados de tempo obtido a cada teste fossem calculados e devolvidos ao usuário, para que posteriormente, fosse feita uma análise dos resultados.</b>}</p>
<p>{📌<b>Se for o caso, lembre-se de antes apresentar quais bibliotecas foram utilizadas para tal captação do tempo, bem como uma breve explicação sobre sua implementação e como a mesma foi feita.</b>}</p>

<p>Para coletar o tempo gasto para cada interação nas diferentes estruturas, utilizou-se a biblioteca <code>< chrono ></code>, bem como o <code>namespasce chrono</code>. Inicialmente, tentou-se utilziar a biblioteca <code>< time.h ></code>, porém, a mesma mostrou desempenho duvidoso enquanto rodando no Windows 10 em um WSL de Ubuntu. Por conta disso, seus resultados não compatíveis trouxeram a necessiade de uma nova bilbioteca que tivesse haver com tempo de execução. A Chrono, por sua vez, mostrou-se eficiente mesmo no Win10, exibindo resultados compatíveis e bastante precisos. Sua implementação não é tão simples quanto a da outro bilbioteca, porém não é nada muito complexo também!</p>

<div align="center">
<p>Imagem 4, mostrando uma função</p>ㅤㅤㅤㅤㅤㅤ
<center><i>Figura 4: Inicialização/declaração necessárias da bib. Chrono.</i></center>
</div>

<br/>
<p>Perceba que é atribuido como valor para cada variável a função <code>(t1 - t1)</code>, que nada mais serve para zera-las, evitando lixo de memória e tempos sobrepostos. Provavelmente exista algum método próprio para isso, ou um jeito mais inteligente de se fazer. Este está funcionando, e foi o pensado na hora, por tanto, está ótimo!.</p>

 # RESULTADOS E ANÁLISE

<p>{🔎<b>Sem dúvidas, a parte mais importante da documentação do trabalho. Aqui os resultados devem ser mostrados de forma clara.</b>}</p>


<p>Antes de qualquer análise, é importante lembrar que os testes apresentarão resultados diferentes para diferentes máquinas que rodarem o programa. Como diz a intuição, máquinas mais potentes, apresentarão resultados melhores. O computador no qual foi rodado todos os testes que verão abaixo possui as seguintes configurações: Processador {<b>modelo processador</b>}, {<b>qntd. memória RAM</b>} e GPU {<b>modelo GPU</b>}.</p>

<p>{⚠️<b>Como foi apresentado em sala de aula, reforçar que os resultados são baseados na configuração da SUA máquina é um passo muito importante. Por isso, os resultados obtidos não devem ser levados como verdade absoluta, uma vez que diferentes máquinas apresentarão diferentes valores!.</b>}</p>

<p>Após terminar todo o projeto, realizou-se diversos testes (mais especificadamente 3 testes para cada tamanho de arquivo), e tirou-se a média de tempo que cada estrutura gastou para realizar determinada ação. É importante lembrar que para a função <code>Search</code>, utilizou-se como padrão o arquivo "entrada.txt", o qual carregava consigo 10.000 valores flutuantes que seriam pesquisados em cada estrutura. Desses dez mil arquivos, alguns deles (60%) propositalmente foram inseridos sabendo que os mesmos <b>NÃO</b> existem em nenhuma das entradas, enquanto os outros 40%, são valores que existem nos arquivos, por tanto, estarão dentro das estruturas, se tudo tiver ocorrido be. Os resultados obtidos estão na grandeza dos segundos, e podem ser visualizados abaixo.</p>

<p>{🔎<b>Opte por utilizar tabelas, são melhores para mostrar resultados de forma organizada.</b>}</p>

| Entrada: 500           |  Insert                            |  Search      | Remove     | Total      |
| -----------------------| -----------------------------------|--------------|------------|------------|
|  <i>"APB"</i>           | 0,0004435  s                      |0,0067838 s   |0,0069817 s |0,014209 s |
|  <i>"AVL"</i>           | 0,0004673  s                      |0,0069382  s  |0,0068141 s |0,0142196 s |
|  <i>"ARB"</i>           | 0,0004237  s                      |0,0069413 s   |0,0065474 s |0,0139124 s |
|  <i>"MAP"</i>           | 0,0005779  s                      |0,0085797 s   |0,0088016 s |0,0179592 s |
|  <i>"U_MAP"</i>         | 0,0005482  s                      |0,0081461 s   |0,0085326 s |0,0172269 s |
|  <i>"VECTOR"</i>        | 0,0004403  s                      |0,0087349 s   |0,0086568 s |0,017832 s |
</hr>

| Entrada: 500000        |  Insert                            |  Search      | Remove     | Total      |
| -----------------------| -----------------------------------|--------------|------------|------------|
|  <i>"APB"</i>          | 0,864255  s                        |0,0071688 s   |0,0069133 s |0,8783371 s |
|  <i>"AVL"</i>          | 0,838687  s                        |0,0073495  s  |0,0069745 s |0,853011 s |
|  <i>"ARB"</i>          | 0,643372  s                        |0,0075557 s   |0,0068262 s |0,6577539 s |
|  <i>"MAP"</i>          | 0,88168  s                         |0,0106540 s   |0,0159773 s |0,9083113 s |
|  <i>"U_MAP"</i>        | 0,722394   s                       |0,0079768 s   |0,0109511 s |0,7413219 s |
|  <i>"VECTOR"</i>       | 0,5242  s                          |0,0113803 s   |0,0964162 s |0,6319965 s |
</hr>

	
| Legenda                |  Significado                                                                                      |                     
| -----------------------| ------------------------------------------------------------------------------------------------- |
|  "APB"                 |Árvore de Busca Binária                                                                            |
|  "AVL"                 | Árvore AVL (Adelson Velsky e Landis)                                                              |               
|  "ARB"                 | Árvore Red/Black                                                                                  |
|  "MAP"                 | Mapa (C++)                                                                                        |
|  "U_MAP"               | Mapa Desordenado (C++)                                                                            |
|  "VECTOR"              | Vector (C++)                                                                                      |

<p>{⚠️<b>Usou tabelas? Sempre faça legendas! Nenhum leitor tem a capacidade de adivinhar o que estava passando na sua cabeça durante a escrita da tabela. Mesmo que sejam abreviações comuns, formalize seus signifcados na legenda para evitar confusões.</b>}</p>

<h2>📈 Conclusões: </h2>

<p>{🔎<b>Utilize argumentos sólidos, lembre-se de que a máquina impacta nos resultados e aborde todos os recursos anteriormente apresentados.</b>}</p>

<p>Como citado no começo do texto, uma coisa que chama a atenção ao analisar os dados, é a excelente eficiência da ordenação <i>QuickSort</i>, que permitiu com que o vector, mesmo sendo "defasado" por precisar ser ordenado, conseguisse concluir a carga de testes com um tempo parcialmente satisfatório. Entretanto, vale dizer que esse tempo relativamente baixo não se dá pela estrutura em sí do Vector e sim pela eficiência do algorítmo Sort. Antes de implementar o QuickSort, utilizou-se apenas para fins comparativos, a ordenação BubbleSort. Com ela, a inserção/ordenação de 5.000 entradas levava em torno de 30 - 33 minutos, valor este que se reduziu a uma fração de segundos com o quick. Para a entrada de 500.000 então... o bubble sort apresentou comportamento deplorável, simplesmente não conseguindo concluir a inserção ordenada, nunca (O algoritmo ficou rodando por mais de 5 horas). Com isso, pode-se concluir sobre o vector que: Para valores de entrada grandes, é essencial o uso de um bom algorítmo de ordenação e ainda assim, apresentará resultados inferiores quando comparadas ás árvores. Caso não seja possível implementar um bom algorítmo de busca, exclua essa estrutura da sua lista de opções, será horrível.</p>

<p>{📌<b>Opte por utilizar tabelas, listas coloridas, ou qualquer outro meio que facilite a leitura e o entendimento. O Excesso de texto pode causar perda de interesse e confusão em você e em quem lê!.</b>}</p>

<p><b>Continuação...</b></p>

<p>Por fim, todas as estruturas foram capazes de finalizar e objetivar o trabalho. Apesar disso, não foram todas que apresentaram bom desempenho ao final. A escolha de determinada estrutura de dados não depende apenas do quanto ela se mostra eficiente. Cada tipo de problema pode exigir e se mostrar mais simples a partir de certa estrutura. Conclui-se então que, para os testes feitos, a Árvore Red/Black, apesar de possuir difícil implementação, teve melhor o melhor desempenho de todas as estruturas, obtendo tempos excelentes. Como consideração final, vale dizer que, mesmo perdendo nas comparações de tempo, o Unordered_Map (C++) se mostrou ser relativamente prático e bom. Precisando de praticamente uma única linha para gerar sua implementação, talvez (dependendo do problema), a diferença de tempo não seja um obstáculo que deva te impedir de usá-lo.</p>

# COMPILAÇÃO E EXECUÇÃO

<p>{🔎<b>Instruções de compilação SEMPRE devem estar presentes ao fim da documentação e a falta delas certamente causará penalidade na avaliação. Utilize este modelo como padrão, apenas adapte para seu projeto.</b>}</p>

A algorítmo disponibilizado possui um arquivo Makefile que realiza todo o procedimento de compilação e execução. Para tanto, temos as seguintes diretrizes de execução:


| Comando                |  Função                                                                                           |                     
| -----------------------| ------------------------------------------------------------------------------------------------- |
|  `make clean`          | Apaga a última compilação realizada contida na pasta build                                        |
|  `make r`                | Executa a compilação do programa utilizando o gcc, e o resultado vai para a pasta build, além de em seguida executar o programa da pasta build após a realização da compilação             |

# BIBLIOTECAS 

<p>{🔎<b>Todas bibliotecas utilizadas durante o desenvolvimento devem ser listadas aqui, mesmo aquelas que você não tem certeza sobre se estão ou não sendo utilizadas. É melhor sobrar do que faltar!</b>}</p>

Para o funcionamento desejado, é necessário incluir as seguintes bibliotecas no programa:<br/>

<ul>
	<li><code>#include 'biblioteca x'  </code></li>
	<li><code>#include 'biblioteca y'</code></li>
	<li><code>#include 'biblioteca z'</code></li>
	<li><code>#include 'biblioteca w'</code></li>
</ul>

<hr/>

# REFERÊNCIAS

<p>{🔎<b>Todos sites, artigos, livros e fontes que serviram de pesquisa (tanto para o desenvolvimento, quanto para formulação da documentação) devem estar listadas aqui. Dessa forma, caso o leitor tenha alguma dúvida específica de um tema, terá onde buscar!</b>}</p>

<ul>
	<li>Referrência x</li>
    <li>Referrência y</li>
    <li>Referrência z</li>
    <li>Referrência w</li>
</ul>

</div>

# AUTOR
Criado por {<b>nome autor</b>};

Aluno do {<b>número período</b>}° periodo do curso de `Engenharia da Computação` no [CEFET-MG](https://www.cefetmg.br)

