author:            Davidson Castro Orlando Souto
summary:           Programa de estágio do Banco Inter
id:                estagio
categories:        javascript
environments:      web
status:            draft
feedback link:     github.com/mariopce
analytics account: 0

# Inter estágio

## Introdução
Duration: 3:00

Este será o seu guia para construção do desafio. O primeiro e mais importe ponto é:
* Relaxe, todos nós já estivemos na sua situação, e sabemos o quão dificil é, então procurem se divertir e lembrem-se que errar faz parte do aprendizado. 
* Nós temos diversas vagas, então não se preocupem com a competição. Deêm o seu melhor.
* No seu ambiente de trabalho o sucesso é e sempre será resultado de um trabalho em equipe!!!
* No decorrer deste guia vocês poderão encontrar novos termos, mas não se preucupem, pois não esperamos que vocês já os conheçam. O próprio guia irá desmistificá-los e vocês podem pedir ajuda a qualquer momento.

Bora para a parte prática!!! O desafio possui duas partes, uma de desenvolvimento e outra de criação/especificação.
O segredo é dividir para conquistar!!!

O que iremos utilizar:

* Internet
* Firebase
* Javascript
* Html
* Css
* Visual code
* Node(npm)
* Papel e caneta


## Desafio
Duration: 3:00

* Vocês irão construir um novo produto para o Banco Inter, chamado Inter Viagens. Este produto oferecerá diversas funcionalidades relacionadas à viagens aéreas.

* O desenvolvimento de software morderno é realizado de forma incremental, ou seja, criamos pequenas versōes funcionais do nosso produto que agregue valor para nossos clientes.

Positive 
: Não é necessário ter todo o produto desenvolvido/especificado para lancá-lo.

* A primeira versão funcional do nosso produto será a construção de um buscador de passagens aéreas. Vocês irão desenvolver esta parte.

Negative
: Não é necessário que a primeira versão esteja concluída para começarmos a especificar a segunda fase do nosso produto.

* Como sugestão, vocês deverão criar um programa de fidelidade para o Inter Viagens (Exemplos: Smiles, Km de vantagem, Clube azul).

Para documentar os requisitos levantados, poderão utilizar recursos como:

*  Estória de usuário - Descrição simples da necessidade, sob o ponto de vista do usuário.

O que é Estória de usuário [usuário?](http://blog.myscrumhalf.com/2011/10/user-stories-o-que-sao-como-usar)

O que é um critério de [aceitação](http://blog.myscrumhalf.com/2011/10/criterios-de-aceitacao-das-user-stories)

* Diagramas - Diagrama de atividade, sequência, etc.

* Protótipos - Protótipos de tela.


## A primeira estória
Duration: 3:00

Buscar passagens:

Eu como cliente desejo buscar passagens aéreas para facilitar o meu dia a dia na compra de passagens.

Critérios de aceitação:
* O cliente deverá informar o aeroporto de origem.
* O cliente deverá informar o aeroporto de destino.
* Após a busca o sistema deverá exibir para o cliente o resultado da mesma.


Dicas: 
* A segunda fase do nosso projeto já pode ser iniciada!!!
* Esta é provavelmente a primeira estória de usuário que vocês viram na vida. Não se preucupem com a perfeiçao, o ótimo é inimigo do bom.
* Para as pessoas que irão construir a especificação, deêm uma olhada no último item deste guia "Bonus".


## O desenvolvimento
Duration: 3:00

Lembrem-se: A internet poderá ser utilizada a qualquer momento.



* Como já dito, html e javascript serão utilizados para o desenvolvimento do nosso produto.
* O firebase será utilizado para hostear a aplicação e também como base de dados.


Positive
: O Firebase é uma plataforma de desenvolvimento de aplicativos para dispositivos móveis e da Web desenvolvida pela Firebase, Inc. em 2011 e adquirida pelo Google em 2014.


* [Acessar](https://firebase.google.com/?hl=pt-br) ( Caso vocês não possuam uma conta no google, chegou o momento haha!)

* Ir para o console ![Console firebase](https://github.com/DaviCastro/viagens/blob/master/img/1.png?raw=true)

* Criar um novo projeto.

## Configuracao Ambiente
Duration: 3:00

* Abra o powerShell do windows.
* Aqui utilizaremos o gerenciador de dependências do node o npm.

Positive
: Node.js é uma plataforma construída sobre o motor JavaScript do Google Chrome para facilmente construir aplicações de rede rápidas e escaláveis. 

* Verificar se o node está instalado.

``` javascript
npm help
```

* Verificar se o  utilitário de linha de comando do firebase está instalado.

``` javascript
firebase help
```

* Caso o firebase não esteja instalado. 

``` javascript
npm install -g firebase-tools
```

* Acesse o firebase, clique em hosting e siga o tutorial.

* Basicamente

``` javascript
firebase login
```

``` javascript
firebase init
```

``` javascript
firebase deploy
```

Ao rodar o commando firebase init vocês deverão selecionar "Database e Hosting" e isto irá criar um projeto inicial. O terminal permitirá que vocês selecionem o projeto desejado.
Quando o terminal solicitar "Configure as a single-page app", selecione "y".

* Após rodar o comando deploy o projeto será hostiado no firebase. Vocês poderão conferir acessando hosting e clicando no dominio.

![Deploy](https://github.com/DaviCastro/viagens/blob/master/img/2.png?raw=true)

## Configurando Dependências
Duration: 3:00 

* Acessar a pasta public do seu projeto. 
* Abrir o arquivo index e alterar conforme [link](https://gitlab.com/snippets/1754760). O html no link disponibilizado é apenas para auxílio, não precisa ser necessariamente seguido. Este index.html já está configurado com as dependências do firebase e bootstrap.
* O bootstrap é totalmente opcional.

Para facilitar a busca do nosso cliente utilizaremos um componente de autoComplete. Vocês não precisarão desenvolver este componente, apenas utilizá-lo.

Vocês deverão criar um arquivo chamado autoComplete.js e autoComplete.css.

* [Acesse](https://gitlab.com/snippets/1754761) para pegar o conteúdo do arquivo autoComplete.js

* [Acesse](https://gitlab.com/snippets/1754762) para pegar o conteúdo do arquivo autoComplete.css

* Adicionar o autoComplete.js e autoCompletye.css no index.html
 

## Configurando o Banco de Dados
Duration: 3:00

* Utilizaremos um recurso extremamente interessante do firebase: o seu banco de dados em tempo real.

Positive
: O Firebase Realtime Database é um banco de dados hospedado na nuvem, em que os dados são armazenados como JSON e sincronizados em tempo real com todos os clientes conectados. Quando você cria apps em plataformas cruzadas com nossos SDKs para iOS, Android e JavaScript, todos os clientes compartilham uma instância do Realtime Database e recebem automaticamente atualizações com os dados mais recentes.

1. Acesse o firebase e clique em database
2. Escolha Realtime database 

![Banco de dados](https://github.com/DaviCastro/viagens/blob/master/img/3.png?raw=true)

Criamos uma pequena base de dados para vocês. Segue o link do json a ser importado no [firebase](https://gitlab.com/snippets/1754772)

Positive 
: JSON (JavaScript Object Notation) é um modelo para armazenamento e transmissão de informações no formato texto. Apesar de muito simples, tem sido bastante utilizado por aplicações Web devido a sua capacidade de estruturar informações de uma forma bem mais compacta do que a conseguida pelo modelo XML, tornando mais rápido o parsing dessas informações. Isto explica o fato de o JSON ter sido adotado por empresas como Google e Yahoo, cujas aplicações precisam transmitir grandes volumes de dados.

## Construindo a aplicação
Duration: 3:00

O desenvolvimento será feito praticamente na sua totalidade utilizando dois arquivos, o index.html e o main.js (ops ainda criamos o segundo).

* Criar um arquivo chamado main.js e importar o mesmo no index.html

Para nossa aplicação funcionar integrada ao firebase precisamos de algumas configurações.

* O firebase suporta aplicações web, android e ios, no nosso caso vamos selecionar web.

![Web App](https://github.com/DaviCastro/viagens/blob/master/img/4.png?raw=true)

Será necessária a utilizaçaão do código que o firebase fornecerá. Vocês deverão criar uma função dentro do arquivo main.js com este código.

![Código Firebase](https://github.com/DaviCastro/viagens/blob/master/img/5.png?raw=true)


* Seguem abaixo exemplos de como criar uma function utilizando a nova versão do javascript (se não ficar claro como utilizar, o google está sempre ai).

```javascript

// Definição de uma função
const interHelloWordFuncaoSoma = (x, y) => {
  return x + y
}

const interHelloWordFuncao = () => {
  console.log('Hello World');
}

//Executando a função
interHelloWordFuncaoSoma(1, 2) // 3

interHelloWordFuncao(); // Hello World

```

* O browser utiliza o DOM para renderizar os componentes.

Positive
: Então, o que é o DOM? O DOM (Document Object Model) é uma interface que representa como os documentos HTML e XML são lidos pelo seu browser. Após o browser ler seu documento HTML, ele cria um objeto que faz uma representação estruturada do seu documento e define meios de como essa estrutura pode ser acessada. Nós podemos acessar e manipular o DOM com JavaScript, é a forma mais fácil e usada.Existem diversos detalhes relacionados ao DOM, mas o mais importe por hora é que normalmente precisamos esperar o browser carregar o DOM antes de comecarmos a manipular o mesmo.

* Segue o código que poderá auxiliar neste processo. 

```javascript
document.onreadystatechange = () => {
    if (document.readyState === 'complete') {
        //Colocar código que será executado após o DOM terminar de carregar.
    }
};
```


Dicas: 
* Utilizem o máximo possīvel de funcões para separar o seu código. Além de mais legivel, isola melhor as responsabilidades.

[Sobre funcoes javascript](https://www.sitepoint.com/es6-arrow-functions-new-fat-concise-syntax-javascript)

[Mais sobre Funcoes javascript](https://www.sitepoint.com/es6-arrow-functions-new-fat-concise-syntax-javascript)


## Buscando dados
Duration: 3:00

Para que nosso cliente possa escolher quais aeroportos ele pode viajar, precisamos buscar os dados de nossa base!!!

```javascript
let refDb = firebase.database().ref('valorBuscado');
    refDb.on('value', function (snapshot) {

        let valorDados = snapshot.val();
       //Codigo a ser executado após callback

    });
```

Quando pedimos o firebase para nos disponbilizar os dados, ele não o faz de forma síncrona.
No momento em que o firebase estiver pronto para disponbilizar os dados, ele irá fazer um "callBack". Na prática o código 
dentro do método "on" só será executado quando o firebase estiver pronto.

* Lembrem-se: Ao realizar a busca, vocês irão recuperar um array de objetos.

[Como acessar propriedades de um objeto](https://www.w3schools.com/js/js_object_properties.asp)

## AutoComplete
Duration: 3:00

Para que nosso cliente não precise digitar todo o nome da cidade do aeroporto iremos utilizar um componente de autoComplete.


Parâmetros do autoComplete (elemento, array de strings).

```javascript
 autocomplete(document.getElementById("idElemento"), objetoArrayString);
```

* Link para maiores [dúvidas](https://www.w3schools.com/howto/howto_js_autocomplete.asp)


Dicas: 
* Vocês provavelmente precisarão trabalhar o objeto retornado pelo Firebase. Existe um método chamado "map" que pode ser útil. 

```javascript
// O que voce tem
const pessoas = [
  { id: 20, nome: 'Captain Piett' },
  { id: 24, nome: 'General Veers' },
  { id: 56, nome: 'Admiral Ozzel' },
  { id: 88, nome: 'Commander Jerjerrod' }
];
// O que voce precisa
[20, 24, 56, 88]


let ids = pessoas.map(pessoa => {
  return pessoa.id;
});

```

## Buscando as passagens
Duration: 3:00

Precisaremos construir uma função no main.js para buscar as passagens e uma forma de acioná-la.

Uma das maneiras é criar um botão com o evento html de "onClick"
[Html evento de clique](https://www.w3schools.com/jsref/event_onclick.asp)

Para buscarmos as passagens precisamos das informações preenchidas pelo nosso cliente. Logo, precisaremos do valor preenchido no DOM!!

```javascript
document.getElementById("idElemento").value;
```

Lembrem-se: O elemento DOM irá apenas retornar o nome da cidade. Como vocês vão perceber as passagens não possuem o nome da cidade, apenas o código do aeroporto.


Para realizarmos a busca das passagens precisamos que as informações preenchidas pelo nosso cliente, objeto de aeroportos e objeto de passagens se encontrem. O método filter poderá auxiliar.


```javascript

let pessoas = [{
    nome: "Maria",
    bairro: "Castelo",
    idade: 15
},

{
    nome: "Jose",
    bairro: "Buritis",
    idade: 20
},

{
    nome: "Bruna",
    bairro: "Buritis",
    idade: 20
}];

// O metodo filter sempre retorna um array, mesmo que o resultado seja apenas um resultado;
// Caso seja necessario podemos pegar apenas a 1 posicao utilizando [0];
let pessoa = pessoas.filter(p => p.nome === "jose")[0];
console.log(pessoa.bairro);
//Filtramos a pessoa desejada e agora podemos ter acesso as propriadades da mesma 
//Maneira direta
pessoas.filter(p => p.nome === "jose")[0].bairro;
// Outra maneira de utilizar o metodo filter
  let pessoasFilter = pessoas.filter(pessoa => {
       return pessoa.bairro === "Buritis" && pessoa.idade === 20;
    });
```




Dicas:
* Lembrem-se que os dados de passagens estão no firebase.
* O objeto aeroportos recuperado do firebase possui o campo "city".
* Os objetos passagens e aeroportos possuem o campo "code" em comum.


## Exibindo os dados para nosso cliente
Duration: 3:00

Depois de buscarmos os dados precisamos exibi-los para o nosso cliente

* Uma das maneiras seria exibindo uma tabela. Sinta-se a vontade para inovar.

```javascript
    //Uma das maneiras de criar elementos no DOM, utilizando javascript
    let tabela = document.createElement("TABLE");
    // Como atribuir uma classe ao elemento tabela, de uma olhada nas classes de tabela do bootstrap
    tabela.className = "MinhaClasse1 MinhaClasse1-borda";
```

* Para criação das linhas e colunas desta tabela dê uma olhada no artigo https://www.w3schools.com/jsref/met_table_insertrow.asp

O método forEach pode ser muito interessante para iterarmos sobre arrays.

```javascript

let pessoas = [{
    nome: "Maria",
    bairro: "Castelo",
    idade: 15
},

{
    nome: "Jose",
    bairro: "Buritis",
    idade: 20
},

{
    nome: "Bruna",
    bairro: "Buritis",
    idade: 20
}];

 pessoas.forEach((elemento, index) => {
        console.log(elemento.nome + " do index" + index);
    });
```


Para adicionarmos um elemento a um já existente vocês poderão utilizar:

```javascript
let novoElemento = document.createElement("div");
document.getElementById("meuElementoExistente").appendChild(novoElemento);
```


Dicas: 
* Não existe nenhum problema em exibir apenas os dados do objeto passagens, ou seja, não é necessário exibir o nome da cidade.
* Mesmo se a combinação escolhida pelo cliente não retornar dados, não se preucupem, melhoraremos isto na próxima versão.


## Deploy
Duration: 3:00

Positive
: Agora só falta publicar a sua aplicação. Basta rodar o comando abaixo dentro do diretório da sua aplicação.

```javascript
firebase deploy
```


## Bônus
Duration: 3:00

Positive
: Se vocês chegaram até aqui com tudo funcionando, parabêns vocês estão indo muito bem!!

Vamos atualizar a nossa estória de usuário "Buscar Passagens".

Buscar passagens:

Eu como cliente desejo buscar passagens aéreas, para facilitar o meu dia a dia na compra de passagens.

Critérios de aceitação:

* O cliente deverá informar o aeroporto de origem.
* O cliente deverá informar o aeroporto de destino.
* O sistema deverá validar se o cliente preencheu origem e destino.
* Após o cliente acionar a busca de passagens, o sistema deverá exibir para ele o resultado da mesma.
* O sistema deverá informar ao cliente se a busca não retornar nenhum resultado.
* O cliente deve conseguir selecionar uma passagem a partir da busca.

As seguintes informações devem ser exibidas para o cliente após a busca:

* Cidade origem concatenada com código do aeroporto.
* Cidade destino concatenada com código do aeroporto.
* Data de origem formatada em "dd/MM/yyyy hh:mm:ss".
* Data de destino formatada em "dd/MM/yyyy hh:mm:ss".
* Preço arrendodado para inteiro.













