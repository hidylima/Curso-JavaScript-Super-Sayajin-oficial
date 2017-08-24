# Aula 2 - Utilizando nossas operações




## Desafio

Criar a função de divisão utilizando apenas a função de soma, <br>
onde ela receba 2 valores inteiros e consiga retornar um <br>
valor decimal. Por exemplo: `5 / 2 = 2.5`

Além disso explique como dois valores do conjunto dos Números Naturais<br>
transformou-se em um valor que não está contido nesse grupo e qual o grupo que ele pertence.

> **Lembrando que a ÚNICA função aceita dentro da divisão será a da soma!**


## Exponenciação e Radiciação

![Exponenciação](http://mundoeducacao.bol.uol.com.br/upload/conteudo_legenda/ba789adb96c654e9c0d7c4d9ee79496f.jpg)

Como você já deve saber a exponenciação é a função inversa da radiciação<br>
e vice-versa e as derivam da multiplicação e divisão.

Então vamos parar de enrolar e criar nossa função de exponenciação (`pow`).


```js
const pow = ( y ) => ( x ) =>
  Math.pow( x, y )
```

Claramente você percebeu que estamos usando a função [`Math.pow`](http://mdn.io/pow), <br>
que é nativa do JavaScript, caso queira saber mais *click* no *link* acima.

Nesse caso nossa função `pow` recebe primeiramente seu expoente `y` e depois<br>
sua base `x`



## Aplicação

Imagine que temos um *Array* de Objetos e precisamos antes de somar<br>
os salários retirar 10% do valor de cada um e depois fazer uma média.

```js

const workers = [ 1000, 2500 , 10000 ]

const withdraw = ( list, percent ) => {

  let counter = 0
  let newList = []

  while ( counter < list.length) {
    const percentValue = list[ counter ] * ( percent / 100 )
    const newSalary = list[ counter ] - percentValue

    newList[ counter ] = newSalary 
    counter++
  }

  return newList
}

console.log( 'New Salaries: ', withdraw( workers, 10 ) )

```

No código acima nós apenas criamos um *Array* novo com os valores<br>
dos valores calculados pela nossa função

```js

const workers = [ 1000, 2500 , 10000 ]

const sumAll = ( list, percent ) => {

  let counter = 0
  let total = 0

  while ( counter < list.length) {
    const percentValue = list[ counter ] * ( percent / 100 )
    const newSalary = list[ counter ] - percentValue

    total += newSalary 
    counter++
  }

  return total
}

console.log( 'Sum of Salaries: ', sumAll( workers, 10 ) )

```

### Lembrete 1

> Percebeu que não criamos **funções** porém não criamos nenhuma constante <br>
> para os valores que passaremos como parâmetro?

Isso se deve graças a dois conceitos que são obrigatórios para uma linguagem <br> estar contida no Paradigma Funcional:

- [First-class Function]()
- [High-Order Function]()

**Falarei melhor sobre esses conceitos na próxima aula!**