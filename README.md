 # <center>JavaScript Básico</center>

****

###### <center>JavaScript Básico</center>

## Comentar seu código JavaScript

Comentários são linhas de código que JavaScript vai ignorar intencionalmente. Os comentários são uma ótima maneira de deixar anotações para você mesmo e para outras pessoas que mais tarde precisarão descobrir o que esse código faz.

Existem duas maneiras de escrever comentários em JavaScript:

Usar `//` dirá ao JavaScript para ignorar o resto do texto na linha atual. Isso é um comentário de uma linha:

```js
// This is an in-line comment.
```

Você pode fazer um comentário de mais de uma linha, começando com `/*` e terminando com `*/`. Este é um comentário em várias linhas:

```js
/* This is amulti-line comment */
```

***

## Declarar variáveis JavaScript

Na ciência da computação, dado é qualquer coisa que tenha significado para o computador. JavaScript fornece oito tipos de dados diferentes que são `undefined`, `null`, `boolean`, `string`, `symbol`, `bigint`, `number` e `object`.

Por exemplo, os computadores distinguem números, como o número`12`, e `strings`, como o `"12"`, `"dog"`, ou`"123 cats"`, as quais são coleções de caracteres. Computadores podem realizar operações matemáticas em um número, mas não em uma string.

Variáveis permitem aos computadores armazenar e manipular dados de forma dinâmica. Elas fazem isso usando uma "etiqueta" para apontar para o dado ao invés de usar o próprio dado. Qualquer um dos 8 tipos de dados pode ser armazenado em uma variável.

Variáveis são similares às variáveis x e y utilizadas na matemática, o que significa que elas são simples nomes para representar os dados aos quais se referem. Variáveis de computador diferem das variáveis matemáticas porque elas podem armazenar diferentes valores em momentos diferentes.

Dizemos ao JavaScript para criar ou declarar uma variável colocando a palavra-chave `var` na frente dela, dessa forma:

```js
var ourName;
```

cria uma variável chamada `ourName`. Em JavaScript, terminamos uma instrução com ponto e vírgula. Nomes de variáveis podem ser formados por números, letras e `$` ou `_`, mas não podem conter espaços ou começar com um número.

***

## Armazenar valores com o operador de atribuição

Em JavaScript, você pode armazenar um valor em uma variável com o operador de atribuição (`=`).

```js
myVariable = 5;
```

Isso atribui um valor do tipo `Number` de `5` para `myVariable`.

Se há qualquer cálculo à direita do operador `=`, esses cálculos são executados antes do valor ser atribuído à variável na esquerda do operador.

```js
var myVar;
myVar = 5;
```

Primeiro, esse código cria uma variável chamada `myVar`. Em seguida, o código atribui `5` para `myVar`. Agora, se `myVar` aparece novamente no código, o programa vai tratá-la como se fosse `5`.

****

## Atribuir o valor de uma variável para outra

Após um valor ser atribuído para uma variável usando o operador de atribuição, você pode atribuir o valor daquela variável para outra variável usando o operador de atribuição.

```js
var myVar;
myVar = 5;
var myNum;
myNum = myVar;
```

O código acima declara uma variável `myVar` sem valor, e então atribui a ela o valor `5`. Em seguida, uma variável chamada `myNum` é declarada sem valor. Depois, o conteúdo de `myVar` (o qual é `5`) é atribuído para a variável `myNum`. Agora, `myNum` também possui o valor de `5`.

****

## Inicializar variáveis com o operador de atribuição

É comum inicializar a variável com um valor inicial na mesma linha em que é declarada.

```js
var myVar = 0;
```

Cria uma nova variável chamada `myVar` e atribua o seu valor inicial como `0`.

****

## Declarar variáveis de string

Anteriormente, você usou o seguinte código para declarar uma variável:

```js
var myName;
```

Mas você também pode declarar uma variável string assim:

```js
var myName = "your name";
```

`"your name"` é chamado de string literal. Uma string literal, ou string, é uma série de 0 ou mais caracteres entre aspas simples ou duplas.

****

## Entender variáveis não inicializadas

Quando as variáveis de JavaScript são declaradas, elas têm um valor inicial de `undefined`. Se você fizer uma operação matemática em uma variável `undefined`, seu resultado será `NaN`, o que significa que "Não é um número". Se você concatenar uma string com uma variável `undefined`, você receberá uma string com o valor `undefined`.

****

## Entender a sensibilidade a caracteres maiúsculos e minúsculos em variáveis

Em JavaScript todas os nomes de variáveis e funções são sensíveis a caracteres maiúsculos e minúsculos. Isso significa que a capitalização importa.

`MYVAR` não é o mesmo que `MyVar` nem `myvar`. É possível ter diversas variáveis distintas com o mesmo nome mas com capitalização diferente. É extremamente recomendado pelo bem da clareza, que você *não* use esse recurso da linguagem.

**Melhores práticas**

Escreva nomes de variáveis em JavaScript em camelCase. Em camelCase, nomes de variáveis com mais de uma palavra possuem a primeira palavra toda em minúscula e a primeira letra de cada palavra subsequente capitalizada.

****

## Diferenciar entre as  palavras-chave var e let

Um dos maiores problemas ao declarar variáveis com a palavra-chave `var` é que você pode sobrescrever facilmente declarações de variável:

```js
var camper = "James";
var camper = "David";
console.log(camper);
```

No código acima, a variável `camper` é originalmente declarada com o valor `James` e então substituída pelo valor `David`. O console, então, vai exibir a string `David`.

Em uma aplicação pequena, você pode não encontrar esse tipo de problema. Mas à medida que sua base de código se tornar maior, você pode sobrescrever acidentalmente uma variável que você não pretendia. Como esse comportamento não lança um erro, a busca e correção de bugs tornam-se mais difíceis.

Uma palavra-chave chamada `let` foi introduzida na ES6, uma grande atualização para o JavaScript, para resolver este possível problema com a palavra-chave `var`. Você vai aprender sobre outros recursos da ES6 em desafios posteriores.

Se você substituir `var` por `let` no código acima, ele resultará em um erro:

```js
let camper = "James";
let camper = "David";
```

O erro pode ser visto no console do seu navegador.

Então, diferente de `var`, ao usar `let`, uma variável com o mesmo nome só pode ser declarada uma única vez.

****

## Declarar variáveis somente de leitura com a palavra-chave const

A palavra-chave `let` não é a única nova forma de declarar variáveis. Na versão ES6, você também pode declarar variáveis usando a palavra-chave `const`.

`const` possui todos os recursos maravilhosos que `let` tem, com o bônus adicional que variáveis declaradas usando `const` são somente de leitura. Elas têm um valor constante, o que significa que a variável atribuída com `const` não pode ser atribuída novamente:

```js
const FAV_PET = "Cats";
FAV_PET = "Dogs";
```

O console vai exibir um erro devido à reatribuição do valor de `FAV_PET`.

Você sempre deve nomear variáveis que você não quer reatribuir, usando a palavra-chave `const`. Isso ajuda quando você acidentalmente tenta reatribuir uma variável que deveria ser constante.

**Observação:** é comum que os desenvolvedores usem nomes de variáveis maiúsculas para valores imutáveis e minúsculas ou camelCase para valores mutáveis (objetos e arrays). Você aprenderá mais sobre objetos, arrays e valores imutáveis e mutáveis em desafios futuros. Em desafios posteriores, você também verá exemplos de identificadores de variáveis maiúsculas, minúsculas ou em camelCase.

****

## Adicionar dois números com JavaScript

`Number` é um tipo de dado em JavaScript que representa um dado numérico.

Agora, vamos tentar adicionar dois números usando JavaScript.

JavaScript utiliza o símbolo `+` como um operador de adição quando colocado entre dois números.

**Exemplo:**

```js
const myVar = 5 + 10;
```

`myVar` agora tem o valor de `15`.

****

## Subtrair um número de outro com JavaScript

Nós também podemos subtrair um número de outro.

JavaScript usa o símbolo `-` para subtração.

**Exemplo**

```js
const myVar = 12 - 6;
```

`myVar` teria o valor `6`.

****

## Multiplicar dois números com JavaScript

Nós também podemos multiplicar um número por outro.

JavaScript usa o símbolo `*` para multiplicação de dois números.

**Exemplo**

```js
const myVar = 13 * 13;
```

`myVar` teria o valor `169`.

****

## Dividir um número por outro com JavaScript

Nós também podemos dividir um número por outro.

JavaScript usa o símbolo `/` para divisão.

**Exemplo**

```js
const myVar = 16 / 2;
```

`myVar` agora possui o valor `8`.

****

## Incrementar um número com JavaScript

Você pode facilmente incrementar ou adicionar 1 à variável com o operador `++`.

```js
i++;
```

é o equivalente a

```js
i = i + 1;
```

**Observação:** a linha inteira torna-se `i++;`, eliminando a necessidade para o sinal de igual (atribuição).

****

## Decrementar um número com JavaScript

Você pode facilmente decrementar ou diminuir uma variável por um com o operador `--`.

```js
i--;
```

é o equivalente a

```js
i = i - 1;
```

**Observação:** a linha inteira torna-se `i--;`, eliminando a necessidade para o sinal de igual (atribuição).

****

## Criar números decimais com JavaScript

Nós também podemos armazenar números decimais em variáveis. Números decimais são às vezes referidos como números de ponto flutuante ou floats.

****

## Multiplicar dois decimais com JavaScript

Em JavaScript, você também pode realizar cálculos com números decimais, assim como com números inteiros.

****

## Descobrir o resto em JavaScript

O operador de resto `%` retorna o resto da divisão de dois números.

**Exemplo**

> 5 % 2 = 1 porque  
> Math.floor(5 / 2) = 2 (Quociente)  
> 2 * 2 = 4  
> 5 - 4 = 1 (Resto)

**Uso**  
Na matemática, um número pode ser verificado como par ou ímpar por meio do resto da divisão do número por `2`.

> 17 % 2 = 1 (17 é Ímpar)  
> 48 % 2 = 0 (48 é Par)

**Observação:** o operador de resto às vezes é referido incorretamente como o operador de módulo. É muito semelhante ao módulo, mas não funciona adequadamente com números negativos.

****

## Atribuir de modo composto com adição aumentada

Na programação, é comum usar atribuições para modificar o conteúdo de uma variável. Lembre-se de que tudo à direita do sinal de igual é avaliado primeiro, para que possamos dizer:

```js
myVar = myVar + 5;
```

para adicionar `5` a `myVar`. Como este é um padrão tão comum, existem operadores que realizam uma operação matemática e atribuição em um passo.

Um desses operadores é o operador `+=`.

```js
let myVar = 1;
myVar += 5;
console.log(myVar);
```

`6` seria exibido no console.

****

## Atribuir de modo composto com subtração aumentada

Como o operador `+=`, `-=` subtrai um número de uma variável.

```js
myVar = myVar - 5;
```

vai subtrair `5` de `myVar`. Essa expressão pode ser reescrita assim:

```js
myVar -= 5;
```

****

## Atribuir de modo composto com multiplicação aumentada

O operador `*=` multiplica uma variável por um número.

```js
myVar = myVar * 5;
```

multiplicará `myVar` por `5`. Essa expressão pode ser reescrita assim:

```js
myVar *= 5;
```

****

## Atribuir de modo composto com divisão aumentada

O operador `/=` divide uma variável por outro número.

```js
myVar = myVar / 5;
```

dividirá `myVar` por `5`. Essa expressão pode ser reescrita assim:

```js
myVar /= 5;
```

****

## Escapar aspas literais em strings

Quando você estiver definindo uma sequência de caracteres você deve iniciar e terminar com uma aspa simples ou dupla. O que acontece quando você precisa de uma aspa literal: `"` ou `'` dentro de sua string?

Em JavaScript, você pode escapar uma aspa para que não seja considerada como o fim de uma string ao colocar a barra invertida (`\`) na frente da aspa.

```js
const sampleStr = "Alan said, \"Peter is learning JavaScript\".";
```

Isso sinaliza ao JavaScript que a aspa seguinte não é o fim de uma string, mas que deve aparecer dentro da string. Então, se você fosse imprimir isso no console, você obteria:

```js
Alan said, "Peter is learning JavaScript".
```

****

## Cercar uma string com aspas simples

Valores de string em JavaScript podem ser escritas com aspas simples ou duplas, desde que você comece e termine com o mesmo tipo de aspas. Diferente de outras linguagens de programação, aspas simples e duplas funcionam da mesma forma em JavaScript.

```js
const doubleQuoteStr = "This is a string"; 
const singleQuoteStr = 'This is also a string';
```

O motivo pelo qual você pode querer usar um tipo de aspas no lugar da outra é se você vir a querer usar ambas em uma string. Isso pode acontecer se você quiser salvar uma conversa em uma string e ter a conversa entre aspas. Outro uso para isso seria salvar uma tag `<a>` com vários atributos em aspas, tudo dentro de uma string.

```js
const conversation = 'Finn exclaims to Jake, "Algebraic!"';
```

Porém, isso se torna um problema se você precisar usar as aspas mais extremas dentro dela. Lembre-se, uma string tem o mesmo tipo de aspas no início e no final. Mas se você tem aquela mesma aspa em algum lugar no meio, a string vai terminar mais cedo e lançará um erro.

```js
const goodStr = 'Jake asks Finn, "Hey, let\'s go on an adventure?"'; 
const badStr = 'Finn responds, "Let's go!"';
```

Aqui `badStr` lançará um erro.

Na string goodStr acima, você pode usar ambas as aspas com segurança ao usar a barra invertida `\` como um caractere de escapamento.

**Observação:** a barra invertida `\` não deve ser confundida com a barra comum `/`. Elas não fazem a mesma coisa.

****

## Escapar sequências em strings

Aspas não são os únicos caracteres que podem ser escapados dentro de uma string. Há dois motivos para usar caracteres de escapamento:

1. Para permitir que você use caracteres que você pode não ser capaz de digitar do contrário, como o caractere de retorno de carro.
2. Para permitir que você represente várias aspas em uma string sem o JavaScript entender erroneamente o que você quis dizer.

Aprendemos isso no desafio anterior.

| Código | Saída             |
| ------ | ----------------- |
| `\'`   | aspas simples     |
| `\"`   | aspas duplas      |
| `\\`   | barra invertida   |
| `\n`   | nova linha        |
| `\r`   | retorno de carro  |
| `\t`   | tab               |
| `\b`   | limite de palavra |
| `\f`   | quebra de página  |

*Note que a própria barra invertida deve ser escapada para ser exibida como uma barra invertida.*

****

## Concatenar strings com o operador mais

Em JavaScript, quando o operador `+` é usado com um valor de `String`, ele é chamado de operador de concatenação. Você pode criar uma nova string a partir de outras strings ao concatenar elas juntos.

**Exemplo**

```js
'My name is Alan,' + ' I concatenate.'
```

**Observação:** cuidado com os espaços. A concatenação não adiciona espaços entre strings concatenadas, então você mesmo precisará adicioná-las.

Exemplo:

```js
const ourStr = "I come first. " + "I come second.";
```

A string `I come first. I come second.` seria exibida no console.

****

## Concatenar strings com o operador mais igual

Também podemos usar o operador `+=` para concatenar uma string no final de uma variável string existente. Isso pode ser muito útil para quebrar uma longa string em várias linhas.

**Observação:** cuidado com os espaços. A concatenação não adiciona espaços entre strings concatenadas, então você mesmo precisará adicioná-los.

Exemplo:

```js
let ourStr = "I come first. ";
ourStr += "I come second.";
```

`ourStr` agora deve ter como valor a string `I come first. I come second.`.

****

## Criar strings com variáveis

Às vezes, você precisará criar uma string. Usando o operador de concatenação (`+`), você pode inserir uma ou mais variáveis em uma string que você está criando.

Exemplo:

```js
const ourName = "freeCodeCamp";
const ourStr = "Hello, our name is " + ourName + ", how are you?";
```

`ourStr` teria o valor da string `Hello, our name is freeCodeCamp, how are you?`.

****

## Adicionar variáveis para strings

Assim como podemos construir uma string em várias linhas através das strings literais, nós também podemos adicionar as variáveis para a string usando o operador mais igual (`+=`).

Exemplo:

```js
const anAdjective = "awesome!";
let ourStr = "freeCodeCamp is ";
ourStr += anAdjective;
```

`ourStr` teria o valor `freeCodeCamp is awesome!`.

****

## Encontrar o tamanho de uma string

Você pode encontrar o tamanho de um valor de `String` ao escrever `.length` após a variável de string ou literal de string.

```js
console.log("Alan Peter".length);
```

O valor `10` seria exibido no console. Observe que o caractere de espaço entre "Alan" e "Peter" também é contado.

Por exemplo, se nós criássemos uma variável `const firstName = "Ada"`, poderíamos descobrir qual o tamanho da string `Ada` usando a propriedade `firstName.length`.

****

## Usar notação de colchetes para encontrar o primeiro caractere em uma string

Notação de colchetes é uma forma de pegar um caractere no índice especificado dentro de uma string.

A maioria das linguagens de programação modernas, como JavaScript, não começa contando do 1 como humanos fazem. Elas começam no 0. Isso é referido como indexação baseada em zero.

Por exemplo, o caractere no índice 0 da palavra `Charles` é `C`. Então, se `const firstName = "Charles"`, você pode pegar o valor da primeira letra da string usando `firstName[0]`.

Exemplo:

```js
const firstName = "Charles";
const firstLetter = firstName[0];
```

`firstLetter` teria o valor da string `C`.

****

## Entender a imutabilidade das strings

Em JavaScript, valores `String` são imutáveis, o que significa que elas não podem ser alteradas após serem criadas.

Por exemplo, o código a seguir produzirá um erro porque a letra `B` na cadeia de caracteres `Bob` não pode ser alterada para a letra `J`:

```js
let myStr = "Bob";
myStr[0] = "J";
```

Observe que isso *não* significa que `myStr` não possa ser reatribuída. A única forma de alterar `myStr` seria atribuindo a ela um novo valor, deste modo:

```js
let myStr = "Bob";
myStr = "Job";
```

****

## Usar notação de colchetes para encontrar o enésimo caractere em uma string

ocê também pode usar notação de colchetes para pegar caracteres em outras posições em uma string.

Lembre-se de que computadores começam contando do `0`. Então, o primeiro caractere é na verdade o caractere na posição 0.

Exemplo:

```js
const firstName = "Ada";
const secondLetterOfFirstName = firstName[1];
```

`secondLetterOfFirstName` teria o valor da string `d`.

****

## Usar a notação de colchetes para encontrar o último caractere em uma string

Para pegar a última letra de uma string, você pode subtrair um do tamanho da string.

Por exemplo, se `const firstName = "Ada"`, você pode pegar o valor da última letra da string ao usar `firstName[firstName.length - 1]`.

Exemplo:

```js
const firstName = "Ada";
const lastLetter = firstName[firstName.length - 1];
```

`lastLetter` teria o valor da string `a`.

****

## Usar a notação de colchetes para descobrir o enésimo caractere antes do último em uma string

Você pode usar o mesmo princípio que nós acabamos de usar para recuperar o último caractere em uma string, para recuperar o enésimo caractere antes do último caractere.

Por exemplo, você pode pegar o valor da antepenúltima letra da string `const firstName = "Augusta"` usando `firstName[firstName.length - 3]`

Exemplo:

```js
const firstName = "Augusta";
const thirdToLastLetter = firstName[firstName.length - 3];
```

`thirdToLastLetter` teria o valor da string `s`.

****

## Preencher espaços em branco

Você recebe frases com algumas palavras faltando, como substantivos, verbos, adjetivos e advérbios. Você então preencherá os pedaços faltantes com palavras de sua escolha de modo que a frase completa faça sentido.

Considere a frase - Era realmente **____** e nós **____** nós mesmos **____**. Essa frase possui três pedaços faltando - um adjetivo, um verbo e um advérbio, e nós podemos adicionar palavras de nossa escolha para completar. Em seguida, podemos atribuir a frase completa para uma variável como se segue:

```js
const sentence = "It was really " + "hot" + ", and we " + "laughed" + " ourselves " + "silly" + ".";
```

****

## Armazenar múltiplos valores em uma variável usando arrays JavaScript

Com as variáveis de `array` em JavaScript, podemos armazenar diversos dados em um único lugar.

Você começa uma declaração de um array com a abertura de um colchetes, terminando com o fechamento do colchetes e colocando vírgulas entre cada entrada, dessa forma:

```js
const sandwich = ["peanut butter", "jelly", "bread"];
```

****

## Aninhar um array em outro array

Você também pode aninhar arrays dentro de outros arrays, como abaixo:

```js
const teams = [["Bulls", 23], ["White Sox", 45]];
```

Isso é chamado um array multidimensional.

****

## Acessar array de dados com índices

Podemos acessar os dados dentro de arrays usando indexes.

Os índices de um array são escritos na mesma notação com colchetes que as strings usam. Porém, em vez de especificar um caractere, eles estão especificando um item do array. Assim como ocorre com as strings, os arrays usam indexação de base zero, de forma que o primeiro elemento de um array possui índice `0`.

**Exemplo**

```js
const array = [50, 60, 70];
console.log(array[0]);
const data = array[1];
```

O `console.log(array[0])` exibirá `50` e `data` terá o valor de `60`.

****

## Modificar dados de array com índices

Ao contrário das strings, as entradas de arrays são mutáveis e podem ser alteradas livremente, mesmo se o array foi declarado com `const`.

**Exemplo**

```js
const ourArray = [50, 40, 30];
ourArray[0] = 15;
```

`ourArray` agora tem o valor `[15, 40, 30]`.

**Observação:** não deve haver espaços entre o nome do array e os colchetes, como `array [0]`. Embora JavaScript seja capaz de processar isso corretamente, isso pode confundir outros programadores lendo seu código.

****

## Acessar arrays multidimensionais com índices

Uma maneira de pensar em um array multidimensional é como um *array de arrays*. Quando você usa colchetes para acessar seu array, o primeiro conjunto de colchetes se refere às entradas no array mais exterior (o primeiro nível), e cada par adicional de colchetes refere-se ao próximo nível de entradas interno.

**Exemplo**

```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];
```

Neste exemplo, `subarray` tem o valor de `[[10, 11, 12], 13, 14]`, `nestedSubarray` tem o valor de `[10, 11, 12]` e `element` tem o valor de `11` .

**Observação:** não deve haver nenhum espaço entre o nome do array e os colchetes como `array [0][0]` e até mesmo `array [0] [0]` não é permitido. Embora JavaScript seja capaz de processar isso corretamente, isso pode confundir outros programadores lendo seu código.

****

## Manipular arrays com push()

Uma forma fácil de adicionar dados no final de um array é através da função `push()`.

`.push()` recebe um ou mais parâmetros e "empurra" eles no final do array.

Exemplos:

```js
const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```

`arr1` agora tem o valor de `[1, 2, 3, 4]` e `arr2` tem o valor de `["Stimpson", "J", "cat", ["happy", "joy"]]`.

****

## Manipular arrays com pop()

Outra forma de alterar os dados em um array é com a função `.pop()`.

`.pop()` é usado para remover um valor do final do array. Nós podemos armazenar esse valor removido atribuindo-o a uma variável. Em outras palavras, `.pop()` remove o último elemento de um array e retorna aquele elemento.

Qualquer tipo de entrada pode ser removida de um array - numbers, strings e até mesmo arrays aninhados.

```js
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);
```

O primeiro `console.log` exibirá o valor `6` e o segundo exibirá o valor `[1, 4]`.

****

## Manipular arrays com shift()

`pop()` sempre remove o último elemento de um array. E se você quiser remover o primeiro?

É aí que o `.shift()` vem a ser útil. Ele funciona da mesma forma que `.pop()`, exceto que ele remove o primeiro elemento ao invés do último.

Exemplo:

```js
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
```

`removedFromOurArray` teria o valor da string `Stimpson` e `ourArray` teria o valor de `["J", ["cat"]]`.

****

## Manipular arrays com unshift()

Você pode não apenas usar `shift` para remover elementos do início de um array, como também pode usar `unshift` para adicionar elementos ao início de um array, ou seja, adicionar elementos na posição inicial do array.

`.unshift()` funciona exatamente como `.push()`, mas, ao invés de adicionar o elemento ao final do array, `unshift()` adiciona o elemento no início do array.

Exemplo:

```js
const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```

Após o `shift`, `ourArray` teria o valor `["J","cat"]`. Após o `unshift`, `ourArray` teria o valor `["Happy","J","cat"]`.

****

## Escrever JavaScript reutilizável com funções

Em JavaScript, nós podemos dividir nosso código em partes reutilizáveis chamadas de funções.

Aqui está um exemplo de uma função:

```js
function functionName() {
  console.log("Hello World");
}
```

Você pode chamar ou invocar essa função ao usar seu nome seguido de parênteses, da seguinte forma: `functionName();` Cada vez que a função é chamada, imprimirá no console a mensagem `Hello World`. Todo o código entre as chaves será executado toda vez que uma função for chamada.

****

## Passar valores para funções com argumentos

Parâmetros são variáveis que atuam como espaços reservados para os valores que são passados para uma função, quando ela é chamada. Quando uma função é definida, normalmente ela é definida junto com um ou mais parâmetros. Os valores reais que são entradas de (ou "passadas" para) uma função quando ela é chamada são conhecidos como argumentos.

Aqui está uma função com dois parâmetros, `param1` e `param2`:

```js
function testFun(param1, param2) {
  console.log(param1, param2);
}
```

Então podemos chamar o `testFun` dessa forma: `testFun("Hello", "World");`. Passamos dois argumentos do tipo string, `Hello` e `World`. Dentro da função, `param1` será igual à string `Hello` e `param2` será igual à string `World`. Note que você poderia chamar o `testFun` novamente com diferentes argumentos e os parâmetros assumiriam o valor dos novos argumentos.

****

## Retornar um valor de uma função com return

Nós podemos passar valores para uma função com argumentos. Você pode usar uma instrução `return` para enviar um valor para fora de uma função.

**Exemplo**

```js
function plusThree(num) {
  return num + 3;
}

const answer = plusThree(5);
```

`answer` tem o valor de `8`.

`plusThree` recebe um argumento para `num` e retorna um valor igual a `num + 3`.

****

## Conhecer o escopo global e funções

Em JavaScript, escopo refere-se à visibilidade de variáveis. Variáveis que são definidas fora de um bloco de função tem o escopo Global. Isso significa que elas podem ser vistas em qualquer lugar no seu código JavaScript.

Variáveis que são declaradas sem a palavra-chave `let` ou `const` são automaticamente criadas no escopo `global`. Isso pode criar consequências indesejadas em outro lugar no seu código ou quando executar uma função novamente. Você sempre deve declarar suas variáveis com `let` ou `const`.

****

## Conhecer o escopo local e funções

Variáveis que são declaradas dentro de uma função, assim como parâmetros das funções, possuem escopo local. Isso significa que elas são visíveis apenas dentro da função.

Aqui está uma função `myTest` com uma variável local chamada `loc`.

```js
function myTest() {
  const loc = "foo";
  console.log(loc);
}

myTest();
console.log(loc);
```

A chamada da função `myTest()` vai exibir a string `foo` no console. A linha `console.log(loc)` (fora da função `myTest`) vai lançar um erro, já que `loc` não foi definido fora da função.

****

## Difrerenciar o escopo global e local com funções

É possível ter as variáveis local e global com o mesmo nome. Quando você faz isso, a variável local tem precedência sobre a variável global.

Neste exemplo:

```js
const someVar = "Hat";

function myFun() {
  const someVar = "Head";
  return someVar;
}
```

A função `myFun` retornará a string `Head` porque a versão local da variável está presente.

****

## Entender o valor undefined retornado de uma função

Uma função pode incluir a instrução `return` mas ela não precisa fazer isso. No caso de a função não ter uma instrução `return`, quando você a chamar, a função processa o código interno, mas o valor retornado é `undefined`.

**Exemplo**

```js
let sum = 0;

function addSum(num) {
  sum = sum + num;
}

addSum(3);
```

`addSum` é uma função sem uma instrução `return`. A função vai alterar a variável global `sum`, mas o valor retornado da função é `undefined`.

****

## Atribuir com o valor retornado

Se você se lembrar de nossa discussão sobre como [armazenar valores com o operador de atribuição](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/storing-values-with-the-assignment-operator), tudo à direita do sinal de igual é resolvido antes de o valor ser atribuído. Isso significa que podemos pegar o valor de retorno de uma função e atribuí-lo a uma variável.

Assuma que temos uma função predefinida chamada `sum`, que soma dois números. Então:

```js
ourSum = sum(5, 12);
```

chamará a função `sum`, a qual retorna o valor `17` e então atribui este valor à variável `ourSum`.

****

## Ficar na linha

Na Ciência da Computação, uma fila é uma estrutura de dados abstrata onde itens são mantidos em ordem. Novos itens podem ser adicionados no final da fila e itens mais antigos são removidos do início da fila.

****

## Entender valores booleanos

Outro tipo de dado é o booleano. Booleanos podem ser apenas dois valores: `true` ou `false`. Eles basicamente são interruptores pequenos, onde `true` é ligado e `false` é desligado. Esses dois estados são mutuamente exclusivos.

**Observação:** valores booleanos nunca são escritos com aspas. As strings `"true"` e `"false"` não são booleanos e não tem nenhum significado especial em JavaScript.

****

## Usar lógica condicional com instruções if

instruções `if` são usadas para tomar decisões no código. A palavra-chave `if` diz ao JavaScript para executar o código nas chaves sob certas condições, definidas nos parênteses. Essas condições são conhecidas como condições `Boolean` e elas só podem ser `true` ou `false`.

Quando a condição for `true`, o programa executará as instruções dentro das chaves. Quando a condição booleana for `false`, as instruções dentro das chaves não serão executadas.

**Pseudocódigo**

> if (*condição é verdadeira*) {  
> *instrução é executada*  
> }

**Exemplo**

```js
function test (myCondition) {
  if (myCondition) {
    return "It was true";
  }
  return "It was false";
}

test(true);
test(false);
```

`test(true)` retorna a string `It was true` e `test(false)` retorna a string `It was false`.

Quando `test` é chamado com o valor `true`, a instrução `if` avalia `myCondition` para verificar se é `true` ou não. Já que é `true`, a função retorna `It was true`. Quando chamamos `test` com um valor de `false`, `myCondition` *não é* `true`, a instrução nas chaves não é executada e a função retorna `It was false`.

****

## Comparar com o operador de igualdade

Há muitos operadores de comparação em JavaScript. Todos esses operadores retornam um valor booleano `true` ou `false`.

O operador mais básico é o operador de igualdade `==`. O operador de igualdade compara dois valores e retorna `true` se eles são equivalentes ou `false` se não são. Observe que o operador de igualdade é diferente do operador de atribuição (`=`), que atribui o valor à direita do operador para uma variável à esquerda.

```js
function equalityTest(myVal) {
  if (myVal == 10) {
    return "Equal";
  }
  return "Not Equal";
}
```

Se `myVal` é igual a `10`, o operador de igualdade retorna `true`, assim o código nas chaves será executado e a função retornará `Equal`. Caso contrário, a função retornará `Not Equal`. Para que o JavaScript possa comparar dois tipos de dados diferentes (por exemplo, `numbers` e `strings`), deve converter um tipo para outro. Isto é conhecido como coerção de tipo (casting ou type coercion). No entanto, uma vez que a faça, você pode comparar os termos da seguinte forma:

```js
1   ==  1  // true
1   ==  2  // false
1   == '1' // true
"3" ==  3  // true
```

****

## Comparar com o operador de igualdade de estrita

Igualdade estrita (`===`) é a contrapartida do operador de igualdade (`==`). No entanto, ao contrário do operador de igualdade, que tenta converter ambos os valores em comparação a um tipo comum, o operador estrito de igualdade não realiza uma conversão de tipo.

Se os valores que são comparados tiverem valores diferentes, são considerados desiguais, e o operador de igualdade estrito retornará falso.

**Exemplos**

```js
3 ===  3  // true
3 === '3' // false
```

No segundo exemplo, `3` é um tipo de `Number` e `'3'` é um tipo `String`.

****

## Praticar a comparação de diferentes valores

Nos últimos dois desafios, aprendemos sobre o operador de igualdade (`==`) e o operador de igualdade estrita (`===`). Vamos fazer uma breve revisão e praticar usando esses operadores mais uma vez.

Se os valores sendo comparados não são do mesmo tipo, o operador de igualdade fará a conversão de tipo e, então, avaliará os valores. No entanto, o operador de igualdade estrita vai comparar ambos os tipos de dados e os valores, sem converter de um tipo para outro.

**Exemplos**

`3 == '3'` retorna `true` porque JavaScript faz a conversão de tipo de string para número. `3 === '3'` retorna `false` porque os tipos são diferentes e não é feita a conversão de tipo.

**Observação:** em JavaScript, você pode determinar o tipo de uma variável ou de um valor, com o operador `typeof`, como vemos a seguir:

```js
typeof 3
typeof '3'
```

`typeof 3` retorna a string `number` e `typeof '3'` retorna a string `string`.

****

## Comparar com o operador de desigualdade

O operador de desigualdade (`!=`) é o oposto do operador de igualdade. Significa que não é igual e retorna `false` onde a igualdade retornaria `true` e *vice-versa*. Tal como o operador de igualdade, o operador de desigualdade converterá os tipos de dados de valores enquanto compara.

**Exemplos**

```js
1 !=  2    // true
1 != "1"   // false
1 != '1'   // false
1 != true  // false
0 != false // false
```

****

## Comparar com o operador de desigualdade estrita

O operador de desigualdade estrito (`!==`) é o oposto lógico do operador de igualdade estrito. Significa que "não é estritamente igual" e retorna `false` onde a igualdade estrita retornaria `true` e *vice-versa*. O operador de desigualdade estrita não converterá tipos de dados.

**Exemplos**

```js
3 !==  3  // false
3 !== '3' // true
4 !==  3  // true
```

****

## Comparar com o operador maior que

O operador maior que (`>`) compara os valores de dois números. Se o número à esquerda for maior que o número à direita, ele retorna `true`. Caso contrário, ele retorna `false`.

Tal como o operador de igualdade, o operador maior que converterá os tipos de dados de valores enquanto compara.

**Exemplos**

```js
5   >  3  // true
7   > '3' // true
2   >  3  // false
'1' >  9  // false
```

****

## Comparar com o operador maior ou igual

O operador maior ou igual que (`>=`) compara os valores de dois números. Se o número à esquerda é maior ou igual ao número à direita, ele retorna `true`. Caso contrário, ele retornará `false`.

Tal como o operador de igualdade, o operador maior que converterá os tipos de dados de valores enquanto compara.

**Exemplos**

```js
6   >=  6  // true
7   >= '3' // true
2   >=  3  // false
'7' >=  9  // false
```

****

## Comparar com o operador menor que

O operador menor que (`<`) compara os valores de dois números. Se o número à esquerda for menos que o número à direita, retornará `true`. Caso contrário, retorna `false`. Assim como o operador de igualdade, o operador menor que converte os tipos de dados enquanto compara.

**Exemplos**

```js
2   < 5 // true
'3' < 7 // true
5   < 5 // false
3   < 2 // false
'8' < 4 // false
```

****

## Comparar com o operador menor ou igual

O operador menor ou igual (`<=`) compara os valores de dois números. Se o número à esquerda for menor ou igual ao número à direita, retornará `true`. Se o número à esquerda for maior que o número a direita, retornará `false`. Assim como o operador de igualdade, o operador de menor ou igual que converte os tipos de dados.

**Exemplos**

```js
4   <= 5 // true
'7' <= 7 // true
5   <= 5 // true
3   <= 2 // false
'8' <= 4 // false
```

****

## Comparar com o operador lógico AND

Às vezes, você precisará testar mais de uma coisa de cada vez. O operador lógico AND (`&&`) retornará `true` apenas se os operadores à esquerda e à direita forem verdadeiros.

O mesmo efeito pode ser alcançado aninhando uma instrução if dentro de outro if:

```js
if (num > 5) {
  if (num < 10) {
    return "Yes";
  }
}
return "No";
```

só retornará `Yes` se `num` for maior que `5` e menor que `10`. A mesma lógica pode ser escrita assim:

```js
if (num > 5 && num < 10) {
  return "Yes";
}
return "No";
```

****

## Comparar com o operador lógico OR

O operador lógico OR (`||`) retorna `true` se qualquer um dos operandos for `true`. Caso contrário, retorna `false`.

O operador lógico ou é composto por dois símbolos de pipe: (`||`). Normalmente, ele pode ser encontrado entre as teclas Backspace e Enter.

O padrão abaixo deve parecer familiar aos pontos das passagens anteriores:

```js
if (num > 10) {
  return "No";
}
if (num < 5) {
  return "No";
}
return "Yes";
```

retornará `Yes` apenas se `num` for entre `5` e `10` (5 e 10 incluídos). A mesma lógica pode ser escrita assim:

```js
if (num > 10 || num < 5) {
  return "No";
}
return "Yes";
```

****

## Introduzir instruções else

Quando uma condição para uma instrução `if` for verdadeira, o bloco de código seguinte será executado. E quando a condição for falsa? Normalmente, nada aconteceria. Com uma instrução `else`, um bloco de código alternativo pode ser executado.

```js
if (num > 10) {
  return "Bigger than 10";
} else {
  return "10 or Less";
}
```

****

## Introduzir instruções else if

Se você tem múltiplas condições que precisam ser resolvidas, você pode encadear as instruções `if` junto com instruções `else if`.

```js
if (num > 15) {
  return "Bigger than 15";
} else if (num < 5) {
  return "Smaller than 5";
} else {
  return "Between 5 and 15";
}
```

****

## Usar a ordem lógica em instruções if else

A ordem é importante em instruções `if` e `else if`.

A função é executada de cima para baixo, então você deve ser cuidadoso com qual instrução vem primeiro.

Tomemos como exemplo estas duas funções.

Aqui está a primeira:

```js
function foo(x) {
  if (x < 1) {
    return "Less than one";
  } else if (x < 2) {
    return "Less than two";
  } else {
    return "Greater than or equal to two";
  }
}
```

A segunda apenas altera a ordem das instruções if e else if:

```js
function bar(x) {
  if (x < 2) {
    return "Less than two";
  } else if (x < 1) {
    return "Less than one";
  } else {
    return "Greater than or equal to two";
  }
}
```

Embora as duas funções pareçam praticamente idênticas, se passarmos um número para ambas, teremos saídas diferentes.

```js
foo(0)
bar(0)
```

`foo(0)` retornará a string `Less than one` e `bar(0)` retornará a string `Less than two`.

****

## Encadear instruções if else

Instruções `if/else` podem ser encadeadas por uma lógica complexa. Aqui está o pseudocódigo de várias instruções encadeadas `if`/`else if`:

```js
if (condition1) {
  statement1
} else if (condition2) {
  statement2
} else if (condition3) {
  statement3
. . .
} else {
  statementN
}
```

****

## Selecionar entre várias opções com instruções switch

Se você possui muitas opções pra escolher, use uma instrução switch. Uma instrução `switch` testa um valor e pode ter muitas instruções case as quais definem os diversos valores possíveis. As instruções são executadas desde o primeiro `case` correspondente até que seja encontrado um `break`.

Aqui está um exemplo de uma instrução `switch`:

```js
switch (lowercaseLetter) {
  case "a":
    console.log("A");
    break;
  case "b":
    console.log("B");
    break;
}
```

Valores `case` são testados com o operador de igualdade estrita (`===`). O `break` diz ao JavaScript parar interromper a execução das instruções. Se o `break` for omitido, a próxima instrução case será executada.

****

## Adicionar uma opção padrão em instruções switch

Na instrução `switch`, você não deve ser capaz de especificar todos os possíveis valores como instruções `case`. Ao invés disso, você pode adicionar a instrução `default`, que será executada se nenhuma instrução `case` correspondente for encontrada. Pense nisso como a instrução final `else` em uma cadeia de `if/else`.

A instrução `default` deve ser o último caso.

```js
switch (num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
...
  default:
    defaultStatement;
    break;
}
```

****

## Lidar com várias opções idênticas em instruções switch

Se a instrução `break` for omitida de uma instrução `case` de um `switch`, as instruções `case` seguintes serão executadas até que seja encontrado um `break`. Se você tem várias entradas com a mesma saída, você pode representá-las em uma instrução `switch` da seguinte forma:

```js
let result = "";
switch (val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";
}
```

Todos os casos para 1, 2 e 3 vão produzir o mesmo resultado.

****

## Substituir cadeias de if else por switch

Se você tiver muitas opções para escolher, uma instrução `switch` pode ser mais fácil de escrever do que muitas instruções `if`/`else if` encadeadas. O seguinte:

```js
if (val === 1) {
  answer = "a";
} else if (val === 2) {
  answer = "b";
} else {
  answer = "c";
}
```

pode ser substituído por:

```js
switch (val) {
  case 1:
    answer = "a";
    break;
  case 2:
    answer = "b";
    break;
  default:
    answer = "c";
}
```

****

## Retornar valores booleanos das funções

Você pode se lembrar de [Comparação com o operador de igualdade](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-equality-operator), em que todos os operadores de comparação retornam um valor booleano `true` ou `false`.

Às vezes, as pessoas usam uma instrução `if/else` para fazer uma comparação, dessa forma:

```js
function isEqual(a, b) {
  if (a === b) {
    return true;
  } else {
    return false;
  }
}
```

Mas há uma forma melhor de fazer isso. Já que `===` retorna `true` ou `false`, podemos retornar o resultado da comparação:

```js
function isEqual(a, b) {
  return a === b;
}
```

****

## Retornar o padrão inicial para funções

Quando uma instrução `return` é alcançada, a execução da função atual para e retorna o código para o local da chamada da função.

**Exemplo**

```js
function myFun() {
  console.log("Hello");
  return "World";
  console.log("byebye")
}
myFun();
```

O código acima exibirá no console a string `Hello`, e retorna a string `World`. A string `byebye` nunca vai ser exibida no console, porque a função termina na instrução `return`.

****

## Criar objetos JavaScript

Você talvez tenha ouvido o termo `objeto` antes.

Objetos são similares a `arrays`, exceto que, ao invés de usar índices para acessar e modificar seus dados, você acessa os dados em objetos através do que se chama `propriedades`.

Objetos são úteis para armazenar dados de forma estruturada e podem representar objetos do mundo real, como um gato.

Aqui está um exemplo de objeto gato:

```js
const cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};
```

Neste exemplo, todas as propriedades são armazenadas como strings, como `name`, `legs` e `tails`. Porém, você também pode usar números como propriedades. Você pode até omitir as aspas para propriedades de string com uma única palavra, da seguinte forma:

```js
const anotherObject = {
  make: "Ford",
  5: "five",
  "model": "focus"
};
```

No entanto, se seu objeto tem quaisquer propriedades que não sejam strings, o JavaScript automaticamente definirá seus tipos como strings.

****

## Acessar propriedades de objetos com notação de pontos

Existem duas formas para acessar as propriedades de um objeto: notação de ponto (`.`) e notação de colchetes (`[]`), de forma similar a um array.

Notação de ponto é o que você utiliza quando você sabe o nome da propriedade que você está tentando acessar antecipadamente.

Aqui está um exemplo usando notação de ponto (`.`) para ler uma propriedade do objeto:

```js
const myObj = {
  prop1: "val1",
  prop2: "val2"
};

const prop1val = myObj.prop1;
const prop2val = myObj.prop2;
```

`prop1val` teria o valor `val1` e `prop2val` teria o valor `val2`.

****

## Acessar propriedades de objeto com notação de colchetes

A segunda forma para acessar as propriedades de um objeto é a notação de colchetes (`[]`). Se a propriedade do objeto que você está tentando acessar possui um espaço no seu nome, você precisará usar a notação de colchetes.

No entanto, você ainda pode usar a notação de colchetes nas propriedades dos objetos sem espaços.

Aqui está um exemplo usando a notação de colchetes para ler uma propriedade de um objeto:

```js
const myObj = {
  "Space Name": "Kirk",
  "More Space": "Spock",
  "NoSpace": "USS Enterprise"
};

myObj["Space Name"];
myObj['More Space'];
myObj["NoSpace"];
```

`myObj["Space Name"]` seria a string `Kirk`, `myObj['More Space']` seria a string `Spock` e `myObj["NoSpace"]` seria a string `USS Enterprise`.

Note que os nomes das propriedades com espaços neles precisam estar entre aspas (simples ou duplas).

****

## Acessar propriedades de objetos com variáveis

Outro uso de notação de colchetes em objetos é para acessar a propriedade a qual está armazenada como o valor de uma variável. Isso pode ser muito útil para iterar através das propriedades de um objeto ou quando acessando uma tabela de pesquisa.

Aqui está um exemplo de usar uma variável para acessar uma propriedade:

```js
const dogs = {
  Fido: "Mutt",
  Hunter: "Doberman",
  Snoopie: "Beagle"
};

const myDog = "Hunter";
const myBreed = dogs[myDog];
console.log(myBreed);
```

A string `Doberman` seria exibida no console.

Observe que *não* usamos aspas em torno do nome da variável ao usá-la para acessar a propriedade, porque estamos usando o *valor* da variável, e não o *nome*.

****

## Atualizar propriedades do objeto

Depois de criar um objeto JavaScript, você pode atualizar suas propriedades a qualquer momento, como você atualizaria qualquer outra variável. Você pode usar notação de ponto ou colchete para atualizar.

Por exemplo, vamos dar uma olhada em `ourDog`:

```js
const ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};
```

Como ele é um cachorro particularmente feliz, vamos mudar seu nome para o texto `Happy Camper`. Veja como atualizamos a propriedade name do objeto: `ourDog.name = "Happy Camper";` ou `ourDog["name"] = "Happy Camper";` Agora, quando avaliamos `ourDog.name`, em vez de obter `Camper`, teremos seu novo nome, `Happy Camper`.

****

## Adicionar novas propriedades para um objeto JavaScript

Você pode adicionar novas propriedades para um objeto JavaScript existente da mesma forma pela qual você os modificaria.

Aqui está como adicionaríamos uma propriedade `bark` para `ourDog`:

```js
ourDog.bark = "bow-wow";
```

ou

```js
ourDog["bark"] = "bow-wow";
```

Agora, quando acessamos `ourDog.bark`, nós teremos o seu latido, `bow-wow`.

Exemplo:

```js
const ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

ourDog.bark = "bow-wow";
```

****

## Excluir propriedades de um objeto JavaScript

Podemos também excluir propriedades de objetos dessa forma:

```js
delete ourDog.bark;
```

Exemplo:

```js
const ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"],
  "bark": "bow-wow"
};

delete ourDog.bark;
```

Após a última linha mostrada acima, `ourDog` se parece com:

```js
{
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
}
```

****

## Usar objetos para pesquisas

Objetos podem ser pensados como armazenamento de chave/valor, como um dicionário. Se você tem um dado tabular, você pode usar um objeto para pesquisar valores ao invés de uma instrução `switch` ou uma cadeia de `if/else`. Isso é mais útil quando você sabe que o seu dado de entrada é limitado para um certo intervalo.

Aqui está um exemplo de uma simples pesquisa reversa no alfabeto:

```js
const alpha = {
  1:"Z",
  2:"Y",
  3:"X",
  4:"W",
  ...
  24:"C",
  25:"B",
  26:"A"
};

const thirdLetter = alpha[2];
const lastLetter = alpha[24];

const value = 2;
const valueLookup = alpha[value];
```

`thirdLetter` é a string `Y`, `lastLetter` é a string `C` e `valueLookup` é a string `Y`.

****

## Testar objetos por propriedades

Às vezes, é útil verificar se a propriedade de um determinado objeto existe ou não. Podemos usar o método de objetos `.hasOwnProperty(propname)` para determinar se aquele objeto possui o nome de propriedade fornecido. `.hasOwnProperty()` retorna `true` ou `false` se a propriedade for encontrada ou não.

**Exemplo**

```js
const myObj = {
  top: "hat",
  bottom: "pants"
};

myObj.hasOwnProperty("top");
myObj.hasOwnProperty("middle");
```

O primeiro `hasOwnProperty` retorna `true`, enquanto o segundo retorna `false`.

****

## Manipular objetos complexos

Às vezes, você pode querer armazenar dados em uma Estrutura de Dados flexível. Um objeto JavaScript é uma forma de lidar com dados flexíveis. Eles permitem combinações arbitrárias de strings, numbers, booleans, arrays, functions e objects.

Aqui está um exemplo de estrutura de dados complexas:

```js
const ourMusic = [
  {
    "artist": "Daft Punk",
    "title": "Homework",
    "release_year": 1997,
    "formats": [ 
      "CD", 
      "Cassette", 
      "LP"
    ],
    "gold": true
  }
];
```

Este é um array que contém um objeto dentro dele. O objeto possui vários pedaços de metadados sobre um álbum. Também possui um array aninhado `formats`. Se você quiser adicionar mais álbuns, você pode fazer isso adicionando os discos ao array de alto nível. Objetos armazenam dados em uma propriedade, a qual possui um formato de chave-valor. No exemplo acima, `"artist": "Daft Punk"` é uma propriedade que tem uma chave `artist` e um valor de `Daft Punk`.

**Observação:** você precisará colocar uma vírgula após cada objeto no array, a não ser que ele seja o último objeto no array.

****

## Acessar objetos aninhados

As subpropriedades de objetos podem ser acessadas ao encadear a notação de ponto e de colchetes.

Aqui está um objeto aninhado:

```js
const ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": { 
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};

ourStorage.cabinet["top drawer"].folder2;
ourStorage.desk.drawer;
```

`ourStorage.cabinet["top drawer"].folder2` seria a string `secrets` e `ourStorage.desk.drawer` seria a string `stapler`.

****

## Acessar arrays aninhados

Como vimos em exemplos anteriores, objetos podem conter tanto objetos aninhados quanto arrays aninhados. Semelhante ao acesso de objetos aninhados, a notação de colchetes pode ser encadeada para se acessar arrays aninhados.

Aqui está um exemplo de como se acessar um array aninhado:

```js
const ourPets = [
  {
    animalType: "cat",
    names: [
      "Meowzer",
      "Fluffy",
      "Kit-Cat"
    ]
  },
  {
    animalType: "dog",
    names: [
      "Spot",
      "Bowser",
      "Frankie"
    ]
  }
];

ourPets[0].names[1];
ourPets[1].names[0];
```

`ourPets[0].names[1]` seria a string `Fluffy` e `ourPets[1].names[0]` seria a string `Spot`.

****

## Iterar com laços while em JavaScript

Você pode rodar o mesmo código várias vezes usando um laço.

O primeiro tipo de laço que aprenderemos é chamado de laço `while` porque ele rodará enquanto uma condição específica for verdadeira e vai parar uma vez que a condição não for mais verdadeira.

```js
const ourArray = [];
let i = 0;

while (i < 5) {
  ourArray.push(i);
  i++;
}
```

No código de exemplo acima, o laço `while` executará por 5 vezes e adicionará os números de 0 até 4 a `ourArray`.

Vamos tentar fazer um laço while funcionar empurrando valores para um array.

****

## Iterar com laços for em JavaScript

Você pode rodar o mesmo código várias vezes usando um laço.

O tipo mais comum de laço JavaScript é chamado de laço `for`, porque ele é executado por um número especificado de vezes.

Laços for são declarados com três expressões opcionais separadas por ponto e vírgula:

`for (a; b; c)`, onde `a` é a declaração de inicialização, `b` é a declaração de condição, e `c` é a expressão final.

A declaração de inicialização é executada apenas uma vez antes de o laço iniciar. Normalmente, é usada para definir e configurar sua variável de laço.

A declaração de condição é verificada no início de cada iteração do laço e vai continuar enquanto seu valor for `true`. Quando a condição for `false` no início da iteração, o laço vai parar de executar. Isso significa que se a condição de início for falsa, seu laço nunca será executado.

A expressão final é executada no final de cada iteração do laço, antes da verificação da próxima condição e normalmente é usada para incrementar ou decrementar o contador do laço.

No exemplo a seguir, inicializamos com `i = 0` e iteramos enquanto nossa condição `i < 5` for verdadeira. Nós incrementaremos `i` em `1` em cada iteração do laço com `i++` como nossa expressão final.

```js
const ourArray = [];

for (let i = 0; i < 5; i++) {
  ourArray.push(i);
}
```

`ourArray` agora terá o valor de `[0, 1, 2, 3, 4]`.

****

## Iterar números ímpares com um laço for

Laços for não tem de iterar um de cada vez. Ao alterar nossa `final-expression`, nós podemos contar os números pares.

Começaremos em `i = 0` e um laço while `i < 10`. Incrementaremos `i` em 2 a cada iteração com `i += 2`.

```js
const ourArray = [];

for (let i = 0; i < 10; i += 2) {
  ourArray.push(i);
}
```

`ourArray` agora conterá `[0, 2, 4, 6, 8]`. Vamos mudar nossa `initialization` para que possamos contar por números ímpares.

****

## Contar pra trás com um laço for

Um laço for também pode contar pra trás, contanto que possamos definir as condições certas.

Para decrementar em dois cada iteração, nós precisamos alterar nossa inicialização, condição e expressão final.

Nós começaremos em `i = 10` e vamos iterar enquanto `i > 0`. Nós decrementamos `i` por dois em cada iteração com `i -= 2`.

```js
const ourArray = [];

for (let i = 10; i > 0; i -= 2) {
  ourArray.push(i);
}
```

`ourArray` agora vai conter `[10, 8, 6, 4, 2]`. Vamos mudar nossa inicialização e expressão final para que possamos contar para trás em dois para criar um array de números ímpares decrescentes.

****

## Iterar através de um array com laço for

Uma tarefa comum em JavaScript é para iterar através do conteúdo de um array. Uma forma de fazer isso é com um laço `for`. Esse código vai exibir cada elemento do array `arr` no console:

```js
const arr = [10, 9, 8, 7, 6];

for (let i = 0; i < arr.length; i++) {
   console.log(arr[i]);
}
```

Lembre-se de que arrays têm indexação baseada em zero, o que significa que o último índice do array é de `length - 1`. Nossa condição para esse laço é `i < arr.length`, que interrompe o laço quando `i` é igual a `length`. Nesse caso a última iteração é `i === 4`, ou seja, quando `i` se tornar igual a `arr.length - 1` e exibir `6` no console. Em seguida, `i` aumenta para `5`, e o laço é interrompido porque `i < arr.length` é `false`.

****

## Aninhar laços for

Se você possui um array multidimensional, você pode usar a mesma lógica no ponto de passagem anterior para iterar através de arrays e de qualquer sub-array. Exemplo:

```js
const arr = [
  [1, 2], [3, 4], [5, 6]
];

for (let i = 0; i < arr.length; i++) {
  for (let j = 0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
```

Isso exibe no console cada subelemento dentro de `arr`, um de cada vez. Note que para o laço interno, nós estamos verificando a propriedade `.length` de `arr[i]`, desde que `arr[i]` também seja um array.

****

## Iterar com laços do...while em JavaScript

O próximo tipo de laço que você aprenderá é chamado de laço `do...while`. O laço `do...while` é chamado assim porque primeiro fará algo (`do`) ou executará algo uma vez dentro do bloco de código, não importando o que acontecer. Em seguida, continuará a executar o laço enquanto (`while`) a condição for `true`.

```js
const ourArray = [];
let i = 0;

do {
  ourArray.push(i);
  i++;
} while (i < 5);
```

O exemplo acima se comporta de forma similar a outros tipos de laços, e o array resultante se parecerá com `[0, 1, 2, 3, 4]`. No entanto, o que torna o laço `do...while` diferente de outros laços é como ele se comporta quando uma condição falha na primeira verificação. Vamos ver isso na prática. Aqui está um laço comum `while` que rodará o código no laço enquanto `i < 5`:

```js
const ourArray = []; 
let i = 5;

while (i < 5) {
  ourArray.push(i);
  i++;
}
```

Nesse exemplo, inicializamos o valor de `ourArray` como um array vazio e o valor de `i` sendo 5. Quando executamos o laço `while`, a condição é igual a `false` porque `i` não é menor que 5, portanto nós não executamos o código dentro do laço. O resultado é que `ourArray` terminará sem valores adicionados a ele, e ainda se parecerá com `[]` quando todas as linhas do código no exemplo acima forem completamente executadas. Agora, dê uma olhada no laço `do...while`:

```js
const ourArray = []; 
let i = 5;

do {
  ourArray.push(i);
  i++;
} while (i < 5);
```

Nesse caso, nós inicializamos o valor de `i` para 5, assim como fizemos com o laço `while`. Quando chegamos na próxima linha, não há condição a ser analisada, então nós vamos ao código dentro das chaves e o executamos. Nós adicionaremos um único elemento ao array e então incrementamos `i` antes de chegarmos à verificação da condição. Quando nós finalmente temos o resultado da condição `i < 5` na última linha, nós notamos que `i` agora é 6, o que não cumpre a verificação da condição, então nós saímos do laço e terminamos. Ao final do exemplo acima, o valor de `ourArray` é `[5]`. Essencialmente, um laço `do...while` garante que o código dentro do laço será executado pelo menos uma vez. Vamos tentar fazer um laço `do...while` funcionar inserindo valores em um array.

****

## Substituir laços usando recursão

Recursão é o conceito de que uma função pode ser chamada por ela mesma. Para ajudar a entender isso, comece a pensar sobre a seguinte tarefa: multiplique os primeiros `n` elementos de um array para criar o produto desses elementos. Usando um laço `for`, você poderia fazer isso:

```js
  function multiply(arr, n) {
    let product = 1;
    for (let i = 0; i < n; i++) {
      product *= arr[i];
    }
    return product;
  }
```

No entanto, note que `multiply(arr, n) == multiply(arr, n - 1) * arr[n - 1]`. Isso significa que você pode reescrever `multiply` dentro da própria função e nunca precisar usar um laço.

```js
  function multiply(arr, n) {
    if (n <= 0) {
      return 1;
    } else {
      return multiply(arr, n - 1) * arr[n - 1];
    }
  }
```

A versão recursiva de `multiply` fica dessa forma. No caso de base, onde `n <= 0`, ele retorna 1. Para valores maiores de `n`, a função chama a si mesma, mas com `n - 1`. Essa chamada da função é avaliada da mesma forma, chamando `multiply` novamente até que `n <= 0`. Nesse ponto, todas as funções podem retornar e a função `multiply` original retorna a resposta.

**Observação:** funções recursivas precisam ter um caso de base quando elas retornam sem chamar a função novamente (nesse exemplo, quando `n <= 0`), caso contrário, elas nunca vão parar de executar.

****

## Gerar frações aleatórias com JavaScript

Números aleatórios são úteis para criar comportamento aleatório.

JavaScript tem a função `Math.random()` que gera um número decimal aleatório entre `0` (incluso) e `1` (excluso). Assim, `Math.random()` pode retornar um `0` mas nunca retornará `1`.

**Observação:** como ao [armazenar valores com operador de atribuição](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/storing-values-with-the-assignment-operator), todas as chamadas de funções serão resolvidas antes de executar o `return`, para que possamos dar ao `return` o valor da função `Math.random()`.

****

## Gerar números inteiros aleatórios com JavaScript

É ótimo podermos gerar números decimais aleatórios, mas é ainda mais útil se usarmos isso para gerar números inteiros aleatórios.

1. Use `Math.random()` para gerar um decimal aleatório.
2. Multiplique o decimal aleatório por `20`.
3. Use outra função, `Math.floor()` para arredondar o número para baixo para o número inteiro mais próximo.

Lembre-se de que `Math.random()` pode nunca retornar um `1` e, por estarmos arredondando, é impossível também receber `20`. Essa técnica nos dará um número inteiro entre `0` e `19`.

Juntando tudo, é assim que nosso código se parece:

```js
Math.floor(Math.random() * 20);
```

Nós estamos chamando `Math.random()`, multiplicando o resultado por 20, e em seguida passando o valor para a função `Math.floor()` para arredondar o valor para o número inteiro mais próximo abaixo.

****

## Gerar números inteiros aleatórios dentro de um intervalo

Ao invés de gerar um número inteiro aleatório entre 0 e um número especificado, como fizemos anteriormente, nós podemos gerar um número inteiro aleatório que fica em um intervalo entre dois números especificados.

Para isso, definiremos um número mínimo `min` e um número máximo`max`.

Aqui está a fórmula que usaremos. Leve um momento para ler e entender o que esse código está fazendo:

```js
Math.floor(Math.random() * (max - min + 1)) + min
```

****

## Usar a função parseInt()

A função `parseInt()` analisa uma string e retorna um inteiro. Exemplo:

```js
const a = parseInt("007");
```

A função acima converte a string `007` para o inteiro `7`. Se o primeiro caractere na string não pode ser convertido em um número, então ele retorna `NaN`.

****

## Usar a função parseInt com um radix

A função `parseInt()` analisa uma string e retorna um inteiro. É preciso um segundo argumento para o radix, que especifica a base do número na string. O radix pode ser um inteiro entre 2 e 36.

A chamada da função se parece com:

```js
parseInt(string, radix);
```

Exemplo:

```js
const a = parseInt("11", 2);
```

A variável radix diz que `11` está no sistema binário, ou base 2. Esse exemplo converte a string `11` para um inteiro `3`.

****

## Usar o operador condicional (ternário)

O operador condicional, também chamado de operador ternário, pode ser usado como uma expressão if-else de uma linha.

A sintaxe é `a ? b : c`, onde `a` é a condição, `b` é o código executado quando a condição retorna `true` e `c` é o código executado quando a condição retorna `false`.

A função a seguir usa a instrução `if/else` para verificar uma condição:

```js
function findGreater(a, b) {
  if(a > b) {
    return "a is greater";
  }
  else {
    return "b is greater or equal";
  }
}
```

Isto pode ser reescrito usando o operador condicional:

```js
function findGreater(a, b) {
  return a > b ? "a is greater" : "b is greater or equal";
}
```

****

## Usar operadores de múltiplas condições (ternários)

No desafio anterior, você usou um único operador condicional. Você também pode encadear eles juntos para verificar por múltiplas condições.

A seguinte função usa as instruções `if`, `else if` e `else` para verificar múltiplas condições:

```js
function findGreaterOrEqual(a, b) {
  if (a === b) {
    return "a and b are equal";
  }
  else if (a > b) {
    return "a is greater";
  }
  else {
    return "b is greater";
  }
}
```

A função acima pode ser rescrita usando operadores de múltiplas condições (operador ternário):

```js
function findGreaterOrEqual(a, b) {
  return (a === b) ? "a and b are equal" 
    : (a > b) ? "a is greater" 
    : "b is greater";
}
```

É considerada a melhor prática para formatar operadores de múltiplas condições, já que cada condição está em uma linha separada, como mostrado acima. Usar operadores de múltiplas condições sem a indentação adequada pode dificultar a leitura do seu código. Por exemplo:

```js
function findGreaterOrEqual(a, b) {
  return (a === b) ? "a and b are equal" : (a > b) ? "a is greater" : "b is greater";
}
```
