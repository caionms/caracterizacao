# Guia para Caracterização de Linguagens de Programação

+ Linguagem de Programação: Elixir

  * [Apresentação e histórico](#apresenta--o-e-hist-rico)
  * [Características da Linguagem](#caracter-sticas-da-linguagem)
  * [Capacidades da Linguagem](#capacidades-da-linguagem)
  * [Produtividade do Desenvolvedor](#produtividade-do-desenvolvedor)
  * [Ecossistema](#ecossistema)
  * [Informações Adicionais](#informa--es-adicionais)
  * [Referências](#refer-ncias)

## Apresentação e histórico

O [Elixir](http://elixir-lang.org/) foi criado em 2011 e criado por José Valim, através de um projeto de pesquisa e desenvolvimento da empresa de consultoria de software Plataformatec. Seu código é executado através de processos isolados, que trocam informações por meio de mensagens. A linguagem de programação Elixir, atualmente  na versão 1.6, teve sua primeira versão lançada em 2014. Trata-se de uma linguagem com código aberto que é executada na Máquina Virtual Erlang (Erlang VM), cujo principal objetivo é oferecer uma programação produtiva para aplicações distribuídas seguras e de fácil manutenção, potencializando os recursos da máquina virtual sobre a qual está fundada sem custos de performance. Ou seja, o foco principal da linguagem é fornecer, de forma produtiva, ferramentas para construir aplicações distribuídas e de fácil manutenção.

## Características da Linguagem
  ### Paradigma
   A linguagem é considerada multiparadigma, de programação funcional, concorrente, distribuída e orientada a processos. Onde: 
   + **Programação funcional:** É o processo de construir software através de composição de funções puras, evitando compartilhamento de estados, dados mutáveis e efeitos colaterais.
   + **Programação concorrente:** É um paradigma de programação usado na construção de programas que fazem uso da execução simultânea de diversas tarefas que podem ser implementadas como programas separados ou como um único programa que dispara várias linhas de execução em paralelo. As linhas de execução também são conhecidas como threads. A programação concorrente permite a execução em paralelo de vários programas no computador e está relacionada com a programação paralela. As tarefas sendo podem ser executadas concorrentemente em um único processador, vários processadores em um equipamento ou vários processadores espalhados em uma rede de servidores.
   + **A Programação Distribuída:** É quando a execução do sistema ocorre em vários ambientes que se tornam interligados por uma rede de internet ou intranet.
   + **A Programação Orientada a Objetos:** É um padrão de desenvolvimento de softwares largamente utilizado em muitas linguagens de programação atuais, como Java, C#, PHP, Python, C++, entre outras. Nesse processo de programação, são criadas coleções de objetos com estrutura e comportamentos próprios. Tais objetos interagem entre si e executam as ações solicitadas. O objetivo da POO é, portanto, aproximar o mundo real do mundo virtual e promover, também, a unificação de dados e processos e o agrupamento e reutilização de códigos.
  
  ### Propósito
  O foco principal da linguagem é fornecer, de forma produtiva, ferramentas para construir aplicações distribuídas e de fácil manutenção. 
  
  ### Sistema de Tipagem
  Seu principal objetivo é oferecer uma programação produtiva para aplicações distribuídas seguras e de fácil manutenção, potencializando os recursos da máquina virtual sobre a qual está fundada sem custos de performance. Ou seja, o foco principal da linguagem é fornecer, de forma produtiva, ferramentas para construir aplicações distribuídas e de fácil manutenção.
  
  ### Ambiente de Execução
  O Elixir é compilado para bytecode da máquina virtual da linguagem Erlang (BEAM). O bytecode compilado é compatível com o byteode Erlang, consequentemente o ambiente de execução do Elixir inclui todas as bibliotecas e programas disponíveis também para o Erlang.
  
  ### Implementação
  Inicialmente escrito em Erlang, hoje é implementado com praticamente todo seu código na linguagem Elixir, onde é feita a compilação do código para a BEAM.
  
  ### Modelo de tradução

<body>
	<p>
		É uma linguagem executada através da Erlang VM, uma máquina virtual conhecida por criar aplicações distribuídas com baixa latência e tolerante a falhas. Por ser executado através dessa Virtual Machine, permite que os desenvolvedores utilizem todas as bibliotecas do Erlang enquanto desenvolvem com o Elixir.
	</p>
	<p>
		O Erlang VM é executado como um processo de sistema operacional. Por padrão, ele executa um thread do SO por núcleo para atingir a utilização máxima da máquina. O número de threads e em quais núcleos eles são executados pode ser definido quando a VM é iniciada. Os processos Erlang são implementados inteiramente pela VM Erlang e não têm conexão com os processos do SO ou threads do SO. Portanto, mesmo se você estiver executando um sistema Erlang com mais de um milhão de processos, ele ainda será apenas um processo do sistema operacional e um thread por núcleo. Portanto, neste sentido, a VM Erlang é uma "máquina virtual de processo", enquanto o próprio sistema Erlang se comporta como um SO e os processos Erlang têm propriedades muito semelhantes aos processos do SO, por exemplo, isolamento.
	</p>
</body>
  
  ### Custos 
  Por ser uma linguagem menos conhecida do que outras mais dinfundidas como a Linguagem 1 (JAVA) e sabendo que é gratuita, além dos custos básicos como infraestrutura e tempo. É necessário citar que a mão de obra para projetos nessa linguagem vai ser mais especializada do que em outros casos, tornando um pouco mais custoso e resultando em menores equipes. Porém, é válido destacar que o custo final de um projeto vai depender de vários outros fatores.

## Capacidades da Linguagem

  ###  Metaprogramação
  O programador ao trabalhar com a linguagem consegue manipular a árvore sintática abstrata (AST) das expressões através de comandos. Torna-se possível definir macros para definir uma expressão que deve ser substituída em tempo de compilação. 
  
  ### Gerenciamento de Ciclo de Vida
  Esse é gerenciado pela Virtual Machine e utiliza os mecanismos de garbage collection existentes no Erlang. Dessa forma, quando uma variável é declarada no código, após o fim da execução, o garbage collector tem a função de remove-la.
  
  ### Segurança 
  Uma das características do Elixir é sua tolerância a falhas. Fornecendo mecanismos de segurança que permitem que a aplicação continue funcionando mesmo quando algo dá errado. Os processos alertam sobre uma falha nos processos dependentes, mesmo em outros servidores, para que possam corrigir o problema imediatamente. Além disso, o mecanismo de garbage collection assegura memory safety em Elixir.
  
  ### Performance
  O Elixir se mostra bastante eficiente em casos onde são utilizados algoritmos favoráveis à concorrência. Entretanto, no geral é mais lento que outras linguagens compiladas como a Linguagem 1 (JAVA).
  
  ### Escalabilidade
  Elixir roda em cima da Máquina Virtual do Erlang (BEAM), tornando possível rodar a aplicação em múltiplos nós. Ao combinar esses fatores com o sistema distribuído torna-se um efeito colateral uma boa performance da aplicação.
  
  ### Confiabilidade
  Mesmo sendo uma linguagem relativamente nova, a máquina virtual onde é rodada possui um pouco mais tempo de "vida". A cada dia que passa, a comunidade de Elixir cresce, resultando em mais desenvolvedores focados em identificar e corrigir os problemas apresentados. Além de ser usado por grandes empresas como [Bleacher Report](https://bleacherreport.com/) e [Adobe](https://www.adobe.com/br/), e em produtos renomados como [WhatsApp](https://www.whatsapp.com/) e [Discord](https://discord.com/). Temos ainda a palavra do criador, onde em 2017, em uma entrevista para o InfoQ, ele respondeu ao ser perguntado em que direção a linguagem irá evoluir?: *"Eu apresentei recentemente em meu keynote no ElixirConf US 2017 como a linguagem continuará evoluindo com a produtividade, manutenibilidade e confiabilidade em mente. Em particular, as próximas versões do Elixir incluirão um Code Formatter, para unificar os estilos de código utilizados pelas empresas e pela comunidade. Também estamos trabalhando na adição de princípios de property testing ao Elixir, o que ajudará os desenvolvedores a projetar e escrever um software completamente testável."*, podemos crer que confiabilidade faz parte do futuro da linguagem.

  ### Concorrência e Threading 
  Como dito mais acima, processos da máquina virtual Erlang não compartilham memória e só se comunicam através de mensagens, fazendo com que o Elixir seja extremamente performático para a programação concorrente.

## Produtividade do Desenvolvedor

  ### Frameworks e Contâiners
  Assim como a Linguagem 1 (JAVA), existe um framework focado em testes. Nesse caso, a linguagem disponibiliza um framework chamado ExUnit para a realização de testes unitários e, ainda, possui um terminal interativo, o IEx (Elixir’s Interactive Shell), que oferece funcionalidades como:
  
  + Autocompletar;
  + Histórico;
  + Avaliação de expressões.

E, como é visto em outras linguagens nesse formato imperativo de programar, é possível executar códigos com comandos e funções em tempo real. Isso é muito bom para quem está aprendendo a lidar com linguagem ou que possui uma grande demanda de projetos a serem executados.

Outros Frameworks mais conhecidos do Elixir são:

 + **Phoenix:** Permite criar aplicativos interativos na web rapidamente. Pode ser utilizado, portanto, para o desenvolvimento web, de APIs e aplicativos HTML5;
 + **Nerves:** Trata-se da plataforma e infraestrutura de código aberto que permite criar, implantar e gerenciar dispositivos IoT com total segurança, velocidade e em escala. Também serve para Embedded;
 + **Plug:** Destinado para aplicações na web;
 + **Sugar:** Muito utilizado para desenvolvimento web, garantindo rapidez, facilidade e eficácia ao projeto.
  
  ### Ferramentas Disponíveis
  O Elixir pode ser utilizado desde uma aplicação web até em um sistema embarcado. Tem um grande ecossistema e boas ferramentas para facilitar a vida dos desenvolvedores. 
  
  Ele conta, por exemplo, com o Mix, uma ferramenta de compilação que fornece tarefas para criar, compilar, testar aplicativos e gerenciar projetos e dependências. E através do Hex, seu package manager oficial, é possível encontrar uma quantidade gigante de libs, incluindo as do Erlang.
  
  ### Sintaxe, Semântica e Operações Predefinidas

#### Nomes

   ##### Casing
<body>
	<p>
		Os desenvolvedores do Elixir devem usar <code>snake_case</code> ao definir variáveis, nomes de funções, atributos de módulo e assim por diante.
	</p>
	<p>
		Aliases, comumente usados como nomes de módulos, são uma exceção, pois devem ser escritos em maiúsculas e escritos em <code>CamelCase</code>, como <code>OptionParser</code>. Para aliases, as letras maiúsculas são mantidas em siglas, como <code>ExUnit.CaptureIO</code> ou <code>Mix.SCM</code>. 
	</p>
	<p>
		Os átomos podem ser escritos em: <code>snake_case</code> ou <code>CamelCase</code>, embora a convenção seja usar a versão snake case em todo o Elixir. 
	</p>
	<p>
		De um modo geral, os nomes dos arquivos seguem a convenção <code>snake_case</code> do módulo que eles definem. Por exemplo, <code>MyApp</code> deve ser definido dentro do arquivo <code>my_app.ex</code>. No entanto, esta é apenas uma convenção. No final das contas, qualquer nome de arquivo pode ser usado, pois eles não afetam o código compilado de forma alguma. 
	</p>
</body>

   ##### Underscore <code>_foo</code>

<body>
	<p>
		Elixir utiliza de sublinhados em diferentes situações:
	</p>
	<p>
		<ol>
			<li>
				Um valor que não deve ser usado deve ser atribuído a _ ou a uma variável começando com sublinhado.
			</li>
			<li>
				Os nomes das funções também podem começar com um sublinhado. Essas funções nunca são importadas por padrão.
			</li>
			<li>
				Devido a essa propriedade, o Elixir depende de funções que começam com sublinhado para anexar metadados de tempo de compilação aos módulos. Essas funções geralmente estão no formato <code>__foo__</code>. Por exemplo, cada módulo no Elixir tem uma função <code>__info __/1</code>. 
			</li>
			<li>
				Elixir também inclui cinco formas especiais que seguem o formato de sublinhado duplo: <code>__CALLER__/0</code>, <code>__DIR__/0</code>, <code>__ENV__/0</code> e <code>__MODULE__/0</code> recuperam informações de tempo de compilação sobre o ambiente atual, enquanto __STACKTRACE __ / 0 recupera o stacktrace para a exceção atual.
			</li>
		</ol>
	</p>
</body> 

   ##### Trailing bang <code>foo!</code> 

<body>
	<p>
		Um trailing bang (ponto de exclamação) significa uma função ou macro em que os casos de falha levantam uma exceção. 
	</p>
	<p>
		Muitas funções vêm em pares, como <code>File.read/1</code> e <code>File.read!/1</code>. <code>File.read/1</code> retornará uma tupla de sucesso ou falha, enquanto <code>File.read!/1</code> retornará um valor simples ou então levantará uma exceção 
	</p>
	<p>
		A versão sem ! é preferível quando você deseja lidar com resultados diferentes usando correspondência de padrões.
	</p>
	<p>
		No entanto, se você espera que o resultado sempre seja bem-sucedido (por exemplo, se você espera que o arquivo sempre exista), a variação bang pode ser mais conveniente e irá gerar uma mensagem de erro mais útil (do que uma correspondência de padrão com falha) em caso de falha.
	</p>
	<p>
		Mais exemplos de funções emparelhadas: <code>Base.decode16/2</code> e <code>Base.decode16!/2</code>, <code>File.cwd/0</code> e <code>File.cwd!/0</code>.
	</p>
	<p>
		Existem também algumas funções não emparelhadas, sem variante não bang. O trailing bang ainda significa que gerará uma exceção em caso de falha. Exemplo: <code>Protocol.assert_protocol!/1</code>.
	</p>
</body>

   ##### Trailing question mark <code>foo?</code>

<body>
	<p>
		As funções que retornam um booleano são nomeadas com um ponto de interrogação à direita. 
	</p>
	<p>
		Exemplos: <code>Keyword.keyword?/1</code>, <code>Mix.debug?/0</code>, <code>String.contains?/2</code>.
	</p>
	<p>
		No entanto, as funções que retornam booleanos e são válidas em guardas seguem outra convenção, descrita a seguir. 
	</p>
</body>

   ##### <code>is_</code> prefix <code>is_foo</code>

<body>
	<p>
		As verificações de tipo e outras verificações booleanas permitidas nas cláusulas de guarda são nomeadas com um prefixo <code>is_</code>. 
	</p>
	<p>
		Exemplos: <code>Integer.is_even/1</code>, <code>Kernel.is_list/1</code>
	</p>
	<p>
		Essas funções e macros seguem a convenção Erlang de um prefixo <code>is_</code>, em vez de um ponto de interrogação final, precisamente para indicar que são permitidas em cláusulas de guarda.
	</p>
	<p>
		Observe que as verificações de tipo que não são válidas nas cláusulas de proteção não seguem esta convenção. Por exemplo: <code>Keyword.keyword?/1</code>. 
	</p>
</body> 

   ##### Nomes especiais

<body>
	<p>
		Alguns nomes têm um significado específico em Elixir. Segue esses casos abaixo:
	</p>
</body>

   ###### length and size

<body>
	<p>
		Quando você vê o tamanho em um nome de função, significa que a operação é executada em tempo constante, porque o tamanho é armazenado junto com a estrutura de dados.
	</p>
	<p>
		Exemplos: <code>Kernel.map_size/1</code>, <code>Kernel.tuple_size/1</code>
	</p>
	<p>
		Quando você vê o comprimento, a operação é executada em tempo linear ("tempo O (n)") porque toda a estrutura de dados deve ser percorrida.
	</p>
	<p>
		Exemplos: <code>Kernel.length/1</code>, <code>String.length/1</code>
	</p>
	<p>
		Em outras palavras, as funções que usam a palavra "size" em seu nome levarão o mesmo tempo, independentemente de a estrutura de dados ser pequena ou enorme. Por outro lado, as funções com "length" no nome levarão mais tempo à medida que a estrutura de dados aumenta de tamanho. 
	</p>
</body>
  
#### Operadores
Elixir fornece os seguintes operadores integrados que são definidos como funções que podem ser substituídas:

+ <code>+</code> e <code>-</code> - unário positivo / negativo
+ <code>+</code>, <code>-</code>, <code>*</code> e <code>/</code> - operações aritméticas básicas
+ <code>++</code> e <code>--</code> - lista de concatenação e subtração
+ <code>and</code> e <code>&&</code> - booleano estrito e relaxado "e"
+ <code>or</code> e <code>||</code> - booleano estrito e relaxado "ou"
+ <code>not</code> e <code>!</code> - booleano "não" estrito e relaxado
+ <code>in</code> e <code>not in</code> - adesão
+ <code>@</code> - atributo do módulo
+ <code>..</code> - criação de gama
+ <code><></code> - concatenação binária
+ <code>|></code> - pipeline
+ <code>=~</code> - correspondência baseada em texto
	
Alguns outros operadores são formulários especiais e não podem ser substituídos:

+ <code>^</code> - operador de pino
+ <code>.</code> - operador ponto
+ <code>=</code> - operador de correspondência
+ <code>&</code> - operador de captura
+ <code>::</code> - tipo operador
	
Temos também os Operadores de comparação, a linguagem fornece os seguintes operadores de comparação integrados (todos os quais podem ser usados ​​em guardas):
+ <code>==</code> - igual a
+ <code>===</code> - estritamente igual a
+ <code>!=</code> - desigual para
+ <code>!==</code> - estritamente desigual para
+ <code><</code> - Menor que
+ <code>></code> - Maior que
+ <code><=</code> - menos que ou igual a
+ <code>>=</code> - Melhor que ou igual a
	
A única diferença entre == e === é que === é estrita quando se trata de comparar inteiros e flutuantes. != e !== agem como a negação de == e ===, respectivamente.
	
### Guards
Os guardas são uma forma de aumentar a correspondência de padrões com verificações mais complexas. Eles são permitidos em um conjunto predefinido de construções onde a correspondência de padrões é permitida, como definições de função, cláusulas de caso e outros.

Nem todas as expressões são permitidas nas cláusulas de guarda, mas apenas algumas delas. Esta é uma escolha deliberada. Desta forma, Elixir (e Erlang) pode garantir que nada de ruim aconteça durante a execução de guardas e nenhuma mutação aconteça em qualquer lugar. Também permite que o compilador otimize o código relacionado aos guardas de forma eficiente.

### Estruturas de controle
	
 #### if and unless
	
 	iex> if String.valid?("Hello") do
 	...>	"Valid string!"
	...> else
  	...>	"Invalid string."
	...> end
	"Valid string!"

 	iex> if "a string value" do
 	...>	"Truthy"
	...> end
	"Truthy"
 Usar unless é como if só funciona no negativo:

	iex> unless is_integer("hello") do
 	...>	"Not an Int"
	...> end
	"Not an Int"
 #### case
 Se for necessário testar várias probabilidades de valores, podemos usar o case:
	
 	iex> case {:ok, "Hello World"} do
 	...> {:ok, result} -> result
 	...> {:error} -> "Uh oh!"
 	...> _ -> "Catch all"
 	...> end
	"Hello World"
 A variável _ é uma inclusão importante nas instruções case. Sem ela, a falha em encontrar uma correspondência gerará um erro. o _ funiona como o else que corresponderá a “todo o resto”. 
	
 Outra característica interessante do case é seu suporte para cláusulas de guard:
	
 	iex> case {1, 2, 3} do
 	...> {1, x, 3} when x > 0 ->
 	...>	"Will match"
 	...> _ ->
 	...>	"Won't match"
 	...> end
	"Will match"
	
	
 #### cond
 Quando precisamos combinar condições em vez de valores, podemos nos voltar para cond, que funciona como  else if ou elsif de outras linguagens:
	
 	iex> cond do
 	...> 2 + 2 == 5 ->
 	...>	"This will not be true"
 	...> 2 * 2 == 3 ->
 	...>	"Nor this"
 	...> 1 + 1 == 2 ->
 	...>	"But this will"
 	...> end
	"But this will"

 #### with
 A forma especial with é útil quando você pode usar uma instrução case aninhada ou situações que não podem ser conectadas de forma limpa. A expressão with é composta pelas palavras-chave, os geradores e, finalmente, uma expressão:
	
 	iex> user = %{first: "Sean", last: "Callan"}
 	%{first: "Sean", last: "Callan"}
 	...> with {:ok, first} <- Map.fetch(user, :first),
 	...>	{:ok, last} <- Map.fetch(user, :last),
 	...>	do: last <> ", " <> first
	"Callan, Sean"
 No caso de uma expressão não corresponder, o valor não correspondente será retornado:
	
 	iex> user = %{first: "doomspork"}
 	%{first: "doomspork"}
 	...> with {:ok, first} <- Map.fetch(user, :first),
 	...>	{:ok, last} <- Map.fetch(user, :last),
 	...>	do: last <> ", " <> first
	:error
 
#### Obs:
 Vale ressaltar que no Elixir não existem loops, as repetições são feitas por recursão.
	
 ####  Legibilidade e Redigibilidade
  A linguagem tem uma sintaxe com boa legibilidade, com possibilidades para boas melhoras. Assim como o Ruby, linguagem que foi uma inspiração, possui um design moderno, que permite escrever programas de modo natural ao problema. Tal fato pode ser notado em situações como não precisar utilizar o retorno explicito em funções ou utilizar Pparênteses obrigatoriamente. Existem ainda opções para tornar o código mais legível como o piper operator, que torna a legbilidade consideravelmente mais alta.

## Ecossistema
  + Maturidade
  
  ### Comunidade
  Apesar de ser uma linguagem relativamente nova, possui uma grande biblioteca de projetos open-source mantida pela própria comunidade e empresas que usam a linguagem no seu cotidiano. Destaca-se também por desenvolvedores com maior experiência sempre estão ajudando e compartilhando os seus conhecimentos, em redes sociais, meetups e video tutoriais.
  
  Como processo natural desse engajamento surgem as conferências, como por exemplo: ElixirConf US, ElixirConf EU, ElixirConfLA. Demonstrando que em todos os cantos o funcional chamou atenção dos desenvolvedores de todo mundo. Nesse movimento o Brasil conta com um evento próprio e será sobre ele que vamos falar um pouco mais aqui.
  
  + Governança
  + Fragmentação

---

## Informações Adicionais


## Referências 

1. https://www.hostgator.com.br/blog/elixir-linguagem-programacao-brasileira/
2. https://elixir-lang.org/
3. http://www.each.usp.br/petsi/jornal/?p=2459
4. https://hexdocs.pm/elixir/
5. https://www.alura.com.br/artigos/programacao-funcional-o-que-e
6. https://sites.google.com/site/profferdesiqueiraprogconc/aulas/1-introducao-a-programacao-concorrente
7. https://controlf5it.com.br/blog/programacao-distribuida-o-que-e-e-onde-e-usada/
8. https://www.ev.org.br/cursos/introducao-a-programacao-orientada-a-objetos-poo
9. https://pt.stackoverflow.com/questions/252572/duck-type-em-elixir
10. https://latam.sinch.com/blog/elixir-brasil-o-funcional-encontra-se-aqui/
11. https://elixirschool.com/en/lessons/basics/control_structures#with-3
	
