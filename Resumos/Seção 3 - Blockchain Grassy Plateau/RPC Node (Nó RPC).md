# **RPC *Node* (Nó RPC)**

- As funcionalidades de aplicações descentralizadas (DApps) exigem dados de diferentes redes *Blockchain* para completar as requisições dos usuários;

- As DApps não podem operar sozinhas e precisam se conectar a uma *Blockchain* para atender às solicitações, o RPC *Node* (Nó RPC, ou Chamadas de Procedimento Remoto) é uma função eficaz nos nós para conectar DApps a redes *Blockchain*;

- Os nós RPC também podem ajudar a permitir que aplicações Web3 interajam com a tecnologia *Blockchain*, além de facilitar o acesso aos dados dos usuários;

## **Definição de RPC**

- O *Remote Procedure Call* (Chamada de Procedimento Remoto, em português) é um protocolo de comunicação leve para facilitar a interação entre aplicativos de software;

- A principal função do RPC é permitir que programas se comuniquem com outros programas em redes remotas, as chamadas RPC não exigem detalhes sobre a rede do servidor;

- Qualquer pessoa pode usar um RPC em seu computador local para solicitar diferentes recursos de um sistema de servidor remoto;

- Ao finalizar a solicitação do cliente, o RPC solicita ao servidor que execute uma sub-rotina ou um procedimento, a relação entre nós e *Blockchain* no RPC é evidente, considerando que as DApps necessitam de dados da *Blockchain* para funcionarem corretamente;

- No modelo cliente-servidor de RPC, as DApps atuam como clientes, enquanto o nó RPC assume o papel de servidor.

## **Entendendo o Nó RPC**

- Nós RPC são computadores que utilizam software cliente de *Blockchain*, como um servidor que executa tanto a camada de execução quanto a infraestrutura da camada de consenso;

- É possível encontrar detalhes sobre o nó RPC nas diferentes categorias de nós no *Ethereum*, como nós arquivados, nós leves e nós completos;

- Entretanto, a *Blockchain* *Solana* permite a execução de nós validadores e nós RPC, os nós validadores podem operar o protocolo de consenso da *Solana* e receber recompensas por validar blocos;

- Já os nós RPC da *Solana* oferecem uma porta de entrada para que as DApps de *Solana* acessem dados relevantes da *Blockchain*, qualquer nó com a capacidade de responder a solicitações RPC pode ser chamado de nó RPC.

## ***Endpoint*** **RPC**

- Um *endpoint* RPC é o local na rede onde um programa pode enviar suas solicitações RPC para acessar dados do servidor;

- Uma vez que você conecta uma DApp a uma *endpoint* RPC, pode acessar diferentes operações, o que possibilita o uso em tempo real dos dados da *Blockchain*;

- O nó com o software adequado possui a capacidade necessária para atender às solicitações RPC, o *endpoint* RPC está vinculado ao nó e serve como a conexão utilizada pela DApp para recuperar informações da *Blockchain* para os casos de uso desejados;

- Em outras palavras, *endpoints* RPC operam em nós RPC, sendo nós com *endpoints* RPC, portanto, é possível usar os termos “RPC *endpoint*” e “RPC *node*” de forma intercambiável.

## **Tipos de RPC *Endpoints***

- A introdução ao RPC e a importância dos nós de *Blockchain* RPC também destacam as abordagens de infraestrutura importantes em variantes públicas e privadas;

- *Endpoints* RPC alternativos podem ajudar no suporte a *endpoints* públicos e privados de RPC, com a vantagem de backups tolerantes a falhas;

- Para entender o que é um nó RPC na *Blockchain* *Solana*, é preciso entender os diferentes tipos de *endpoints* RPC.

### ***Endpoints*** **RPC Públicos**

- Os *endpoints* RPC públicos desempenham um papel importante dentro dos diferentes tipos de utilização de *endpoints* RPC;

- Ademais, eles se referem a recursos compartilhados, com restrições de tempo, que estão disponíveis gratuitamente a qualquer momento;

- Esses *endpoints* funcionam em nós RPC acessíveis a qualquer pessoa para realizar as solicitações desejadas, a *Blockchain* oferece *endpoints* RPC públicos para facilitar o envio e o recebimento de dados da *Blockchain*;

- O uso de nós RPC em detalhes reflete como os *endpoints* RPC públicos são gratuitos e prontamente disponíveis, entretanto, você não pode usá-los para aplicações de nível de produção devido à sua taxa de limitação;

- Além disso, os *endpoints* públicos de RPC não oferecem suporte ao cliente e não possuem uma infraestrutura ativa de desenvolvedor;

- Os *endpoints* públicos de RPC também não conseguem atender aos requisitos de escalabilidade para operações de DApps.

### ***Endpoints*** **RPC Privados**

- Os *endpoints* RPC privados são aqueles que atendem especificamente às necessidades de sua DApp, utilizá-los ajuda a evitar problemas de congestionamento de solicitações por outros programas;

- Além disso, os *endpoints* privados de RPC oferecem um serviço de chamada de procedimento remoto ultrarrápido e altamente consistente;

- A definição de um *endpoint* privado de nó RPC enfatiza como eles podem operar sob demanda do usuário, esses *endpoints* são eficazes em casos de uso que envolvem um provedor de nós;

- Os *endpoints* privados de RPC também ajudam a manter *service-level agreements* (SLAs, acordos de nível de serviço em português), garantindo alto desempenho para a sua DApp.

### ***Endpoints*** **RPC Alternativos**

- A preocupação com o tempo de inatividade dos *endpoints* RPC pode afetar as funcionalidades das DApps, nesses casos, você pode contar cum um *endpoint* alternativo de chamada de procedimento remoto que funcione como um *endpoint* de backup;

- *Endpoints* alternativos ajudam a DApp a manter uma experiência de usuário mais estável, sem um *endpoint* RPC alternativo, a falha do *endpoint* principal resultaria na falha de todas as transações dos usuários;

- Desenvolver DApps com *endpoints* RPC alternativos é uma das melhores práticas para evitar um único ponto de falha.

## **Funcionamento dos Nós RPC**

- Esses nós operam conectando DApps aos dados da *Blockchain*, ao iniciar uma sub-rotina, o programa depende dos nós RPC para recuperar as solicitações necessárias pela rede *Blockchain*, enviando o *payload* de volta à aplicação descentralizada;

- A melhor maneira de entender o nó RPC na *Blockchain* é compreender o protocolo JSON-RPC, esse protocolo é a especificação padrão de RPC utilizada em redes *Blockchain*, oferecendo a vantagem de processar pedidos de dados com rapidez;

- No modelo servidor-cliente, a DApp atua como cliente, e o *endpoint* RPC funciona como servidor;

- O JSON-RPC oferece métodos específicos que podem ser utilizados para solicitar serviços ao *endpoint* RPC;

- Cada *Blockchain* oferece métodos JSON-RPC distintos, no caso do *Ethereum*, esses métodos são divididos em três categorias principais:  
  * Métodos de *Gossip*;  
  * Métodos de Histórico;  
  * Métodos de Estado.

- Os métodos de gossip acompanham o cabeçalho da *Blockchain* e ajudam a localizar blocos;

- Já os métodos de estado retornam informações sobre o estado atual dos dados da *Blockchain*;

- E os métodos de histórico recuperam registros históricos de qualquer bloco na cadeia;

- Quando as ações de um usuário necessitam de dados da *Blockchain*, a aplicação utiliza métodos JSON-RPC para fazer chamadas;

- As sub-rotinas através do nó RPC ou servidor retornam informações que podem ser usadas pela aplicação;

- Desenvolvedores podem acessar nós RPC de três maneiras:  
  * Por meio de um provedor de nós para um *endpoint* privado;  
  * Hospedando um nó próprio;  
  * Direcionando o tráfego para nós RPC públicos.

## **Utilização do Provedor de Nós RPC**

- Outro ponto importante sobre o significado do nó RPC são as formas de usar um provedor de nós;

- Provedores de nós gerenciam a configuração, manutenção e administração de nós para as DApps, garantindo que as DApps operem sem falhas;

- A utilização de provedores de nós é uma das melhores práticas para desenvolvedores Web3;

- Provedores de nós também permitem que desenvolvedores economizem tempo e energia ao ficarem em inovações para o usuário final;

- Existem provedores de nós para as principais redes *Blockchain*, como *Ethereum*, *Solana* e outras *Blockchains* de camada 2\.

## **Utilizando a Infraestrutura de Nó RPC no *Alchemy***

- As discussões sobre o uso de nós e *endpoints* RPC chamam atenção para usos práticos de nós RPC;

- Você pode responder à pergunta “O que é um nó RPC na *Blockchain* *Solana*?” utilizando um provedor de nós como o *Alchemy*, o qual oferece endpoints RPC para *Ethereum*, *Arbitrum* e *Solana*;

- É possível iniciar o uso de nós RPC no *Alchemy* com a garantia de alto desempenho em poucos passos:  
  * Crie uma conta no *Alchemy*;

  * Desenvolva sua primeira aplicação utilizando a opção “*Create App*” no painel;

  * Dê um nome para a sua aplicação e escolha a rede *Blockchain* e o tipo de rede;

  * Por fim, utilize a opção “*View Key*” no painel para copiar a URL do novo nó e começar a enviar requisições RPC.

## **Executando Nós RPC**

- Executar o seu próprio nó é uma opção que pode dar às equipes Web3 e desenvolvedores controle total sobre a configuração de nós;

- É possível executar um nó RPC para *Ethereum* em algumas etapas simples:  
  * A primeira etapa é selecionar a configuração do nó RPC, considerando implementação do cliente, configurações e ambiente de hardware e sistema;

  * Em seguida, você pode iniciar o nó por meio de um serviço de configuração ou instalação manual pela linha de comando (CLI);

  * Contudo, é necessário estar preparado para compensações, como o longo tempo de sincronização e a necessidade de manutenção constante dos nós RPC.

## **Considerações Finais**

- A visão geral sobre o nó RPC e sua importância para desenvolvedores Web3 sugere a necessidade de aprender mais sobre ele;

- À medida que as DApps crescem e se expandem com novas funcionalidades, os nós RPC ajudam a interagir com diferentes redes *Blockchain*;

- Provedores de nós surgiram como uma das opções plausíveis para atender à demanda por desenvolvimento de aplicações eficientes e rápidas;

- Além disso, os provedores de nós oferecem uma vantagem credível sobre operar o seu próprio nó, embora com algumas limitações de privilégios.