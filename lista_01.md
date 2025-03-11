# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
a) A saída será undefined seguido de erro 

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

- Resposta: alternativa "a".
- Justificativa: A primeira saída será "undefined" pois a varíavel "x" ainda não possuía um valor quando o método "console.log(x)" foi chamado, apesar de já poder ser acessada por ser um "var". Já a segunda saída será erro, pois a varíavel "y" ainda não havia sido declarada quando o método "console.log(y)" foi chamado, e, por ser uma variável "let", ainda não existia nesse ponto, causando assim um erro.


**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

- Resposta: alternativa "a".
- Justificativa: o código pretende retornar um erro caso o usuário tente inserir o valor 0 para um dos parâmetros da função "soma(a, b)", portanto, para verificar esse caso, a condição inserida na estrutura "if" deve verificar se um dos parâmetros, ou os dois, vale 0, de forma que apenas a alternativa "a" apresenta a resolução correta para obter esse resultado. 

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200.

c) O código imprime 50.

d) O código gera um erro.

- Resposta: alternativa "b".
- Justificativa: apesar do parâmetro inserido ser "eletrônico", cujo preço indicado é 1000, há um erro na estrutura do case, pois não há um "break" após o case "eletrônico" ser verificado, dessa forma, o próximo case é verificado e o valor de "preco" é atualizado.

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

d) 24

- Resposta: alternativa "d".
- Justificativa: vários métodos são aplicados sobre a lista "numeros" para criar a varíavel resultado, sendo eles ".map(x => x * 2), que cria uma nova lista com todos os valores contidos em "numeros" dobrados [2, 4, 6, 8, 10], ".filter(x => x > 5)", que cria uma nova lista onde são mantidos apenas os valores maiores que 5 [6, 8, 10], e ".reduce((a, b) => a + b, 0)", que, por fim, soma todos os elementos da nova lista criada, de modo a retornar 24.
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

- Resposta: alternativa "c".
- Justificativa: o método ".splice(1, 2, "abacaxi", "manga")" adicona a partir do index 1 da lista 2 novos elementos que substituem os antigos, sendo assim, os valores "maça" e "uva" são trocados por "abacaxi" e "manga".  
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

- Resposta: alternativa "b".
- Justificativa: a segunda afirmativa não justifica a primeira pois corresponde apenas a forma como a herança é implementada, e não as suas funcionalidades.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

- Resposta: alternativa "a".
- Justificativa: a afirmativa III é falsa pois o JavaScript suporta, sim, herança de classes, o que é explicitado nas afirmativas I e II que demonstram ações que são possíveis por meio da herança de classe.

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção

- Resposta: alternativa "b".
- Justificativa: apesar do conceito de sobrecarga de métodos existir, não é possível aplicá-lo de modo tradicional no JavaScript, sendo assim, a razão é falsa, contudo, a asserção está correta e define corretamente o conceito de polimorfismo.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```
- Resolução:
```javascript
function somaArray(numeros) {
    let soma = 0; // Declara a variável soma antes de utilizá-la
    for (let i = 0; i < numeros.length; i++) { // Itera a lista de acordo com o tamanho dela
        soma += 2 * numeros[i]; // Soma ao valor de "soma" o dobro de cada elemento da lista
    }
    return soma; // Retorna o valor final da soma de todos elementos
}
console.log(somaArray([1, 2, 3, 4])); // Mostra no console o resultado da função aplicada à lista definida
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.
