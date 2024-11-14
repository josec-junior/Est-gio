# **Algoritmos de Consenso, Tecnologia *Blockchain* e *Bitcoin* \- por *Andreas M. Antonopoulos***

- ***Bitcoin*** é um sistema composto por um protocolo de rede, funções criptográficas e um sistema de equilíbrio econômico baseado em teoria dos jogos;

- Esses componentes influenciam a operação do protocolo da rede, criando um sistema descentralizado;

- A inovação do *Bitcoin* está na combinação de várias tecnologias pré-existentes das décadas de 70, 80 e 90, criando algo novo através de sua **arquitetura** e **design**.

## **Componentes do *Bitcoin***

### **SHA-256**

- Trata-se de uma função de *hash* criptográfica que transforma dados de uma entrada (*input*) em uma saída (*output*) de tamanho fixo (256 bits);

- Essa função de hash possui as seguintes características:  
  * **Determinística**: uma mesma entrada gera sempre uma mesma saída;

  * **Aparência aleatória**: a saída aparenta ser aleatória, mas segue um padrão quando a mesma entrada é usada;

  * **Imprevisível**: é praticamente impossível prever a saída apenas a partir da entrada.

### ***Proof of Work*** **(Prova de Trabalho)**

- Satoshi Nakamoto aplicou o conceito de “*proof of work*”, originalmente usado no sistema anti-spam *HashCash*, para o consenso em uma rede descentralizada;

- O trabalho computacional necessário para encontrar um número (*nonce*) que gere um *hash* com um certo número de zeros no início é a base desse mecanismo;

- Quanto menor o número-alvo (*target*), mais difícil se torna encontrar o *hash*, e essa dificuldade é ajustada pela rede de *Bitcoin* para manter o tempo de processamento de blocos em cerca de 10 minutos.

## ***Hashing*** **com SHA-256**

- SHA-256 é utilizado para gerar uma “impressão digital” ou *hash* de um conjunto de dados, como um contrato ou software para garantir que nada foi alterado;

- A menor mudança nos dados de entrada resulta em um *hash* completamente diferente devido ao **efeito cascata**;

## ***Proof of Work*** **(Prova de Trabalho) no *Bitcoin***

- A dificuldade do *Bitcoin* é definida pela quantidade de zeros no início do *hash* gerado, cada zero adicional aumenta exponencialmente a dificuldade de encontrar um hash válido;

- Os mineradores precisam realizar tentativas de força bruta para encontrar um ***nonce*** que produza um *hash* com a quantidade necessária de zeros no início.

### **Mineração de Blocos**

- O processo envolve encontrar um *nonce* que quando, combinado com o cabeçalho do bloco, gere um *hash* que atenda à dificuldade-alvo;

- Mineração requer um grande poder computacional, pois são executados milhões de cálculos por segundo, para isso, é utilizado hardware especializado (***Application-Specific Integrated Circuit*****s \- ASICs**) e há uma grande quantidade de energia sendo consumida.

### **Energia e Termodinâmica**

- A execução da função SHA-256 consome bastante energia e dissipa o calor, o que vincula diretamente a mineração de *Bitcoin* ao consumo de eletricidade.

## **Recompensa do Minerador no *Bitcoin***

- No *Bitcoin*, a recompensa por minerar um bloco é de 25 *bitcoins*, quando um minerador cria/minera um bloco, a primeira transação incluída é uma que paga a si mesmo essa recompensa, chamada de transação ***coinbase***;

- Diferente das outras transações no *Bitcoin*, que têm entradas e saídas, a transação *coinbase* não possui entradas, o que significa que o minerador está essencialmente “criando” 25 *bitcoins* do nada.

### **Limite da Recompensa e a Validação**

- O minerador não se paga mais do que 25 *bitcoins*, porque os outros mineradores validariam o bloco e rejeitariam qualquer valor além do permitido pelas regras de consenso;

- Essas regras especificam a quantidade exata que pode ser gerada em cada bloco, e essa quantidade vai diminuindo ao longo do tempo;

- No começo, a recompensa era de 50 *bitcoins*, depois caiu para 25, em agosto de 2016 a recompensa caiu para 12,5 *bitcoins* e atualmente o valor da recompensa é de 6,25 *bitcoins*;

- As regras são baseadas no número de blocos minerados, a cada 210 mil blocos, a recompensa é reduzida pela metade;

- Então, se um minerador tentasse pagar a si próprio mais do que o permitido, seu bloco seria rejeitado pela rede.

## **Regras de Validação no *Bitcoin***

- Essas regras de validação são definidas no código do *Bitcoin*, especificamente na implementação de referência chamada ***Bitcoin Core***, escrita em C++;

- Esse código contém todas as funções que determinam se um bloco ou transação é válida, e é aí que as regras de consenso são realmente definidas;

- Se alguém quisesse criar uma implementação alternativa do *Bitcoin*, teria que replicar todos os bugs e falhas encontrados desde 2009, porque esses erros fazem parte do processo de validação;

- Ou seja, a implementação de referência define as regras, incluindo suas falhas, e qualquer tentativa de reescrever o software precisaria incluir esses detalhes;

## **Validação e Consenso no *Bitcoin***

- A tomada de decisões e a aplicação dessas regras de consenso na rede *Bitcoin* é descentralizada e feita através da “cadeia de maior dificuldade”;

- Ou seja, cada minerador valida um novo bloco e decide se o aceita ou não, baseado na cadeia de blocos que tem a maior quantidade acumulada de *Proof of Work* (prova de trabalho);

- Cada bloco contém a referência (*hash* do bloco anterior) ao bloco anterior, formando uma cadeia contínua, desde o primeiro bloco (bloco gênesis);

- Esse processo é essencial para garantir que o *Bitcoin* permaneça seguro e descentralizado, quando um novo nó se junta à rede ou fica offline por um tempo, ele pode verificar toda a cadeia de blocos desde o primeiro bloco, o bloco gênesis, até o bloco mais recente, para garantir que está em sincronia com a verdade consensual.

## **Resolução de *Forks* (Bifurcações) na *Blockchain***

- Se dois mineradores encontrarem blocos válidos quase simultaneamente, a rede pode se dividir temporariamente;

- O consenso final é alcançado quando outro minerador encontra o próximo bloco e o difunde, fazendo com que a rede siga a cadeia mais longa;

- **Um exemplo de cenário de *fork***: um minerador no Canadá encontra um bloco válido 200 milissegundos antes de um minerador na Austrália;

- Ambos os blocos se propagam pela rede, causando uma bifurcação, o critério para escolher qual bloco será aceito pela rede é a “cadeia mais longa”, ou seja, a que representa mais trabalho computacional acumulado (*Proof of Work*).

## **Construção e Validação da *Blockchain***

- Cada novo bloco contém uma referência ao bloco anterior, garantindo a integridade da cadeia;

- Os nós validam cada bloco novo e o conectam à *Blockchain*, verificando também se ele contém a prova de trabalho necessária;

- Quando um nó se desconecta e volta, ele pode recuperar todos os blocos que perdeu e reconstruir a *Blockchain* de forma independente;

- Isso permite que a rede mantenha uma versão única e verificável do histórico da *Blockchain*.

## **Propagação dos Blocos na Rede**

- Quando um minerador encontra um bloco válido, ele se apressa para disseminá-lo pela rede, para que seja aceito como parte da cadeia mais longa;

- A proximidade geográfica dos nós pode causar uma diferença na rapidez com que eles recebem blocos, o que pode gerar *forks* temporários;

- Os nós mais próximos do minerador que encontrou o bloco validam e propagam primeiro esse bloco.

## **Protocolos Alternativos de Consenso e Impactos no *Bitcoin***

- Existem outros protocolos de consenso além do utilizado no *Bitcoin*, entretanto, esses protocolos podem causar efeitos indesejados na rede;

- No *Bitcoin*, após 10 minutos, a rede converge, e esse modelo tem se mostrado eficaz.

### **Protocolo GHOST**

- **O protocolo GHOST (*Greedy Heaviest-Observed Subtree*)**, diferente do *Bitcoin*, ele permite que blocos de prova de trabalho (*Proof of Work*) que não foram incluídos na cadeia principal ainda sejam contados;

- Mesmo que o bloco não esteja na cadeia principal, os mineradores podem receber uma recompensa parcial.

### **Simplicidade do *Bitcoin***

- O *Bitcoin* utiliza um algoritmo simples comparado a outros mecanismos de consenso, mas que já se mostrou muito eficaz ao longo do tempo;

- Há muitos outros algoritmos de consenso sendo utilizados e desenvolvidos em diferentes *Blockchains*, além do utilizado pelo *Bitcoin*;

- Esses algoritmos têm como objetivo alcançar o consenso entre os participantes da rede, garantindo que as transações e os blocos sejam verificados e aceitos, entretanto, cada algoritmo tem suas particularidades e às vezes, podem causar problemas na rede.

## **A Longa Cadeia de Blocos e a Validade de Transações no *Bitcoin***

- Cada bloco minerado contém uma determinada recompensa em *bitcoins*;

- A transação e o bloco que a contém só são válidos se fizerem parte da **cadeia mais longa**;

- Se não está na cadeia mais longa, ela é então invalidada, como se nunca tivesse ocorrido.

### **Retenção de Recompensas e Confirmação**

- Quando um minerador recebe uma recompensa por minerar um bloco, ele não pode gastar essa recompensa imediatamente;

- A recompensa só pode ser gasta após a **confirmação de mais 100 blocos**;

- Durante um bloco, a história da rede é volátil, mas após 100 blocos, torna-se fixa e parte do histórico imutável da *Blockchain*.

## **Analogia entre *Blockchain* e Estratos Geológicos**

- No início, a *Blockchain* é como a superfície de gelo na Antártida: instável e sujeita a mudanças;

- À medida que novos blocos são adicionados e compactados, os blocos mais antigos se tornam mais difíceis de alterar, assim como camadas geológicas profundas;

- Com 144 confirmações (equivalente a 1 dia), a probabilidade de um bloco ser alterado torna-se muito pequena.

### **Possibilidade de Alteração**

- Apesar de improvável, tecnicamente é possível alterar um bloco anterior;

- Para isso, seria necessário criar uma cadeia nova mais longa, que tenha mais prova de trabalho acumulada do que a atual cadeia, a qual contém centenas de milhares de blocos.

## **Importância da Eficiência e Propagação na Mineração**

- O custo da eletricidade e a latência da rede são fundamentais;

- A eficiência do equipamento de mineração é limitada pelo **limite superior da Lei de Moore**;

- A mineração de *Bitcoin* está ultrapassando o desenvolvimento de computação de desktop, devido ao incentivo econômico massivo, estimado em cerca de 3 bilhões de dólares.

### **Impacto da Latência na Rede**

- A capacidade de propagar blocos rapidamente na rede é crucial e a latência afeta diretamente isso;

- Mineradores na China, que têm eletricidade barata, enfrentam desafios de latência devido a limitações de largura de banda, o que os coloca em desvantagem à medida que o tamanho dos blocos aumenta.

## **Ocorrência de *Forks* na Rede *Bitcoin***

- Um *fork* de dois blocos ocorre cerca de uma vez por semana, enquanto *forks* maiores, como de três ou mais blocos, são extremamente raros;  
- *Forks* maiores podem sinalizar problemas significativos na rede.

### ***Forks*** **Históricos Notáveis**

- **Abril de 2013**: um *fork* de 26 blocos ocorreu devido a uma mudança no banco de dados da rede do *Bitcoin*, criando uma bifurcação quase perfeita, de 50% da rede;

- A mudança de ***Berkeley DB*** para ***Level DB***, juntamente com um bug relacionado ao limite de descritores de arquivo, levou à incapacidade de metade da rede processar certos blocos;

- Este evento foi resolvido após um esforço de coordenação entre mineradores, restaurando a cadeia mais longa e invalidando a cadeia menor.

## **BIP 66 (*Bitcoin Improvement Proposal 66*) e *Forks* Recentes**

- O BIP 66 foi uma proposta introduzida para fortalecer a verificação de assinaturas de transações no *Bitcoin*;

- Após ser votado pela rede, a mudança foi implementada gradualmente, exigindo que todas as transações usassem um formato estrito de assinatura.

### ***Fork*** **de Julho de 2015**

- O evento foi causado pela adoção parcial do BIP 66 por alguns mineradores, que não validaram corretamente os blocos de acordo com as novas regras;

- O *fork* resultou em perdas de cerca de 50.000 dólares para os mineradores que não seguiram as novas regras de consenso.

## **Validação de Nós na *Blockchain***

- Cada nó da rede *Bitcoin* precisa validar completamente todas as transações desde o bloco gênesis (o primeiro bloco da cadeia) até o presente;

- Isso garante a integridade e a autenticidade de toda a cadeia de blocos;

- Teoricamente, seria possível modificar alguns blocos recentes, mas não a maior parte da cadeia;

- Para realizar tal modificação, seria necessário manter 51% da taxa de *hash* e realizar cerca de 366 mil blocos de *Proof of Work* em 10 minutos, o que é altamente improvável;

- Cada nó, ao iniciar, só conhece o bloco gênesis e precisa sincronizar com a rede, verificando independentemente toda a cadeia de blocos;

- Esse processo pode levar de 4 a 5 dias e requer cerca de 40GB de espaço (dependendo da indexação das transações).

## **Consenso Nakamoto e Algoritmos Alternativos**

- Baseado no conceito de “*longest chain*” (cadeia mais longa) com *Proof of Work*, usando o algoritmo de *hashing* SHA-256;

- A maioria das criptomoedas alternativas ao *Bitcoin* (*altcoins*) utilizam esse tipo de consenso;

- Alguns *altcoins* usam algoritmos de *hashing* diferentes (como Scrypt);

- Existem também formas modificadas de consenso, como o GHOST, que leva em consideração blocos órfãos;

- Além de *Proof of Work*, há experimentações com *Proof of Stake*, *delegated Proof of Stake* e outros mecanismos de consenso.

### **Escalabilidade de Algoritmos de Consenso**

- A maior dificuldade para um novo algoritmo de consenso escalar é a necessidade de atingir uma escala global antes de ser atacado;

- O *Bitcoin* conseguiu fazer isso porque foi ignorado nos primeiros anos, permitindo que ele se fortalecesse antes de ser alvo de ataques.

## **Algoritmos de Consenso como Disciplina Científica**

- O estudo de algoritmos de consenso emergiu como uma possível nova disciplina científica no campo da Computação Distribuída;

- Desde o artigo de Satoshi Nakamoto, a área tem se expandido rapidamente, com centenas de trabalhos acadêmicos publicados;

- O consenso está se tornando uma parte integral dos currículos de Ciência da Computação, marcando o nascimento de uma nova área de pesquisa.

## **Processo de Consenso no *Bitcoin***

- O processo começa com um debate de propostas de melhorias (BIPs) discutidas entre os desenvolvedores;

- Após consenso na comunidade, o software é testado, implementado e então lançado na rede;

- Depois que o software é lançado, os usuários devem atualizar suas versões, e o consenso entre diferentes grupos da rede deve ser atingido.

## **Partes Interessadas no Consenso**

- São cinco os principais grupos no consenso:

  * **Desenvolvedores**: responsáveis pela implementação de referência;

  * **Mineradores**: implementam o consenso na mineração de blocos;

  * ***Exchanges***: validam transações para conversão de moedas;

  * **Carteiras (*Wallets*)**: criam e validam transações;

  * **Comerciantes**: validam transações ao aceitar *Bitcoin* como forma de pagamento.

- Há riscos de divergência entre mineradores e outros grupos, se os mineradores divergirem dos comerciantes, *Exchanges* e carteiras, as transações mineradas podem ser rejeitadas.

## **Dificuldade de Modificar o Consenso**

- “Ossificação” do protocolo: à medida que o protocolo do *Bitcoin* se torna mais difundido, ele também se torna cada vez mais difícil de ser modificado;

- Exemplos como o protocolo IPv4 mostram como a “ossificação” impede inovações e mudanças rápidas.

## **Limitação de Capacidade e Debate sobre o Tamanho dos Blocos**

- Até hoje, o tamanho máximo de um bloco é de 1 MB, o que limita a rede a processar entre 3 e 7 transações por segundo;

- Há um debate sobre como e quando aumentar o limite de capacidade;

- Diversas propostas de aumento do tamanho dos blocos para 8MB, seguido por aumentos continuos a cada 4 anos, já foram apresentadas;

- O aumento para 20 GB por bloco até 2032 pode permitir a rede processar até 100 mil transações por segundo, equiparando-se à capacidade da rede Visa.

## **Transações *Off-chain***

- Há tecnologias que permitem realizar transações fora da *Blockchain* (*off-chain*) e registrar apenas o saldo final na *Blockchain*;

- Isso aumenta significativamente a capacidade efetiva de transações da rede.

- Assim como o dinheiro físico circula várias vezes na economia, a *Blockchain* pode registrar transações que representam várias operações *off-chain*.