# **AWS re:Invent 2022 \- Quando usar *Blockchain*: Casos de Uso Privados e Públicos**

- Para responder à questão de quando usar *Blockchain*, primeiro temos que responder à questão de para que servem as *Blockchains*;

- A *Blockchain* é útil quando as seguintes necessidades são atendidas:  
  * **Descentralização**: múltiplos participantes precisam compartilhar dados ou colaborar sem a presença de um controle centralizado;  
  * **Imutabilidade**: registros não podem ser alterados uma vez que são gravados;  
  * **Automação**: Processos automatizados (como os *Smart Contracts*/Contratos Inteligentes) são essenciais.

- Há quatro critérios que podem ser utilizados para ajudar a identificar quando a *Blockchain* deve ser usada:  
  * **Descentralização e Fragmentação de Processos**: se o seu fluxo de trabalho tiver processos de negócios fragmentados, conjuntos de dados isolados e múltiplas fontes de verdade ou fontes incompletas;

  * **Número de Partes Envolvidas**: se várias entidades estão envolvidas no processo (como empresas diferentes, departamentos segregados dentro de uma empresa, indivíduos ou até mesmo uma combinação desses três), *Blockchain* pode aumentar a eficiência;

  * **Igualdade de Direitos e Responsabilidades**: Um dos critérios mais importantes, quando as partes envolvidas precisam de direitos iguais e responsabilidades compartilhadas, *Blockchain* é útil, exemplos incluem o *Bitcoin* (camada de troca financeira peer-to-peer independente de uma entidade central) e *workflows* colaborativos empresariais;

  * **Requisitos de Desempenho**: Se há a necessidade de alta performance, por exemplo: 50.000 transações por segundo, a *Blockchain* tradicional pode não ser adequada devido aos limites de consenso (cerca de 20.000 transações por segundo, com finalização em 2-3 segundos).

## ***Blockchain*** **Privada vs. *Blockchain* Pública**

- Vale salientar que essas duas categorias de *Blockchain* não competem entre si, mas simplesmente abordam os casos de uso que você deseja resolver;

### ***Blockchain*** **Privada**

- É caracterizada por:  
  * ***Permissioned Networks*** (**Redes Permissionadas**) com controle sobre quem pode se juntar que papel irá desempenhar;

  * **Conhecimento prévio da identidade dos membros**, com forte controle de acesso a recursos e dados;

  * **Emprego de mecanismos de consenso mais eficientes**, como ***Proof of Authority*** (**PoA**), permitindo um maior ***throughput*** (**rendimento**) de transações e um consumo menor de energia.

- Casos de Usos:  
  * **Setores que precisam de privacidade e conformidade**, como finanças, cadeias de suprimentos e soluções de identidade governamental.

### ***Blockchain*** **Pública**

- É caracterizada por:  
  * ***Permissionless Networks*** (**Redes sem Permissão**), onde qualquer pessoa pode participar e deixar a rede;

  * Participantes não identificados, com grande foco em proteger o anonimato;

  * Inovação constante, com novas soluções como *Proof of Stake* (PoS) e *rollups* que aumentam a escalabilidade e a sustentabilidade.

- Casos de Usos:  
  * Setores como finanças descentralizadas (DeFi), *Non-fungible tokens* (NTFs, Tokens não fungíveis) que representam ativos digitais, e pagamentos digitais, os quais se beneficiam da natureza aberta e descentralizada.

## **Exemplos de Aplicações**

### ***Blockchain*** **Privada**

- **Rastreamento e Verificação de Produtos**  
  * Aplicável a diversas indústrias (um exemplo é o combate à falsificação e rastreamento de remessas em tempo real);

  * Desafios incluem a necessidade de alinhar múltiplas partes, mas já existem exemplos de sucesso, como o da ***CJ Corporation***.

- **Finanças**  
  * Aumenta a eficiência da liquidação de ativos como *bonds* e *private equity*, que ainda usam base de dados isoladas e reconciliações diárias.

- **Soluções de Identidade Governamental**  
  * Governos digitalizam credenciais (como carteiras de motorista e passaportes) e compartilham em tempo real, com precisão, entre diferentes agências e países.

### ***Blockchain*** **Pública**

- ***Decentralized Finance*** **(DeFi, Finanças Descentralizadas)**  
  * Redefiniu sistemas financeiros tradicionais, permitindo novas formas de participação em trocas financeiras, sem bancos convencionais e riscos centralizados;

  * Dentre as inovações, estão *exchanges* descentralizadas, plataformas de empréstimos e novos instrumentos como ***flash loans***.

- ***Digital Payments*** **(Pagamentos Digitais)**  
  * Utilização de criptomoedas e *stablecoins*, como **USDC**, com crescente aceitação por parte de consumidores e comerciantes;

  * Grandes *players*, como **Visa** e **MasterCard**, continuam expandindo suas ofertas nesse setor.

- **Non-Fungible Tokens (NFTs, Tokens Não Fungíveis)**  
  * Em 2021, houve uma popularização de *Blockchains* públicas com arte digital, colecionáveis e inovações;

  * Em 2022, o foco está na utilidade contínua para NFTs, promovendo mais engajamento e experiências sustentáveis de longo prazo.

## **Exemplos de Tecnologias *Blockchain***

### ***Blockchain*** **Privada**

- ***Hyperledger Fabric***  
  * Modular, altamente flexível, permite trocas de protocolos e banco de dados, com canais de privacidade entre pares.

- ***Hyperledger Besu***  
  * Compatível com *Ethereum*, sendo ideal para *workflows* (fluxos de trabalho) que possam integrar-se com *Blockchains* públicas.

- ***R3 Corda***  
  * Projetado para finanças e seguros, com alta taxa de transações e integração com sistemas financeiros existentes.

- **Outras**  
  * Há outras tecnologias de *Blockchain* privada, como *Indy* e *Quorum*, com propostas de valor específicas.

### ***Blockchain*** **Pública**

- ***Ethereum***  
  * Inovações como *rollups* de conhecimento zero e *rollups* otimistas aumentam a escalabilidade.

- ***Bitcoin***  
  * Principalmente utilizado como camada de liquidação descentralizada e segura.

- **Outras**  
  * Outras tecnologias de *Blockchain* pública, focadas em interoperabilidade e escalabilidade, são: *Cardano* e *Litecoin*.

## **Evolução da Internet e a Chegada da Web3**

- A Web3 é apenas uma evolução contínua da Internet que começou na década de 1990 (**Web 1.0**), como uma experiência de somente leitura, ***GeoCities*** é um bom exemplo da experiência daquela época;

- Com a **Web 2.0**, a Internet evoluiu para um modelo interativo/dinâmico, o qual permitia uma experiência de leitura e escrita;

- Exemplo: redes sociais como ***Facebook*** (atualmente ***Meta***) e ***Twitter***;

- Sua desvantagem era a centralização do controle de dados privados e da criação de valor na internet;

- Atualmente estamos na **Web 3.0**, uma evolução da **Web 2.0** com um modelo colaborativo, onde criadores de conteúdo, consumidores e construtores compartilham o controle de dados e o valor gerado;

- O foco da Web 3.0 está em redes descentralizadas, através da tecnologia emergente *Blockchain*.

## **Adaptação Corporativa e Desafios de Adoção**

- Embora toda a inovação que há atualmente seja impulsionada por *Blockchains* públicas, à medida que as empresas adotam as tecnologias Web3 em grande escala, elas precisam equilibrar o uso de *Blockchains* públicas com a necessidade de conformidade e segurança;

- Muitas vezes utilizando *Blockchains* privadas para partes mais sensíveis de suas operações, garantindo assim os benefícios da Web3 enquanto cumprem com regulamentações e protegem dados críticos;

- Por exemplo: *Blockchains* privadas e públicas sendo utilizadas em conjunto para cumprir requisitos empresariais e de **ESG (*Environmental, Social and Governance*)**.

### **Exemplo de Aplicação em Cadeia de Suprimentos**

- Uma empresa de tênis, utiliza ***Blockchain*** **privada** **para gerenciar sua cadeia de suprimentos** de forma eficiente e utiliza ***Blockchain pública*** e **NFTs** **para oferecer aos consumidores a verificação da sustentabilidade dos produtos e experiências digitais** (como eventos exclusivos ou skins digitais no metaverso);

- E com o uso de identidades descentralizadas para proteger a privacidade dos indivíduos e permitir, ao mesmo tempo, a identificação segura quando necessário.

## **AWS e Suporte à Construção de Aplicações Web3**

### **Serviços da AWS para Web3**

- ***Amazon Managed Blockchain***  
  * Serviços gerenciados para *Blockchains* públicas (como o *Ethereum*) e privadas (como o *Hyperledger Fabric*);

- **Casos de Uso de Clientes da AWS**  
  * Empresas utilizam EC2 para computação, S3 para armazenamento de arquivos grandes (como mídias associadas a NFTs) e serviços como *API Gateway* para criar e escalar APIs seguras;

  * Em questão de segurança: utilização do **AWS KMS** (*Key Management Service*) e *Nitro Enclaves* para proteger chaves privadas de criptomoedas e controlar o acesso a contratos inteligentes.

- **Fusão de dados *on-chain* e *off-chain***  
  * Serviços de dados da AWS permitem a fusão de informações da *Blockchain* com dados fora dela, para gerar insights de negócios e automatizar processos.

## ***Blockchain*** **e Inovação na *CJ Corporation***

### **Visão Geral da *CJ Corporation***

- A *CJ Corporation* é uma empresa diversificada em diversos setores;

- **Setores de Atuação**  
  * Serviços de Alimentação;  
  * Bioindústria;  
  * Logística e Varejo;  
  * Entretenimento e Cultura.

- Um exemplo de sucesso é o filme “**Parasita**” (vencedor do Óscar 2020), apoiado pelo braço de entretenimento *CJ ENM*;

- Pioneiros na difusão da ***K-culture*** (cultura coreana) e do gênero **K-Pop**, com eventos como **KCON** e ***MNET Asian Music Awards***;

### **Inovações com *Blockchain* no Grupo CJ**

- ***SMART HACCP***  
  * Sistema para evitar manipulação de dados em relatórios de controle de qualidade na indústria alimentícia por meio da utilização de *Blockchain*.

- **Gestão de Direitos Autorais de Músicas (BGM)**  
  * *Blockchain* usada para melhorar a transparência no pagamento de direitos autorais, reduzindo erros de pagamento excessivo aos detentores de direitos.

- **Chain One (Cadeia de Suprimentos)**  
  * Solução desenvolvida para gerenciar cadeias de fornecimento de medicamentos, garantindo integridade de dados como temperatura e qualidade durante o transporte.

## **Uso da Tecnologia *Blockchain* AWS na Cadeia de Suprimentos da *CJ Corporation***

### **Desafios da Cadeia de Suprimentos Farmacêutica Durante a Pandemia de COVID-19** 

- Aumento da demanda por medicamentos durante a pandemia, exigindo maior regulamentação no transporte e na qualidade dos produtos;

- Falta de padronização de dados entre diferentes *players* da cadeia (de pequenas a grandes empresas farmacêuticas).

### **Solução e Benefícios com o Uso de *Blockchain***

- **Padronização de Dados**  
  * Melhoria na transparência e eficiência ao padronizar os dados compartilhados na cadeia de suprimentos.

- **Monitoramento em Tempo Real**  
  * Exemplo de monitoramento de temperatura de vacinas e outros produtos sensíveis, com alertas automáticos em caso de desvios.

- **Automação e Resolução Rápida de Problemas**  
  * A tecnologia *Blockchain* permite ações imediatas para problemas identificados (por exemplo: deterioração de produtos devido a variações de temperatura fora do padrão).

## **AWS como Parceira da *CJ Corporation* na Utilização de *Blockchain***

Razões para a escolha da AWS

- **Facilidade de Uso**  
  * A implementação do ***Hyperledger Fabric*** com **AWS** simplifica a configuração e gestão de redes privadas de *Blockchain*.

- **Segurança Robusta**  
  * ***Key Management Service*** (**KMS**) para gerenciamento seguro de chaves e EC2 para escalabilidade automatizada.

- **Serviços Integrados**  
  * Soluções como ***Quantum Ledger Database*** (**QLDB**) para integridade dos dados e *Fargate* para gerenciar servidores sem a necessidade de configuração manual.

## **Expansão e Próximos Passos**

- A *CJ Corporation* se mostra empolgada em continuar sua jornada com a AWS, explorando novas possibilidades de uso de *Blockchain* para otimizar suas operações e expandir seu impacto em outros setores;

- Os planos futuros da *CJ Corporation* com *Blockchain* envolvem a expansão para outras indústrias, como produtos de luxo e alimentos;

- E a colaboração com agências governamentais para criar novos padrões regulatórios na cadeia de suprimentos farmacêutica.

## **Introdução à *Toyota Connected***

- Fundada em 2016, como aceleradora de inovação em software;

- O **objetivo principal** é o desenvolvimento de serviços conectados para oferecer um suporte global à Toyota;

- Tendo como **foco principal**:  
  * **Desenvolvimento de Software**;  
  * ***Data Science*** **(Ciência de Dados)**;  
  * ***Data Engineering*** **(Engenharia de Dados)**;  
  * ***Machine Learning*** **(Aprendizado de Máquina)**;  
  * **Inteligência Artificial**.

- **Serviços Desenvolvidos** focados em mobilidade, conveniência e segurança;

- Com relação à **natureza da empresa**, em suma, trata-se de uma empresa de tecnologia com uma equipe predominantemente técnica.

## **Motivação da *Toyota Connected* para Explorar a Web3**

- **Oportunidade** de captar um novo público e criar um maior engajamento com os clientes;

- **Adoção crescente** das tecnologias da Web3, logo a *Toyota Connected* viu uma oportunidade de usar isso para se conectar emocionalmente com seus clientes;

- Enquanto outras empresas focaram em “*airdrops*” e em torno dos NFTs convencionais, a Toyota Connected viu uma oportunidade diferente e utilizou assim uma **outra abordagem no uso de NFTs**, mais focada em fornecer utilidade e criar uma conexão emocional com os clientes, especialmente com base nas memórias ligadas aos seus veículos.

## **Aplicação da Tecnologia NFT no *Lexus Performance Driving School***

- O programa permite que os participantes dirijam veículos *Lexus*, como *Lexus RCF*, *Lexus IS 500 F-Sport Performance* e *Lexus LC*, em pistas icônicas como *Road America*, *Laguna Seca* e *Indianapolis Motor Speedway*;

- Os participantes experimentam adrenalina e velocidade, recebendo certificados em papel, ao final do programa;

- A equipe então **identificou uma oportunidade**: os certificados em papel poderiam ser transformados em uma experiência mais memorável e digital, usando NFTs para capturar as emoções e as lembranças dos participantes;

- Uma das maneiras encontradas para “tornar o intangível (memórias e emoções) em algo tangível”, foi com a utilização dos dados gerados pelos carros durante o evento, como velocidade, força G e pressão do pedal de freio, como elementos incorporados aos NFTs.

## **Desenvolvimento da Plataforma de NFTs**

- **Em parceria com a AWS**, foram utilizadas ferramentas como *AWS Lambda*, *Step Functions* e *Cognito*, para criar uma plataforma de “mintagem” (processo de registrar um ativo digital, como um NFT, em uma *Blockchain*) de NFTs;

- Dentre os **desafios técnicos**, estavam a captura de dados específicos dos veículos, como o motorista, o carro utilizado e o timestamp, e armazenagem em um *bucket* S3;

- Como também a **rotatividade rápida de carros**, em alguns casos, a troca entre os motoristas e veículos era menor que dois minutos;

- Também foi feita uma **integração de mídia**, por meio de combinação de imagens pré-gravadas com filmagens ao vivo do evento, além de ativos 3D para criar os NFTs personalizados;

- Com uma meta de **entrega rápida**: entregar os NFTs aos participantes dentro de 24 horas após o evento, e sendo cumprida.

## **Experiência do Cliente na “Mintagem” de NFTs**

- O processo foi **simplificado para facilitar o acesso dos participantes**, muitos dos quais não eram familiarizados com a Web3;

- O **método de acesso** se deu por e-mails que foram enviados aos participantes com um link para reivindicar o NFT;

- Verificação por e-mail, criação de senha e *Multi-factor Authentication* (MFA, Autenticação Multifator) foram implementados para garantir a segurança.

### **O processo de “Mintagem”**

- O NFT só seria registrado na *Blockchain* pública (*Polygon*) após o participante clicar no botão de “reivindicar”, garantindo controle total ao usuário;

-  Carteiras Web3 foram criadas automaticamente para os usuários, eliminando a necessidade de conhecimento prévio sobre criptomoedas.

## **Impacto do Programa e Resultados**

- **Engajamento dos Participantes**:  
  * De acordo com as pesquisas realizadas pós-evento: 100% dos participantes ficaram “empolgados” ou “muito empolgados” em receber o NFT;

  * No início, poucos demonstraram interesse em NFTs, mas isso mudou quando viram o que receberiam;

  * Com relação às **taxas de adesão**:  
    * 80% dos 130 participantes registraram interesse em obter o NFT;

    * 50% completaram o processo de “mintagem”;

    * 10% transferiram o NFT para as suas próprias carteiras compatíveis com *Polygon*.

  * **Público surpreendente**: um dos primeiros a reivindicar o NFT foi um homem de quase 80 anos, demonstrando o sucesso do projeto em atrair um público diversificado.

## **Aprendizados e Desafios**

### **Desafio de Talento**

- Encontrar desenvolvedores com experiência em Web3 e combiná-los com as equipes internas da Toyota Connected foi um grande desafio;

- A empresa conseguiu combinar o conhecimento interno com novos talentos de Web3 para então formar uma equipe de alto desempenho.

### **Reação do Público aos NFTs**

- A marca NFT ainda enfrenta ceticismo por parte do público em geral, muitas vezes associada a fraudes;

- Focar no valor prático e na experiência oferecida foi fundamental para vencer essa barreira.

### **Problemas Técnicos e Operacionais**

- A equipe enfrentou desafios com tempo de resposta e dependências técnicas, como problemas com *web hooks* e a necessidade de criar serviços complementares para garantir uma experiência fluida.

### **Navegando no Ruído da Indústria**

- A *Toyota Connected* optou por não seguir a tendência de criar “hype” em torno de NFTs, como o uso de servidores Discord, preferindo focar na utilidade e na experiência real dos clientes.

## **Visão de Futuro e Próximos Passos**

- A *Toyota Connected* pretende expandir o uso de NFTs para além do automobilismo, incorporando-os a lançamentos de produtos de luxo, experiências sustentáveis e outras interações com os clientes;

- A portabilidade dos NFTs oferece oportunidades de integração com outros setores, como jogos e atividades ao ar livre;

- Exemplos incluem usar NFTs em títulos de jogos ou conectar os proprietários de veículos a marcas que oferecem acessórios específicos para *off-road*.

### **Mensagem Final**

- A *Toyota Connected* está comprometida em continuar explorando maneiras inovadoras de engajar seus clientes e entusiasmada com as possibilidades futuras;

- A empresa também acredita que NFTs podem ser uma ponte para experiências e oportunidades únicas, tanto no mundo físico quanto no digital.