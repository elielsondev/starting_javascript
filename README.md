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

```
let mes = 'maio';
let estacaoDoAno = '?';

switch (mes) {
    case 'janeiro':
    case 'fevereiro':
    case 'março':
        estacaoDoAno = 'Verão';
        break;
    case 'abril':
    case 'maio':
    case 'junho':
        estacaoDoAno = 'Outono';
        break;
    case 'julho':
    case 'agosto':
    case 'setembro':
        estacaoDoAno = 'Inverno';
        break;
    case 'outubro':
    case 'novembro':
    case 'dezembro':
        estacaoDoAno = 'Primavera';
}

console.log(estacaoDoAno); // Outono
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
```
console.log(!true); // false
console.log(!false); // true
```

Conheça mais sobre o `!` clique no link: [Logical NOT !](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_NOT)
_________
##### Saiba mais: [Operadores](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators)

_________
**Array**
[Assistir Vídeo](https://www.youtube.com/watch?v=lXsKBDhixXQ)

*Os `Arrays` podem receber tanto valores do mesmo tipo, como também de tipos ditintos*

Exemplo:
```
let fruits = ['apple', 'banana', 'papaya', 'strawberry'];

let myList = ['go', 2022, true, undefined, null];

```
Conheça algumas das possibilidades mais utilizadas para manipular arrays.[Conheça](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Array)
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
>for/in
```
let cars = ['Saab', 'Volvo', 'BMW'];

for (let index in cars) {
  console.log(cars[index]);
}

// Saab
// Volvo
// BMW
```
Um outro exemplo é a iteração nas chaves de um objeto:
```
let car = {
  type: 'Fiat',
  model: '500',
  color: 'white',
};

for (let index in car) {
  console.log(index, car[index]);
}

// type Fiat
// model 500
// color white
```

>for/of
```
let food = ['hamburguer', 'bife', 'acarajé'];
for (let value of food) {
  console.log(value);
};

// hamburguer
// bife
// acarajé
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

_________
**While**
##### ⚠️ Tenha muito cuidado! É fácil causar loops infinitos utilizando o while!

*Ao contrário do for, o while executa a iteração com apenas uma condição. Enquanto essa condição for verdadeira o conteúdo de escopo do while vai sendo cumprido e ao encontrar uma condição falsa o bloco é então encerrado. Por exemplo:*
```
let counter = 0;

while(counter !== 5) {
  counter += 1;
}

```
Neste caso o while irá rodar até que a variável counter alcance o valor 5. Mas e se o valor inicial fosse 6, o que aconteceria?

Ele entraria em um loop infinito, e provavelmente travaria o computador. Para então não termos esse problema é importante nos certificarmos do valor inicial que será atribuído.

###### 💡 Dica: com o comando break é possível também encerrar o loop while quando assim desejar. [Veja um exemplo aqui](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/break#exemplos)

Saiba mais: Há outras maneiras de iterarmos sobre uma operação, utilizando o do…while, se quiser saber mais, [veja aqui](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/do...while)

__________
**Object**

*A classe `Object` representa um dos tipos de dados do JavaScript. É usado para armazenar várias coleções de chaves e entidades mais complexas*
```
const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```
__________
**Functions**
[Assistir Vídeo](https://www.youtube.com/watch?v=lXsKBDhixXQ)

*Cada função JavaScript é na verdade um objeto `Function`, ou seja é uma estrutura de dados criada para uma 'função' designada a ela.*

No exemplo a seguir vamos criar uma função simples que retorna a soma de dois valores passados por parametros.

```
function soma (n1, n2) {
  return n1 + n2;
}

console.log(soma(10, 20));
```

`Atenção!!! Pesquise mais  a fundo cada tópico abordado aqui e principalmente sobre funções, pois o conhecimento sobre essas ferramentas são muito importantes para iniciar sua carreira em JavaScript, de coração lhe desejo sucesso futuro DEV.`

## JavaScript ES6 - Template literal, Arrow function, Ternary operator
**Template literal
```
// Sem template literal

const name = 'Elielson';
console.log('Olá' + ' ' + name + '!')
```

```
// Com template literal

const name = 'Elielson';
console.log(`Olá ${name}!`)
```

**Arrow function**
```
// Sem arrow function
function userName() {
  const name = 'Elielson';
  return name;
}

console.log(userName());
```
```
// Com arrow function
const userName = () => { 
const name = 'Elielson';
return name;
};

console.log(userName());
```

**Ternary operator**
```
let colorSky = 'azul';

colorSky === 'azul' ? console.log('verdadeiro') : console.log('falso');
```

> Dica de Ouro: Consultar a [documentação](https://developer.mozilla.org/en-US/docs/Web/JavaScript) é o segredo para um bom aprendizado.
