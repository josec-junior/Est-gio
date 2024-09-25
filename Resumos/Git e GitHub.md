# **Git e GitHub**

- O Git é um sistema de controle de versão distribuído, gratuito e de código aberto;  

- O GitHub é um serviço de hospedagem de projetos/repositórios que utilizam o Git;  

- O Git armazena repositórios localmente, enquanto o GitHub faz uma sincronização com o Git, armazenando repositórios na nuvem;  

- O GitHub também permite a colaboração em projetos/repositórios.

## **Repositório**

- É um armazenamento digital centralizado que os desenvolvedores usam para gerenciar alterações no código-fonte de uma aplicação;  

- Um repositório tem recursos que permitem aos desenvolvedores rastrear facilmente as alterações de código, editar arquivos simultaneamente, e colaborarem com eficiência no mesmo projeto, em qualquer local;  

- É possível inicializar um repositório localmente através do comando `git init`.  

- Após inicializar o repositório, é possível verificar o estado do diretório de trabalho utilizando o comando `git status`;

## **Tracking**

- Quando inicializado o repositório, os arquivos do diretório estão no estado de *untracked,* ou seja, se houver alterações nos arquivos, o git não irá tirar o *snapshot* (fazer uma cópia e criar uma nova versão);

- *Tracking* refere-se ao relacionamento entre um arquivo ou branch no repositório local e sua contraparte no repositório remoto;  
- É possível fazer o _tracking_ por arquivo ou para todos os arquivos do diretório, através do comando `git add`;  

- Para adicionar um ou mais arquivos, utiliza-se o comando `git add <arquivo>`, e para adicionar todos os arquivos de uma vez, pode utilizar o comando `git add –-all` ou `git add .`;  

- Os arquivos que forem adicionados, passam a ser *tracked*, isso significa que o Git começará a monitorar as alterações nesses arquivos, permitindo que você veja as alterações que foram feitas;  

- Arquivos adicionados com o `git add` estão no estado *staged*, ou seja, preparados para serem “commitados”;  

- Para mudar esses arquivos para *untracked*, basta utilizar o comando `git rm --cached <arquivo>`;

## **Commit**

- Para criar uma versão ou *snapshot* dos arquivos de status *staged*, utiliza-se o comando `git commit -m "<mensagem>"`;  

- É recomendado adicionar uma mensagem ao commit descrevendo as alterações que foram feitas no projeto, naquele commit;  

- Cada commit representa um *snapshot* do estado do projeto em determinado momento, contendo as alterações feitas desde o último commit;  

- Com o comando `git diff`, é possível visualizar as diferenças entre versões de arquivos no repositório, ajudando a comparar alterações entre o estado atual do projeto e estados anteriores;  

- O comando `git diff` é muito útil para visualizar o que foi modificado antes de fazer um commit ou para revisar alterações entre diferentes branches ou commits;  
- No Git, o ciclo de vida de um arquivo passa por três estágios principais:  
1. *Working Directory*;  
2. *Staging Area*;  
3. *Commit*.

### ***Working Directory***

- O *Working Directory* é o estado atual do seu projeto, ou seja, os arquivos que que estão sendo editados no momento, aqui são feitas todas as alterações no código, adição de novos arquivos e modificação ou exclusão de arquivos existentes;  

- Arquivos no *Working Directory* podem estar em três estados:  
  * ***Untracked*** \- arquivos que foram criados, mas que o Git ainda não está monitorando;  

  * ***Modified*** \- arquivos que foram alterados, mas ainda não foram adicionados à área de staging;  
  
  * ***Unmodified*** \- arquivos que não sofreram alterações desde o último commit.

### ***Staging Area***

- É uma área intermediária onde são preparadas as mudanças que serão incluídas no próximo commit;  

- Quando são feitas alterações em arquivos no *Working Directory*, e você deseja que essas mudanças sejam salvas no próximo commit, você precisa adicionar essas alterações à *Staging Area*, utilizando o comando `git add`;  

- A *Staging Area* permite que você escolha exatamente quais mudanças serão incluídas no próximo commit, fornecendo um controle mais fino sobre o que é registrado no histórico do repositório;  

- É possível pular o estágio de *Staging Area* utilizando comando `git commit -a -m "<mensagem>"`, mas é recomendado que isso só seja feito quando tiver certeza que pode ser feito o commit das alterações feitas no projeto.

### ***Commit***

- Um commit é um *snapshot* de todas as mudanças que estão na *Staging Area*, naquele momento;

- Quando você faz um commit, essas mudanças são registradas permanentemente no histórico do repositório;  

- Cada commit tem uma mensagem descritiva e um identificador único (SHA) que permite rastrear e reverter para aquele ponto no tempo, se necessário;  

- No Git, o commit também está associado ao repositório local, e só após um `git push`, as mudanças são movidas para o repositório remoto.

## **Renomeando, movendo, removendo e restaurando arquivos** 

- **Para remover um arquivo do diretório de trabalho e do controle de versão**, utiliza-se o comando `git rm <arquivo>`, após rodar esse comando, o arquivo será excluído fisicamente do seu projeto e essa remoção será registrada no próximo commit;  

- **Para remover um arquivo do Git, mas mantê-lo no diretório local**, usa-se o comando `git rm --cached <arquivo>`, isso é útil quando você quer parar de rastrear um arquivo, mas não deseja deletá-lo do sistema de arquivos;  

- **Se você fez alterações em um arquivo, mas ainda não o “commitou”** e deseja desfazê-las, você pode usar o comando `git restore <arquivo>` para restaurar o arquivo para o seu estado no último commit;  

- **Se você já adicionou um arquivo modificado à *Staging Area* com git add**, mas quer remover essas mudanças da área de *staging* (fazer com que ele volte a ser *unstaged*), você pode usar o comando `git restore --staged <arquivo>`;  

- Para renomear arquivos, você pode usar o comando `git mv <nome atual do arquivo> <novo nome do arquivo>`;  

- O comando `git mv` também pode ser usado para mover arquivos para outros diretórios, isso é útil se você está reorganizando a estrutura de diretórios do seu projeto, basta utilizar o comando `git mv <arquivo> <novo diretório/arquivo>`.

## **Alterando commits com Amend e acessando histórico de commits**

- O comando `git commit \--amend` no Git é usado para modificar o último commit, ele permite que você edite tanto o conteúdo (arquivos e alterações) quanto a mensagem do commit mais recente, sem criar um novo commit;  

- Isso é útil quando você comete um erro no commit anterior, como esquecer de incluir um arquivo ou deseja melhorar a mensagem do commit;  

- Se você quer **apenas alterar a mensagem do último commit**, sem mudar os arquivos, pode usar o comando da seguinte forma: `git commit --amend -m "<nova mensagem>`";  

- Se você já fez um commit, mas percebeu que esqueceu de incluir alguma modificação ou arquivo e deseja **adicionar mudanças ao último commit**, pode corrigir isso adicionando o arquivo e fazendo o amend:  
1. Faça as alterações desejadas;  

2. Adicione esses arquivos à área de staging com o comando `git add <arquivo>`;  

3. Use o `git commit –amend` para incluir essas mudanças no commit anterior;  

4. Isso vai abrir o editor de texto padrão (ou você pode adicionar `-m` ao comando anterior para uma mensagem de commit direta) e permitirá que você confirme o novo estado do commit com os arquivos corrigidos.

### **Cuidados ao usar o `amend`**

- **Evite usar em commits já enviados ao repositório remoto**, se o commit já foi enviado (com `git push`), fazer um `amend` cria um novo commit com um hash diferente, o que pode causar problemas para outras pessoas que estão trabalhando no mesmo projeto;  

- **Reescreve o histórico**: O `amend` não cria um novo commit, ele sobrescreve o último, por isso, só deve ser usado quando você tem certeza de que quer modificar o último commit em vez de adicionar um novo.

### **Acessando o histórico de commits com o `git log`**

- O comando `git log` é utilizado para exibir o histórico de commits de um repositório, ele permite que você veja uma lista dos commits realizados, junto com detalhes importantes como o hash do commit, a mensagem, o autor e a data;  

- O `git log` é muito flexível, permitindo várias opções para filtrar, formatar e navegar pelo histórico de commits;  

- Por padrão, o git log exibe os commits mais recentes primeiro e inclui:  
  * O hash SHA-1 (identificador único de 40 caracteres) de cada commit;  
  * O nome e o e-mail do autor;  
  * A data do commit;  
  * A mensagem do commit.

- Algumas das opções úteis do git log são:  
  * `git log` \- Exibe o histórico completo;  
  * `git log -n <n>` \- Exibe os últimos n commits;  
  * `git log --oneline` \- Exibe o histórico de forma compacta;  
  * `git log -p` \- Mostra o diff de cada commit;  
  * `git log --author="<nome>"` \- Filtra commits por autor;  
  * `git log --since="<data>" --until="<data>"` \- Filtra commits por data;  
  * `git log -- <arquivo>` \- Filtra commits que modificaram um arquivo específico;  
  * `git log --graph` \- Exibe o histórico com um gráfico de branches.

## **Git Reset**

- O comando `git reset` no Git é uma ferramenta poderosa usada para desfazer mudanças em um repositório;  

- Ele permite que você altere o estado de commits, a área de *staging* (índice) e o diretório de trabalho (*working directory*);  

- Dependendo da opção usada com `git reset`, ele pode modificar apenas a área de *staging*, o commit mais recente ou até desfazer mudanças no diretório de trabalho;  

- O `git reset` pode ser usado de três maneiras, dependendo da “profundidade” da modificação que você deseja fazer no repositório:  
  * `--soft` \- Reseta o último commit, mantendo as mudanças no staging;  

  * `--mixed` (padrão) \- Reseta o último commit e remove as mudanças do staging, mantendo as alterações no diretório de trabalho;  

  * `--hard` \- Reseta o último commit e remove as mudanças tanto do staging quanto do diretório de trabalho (perde as alterações completamente).  

- A sintaxe do comando é a seguinte: `git reset [opção] <commit>`  
  * Onde `[opção]` pode ser `--soft`, `--mixed` ou `--hard`, quando não especificado, o Git usa `--mixed` por padrão;  
  * `<commit>` é o hash (identificador) do commit para o qual você quer voltar.

### **`git reset --soft` (Voltar um commit e manter as alterações no staging)**

- Essa opção **volta o ponteiro de commits** (HEAD) **para o commit especificado**, mas **mantém todas as mudanças na *staging area***;  

- É útil quando você quer refazer o último commit, mas mantendo as alterações preparadas para o próximo commit.

### **`git reset --mixed` (Voltar um commit e mover as alterações para o diretório de trabalho)**

- Essa opção é o comportamento padrão do git reset;  

- Ele remove o último commit e coloca as mudanças no diretório de trabalho (*working directory*), mas não as mantém no *staging*;  

- É preciso usar o `git add` novamente, se quiser fazer o commit dessas alterações.

### **`git reset --hard` (Voltar um commit e descartar todas as alterações)**

- Essa opção é a mais destrutiva, pois ela **volta o commit e remove as mudanças tanto do staging quanto do diretório de trabalho**;  

- Isso significa que as alterações feitas serão **perdidas permanentemente**, a menos que estejam salvas em outro lugar.

### **Diferença entre `git reset` e `git revert`**

- O comando `git reset` altera o histórico de commits diretamente, ele **remove commits de forma destrutiva e muda o ponteiro HEAD para um commit anterior**, potencialmente removendo as mudanças do repositório;  

- O comando `git revert` **cria um novo commit que desfaz as alterações de um commit anterior**, o histórico de commits é preservado, mas o conteúdo do commit é revertido;  

- Se o repositório já foi compartilhado (já foi feito `git push`), dê preferência ao comando `git revert` para não alterar o histórico de commits de forma destrutiva e evitar problemas com outros colaboradores.

## **Atalhos com `git alias`**

-  O comando `git alias` permite que você crie atalhos personalizados para comandos do git, tornando seu uso mais eficiente;  

- Com o `alias`, você pode definir abreviações para comandos longos ou frequentemente utilizados, o que economiza tempo ao trabalhar no terminal;  

- Os *aliases* (atalhos) são definidos no arquivo de configuração do Git (geralmente o `.gitconfig`);  

- Esses *aliases* podem ser tanto para comandos simples quanto para combinações de comandos mais complexos;  

- Para criar um *alias*, você utiliza o comando `git config --global alias.<nome do alias> "<comando>"`  
  * `--global` \- Faz com que o *alias* seja válido para todos os repositórios no sistema, se você quiser criar um *alias* apenas para o repositório atual, omita o `--global`;  
  * `<nome do alias>` \- O nome que você deseja para o atalho (por exemplo, cm para commit);  
  * `<comando>` \- O comando Git que o *alias* deve executar.

- Para verificar todos os *aliases* configurados, você pode executar o seguinte comando: `git config \--get-regexp alias`;  

- Se você quiser remover um *alias*, pode utilizar o comando `git config --global --unset alias.<nome do alias>`;  

- As vantagens de utilizar o `git alias` são:  
  * Produtividade, pois reduz a quantidade de digitação e acelera o uso de comandos longos;  
  * Personalização, ao permitir criar comandos personalizados que melhor atendem às suas necessidades;  
  * Simplicidade, pois facilita o uso do Git, especialmente para comandos que você usa com frequência ou são complicados.

## **Branch** 

- Uma branch (ramificação) no Git é uma linha independente de desenvolvimento, que permite trabalhar em diferentes funcionalidades, correções ou versões de um projeto sem alterar a linha principal de desenvolvimento;  

- As branches facilitam o trabalho colaborativo e paralelo, permitindo que os desenvolvedores trabalhem em várias funcionalidades ou correções ao mesmo tempo;  

- Quando você inicializa um repositório Git, por padrão, ele começa com uma branch principal, geralmente chamada de master ou main, essa branch contém o histórico principal do projeto;  

- Você pode criar novas branches a partir de qualquer commit, permitindo que desenvolva novas funcionalidades ou faça correções de bugs sem afetar o código da branch principal.

### **Criando uma branch**

- Uma branch é essencialmente um ponteiro para um commit específico no histórico;  

- À medida que você faz commits, o ponteiro da branch avança para o novo commit;  

- Isso cria uma “linha do tempo” de commits isolada da branch principal ou de outras branches;  

- Para criar uma nova branch, você usa o comando: `git branch <nome da branch>`;  

- Isso cria uma nova branch, mas você ainda estará na branch anterior, para começar a trabalhar na nova branch, você precisa mudar para ela usando o comando `git checkout <nome da branch>` ou o mais recente `git switch <nome da branch>`;  

- Agora você está “dentro” da nova branch e qualquer commit feito será registrado apenas nesta branch.

### **Ciclo de vida de uma branch**

- **Criação** \- Você cria uma branch para trabalhar em uma nova funcionalidade, correção de bug ou experimento, as mudanças feitas nesta branch não afetam as outras branches;  

- **Trabalho paralelo** \- Enquanto você trabalha na sua nova branch, outros desenvolvedores podem continuar a trabalhar na branch principal ou em outras branches, de forma independente;  

- **Commitar mudanças** \- Você faz commits conforme trabalha na nova funcionalidade ou correção, esses commits ficam restritos à nova branch, sem afetar as outras;  

- **Merge (união)** \- Quando a nova funcionalidade ou correção está completa e testada, você pode integrar (fazer o merge) essa branch com a branch principal, o merge junta as mudanças da branch atual com outra branch (geralmente a main ou master);  
  * Primeiro, troque para a branch onde deseja aplicar as mudanças com o `git checkout <nome da branch>` e depois faça o merge com o `git merge -m "<mensagem>" <nome da branch>`;  

- **Exclusão da branch** \- Após o merge, se a branch não for mais necessária, você pode excluí-la para manter o repositório limpo, utilizando o comando `git branch -d <nome da branch>`.

### **Vantagens do uso de branches**

- **Trabalho isolado** \- Cada branch é um ambiente isolado, onde você pode testar e desenvolver novas funcionalidades sem interferir na versão estável do projeto;  

- **Colaboração eficiente** \- Vários desenvolvedores podem trabalhar em diferentes funcionalidades simultaneamente, sem conflitos diretos;  

- **Facilidade de reversão** \- Se algo der errado em uma branch, você pode simplesmente não mesclá-la (realizar o merge) à branch principal ou descartá-la sem afetar o projeto;  

- **Controle de versões** \- Permite criar diferentes versões do projeto, como branches para desenvolvimento, produção, correções de bugs, etc.

## **Repositório Remoto com o GitHub**

- Um repositório no GitHub é um repositório remoto, o qual permite que você sincronize mudanças entre o repositório local (no seu computador) e o repositório no GitHub (na nuvem);  

- Após criado a sua conta no GitHub e feito login, clique no ícone de “+” no canto superior direito e selecione “New Repository” e então preencha os seguintes campos:  
  * **Repository name**: Nome do seu repositório (exemplo: meu-projeto);  
  * **Description** (opcional): Uma breve descrição do repositório;  
  * Escolha a visibilidade do repositório: **Public** (público) ou **Private** (privado);  
  * Selecione se deseja criar um arquivo `README.md` inicial, um arquivo `.gitignore` e escolher uma licença para o projeto.  
- Por fim, clique em **Create Repository** (Criar repositório).

- Após criar o repositório no GitHub, ele fornecerá um link remoto, use este link para conectar o seu repositório local ao remoto;  
  * Primeiro, copie a URL do seu repositório no GitHub (será algo como https://github.com/usuario/meu-projeto.git);  
  * No terminal, dentro da pasta do seu projeto, adicione o repositório remoto com o comando `git remote add origin https://github.com/usuario/meu-projeto.git`;  

- Este comando vincula o repositório local ao remoto no GitHub, o nome `origin` é um nome padrão que aponta para o repositório remoto;  

- Agora que o repositório local está vinculado ao remoto, você pode enviar seus commits para o GitHub com o comando `git push`;  

- No primeiro envio utiliza-se o comando `git push -u origin main`;  
  * O `-u` indica que você quer configurar o `origin` como o destino padrão para os futuros pushes;  
  * `main` (ou `master`, dependendo da sua configuração) é o nome da branch principal do seu projeto.  

- Após isso, o GitHub terá uma cópia do seu repositório local e todos os arquivos estarão disponíveis online.

### **Branches remotas**

- Branches também podem existir em repositórios remotos, como o GitHub;  

- Você pode criar branches localmente e enviá-las para o servidor remoto, ou criar branches diretamente no servidor;  

- Para criar e enviar uma branch para o repositório remoto, utiliza-se o comando `git push -u origin <nome da branch>`;  

- Para listar as branches que existem no repositório remoto, utiliza-se o comando `git branch -r`;  

- Para excluir uma branch remota, utiliza-se o comando `git push origin --delete <nome da branch>`.

### ***Issue***

- No GitHub, um *Issue* é uma ferramenta usada para rastrear e gerenciar tarefas, bugs, ideias ou qualquer outro tipo de trabalho relacionado ao projeto;  

- Ele serve como uma espécie de fórum de discussão, onde desenvolvedores e colaboradores podem reportar problemas, sugerir melhorias, discutir novas funcionalidades ou compartilhar ideias;  

- Um *Issue* no GitHub funciona da seguinte forma:  
  * **Relatar Problemas ou Bugs**: Quando alguém encontra um erro no projeto (por exemplo, um bug no código), pode abrir um *Issue* descrevendo o problema, outros membros da equipe podem então discutir a melhor forma de resolvê-lo;  

  * **Planejar Novas Funcionalidades**: Você pode criar um *Issue* para planejar e discutir o desenvolvimento de uma nova funcionalidade, isso permite que todos os membros da equipe compartilhem suas ideias e colaborem antes de começar a codificar;  

  * **Gerenciar Tarefas**: *Issues* podem ser usados para organizar e acompanhar tarefas dentro do projeto, atribuir *Issues* a diferentes colaboradores ajuda a distribuir o trabalho de maneira clara;  

  * **Documentação e Discussão**: Cada *Issue* tem uma seção de comentários, onde desenvolvedores e colaboradores podem discutir o problema, compartilhar soluções e adicionar atualizações.

### **Principais elementos de um *Issue***

- **Título**: Um título curto e descritivo do problema ou tarefa;  

- **Descrição**: Um campo onde você pode detalhar o problema, a funcionalidade ou a tarefa, podendo incluir informações como:  
  * Passos para reproduzir o problema;  
  * Descrição de como a funcionalidade deve funcionar;  
  * Detalhes técnicos, capturas de tela ou código de exemplo.  

- **Comentários**: Outros usuários podem deixar comentários no *Issue*, discutir soluções e compartilhar ideias;  

- **Atribuições**: Você pode atribuir o *Issue* a uma pessoa ou equipe, indicando quem será o responsável por resolver o problema ou implementar a funcionalidade;  

- ***Labels*** **(etiquetas)**: Categorias que ajudam a organizar os *Issues*, por exemplo, você pode adicionar labels como “bug”, “feature request”, “documentation”, etc, para facilitar a triagem;  

- ***Milestones***: Você pode associar um *Issue* a um marco (milestone) para acompanhar o progresso de um conjunto de *Issues* relacionados a uma versão ou uma fase do projeto;  

- **Fechar/Reabrir**: Um *Issue* pode ser fechado quando o problema é resolvido ou a funcionalidade é implementada, no entanto, ele pode ser reaberto se necessário.

### **Criando um *Issue* no GitHub**

- No repositório do projeto no GitHub, clique na aba ***Issues***;  

- Crie um novo *Issue*, clicando em ***New Issue***;  

- Preencha os detalhes, como título e a descrição, sendo claro e detalhado;  

- Use *labels* para categorizar o *Issue*, atribua o *Issue* a um ou mais colaboradores e se aplicável, associe o *Issue* a um *milestone* para monitoramento de progresso;  

- Clique em ***Submit new issue*** para criar o *Issue*.

### **Exemplo de ciclo de vida de um *Issue***

- **Abertura**: Um desenvolvedor descobre um bug e abre um Issue descrevendo o problema;  

- **Discussão**: Outros desenvolvedores comentam com possíveis soluções ou discutem como reproduzir o bug;  

- **Associação e Atribuição**: O Issue é atribuído a um desenvolvedor que ficará responsável por corrigí-lo, e uma label de “bug” é adicionada;  

- **Resolução**: O desenvolvedor corrige o bug e faz o commit do código com uma mensagem referenciando o *Issue* (exemplo: “Fixes \#23”);  

- **Fechamento**: O *Issue* é então fechado automaticamente pelo GitHub quando o commit referenciado é integrado (via merge) à branch principal do projeto.

### ***Releases*** **no GitHub**

- Uma *Release* no GitHub é uma versão específica do seu projeto, geralmente marcada por um ponto importante no desenvolvimento, como o lançamento de uma nova funcionalidade, uma correção significativa ou uma versão estável;  

- As *releases* são usadas para distribuir versões “congeladas” do software para os usuários finais, permitindo que eles baixem uma versão específica do projeto, em vez de trabalhar com o código em desenvolvimento;  

- Ao criar uma *release*, o GitHub tira um *snapshot* do código em um determinado momento, isso geralmente é feito em uma branch específica, como `main` ou `master`, ou após um commit importante;  

- Releases são geralmente numeradas usando a convenção de versionamento semântico, como `v1.0.0`, `v2.1.0`, etc, cada *release* contém o código-fonte naquele estado específico e pode incluir notas da versão (*release notes*), descrevendo o que mudou desde a última *release*;  

- Você também pode anexar arquivos binários ou builds compilados à *release*, permitindo que os usuários baixem executáveis diretamente, sem precisar compilar o código por conta própria;

### **Elementos de uma *Release***

- **Tag**: É uma referência a um commit específico no histórico do Git, geralmente segue um esquema de versionamento semântico (exemplo `v1.0.0`), e é o que diferencia uma versão da outra;  

- **Notas de Versão (*Release Notes*)**: Descrição das mudanças, correções e novas funcionalidades incluídas na release, ajudando os usuários a entenderem o que mudou desde a última versão;  

- **Arquivos Anexados (opcional)**: Você pode anexar arquivos binários, como builds pré-compilados ou instaladores, isso é útil se você quiser distribuir uma versão do software que os usuários podem baixar diretamente, sem a necessidade de compilar o código;  

- **Branch ou Commit Base**: Uma *release* é geralmente baseada em uma branch (`main`, `master`) ou em um commit específico do projeto.

### **Criando uma *Release* no GitHub**

- Acesse o repositório no GitHub e clique na aba ***Releases***;  

- Crie uma nova release clicando no botão ***Draft a new release*** (Rascunhar uma nova *release*);  

- Selecione ou crie uma **Tag** que identifica a versão do projeto, exemplo: v1.0.0, e escolha a **Branch** ou o commit a partir do qual a release será feita (geralmente a branch main ou master);  

- Adicione o **Título da *Release*** (*Release Title*), exemplo: “Primeira Versão Oficial” e as **Notas da Versão** (*Release Notes*), que descrevem as mudanças feitas desde a última *release*;  

- Anexe arquivos, caso o projeto gere artefatos ou arquivos binários (como instaladores ou executáveis), para que os usuários possam baixá-los diretamente;  

- Clique em ***Publish release*** para tornar a *release* disponível publicamente.

### **Diferença entre Tags e *Releases***

- Uma tag no Git é apenas uma referência a um commit específico, usado para marcar pontos importantes no histórico do projeto, é comum marcar versões de software com tags, como `v1.0.0`, `v2.0.0`, etc;  

- Uma *Release* é uma tag “com informações extras”, ela contém as notas da versão, possíveis arquivos binários anexados, e é uma maneira organizada de distribuir versões específicas do software para os usuários;  

- Toda *release* está associada a uma tag, mas nem toda tag precisa ter uma *release*.

### **Vantagens de usar *Releases* no GitHub**

- **Distribuição fácil** \- *Releases* permitem que você distribua versões específicas do seu software para os usuários sem que eles precisem ter contato diretamente com o código-fonte;  

- **Controle de versão** \- Facilita o controle e rastreamento de versões importantes, permitindo aos usuários acessarem versões anteriores estáveis;  

- **Automatização** \- O GitHub pode se integrar com ferramentas de CI/CD (Integração Contínua/Entrega Contínua) para criar e publicar automaticamente releases a partir de builds;  

- **Histórico claro** \- Ao usar *Releases*, fica mais fácil visualizar o histórico de lançamentos do projeto, com detalhes de cada versão.

### **Pull**

- O comando `git pull` é utilizado para sincronizar o repositório local com o repositório remoto;  

- Ele faz isso de forma automática, combinando dois comandos: `git fetch` e `git merge`;  

- Ao executar o `git pull`, o Git busca as alterações mais recentes do repositório remoto e as mescla (merge) com a sua branch local;

### **Funcionamento detalhado do `git pull`**

- `git fetch`:  
  * Primeiro, o Git busca as mudanças mais recentes do repositório remoto (como commits, novas branches ou tags), mas não altera seu diretório local ainda.

- `git merge`:  
  * Depois, o Git mescla as mudanças que foram trazidas pelo fetch à sua branch local e as alterações do repositório remoto são integradas no seu histórico de commits.

### **Situações que podem ocorrer durante um git pull**

- **Fast-forward**  
  * Se sua branch local não tiver alterações que conflitem com as atualizações remotas, o Git simplesmente avança sua branch local para incluir os novos commits, nesse caso, nenhum novo commit de merge é criado e o histórico se mantém linear.

- **Merge com commit**  
  * Se houver mudanças em ambas as versões (local e remota), o Git tentará mesclar essas alterações automaticamente, podendo resultar em um **commit de merge**, que acontece quando a mesclagem não pode ser feita como um *fast-forward*.

- **Conflitos de merge**  
  * Se o Git não conseguir resolver automaticamente as diferenças entre as versões, local e remota, ele gera **conflitos de merge**, nesse caso, você terá que resolver manualmente esses conflitos nos arquivos afetados e depois finalizar o merge com um commit.