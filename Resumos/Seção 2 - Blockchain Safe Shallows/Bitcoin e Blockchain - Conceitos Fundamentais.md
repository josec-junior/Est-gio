# ***Bitcoin*** **e *Blockchain* \- Conceitos Fundamentais**

## **Contexto Histórico e o Surgimento do *Bitcoin***

- Em 2008, o mundo está em crise com o estouro da bolha americana;

- Vários bancos estão à beira da falência, e os Bancos Centrais dos principais países desenvolvidos fizeram injecções utilizando o dinheiro dos contribuintes para tentar salvar esses bancos;

- No entanto, várias pessoas também foram à falência, mas não receberam esse apoio, o que gerou insatisfação popular e protestos.

- Nesse contexto de crise, é criado o *Bitcoin* como uma resposta às falhas do sistema bancário tradicional e visando evitar cenários como esse;

- Um artigo descrevendo o funcionamento do *Bitcoin* foi publicado ainda em 2008, por **Satoshi Nakamoto**, pseudônimo de um programador ou grupo de programadores anônimo(s);  
    
- E em 2009 foi feito o primeiro bloco do Bitcoin, chamado de *Genesis Block*.

## **Características do *Bitcoin***

- O *Bitcoin* é uma unidade de troca, assim como o dinheiro tradicional, com um sistema de pagamento embutido, o qual permite transferências diretas sem intermediários;

- Além disso, o *Bitcoin* funciona como **Reserva de Valor**, ou seja, ele pode ser utilizado para preservar o valor do dinheiro ao longo do tempo, como uma espécie de “cofre digital”;

- O **limite de emissão** do *Bitcoin* é o que permite que ele funcione dessa maneira, pois nunca existirão mais do que **21 milhões de *Bitcoins* em circulação**, independentemente de quanto tempo passe ou de quantas pessoas o utilizem;

- O *Bitcoin* funciona graças a uma combinação de criptografia, *Blockchain*, redes descentralizadas e uma espécie de “Engenharia de Incentivo”, a qual consiste em os utilizadores ganharem dinheiro à medida que seguem as regras do *Bitcoin*;

- Apesar dessas vantagens, existem vários serviços que o sistema financeiro tradicional fornece que o *Bitcoin* ainda não é capaz de realizar, como fazer empréstimos e comprar ações. 

## **Diferenças entre *Bitcoin* e o Sistema Financeiro Tradicional**

- Algumas das principais características no Sistema Financeiro Tradicional e como é feito no *Bitcoin*:

### **Contabilidade**

- **Sistema Tradicional**: Centralizado, com o banco controlando saldos;

- ***Bitcoin***: Feito pela *Blockchain*, algo como se fosse um livro gigantesco, contendo todas as transações já realizadas no mundo do *Bitcoin*.

### **Armazenamento**

- **Sistema Tradicional**: Bancos só guardam uma fração do dinheiro depositado (**reserva fracionada**), se todos os clientes do banco resolverem sacar dinheiro na mesma hora, o banco quebra, pois não tem dinheiro de todo mundo ao mesmo tempo;

- ***Bitcoin***: Não há frações, se você possui 2 *Bitcoins*, eles são 100% seus.

### **Segurança**

- **Sistema Tradicional**: Segurança institucional, cada banco tem a sua forma de segurança, como biometria, senhas e tokens;

- ***Bitcoin***: Segurança feita por criptografia.

### **Emissão de Moeda**

- **Sistema Tradicional**: Depende de políticas econômicas (governos podem imprimir dinheiro);

- ***Bitcoin***: Pré-definido desde o início (máximo de 21 milhões de *Bitcoins*).

### **Transações**

- **Sistema Tradicional**: Realizadas de forma **centralizada**, dependendo de um **banco**;  
- ***Bitcoin***: Realizadas de forma **distribuída**, em uma **rede *peer-to-peer*** (ponto-a-ponto).

### **Autenticação**

- **Sistema Tradicional**: Desempenhada de forma centralizada, sendo feita pelo banco, por exemplo: um comprovante de pagamento;

- ***Bitcoin***: Desempenhada de forma distribuída, sendo feita pela própria *Blockchain*, onde todas as transações ficam registradas.

### **Regulamentação**

- **Sistema Tradicional**: Regulamentado pelo Banco Central;

- ***Bitcoin***: Regulamentação ainda indefinida na maioria dos países, sendo visto como algo benéfico por alguns e perigoso, por outros.

### **Processo de Decisão**

- **Sistema Tradicional**: Arbitrário, sendo decidido por instituições centrais, como o Banco Central;

- ***Bitcoin***: Democrático, mudanças precisam de consenso entre os participantes da rede.

### **Controle do Dinheiro**

- **Sistema Tradicional**: O banco controla o dinheiro, podendo ser congelado ou perdido em falências;

- ***Bitcoin***: Controle total do usuário, mesmo ordens judiciais não podem congelar *Bitcoins*.

## ***Blockchain***

- *Blockchain* é uma cadeia de blocos, onde cada bloco contém uma série de dados, como transações (no caso do *Bitcoin*), podendo conter qualquer tipo de dado, como imagens, vídeos, textos, etc;

- Caba bloco contém informações sobre o bloco anterior, formando a assim uma cadeia de blocos conectados entre si;

- A *Blockchain* é caracterizada pela **imutabilidade**, ou seja, se um dado em um bloco for alterado, o bloco inteiro e todos os blocos seguintes serão modificados;

- Isso garante a segurança da *Blockchain* e funciona graças a uma função matemática chamada **Função *Hash***. 

### **Função *Hash***

- Função matemática que transforma um dado de entrada (***input***) em um código de saída, de tamanho fixo chamado ***output***;

- O *input* pode ter qualquer tamanho, mas o *output* sempre terá um tamanho fixo, sendo uma sequência de letras e números;

- Um exemplo ilustrativo de função *Hash* em textos como “Fox” ou até frases maiores, apesar do tamanho do *input* variar, o *output* tem sempre o mesmo formato:

![Exemplo ilustrativo de uma Função Hash][imageExemploHash]

### **Propriedades Criptográficas da Função *Hash***

- **Fácil de Computar**  
  * Dado um *input*, é fácil para o computador calcular o *output* correspondente, no exemplo ilustrado, “Fox” resulta em um *hash* específico (DFCD3454).

- **Livre de Colisão**  
  * É muito improvável que dois *inputs* diferentes gerem o mesmo *output*, mesmo com infinitos *inputs* e um número limitado de *outputs*, encontrar uma colisão é praticamente impossível.

- **Unidirecional**  
  * Dado um *output*, é muito improvável ou praticamente impossível descobrir qual foi o *input* original sem testar todos os *inputs* possíveis.

- **“*Puzzle-Friendly*”**  
  * Pequenas mudanças no *input* resultam em grandes mudanças no *output*, no exemplo ilustrado, a mudança de uma palavra em uma frase gera *hashes* completamente diferentes.

- Graças a essas propriedades criptográficas que a *Blockchain* é segura.

### ***Blockchain*** **e Função *Hash***

- Cada bloco da *Blockchain* contém:  
  * O ***hash*** **do bloco anterior** (também chamado de *hash pointer*);  
  * O ***hash*** **bloco atual**, o qual é gerado com base nos dados e no *hash* do bloco anterior anterior;  
  * **Dados do bloco**, como transações ou outras informações.

![Blockchain][imageBlockchain]

- Como cada bloco da *Blockchain* contém o *hash* do bloco anterior, além do *hash* do próprio bloco (sendo um *hash* único), isso é fundamental para garantir que a *Blockchain* seja inviolável.

### **Tentativa de Fraude e Garantia de Segurança**

- Suponhamos um ataque de um Hacker:  
  * Se um hacker alterar um bloco, todos perceberão, pois o *hash* não corresponderá mais aos dados;

  * O hacker precisaria modificar o *hash* do próprio bloco e o *hash* do bloco anterior para todos os blocos subsequentes, para manter a cadeia, o que demandaria uma quantidade imensa de recursos computacionais.

![Tentativa de Hackear a Blockchain][imageBlockchainHackeada]

- Qualquer tentativa de falsificação exigiria recriar toda a *Blockchain* a partir do ponto modificado, o que torna a falsificação inviável;

- A segurança do *Bitcoin* e outras criptomoedas que utilizam *Blockchain* é garantida pelas propriedades das funções *hash* criptográficas e pela estrutura de ligação entre os blocos.

## **Assinaturas Digitais**

- O *Bitcoin* tem um sistema de segurança para garantir que apenas o dono possa usar os *bitcoins* de sua “conta”;

- As **Assinaturas Digitais** garantem a segurança das transações no *Bitcoin*.

### **Propriedades das Assinaturas Digitais**

- **Somente o dono pode assinar** \- Apenas quem possui a chave secreta pode assinar;

- **Qualquer um pode verificar a assinatura** \- A chave pública é usada para verificar se a assinatura é autêntica;

- **Assinatura atrelada ao documento** \- Cada assinatura é única para o documento específico e não pode ser copiada para outro documento.

### **Funcionamento das Assinaturas Digitais**

- Assinaturas Digitais funcionam através de um sistema criptográfico chamado Criptografia de Chave Pública;

- Onde o dono da assinatura possui duas chaves geradas pelo computador, através de uma função matemática:  
  * **Chave Secreta (*Secret Key*)** \- Apenas o dono conhece;  
  * **Chave Pública (Public Key)** \- Pode ser compartilhada publicamente para verificar assinaturas.

- Um exemplo ilustrativo:  
  * José gera uma chave secreta e uma chave pública;

  * Ele então assina um documento, utilizando sua chave secreta para gerar uma assinatura única para aquele documento, e o envia, junto com a assinatura dele (espécie de código único atrelado ao documento) e a chave pública para Maria;

  * Maria recebe o documento e verifica a assinatura com a chave pública de José e a assinatura atrelada ao documento.

![Funcionamento das Assinaturas Digitais][imageAssinaturasDigitais]

### **Verificação de Assinaturas Digitais**

- A verificação de assinaturas digitais é feita utilizando uma **função matemática** que recebe o documento, a assinatura atrelada ao documento e a chave pública e retorna um resultado informando se a assinatura é verdadeira ou falsa;

- Qualquer um pode verificar se uma assinatura digital é verdadeira, basta pegar um documento, a assinatura dele, e a chave pública e utilizar a função matemática referida anteriormente.

### **Impossibilidade de Falsificação**

- Como cada assinatura é única para o documento, sendo gerada usando a chave secreta e o documento, então não adianta utilizar uma assinatura atrelada a um documento e tentar combinar com outro documento;

- Somente quem possui a chave secreta pode assinar, portanto, enquanto a chave secreta for mantida em sigilo, ninguém pode usar os *bitcoins* da pessoa dona dessa chave.

### **Associações no Sistema *Bitcoin***

- No sistema de *Bitcoin*, uma chave pública é equivalente a uma conta bancária;

- Cada pessoa pode ter quantas chaves públicas quiser e cada um delas vai estar atrelado a uma chave secreta;

- Para realizar uma transação, o destinatário informa sua chave pública, e o remetente usa essa informação para enviar *bitcoins*.

## **Criando uma Moeda Virtual (*CentralCoin*)**

- Os conceitos de *Blockchain* e seu uso com funções *hash* criptográficas e do Sistema de assinaturas digitais permitem criar uma moeda digital, mas ainda não o *Bitcoin*;

- Os problemas resolvidos pelo sistema financeiro tradicional são:  
  * **Controle de Saldo**: Quem tem quanto dinheiro;  
  * **Registro de Transações**: Quem transferiu quanto dinheiro para quem.

- Nas moedas digitais, o principal problema é definir quem transferiu quanto dinheiro para quem (Registro de Transação);

### **Moeda Digital Centralizada (*CentralCoin*)**

- A moeda digital que será criada chama-se *CentralCoin*, ela é baseada em *Blockchain*, assim como o *Bitcoin*, e usa o sistema de assinaturas digitais;

- Mas ela é diferente do *Bitcoin*, pois ela possui uma autoridade central, chamada Banco Central (não confundir com o Banco Central do Brasil);

- Todas as transações na *CentralCoin* são armazenadas na *Blockchain*, a qual é pública, assim como no *Bitcoin*;

- As moedas podem ter qualquer valor, por exemplo o *Bitcoin*: divisível em até 100 milhões de partes, sendo a unidade mínima o **Satoshi**, podendo ser comprada uma fração pequena de *Bitcoin***;**

- O processo de transações na *CentralCoin* consiste em:  
  * **Transações de criação de moedas**: O banco central é responsável por criar novas moedas e as distribuir;  
  * **Transações de pagamento**: moedas são “destruídas” e novas moedas são criadas para realizar o pagamento.

### **Processo de Criação de Moedas**

- Cada transação, tanto de criação de moedas como de pagamento, recebe um identificador único, esse identificador é equivalente ao nome da transação (Exemplo: “ID 77”);

- Dentro da transação de criação, várias moedas podem ser geradas;

- Cada moeda criada possui:  
  * **Índice**: por exemplo: “Moeda 77(1)”, “Moeda 77(2)” e “Moeda 77(3)”;

  * **Valor**: cada moeda pode ter qualquer valor, por exemplo: a Moeda 77(1) vale 5 *CentralCoins,* a Moeda 77(2) vale 1.2 *CentralCoins* e a Moeda 77(3) vale 0.003 *CentralCoins*;

  * **Chave pública do destinatário**: cada moeda criada é atribuída a uma chave pública específica (equivalente a identificação da pessoa), o sistema não precisa saber a identidade da pessoa, apenas a chave pública.

- No *CentralCoin*, apenas o banco central pode criar novas moedas, este processo é similar ao de imprimir dinheiro no sistema tradicional;

- As moedas criadas podem ser distribuídas para qualquer pessoa com uma chave pública, de acordo com as regras estabelecidas pelo banco central.

![Exemplo de Criação de Moedas][imageCriarMoedas]

### **Processo de Pagamento**

- Para realizar um pagamento, o remetente deve utilizar moedas que já possui, essas moedas são identificadas na transação, por exemplo: José usa a “Moeda 65(2)”, “Moeda 73(1)” e “Moeda 15(4)” para pagar Maria;

- Essas moedas são destruídas durante a transação de pagamento e novas moedas são criadas para os destinatários;

- Assim como no processo de criação, o pagamento também envolve a criação de novas moedas, por exemplo: José cria a “Moeda 123(1)” valendo 12 *CentralCoins* e a transfere para a chave pública de Maria;

- Se necessário, o remetente também pode criar uma moeda de troco para si próprio;

- O remetente (nesse caso, José) deve assinar digitalmente a transação utilizando sua chave secreta, essa assinatura garante que ele é o dono das moedas que está gastando e que a transação é autêntica;

- A chave pública associada à chave secreta permite que o banco central valide a transação;

- O banco central verifica se a transação é válida, o que inclui:  
  * Conferir a assinatura digital do remetente;

  * Verificar se as moedas usadas não foram consumidas anteriormente;

  * Certificar-se de que a soma das moedas consumidas seja maior que a soma das moedas criadas (a diferença é a **Tarifa de Transação**).

- Se todas as verificações forem positivas, o banco central adiciona essa transação à *Blockchain* e o pagamento está completo;

- O destinatário (nesse caso, Maria) não precisa estar online ou fazer algo para receber as novas moedas, pois elas ficam registradas na *Blockchain* até serem utilizadas em uma nova transação.

![Exemplo de Pagamento][imagePagamento]

### **Tarifa de Transação**

- A diferença entre o valor total das moedas consumidas e o valor das moedas criadas durante a transação representa uma tarifa;

- No caso da *CentralCoin*, essa tarifa vai para o banco central como forma de pagamento pelos serviços de verificação e adição de blocos;

- No caso do *Bitcoin*, essa tarifa é destinada aos mineradores, que desempenham o papel de validar e adicionar as transações à *Blockchain*.

### **Sistema de Troco**

- Em muitos casos, o remetente não possui moedas exatas para o valor que quer pagar;

- O sistema permite que ele crie moedas para o valor total e se houver excedente, ele pode criar uma nova moeda de troco para si;

- Por exemplo, José quer pagar 12 *CentralCoins*, mas só possui moedas de 10 e 4 *CentralCoins*, ele destrói ambas, cria uma moeda de 12 para pagar Maria e outra de 2 para si, como troco.

### **Diferenças em Relação ao Sistema Bancário Tradicional**

- Transações não envolvem saldos em contas, apenas a criação e destruição de moedas;

- A desvantagem da *CentralCoin* é a dependência de uma autoridade central para garantir a segurança, essa centralização vai contra a filosofia de descentralização que o *Bitcoin* busca implementar;

- No sistema do *Bitcoin*, uma das maiores inovações é a eliminação de uma autoridade central, não há um banco central ou qualquer entidade única responsável por verificar ou validar transações;

- Em vez disso, o *Bitcoin* usa uma **rede distribuída** de nós (computadores conectados ao sistema) que validam as transações e mantêm a *Blockchain* de maneira descentralizada, eliminando o problema de confiar em uma única entidade, como no caso da *CentralCoin*.

## ***Bitcoin***

- A diferença entre a *CentralCoin* e o *Bitcoin* é que na *CentralCoin* há o banco central, responsável por realizar a verificação das transações e manter a *Blockchain*;

- Enquanto no *Bitcoin*, o papel do banco central é substituído por uma rede distribuída *peer-to-peer* (P2P) de computadores e mineradores, onde não há hierarquia e todos os computadores se conectam entre si, sem a presença de um nó central;

- Esses computadores precisam seguir um protocolo de consenso, para entrarem em acordo, mesmo que alguns desses computadores sejam maliciosos, ou seja, a segurança da rede tem que ser garantida para funcionar mesmo que haja a presença de hackers;

### **Estrutura da Rede *Bitcoin***

- **Rede P2P**:  
  * Qualquer pessoa pode participar da rede *Bitcoin*, basta baixar o software ***Bitcoin Core***, no próprio site do *Bitcoin*;

  * Geralmente os usuários comuns usar softwares de carteiras, chamados *Wallets*, que facilitam o uso da rede;

- **Nó da rede Rede *Bitcoin***: qualquer computador conectado à rede *Bitcoin* é um nó desta rede;

- Existem dois tipos de nós:  
  * ***Full Nodes*** **(Nós Completos)**: armazenam toda a *Blockchain* e validam transações, mantendo a consistência da *Blockchain*;

  * ***Light Nodes*** **(Nós Leves)**: armazenam apenas parte da *Blockchain* e dependem dos *Full Nodes* para mais informações.

- Mineradores geralmente operam como *Full Nodes* e as carteiras podem ou não ser *Light Nodes*.

### **Função dos Full Nodes**

- Responsáveis pela validação de transações e novos blocos criados pelos mineradores;

- *Full Nodes* também armazenam e mantêm a *Blockchain* atualizada;

- *São* consultados pelos *Light Nodes* para obter informações adicionais quando necessário.

### **Processo de Transação no *Bitcoin***

- Exemplo de José transferindo *Bitcoins* para Maria:

1. José escolhe as moedas que está enviando;

2. Ele cria moedas novas e assina a transação digitalmente;

3. A transação é enviada para um nó da rede *Bitcoin*;

4. O nó valida a transação e a retransmite para outros nós da rede;

5. Esse processo usa o Protocolo de “Fofoca” (*Gossip Protocol*), que propaga a transação para a rede inteira.

![Processo de Transação no Bitcoin][imageTransacao]

### **Desafios de Sincronização na Rede *Bitcoin***

- Vários usuários podem enviar transações simultaneamente de diferentes partes do mundo;

- O problema da Rede *Bitcoin* não possuir um nó central é como a rede entra em acordo sobre a validade e a ordem dessas transações;

- A solução para isso é o **Protocolo de Consenso**.

### **Papel dos Mineradores**

- Os mineradores substituem o papel do banco central (da *CentralCoin)* na validação de transações e construção de blocos;

- Competem entre si pelo direito de adicionar o próximo bloco na *Blockchain*;

- Cada bloco contém mais do que uma transação, até um máximo de 1MB por bloco;

- Cada minerador monta seu próprio bloco, que pode conter diferentes transações;

- Quando um minerador encontra um bloco:  
1. Informa aos outros mineradores;

2. Outros mineradores verificam o bloco;

3. Se válido, o bloco é adicionado à *Blockchain*.

- Os mineradores sempre estendem o ramo mais longo da *Blockchain*.

![Processo de Mineração][imageMineradores]

## **Proof of Work (PoW)**

- Os mineradores competem para validar e adicionar o próximo bloco à *Blockchain*, através do protocolo *Proof of Work* (Prova de Trabalho);

- Blocos contêm informações de transações,o *hash* do bloco anterior, um *nonce* (um número aleatório ajustado repetidamente pelos mineradores para encontrar um *hash* válido) e um *hash* único, esse *hash* é feito computando todas as transações, o *hash* do bloco anterior e o *nonce*;

- O minerador que vai ter o direito de adicionar o próximo bloco na *Blockchain*, é o primeiro minerador que conseguir encontrar um bloco cujo *hash* tenha um determinado número de zeros no começo (essa quantidade de zeros é chamada de **dificuldade**);

- Mineradores montam blocos com transações e ficam testando diferentes valores de ***nonce*** até encontrar um *hash* que atenda à dificuldade estabelecida;

- A **dificuldade** é calculada periodicamente para garantir que um bloco novo seja encontrado a cada 10 minutos, independentemente do número de mineradores.

![Um bloco da Blockchain detalhado][imageBlocoDetalhado]

### **Propriedades Criptográficas do *Hash***

- **Fácil de computar**: Rápido de calcular o *hash* de um bloco, mas complexo encontrar um *hash* com o número certo de zeros;

- **Unidirecional**: É muito improvável descobrir o *input*, dado o seu *hash*;

- **“*Puzzle Friendly*”**: Pequenas mudanças no *input* resultam em grandes mudanças no *hash*;

- Essas propriedades garantem que os mineradores não possam prever o resultado do *hash* ou utilizem soluções anteriores, fazendo pequenas modificações para essa solução e chegar rapidamente numa solução para o bloco novo.

### **Processo de Mineração**

- Mineradores tentam calcular um *hash* válido mudando o *nonce* repetidamente;

- Quando um minerador encontra um bloco válido, ele transmite a solução para a rede;

- Os outros mineradores validam implicitamente ao começarem a minerar o próximo bloco com base nesse.

- O minerador que encontra o bloco válido primeiro tem o direito de adicionar esse bloco à *Blockchain* e recebe:  
  * **Recompensa em *Bitcoins***: através de uma ***Coinbase Transaction***, onde o minerador cria novos *bitcoins* para si próprio;

  * **Taxas de Transação**: pagas por usuários que enviam transações dentro daquele bloco.

- **Halving**: a recompensa de blocos diminui pela metade a cada 4 anos, controlando a emissão de *bitcoins*, no começo, cada Coinbase Transaction começou com 50 *bitcoins* por bloco, depois 25, agora está em 6.25 *bitcoins* por bloco (em 2024), esse valor irá continuar caindo pela metade até chegar a 0;

- Isso é feito de forma que no futuro, o número máximo de *bitcoins* em circulação será de 21 milhões;

- No início, era possível minerar *bitcoins* com computadores convencionais, mas atualmente isso é inviável devido à alta **dificuldade**;

- Mineração de *Bitcoin* é um negócio profissional, com investimentos consideráveis em hardware específico, os **ASICs** (***Application-Specific Integrated Circuits***), criados exclusivamente para minerar *bitcoins* de maneira eficiente e muito mais rápida que CPUs e GPUs;

- Atualmente, a mineração de *Bitcoin* consome cerca de 0,16% da eletricidade mundial, o que tem gerado debates sobre o impacto ambiental;

### ***Mining Pools***

- Como encontrar um bloco individualmente pode demorar anos para mineradores pequenos, foram criados as ***Mining Pools*** (Pools de Mineração);

- Mineradores unem seus recursos para tentar encontrar blocos juntos, o coordenador do *pool* divide o problema de mineração em subproblemas menores, que são distribuídos para os mineradores resolverem;

- Quando o *pool* encontra um bloco, os mineradores enviam suas soluções de volta ao coordenador, ele as verifica e caso a solução atenda à **dificuldade** do bloco, o coordenador submete essa solução à rede do *Bitcoin*;

- A recompensa é dividida pelo coordenador do *pool*, entre todos os mineradores participantes, proporcionalmente ao trabalho realizado durante o período em que o bloco foi encontrado;

- Mineradores recebem recompensas menores, mas de forma mais constante, **reduzindo o risco de minerar sem sucesso por longos períodos**;

- Os *pools* podem **otimizar o processo de mineração**, escolhendo a criptomoeda mais rentável a cada momento.

![Exemplo de Mining Pool][imageMiningPool]

### **Segurança e a Finalidade da Mineração**

- O grande consumo de energia e o esforço envolvido na mineração são justificados pelo aumento da segurança e integridade da *Blockchain*;

- Quanto mais difícil e custosa a mineração, mais difícil é para um atacante comprometer a rede;

- O gasto de energia e poder computacional cria um sistema onde a manipulação da *Blockchain* se torna inviável para atacantes.

## **Evitando o Gasto Duplo**

- A mineração é um processo dispendioso, tanto em termos de tempo quanto de consumo de energia elétrica;

- Muitos críticos consideram o processo ineficiente devido ao alto consumo de energia e os grandes investimentos necessários;

- A mineração parece ser inútil à primeira vista, pois os mineradores resolvem funções que não têm propósito prático além de manter a segurança da rede *Bitcoin*;

- O trabalho dos mineradores garante a segurança da rede *Bitcoin*, pois a mineração evita o “**Gasto Duplo**”, ou seja, a possibilidade de uma mesma moeda ser usada em mais de uma transação;

- A rede *Bitcoin* resolve esse problema através do mecanismo de ***Proof of Work*** (**Prova de Trabalho**), assegurando que as transações e blocos sejam verificados de forma descentralizada.

### **Bifurcações na *Blockchain***

- Às vezes, dois mineradores podem encontrar blocos ao mesmo tempo, criando uma bifurcação (divisão) na *Blockchain*;

- Isso cria dois blocos simultâneos, onde parte dos nós da rede reconhecem um bloco, enquanto outros reconhecem o outro;

- Mineradores devem seguir a **regra do bloco mais longo**:  
  * A cadeia mais longa é considerada a válida;

  * Quando novos blocos são adicionados, o ramo mais curto é abandonado e os mineradores mudam para o ramo mais longo;

  * As transações no bloco abandonado são eventualmente incluídas em blocos subsequentes.

### **Ataque de Gasto Duplo**

- Em um ataque de gasto duplo, um indivíduo tenta gastar a mesma moeda duas vezes em diferentes transações;

- Por exemplo: José compra um curso com *Bitcoin* e, depois de receber o curso, tenta incluir uma transação em outra bifurcação para “reverter” o pagamento;

- Para que esse ataque seja bem-sucedido, o atacante precisa minerar blocos mais rápido do que a rede inteira;

- Para evitar ataques de gasto duplo, há uma boa prática de aguardar **seis confirmações** de blocos subsequentes, após a inclusão de uma transação.

### **Ataque de 51%**

- Um ataque bem-sucedido ao *Bitcoin* só seria se possível se o atacante conseguisse controlar **mais de 51% do poder computacional** (***Hash Power***) da rede;

- Para realizar um ataque de 51%, o hacker precisaria investir milhões de dólares em hardware e energia, além de minerar mais rápido que todos os outros mineradores da rede;

### **Relação entre Segurança e Incentivos**

- O sistema *Bitcoin* funciona porque os incentivos econômicos encorajam os mineradores a seguir as regras;

- Mineradores ganham recompensas por minerar blocos válidos e que serão aceitos na cadeia de longo prazo;

- Um ataque bem-sucedido comprometeria a confiança no sistema, fazendo com que o *Bitcoin* perca o seu valor.

### **Tipos de Ataques no *Bitcoin***

- Muitos ataques relacionados ao *Bitcoin* não envolvem o sistema em si, mas o roubo de **chaves secretas** dos usuários, permitindo que os atacantes transfiram os *bitcoins* das **chaves públicas** das vítimas, para as suas próprias chaves;

- Esses ataques não são equivalentes aos ataques de gasto duplo e não comprometem a segurança do *Bitcoin* em si.

## ***Bitcoin*** **e Outras Moedas na Prática**

- **Sistema Bancário Tradicional**: ter 5 mil reais em uma conta significa que o banco promete devolver esse valor quando solicitado;

- ***Bitcoin***: não há saldo ou conta registrada em algum lugar específico, o que se tem são **moedas** que foram criadas e estão associadas a uma **chave pública** controlada pelo usuário.

- A **chave pública** funciona como o “endereço” da conta dela, onde as moedas estão associadas;

- A **chave secreta** seria como uma “senha”, ela dá a capacidade de gastar as moedas associadas à chave pública;

- Por exemplo: Maria possui uma chave pública e uma chave secreta:  
  * As moedas criadas e endereçadas à chave pública de Maria determinam seu saldo;

  * Neste exemplo, Maria possui 4.52 *bitcoins* endereçados à sua chave pública.

- **Conferência de Saldo**: para saber o seu saldo, Maria precisa verificar todas as transações na *Blockchain* que apontam moedas para a sua chave pública.

### **Gasto de *Bitcoins***

- Para gastar *bitcoins*, o usuário deve:  
  * Selecionar as moedas que estão endereçadas à sua chave pública;  
  * Assinar a transação usando sua **chave secreta**.

- **Processo Automatizado**: O software de carteira faz isso automaticamente, sem a necessidade do usuário procurar manualmente na *Blockchain* ou selecionar moedas.

### **Segurança no Armazenamento de *Bitcoins***

- **Chave Secreta**: Fundamental para garantir a segurança e o controle sobre os *bitcoins*, **guardar *bitcoins*** \= **guardar a chave secreta**;

- **Multiplicidade de Chaves Públicas:** Usuários podem ter várias chaves públicas;

- Se uma chave secreta for perdida ou roubada, apenas os *bitcoins* associados àquela chave pública específica estarão em risco;

- **Ter *Bitcoins*** significa **ter uma chave secreta** associada a uma **chave pública** para a qual existem moedas na *Blockchain*;

### **Criação de Chaves Públicas e Secretas**

- **Geração Automática**: As chaves públicas e secretas são geradas automaticamente por softwares de carteira (*Wallets*);

- **Exemplo de Geração de Chaves**: Sites como o [WalletGenerator](https://www.walletgenerator.com/) permitem a criação de um par de chaves (pública e secreta) para uso em transações com *bitcoins*;

- **Uso da Chave Pública**: Compartilhada para receber pagamentos;

- **Uso da Chave Secreta**: Deve ser mantida em segredo para garantir a segurança da chave pública;

## **Carteiras (*Wallets*)**

- As carteiras são na maior parte das vezes softwares que ajudam a guardar a chave secreta e a realizar transações com *Bitcoin*;

- São características desejadas de uma carteira:  
  * **Disponibilidade**: acessível a qualquer momento;  
  * **Segurança**: deve ser difícil de roubar;  
  * **Conveniência**: facilidade em realizar transações.

- *Bitcoin* é mais usado como investimento e armazenamento de valor do que moeda do dia a dia, logo, a segurança é a característica mais priorizada.

### **Tipos de Carteiras**

- Existem diversos tipos de carteiras, cada uma com um propósito, os principais tipos são:

  * **Carteira de Papel**  
    * Chave pública e chave secreta escritas em papel;

    * A **segurança** depende de onde o papel é armazenado;  
      * Se bem guardado, pode ser seguro;  
      * Riscos de destruição física, como umidade e rasgos;  
      * Se a chave secreta for perdida, os *bitcoins* ficam inacessíveis.

    * **Vantagens**:  
      * Imune a ataques virtuais (se não houver cópias no computador).

    * **Desvantagens**:  
      * Inconveniente para uso diário;  
      * Suporta apenas um par de chave pública e secreta;  
      * Vulnerável em caso de perda ou destruição.

![Exemplo de Carteira de Papel][imageCarteiraDePapel]

* **Carteira de Hardware**  
  * Dispositivo físico semelhante a um pen drive;

    * **Extremamente seguras**:  
      * Chaves secretas geradas e armazenadas no dispositivo;  
      * Transações são feitas no hardware, sem expor a chave ao computador;  
      * Protegida mesmo se o computador estiver infectado.

    * **Vantagens**:  
      * Permite a recuperação de *bitcoins* em caso de perda do dispositivo através de uma “semente”;  
      * Suporta múltiplos pares de chaves.

    * **Desvantagens**:  
      * Preço elevado, sendo viável apenas para grandes investimentos.

![Exemplo de Carteira de Hardware][imageCarteiraDeHardware]

* **Carteira de Software**  
  * Software para desktop ou smartphone;

    * A **segurança** depende da segurança do dispositivo (computador/smartphone), se o dispositivo for infectado, a carteira pode ser comprometida;

    * **Vantagens**:  
      * Suporta múltiplos pares de chaves;  
      * Funcionalidades adicionais, como conversão entre criptomoedas;  
      * Praticidade no uso e envio de *bitcoins*.

    * **Desvantagens**:  
      * Vulnerável a ataques se o dispositivo não for seguro.

![Exemplo de Carteira de Software][imageCarteiraDeSoftware]

* **Carteira Online**  
  * Carteira armazenada na nuvem e acessada pela internet;

    * A **segurança** depende do servidor que a hospeda, risco de ataque hacker e o usuário não tem acesso direto à chave secreta.

    * **Vantagens**:  
      * Prática e fácil de usar;  
      * Ideal para pequenas quantidades de *bitcoins*.

    * **Desvantagens**:  
      * Não recomendada para grandes quantias devido ao risco de perda de controle sobre as chaves.

![Exemplo de Carteira Online][imageCarteiraOnline]

- A **escolha da carteira** depende da quantidade de *bitcoins* e das necessidades de segurança e conveniência;

- **Riscos e Benefícios**:  
  * Carteira mais seguras são menos convenientes e vice-versa;  
  * É crucial pensar no tipo de investimento para escolher a carteira adequada.

## ***Exchanges***

- Na prática, as criptomoedas são ativos como qualquer outro: ações, ouro, *commodities*, etc;

- *Exchanges* (corretoras) é a maneira mais tradicional e segura de comprar *bitcoins*;

- Funcionamento semelhante ao da bolsas de valores e casas de câmbio, onde o preço é determinado pelo mercado;

- A criação de contas em *Exchanges* envolve a inserção de dados pessoais como CPF, RG, e fotos para segurança.

### **Funcionamento de Transações em *Exchanges***

- O processo envolve:  
1. Depósito de dinheiro ou *bitcoins*, pelo usuário, na exchange;  
2. A *Exchange* não realiza a transferência imediatamente, apenas “registra” a intenção de compra e venda dentro do sistema;  
3. A *Exchange* garante que quando o usuário solicitar um saque (de dinheiro ou *bitcoins*), a transação será concluída.

- Garantias da *Exchange*:  
  * A *Exchange* “promete” que, ao solicitar o saque, o comprador receberá o valor que comprou (dinheiro ou *bitcoins*) e o vendedor receberá a quantia correta pela venda.

### **Riscos Associados às *Exchanges***

- **Falta de regulamentação**:  
  * As *Exchanges* ainda não possuem uma regulamentação, logo, não são obrigadas a manter uma reserva de segurança, como os bancos;

  * Não há garantias como o Fundo Garantidor de Créditos (FGC) dos bancos;

  * A *Exchange* pode usar dinheiro do cliente para qualquer finalidade, sem supervisão.

- **Ataques cibernéticos**:  
  * *Exchanges* são alvos de hackers por concentrarem grandes quantias de criptomoedas;

  * Exemplos: hackeamento da *Mt. Gox* e *Youbit*.

- **Falência de *Exchanges***:  
  * Se uma Exchange falir ou for hackeada, os usuários podem perder seus fundos sem chances de ressarcimento.

### **Esquemas de Pirâmide Relacionados à *Bitcoin***

- **Características dos esquemas**:  
  * Marketing multinível, mineração na nuvem, retornos garantidos;

  * Promessas de lucros sem riscos, com foco em trazer mais investidores;

  * Dificuldades para sacar o dinheiro indicam possível fraude.

### **Cuidados ao Usar *Exchanges***

- Verifique a reputação da Exchange e a existência de medidas de segurança;

- Tome cuidado com promessas de retornos altos e fáceis.

## **Anonimato no *Bitcoin***

- *Bitcoin* é visto por alguns como uma moeda usada para atividades ilícitas, como lavagem de dinheiro;  
- Há a crença de que o *Bitcoin* seja completamente anônimo.

### **Debate sobre Anonimato no *Bitcoin***

- ***Andreas Antonopoulos*** afirma que o *Bitcoin* é frequentemente caracterizado erroneamente como anônimo, mas é possível associar identidades a endereços usando análise de padrões de transação;

- ***Wikileaks*** defende que o *Bitcoin* é uma moeda digital segura e anônima, embora não seja impossível rastrear as transações.

### **Exemplo Histórico da *Silk Road***

- ***Silk Road*** foi um mercado na *Deep Web* que utilizava *Bitcoin* para pagamentos e a tecnologia do Tor para garantir o anonimato;

- ***Dread Pirate Roberts***, criador do Silk Road, foi preso por descuido ao vazar um endereço de e-mail, mostrando que falhas humanas podem comprometer o anonimato.

### **Anônimo vs. Pseudônimo no *Bitcoin***

- **Definição de pseudônimo**: no *Bitcoin*, o usuário não se identifica diretamente, mas suas transações são públicas e podem ser rastreadas;

- **Transações rastreáveis**: todas as atividades financeiras no *Bitcoin* estão registradas na *Blockchain*, o que torna possível associar uma chave pública a uma identidade.

- **Associação com identidade**: é fácil associar uma chave pública a uma pessoa através de serviços que requerem identificação, como *Exchanges*;

- **Carteiras**: mesmo usando carteiras online, fornecer dados como e-mail pode expor a identidade;

- **Compras físicas**: ao fazer compras com *Bitcoin*, o endereço de entrega pode ser usado para descobrir a identidade do comprador;

- **Entrada e saída de dinheiro**: o uso de *Exchanges* para converter *Bitcoin* em moeda fiduciária deixa rastros que podem ser monitorados pelas autoridades.

### **Limitações do *Bitcoin* para lavar dinheiro**

- **Monitoramento por autoridades**: grandes quantidades de dinheiro movimentadas podem ser facilmente rastreadas pelas autoridades fiscais e financeiras.

### **Técnicas para Melhorar o Anonimato**

- Criar uma nova chave pública a cada transação aumenta a dificuldade de rastrear as atividades, mas não garante anonimato completo;

- Usar navegadores anônimos, como o Tor, pode dificultar o rastreamento de IPs, melhorando a privacidade;

- Usar VPNs, pois elas podem ocultar o endereço IP e aumentar a privacidade.

### **Serviços de Mistura (*Mixing Services*)**

- “*Mixing*” é o processo de misturar *bitcoins* de diferentes usuários para dificultar o rastreamento de transações;

- Por exemplo: vários usuários depositam *bitcoins* em um serviço de *mixing*, e cada um recebe de volta *bitcoins* misturados de forma que a origem e o destino das moedas ficam embaralhados.

## **Introdução ao *Ethereum***

- Como o *Bitcoin* foi projetado para uma aplicação específica, como uma forma de transferir moedas e realizar pagamentos;

- No entanto, a tecnologia (*Blockchain*) em que ele está baseado permite muitas outras aplicações, isso levou ao surgimento de diversas ***Altcoins*** (*Alternative Coins*, moedas alternativas ao *Bitcoin*);

- *Ethereum* possui o **segundo maior *cap rate*** de todas as criptomoedas (atrás apenas do *Bitcoin*), ou seja, o valor monetário de todas as moedas em circulação;

- Comunidade ativa e em crescimento, desenvolvendo tanto a criptomoeda quanto seu ecossistema;

- Conceitualmente diferente do *Bitcoin*, o que permite explorar novos conceitos;

- Projeto ambicioso, com impacto significativo no mundo.

### **Diferenças em Relação ao *Bitcoin***

- *Bitcoin* foi projetado como uma forma de transferência de valor;

- *Ethereum* agrega capacidades computacionais, permitindo rodar programas dentro da rede (*Smart Contracts*, Contratos Inteligentes).

### **Capacidades do *Ethereum***

- Além das funções básicas do *Bitcoin*, o *Ethereum*:  
  * Permite executar programas de computador dentro da rede;

  * Funciona como um “*Bitcoin* com capacidade de um computador”;

  * Em teoria, o único limite do *Ethereum* é a criatividade de quem desenvolve os programas para a rede.

- São funções adicionais do *Ethereum:*  
  * Transferências de dinheiro;

  * Execução de ***Smart Contracts*** (Contratos Inteligentes), programas que recebem uma quantia monetária e executam um serviço computacional, sendo usados em transações automáticas e outras aplicações computacionais na rede *Ethereum* (como uma máquina de venda automática);

  * Usado como ferramenta de captação de recursos para empresas (ICO \- ***Initial Coin Offering***).

### **Identidade no *Ethereum***

- No *Bitcoin*, a identidade está ligada a uma chave pública que controla um saldo, como uma conta bancária;

- No *Ethereum*, a identidade está mais próxima de um CNPJ, associada a contas que podem interagir com contratos inteligentes e transações;

- Como no *Bitcoin* é possível ter várias chaves públicas e chaves secretas, no *Ethereum* é possível ter várias contas;

### **Propriedade no *Ethereum***

- No *Ethereum*, pode-se possuir e transacionar ativos que vão **além da moeda**, como itens digitais;

- Um exemplo é o ***CryptoKitties***, um jogo de colecionar gatinhos digitais:

  * Compra e venda de gatinhos digitais, armazenados na *Blockchain* e com a propriedade única e imutável;

  * Preços variam, alguns chegando a valores altíssimos;

  * Os gatinhos podem ser comprados, vendidos e até mesmo reproduzidos, tudo gerenciado por contratos inteligentes.

- O *CryptoKitties* é um exemplo de como o *Ethereum* expande as funcionalidades da Blockchain e de toda a tecnologia introduzida pelo *Bitcoin*, permitindo novos tipos de aplicações, como contratos inteligentes e jogos baseados em *Blockchain*.

## **Características Básicas do Ethereum**

- O *Ethereum* foi projetado para suportar múltiplas aplicações, ao contrário do Bitcoin, que tem um propósito específico;

- Da mesma forma que o *Bitcoin*, possui uma moeda nativa (*Ether*), esse *Ether* é altamente divisível (pode chegar até 1 milhão de partes menores), o que facilita a execução de ***Smart Contracts***;

- Mineração ***Memory Hard*** (Focada em Memória), diferente do *Bitcoin*, o *Ethereum* utiliza memória em vez de poder de processamento para minerar, evitando a especialização excessiva;

- Há uma discussão sobre a futura transição da mineração de ***Proof of Work*** (PoW) para ***Proof of Stake*** (PoS).

- Além de transferir valores, no Ethereum também é possível **transferir dados e processar códigos**, isso permite a execução de *Smart Contracts*, que são fundamentais para a rede.

### **Transparência e Fundadores**

- Ao contrário do *Bitcoin*, o *Ethereum* tem **fundadores conhecidos**, o que traz maior legitimidade para o projeto;

- Criada com o dinheiro arrecadado na criação do *Ethereum*, a ***Ethereum Foundation*** (Fundação Ethereum) coordena e financia o desenvolvimento da rede, trabalhando com desenvolvedores, mineradores e governos;

- Por isso, o Ethereum tem um **Consenso Guiado**, embora a rede funcione de forma descentralizada, a fundação influencia nas decisões e direções do projeto.

### **Descentralização e Críticas**

- Apesar do Ethereum se basear em consenso, algumas poucas pessoas têm grande influência sobre o projeto;

- Críticas surgem em relação à rede ser uma “Ditadura benevolente” devido à forte influência de indivíduos específicos.

### **Capacidades Computacionais do Ethereum**

- O *Ethereum* funciona como uma “***Blockchain*** **programável**”, pois possui a capacidade de executar qualquer tipo de algoritmo na rede;

- Teoricamente, qualquer programa pode ser executado, o que torna o *Ethereum* **Turing-completo**, em teoria;

- O que permite que isso aconteça é a ***Ethereum Virtual Machine*** **(EVM)**, a qual é fundamental para o funcionamento da rede, permitindo a execução de contratos inteligentes e outras aplicações descentralizadas;

- Os seis elementos principais do Ethereum são:  
  * Blockchain;

  * Criptografia de chave pública;

  * Mineração;

  * Redes descentralizadas;

  * ***Smart Contracts*** **(Contratos Inteligentes)**;

  * ***Ethereum Virtual Machine*** **(EVM)**.

## ***Accounts and States*** **(Contas e Estados)**

- O Ethereum é uma **máquina de estados** e seu funcionamento é baseado em **contas**;

- No *Ethereum*, existem dois tipos de contas:

  * ***Externally Owned Accounts*** **(EOA)**: Contas de usuários controladas por chaves secretas;

  * ***Smart Contract Accounts***: Contas controladas por códigos (*Smart Contracts*), sendo ativadas por EOAs.

- Similaridades entre contas de usuários e contas de contratos inteligentes:  
  * Ambas possuem um **endereço** e um **saldo**;  
  * Ambas podem armazenar valores e informações adicionais.

### **Funcionamento das Contas no Ethereum**

- No *Ethereum*, cada conta tem um estado específico em um momento no tempo, exemplo: saldo e dados associados;

- Cada nova transação ou bloco que chega pode **atualizar o estado** de uma conta;

- Por exemplo: se uma transação é processada, o saldo da conta da Maria pode ser atualizado de 4.52 *Ether* para 2.50 *Ether*;

![Exemplo do Funcionamento de Contas de Usuário][imageContasUsuario]

- No *Bitcoin*, o saldo é baseado em **transações não gastas**;

- No *Ethereum*, o saldo é atualizado diretamente, de forma mais intuitiva e similar a uma conta bancária.

### **Contas de *Smart Contracts***

- Contas de *Smart Contracts* também possuem estados que podem ser atualizados com base nas transações;  
- Exemplo: uma máquina de refrigerante representada como um contrato inteligente no *Ethereum*:  
  * Tem saldo e pode armazenar informações como quantos refrigerantes ainda estão disponíveis;

  * O estado dessa conta pode ser alterado com transações, como quando alguém compra um refrigerante.

![Exemplo de Funcionamento de Contas de Smart Contracts][imageContasSmartContracts]

### **Armazenamento dos Estados das Contas**

- Os estados das contas no *Ethereum* são armazenados fora da *Blockchain*, em uma estrutura de dados chamada ***State Tree***;

- Todos os nós da rede mantêm cópias desses estados e os atualizam a cada novo bloco;

- As transações armazenadas na *Blockchain* são responsáveis por alterar esses estados;

- O *Ethereum* escolheu esse modelo por dois motivos:  
  * **Simplicidade Conceitual**: Trabalhar com contas e estados é mais intuitivo para programadores e facilita a criação de programas na rede, especialmente com o foco em contratos inteligentes;

  * **Eficiência Computaciona**l: O modelo de contas no *Ethereum* é mais eficiente do que o modelo de transações não gastas do *Bitcoin*, o que é crucial para rodar **contratos inteligentes** e outras operações complexas na rede.

## ***Ethereum Virtual Machine*** **(EVM)**

- A *Ethereum Virtual Machine* (EVM) é essencial para o funcionamento da rede;

- No *Bitcoin*, os mineradores verificam e validam transações financeiras (moedas destruídas e criadas);

- No *Ethereum*, além de validar transações, os mineradores também executam códigos complexos, já que o *Ethereum* é Turing-completo;

- Todos os nós da rede devem executar o código em todos os blocos para manter os estados atualizados, criando um desafio de **eficiência**.

### **Problemas de Compatibilidade entre Máquinas**

- Diferentes dispositivos, como computadores, smartphones e até mesmo máquinas de refrigerantes, precisam executar o mesmo código;

- Uma comparação com consoles de videogames antigos, cada console usava cartuchos específicos, assim como diferentes sistemas operacionais exigem versões específicas de softwares;

- O problema é que o código do *Ethereum* precisa ser executado **independentemente do hardware**.

### **A solução: *Ethereum Virtual Machine* (EVM)**

- A EVM é solução para garantir que o mesmo código possa rodar em diferentes máquinas, independentemente de suas características;

- A EVM atua como um **intermediário**, cada dispositivo instala sua própria versão da EVM, mas a interação com o código do *Ethereum* é sempre a mesma;

- Isso permite que o código seja executado uniformemente em diferentes tipos de dispositivos.

### **Comparação com a Java Virtual Machine (JVM)**

- O conceito da EVM é semelhante ao da *Java Virtual Machine* (JVM), assim como aplicações podem ser acessadas em qualquer sistema operacional com a JVM, o código do *Ethereum* pode ser executado em qualquer dispositivo com a EVM;

- A JVM cria uma máquina virtual que executa essas aplicações, independentemente do hardware ou sistema operacional.

### **Benefícios da EVM**

- Assim como a JVM, a EVM elimina a necessidade de programadores se preocuparem com a máquina onde o código será executado;

- Os programadores podem usar **linguagens de alto nível** como ***Solidity***, a linguagem do *Ethereum*, para escrever contratos inteligentes de maneira mais fácil e intuitiva.

## **Gas no Ethereum**

- Todos os nós da rede *Ethereum* devem executar o código de todos os blocos, o que resulta em ineficiência;

- A execução do código ocorre tanto em computadores potentes quanto em dispositivos com capacidades limitadas.

### **Limitações da Rede *Ethereum***

- **Custo de processamento**: Executar códigos na rede gera custos, especialmente para os mineradores;

- **Vulnerabilidade a ataques DDoS (*Denial of Service*)**: Um atacante pode enviar programas inúteis para sobrecarregar a rede, tornando-a mais lenta e cara;

- **Algoritmos com problemas**: Códigos com erros ou travamentos podem prejudicar a rede;

- **Loops infinitos**: Programas que repetem operações indefinidamente podem travar a rede.

**Solução: Gas no *Ethereum***

- **Gas** é o sistema de combustível utilizado para rodar transações e programas na rede *Ethereum*;

- Cada transação na rede tem um custo em Gas, que deve ser pago em *Ether*;

- O Gas é necessário para executar qualquer operação, e quanto mais complexo for o programa, maior será o custo.

### **Funcionamento do Gas**

- Para rodar um programa na rede, o usuário deve fornecer uma quantidade de Gas junto com o código;

- Existem três possíveis resultados para a execução de uma transação:  
1. **Execução bem-sucedida**: Se houver Gas suficiente, a transação é concluída, e o Gas restante é devolvido;

2. **Falta de Gas**: Se o programa consumir todo o Gas antes de finalizar, ele será interrompido e a operação não será concluída;

3. **Limite de Gas**: Cada transação tem um limite de Gas que pode ser utilizado, evitando a execução de programas excessivamente complexos.

### **Benefícios do Sistema de Gas**

- **Protege contra loops infinitos**: A execução do programa para quando o Gas acaba, evitando travamentos na rede;

- **Impede ataques DDoS**: Atacar a rede com programas inúteis se torna caro, pois cada execução requer pagamento em Gas;

- **Incentiva a eficiência**: Os programadores são incentivados a criar códigos mais eficientes para gastar menos Gas;

- **Facilita a precificação**: O custo em Gas para uma transação é constante, mas o preço do Gas varia de acordo com a demanda da rede.

### **Variação no Preço do Gas**

- Para uma mesma operação, o custo em Gas é sempre o mesmo;

- Como o preço do Gas varia de acordo com a demanda, o preço do Gas aumenta quando a rede está congestionada, tornando as transações mais caras;  
- Em momentos de alta demanda, apenas transações prioritárias são processadas rapidamente, enquanto outras aguardam o preço do Gas cair.

![Gráfico do Preço do Gas ao longo do tempo][imageGraficoGas]

## ***Smart Contracts*** **(Contratos Inteligentes)**

- ***Smart Contracts*** são a funcionalidade mais famosa do Ethereum e uma das principais inovações dessa tecnologia;

- Eles permitem que qualquer aplicação seja executada na *Blockchain*, com limitações apenas na capacidade de criação de contratos;

- A execução dos *Smart Contracts* segue o princípio de que tudo o que foi programado para acontecer, e de fato acontece, sem necessidade de confiança entre as partes envolvidas.

### **Funcionamento dos *Smart Contracts***

- Tomamos como exemplo: Maria compra um curso online de José, no modelo tradicional, a transação depende de questões de confiança;

- Já com *Smart Contracts*, a lógica interna do contrato garante a execução sem a necessidade de confiança;

- A lógica do contrato funciona como uma **máquina de refrigerante**: Maria envia *Ether* e informações, e o contrato retorna o produto ou serviço, conforme a programação;

- A maioria dos contratos são **autônomos**, operando sem intervenção humana, apenas obedecendo à programação interna.

### **Origem dos *Smart Contracts***

- O conceito de *smart contracts* foi introduzido em **1993**, por ***Nick Szabo***, que comparava esses contratos com os contratos legais tradicionais;

- Um *smart contract digital* trata-se de um conjunto de regras combinadas entre as partes e executado automaticamente quando as condições são atendidas, sem a possibilidade de violação, a menos que o contrato inclua uma cláusula de reversão.

### **Criação e Estrutura dos *Smart Contracts***

- No *Ethereum*, um *smart contract* é um conjunto de código e dados que residem em um uma conta na rede;

- Assim como as contas controladas por usuários, os *smart contracts* possuem um **endereço**, um **saldo de *Ether*** e recebem dados e instruções para execução de ações;

- A criação de um *smart contract* envolve a realização de uma transação que contém as **instruções para montar o código do contrato** e uma **quantidade de *Ether*** para pagar o minerador que processará essa transação;

- *Smart contracts* podem comunicar entre si, enviar mensagens para contas de pessoas e até mesmo realizarem autodestruição;

- A única limitação para o funcionamento de um *smart contract* é a capacidade de programá-lo corretamente.

### **Exemplos de Aplicações de *Smart Contracts***

- **Armazenamento Seguro de Fundos**:  
  * Por exemplo, José e Maria criam um *smart contract* que armazena o dinheiro deles e para retirar os fundos, é necessário obter a assinatura de ambos.

- **Compra Automatizada**:  
  * Maria quer comprar algo de uma “máquina de refrigerante” virtual, ela então envia *Ether* junto com as informações do produto desejado, e o contrato automaticamente realiza a transação, retornando o item.

- **Governança Descentralizada**:  
  * Empresas podem usar *smart contracts* para emitir **tokens** que funcionam como ações, investidores podem comprar esses tokens e usá-los para votar nas decisões da empresa, o contrato garante que as decisões sejam executadas com base na maioria dos votos.

## **DApps \- Aplicativos Descentralizados**

- *Smart contracts* funcionam como blocos ou tijolos para construir **aplicativos descentralizados (DApps)**;

- Aplicativos descentralizados (DApps), como o nome sugere, são diferentes dos aplicativos tradicionais por não terem controle centralizado;

- DApps variam em graus de descentralização, alguns são completamente descentralizados, como o *Bitcoin*, enquanto outros têm componentes centralizados e uma pequena parte descentralizada;

- A descentralização pode ser um espectro, com diferentes níveis entre aplicativos;

- ***BitTorrent*** é um exemplo de aplicativo descentralizado para compartilhamento de arquivos, sem um servidor central, resistente a tentativas de encerramento;

- DApps geralmente são *open-source*, sem intermediários, sem um ponto central de falha e com alta resiliência.

### **Diferenças entre DApps e Aplicativos Tradicionais**

- DApps, ao contrário dos aplicativos tradicionais, não possuem um ponto central de falha, o que aumenta a segurança e resiliência;

- Em um DApp totalmente descentralizado, todos os usuários participam da operação do aplicativo, tornando impossível parar sua execução sem interromper todos os usuários.

### **Vantagens da Descentralização**

- Resiliência contra censura ou controle;

- Maior transparência e segurança, pois o código é geralmente *open-source*;

- Ausência de intermediários, o que pode reduzir custos e aumentar a eficiência.

### **Exemplos Reais de DApps**

- ***HyperDragons***: Jogo de estratégia onde os jogadores podem comprar dragões únicos e usar tokens com valor monetário real;

- ***Geon***: Um aplicativo de marketing descentralizado que recompensa usuários que visitam locais físicos, com tokens;

- ***MakerDAO***: Criação de uma moeda estável (**DAI**) que sempre vale um dólar, oferecendo uma economia estável baseada em criptomoedas.

### **Desafios dos Aplicativos Descentralizados**

- ***Decentralized Autonomous Organization*** **(DAO)**: Um exemplo de DApp que fracassou devido a um bug no *smart contract* que permitiu o roubo de 50 milhões de dólares e resultou em um *hard fork* na *Blockchain* *Ethereum*, gerando as moedas *Ethereum* e *Ethereum Classic*;

- **A lição aprendida com a DAO**: Apesar da potencialidade dos *Smart contracts*, isso ainda está no começo e são suscetíveis a falhas;

- Apesar disso, o desenvolvimento de DApps continua crescendo, com potencial para criar uma sociedade mais descentralizada no futuro.

[imageExemploHash]: <https://github.com/user-attachments/assets/aecb3522-9dde-4a33-9233-e8bde00afe3a> 

[imageBlockchain]: <https://github.com/user-attachments/assets/7dd3d6fc-3786-40fa-be6b-b6f2d6b69e41>

[imageBlockchainHackeada]: <https://github.com/user-attachments/assets/5150b509-c1e0-4380-a382-555492e1ad58>

[imageAssinaturasDigitais]: <https://github.com/user-attachments/assets/b949abc2-ca32-44cc-b2d8-5d17c04f9dd6>

[imageCriarMoedas]: <https://github.com/user-attachments/assets/bebb3162-a258-43f4-a1c2-991df0d3fbf0>

[imagePagamento]: <https://github.com/user-attachments/assets/91d60dae-f433-4705-b103-fc95d5131250>

[imageMineradores]: <https://github.com/user-attachments/assets/897a2ec3-c7c8-4526-8ad7-81b6cbecd1aa>

[imageTransacao]: <https://github.com/user-attachments/assets/a63d7ca1-f7fb-4efc-8ab1-7a1aa85abc4e>

[imageBlocoDetalhado]: <https://github.com/user-attachments/assets/bc50a962-d07e-422d-a2bf-280402c98b73>

[imageMiningPool]: <https://github.com/user-attachments/assets/420ad2bc-0a4a-4f97-af77-5102a19fa6e6>

[imageCarteiraDePapel]: <https://github.com/user-attachments/assets/c0d1209d-e6c2-4404-9064-85c0f4fc1989>

[imageCarteiraDeHardware]: <https://github.com/user-attachments/assets/a9afb1c6-683c-4743-a293-412b511702ef>

[imageCarteiraDeSoftware]: <https://github.com/user-attachments/assets/015a45ce-e10a-4123-b93a-10b7edb56058>

[imageCarteiraOnline]: <https://github.com/user-attachments/assets/1ea1d52f-53fb-472b-8368-2d169b5ec39d>

[imageContasUsuario]: <https://github.com/user-attachments/assets/89ad4fda-183a-43b1-b2e8-3d93dfe1738a>

[imageContasSmartContracts]: <https://github.com/user-attachments/assets/54e5b027-5e27-4361-b0d0-963e6f1dc9c6>

[imageGraficoGas]: <https://github.com/user-attachments/assets/76b58db6-359d-4c36-bf52-47db7a0f85a5>