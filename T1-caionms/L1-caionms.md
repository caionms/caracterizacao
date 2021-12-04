# Guia para Caracterização de Linguagens de Programação

+ Linguagem de Programação: Java

  * [Apresentação e histórico](#apresenta--o-e-hist-rico)
  * [Características da Linguagem](#caracter-sticas-da-linguagem)
  * [Capacidades da Linguagem](#capacidades-da-linguagem)
  * [Produtividade do Desenvolvedor](#produtividade-do-desenvolvedor)
  * [Ecossistema](#ecossistema)
  * [Informações Adicionais](#informa--es-adicionais)
  * [Referências](#refer-ncias)

## Apresentação e histórico

[Java](https://www.java.com/pt-BR/) é uma linguagem de programação orientada a objetos. A linguagem foi criada por James Gosling e sua equipe da Sun Microsystems na década de 1990, sendo posteriormente adquirida pela Oracle. O Java teve como berço o Green Project, liderado pela James, além de Patrick Naughton e Mike Sheridan. O projeto tinha como objetivo viabilizar sua visão de futuro, onde haveria uma convergência dos computadores com os equipamentos e eletrodomésticos frequentemente usados pelas pessoas no seu dia-a-dia. 
<br><br>
O protótipo dessa ideia foi o Star Seven, um controle remoto com uma interface gráfica touchscreen. Para esse novo equipamento foi desenvolvido uma linguagem de programação chamada de Oak. Com o "estouro" da internet, Gosling ficou encarregado de adaptar o Oak para a internet e o resultado desse trabalho foi a nova versão batizada de Java.
<br><br>
A linguagem foi projetada para uso no ambiente distribuído da Internet. Ela foi projetada com a intenção intenção de permitir que os desenvolvedores escrevam o programa apenas uma vez e o executem por meio de qualquer dispositivo.

### Árvore evolutiva do Java:
![image](./java.png)

## Características da Linguagem

  ### Paradigma
   A linguagem popularizou o paradigma orientado a objetos, permitindo uma programação multiplataforma de forma igual. Nesse paradigma todos os objetos têm determinados estados e comportamentos. Os estados são descritos pelas classes como atributos. Já a forma como eles se comportam (sua funcionalidade) é definida por meio de métodos, que são equivalentes à funções do paradigma funcional. O objeto recebe e envia mensagem, executa processamento e possue um estado local que ele pode modificar. Dessa forma, os problemas são resolvidos através de objetos que enviam mensagens uns para os outros.
  ### Sistema de Tipagem
   O Java é uma linguagem de tipagem estática, ou seja, existe um sistema de tipos bem definido e que é validado durante o tempo de compilação do código. Para isso, é necessário definir tipos explícitos para as variáveis que são criadas.
  ### Modelo de tradução

<body>
	<p> 
		Java é uma linguagem compilada e interpretada. O compilador Java, chamado javac, compila o código-fonte do Java para um código de nível intermediário chamado códigos de bytes. Esses códigos de bytes não são diretamente executáveis em qualquer plataforma de hardware existente; mas esses códigos são interpretados pelo interpretador Java, o qual pode operar por si mesmo ou como parte de um navegador Web. Podemos dizer então que sua compilação ocorre em duas etapas, onde a primeira vai envolver um compilador independente do SO e na segunda através da Java Virtual Machine, que é adaptada para cada tipo de SO que suporta seu código.
	</p>
	<p>
		Em intermédio entre a primeira e a segunda compilações, ao converter o código-fonte em bytecode, o compilador segue as seguintes etapas de forma cronológica:
 		<ul>
			<li><b>Etapa de Análise</b>: Lê os arquivos de origem <code>.java</code> e faz o mapeamento da sequência de tokens resultante em nós de uma AST <b>Árvore Sintática Abstrata (Abstract Sintax Tree).</b></li>
			<li><b>Enter</b>: Insere elementos para as suas definições na tabela de símbolos.</li>
			<li><b>Anotações de Processos</b>: Processa as anotações encontradas nas unitdades de compilação especificadas.</li>
			<li><b>Atribuição</b>: Atribui as árvores de sintaxe. Esta etapa inclui resolução de nome, verificação de tipo e dobra constante</li>
			<li><b>Fluxo/Flow</b>: Executa a análise de fluxo da etapa anterior, incluindo as verificações de atribuições e também os acessos.</li>
			<li><b>Desugar</b> Reescreve as AST e traduz o que se chama de <i>Sintatic Sugar</i>.</li>
			<li><b>Geração</b>: Gera os arquivos do tipo <code>.Class</code></li> 
 		</ul>
 	</p>
</body>

### Compilação e Execução

<body>
	<p>
		As cinco fases pelas quais a aplicação passa até ser realmente executada podem ser divididas em:
		<ul>
			<li>
				<b>Criação/edição de um programa Java</b>: Nesta primeira fase se dá a criação ou edição de arquivos em um programa editor, onde são inseridos os códigos pelo programador, os quais são posteriormente salvos em uma unidade física de armazenamento como um programa de extensão <code>.java</code>.
			</li>
			<li>
				<b>Compilação do programa Java em bytecodes</b>: Supondo que em um exemplo geramos um arquivo chamado <code>Ola.java</code>, na hora da compilação, o compilador produz um arquivo <code>.class</code> chamado <code>Ola.class</code> onde contém a versão compilada. O compilador Java converte o código-fonte em bytecodes que representam tarefas a serem executadas na fase de execução. Os bytecodes são executados pela Java Virtual Machine (JVM) - uma parte do JDK e a base da plataforma Java. Máquina Virtual (Virtual Machine - VM) é um aplicativo software que simula um computador, mas oculta o sistema operacional e o hardware subjacente dos programas que interagem com ela, o que garante a possibilidade de execução de programas Java em vários sistemas operacionais distintos.
			</li>
			<li>
				<b>Carregando um programa na memória</b>: A JVM armazena o programa na memória para executá-lo, efetuando o carregamento. O carregador de classe da JVM pega os arquivos <code>.class</code> que contêm os bytecodes do programa e os transfere para a memória primária.
			</li>
			<li>
				<b>Verificação de bytecode</b>: Enquanto as classes são carregadas, o verificador examina seus bytecodes para assegurar que são válidos e não violam restrições de segurança do Java.
			</li>
			<li>
				<b>Execução</b>: As JVMs executam bytecodes utilizando uma combinação de interpretação chamada compilação JIT (Just In Time) - conhecido como compilador Java HotSpot. O Java HotSpot traduz os bytecodes para a linguagem de máquina, quando a JVM encontra novamente essas partes compiladas, o código de linguagem de máquina é executado mais rápido. Uma explicação mais detalhada é que o programa Java passa por duas fases de compilação que são:
				<ul>
					<li>
						Quando o código-fonte é traduzido em bytecodes que acaba tendo uma portabilidade entre JVMs em diferentes plataformas do computador
					</li>
					<li>
						E a outra é durante a execução, os bytecodes são traduzidos em linguagem de máquina para o computador real em que o programa é executado.
					</li>
				</ul>
			</li>
		</ul>
	</p>
</body>

## Nomes, variáveis e vinculação

### Nomes

<body>
	<p>
		As convenções de nomenclatura tem como objetivo tornar os programas mais compreensíveis, tornando-os mais fáceis de ler. Eles podem também fornecer informações sobre a função do identificador, por exemplo, quer se trate de um pacote, constante, ou de classe que pode ser útil na compreensão do código.
	</p>
    <p>
		As convenções de nomes mais impactantes são:
		<li><b>Packages</b>: O prefixo do nome do pacote deve ser único, deve sempre ser escrito em letras minúsculas todo-ASCII e deve ser um dos nomes de domínio de nível superior, atualmente com, edu, gov, mil, net, org, códigos de duas letras identificando os países, tal como especificado na norma ISO 3166, 1981. Componentes subseqüentes do nome do pacote varia de acordo com uma organização próprias convenções de nomenclatura internos. Tais convenções podem especificar que certos componentes do nome do diretório haver divisão, departamento, projeto, máquina, ou nomes de login.</li>
		<div align=center><code> com.apple.quicktime.v2 </code></div>
		<li><b>Classes</b>: Os nomes de classe devem ser substantivos, em maiúsculas e minúsculas com a primeira letra de cada palavra interna em maiúscula. Tente manter seus nomes de classe simples e descritivo. Sempre evite palavras-ligadas , evite todas siglas e abreviaturas, seja semântico. </li>
		<div align=center><code> class MyClass{} </code></div>
		<li><b>Interfaces</b>: Nomes de interfaces devem ser usadas com as primeiras letras em maiúsculas como nome de classes.</li>
		<div align=center><code> interface MyInterface </code></div>
		<li><b>Methods</b>: Métodos devem ser verbos, com a letra minúscula em primeiro lugar, com a primeira letra de cada palavra interna em maiúscula.</li>
		<div align=center><code> public void myMethod() </code></div>
		<li><b>Variables</b>: Os nomes de variáveis não deve começar com underscore _ ou sinal de dólar $ personagens, mesmo que ambos não são permitidos. Os nomes de variáveis devem ser curtos, mas significativo. A escolha de um nome variável deve ser mnemônico, isto é, concebidos para indicar ao observador casual a intenção da sua utilização. Um personagem nomes de variáveis devem ser evitadas, exceto para temporários "descartáveis" variáveis. Os nomes comuns para variáveis temporárias são i, j, k, m, n e para inteiros, c, d, e e para caracteres.</li>
		<div align=center><code> char myVariable</code></div>
		<li><b>Constants</b>: Os nomes de variáveis declaradas constantes de classes e de constantes ANSI deve ser todo em letras maiúsculas com palavras separadas por sublinhados ("_").</li>
		<div align=center><code> static final int MIN_WIDTH = 4 </code></div>
	</p>
</body>

### Variáveis

<body>
	<p>
		Uma variável é uma estrutura que permite armazenar dados na memória durante a execução do programa, para processamento de informações. Todas as variáveis devem ser declaradas antes que possam ser usadas. Declarar uma variável significa criá-la em algum ponto do programa. A linguagem Java é fortemente tipada. Isso significa que cada variável obrigatoriamente deve ter um tipo declarado antes que possa ser utilizada. Podemos dividir as variáveis em 3 tipos:
	</p>
		<ol>
			<li><b>Variáveis Locais</b>: Podem ser utilizadas dentro do método onde foram declaradas, não sendo acessíveis de outros pontos do programa.</li>
			<li><b>Variáveis de Instância</b>: Uma classe pode conter variáveis que são declaradas fora dos métodos, chamadas de Variáveis de Instância. São usadas pelos objetos para armazenar seus estados. Seus valores são específicos de cada instância e não são compartilhados entre as instâncias.</li>
			<li><b>Variáveis de Classe</b>: Variáveis declaradas como estáticas são variáveis compartilhadas entre todos os objetos instanciados a partir de uma classe. Por isso, essas variáveis também são conhecidas como Variáveis de Classe.</li>
		</ol>
	</p>
</body>

### Vinculação (Binding)

<body>
	<p>
		Os dois tipos de vinculação que temos na linguagem são:
	</p>
	<p>
      <ul>
        <li><b>Vinculação Estática</b>: A variável é determinada pelo compilador antes do programa ser executado, ou seja, em tempo de compilação. Temos este tipo de vinculação quando há algum método <code>private</code>, <code>static</code> ou <code>final</code>.</li>
        <li><b>Vinculação Dinâmica</b>: A variável é determinada em tempo de execução. Ocorre em situações de código mais livre de encapsulamento, tornando o código mais versátil.</li>
      </ul>
    </p>
</body>

### Escopo, tempo de vida e ambientes de referência.

#### Escopo e tempo de vida

<body>
	<p>
		Escopo é a vida de uma variável em Java, tratando-se dos locais nos quais ela pode ser acessada. Em Java, o escopo de variáveis vai de acordo com o bloco onde ela foi declarada. A variável é criada no primeiro acesso a ela e destruída após o interpretador sair do bloco de execução ao qual ela pertence.
	</p>
	<p>
		Logo, se uma variável for criada dentro de um determinado método, quando este método chegar ao final, esta variável é  destruída. Se uma variável for declarada no começo da classe (fora dos métodos), estas variáveis podem ser acessadas por todos os métodos da classe. São os chamados atributos da classe.
	</p>
</body>

#### Ambientes de Referência

<body>
	<p>
		A linguagem Java é dita de escopo estático e apesar de ter recursos os quais podemos fazer vinculações dinâmicas, suas variáveis são referenciadas dentro de um ambiente estático.
	</p>
</body>

  ### Ambiente de Execução
   O Java™ Runtime Environment (JRE), também conhecido por ambiente de execução Java, é um conjunto de componentes para criar e executar aplicações Java. Ele está incluído no   kit de desenvolvimento Java (JDK).
Os componentes do JRE incluem a máquina virtual Java (JVM), bibliotecas de classe Java e o carregador de classes Java. Os JDKs são usados para desenvolver softwares Java, os JREs oferecem ferramentas de programação e tecnologias de implantação, e as JVMs executam programas nessa linguagem.

## Capacidades da Linguagem

  ### Metaprogramação
   Sabendo que a metaprogramação é a programação de programas que escrevem ou manipulam outros programas (ou a si próprios) assim como seus dados, ou que fazem parte do trabalho em tempo de compilação. Em alguns casos, permitindo que os programadores sejam mais produtivos ao evitar que parte do código seja escrita manualmente. Podemos visualizar que a linguagem Java, ao ter a possibilidade de um programa poder analisar a si próprio, se encaixa no caso de reflexão, onde ela é sua própria metalinguagem. 
   <br><br>
   O java consegue descobrir a classe de um objeto, modificadores de acesso, superclasse, campos, construtores, métodos, etc. A linguagem também pode criar instancia da classe, obter e modificar a variaveis de instância, etc. Porém existem casos onde o seu programa necessita processar o próprio programa ou outros programa, para isso temos como o exemplo mais conhecido, a API Java Reflection. Essa API pode ser usada em casos como: um navegador de classes, um depurador, um construtor de GUI ou uma IDE, tal como Netbeans ou Eclipse.

  ### Gerenciamento de Ciclo de Vida
   Podemos destacar dois ciclos de vida, o do produto que normalmente é divido em 7 estágios e do objeto em Java. Os 7 estágios do ciclo de vida de um produto são:
   	<body>
		<ol>
			<li><b>LEVANTAMENTO DE REQUISITOS</b></li>
			<li><b>ANÁLISE</b></li>
			<li><b>PROJETO</b></li>
			<li><b>IMPLEMENTAÇÃO</b></li>
			<li><b>TESTES</b></li>
			<li><b>IMPLANTAÇÃO</b></li>
			<li><b>MANUTENÇÃO</b></li>
		</ol>
	</body>
   Já o ciclo de vida de um objeto :
   
   + Antes de um objeto pode ser criado a partir de uma classe, a classe deve ser carregado. Para isso, o tempo de execução Java localiza a classe no disco (em um .classe Arquivo) e lê-lo na memória. Em seguida, Java procura por qualquer inicializadores estáticos que inicializar campos estáticos - campos que não pertencem a qualquer instância específica da classe, mas pertencem à própria classe e são compartilhados por todos os objetos criados a partir da classe. A classe é carregada pela primeira vez, você cria um objeto da classe ou a primeira vez que você acessar um campo estático ou método da classe. Quando você executa o a Principal método de uma classe, por exemplo, a classe é inicializado porque o a Principal método é estático. 
   + Um objeto é criado a partir de uma classe quando você usa o Novo palavra-chave. Para inicializar a classe, Java aloca memória para o objeto e define uma referência para o objeto para que o tempo de execução Java pode acompanhar isso. Então Java chama a classe construtor, que é como um método, mas é chamado apenas uma vez: quando o objeto é criado. O construtor é responsável por fazer qualquer processamento necessário para inicializar o objeto - variáveis inicializar, abrir arquivos ou bancos de dados, e assim por diante. 
   + O objeto vive sua vida, proporcionando acesso a seus métodos públicos e campos para quem quer e precisa deles. 
   + Quando é hora para o objeto de morrer, o objeto é removido da memória, e Java deixa cair a sua referência interna para isso. Você não tem que destruir objetos si mesmo. Uma parte especial do tempo de execução Java chamado “coletor de lixo” se encarrega de destruir todos os objetos quando eles não estão mais em uso.
  
  ### Segurança
   Desde que o código Java compilado foi desenvolvido para ser transportado em formato binário através da rede, segurança consiste em um tópico de extrema importância. Devido aos bytecodes do Java rodarem nas máquinas do usuário, existem considerações especiais a se fazer. Usuários que carregam arquivos de classe Java de servidores remotos, lugares possivelmente pouco seguros, precisam se certificar que o código Java carregado não pode derrubar o interpretador de bytecodes por realizar operações ilegais. Os níveis mais baixos do interpretador Java implementa segurança de várias formas:
   #### Segurança através de publicação
   O código fonte completo para ambos o interpretador e o compilador Java estão disponíveis para inspeção. Não é esperado que o usuário acredite na palavra dos desenvolvedores, de que a linguagem Java é segura. Auditorias de segurança do código do Java estão sendo efetuadas no momento.
   #### Segurança por ser bem definido
   A linguagem Java é rigorosa com relação as suas definições de linguagem:
   
   + Todas os tipos primitivos da linguagem são garantidas de serem de tamanho específico.
   + Todas as operações são definidas para serem realizadas em uma ordem específica.
   
   Dois compiladores Java corretos, ou seja, com a sua implementação de acordo com a especificação, nunca vão gerar resultados diferentes na execução do programa. Isto é bastante diferente de C e C++, nos quais os tamanhos dos tipos primitivos são dependentes da máquina e do compilador, e a ordem de execução é indefinida exceto em casos especiais.
   #### Segurança por falta de aritmética de ponteiros
   A linguagem Java não possui aritmética de ponteiros, portanto programadores não podem forjar um ponteiro para memória. Todas as referências à métodos e variáveis instanciadas são feitas por nomes simbólicos. O usuário não pode criar código que possua deslocamentos suspeitos, nos quais pode acontecer de se apontar justamente para uma região de dados confidenciais. Usuários não podem criar código que destruam variáveis do sistema ou que acessem dados privados.
   #### Segurança através de Garbage Collection
   Garbage Collection faz os programas em Java ficarem tanto mais seguros quanto mais robustos. Dois bugs comuns em programas em C e C++ são:
   
   + Falhar na liberação de memória visto que não é mais necessária.
   + Acidentalmente liberar o mesmo pedaço de memória duas ou mais vezes.
   
   Falhar na liberação da memória que não é mais acessada pode causar em um programa o uso crescente de memória. Acideltalmente liberando o mesmo espaço de memória ocasionalmente causa bugs de corrupção de memória que são difíceis de localizar. A linguagem Java elimina a necessidade de programadores se preocuparem com estas questões.
   #### Segurança através de checagem em tempo de compilação rigorosa
   O compilador Java realiza uma checagem extensiva e rigorosa durante tempo de compilação de forma a se ter o maior número de erros possível detectados pelo compilador. Os tipos na linguagem Java são rigorosos. Diferente de C e C++, os tipos do sistema não possuem nenhuma brecha:
   
   + Objetos não podem ser convertidos para uma subclasse sem uma explícita checagem em runtime.
   + Todas as referências à métodos e variáveis são checadas para se ter certeza de que os objetos são do tipo apropriado. Em adição, o compilador checa se as barreiras de segurança, isto é, referências a variáveis do tipo private ou métodos de outras classes, não são violadas.
   + Inteiros não podem ser convertidos para objetos, nem objetos serem convertidos para inteiros.

   O compilador também assegura rigorosamente que o programa não acessa o valor de uma variável local não inicializada.
   #### Verificação dos Arquivos de Classe
   Mesmo o compilador realizando uma checagem nos tipos, existe ainda a possibilidade de ataque via o uso de um compilador "hostil". Aplicações tais como o browser HotJava não carregam o código fonte para depois compilá-lo. Estas aplicações carregam arquivos de classe já compilados. O browser HotJava não tem como determinar se os bytecodes produzidos foram produzidos por compilador confiável, ou se vieram de um adversário tentando explorar o interpretador.

  Um problema adicional em tempo de compilação correponde a versão das classes em uso. Um usuário pode compilar com sucesso uma classe chamada MeuCofre para ser uma subclasse de Cofre. Mas a definição de Cofre pode ter mudado desde que a classe foi compilada. Métodos podem ter desaparecido ou mudado os argumentos, variáveis podem ter mudado seu tipo ou mudado de dinâmica(por objeto) para estática(por classe). A visibilidade de um método ou uma variável pode mudar de público para privado.

  Todas as classes vindas de uma máquina remota estão sujeitas ao verificador. Este verificador se certifica que os arquivos de classe estão no formato correto. Os bytecodes são verificados utilizando um simples comprovador de teorema, o qual estabelece um conjunto de restrições estruturais nos bytecodes.

  O verificador de bytecode também aumenta a performance do interpretador. A checagem em runtime que seria feita para cada instrução interpretada pode ser eliminada. Ao contrário, o interpretador pode assumir que esta checagem já foi realizada. Embora cada checagem individual seja inexpressiva, muitas instruções de máquina para a execução de cada instrução de bytecode são eliminadas.

  Por exemplo, o interpretador já sabe que o código segue as seguintes restrições:
  
  + Não há Overflow nem Underflow na pilha.
  + Todos os acessos e armazenamentos em registros são válidos.
  + Os parâmetros de todas as instruções de bytecode estão corretas.
  + Não existe nenhuma conversão ilegal de dados.

  O verificador é independente do compilador Java. Embora este vá certificar todo o código gerado pelo compilador corrente, o verificador deve poder também certificar código que o compilador corrente não pode gerar. Qualquer conjunto de bytecodes que satisfaça o critério estrutural vai ser certificado pelo verificador.

  O verificador é extremamente conservativo. Este vai recusar alguns arquivos de classe que um comprovador de teorema mais sofisticado certamente certificaria.

  Outras linguagens podem ser compiladas em formato de classe. O verificador de bytecode, por não ser desenvolvido especificamente para a linguagem Java, permite aos usuários importar código de fora do firewall confidencialmente.
  #### Gerenciador de Segurança
  Os tópicos vistos anteriormente com relação a segurança no Java dizem respeito as camadas mais baixas de proteção fornecidas. Além destes níveis de proteção, existe ainda um objeto contido no ambiente de runtime do Java, um gerenciador de segurança, que fica trabalhando o tempo todo enquanto o sistema está rodando. O gerenciador de segurança deve aprovar todas as operações que serão potencialmente tratadas, antes delas poderem ser completadas. Se, por alguma razão, o gerenciador de segurança desabilitar alguma certa operação, este lança uma exceção SecurityException. Do contrário, a operação é realizada normalmente.

  #### Performance
  No desenvolvimento de software, a linguagem de programação Java foi historicamente considerada mais lenta do que as linguagens tipadas de 3ª geração mais rápidas, como C e C ++. O principal motivo é o design de uma linguagem diferente, em que, após a compilação, os programas Java são executados em uma máquina virtual Java (JVM) ao invés de diretamente no processador do computador como código nativo, como fazem os programas C e C ++. O desempenho era motivo de preocupação porque muitos softwares de negócios foram escritos em Java depois que a linguagem rapidamente se tornou popular no final dos anos 1990 e no início dos anos 2000.

  Desde o final da década de 1990, a velocidade de execução de programas Java melhorou significativamente com a introdução da compilação just-in-time (JIT) (em 1997 para Java 1.1), a adição de recursos de linguagem que suportam um código melhor análise e otimizações na JVM (como HotSpot tornando-se o padrão para JVM da Sun em 2000). A execução de bytecode Java em hardware, como o oferecido pelo Jazelle da ARM, também foi explorada para oferecer melhorias de desempenho significativas.

  O desempenho de um programa Java compilado por bytecode Java depende de quão otimamente suas tarefas são gerenciadas pela máquina virtual Java host (JVM), e quão bem a JVM explora os recursos do hardware do computador e sistema operacional (SO) ao fazê-lo. Assim, qualquer teste de desempenho ou comparação de Java deve sempre relatar a versão, fornecedor, sistema operacional e arquitetura de hardware da JVM usada. De maneira semelhante, o desempenho do programa equivalente compilado nativamente dependerá da qualidade de seu código de máquina gerado, portanto, o teste ou comparação também deve relatar o nome, a versão e o fornecedor do compilador usado e suas diretivas de otimização do compilador ativadas .
  
  #### Escalabilidade
  A escalabilidade é a capacidade de um sistema de atender um volume crescente de carga de processamento sem comprometer seriamente a performance ou o tempo de resposta para os usuários. A escalabilidade de um software é uma característica desejável em todo o sistema, em uma rede ou em um processo, que indica sua habilidade de manipular uma porção crescente de trabalho de forma uniforme, ou estar preparado para crescer. Quando falamos da escalabilidade do software em si estamos falando sobre ter um código e uma arquitetura que é fácil de dar manutenção, de aumentar suas funcionalidades, de várias pessoas trabalharem nele. Enquanto que escalabilidade de código tem a ver com como é fácil o código crescer e ainda ser administrável. Em geral a escalabilidade de código tem a ver com escalabilidade de equipe, porque é raro um código ser muito grande e mantido por uma pessoa, mas é possível ser só sobre o código.
  
  O Java fornece suporte de armazenamento de componentes Java EE como EJBs. Existem diversas ferramentas de suporte para depuração, análise, etc. As construções de linguagem permitem e exploram o potencial de otimização e se adaptam bem ao hardware moderno. Por outro lado o tempo de execução, em java, não está livre de sobrecarga e custos de funcionalidade desnecessários ou indesejados,em particular, há muita sobrecarga de espaço.

  #### Confiabilidade
  Um ponto importante de uma linguagem de programação é a sua confiabilidade, pois uma linguagem confiável possibilita a criação de programas mais seguros, mais simples de serem desenvolvidos e com maior facilidade de aceitação por parte do usuário. A confiabilidade nas linguagens pode ser percebida por diversos fatores como, por exemplo: a legibilidade, o tratamento de exceções, a verificação de tipos e a facilidade de escrita.
  
  Através do uso de interfaces, onde uma classe pode herdar características de uma superclasse e ainda implementar métodos de uma ou mais interfaces. Toda a variável ou método pertence a uma classe ou objeto só pode ser invocada através dessa classe ou objeto. Isso reforça seu forte caráter orientado a objeto.

  O Java também garante a confiabilidade dos programas produzidos. O processo de compilação elimina uma gama enorme de possíveis problemas e uma checagem dinâmica (realizada em tempo de execução) contorna muitas situações que poderiam gerar erros.
  
  A confiabilidade dos programas escritos com o Java também é incrementada com um mecanismo eficiente para contornar situações inesperadas que podem ocorrer em tempo de execução. Essas condições excepcionais, chamas exceções, podem ser devidamente tratadas para evitar que o programa aborte, mesmo frente a situações de erro.
  
  Em Java não se tem acesso direto ao endereço de memória. Sendo assim, a linguagem Java se torna mais confiável.
  
  Outro ponto importante ainda sobre a confiabilidade é o tratamento de exceções, na qual as linguagens que dispõem de recursos para o programador tratar exceções, evitando que o programa seja finalizado inesperadamente e deixem o usuário “perdido”, são consideradas mais confiáveis e melhores também para o usuário. Com estas ferramentas o programador implementa um código que possa tratar estas exceções caso ocorram.
  
  Em Java, toda exceção é um objeto e existem classes prontas para o tratamento das mais variadas exceções. A superclasse de todas as exceções de Java é a classe java.lang.Throwable. Todos os objetos dessa classe ou de suas subclasses podem ser gerados ou capturados por meio do tratamento de exceções e assim facilitando o processo de tratar exceções e também tornando mais fácil sua visualização.
  
  #### Concorrência e Threading 
  Multithreading é um recurso Java que permite a execução simultânea de duas ou mais partes de um programa para utilização máxima da CPU. Cada parte desse programa é chamada de thread. Portanto, os threads são processos leves dentro de um processo. Threads podem ser usados para realizar tarefas complicadas em segundo plano, sem interromper o programa principal. Na linguagem, threads podem ser criados usando dois mecanismos:
  + Estendendo a classe Thread
  + Implementando a Interface Executável
  
  #### Custos 
   Como custo, sabemos que a linguagem é gratuita, sendo possível para qualquer pessoa ou equipe utilizar. Logo temos como custo, a mão de obra, a infraestrutura e principalmente o tempo. Existem profissionais especializados em calcular o custo de um serviço e esses são essenciais para qualquer equipe. Dessa forma, o custo final vai depender de vários fatores, como os citados acima. 

## Produtividade do Desenvolvedor

  ### Frameworks e Contâiners
   #### Frameworks
   Frameworks Java são grupos de códigos previamente escritos usados pelos desenvolvedores para criar aplicações por meio da linguagem de programação Java. 
   
   Frameworks Java são específicos a essa linguagem de programação. Eles são uma plataforma específica para desenvolver aplicações de software e programas Java.

   Frameworks Java são grupos de códigos previamente escritos e reutilizáveis, usados como templates pelos desenvolvedores na criação de aplicações. Esses frameworks elimina o trabalho manual excessivo ao programar uma aplicação uma vez que os desenvolvedores só precisam incluir código personalizado se for necessário.

   Os frameworks Java podem incluir funções e classes predefinidas (como categorias de objetos), que são usadas para processar, inserir e gerenciar dispositivos de hardware, além de interagir com o software do sistema. Isso depende do tipo de framework, da habilidade do desenvolvedor Java, do que ele está tentando realizar e das preferências pessoais dele.
   
   #### Contâiners
   Dificilmente uma aplicação gráfica é composta por um único componente, mas sim por vários componentes inter-relacionados. Para este tipo de aplicação, um componente fundamental é a área onde os demais componentes da aplicação estarão dispostos. Um componente que pode conter outros componentes é denominado um container.

   Em Java, a classe Container é a classe abstrata que define as funcionalidades básicas associadas a um container, tais como adicionar e remover componentes, o que é possível através dos métodos add() e remove(), respectivamente. É possível também estabelecer qual a estratégia de disposição de componentes no container, ou seja, qual o método de gerência de layout, através do método setLayout().
  
  ### Ferramentas Disponíveis
   Existem uma infinidade de ferramentas disponíveis para a linguagem, que podem auxiliar o desenvolvedor na entrega de um produto muito melhor, facilitando e melhorando diversas etapas do desenvolvimento de um software. Podemos citar ferramentas que auxiliam na compilação, configuração e deploy de aplicações, como o Eclipse, pois faz uso de um script ou XML, mas o usuário normalmente não tem conhecimento do que está ocorrendo por trás. Ou ferramentas que auxiliam nos testes de software, como o JUnit, que facilitam na manutenção e segurança do código.
  
  ### Sintaxe, Semântica e Operações Predefinidas
   
   #### Palavras reservadas
   Como qualquer linguagem de programação, a linguagem Java designa determinadas palavras que o compilador reconhece como especiais. Por essa razão, você não pode usá-las para nomear suas construções Java. A lista de palavras reservadas é surpreendentemente curta:
   
   	abstract, assert, boolean, break, byte, case, catch, char, class, const, continue, default, do, double, else, enum, extends, final, finally, float, para, goto, if, implements, import, instanceof, int, interface, long, native, new, package, private, protected, public, return, short, static, strictfp, super, switch, synchronized, this, throw, throws, transient, try, void, volatile, while
   Observe que true, false e null são tecnicamente palavras não reservadas. Embora sejam literais, elas estão na lista porque não é possível usá-las para nomear construções Java.
    
   #### Estrutura de uma classe
   Uma classe é um blueprint para uma entidade discreta (objeto) que contém atributos e comportamentos. A classe define a estrutura básica do objeto e, no tempo de execução, seu aplicativo cria uma instância do objeto. Um objeto tem um limite e um estado nítidos e pode fazer ações quando corretamente solicitado. Cada linguagem orientada a objetos possui regras sobre como definir uma classe. No Java, classes são definidas da seguinte forma:
   
   	public class NomeClasse extends SuperClasse implements Interface {
 		private String atributoClasseString;
		
		public NomeClasse(String variavel) {
    			this.atributoClasseString = variavel;
		}
		
		public int quantidadeDeLetrasDoAtributo() {
			int tamanho = this.atributoClasseString.length();
			return tamanho;
		}
		
		// Isso é um comentário
		/* Isso também */
		/* E
		   Isso
		   Também */
	}	
   Temos então uma classe que possui um modificador de visibilidade (public, private, default ou protected), seu nome, uma possível super classe e possíveis interfaces. No contéudo da classe, temos um atributo que possui também um modificador, seu tipo e seu nome, podendo ser instânciado um valor default (= "teste"). Temos também, um método que possui seu modificador, seu tipo de retorno e um nome, podendo ter parâmetros entre parênteses. Dentro do método, caso seu tipo de retorno não seja void, é preciso retornar um valor nulo ou do mesmo tipo do retorno.
   
   Para instanciarmos a classe e criarmos um objeto, podemos fazer da seguinte forma:
   
   	public class Main {
   		public static void main(String[] args) throws IOException {
        		NomeClasse classe = new NomeClasse("valor do atributo");
    		}
	}
   
   #### Estruturas de controle

<body>
	<p>
		Controle de fluxo é a habilidade de ajustar a maneira como um programa realiza suas tarefas. Por meio de instruções especiais, chamadas comandos, essas tarefas podem ser executadas seletivamente, repetidamente ou excepcionalmente. Não fosse o controle de fluxo, um programa poderia executar apenas uma única seqüência de tarefas, perdendo completamente uma das características mais interessantes da programação: a dinâmica.
	</p>
	<p>
		Podemos classificar os comandos aceitos pela linguagem Java em basicamente quatro categorias: 
	</p>
	<p>
		<ol>
			<li>
				Tomada de decisões: <code>if-else, switch-case</code>
			</li>
			<li>
				Laços ou repetições: <code>for, while, do-while</code>
			</li>
			<li>
				Apontamento e tratamento de excessões: <code>try-catch-finally, throw</code>
			</li>
			<li>
				Outros: <code>break, continue, label:, return</code>
			</li>
		</ol>
	</p>
</body>

##### Execução Condicional

<body>
	<p>
		A forma mais simples de controle de fluxo é o comando if-else. Ele é empregado para executar seletivamente ou condicionalmente um outro comando mediante um critério de seleção. Esse critério é dado por uma expressão, cujo valor resultante deve ser um dado do tipo booleano, isto é, true ou false. Se esse valor for true, então o outro comando é executado; se for false, a excecussão do programa segue adiante. 
	</p>
	<p>
		Uma variação do comando if-else permite escolher alternadamente entre dois outros comandos a executar. Nesse caso, se o valor da expressão condicional que define o critério de seleção for true, então o primeiro dos outros dois comandos é executado, do contrário, o segundo. 
	</p>
</body>

##### Execução Seletiva de Múltiplos Comandos

<body>
	<p>
		Frequentemente, desejamos que um único comando (ou único bloco de comandos) de uma lista seja executado mediante um dado critério. Isso pode ser feito através do aninhamento ou acoplamento de vários comandos if-else.
	</p>
	<p>
		A presença do último else, juntamente com seu comando, é opcional. Neste código, o [comando 1] será executado (e os demais saltados) caso a primeira condição seja true, o [comando 2] será executado (e os demais saltados) caso a primeira condição seja false e a segunda condição seja true, e assim sucessivamente. O [comando n] (se houver) somente será executado (e os demais saltados) caso todas as condições sejam false. 
	</p>
</body>

##### Execução Seletiva por Valores

<body>
	<p>
		Assim como no caso execução seletiva de múltiplos comandos, há situações em que se sabe de antemão que as condições assumem o valor true de forma mutuamente exclusiva, isto é, apenas uma entre as condições sendo testadas assume o valor true num mesmo momento. Nesses casos, a linguagem Java (como também as linguagem C, C++ e Pascal) provê um comando de controle de fluxo bastante poderoso. 
	</p>
	<p>
		A [expressão] pode ser qualquer expressão válida. Esta é avaliada e o seu valor resultante é comparado com as constantes distintas [constante 1], [constante 2], ..., [constante n]. Caso esse valor seja igual a uma dessas constantes, o respectivo comando é executado (e todos os demais são saltados). Se o valor for diferente de todas essas constantes, então o comando presente sob o rótulo default: é executado (e todos os demais são saltados), caso este esteja presente.
	</p>
</body>

##### Laço de iteração enquanto/faça

<body>
	<p>
		Frequentemente, desejamos que uma tarefa seja executada repetidamente por um programa enquanto uma dada condição seja verdadeira. Isso é possível pela utilização do comando while. Este comando avalia uma expressão condicional, que deve resultar no valor true ou false. Se o valor for true, então o comando subjacente é executado; se a expressão for false, então o comando é saltado e a execução prossegue adiante. A diferença é que após executar o comando subjacente, a expressão condicional é novamente avaliada e seu resultado novamente considerado. Desse modo a execução do comando subjacente se repetirá, até que o valor da expressão condicional seja false. Observe, porém, que a expressão é avaliada antes de uma possível execução do comando subjacente, o que significa que esse comando pode jamais ser executado. 
	</p>
	<p>
		Uma das observações importantes é sempre certificar que não ocorra o laço infinito (um laço que nunca para, pois a condição sempre é verdadeira). Caso tenha alguma chance de entrar no laço infinito, coloque um contador ou user o laço for. 
	</p>
</body>

##### Laço de iteração faça/enquanto

<body>
	<p>
		Um outro tipo de laço de repetição, similar ao enquanto/faça, é o laço faça/enquanto, este é introduzido por um par de comandos do/while.
	</p>
	<p>
		Diferente do laço enquanto/faça, este tipo de laço de repetição executa o comando e em seguida avalia a expressão condicional. A repetição ocorre se o valor dessa expressão for true. Se esse valor for false, a execução prossegue adiante do while.
	</p>
</body>

##### Laço de iteração com contagem

<body>
	<p>
		Em certas situações, precisamos de laços de repetições nos quais alguma variável é usada para contar o número de iterações. Para essa finalidade, temos o laço for. Este é o tipo de laço mais geral e mais complicado disponível na linguagem Java. 
	</p>
	<p>
		Isto que dizer que o laço for avalia inicialmente a expressão de inicialização. Em seguida, avalia a expressão condicional. Se o valor desta for true, então o comando é executado,  a segunda expressão é avaliada em seguida, e finalmente o laço volta a avaliar novamente a expressão condicional. Do contrário, se o valor da expressão for false, a execução prossegue adiante do laço for. Este arranjo é muito conveniente para manter variáveis de contagem.
	</p>
</body>

##### Break e continue

<body>
	<p>
		O comando break é usado para interromper a execução de um dos laços de iteração vistos acima ou de um comando switch. Este comando é comumente utilizado para produzir a parada de um laço mediante a ocorrencia de alguma condição específica, antes da chegada do final natural do laço.
	</p>
	<p>
		O comando continue tem a função de pular direto para final do laço, mas em vez de interromper o laço como no break, ele continua executando o próximo passo do laço. Não vamos ficar estudando o uso de continue por ser puco usual na programação estruturada. 
	</p>
</body>

### Legibilidade e Regibilidade
 O código-fonte é lido tanto pelo compilador, que não se preocupa com seu estilo de escrita, quanto pelas pessoas, que se importam enormemente com seu estilo de escrita. TODOS os programadores profissionais insistem que certas regras de legibilidade devem ser seguidas. Alguns dos mais importantes são:
  + ** Recuo: ** As instruções contidas em uma classe, um método, um loop, etc, devem ser indentadas à direita. Existem dois estilos comuns de indentação: Allman e K&R; use um deles.
  + ** Espaço em branco: ** Assim como usar parágrafo e espaçamento entre palavras corretos em línguas naturais torna-os muito mais fáceis de ler, o uso apropriado de linhas em branco e espaçamento interno em uma declaração pode torná-los muito mais legíveis. Alguns IDEs, como o NetBeans, irão recuar seu programa em qualquer um dos estilos.
  + ** Nomes com significados: ** Variáveis, métodos, classes, etc. devem ter nomes que signifiquem algo para o leitor. Use apenas nomes como "a", "b" e "c" quando não houver nenhum significado inerente em uma variável - é apenas um número abstrato. Veja Nomes para uma discussão mais detalhada.
  + ** Simplicidade: ** Sempre tente tornar o programa o mais simples possível. Resista à tentação de ser inteligente. Em algumas situações, a forma mais exlusiva ou mais rápida para se resolver um problema pode não ser a mais lara para a maioria dos programadores.
  + ** As convenções são importantes a seguir: ** Existem nomenclatura, formatação, documentação e convenções de uso padrão para Java. O uso dessas convenções torna o código-fonte do programa muito mais fácil para outras pessoas lerem.

## Ecossistema

  ### Maturidade
   Por ser uma linguagem antiga, podemos considerar que por todos os avanços e atualizações, ela tem uma boa maturidade. Com o passar do tempo, não só linguagem, mas os produtos no ramo da tecnologia em geral, tendem a evoluir e o Java não foge disso.
  
  ### Comunidade
   Pelo tempo que a linguagem tem de "vida" e por quão popular ela se tornou em todo mundo, é fácil notar que sua comunidade vai ser gigantesca. É muito fácil encontrar tópicos e debates sobre assuntos da linguagem, facilitando para novos adeptos da linguagem. Com qualquer busca rápida é possível encontrar diversos materiais de ótima qualidade sobre a linguagem Java.
  
  ### Governança
   Como dito mais acima no documento, o Java foi adquirido pela Oracle Corporation em meados de 2008 e continua sendo mantida por ela.

## Referências 

1. https://www.gartner.com/en/documents/2071615/programming-languages 
2. https://slideplayer.com/slide/6312477/
3. https://pt.wikipedia.org/wiki/Java_(linguagem_de_programa%C3%A7%C3%A3o)
4. https://www.zup.com.br/blog/java
5. https://rockcontent.com/br/blog/o-que-e-java/
6. https://tecnoblog.net/416833/o-que-e-java-guia-para-iniciantes/
7. https://www.programador.com.br/linguagens-de-programacao/linguagem-java.html
8. https://www.dm.ufscar.br/~waldeck/curso/java/part26.html
9. https://homepages.dcc.ufmg.br/~mlbc/cursos/internet/java/
10. https://www.devmedia.com.br/processo-de-interpretacao-e-compilacao-entendendo-o-java-de-uma-forma-diferente/24257
11. https://blog.betrybe.com/tecnologia/paradigmas-de-programacao/
12. https://www.treinaweb.com.br/blog/conhecendo-variaveis-e-constantes-no-java
13. https://www.devmedia.com.br/conheca-o-ambiente-de-execucao-java/32477
14. https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-a-Java-runtime-environment
15. https://faqcartx.info/programa%C3%A7%C3%A3o/41126-qual-%C3%A9-o-ciclo-de-vida-de-um-objeto-em-java.html
16. https://www.teclogica.com.br/seguranca-em-java/
17. https://www.gta.ufrj.br/grad/flavio/security.html
18. https://en.wikipedia.org/wiki/Java_performance
19. https://pt.stackoverflow.com/questions/90297/o-que-significa-escalabilidade-de-software
20. https://pt.stackoverflow.com/questions/364945/o-que-%C3%A9-um-c%C3%B3digo-escal%C3%A1vel
21. https://tableless.com.br/java-principais-caracteristicas/
22. http://ttechtecnologia.blogspot.com/2013/08/confiabilidade-e-tratamento-de-excecoes.html
23. https://www.geeksforgeeks.org/multithreading-in-java/
24. https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-a-Java-framework
25. https://www.dca.fee.unicamp.br/cursos/PooJava/graphic/containers.html
26. https://www.devmedia.com.br/principais-ferramentas-de-apoio-ao-desenvolvimento-java/34126
27. https://developer.ibm.com/br/tutorials/j-introtojava1/
28. https://perso.ensta-paris.fr/~diam/java/online/notes-java/principles_and_practices/style/readability.html
