# **Algoritmo de Consenso: Um Guia para Iniciantes**

- Algoritmo de Consenso tem um lugar importante na Ciência da Computação, ele é utilizado por computadores para chegar a um acordo sobre um único ponto do valor dos dados, e é usado apenas por processos ou sistemas distribuídos;

- Em uma rede distribuída, não é comum que todos os nós do sistema estejam online sempre que um consenso é necessário, além disso, há chances de que algumas informações se percam durante a transmissão;

- O algoritmo de consenso resolve o maior problema enfrentado por um sistema distribuído ou multiagente, ele **garante que o consenso seja alcançado com recursos mínimos**, **mantendo a integridade e transparência nas decisões tomadas**;

- Para garantir que todo o sistema seja tolerante a falhas, o algoritmo de consenso exige uma resposta de 51% dos recursos de cada vez;

- Por exemplo: uma pessoa envia 0,2 *bitcoins* de sua carteira para outra carteira, para garantir o sucesso da transação, o minerador minera o bloco no qual a transação precisa estar;

- Os mineradores, começam a minerar o bloco e após algum tempo, ele será validado, quando o sistema realizar o mínimo necessário de validações;

- No caso do *Bitcoin*, são necessárias apenas seis validações para se alcançar o consenso;

- Existem diversos tipos de algoritmos de consenso, isso significa que o funcionamento interno depende do tipo de algoritmo de consenso utilizado.

## **Aplicações do Algoritmo de Consenso**

- Há diferentes aplicações do algoritmo de consenso, embora seja usado principalmente por sistemas descentralizados, ele também pode ser útil em sistemas centralizados;

- Para entender melhor, segue uma lista dos casos de uso do algoritmo de consenso:  
  * A aplicação mais básica do algoritmo é decidir se uma transação em um ambiente distribuído, precisa ou não ser implementada, sendo utilizada pela maioria das redes de *Blockchain*;

  * O algoritmo de consenso também é muito útil para atribuir o status de líder a um nó da rede;

  * Por fim, ele também é utilizado para sincronizar dados em redes descentralizadas e garantir que a consistência seja alcançada.

## **Tipos de Algoritmos de Consenso**

- Há diversos tipos de algoritmos de consenso, sendo os seguintes os mais populares:

### ***Proof of Work*** **(PoW)**

- O *Proof of Work* (Prova de Trabalho) é o algoritmo de consenso mais popular, sendo utilizado pelo *Bitcoin*, *Litecoin* e antigamente pelo *Ethereum*;

- Foi criado por **Satoshi Nakamoto**, quando ele o utilizou em sua implementação do *Bitcoin*;

- Entretanto, é também a maneira mais ineficiente de se alcançar o consenso em uma *Blockchain*, pois requer uma grande quantidade de poder computacional;

- Funciona pedindo aos mineradores que resolvam problemas matemáticos complexos, uma vez que o *hash* é resolvido, o bloco é minerado e a transação é validada simultaneamente;

- Ao resolver os problemas, eles criam blocos os quais são posteriormente adicionados à *Blockchain*, para que isso funcione, 50% do trabalho deve ser sempre honesto.

### ***Proof of Stake*** **(PoS)**

- O segundo algoritmo de consenso mais popular é o *Proof of Stake* (Prova de Participação), utilizado pelo *Peercoin*, *Decred* e *Ethereum*, funciona apostando moedas em uma carteira;

- Os nós que apostaram suas moedas terão voz quando for necessário alcançar um consenso, uma das principais vantagens do PoS é que ele não consome muito poder computacional;

- O recurso gasto nesse caso, são os próprios tokens, se um nó apostador falhar em votar corretamente em uma transação, ele perderá sua participação;

- Se tiver sucesso, terá melhores chances de apostar na próxima transação;

- Assim como outros algoritmos de consenso, o PoS também tem a sua fraqueza: o problema do “*Nothing at Stake* (Nada em Jogo)”, ele ocorre ao validar ambos os lados de um *fork*.

### ***Delegated Proof of Stake*** **(DPoS)**

- O *Delegated Proof of Stake* (Prova de Participação Delegada) pode parecer semelhante ao PoS, mas sua abordagem é diferente;

- A primeira coisa que diferencia a ambos é que o DPoS não é totalmente descentralizado, nesse sistema, os apostadores não validam os blocos, mas escolhem os delegados;

- Esses delegados escolhidos então validam cada transação, geralmente, qualquer sistema descentralizado tem cerca de 20 a 21 delegados que validam as transações;

- Isso torna o DPoS excepcionalmente eficiente, sendo utilizado pelo *EOS*, *Steemit*, entre outros.

### ***Proof of Authority*** **(PoA)**

- O *Proof of Authority* (Prova de Autoridade) é utilizado para sistemas completamente centralizados, isso significa que contas aprovadas (as quais são escolhidas pelos administradores do sistema) realizam as validações em toda a rede;

- Ele é utilizado principalmente em redes privadas, devido à sua natureza mais centralizada.