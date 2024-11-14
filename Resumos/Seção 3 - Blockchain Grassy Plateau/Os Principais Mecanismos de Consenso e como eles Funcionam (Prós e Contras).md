# **Os Principais Mecanismos de Consenso e como eles Funcionam (Prós/Contras)**

- Os algoritmos de consenso são utilizados em diversos sistemas distribuídos, como na tecnologia *Blockchain*;

- Eles servem para que os nós da rede cheguem a um acordo sobre a validade de uma determinada transação.

## **Tipos de Mecanismos de Consenso**

- Existem diversos tipos de mecanismos/algoritmos de consenso, cada um com suas características, vantagens e desvantagens;

- Os principais tipos de algoritmos de consenso são os seguintes:

### ***Proof of Work*** **(PoW)**

- No *Proof of Work* (Prova de Trabalho), os mineradores competem entre si para resolver problemas matemáticos complexos;

- O primeiro a resolver esses problemas, valida um bloco e recebe uma recompensa em criptomoedas;

- **Prós**:  
  * Alta segurança, pois aumenta a dificuldade de ataques ao exigir um vasto poder computacional;

  * Descentralização, uma vez que qualquer um pode participar da mineração.

- **Contras**:  
  * Consumo elevado de energia, pois exige grandes quantidades de eletricidade;

  * Dificuldade em escalar conforme a rede cresce.

### ***Proof of Stake*** **(PoS)**

- No *Proof of Stake* (Prova de Participação), os validadores são escolhidos com base na quantidade de criptomoedas (*stake*) que possuem e estão dispostos a “apostar”;

- Quem valida corretamente aumenta suas chances futuras e quem comete erros, perde *stakes*;

- **Prós**:  
  * Mais eficiente energeticamente, pois há um menor consumo de eletricidade;

  * Processamento rápido.

- **Contras**:  
  * Risco de centralização se poucos controlarem a maioria das moedas.

### ***Delegated Proof of Stake*** **(DPoS)**

- No *Delegated Proof of Stake* (Prova de Participação Delegada), há uma eleição de delegados para validar as transações e criar novos blocos;

- São escolhidos com base em seu nível de atividade de contribuição para a rede;  
- **Prós**:  
  * Escalável e rápido;

  * Mais democrático.

- **Contras**:  
  * Risco de centralização em pequenos grupos de delegados.

### ***Leased Proof of Stake*** **(LPoS)**

- No *Leased Proof of Stake* (Prova de Participação Alugada), os usuários podem alugar suas moedas para delegados, em troca de recompensas;

- **Prós**:  
  * Permite que pequenos detentores de tokens participem do processo de validação, aumentando a descentralização;

  * Delegação do poder de validação com mais flexibilidade que o DPoS.

- **Contras**:  
  * Se um grupo pequeno controla grande parte das moedas alugadas, pode haver centralização de poder;

  * Vulnerável a ataques se os delegados dominantes forem maliciosos.

### ***Proof of Space and Time*** **(PoST)**

- Também conhecido como ***Proof of Capacity*** (PoC, Prova de Capacidade em português), os participantes devem alocar um certo espaço em disco, isso é feito gerando um conjunto de dados que pode ser armazenado em atributos de tempo;

- O espaço reservado é usado para validar transações e criar blocos, a escolha do minerador depende da quantidade de espaço alocado;

- Para assegurar que houve um tempo de espera entre a criação de blocos, um mecanismo como o uso de um verificador de tempo ou um modelo de relógio é aplicado, ajudando a evitar ataques e garantindo que quem participa do consenso realmente completou o trabalho dentro do período correto;

- **Prós**:  
  * Energeticamente mais eficiente em comparação ao *Proof of Work*, pois utiliza espaço em disco ao invés de processamento intensivo;

  * Descentralização, ao permitir que mais participantes possam se envolver, mesmo com hardware comum, promovendo uma rede mais descentralizada.

- **Contras**:  
  * Complexidade de implementação, pois a combinação dos dois (*Space and Time*) requer uma implementação cuidadosa para garantir a segurança;

  * Como está em um estágio mais inicial de adoção e não tem o mesmo nível de testes ou aceitação que o PoW ou PoS, é menos conhecido.

### ***Proof of Weight*** **(PoWeight)**

- O *Proof of Weight* (Prova de Peso) utiliza um conceito onde o “peso” (ou “weight”) é determinado por múltiplos fatores que, podem incluir a quantidade de criptomoedas que um nó possui, o tempo que os tokens foram mantidos ou a contribuição anterior de um nó à rede;

- Em essência, alguns fatores podem ser combinados para determinar a importância (ou peso) de um nó na validação de transações;

- Essa validação é proporcional ao peso atribuído, o que significa que nós com maior peso possuem mais influência na criação de novos blocos;

- **Prós**:  
  * Redução de centralização, ao considerar múltiplos fatores, o PoWeight pode ajudar a mitigar o problema de centralização observado em alguns outros algoritmos de consenso, como o PoS;

  * Incentivos proporcionais, visto que os nós que contribuem mais para a rede (em termos de tempo e quantidade de tokens) podem ter mais influência, o que pode incentivar um maior compromisso com a segurança da rede;

  * Maior escalabilidade, o que permite transações mais rápidas em comparação aos sistemas baseados apenas em *staking* ou *mining*.

- **Contras**:  
  * O cálculo do peso pode ser mais complexo, levando a desafios na implementação ou na compreensão do sistema, pelos participantes;

  * Como o PoWeight não é tão amplamente utilizado e testado quanto outros algoritmos de consenso, sua segurança e eficiência ainda precisam ser avaliadas mais a fundo em ambientes práticos.

### ***Proof of Authority*** **(PoA)**

- Também conhecido como ***Proof of Reputation*** (PoR, Prova de Reputação em português), nele, os validadores são escolhidos com base na sua reputação e identidade digital;

- **Prós**:  
  * Alta eficiência e baixa latência nas transações;  
  * Ideal para redes privadas ou permissionadas.

- **Contras**:  
  * Centralização, já que o poder de validação é restrito;  
  * Possibilidade de corrupção entre validadores autorizados.

### ***Proof of Burn*** **(PoB)**

- No *Proof of Burn* (Prova de Queimada), como o nome sugere, os participantes “queimam” criptomoedas, enviando-as para um endereço inalcançável, em troca do direito de validar blocos;  
- **Prós**:  
  * Cria um incentivo deflacionário com a “queima” de moedas;

  * Baixo consumo de energia, pois não requer cálculos intensivos.

- **Contras**:  
  * Perda permanente de ativos, pois moedas queimadas são permanentemente removidas do sistema;

  * Favorece aqueles que podem se dar ao luxo de queimar grandes quantias de moedas.

### ***Proof of Identity*** **(PoI)**

- No *Proof of Identity* (Prova de Identidade), há a validação de identidades dos validadores, por meio de documentos ou biometria;

- **Prós**:  
  * Segurança baseada na identidade, pois apenas validadores identificados e verificados podem participar;

  * Evita a entrada de atores maliciosos com identidades falsas.

- **Contras**:  
  * Exige a revelação de informações pessoais, o que pode ser contrário aos princípios de privacidade;

  * Tem melhor potencial de ser utilizado em ambientes permissionados e controlados.

### ***Proof of Activity*** **(POA \- híbrido)**

 

- O *Proof of Activity* (Prova de Atividade) combina elementos dos algoritmos de consenso *Proof of Work* e *Proof of Stake*, sendo a mineração feita como no *Proof of Work* e a validação realizada como no *Proof of Stake*;  
- **Prós**:  
  * Combinação dos pontos fortes do *Proof of Work* (PoW) e do *Proof of Stake* (PoS), segurança do PoW com a eficiência do PoS;

  * Há um equilíbrio entre segurança e eficiência.

- **Contras**:  
  * Mais complexo do que usar apenas o PoW ou o PoS;

  * Centralização parcial, podendo favorecer quem tem mais moedas para o PoS.

### ***Proof of Elapsed Time*** **(PoET)**

- O *Proof of Elapsed Time* (Prova de Tempo Decorrido) é utilizado em *Blockchains* permissionadas, onde os nós competem gerando um tempo de espera aleatório;

- **Prós**:  
  * Alta eficiência, pois gasta menos energia do que o PoW;

  * Segurança garantida por hardware, utilizando ambientes de execução confiáveis (***Trusted Execution Environments*** **\- TEEs**).

- **Contras**:  
  * Dependência de hardware especializado, pois requer o uso de tecnologias específicas (Intel TEEs);

  * Aplicável apenas em redes permissionadas.

### ***Proof of Importance*** **(PoImp)**

- No *Proof of Importance* (Prova de Importância), a participação e o número de transações determinam a importância de um nó, influenciando sua chance de validar blocos;

- **Prós**:  
  * Incentiva a participação, visto que usuários mais ativos possuem mais chances de validar blocos;

  * Adequado para redes que desejam maior envolvimento do usuário.

- **Contras**:  
  * Aqueles com mais recursos ou maior influência, possuem mais poder;

  * Pode ser suscetível a manipulação de pontuação de importância.

### ***Byzantine Fault Tolerance*** **(BFT)**

- Projetado para garantir tolerância a falhas bizantinas, permitindo que a rede possa alcançar consenso com a presença de nós maliciosos;  
- **Prós**:  
  * Resiliente contra nós maliciosos;

  * Garantia de segurança em redes permissionadas, além de possuir baixa latência e alta eficiência nesses ambientes.

- **Contras**:  
  * A comunicação entre nós aumenta exponencialmente à medida que o número de nós cresce;

  * Não escalável, pois funciona melhor em redes menores e permissionadas.

### ***Practical Byzantine Fault Tolerance*** **(PBFT)**

- Projetado para garantir que a rede continue funcional, mesmo com a presença de nós com comportamentos maliciosos ou com falhas;

- Baseia-se em comunicação entre nós que devem concordar sobre uma única versão do registro;

- Funciona bem em ambientes onde um número limitado de nós é confiável;

- **Prós**:  
  * Resistente a falhas e ataques, desde que menos de um terço dos nós sejam maliciosos;  
  * Alta segurança e consenso rápido.

- **Contras**:  
  * Dificuldade de escalabilidade em grandes redes, uma vez que o número de mensagens cresce exponencialmente.

### ***Delegated Byzantine Fault Tolerance*** **(DBFT)**

- Neste algoritmo de consenso, há o uso de delegados para alcançar o consenso de forma mais eficiente;

- **Prós**:  
  * Alta eficiência e velocidade, devido ao uso de delegados;

  * Melhor desempenho em redes públicas, com grandes volumes de transações.

- **Contras**:  
  * Pode levar à centralização de poder nas mãos de poucos delegados.

### ***Unique Node List*** **(UNL)**

- *Unique Node List* (Lista de Nós Exclusiva), como o nome sugere, trata-se de um método de consenso baseado na confiança, onde cada nó tem uma lista de nós confiáveis para validar transações;

- A UNL é crucial, pois ajuda a alcançar o consenso sem a necessidade de energia intensiva ou recompensas financeiras, cada nó confia nos nós de sua lista e a maioria deve concordar para validar um novo bloco de transações;

- **Prós**:  
  * Alta velocidade de transações e eficiência;

  * Baixo consumo de energia, pois esse mecanismo não depende de mineração intensiva, como no PoW, tornando-o mais sustentável;

  * Resiliência em algumas configurações.

- **Contras**:  
  * Risco de centralização devido à dependência da lista de nós;  
  * Problemas de confiança podem surgir caso a lista não seja gerenciada adequadamente.

### ***Directed Acyclic Graph*** **(DAG)**

- O *Directed Acyclic Graph* (Grafo Acíclico Dirigido) é uma estrutura de dados alternativo aos tradicionais mecanismos de consenso baseados em *Blockchain*, como PoW e PoS;

- Diferente da *Blockchain*, o DAG não organiza as transações em blocos encadeados linearmente, em vez disso, as transações são organizadas em um grafo, onde cada nova transação aprova transações anteriores, resultando em uma rede de transações;

- No DAG, cada transação é um nó e as transações subsequentes referenciam (ou aprovam) transações anteriores, isso cria uma estrutura de grafo acíclico, em que os nós são conectados, mas não há ciclos;

- Para que uma transação seja considerada válida, ela precisa aprovar um certo número de transações anteriores, esse sistema descentraliza a validação, já que cada usuário que cria uma transação também participa da validação de outras transações.

- **Prós**:  
  * Como cada transação é uma confirmação de outras transações, o sistema pode processar um número elevado de transações facilmente, portanto, é altamente escalável;

  * Frequentemente, as taxas de transação em redes baseadas em DAG são muito baixas ou inexistentes, tornando-as atraentes para uso em situações que requerem microtransações;

  * O uso de DAG permite transações rápidas com confirmação instantânea, já que múltiplas transações podem ser processadas simultaneamente.

- **Contras**:  
  * A implementação de um sistema baseado em DAG pode ser mais complexa do que uma *Blockchain* tradicional, especialmente em relação à gestão de conflitos e consistência de dados;

  * Embora seja resistente a ataques, a segurança total de um DAG pode ser uma preocupação, especialmente com redes menores onde a probabilidade de ataques maliciosos pode aumentar;

  * A falta de blocos e de um tempo rigoroso de criação pode levar a uma falta de clareza nas transações, dificultando algumas formas de auditoria.