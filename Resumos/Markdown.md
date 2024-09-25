# **Markdown**

- Markdown é uma linguagem de marcação simples originalmente criada por John Gruber e Aaron Swartz, utilizada para padronizar e facilitar a formatação de texto na web;  

- É frequentemente utilizada em aplicativos como **Slack** e **GitHub**, também é frequentemente usada para formatar arquivos README;  

- Textos estilizados com Markdown são, na maioria dos casos, apenas texto com caracteres não-alfabéticos, como `#`, `\*` e `![]()`, usados para a configuração de título, listas, itálico, negrito e inserção de imagens;  

- O Markdown funciona como um conversor de texto para *HyperText Markup Language* (HTML), os caracteres não-alfabéticos são traduzidos como `<strong>`, `<em>` e `<a href>`, etc;  

- Já os textos sem formatação entram como parágrafo simples `<p>`.

## **Lista de comandos em Markdown**

- Confira abaixo uma lista dos principais comandos em Markdown e alguns exemplos de seu uso.

### **Titulação**

- Para definir um título em Markdown, equivalente ao *Heading* em HTML, basta utilizar `#` acrescido do texto, por exemplo:  
  * \# Título equivale a `<h1> Título </h1>`;  
  * \#\# Título 2 equivale a `<h2> Título 2 </h2>`;  
  * \#\#\# Título 3 equivale a `<h3> Título 3 \</h3>`;  
  * \#\#\#\# Título 4 equivale a `<h4> Título 4 </h4>`;  
  * \#\#\#\#\# Título 5 equivale a `<h5> Título 5 </h5>`;  
  * \#\#\#\#\#\# Título 6 equivale a `<h6> Título 6 </h6>`.

### **Ênfase**

- Para adicionar ênfase ao conteúdo que será escrito, usa-se o asterisco `*` ou traço-baixo (*underline*) `_`;  
  * **Negrito**: adicione dois asteriscos `**texto**` ou dois *underline*s `__texto__` no início e no fim do conteúdo, isso equivale à tag `<strong> texto </strong>` do HTML;  
  * **Itálico**: adicione apenas um asterisco `*texto*` ou um traço-baixo `_texto_` no início e no fim do conteúdo, isso equivale à tag `<em> texto </em>` do HTML.

### **Listas de itens**

- Para adicionar listas não ordenadas, utilize um asterisco `*` ou um hífen `-` na frente do item da lista, por exemplo:

\* Item 1  
\* Item 2  
\* Item 3

- Outro exemplo:

\- Item 1  
\- Item 2  
\- Item 3

- Isso equivale à tag `<ul\> ... </ul>` do HTML, no caso de listas ordenadas, equivalente à tag ``<ol> … </ol>`` do HTML, utilize o número do item seguido de ponto, por exemplo:

1\. Item 1  
2\. Item 2  
3\. Item 3

### **Citação (*Quote*)**

- Para transformar um texto em uma citação ou comentário, equivalente à tag `<blockquote\> ... </blockquote\>` do HTML, utilize o sinal `>` no início da linha que será formatada, por exemplo:

\> Este é um \*blockquote\*, o sinal usado abre e fecha este código no HTML.  
Para adicionar mais uma linha à citação, basta teclar ENTER para um novo código sinal, isso gerará um novo parágrafo dentro do \*blockquote\*.

### **Código (*Code Highlight*)**

- Há dois modos de adicionar trechos de código ao Markdown:  
  * **Código em linha (*inline code*)**: adicione um acento grave ``‎`‎`` no início e no final do código, por exemplo:  

Para instalar essa lib utilize o comando \`npm install\`

* **Múltiplas linhas de código (*block code*)**: envolva as linhas de código com três acentos graves ``‎```‎`` ou três tils `~~~`, por exemplo:

Para instalar todas as dependências do projeto, utilize o comando:  
\`\`\` pip install \-r requirements.txt\`\`\`

- Para especificar ao Markdown a linguagem que está sendo apresentada no bloco de código, basta adicionar o nome da linguagem de programação após os primeiros ``‎```‎`` ou `~~~`, por exemplo:

\`\`\`python  
print("Este é um código em Python\!")  
\`\`\`

\~\~\~javascript  
console.log("Assim é o print no JavaScript")  
\~\~\~

### **Links**

- Existem duas formas de inserir um link em Markdown, através de um link direto ou usando um texto-âncora, equivalente à tag `<a href> ... </a>` do HTML;  
  * **Texto-âncora**: utilize os caracteres `[]()`, adicionando entre chaves, o texto que você quer que apareça, e entre os parênteses, o endereço de destino, no formato \[exemplo\](https://exemplo.com/);  
  * **Link direto**: envolva o endereço da web em chaves \<\>, o endereço ficará visível e será clicável pelo usuário, o endereço em forma de link direto tem o formato \<https://exemplo.com\>.

### **Imagens**

- O código para inserir uma imagem no conteúdo é semelhante ao código de inserir links-âncora, adicionando um ponto de exclamação `!` no início do código, como no exemplo abaixo:

\!\[Alt ou texto alternativo da imagem\](URL da imagem)

### **Tabela**

- Para inserir uma tabela ao Markdown, use barra `|` para delimitar as colunas, depois, utilize hífen `-` na segunda linha para indicar que acima estão os títulos das colunas, usando novamente o | para delimitar colunas, por exemplo:

| Produto | Valor do Produto |  
| \--------- | \--------- |  
| Fritadeira Elétrica | R$ 899,90 |  
| Smartphone | R$ 2799,00 |  
| Headset | R$ 249,90 |  
| Notebook | R$ 7500,00 |

- Para especificar o tipo de alinhamento que deseja ter nas tabelas, utilize `:` ao lado do campo horizontal de hífens `---`, na segunda linha da tabela, onde:
  - **Alinhado à esquerda**: usar `:` no lado esquerdo (alinhamento padrão);
  - **Alinhado à direita**: usar `:` no lado direito;
  - **Centralizado**: usar `:` em ambos os lados.  
  
| Alinhado à esquerda | Centralizado | Alinhado à direita |  
| :\--------- | :\---------: | \---------: |  
| Esquerda | Centro | Direita |