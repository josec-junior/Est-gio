# **Fundamentos de Segurança da Informação**

- De acordo com o *National Institute of Standards and Technology* (NIST) a segurança da informação é a proteção de informações e sistemas de informação contra o **acesso**, o **uso**, a **divulgação**, a **interrupção**, a **modificação** ou a **destruição**, **não autorizados**, a fim de fornecer **confidencialidade**, **integridade** e **disponibilidade**.

## **Pilares da Segurança da Informação**

- A tríade dos pilares de segurança da informação é o conjunto de tecnologias, processos e políticas que tem como finalidade manter as informações **confidenciais**, **íntegras** e **disponíveis**;

- A segurança da informação tem o papel de proteger os dados, agregando valor e contribuindo para o sucesso do negócio.

### **Confidencialidade**

- Pilar responsável por proteger a informação de acessos não autorizados, evitando situações de ataques por acesso indevido;

- O objetivo é controlar o acesso por múltiplos fatores: autenticação e criptografias;

- Uma rotina com autenticação funciona da seguinte forma:  
  * Especificar requisitos mínimos para uma senha segura;  
  * Autenticação multifator;  
  * Verificação de senha fraca;  
  * Identificador e gerenciador de sessões.

### **Integridade**

- Este pilar deve ser atendido para manter as características originais dos dados, conforme sua criação;

- Controles para impedir a alteração não autorizada devem ser pensados e implementados;

- Dentre as técnicas de integridade estão:  
  * Validação de dados, como hashes;  
  * Verificação de duplicidade;  
  * Tratamento de dados de entrada, como caracteres especiais e comandos.

### **Disponibilidade**

- Os dados devem estar disponíveis para o que for necessário, isso demanda a estabilidade e acesso permanente ao ambiente e aos sistemas;

- São controles existentes para garantir o acesso e uso adequado das informações:  
  * Recursos de redundância, como backup de dados e balanceamento de carga;  
  * Infraestrutura em nuvem;  
  * Gestão de vulnerabilidades.

## **Política de Segurança da Informação (PSI) e Política de Classificação da Informação (PCI)**

- A Compass, assim como todas as demais empresas do grupo, seguem atualmente as orientações de Política de Segurança da Informação (PSI) publicada pelo Grupo UOL, que diz: “a Política de Segurança da Informação e Segurança Cibernética pretende:  
1. Descrever as melhores práticas de Segurança da Informação e Segurança Cibernética quanto à confidencialidade, integridade e disponibilidade de informações;  
2. Estabelecer diretrizes para todos os usuários;  
3. Minimizar os riscos de Segurança da Informação.”

- Para definir o controle mais adequado é necessário conhecer o tipo de informação, a sua criticidade e o público;

- O melhor guia é a Política de Classificação da Informação (PCI);

- “Esta política descreve o processo de classificação da informação, caracterizado pela definição do nível de sensibilidade e os grupos de acesso à informação, visando assegurar que esta receba um nível adequado de proteção, conforme seu valor, sensibilidade e criticidade para a organização”.

## **Classificação da Informação**

-  A Classificação da Informação tem o objetivo de assegurar o nível adequado de proteção para a informação e tem como base o seu valor, criticidade para a organização e requisitos legais;

- Ela surgiu como forma de mitigar o vazamento de informações ou o acesso indevido por falta de conhecimento do tipo de dados que se encontra disponível;

- A Classificação da Informação serve para aplicar a devida proteção das informações e reduzir a probabilidade de ocorrência de incidentes;

- O vazamento de informações, por exemplo, pode ocasionar impactos financeiros, regulatórios e reputacionais, trazendo sanções e prejuízos à Compass, seus clientes, parceiros e profissionais.

## **Níveis de Classificação**

- Conforme descrito na Política de Classificação da Informação (PCI) da Compass, a Compass possui quatro classificações: **Públicas**, **Internas**, **Restritas** e **Confidenciais**.

### **Confidencial**

- São informações altamente sigilosas e que não podem ser divulgadas para evitar danos à empresa, terceiros, funcionários e clientes;

- Seu uso requer medidas de controle e proteção rigorosos contra acessos, cópias, reproduções ou divulgações não autorizadas;

- Devido à sensibilidade dessas informações, várias restrições de uso são aplicadas e o destinatário consegue apenas consultar o documento;

- Sob esta classificação, um possível vazamento de dados certamente causaria grandes danos à **empresa**;

- Exemplos de informações confidenciais:  
  * Ata de reunião de um assunto pertinente ao comitê executivo;  
  * Base de dados de cartões de crédito;  
  * Dados pessoais de clientes, colaboradores, fornecedores e demais entidades;  
  * Desenvolvimento de novos produtos ou segredos industriais;  
  * Informações protegidas por regulamentações de proteção de dados, por exemplo: Lei Geral de Proteção dos Dados (LGPD);  
  * Informações de transferências financeiras;  
  * Modelo de negócios de um novo produto;  
  * Todos os tipos de senha para acesso à sistema, rede ou estações de trabalho;  
  * Código fonte;  
  * Incidentes de segurança.

### **Restrita**

- São informações exclusivas de alguns profissionais e/ou determinadas áreas;

- Significa que nem todos têm acesso à elas, pois os dados desta categoria são disponibilizados apenas aos destinatários nos quais você delega confiança para tratar do assunto;

- Sob esta classificação, um possível vazamento de dados pode causar um impacto significativo **à empresa**, **seus profissionais**, **seus parceiros ou seus clientes**;

- Exemplos de informações restritas:  
  * Código fonte;  
  * Dados ou informações referentes às políticas comerciais;  
  * Divulgação de metas e resultados institucionais;  
  * E-mail de feedback do gestor;  
  * Informações sobre produtos, serviços e projetos;  
  * Propostas comerciais ou de serviços;  
  * Relatório de metas de uma determinada área;  
  * Resultado de auditorias;  
  * Incidentes de segurança.

### **Interna**

- São informações que podem ser divulgadas para os profissionais, estagiários, prestadores de serviços da empresa e precisam de cuidados para evitar a divulgação ao público externo;

- Exemplos de informações internas:  
  * Comunicados;  
  * Políticas e normas corporativas;  
  * Procedimentos operacionais e técnicos;  
  * Relação de endereços de e-mail internos;  
  * Informações disponibilizadas na Intranet.

### **Pública**

- São informações que podem ser divulgadas sem restrições, para o público em geral incluindo clientes, fornecedores, imprensa, concorrentes, entre outros;

- As informações públicas são aqueles dados que podem ser divulgados sem oferecer risco algum à empresa, seus colaboradores e clientes.

## **Engenharia Social**

- Engenharia Social é a habilidade de conseguir acesso à informações ou áreas importantes de algo ou alguém através de habilidades de persuasão;

- O atacante se aproveita da falta de conhecimento, da boa vontade e simpatia da sua vítima para convencê-la a passar informações ou tomar ações de forma que lhe pareçam legítimas;

- O ser humano confia e coopera por natureza, qualquer pessoa pode ser induzida a compartilhar informações, seja por capricho, sentir-se útil, curiosidade, ambição, medo, compaixão, inocência, toda característica pode ser explorada com a abordagem correta;

- Os investimentos para proteção das informações estão cada vez maiores e as tecnologias mais avançadas, com isso, os fraudadores atacam o fator humano, a parte do processo de controles de segurança que tem menos atenção das empresas.

## **Táticas de Abordagens**

- As abordagens variam de acordo com a exposição do atacante, sendo as mais comuns: ***Baiting***, ***Phishing*** e ***Dumpster Diving***.

### ***Baiting***

- Uma isca física ou digital como um *pendrive* ou *download* de um filme, podem trazer um *malware* para o computador da vítima, ao inserir o *pendrive* ou baixar e executar um arquivo, o *malware* oculto ganha acesso ao computador.

### ***Phishing***

- O mais famoso, mas, também mais eficiente;

- O atacante cria conteúdo enganoso muito próximo de algo legítimo e confiável, com o objetivo de obter credenciais ou instalar um *malware*;

- É comum se utilizar do e-mail, mas também é comum por SMS (***Smishing***) ou ligações de voz (***Vishing***).

### ***Dumpster Diving***

- Uma das abordagens menos óbvias, entretanto, caso as empresas não tenham cuidados com o descarte de informações, o atacante pode encontrar relatórios inteiros, discos removíveis, entre outros tipos de mídia com informações de todos os níveis de classificação.

## **Dicas de Prevenção**

- Sempre desconfie e leia novamente antes de tomar alguma ação;

- Não baixe arquivos e anexos em e-mails suspeitos;

- Não responda nem interaja com mensagens de textos suspeitas;

- Valide os links e o remetente dos e-mails;

- Descarte corretamente documentos e equipamentos;

- Adote a prática “mesa e tela limpas”, bloqueando o computador quando estiver ausente e deixando apenas o necessário em seu ambiente de trabalho.

## **Boas Práticas e Diretrizes**

- As principais boas práticas e diretrizes incluem:  

  * Compartilhamento de acesso responsável;  
  * Armazenamento adequado;  
  * Cuidados com Softwares e *Malwares*;  
  * Utilização de senhas seguras;  
  * Uso apropriado da Internet;  
  * Utilização de *Multi-Factor Authenticator* (MFA) e de aplicativos como o *Microsoft Authenticator*;  
  * Constante atualização de Softwares;  
  * Tomar providências com relação a Incidentes de Seguranças;  
  * Cuidados na utilização de Redes Públicas e Domésticas.

### **Compartilhamento de Acesso**

- As credenciais de acesso de qualquer sistema constituem a identificação do usuário, isto é, se ele é autorizado a acessar e trabalhar com aquelas informações;

- As ações executadas com uma credencial são de responsabilidade do próprio profissional e todos os acessos podem ser monitorados, portanto, proteja seu login e senha.

### **Armazenamento**

- As informações devem ser armazenadas nos repositórios oficiais, onde estarão seguras com os devidos controles de proteção;

- Use os recursos da *Udemy*, do *OneDrive* e do *Sharepoint* de seu respectivo *iStudio* para armazenar suas informações.

### **Softwares e Malwares**

- Softwares maliciosos (*Malwares*) são muito comuns em programas ou arquivos baixados da internet, portanto, é necessário ter muita cautela;

- Nosso antivírus gera um alerta a todo software não autorizado e damos o devido tratamento, envolvendo os profissionais e seus gestores, mas, o ideal é que você avalie sempre a lista de softwares homologados antes de instalar algo em seu equipamento;

- Não assuma um risco sozinho, busque orientação;

- Utilizar software não homologado pode gerar riscos desnecessários às nossas informações.

### **Senha Segura**

- Suas senhas concedem o acesso ao ambiente e sistemas na Compass, como também aos clientes, por isso, é preciso seguir alguns cuidados básicos para criar uma senha forte:  

  * Evite nomes, sobrenomes, apelidos, datas de aniversário, número de celular, placa de carro;  
  * Crie senhas diferentes para cada conta, sistema ou site que precisar;  
  * Troque suas senhas com frequência;  
  * Use um aplicativo de gerenciamento de senhas;  
  * Sempre que disponível, utilize um segundo fator de autenticação (MFA);  
  * Reporte ao time **InfoSec** situações suspeitas que pedem suas informações;  
  * Sempre que possível, use letras maiúsculas e minúsculas, números e caracteres especiais.

### **Uso da Internet**

- O conteúdo acessado na Internet e o uso do e-mail corporativo deve respeitar todas as diretrizes e normas de segurança e privacidade, publicadas e divulgadas nas políticas da Compass;

- Com a disseminação de ferramentas de comunicação instantânea, o uso destas para tratar assuntos profissionais se tornou cada vez mais comum;

- Evite-os para tratar assuntos sensíveis e compartilhar arquivos.

- Mantenha o navegador de sua preferência sempre atualizado;

- Não navegue pela *Deep Web* e/ou *Dark Web*, pois isso traz altos riscos de vazamento de informação, sequestro de dados e conteúdo ilícito.

### ***Multi-Factor Authenticator*** **(MFA)** 

- MFA é um controle de segurança que demanda dois ou mais elementos de autenticação para identificar um usuário, a fim de dificultar acessos não autorizados;

- Existem diversos tipos de autenticação e o mais utilizados são:  
  * “**O que sei**”: é exigido algo conhecido, como login, senha ou resposta a uma pergunta secreta;  
  * “**O que tenho**”: necessário algo físico como um token, um cartão inteligente ou um aplicativo em dispositivo móvel para obter a informação, geralmente randômica, para autenticação;  
  * “**Quem sou**”: utiliza-se características físicas do ser humano, como a impressão digital, reconhecimento de voz ou facial, leitura de retina, este talvez seja um dos controles mais populares e é muito utilizado para a proteção de identidade digital nas redes sociais.

### ***Microsoft Authenticator***

- Aqui na Compass, é utilizado para autenticação ao e-mail corporativo, o aplicativo *Microsoft Authenticator*, é preciso instalar em um dispositivo móvel para conseguir gerar o token de verificação;

- A cada 14 dias, é solicitado um novo código para acessar os aplicativos que possuem o MFA, com este código, o colaborador consegue entrar na sua conta;

- Ao trocar de dispositivo móvel, antes de desativar o cadastro do MFA no dispositivo móvel antigo, é necessário ainda utilizá-lo para realizar o cadastro no novo dispositivo.

### **Atualização de Software**

- Sempre mantenha os seus softwares e sistema operacional atualizados;

- Além das correções e proteção contra novas vulnerabilidades identificadas pelos *vendors*, você tem ganhos em desempenho, compatibilidade, estabilidade, além de evitar interrupções, aproveitar novos recursos e funcionalidades.

### **Incidentes de Segurança**

- Incidente de Segurança é um evento de segurança ou um conjunto deles, que podem impactar a **disponibilidade**, **integridade** e **confidencialidade** de um ativo de informação, assim como qualquer violação da Política de Segurança da Informação (PSI);

- Alguns exemplos de Incidentes de Segurança são:  
  * Ferramenta não autorizada instalada;  
  * Vírus e outros códigos maliciosos;  
  * Tentativas não autorizadas de acesso;  
  * Compartilhamento de credenciais.

- Ao você relatar um incidente que foi alvo ou presenciou, abre o caminho para que o time **InfoSec** analise e envolva quem for necessário para corrigir e reduzir a chance de ocorrência novamente;

- Por isso, caso você identifique um incidente de segurança, relate imediatamente, seja de forma identificada ou anônima, ao time **InfoSec**.

### **Redes Wi-Fi**

- Inúmeras vezes colocamos em risco nossas informações, como senhas, histórico de navegação, e-mails, mensagens, dados e arquivos, ao utilizarmos um hotspot desconhecido, gratuito ou com nomes muito convencionais;

- É possível que alguém mal intencionado esteja bisbilhotando todos os pacotes que trafegam naquela rede aberta.

### **Dicas Valiosas para Redes Wi-Fi Públicas e Domésticas**

- Em redes públicas:  
  * Evite se conectar a redes abertas;  
  * Utilize uma VPN confiável, assim seus dados são criptografados em trânsito e protege a privacidade caso os pacotes sejam interceptados;  
  * Desative a opção de conexão automática nas redes Wi-Fi públicas, assim você consegue escolher onde se conectar;  
  * Desabilite o compartilhamento de arquivos e impressoras, isso reduz riscos de acesso não autorizado;  
  * Não instale aplicativos que prometem quebrar senhas ou descobri-las para conectar a redes Wi-Fi protegidas.

- Em sua rede doméstica:  
  * Configure uma senha forte para o seu roteador, troque-a periodicamente e utilize os padrões **WPA2** ou **WPA3**;  
  * Mantenha o firmware atualizado, aqui a atualização automática pode te ajudar muito;  
  * Mude os padrões de fábrica como o nome da sua rede (**SSID**) e as credenciais de administrador do roteador;  
  * Desabilite o acesso remoto ao roteador para manutenção;  
  * Fique atento aos sites onde vai inserir informações confidenciais, confirme que utilizam conexões seguras (**https**, procure pelo cadeado na barra de endereços do navegador).

### ***Have I Been Pwned?***

- Verifique se o seu e-mail está na lista dos vazamentos de dados mais conhecidos, pelo site do [Have I Been Pwned](https://haveibeenpwned.com/).

## **Segurança em Inteligência Artificial (IA) Generativa**

- Inteligência Artificial Generativa é uma subárea da Inteligência Artificial que se concentra na criação de novos conteúdos, dados ou informações como texto, imagens, vídeos, música ou código, a partir de um conjunto de entradas existentes;

- Os algoritmos de IA aprendem com os dados fornecidos e são capazes de gerar saídas semelhantes, mas não idênticas, com base no conhecimento adquirido durante o treinamento.

### **Ambiente e Utilização de Ferramentas de IA**

- Há diversas ferramentas gratuitas e pagas, antes de iniciar um trabalho usando-as, leia e analise todos os itens do contrato ou termo de uso;

- Saber como os dados inseridos serão usados é imprescindível para a segurança dessas informações, pois você pode involuntariamente autorizar o uso ou deixar os dados disponíveis para terceiros;

- Utilize ferramentas homologadas e licenças comerciais em ambiente corporativo, e isso não significa você mesmo comprar uma licença;

- É proibido o uso dessas ferramentas para uso pessoal, atividades ilegais, fraudulentas, danos físicos e econômicos, violação de privacidade ou que contrariam a Política de Segurança da Informação.

### **Formas de Proteger os Dados e Informações**

- Quando buscar apoio de uma IA generativa para melhorar ou agilizar seu trabalho, é fundamental lembrar de proteger as informações de clientes ou da empresa que esteja trabalhando;

- Algumas dicas para a proteção de dados e informações são:  
  * Remover dados pessoais, senhas e tokens das consultas que enviar, independentemente que sejam dados de ambiente ou desenvolvimento ou de produção;  
  * Quando possível, utilizar mascaramento de dados;  
  * Trocar qualquer dado real de clientes ou da empresa, nas consultas, como nomes próprios das empresas, comentários de código, casos reais.

### **Controles Mínimos de Segurança**

- As ferramentas de IA, sejam elas contratadas ou desenvolvidas internamente, devem atender a requisitos mínimos de segurança tais como os controles tecnológicos, gestão de acessos, monitoramento, documentação e revisão dos processos e capacitação das pessoas;

- Alguns processos da sua rotina:  
  * Homologação para validar os controles técnicos;  
  * Análise de riscos;  
  * Utilizar o *Jira* para solicitação de acesso às ferramentas de IA;  
  * Documentar no *Sharepoint* ou *Confluence* os manuais e processos para utilização das ferramentas de IA;  
  * Realizar os treinamentos obrigatórios e participar das ações de capacitação e conscientização sobre o tema.