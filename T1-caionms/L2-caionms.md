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
  Mesmo sendo uma linguagem relativamente nova, a máquina virtual onde é rodada possui um pouco mais tempo de "vida". A cada dia que passa, a comunidade de Elixir cresce, resultando em mais desenvolvedores focados em identificar e corrigir os problemas apresentados. Além de ser usado por grandes empresas como [Bleacher Report](https://bleacherreport.com/) e [Adobe](https://www.adobe.com/br/), e em produtos renomados como [WhatsApp](https://www.whatsapp.com/) e [Discord](https://discord.com/). Temos ainda a palavra do criador, onde em 2017, em uma entrevista para o InfoQ, ele respondeu ao ser perguntado em que direção a linguagem irá evoluir?: "Eu apresentei recentemente em meu keynote no ElixirConf US 2017 como a linguagem continuará evoluindo com a produtividade, manutenibilidade e confiabilidade em mente. Em particular, as próximas versões do Elixir incluirão um Code Formatter, para unificar os estilos de código utilizados pelas empresas e pela comunidade. Também estamos trabalhando na adição de princípios de property testing ao Elixir, o que ajudará os desenvolvedores a projetar e escrever um software completamente testável.", podemos crer que segurança faz parte do futuro da linguagem.
  
  Após 9 anos desde sua criação, executando numa máquina virtual com ainda mais tempo de existência, e criando uma comunidade significativa de contribuidores para o desenvolvimento e uso da linguagem identificando e corrigindo bugs com prontidão, pode-se dizer com segurança que Elixir é uma linguagem suficientemente confiável para ser usada para escrever aplicativos usados em produção em grandes organizações como Pinterest e Discord.
  + Concorrência e Threading 
  + Custos
  _Custos aqui ... _

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
  
  + Sintaxe, Semântica e Operações Predefinidas
    + Legibilidade
    + Redigibilidade
  + Custos 

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
