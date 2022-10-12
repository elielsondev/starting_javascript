# Starting JavaScript

_________
### JavaScript Basics => [Documentation](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics)

_________
**Variáveis & Constantes.**

*Tanto váriáveis quanto constantes servem para armazenar valores, porém a diferença entre eles é que:*


>As 'Variáveis, como o próprio nome sugere pode ter o seu valor alterado/variar:

<h6><em> OBS: Neste no exemplo de variável estamos usando o `var`, porém podemos usar o `let`, que pra falar a verdade 
é o mais recomendado, por motivos que não iremos abordar aqui no momento. </em></h6>

```
var name = 'Elielson';
var age = 32;
```

>Já a constante, após ter o seu valor definido não pode ser alterado (valor constante):
```
const yearOfBirth = 1990; 
```
_________
**Tipos primitivos.**

[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

Exemplo:
```
let name = 'Elielson';
typeof name; //'string'
```

[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

Exemplo:
```
let age = 32;
typeof age; // number
```

[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)

Exemplo:
```
let english = false;
typeof english; //boolean
```
[Undefined](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Undefined)

Exemplo:
```
let item;
typeof item; //undefined
```

[Null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Null)
Exemplo:
```
let foo = null;
typeof foo; //null
```
_________
**Operadores aritméticos.**
 >Soma `+` <br />
 >Subtração `-` <br />
 >Multiplicação `*` <br />
 >Divisão `/` <br />
 >Exponenciação `**` <br />
 >Módulo `%` <br />
 >Incremento `++` (+1) <br />
 >Decremento `--` (-1) <br />

_________
**Estruturas condicionais como if/else e switch/case.**

Vamos imaginar as condições possíveis para um semáforo em funcionamento para demonstrar tanto o `if/else` e também o `switch/case`:
>`IF/ELSE`:
```
let statusSignal = 'amarelo';

if (statusSignal === 'verde') {
  console.log('Siga!')
} else if (statusSignal === 'amarelo') {
  console.log('Pense!')
} else {
  console.log('Pare!')
}
```

>`SWITCH/CASE`:
```
let statusSignal = 'vermelho';

switch(statusSignal) {
  case 'verde':
    console.log('Siga!');
    break;
  case 'amarelo':
    console.log('Pense!')
    break;
  case 'vermelho':
    console.log('Pare!')
    break;
  default:
    console.log('Semáforo fora de sinal')
    break;
}
```
_________
**Operadores lógicos**

>AND `&&` Só retorna true apenas quando as duas condições forem verdadeiras.
```
console.log(true && true); // true
console.log(true && false); // false
console.log(false && true); // false
console.log(false && false); // false
```
Conheça mais sobre o `&&` clique no link:[Logical AND &&](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND)

>OR `||` Só retorna falso quando ambas condições forem falsas.
```
console.log(true || true); // true
console.log(true || false); // true
console.log(false || true); // true
console.log(false || false); // false
```
Conheça mais sobre o `||` clique no link:[Logical OR ||](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_OR)

>NOT `!` Ele é capaz de inverter o valor booleano de um elemento.

Conheça mais sobre o `!` clique no link: [Logical NOT !](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_NOT)
_________
##### Saiba mais: [Operadores](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators)

_________
**Array**

*Os `Arrays` podem receber tanto valores do mesmo tipo, como também de tipos ditintos*

Exemplo:
```
let fruits = ['apple', 'banana', 'papaya', 'strawberry'];

let myList = ['go', 2022, true, undefined, null];

```
Conheça mais sobre o `Array` clique no link: [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Array)
_________
**For**

*O `For` cria loops, obedecendo alguns parametros da sua sintaxe*

>For
```
let myList = [ 'paper', 'rice', 'car', 'beach', 'house', 'blue'];

for (let index = 0; index < myList.length; index +=1) {
  console.log(myList[index])
}

// paper
// rice
// car
// beach
// house
// blue
```
```
for (let index = 1; index <= 10; index += 1) {
  let number = 9;
  console.log(number * index)
};

// 9
// 18
// 27
// 36
// 45
// 54
// 63
// 72
// 81
// 90
```
>for/of
```
let numeros = [1,2,3,4,5];
for(let numero of numeros) {
  console.log(numero);
}

//1
//2
//3
//4
//5
```

```

let word = 'Hello';
for (let letter of word) {
  console.log(letter);
}

// "H"
// "e"
// "l"
// "l"
// "o"
```
__________
**Object**

*A classe `Object` representa um dos tipos de dados do JavaScript. É usado para armazenar várias coleções de chaves e entidades mais complexas*
```
const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```
__________
**Functions**

*Cada função JavaScript é na verdade um objeto `Function`, ou seja é uma estrutura de dados criada para uma 'função' designada a ela.*

No exemplo a seguir vamos criar uma função simples que retorna a soma de dois valores passados por parametros.

```
function soma (n1, n2) {
  return n1 + n2;
}

console.log(soma(10, 20));
```

`Atenção!!! Pesquise mais  a fundo cada tópico abordado aqui e principalmente sobre funções, pois o conhecimento sobre essas ferramentas são muito importantes para iniciar sua carreira em JavaScript, de coração lhe desejo sucesso futuro DEV.`

> Dica de Ouro: Consultar a [documentação](https://developer.mozilla.org/en-US/docs/Web/JavaScript) é o segredo para um bom aprendizado.
