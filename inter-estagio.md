author:            Davidson Castro Orlando Souto
summary:           Programa de estágio do Banco Inter
id:                estagio
categories:        javascript
environments:      web
status:            draft
feedback link:     github.com/mariopce
analytics account: 0

# Inter estágio

## Overview of the tutorial
Duration: 0:05

Este será o seu guia para construção do desafio.O primeiro e mais importe ponto é:
* Relaxe, todos nós já estivemos na sua situação, e sabemos o quao dificil é, então procure se divertir e lembre que errar faz parte do aprendizado. 
* Nós temos diversas vagas, entao não se preucupe com a competição, de o seu melhor.
* No seu ambiente de trabalho, o sucesso é sempre será resultado de um trabalho em equipe!!!
* Durante este guia, voce pode encontrar novos termos, nao se preucupe, nao esperamos que você já os conheca,o proprio guia irá dismitifcar alguns e vocês podem pedir ajuda a qualquer momento, estamos aqui para isso!!! Nao tenha vergonha!!

Bora para a parte pratica!!! O desafio possuí duas partes, uma de desenvolvimento e outra de criação/especificação.
O segredo é dividir para conquistar!!!.

Pré-requisitos (Alguns dos requisitos serão explicados nos proximos passos)

* Internet
* Firebase
* Visual code
* Node(npm)
* Papel e caneta


## Desafio

* Iremos construir um novo produto para o Banco Inter, chamado Inter Viagens, este produto oferecera diversas funcionalidades relacionadas a viagens aereas.

* O desenvolvimento de software morderno, é realizado de forma incremental, ou seja, criamos pequenas versōes funcionais do nosso produto que agrege valor para nosso cliente.

Negative : Não é necessario ter todo o produto desenvolvido/especificado para lanca-lo, de grao em grao a galinha enche o papo!!!

* A primeira versão funcional do nosso produto será a construcao buscador de passagens aéreas.(De fato iremos desenvolver esta parte)

Negative: Não é necessário que a primeira versao esteja concluida, para comercamos a especificar a segunda fase do nosso produto.

* Como sugestão, voces devem criar um programa de fidelidade para o Inter viagens(Exemplos: smiles, km de vantagem, Clube azul).

Para documentar os requisitos levantados, poderão utilizar recursos como:

* User estória - Descrição simples da necessidade, sob o ponto de vista do usário.

O que é User Storie? http://blog.myscrumhalf.com/2011/10/user-stories-o-que-sao-como-usar/
O que é Criterio de aceitacao http://blog.myscrumhalf.com/2011/10/criterios-de-aceitacao-das-user-stories/

* Diagramas - Diagrama de atividade, sequencia e etc.

* Prototipos - Prototipos de tela.


## A primeira estória

Buscar passagens:

Eu como cliente desejo buscar passagens aereas, para facilitar o meu dia dia na compra de passagens.

Criterios de aceitação:
* O cliente deverá informar o aeroporto de origem.
* O cliente deverá informar o aeroporto de destino.
* Após a busca o sistema deverá exibir para o cliente o resultado da mesma.


Dica: 
* A segunda fase do nosso projeto já pode ser iniciada!!!
* Esta é provavelmente a primeira estória de usuario que você viu na vida, nao se preucupe com a perfeicao, o ótimo é inimigo do bom.


## O desenvolvimento


Importante, vocês podem pedir ajuda e pesquisar na internet a qualquer momento, este documento tambem ira guialo.

* Iremos utilizar html e javascript para o desenvolvimento do nosso produto.
* Iremos utilizar o firebase para hostear o nosso produto, tambem o utilizaremos como base de dados.


Positive: O Firebase é uma plataforma de desenvolvimento de aplicativos para dispositivos móveis e da Web desenvolvida pela Firebase, Inc. em 2011 e adquirida pelo Google em 2014.


1. Acessar https://firebase.google.com/?hl=pt-br ( Caso voce nao possua uma conta google, chegou o momento haha!)
2. Ir para o console
![console](https://1.png)
3. Criar um novo projeto.
``` bash
npm help
```
## Configuracao Ambiente 

1. Abra o powerShell do windows.
2. Aqui utilizaremos o gerenciador de depedencias do node o npm.

:Positive Node.js é uma plataforma construída sobre o motor JavaScript do Google Chrome para facilmente construir aplicações de rede rápidas e escaláveis. 

3. Verificar se o node esta instalado 
``` bash
npm help
```
4. Verificar se o  utilitario de linha de comando do firebase esta instalado
``` bash
firebase help
```
5. Caso o firebase nao esteja instalado 
``` bash
npm install -g firebase-tools
```
7. Acesse o firebase e clique em hosting e siga o tutorial.

8. Basicamente
``` bash
firebase login
```

``` bash
firebase init
```

``` bash
firebase deploy
```

Ao rodar o commando firebase init voce deve selecionar "Database e Hosting". Isto ira criar um projeto inicial. O terminal ira permitir que voce selecione qual projeto deseja utilizar.
Quando o terminal solicitar "Configure as a single-page app", selecione "y"

* Apos rodar o comando deploy, o seu projeto será hostiado no firebase. Voce pode conferir acessando hosting e clicando no dominio.

![console](https://2.png)



## Configurando Dependencias 


* Acessar a pasta public do seu projeto. 
* Abrir o arquivo index e alterar conforme link https://gitlab.com/snippets/1754760. O html abaixo e apenas para auxiliar, nao precisa ser necessariamente seguido. Este index.html ja esta configurado com as depedencias do firebase e bootstrap.
* O bootstrap é totalmente opcional.

Para facilitar a busca do nosso usuario utilizaremos um componente de autoComplete. Voces nao precisarao desenvolver este componente apenas utiliza-lo.
Criar um arquivo chamado autoComplete.js e autoComplete.css.

* Acesse https://gitlab.com/snippets/1754761 para pegar o conteudo do arquivo autoComplete.js

* Acesse https://gitlab.com/snippets/1754762 para pegar o conteudo do arquivo autoComplete.css

* Adicionar o autoComplete.js e autoCompletye.css no index.html
 

## Configurando o Banco de Dados
Duration: 0:05

* Utilizaremos um recurso extremamente interessante do firebase, o seu banco de dados em tempo real.

:Positive O Firebase Realtime Database é um banco de dados hospedado na nuvem. Os dados são armazenados como JSON e sincronizados em tempo real com todos os clientes conectados. Quando você cria apps em plataformas cruzadas com nossos SDKs para iOS, Android e JavaScript, todos os clientes compartilham uma instância do Realtime Database e recebem automaticamente atualizações com os dados mais recentes.

1. Acesse o firebase e clique em database
2. Escolha Realtime database 
![console](https://3.png)

Criamos uma pequena base de dados para vocês, segue o link do json a ser importado no firebase. https://gitlab.com/snippets/1754772

:Positive JSON (JavaScript Object Notation) é um modelo para armazenamento e transmissão de informações no formato texto. Apesar de muito simples, tem sido bastante utilizado por aplicações Web devido a sua capacidade de estruturar informações de uma forma bem mais compacta do que a conseguida pelo modelo XML, tornando mais rápido o parsing dessas informações. Isto explica o fato de o JSON ter sido adotado por empresas como Google e Yahoo, cujas aplicações precisam transmitir grandes volumes de dados.

## Construindo a aplicação

O desenvolvimento será feito praticamente na sua totalidade utilizando dois arquivos o index.html e o main.js,ops, ainda criamos o segundo.

* Criar um arquivo chamado main.js e importar o mesmo no index.html

Para nossa aplicacao funcionar integrada ao firebase precisamos de algumas configuracoes

* O firebase suporta aplicacoes web,android e ios, no nosso caso vamos selecionar web =)


![console](https://4.png)


Precisaremos do codigo que o firebase irá nos fornecer, voces devem criar uma funcao dentro do arquivo main.js com este codigo.

![console](https://5.png)


* Abaixo exemplos de como criar uma function utilizando a nova versao do javascript, se nao ficar claro como utilizar, o google esta sempre ai!!

```javascript

// Definicao de uma funcao
const interHelloWordFuncaoSoma = (x, y) => {
  return x + y
}

const interHelloWordFuncao = () => {
  console.log('Hello World');
}

//Executando a funcao
interHelloWordFuncaoSoma(1, 2) // 3

interHelloWordFuncao(); // Hello World
```

* O browser para renderizar os componentes utiliza o DOM

:Positive Então, o que é o DOM?
O DOM (Document Object Model) é uma interface que representa como os documentos HTML e XML são lidos pelo seu browser. Após o browser ler seu documento HTML, ele cria um objeto que faz uma representação estruturada do seu documento e define meios de como essa estrutura pode ser acessada. Nós podemos acessar e manipular o DOM com JavaScript, é a forma mais fácil e usada.

Existem diversos detalhes relacionados ao DOM, mas o mais importe por hora é que normalmente precisamos esperar o browser carregar o DOM antes de comecarmos a manipular o mesmo.

* Segue código que poderá auxiliar neste processo 

```javascript
document.onreadystatechange = () => {
    if (document.readyState === 'complete') {
        //Colocar código que será executado após o DOM terminar de carregar.
    }
};
```


* Dica: utilizem o maximo possivel de funcoes para separar o seu codigo, alem de mais legivel isola melhor as responsabilidades.


![Sobre funcoes javascript](https://www.sitepoint.com/es6-arrow-functions-new-fat-concise-syntax-javascript/)
![Mais sobre Funcoes javascript](https://www.sitepoint.com/es6-arrow-functions-new-fat-concise-syntax-javascript/)


## Buscando dados

Para que nosso cliente possa escolher quais aeroportos ele pode viajar, precisamos buscar os dados de nossa base!!!

```javascript
let refDb = firebase.database().ref('valorBuscado');
    refDb.on('value', function (snapshot) {

        let valorDados = snapshot.val();
       //Codigo a ser executado após callback

    });
```

 Quando pedimos o firebase para nos disponbilizar os dados, ele nao o faz de forma sincrona,
 no momento em que firebase estiver pronto para disponbilizar os dados, ele irá fazer um "callBack", na pratica o código 
 dentro do metodo "on" só será executado após o firebase disponbilizar os dados.


 * Lembre-se: Ao realizar a busca voce irá recuperar um array de objetos.
![Como acessar propriedades de um objeto](https://www.w3schools.com/js/js_object_properties.asp)

 ## AutoComplete

 Para que nosso cliente nao precise digitar todo o nome da cidade do aeroporto iremos utilizar um componente de autoComnplete


Parametros do autoComplete, elemento e um array de strings.

```javascript
 autocomplete(document.getElementById("idElemento"), objetoArrayString);
```

* Link para maiores duvidas https://www.w3schools.com/howto/howto_js_autocomplete.asp


Dica: Voces provavelmente precisarao trabalhar o objeto retornado pelo Firebase
Existe um metodo chamao map que pode vir a calhar 


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

Precisaremos construir uma funcao no main.js para buscar as passagens e uma forma de aciona-la.

Uma das maneiras e criar um botao com o evento html de onClick
![Html evento de clique](https://www.w3schools.com/jsref/event_onclick.asp)


Para buscarmos as passagens precisamos das informacoes preenchidas pelo nosso cliente, logo precisaremos do valor preenchido no DOM!!
```javascript
document.getElementById("idElemento").value;
```

Lembre-se o elemento DOM irá apenas retornar o nome da cidade, como voces vao perceber as passagens nao possuem o nome da cidade, apenas o codigo do aeroporto.


Para realizarmos a busca das passagens precisamos que as informacoes preenchidas pelo nosso cliente,objeto de aeroportos e objeto de passagens se encontrem, o metodo filter pode nos auxiliar.


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
Lembre-se que os dados de passagens estao no firebase
O objeto aeroportos recuperado do firebase possui o campo city;
Os objetos passagens e aeroportos possuem o campo code em comum.


## Exibindo os dados para nosso cliente

Depois de buscarmos os dados precisamos exibi-los para o nosso cliente

* Uma das maneiras seria exibindo uma tabela, sinta-se a vontade para inovar =)

```javascript
    //Uma das maneiras de criar elementos no DOM, utilizando javascript
    let tabela = document.createElement("TABLE");
    // Como atribuir uma classe ao elemento tabela, de uma olhada nas classes de tabela do bootstrap
    tabela.className = "MinhaClasse1 MinhaClasse1-borda";
```

* Para criacao das linhas e colunas desta tabela de uma olhada no artigo https://www.w3schools.com/jsref/met_table_insertrow.asp


O metodo forEach pode ser muito interessante para iterarmos sobre arrays

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


Para adicionarmos um elemento a um já existente utilizamos

```javascript
let novoElemento = document.createElement("div");
document.getElementById("meuElementoExistente").appendChild(novoElemento);
```


Dicas: Nao tem nenhum problema exibir apenas os dados do objeto passagens, ou seja, nao e necessario exibir o nome da cidade.
Mesmo se a combinacao escolhida pelo cliente nao retornar dados nao se preucupe, melhoraremos isto na proxima versao.



## Bonus

* Se voce chegou ate aqui com tudo funcionando, parabens voce esta indo muito bem!!


Vamos atualizar a nossa estória de usuário "Buscar Passagens"

Buscar passagens:

Eu como cliente desejo buscar passagens aereas, para facilitar o meu dia dia na compra de passagens.

Criterios de aceitação:
* O cliente deverá informar o aeroporto de origem.
* O cliente deverá informar o aeroporto de destino.
* O sistema deverá validar se o cliente preencheu origem e destino.
* O sistema deverá informar o cliente se a busca nao retornar nenhum dado.
* O cliente deve conseguir selecionar uma passagem a partir da busca.
* Após o cliente acionar a busca de passagens o sistema deverá exibir para o cliente o resultado da mesma.

As seguintes informacoes devem ser exibidas para o cliente apos a busca:

* Cidade origem concatenada com codigo do aeroporto
* Cidade Destino concatenada com codigo do aeroporto
* Data de origem formatada em "dd/MM/yyyy hh:mm:ss"
* Data de destino formatada em "dd/MM/yyyy hh:mm:ss"
* Preço arrendodado para inteiro.













