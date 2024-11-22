# ***Hashing*** **em Criptografia**

- O *Hashing* é um método para identificar um objeto dentro de um grupo, cada objeto recebe um número de identificação único após ser processado pelo *hashing*;

- Tecnicamente, uma função matemática gera uma saída de comprimento fixo a partir de uma string de entrada de qualquer tamanho;

- Por exemplo, transações de *Bitcoin* são processadas por *hashing*, onde cada transação recebe um ID único, se você inserir a string “Hello, World\!” em um algoritmo de *hashing* SHA-256, obterá o seguinte resultado:  
  * Entrada: ```Hello, World!```  
  * Saída: ```dffd6021bb2bd5b0af676290809ec3a53191dd81c7f70a4b28688a362182986f```.

- Aqui, o SHA-256 gera a saída para a entrada fornecida, como visto, utilizamos o algoritmo de *hashing* *Secure Hash Function* (SHA-256), é um dos métodos de *hashing* mais populares, junto com o *Message Digest* (MD5) e o SHA-1;

- As propriedades essenciais das funções *hash* as tornam confiáveis, vamos listá-las:

  * **Determinístico**: o mesmo *input* sempre gera o mesmo *output*, independentemente das circunstâncias;

  * **Resistência a Pré-Imagem**: o valor *hash* gerado não pode ser usado para determinar a entrada original;

  * **Eficiente Computacionalmente**: as funções *hash* são rápidas e não exigem muitos recursos computacionais;

  * **Irreversível**: não é possível realizar engenharia reversa para determinar a entrada original;

  * **Resistência a Colisões**: garante que dois *inputs* diferentes não gerem a mesma saída.

## **Funções *Hash* e Tabelas *Hash* e seu Funcionamento**

- As funções *hash* são responsáveis por converter entradas grandes em saídas pequenas e de comprimento fixo, as tabelas *hash* armazenam essas saídas;

- No processo de *hashing*, os objetos são distribuídos em pares de chave/valor dentro de um array;

- Se você passar um array de elementos para a função *hash*, receberá um array onde cada elemento agora tem uma chave associada;

- Esses pares chave/valor facilitam o acesso aos elementos em tempo real, com um desempenho impressionante de O(1);

- Existem duas abordagens comuns para implementar funções *hash*:

1. Usar uma função *hash* para converter um elemento em um número inteiro, esse número inteiro pode ser usado para acessar o elemento na tabela *hash*;

2. Colocar o elemento na tabela hash e recuperá-lo posteriormente usando a chave gerada.

- No segundo método, as funções seguem o seguinte processo:

``` python
hash = hash_function(key)  
index = hash % array_size
```

- Aqui, o valor do índice é calculado com base no tamanho do array, utilizando o operador de módulo %;

- Simplificando, uma função *hash* mapeia um conjunto de dados de tamanho indeterminado para um conjunto de dados de tamanho fixo;

- Os valores retornados pela função *hash* podem ser chamados de *hash values*, *hash sums* ou *hash codes*.

## **Criando uma Boa Função *Hash***

- Se você deseja criar uma função *hash* eficiente, é necessário atender a alguns requisitos básicos, como:

1. **Facilidade de Cálculo**: a função deve ser rápida e exigir poucos recursos computacionais;

2. **Distribuição Uniforme**: a saída da função deve ser bem distribuída para evitar agrupamentos nas tabelas *hash*;

3. **Poucas ou Nenhuma Colisão**: o ideal é minimizar colisões, em outras palavras, evitar que dois *inputs* gerem o mesmo *output*.

- Embora as colisões sejam inevitáveis em funções *hash*, o objetivo é criar mecanismos que ofereçam bom desempenho e lidem com colisões por meio de técnicas de resolução apropriadas.

## **Precisamos de uma Boa Função *Hash* para Garantir Eficiência e Evitar Colisões**

- Para entender a necessidade de uma função *hash* eficiente, vamos analisar um exemplo;

- Suponha que queremos criar uma tabela *hash* usando uma técnica de *hashing* em que as strings de entrada sejam as seguintes:

	```{“agk”, “kag”, “gak”, “akg”, “kga”, “gka”}```

- Agora, criamos uma função *hash* que simplesmente soma os valores de ASCII de ```a``` (97), ```g``` (103) e ```k``` (107) e, em seguida, faz o módulo da soma por 307;

- A soma dos três números é exatamente 307, ou seja, se permutarmos os caracteres e fizermos a operação de módulo, obteremos o mesmo resultado;

- O resultado final seria armazenar todas as strings no mesmo índice da tabela, além disso, o tempo computacional dessa função seria O(n), o que não é desejável;

- Podemos facilmente concluir que essa função *hash* não é eficiente para cenários da vida real;

- Para corrigir a função *hash*, podemos dividir a soma dos valores ASCII de cada elemento por outro número primo, como 727, garantindo saídas diferentes para o array de strings fornecido.

## **Aprendendo Sobre Tabelas Hash**

- As tabelas *hash* são extremamente úteis para armazenar os resultados de uma função *hash*;

- Elas calculam o índice e armazenam um valor associado a ele, o resultado final é um processo computacional mais rápido, com complexidade O(1);

- Tradicionalmente, tabelas *hash* são uma boa escolha para resolver problemas que requerem tempo O(n);

- Por exemplo, considere uma string fixa e o problema de contar a frequência de seus caracteres;

- Se a string for “aacddce”, uma abordagem genérica seria percorrer a string várias vezes e armazenar a frequência de cada caractere;

- **Exemplo em Python**:

```python
# Forneça uma string de entrada e conte a frequência dos caracteres

# O algoritmo possui complexidade O(n)

temp_list = []  
start = "a"  
str = "ababcddefff"

def alpha_zeta():  
    alpha = 'a'  
    for i in range(0, 26):  
        temp_list.append(alpha)  
        alpha = chr(ord(alpha) + 1)  
    return temp_list

temp_list = alpha_zeta()

def character_frequency(str, temp_list):  
    for each in temp_list:  
        freq = 0  
        for i in str:  
            if i == each:  
                freq += 1  
        print(each, freq)

character_frequency(str, temp_list)
```

- **Saída do Programa**:

```shell
a 2    
b 2    
c 1    
d 2    
e 1    
f 3    
g 0    
h 0    
i 0    
...    
...  
```

- **Exemplo em C++**:

```cpp
#include <iostream>  
using namespace std;

int Frequency[26];

int hashFunc(char c) {  
    return (c - 'a');  
}

void countFre(string S) {  
    for (int i = 0; i < S.length(); ++i) {  
        int index = hashFunc(S[i]);  
        Frequency[index]++;  
    }  
    for (int i = 0; i < 26; ++i) {  
        cout << (char)(i + 'a') << ' ' << Frequency[i] << endl;  
    }  
}

int main() {  
    cout << "Hello World" << endl;  
    countFre("abbaccbdd");  
    return 0;  
}
```

- **Saída do Programa**:

```shell
a 2    
b 3    
c 2    
d 2  
```

- A complexidade O(N) do algoritmo o torna mais rápido em comparação com outras abordagens lineares.

### **Resolvendo Colisões**

- Existem várias maneiras de resolver colisões em funções *hash*, um dos métodos mais populares é o encadeamento separado, também conhecido como *hashing* aberto;

- Ele é implementado com uma lista encadeada, onde cada elemento da cadeia é, por si só, uma lista encadeada;

- Essa abordagem permite armazenar elementos e garantir que certos elementos pertençam apenas a uma lista específica, resolvendo a colisão;

- Isso significa que nenhum valor de entrada pode ter o mesmo valor *hash* de saída.

## **Explorando *Hash* em Python**

- Como o *hashing* é uma função comum, ele já está implementado na biblioteca padrão do Python;

- Utilizando o módulo hash(), você pode fornecer um objeto como entrada e obter o valor *hash* correspondente;

- A sintaxe do método *hash* é:

```python
hash(objeto)
```

- O método aceita um único parâmetro, que pode ser um número inteiro, decimal ou string;

- O valor retornado pelo método hash() depende da entrada, para inteiros, pode retornar o mesmo número, enquanto que para decimais e strings, os resultados serão diferentes;

- **Exemplo em Python**:

```python
num = 10  
deci = 1.23556  
str1 = "Nitish"

print(hash(num))  
print(hash(deci))  
print(hash(str1))
```

- **Saída do Programa**:

![Imagem da Saída do Programa][imageRunningCode]

- Entretanto, o *hashing* não pode ser aplicado a todos os tipos de objetos;

- Por exemplo, no programa inicial em que criamos uma lista de a a z, se tentarmos aplicar *hashing*, será gerado um erro:

```shell
TypeError: unhashable type: 'list'
```

![Imagem de Saída com Mensagem de Erro][imageRunningWithError]

- Para aplicar *hashing* a uma lista de objetos, é necessário convertê-la em uma tupla:

```python
vowels = ('a', 'e', 'i', 'o', 'u')  
print(hash(vowels)) # Saída ⇒ -5678652950122127926
```

## ***Hashing*** **em Criptografia**

- O *hashing* é muito útil na criptografia, o *Bitcoin* utiliza *hashing* para criar e gerenciar árvores de *Merkle*, além disso, o *hashing* tem sido utilizado na criptografia há muito tempo;

- Um dos melhores casos de uso do *hashing* é proteger senhas por meio de seu *hash* e armazenamento seguro.

### ***Merkle Trees*** **(Árvores de *Merkle*)**

- A árvore de *Merkle* é uma estrutura de dados útil para a verificação segura de informações em um grande conjunto de dados;

- Tanto *Bitcoin* quanto *Ethereum* utilizam árvores de *Merkle* para resolver barreiras tecnológicas relacionadas ao armazenamento e acesso de dados em redes descentralizadas;

- Em redes centralizadas, o armazenamento e o acesso aos dados ocorrem em uma única fonte;

- Porém, em redes descentralizadas, os dados precisam ser replicados entre centenas de participantes;

- As árvores de *Merkle* resolvem esse problema ao fornecer uma forma confiável e eficiente de compartilhar e verificar dados entre os pares;

- As árvores de *Merkle* **utilizam o *hash* como funcionalidade central** para conectar diferentes nós e blocos de dados;

- Além disso, sua estrutura é semelhante a uma árvore invertida, que pode resumir todo o conjunto de transações.

![Exemplo de Merkle Tree][imageMerkleTreeExample]

### ***Mining Process*** **(Processo de Mineração)**

- O processo de mineração também utiliza o *hashing*, no contexto da mineração de *Bitcoin*, um novo bloco é adicionado à *Blockchain* quando necessário;

- Para adicionar o bloco, um método específico deve ser seguido, um valor de *hash* é gerado com base no conteúdo do bloco quando ele chega;

- Além disso, se o *hash* gerado for maior do que a dificuldade da rede, o processo de adição do bloco à *Blockchain* é iniciado;

- Uma vez concluído, todos os pares na rede reconhecem a adição do novo bloco, entretanto, isso raramente acontece, pois a dificuldade da rede geralmente é maior do que o *hash* gerado;

- Outro elemento fundamental no processo de mineração é o ***nonce***;

- O ***nonce*** é um valor arbitrário adicionado ao *hash* do bloco, após essa adição, a string concatenada é comparada ao nível de dificuldade;

- Se o nível de dificuldade for menor que a string concatenada, o ***nonce*** é alterado até que o nível de dificuldade seja superado;

- O processo pode ser resumido nos seguintes passos:  
1. O conteúdo de um novo bloco é transformado em um *hash* para gerar um novo valor de *hash*;

2. Um novo valor de ***nonce*** é gerado e adicionado ao *hash*;

3. O processo de *hashing* é realizado na nova string concatenada;

4. O valor final do *hash* é comparado ao nível de dificuldade da rede;

5. Se o valor final do *hash* for menor que o ***nonce***, o processo é repetido, ele só para quando o valor do *hash* for maior que o ***nonce***;

6. O bloco é então adicionado à cadeia quando o nível de dificuldade é superado;

7. Os mineradores são responsáveis por minerar o novo bloco e compartilhar as recompensas entre si.

- O termo “*hash rate*” (taxa de *hash*) também surge nesse contexto e refere-se à velocidade com que as operações de *hashing* ocorrem;

- Uma maior taxa de *hash* significa que os mineradores precisam de mais poder computacional para participar do processo de mineração.

[imageRunningCode]: <https://github.com/user-attachments/assets/40f5ce91-aba6-403f-b73e-7ae71eeca34d>

[imageRunningWithError]: <https://github.com/user-attachments/assets/26b124de-c08c-4fb4-9a0e-6265ec53268d>

[imageMerkleTreeExample]: <https://github.com/user-attachments/assets/efa593e1-e35c-44f8-830f-075282fa0b01>