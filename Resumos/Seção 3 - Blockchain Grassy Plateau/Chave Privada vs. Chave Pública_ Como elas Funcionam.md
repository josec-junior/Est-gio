# **Chave Privada vs. Chave Pública: Como elas Funcionam**

- A chave privada é uma chave secreta utilizada para criptografar e descriptografar mensagens, ela é utilizada em conjunto com a chave pública e precisa ser sempre mantida em sigilo;

- Nas criptomoedas, as chaves privadas são utilizadas pelas carteiras para proteger os seus ativos, como elas não podem ser revertidas (decifradas), elas protegem seus ativos sem qualquer risco de comprometimento;

- Por exemplo, uma carteira de *Bitcoin* tem uma chave privada associada a ela, quando uma nova carteira é criada, as chaves privada e pública são geradas junto com ela;

- Após recebê-la, é essencial fazer um backup da sua chave privada em algum lugar seguro;

- Caso perca sua chave privada, não poderá acessar sua carteira ou seus fundos, portanto, é sempre uma boa ideia fazer um backup, seja anotando em um diário privado ou imprimindo.

- A chave pública, por outro lado, é utilizada apenas para criptografar a mensagem;

- Ela pode ser enviada a outras pessoas para fins de criptografia, uma vez que o remetente criptografa uma mensagem utilizando sua chave pública, você pode desbloqueá-la apenas com sua chave privada;

- Para entender como essas chaves funcionam, é preciso conhecer os dois tipos de criptografia.

## **Criptografia Assimétrica**

- A criptografia assimétrica é um algoritmo criptográfico que permite enviar mensagens de forma segura e funciona gerando um par de chaves privada/pública;

- Nesse algoritmo não é possível deduzir a chave privada a partir da chave pública;

- Assinaturas digitais são usadas para compartilhar uma chave pública, a chave privada, por sua vez, é armazenada de forma segura no software com criptografia.

## **Criptografia Simétrica**

- A criptografia simétrica utiliza apenas chaves privadas, este método é extremamente útil para criptografar dados em um servidor;

- A criptografia simétrica utiliza apenas chaves privadas, este método é extremamente útil para criptografar dados em um servidor;

- A criptografia assimétrica e a simétrica podem funcionar em conjunto, por exemplo, a criptografia assimétrica pode ser utilizada para enviar chaves privadas pela rede;

- Após chegar ao destino, as chaves privadas podem ser usadas para criptografar e descriptografar dados, permanecendo segura, pois foi enviada utilizando a criptografia assimétrica.

## **Funcionamento das Chaves**

- O processo começa quando alguém decide transferir criptomoedas para outra pessoa, pela *Blockchain*;

- Como usuário, você tem acesso apenas à sua chave privada e à sua chave pública, as chaves são uma sequência longa de números e letra;

- Aqui está um exemplo de uma chave de criptografia de 512 *bits*:

```plaintext
KaPdSgVkYp2s5v8y/B?E(H+MbQeThWmZq4t6w9z$C&F)J@NcRfUjXn2r5u8x!A%D
```

- A chave é gerada aleatoriamente a partir de um gerador de chaves de criptografia;

- Após iniciar uma transação, a *Blockchain* gera uma assinatura para garantir que a transação ocorra sem alterações ou gastos duplos, a assinatura é então usada para confirmar a transação.

## **Como a Chave Pública e o Endereço são Gerados**

- A chave pública também é gerada utilizando a chave privada, a chave pública passa então por uma função hash unidirecional, que por sua vez, gera seu endereço público;

- O endereço público é visível para todos e pode ser compartilhado para enviar criptomoedas ou fundos;

- É possível gerar tanto a chave pública quanto o endereço a partir da chave privada, entretanto, o processo inverso não é possível;

- Ou seja, você não pode gerar a chave privada mesmo que tenha o endereço ou a chave pública de uma pessoa.

- Tecnicamente seria possível reverter o processo, mas isso levaria mais de 40e31 (40 seguido de 31 zeros) anos com o computador mais potente, o que não é viável e portanto, torna todo o processo computacionalmente seguro.

## **Considerações Finais**

- Como usuário, você deve proteger sua chave privada a todo custo, não compartilhe sua chave com ninguém, ou você poderá perder seus fundos;

- Existem muitos golpes online que tentarão solicitar a sua chave privada, se alguém fizer isso, fuja imediatamente.