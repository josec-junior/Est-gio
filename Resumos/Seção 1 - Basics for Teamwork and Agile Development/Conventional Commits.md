# **Conventional Commits**

- A especificação do *Conventional Commits* é uma convenção simples para utilizar nas mensagens de commit;  

- Ela define um conjunto de regras para criar um histórico de commit explícito, facilitando a criação de ferramentas automatizadas;  

- Esta convenção segue o **SemVer** (*Semantic Versioning*/Versionamento Semântico), descrevendo os recursos, correções e modificações que quebram a compatibilidade nas mensagens de commit;  

- A mensagem do commit deve ser estruturada da seguinte forma:

\<tipo\> \[escopo opcional\]: \<descrição\>  
\[corpo opcional\]  
\[rodapé opcional\]

- O commit contém os seguintes elementos estruturais, para comunicar a intenção ao utilizador do seu projeto:  
  * **fix**: um commit do tipo `fix` soluciona um problema na sua base de código (isso se correlaciona com `PATCH` do Versionamento Semântico);  
    * **Exemplo**: aplicar tratativa para uma função que não está tendo o comportamento esperado e retornando erro.

  * **feat**: um commit do tipo `feat` inclui um novo recurso na sua base de código (isso se correlaciona com `MINOR` do Versionamento Semântico);  
    * **Exemplo**: acréscimo de um serviço, funcionalidade, endpoint, etc.

  * ***BREAKING CHANGE***: um commit que contém o texto `BREAKING CHANGE:` no começo do texto do corpo opcional ou do rodapé opcional, inclui uma modificação que quebra a compatibilidade da API (isso se correlaciona com `MAJOR` do Versionamento Semântico), uma *BREAKING CHANGE* pode fazer parte de commits de qualquer tipo;

  * **test**: um commit do tipo `test` inclui qualquer tipo de criação ou alteração de códigos de teste na sua base de código;  
    * **Exemplo**: criação de testes unitários.

  *  **refactor**: um commit do tipo `refactor` inclui uma refatoração de código que não tenha qualquer impacto na lógica/regras de negócio da sua base de código;  
    * **Exemplo**: mudanças de código após um *code review*.

  * **style**: um commit do tipo `style` é empregado quando há mudanças de formatação e estilo do código que não alteram o sistema de nenhuma forma;  
    * **Exemplo**: mudar o *style-guide*, mudar de convenção *lint*, arrumar indentações, remover espaços em brancos, remover comentários, etc.

  * **chore**: um commit do tipo `chore` indica mudanças no projeto que não afetem o sistema ou arquivos de testes, ou seja, mudanças de desenvolvimento;  
    * **Exemplo**: mudar regras do *eslint*, adicionar *prettier*, adicionar mais extensões de arquivos ao `.gitignore`.

  * **docs**: um commit do tipo `docs` é utilizado quando há mudanças na documentação do projeto;  
    * **Exemplo**: adicionar informações na documentação da API, mudar o README, etc.


  * **build**: um commit do tipo `build` indica mudanças que afetam o processo de build do projeto ou dependências externas;  
    * **Exemplo**: *Gulp*, adicionar/remover dependências do *npm*, etc.

  * **perf**: um commit do tipo `perf` indica uma alteração que melhorou a performance do sistema;  
    * **Exemplo**: alterar `forEach` por `while`, melhorar uma *query*, etc.

  * **ci**: um commit do tipo `ci` é utilizado para mudanças nos arquivos de configuração de CI;  
    * **Exemplo**: *Circle*, *Travis*, *BrowserStack*, etc.

  * **revert**: um commit do tipo `revert` indica a reversão de um commit anterior.

- Também é recomendado `improvement` para commits que melhoram uma implementação atual sem adicionar um novo recurso ou consertar um bug;  

- A especificação do Conventional Commits exige que o tipo de commit (como `fix` ou `feat`) seja informado, no entanto, outros tipos adicionais, como `docs` ou `chore`, não são obrigatórios e não tem efeito implícito no Versionamento Semântico (a menos que incluam uma *BREAKING CHANGE*);  

- Um escopo pode ser adicionado ao tipo do commit, para fornecer informações contextuais adicionais e está contido entre parênteses, por exemplo `feat(parser): adiciona capacidade de interpretar arrays`.

## **Exemplos**

- Mensagem de commit com descrição e *BREAKING CHANGE* no rodapé:

```
feat: permite que o objeto de configuração fornecido estenda outras configurações

BREAKING CHANGE: a chave `extends`, no arquivo de configuração, agora é utilizada para estender outro arquivo de configuração
```

- Mensagem de commit com `!` opcional para chamar a atenção para *BREAKING CHANGE*:

```
feat!: envie um e-mail ao cliente quando um produto for enviado
```

- Mensagem de commit com escopo e `!` para chamar a atenção para *BREAKING CHANGE:*

```
feat(api)!: envie um e-mail ao cliente quando um produto for enviado
```

- Mensagem de commit com ambos `!` e BREAKING CHANGE no rodapé:

```
chore!: abandonar suporte ao Node 6

BREAKING CHANGE: utilize recursos que não estão disponíveis no Node 6.
```

- Mensagem de commit sem corpo:

```
docs: ortografia correta de CHANGELOG
```

- Mensagem de commit sem escopo:

```
feat(lang): adiciona tradução para português brasileiro
```

- Mensagem de commit com corpo de vários parágrafos e vários rodapés:

```
fix: previne corrida de requisições

Introduz um ID de requisição e uma referência à última requisição. Ignora respostas recebidas que não sejam da última requisição.

Remove *timeouts* que eram usados para mitigar o problema de corrida, mas agora são obsoletos.

Revisado por: Z  
Refs: #123
```

## **Especificação**

- As palavras-chaves “DEVE” (“*MUST*”), “NÃO DEVE” (“*MUST NOT*”), “OBRIGATÓRIO” (“*REQUIRED*”), “DEVERÁ” (“*SHALL*”), “NÃO DEVERÁ” (“*SHALL NOT*”), “PODEM” (“*SHOULD*”), “NÃO PODEM” (“*SHOULD NOT*”), “RECOMENDADO” (“*RECOMMENDED*”), “PODE” (“*MAY*”) e “OPCIONAL” (“*OPTIONAL*”), nesse documento, devem ser interpretados como descrito na **RFC 2119**.

1. A mensagem de commit **DEVE** ser prefixado com um tipo, que consiste em um substantivo, como `feat`, `fix`, etc. Seguido por um escopo OPCIONAL, e é OBRIGATÓRIO terminar com dois-pontos e um espaço;  

2. O tipo `feat` **DEVE** ser usado quando um commit adiciona um novo recurso ao seu aplicativo ou biblioteca;  

3. O tipo `fix` **DEVE** ser usado quando um commit representa a correção de um problema em seu aplicativo ou biblioteca;  

4. Um escopo **PODE** ser fornecido após um tipo, um escopo **DEVE** consistir em um substantivo que descreve uma seção da base de código entre parênteses, por exemplo, `fix(parser):`;  

5. Uma descrição **DEVE** existir depois do espaço após o prefixo tipo/escopo. A descrição é um breve resumo das alterações de código, por exemplo, `fix: problema na interpretação do array quando uma string tem vários espaços`;  

6. Um corpo de mensagem de commit mais longo **PODE** ser fornecido após a descrição curta, fornecendo informações contextuais adicionais sobre as alterações no código, o corpo **DEVE** começar depois de uma linha em branco após a descrição;  

7. Um rodapé de uma ou mais linhas **PODE** ser fornecido depois de uma linha em branco após o corpo, o rodapé **DEVE** conter informações adicionais sobre o commit, por exemplo, *pull-requests*, revisores, modificações que quebram a compatibilidade, com uma informação adicional por linha;  

8. A modificação que quebra a compatibilidade **DEVE** ser indicada logo no início da seção do corpo ou no início da seção de rodapé e **DEVE** consistir de um texto em maiúsculas (*BREAKING CHANGE*), seguido por dois-pontos e um espaço;  

9. Uma descrição **DEVE** ser fornecida após o texto “*BREAKING CHANGE*:”, descrevendo o que mudou na API, por exemplo, `BREAKING CHANGE: as variáveis de ambiente agora têm preferência sobres os arquivos de configuração`;  

10. Além de `feat` e `fix`, outros tipos **PODE**M ser usados em suas mensagens de commit;  

11. Cada bloco de informação que compõe o commit convencional **NÃO DEVE** ser tratado como sensível a maiúscula e minúscula pelos implementadores, com exceção de BREAKING CHANGE, que deve ser maiúscula;  

12. Um `!` **PODE** ser acrescentado antes do : no prefixo tipo/escopo, para chamar a atenção para modificações que quebram a compatibilidade, BREAKING CHANGE: descrição também **DEVE** ser incluído no corpo ou no rodapé, junto com o `!` no prefixo.

## **Motivos para utilizar Conventional Commits**

- Criação automatizada de CHANGELOGs;  

- Determinar automaticamente um aumento de versionamento semântico (com base nos tipos de commits);  

- Comunicar a natureza das mudanças para colegas de equipe, o público e outras partes interessadas;  
- Disparar processos de build e deploy;  

- Facilitar a contribuição de outras pessoas em seus projetos, permitindo que eles explorem um histórico de commits mais estruturados.

## **Perguntas Frequentes**

- **Como devo lidar com mensagens de commit na fase inicial de desenvolvimento?**  
  * É recomendado que você proceda como se já tivesse lançado o produto, normalmente alguém, mesmo que seja seus colegas desenvolvedores, está usando seu software. Eles vão querer saber o que foi corrigido, o que quebrou, etc.

- **Os tipos no título das mensagens commit são maiúsculos ou minúsculos?**  
  * Qualquer opção pode ser usada, mas é melhor ser consistente.

- **O que fazer se o commit estiver de acordo com mais de um dos tipos?**  
  * Volte e faça vários commits sempre que possível, parte do benefício do *Conventional Commits* é a capacidade de nos levar a fazer commits e PRs mais organizados.

- **Isso não desencoraja o desenvolvimento rápido e a iteração rápida?**  
  * Desencoraja a movimentação rápida de forma desorganizada, ele ajuda você a ser capaz de se mover rapidamente a longo prazo, em vários projetos com vários colaboradores.

- **O *Conventional Commits* leva os desenvolvedores a limitar o tipo de commits que eles fazem porque estão pensando nos tipos fornecidos?**  
  * O Conventional Commits nos encoraja a fazer mais commits de tipos específicos, por exemplo correções, além disso, a flexibilidade do Conventional Commits permite que sua equipe crie seus próprios tipos e altere ao longo do tempo.

- **Qual a relação com o SemVer?**  
  * Commits do tipo `fix` devem ser enviados para *releases* `PATCH`, commits do tipo `feat` devem ser enviados para *releases* `MINOR` e commits com BREAKING CHANGE nas mensagens, independentemente do tipo, devem ser enviados para *releases* `MAJOR`.

- **Como devo versionar minhas extensões utilizando a especificação do *Conventional Commits Specification*,** e.g. `@jameswomack/conventional-commit-spec`**?**  
  * É recomendado utilizar o SemVer para liberar suas próprias extensões para esta especificação.

- **O que eu faço se acidentalmente usar o tipo errado de commit?**  
  * Antes do merge ou release com o erro, recomendamos o uso de `git rebase -i` para editar o histórico do commit, após o release, a limpeza será diferente, de acordo com as ferramentas e processos que você utiliza;

- **Todos os meus colaboradores precisam usar a especificação do *Conventional Commits*?**  
  * Não, se você usar um *workflow* de git baseado em squash, os mantenedores poderão limpar as mensagens de commit à medida que forem fazendo novos merges, não adicionando carga de trabalho aos committers casuais. Um *workflow* comum para isso é fazer com que o git faça squash dos commits automaticamente de um pull request e apresente um formulário para o mantenedor inserir a mensagem do commit apropriada para o merge.