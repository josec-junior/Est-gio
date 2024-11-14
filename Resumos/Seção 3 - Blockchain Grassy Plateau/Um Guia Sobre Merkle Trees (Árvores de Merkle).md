# **Um Guia Sobre *Merkle Trees* (Árvores de *Merkle*)**

- Uma *Merkle Tree* (Árvore de *Merkle*) é uma estrutura de dados usada para a verificação segura de dados em um grande conjunto de informações;

- É também eficiente e consistente quando se trata de verificar esses dados, tanto o *Ethereum* quanto o *Bitcoin* utilizam Árvores de *Merkle*;

- **O Problema**:  
  * No núcleo de uma rede centralizada, os dados podem ser acessados a partir de uma única cópia, isso significa que não é necessário muito esforço para armazenar ou acessar os dados;

  * Entretanto, quando falamos de uma rede *Blockchain* descentralizada, as coisas se complicam, pois cada dado é copiado entre os nós, assim surge o desafio de acessar dados de forma eficiente;

  * Também é um desafio copiar os dados e compartilhá-los entre os nós, além disso, os dados compartilhados precisam ser verificados para cada um dos nós receptores.

- **A Solução**:  
  * As Árvores de *Merkle* permitem que *Blockchain* descentralizadas compartilhem dados, verifiquem-nos e os tornem confiáveis;

  * Elas organizam os dados de forma que não é necessário muito poder de processamento para compartilhar e verificar essas informações;

  * Também possibilitam transações seguras, graças ao uso de funções de *hash* e criptografia;

  * Satoshi Nakamoto foi o primeiro a implementar Árvores de *Merkle* na tecnologia *Blockchain* por meio do *Bitcoin*;

  * Sua aplicação abriu um novo ramo da Ciência da Computação, onde não é necessária uma autoridade centralizada;

  * Ele também usou Árvores de *Merkle* de forma extensa, implementando **Árvores de *Merkle* Rápidas**;

  * Entretanto, o conceito foi inicialmente introduzido por *Ralph Merkle*, que o patenteou em 1979, elas então receberam o nome em sua homenagem.

## **Funções de *Hash* Criptográficas**

- Uma função de *hash* é responsável por mapear qualquer forma de dado arbitrário de qualquer comprimento para uma saída de tamanho fixo;

- É uma função criptográfica e, por isso, é amplamente utilizada em criptografia, sendo eficiente e conhecida por uma propriedade única: a função **não pode ser revertida**;

- Trata-se de uma função unidirecional projetada para funcionar apenas dessa forma;

- *Hashing* tem várias utilidades, incluindo:  
  * Proteção de senhas;

  * Verificação e checagem de integridade de arquivos;

  * Criptomoedas.

- Existem várias famílias de *hash*, incluindo *Message Digest* (MD), *Secure Hash Function* (SHF) e *RIPE Message Digest* (RIPEMD);

- Se você usar o algoritmo de *hash* **SHA256** e inserir uma entrada como 101Blockchains, terá uma saída:
```perl
fbffd63a60374a31aa9811cbc80b577e23925a5874e86a17f712bab874f33ac9
```

- Em resumo, as principais propriedades das funções de *hash* incluem:  
  * **Determinística**: o mesmo dado de entrada sempre gera a mesma saída;

  * **Resistente a Pré-imagem**: dada uma saída de *hash*, é praticamente impossível descobrir a partir dela qual foi a entrada original;

  * **Computacionalmente Eficiente**: a função de *hash* é rápida para ser calculada;

  * **Não Reversível**: não pode ser revertida para descobrir a entrada original;

  * **Resistente a Colisões**: É muito difícil/improvável encontrar duas entradas diferentes que geram o mesmo valor de *hash*.

## **Funcionamento das Árvores de *Merkle***

- Tecnicamente, Árvores de *Merkle* são estruturas de dados onde o nó não-folha é definido como um valor *hash* de seus respectivos nós filhos;

- Isso também significa que a Árvore de *Merkle* está invertida, onde os nós folha estão na posição mais baixa;

- No núcleo das Árvores de *Merkle*, precisamos entender três termos importantes:  
  * **Raiz de *Merkle***;  
  * **Nós Folha**;  
  * **Nós Não-Folha**.  
- Se observarmos a Árvore de *Merkle* como um todo, ela é uma árvore de ponta-cabeça, capaz de resumir um conjunto completo de transações;

- Isso significa que o usuário pode verificar se uma transação faz parte do bloco ou não;

- Para que as Árvores de *Merkle* funcionem, utiliza-se *hashing*, basicamente, os pares de nós são “hashiados” repetidamente até que reste apenas um valor de *hash*;

- Esse valor valor final é conhecido como *Merkle Root* (Raiz de *Merkle*) ou *Root Hash* (*Hash* da Raiz);

- A árvore é criada de baixo para cima, usando os *hashes* das transações individuais, esses *hashes* individuais são conhecidos como IDs das transações;

- Os nós folha são os nós que contêm os *hashes* dos dados transacionais, no caso dos nós não-folha, eles armazenam o *hash* dos dois *hashes* anteriores;

- Outra característica importante das Árvores de *Merkle* é que elas são binárias, ou seja, precisa que os nós folha sejam em número par para funcionar;

- Caso haja um número ímpar de nós folha, o último *hash* será duplicado para tornar o número par.

## **Entendendo com Um Exemplo**

- Vamos tentar entender isso com um exemplo;

![Exemplo de Merkle Tree][imageMerkleTreeExample]

- Aqui, vemos que quatro transações ocorreram no bloco, essas transações são chamadas de X, Y, Z e W;

- As transações são então “hashiadas” e armazenadas nos nós folha, nomeados como *Hash* *X*, *Hash* *Y*, *Hash* *Z* e *Hash* *W*;

- Em seguida, os nós folha de *Hash X*, *Y*, *Z* e *W* são novamente “hashiados” para criar um *hash* combinado de *XY* e *ZW*;

- Por fim, esses dois *hashes* são utilizados para criar a *Merkle Root* (Raiz de *Merkle*) ou *Root Hash* (*Hash* da Raiz);

- Todo o processo de *hashing* pode ser realizado em um conjunto de dados muito grande, o que torna a estrutura de dados das Árvores de *Merkle* útil para redes descentralizadas;

- Como discutido anteriormente, o uso de algoritmos de *hashing* depende da implementação, entretanto, uma das funções de *hash*, mais comuns é a função de *hash* criptográfica SHA-2;

- Assim, uma transação pode ser verificada, se as transações anteriores forem verificáveis, graças aos valores de *hash*.

## **Sobre a Integridade dos Dados**

- A Árvore de *Merkle* é ideal para a integridade de dados, além disso, não é necessário percorrer toda a transação para verificar sua validade;

- As transações podem ser verificadas usando as informações armazenadas no cabeçalho do bloco, o valor da raiz de *Merkle* é também alterado dependendo das transações anteriores;

- Isso significa que os valores da raiz mudam frequentemente e podem ser utilizados para verificar transações quase que instantaneamente;

- Isso pode parecer um pouco similar a uma lista de *hashes*, mas, em uma lista *hashes*, é necessário baixar a lista completa para verificar as transações ou dados;

- Já no caso da Árvore de *Merkle*, não é necessário baixar toda a árvore para verificar as transações;

- Isso significa que a árvore inteira pode ser dividida em pequenos blocos de dados, que podem ser usados para verificar transações em toda a rede, esse conceito é conhecido como *Merkle Proofs* (Provas de *Merkle*).

## **Funcionamento das Árvores de *Merkle* no *Bitcoin*** 

- O *Bitcoin* foi a primeira criptomoeda a empregar Árvores de *Merkle* de forma eficaz, para garantir que os valores de *hash* estejam protegidos e não possam ser revertidos facilmente, ele utiliza o famoso Algoritmo de *Hash* Seguro **SHA-256**;

- O que significa que a saída dos valores de *hash* tem 256 bits de comprimento, no núcleo, as Árvores de *Merkle* são usadas para armazenar dados e também para pode de transações;

- No *Bitcoin*, cada bloco é conectado aos blocos anteriores usando valores de *hash*, é assim que toda a *Blockchain* é criada;

- Em um bloco, há cabeçalhos que contém informações importantes, como:  
  * *Hash* da *Merkle Root* (Raiz de *Merkle*);  
  * Número da Versão do Bloco;  
  * *Timestamp* (Carimbo de Data/Hora);  
  * *Nonce*;  
  * Dificuldade do Alvo de Mineração;  
  * *Hash* do Bloco Anterior.

- O uso de Árvores de Merkle dessa forma oferece diversos benefícios, um dos benefícios notáveis é a *Simple Payment Verification* (SPV, Verificação Simples de Pagamento em português);

- Esses SPVs são nós que também podem ser chamados de clientes leves, os quais baixam os cabeçalhos de blocos da cadeia mais longa, assim, não precisam baixar a *Blockchain* completa;

- Para fazer tudo isso, precisam verificar se possuem os cabeçalhos dos blocos da cadeia mais longa, é dessa forma que a implementação da Árvore de *Merkle* é feita no *Bitcoin*;

- No final, um SPV pode então usar a Prova de *Merkle* e verificar uma transação usando o *hash* da raiz da Árvore de *Merkle*.

## **Utilização das Árvores de *Merkle* no *Ethereum***

- A *Blockchain* do *Ethereum* também utiliza Árvores de *Merkle*, mas a abordagem é diferente da utilizada no *Bitcoin*;

- No *Ethereum*, é utilizada a ***Merkle Patricia Tree*** **(Árvore de Merkle Patricia)**, uma versão mais complexa da Árvore de *Merkle*, isso é possível porque o *Ethereum* é Turing-completo.

- Existem outras implementações de Árvores de *Merkle*, um dos exemplos mais populares é o ***Git***, um sistema de controle de versão distribuído, utilizado por programadores de todo o mundo para gerenciar os seus projetos;

- Outra implementação útil é encontrada no ***Interplanetary File System*** **(IPFS)**, um protocolo distribuído ponto a ponto, também é de código aberto e permite que dispositivos de computação participem e usem um sistema de arquivos ubíquo;

- Até mesmo autoridades certificadoras utilizam Árvores de *Merkle* a seu favor, elas as usam em mecanismos para criar logs de transparência de certificados verificáveis;

- Como o log é enorme, as Árvores de *Merkle* permitem que os computadores o verifiquem sem desperdiçar muito tempo e esforço;

- O último casos de uso que será discutido são os Sistemas de Banco de Dados, como ***Amazon DynamoDB*** e ***Apache Cassandra***;

- Esses bancos de dados distribuídos NoSQL controlam inconsistências usando Árvores de *Merkle* durante o processo de replicação de dados, se houver problemas, eles podem atualizar ou corrigir os dados usando o processo de reparo anti-entrópico;

- Em resumo, os casos de uso das Árvores de *Merkle* incluem:  
  * Sincronização de dados;  
  * Verificação de dados;  
  * Verificação de consistência.

## **Vantagens das Árvores de *Merkle***

- Dentre as vantagens das Árvores de *Merkle*, estão:

  * **Validar a integridade dos dados**: elas podem ser usadas de forma eficaz para validar a integridade dos dados;

  * **Exigem pouco espaço em disco**: a Árvore de *Merkle* ocupa pouco espaço em disco, em comparação com outras estruturas de dados;

  * **Pequenos pacotes de informações para verificação em redes**: Árvores de *Merkle* podem ser divididas em pequenos pacotes de informação para verificação;

  * **Verificação eficiente**: essa estrutura de dados é eficiente e leva pouco tempo para verificar a integridade dos dados.

## **Considerações Finais**

- A Árvore de *Merkle* é um dos conceitos mais importantes na Ciência da Computação;

- Ela é amplamente utilizada em muitos casos de uso, e sua utilização em criptomoedas deu origem a uma tecnologia revolucionária, a *Blockchain*.

[imageMerkleTreeExample]: <https://github.com/user-attachments/assets/efa593e1-e35c-44f8-830f-075282fa0b01>