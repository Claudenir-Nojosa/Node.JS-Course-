![Logo](https://servidor-estaticos-xi-one.vercel.app/header.jpg)

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/Claudenir-Nojosa/Node.JS-Course-.svg?style=social&label=Star&maxAge=2592000)](https://github.com/Claudenir-Nojosa/Node.JS-Course-/stargazers/)

</div>

# 🔮 NodeJS descomplicado: todo o básico que você precisa saber. 🔮

## 👣 Passo-a-passo

<p>
<strong>	1.</strong> Entender o que é Node.js <br>
<strong>	2.</strong> Recursos do Node.js<br>
<strong>	3.</strong> Como que ele funciona <br> 
<strong>	4.</strong> Módulos <br>
<strong>	5.</strong> Iniciando o módulo "Express" <br>
<strong>	6.</strong> Nodemon <br>
<strong>	7.</strong> Considerações finais <br>

<table>
  <tr>
    <td>   
        <img height="150em" src="https://servidor-estaticos-xi-one.vercel.app/icon1.jpg"/>
    </td>
    <td>     
        <img height="150em" src="https://servidor-estaticos-xi-one.vercel.app/icon2.jpg"/>
    </td>
        <td>     
        <img height="150em" src="https://servidor-estaticos-xi-one.vercel.app/icon3.jpg"/>
    </td>
     <td>      
        <img height="150em" src="https://servidor-estaticos-xi-one.vercel.app/icon4.jpg"/>
    </td>
    <td>      
        <img height="150em" src="https://servidor-estaticos-xi-one.vercel.app/icon5.jpg"/>
    </td>
  </tr>
</table>
</p>

---
<p align="center">
<img height="250em" src="https://servidor-estaticos-xi-one.vercel.app/nodejs%20logo.png"/>
</p>
<h2> 🔫 O que é Node.js?  🔫 </h2>

<p>
É um interpretador Javascript (programa que entende Javascript) que não depende do navegador, ou seja, ele está totalmente desvinculado do navegador.
<div align="center">
    <table>
        <center>
            <tr>
                <td align="center" colspan = "2" style="padding: 24px 0; max-width: 250px">
                    <img src="https://servidor-estaticos-xi-one.vercel.app/v8.png">
                </td>
                <td align="center" colspan = "2" style="padding: 24px 0; max-width: 250px">
                    <img src="https://servidor-estaticos-xi-one.vercel.app/Libuv.svg.png">
                </td>
            </tr>
        </center>
    </table>
</div>

As duas bases para a criação do Nodejs são o V8 e o libuv
<ul>
    <li>V8 é o motor JavaScript da Google, ele é o responsável por entender o JavaScript.
    </li>
    <li>
    Libuv é uma biblioteca que deu características de uma linguagem backend dentro do Node. Ou seja, você consegue se conectar em um banco de dados por causa do libuv, mesma coisa que você faria com  PHP,Java para web, Ruby on Rails,C#.
    </li>
</ul>

O Node.js fornece aos desenvolvedores uma ferramenta abrangente para trabalhar no paradigma de I/O orientado a eventos e sem bloqueio. Ryan Dahl, o criador do Node.js foi “inspirado por aplicativos como o Gmail” e – ao criar o Node.js – teve como objetivo criar sites em tempo real com capacidade push.

<h3>🎢 Qual linguagem o Node.js é escrito? 🎢</h3>  
<br>
Node.js é escrito em C, C++ e JavaScript. 

---

<h2> 🐱‍👤Recursos do Node.js 🐱‍👤</h2>
<ol>
    <li>
    <strong>Fácil</strong> —Node.js é muito fácil de começar. É uma escolha obrigatória para iniciantes em desenvolvimento web. Com muitos tutoriais e uma grande comunidade, é muito fácil começar.
    </li>
    <li>
    <strong>Escalável</strong> —Fornece ampla escalabilidade para aplicativos. Node.js, sendo single-threaded, é capaz de lidar com um grande número de conexões simultâneas com alta taxa de transferência.
    </li>
    <li>
    <strong>Velocidade</strong> —A execução de encadeamento sem bloqueio torna o Node.js ainda mais rápido e eficiente.
    </li>
    <li>
    <strong>Pacotes</strong> —Está disponível um vasto conjunto de pacotes Node.js de código aberto que podem simplificar seu trabalho. Existem mais de um milhão de pacotes no ecossistema NPM hoje.
    </li>
    <li>
    <strong>Forte infra-estrutura</strong> —Node.js é escrito em C e C++, o que o torna rápido e adiciona recursos como suporte de rede.
    </li>
    <li>
    <strong>Multiplataforma</strong> —O suporte multiplataforma permite que você crie sites SaaS, aplicativos de desktop e até mesmo aplicativos móveis.
    </li>
    <li>
    <strong>Eclético</strong> — Node.js é uma escolha fácil para desenvolvedores, pois tanto o front-end quanto o back-end podem ser gerenciados com JavaScript como uma única linguagem.
    </li>
</ol>

---

<h2> 🧞‍♂️ Como funciona o Node.js? 🧞‍♂️</h2>

O Node realmente brilha na criação de aplicativos de rede escaláveis e rápidos. Isso se deve à sua capacidade de lidar com um grande número de conexões simultâneas.

O Node.js usa I/O sem bloqueio e orientada a eventos para permanecer leve e eficiente diante de aplicativos em tempo real com uso intensivo de dados que são executados.

O Node.js é uma plataforma que atende a uma necessidade específica. Por exemplo, você não usaria Node.js para executar operações intensivas de CPU. Quase todas as vantagens do Node são anuladas se ele for usado para computação pesada.

O Node.js usa a arquitetura “Single Threaded Event Loop” para lidar com vários clientes ao mesmo tempo. Para entender como isso é diferente de outros tempos de execução, você precisa entender como os clientes simultâneos multiencadeados são tratados em linguagens como Java.

Em um modelo de solicitação-resposta multiencadeado, vários clientes enviam uma solicitação e o servidor processa cada uma delas antes de enviar a resposta de volta. No entanto, vários encadeamentos são usados para processar chamadas simultâneas. Esses encadeamentos são definidos em um pool de encadeamentos e, sempre que uma solicitação chega, um encadeamento individual é designado para tratá-lo.

<div align="center">
    <img height="500em" src="https://servidor-estaticos-xi-one.vercel.app/node_architecture.png"/>
</div>

<strong>Node.js funciona de maneira diferente. Segue abaixo cada etapa que ele percorre: </strong>
<ol>
    <li>
    O Node.js mantém um pool de threads limitado para atender às solicitações.
    </li>
    <li>
    Sempre quando uma solicitação chega, o Node a coloca em uma fila.
    </li>
    <li>
    Agora, o “loop de evento” de thread único entra em cena. Esse loop de eventos aguarda solicitações indefinidamente.
    </li>
    <li>
    Quando uma solicitação chega, o loop a seleciona da fila e primeiro verifica se ela requer uma operação de entrada/saída (I/O ou INPUT/OUTPUT do inglês) de bloqueio. Caso contrário, ele processa a solicitação e envia uma resposta.
    </li>
    <li>
    Se a solicitação tiver uma operação de bloqueio a ser executada, o loop de eventos irá abrir um encadeamento interno para processar a solicitação. Esse grupo de threads auxiliares é chamado de "Worker Thread Pool".
    </li>
    <li>
    O loop de eventos rastreia as solicitações de bloqueio e as coloca na fila assim que a tarefa de bloqueio é processada. É assim que ele mantém sua natureza não bloqueadora.
    </li>
</ol>
Como o Node.js usa menos threads, ele utiliza menos recursos/memória, resultando em uma execução mais rápida. Quando alguém precisa processar tarefas muito pesadas, com uso intensivo de dados, usar linguagens multiencadeadas como Java faz muito mais sentido. Agora, se for para aplicações em tempo real, graças a toda arquitetura explicada anteriormente, o Node.js é a escolha óbvia.

---

<h2> Vantagens do uso do Node.js: </h2>
<ul>
    <li>
    Extremamente leve, ele utiliza pouca memória RAM e aproveita melhor a CPU. Ou seja, ele é perfeito para aplicações rápidas, que focam no desempenho. 
    </li>
    <li>
    Utiliza Javascript, o qual é uma linguagem bastante simples
    </li>
    <li>
    Tem um dos maiores ecossistemas de bibliotecas, módulos e plug-ins do mundo
    </li>
    <li>
    Suporta um número imenso de requisições (acessos)
    </li>
</ul>

---

<h2> 🛸 Módulos 🛸</h2>

Tipos de módulos Node: Módulo em Node.js é uma funcionalidade simples ou complexa organizada em um ou vários arquivos JS que podem ser usados novamente em todo o aplicativo Node.js. Existem três tipos de módulos Node.js:
<ul>
    <li>
    Módulos locais/baseados em arquivo: Define os módulos Node dentro de um arquivo em seu aplicativo e é usado em seu aplicativo.
    </li>
    <li>
    Módulos principais: Os módulos principais são módulos embutidos no Node.js. Esses módulos fornecem funcionalidade suficiente para que os designers de módulos externos possam adicionar sua própria funcionalidade que pode ser usada durante o desenvolvimento de aplicativos Node. Os módulos principais incluem path, file system, os, util e alguns outros.
    </li>
    <li>
    Módulos de terceiros: Módulos de terceiros são os módulos Node externos. Esses são os módulos Node de terceiros desenvolvidos por desenvolvedores Node que são disponibilizados por meio do ecossistema Node. Mas é necessário um gerenciador de pacotes que mantenha todos os módulos para que possam ser acessados com facilidade. É aqui que o NPM entra em cena.
    </li>
</ul>

<div align="center">
    <img height="350em" src="https://servidor-estaticos-xi-one.vercel.app/npm.png"/>
</div>

NPM (Node Package Manager): NPM é o gerenciador de pacotes padrão para ambiente de tempo de execução JavaScript em Node.js O Node.js Package Manager (npm) é o gerenciador de pacotes padrão e mais popular no ecossistema Node.js, usado principalmente para instalar e manter módulos externos no aplicativo Node.js. Os usuários podem basicamente instalar os módulos de nó necessários para seu aplicativo usando o npm. Como exportar módulos? Primeiro, inicialize um aplicativo node.js digitando npm init no prompt de comando/terminal (verifique se você está presente na pasta do projeto atual). Ele criará um arquivo package.json. Use a seguinte sintaxe para adicionar um módulo no projeto Node.js. Sintaxe:

```bash
  var módulo = require("module_name");
```
**Exemplo de módulo local:** 
Para fazer isso você precisa transformar o código em uma variável. 
Após isso, digite o código:

```jsx

module exports = nome da variável;
```

Depois de exportar o módulo, você precisa “importar” o mesmo no seu arquivo Javascript principal, digitando o código:

```jsx

var nomeVariavel = require(”./nomeDoModulol”);
```

**Exemplo de módulo interno do node:**

“http”:

```jsx

var http = require(”http”);

http.createServer(function(req,res){
       res.end(”Ola”);
).listen(8081);
console.log(”O servidor rodando”);
```

Para acessar o servidor, vá ao seu navegador e digite localhost:8081
No entanto, toda vez que você alterar o código, você precisará reiniciar o servidor para que seja atualizado.

<h2> Alguns módulos importantes inclusos no node: </h2>

| Módulos  | O que são |
| ------------- |:-------------:|
| express, Express.js, ou simplesmente Express      | Uma estrutura de desenvolvimento da Web, "padrão de fábrica" para a maioria dos aplicativos Node.js.    |
| hapi      | Framework para criação de aplicativos web.   |
| connect      | Uma estrutura de servidor HTTP para Node.js, fornecendo uma coleção de plug-ins de alto desempenhos conhecidos como middleware; ele serve como base para o Express.    |
| socket.io e sockjs      | O Socket.IO permite a comunicação baseada em eventos bidirecionais em tempo real.    |
| mongodb e mongojs      | Possibilita a comunicação com a API do MongoDB.  |
| forever     |  Uma ferramenta CLI simples para garantir que um determinado script seja executado continuamente (ou seja, para sempre). |
| bluebird      | Bluebird é uma biblioteca com foco em recursos inovadores e desempenho.    |
| moment.js      | Uma biblioteca de datas JavaScript para analisar, validar, manipular e formatar datas.     |

---

<h2> 🎿 Módulo Express: 🎿 </h2>

Express é um framework, ou seja, é um facilitador no desenvolvimento de diversas aplicações, poupando tempo para quem utiliza, pois otimiza muitas linhas de código. Além de ser rápido, ele é um dos frameworks mais utilizados.

Ele é escrito em Javascript e utilizado por diversas empresas, como a Fox Sports, Uber, IBM, Paypal, entre outras.

<h2> Características do Express.js </h2>

O Express é um framework incrível e possui diversas características 
que facilitam o desenvolvimento de suas aplicações. Dentre suas 
principais características, há:
<ul>
    <li>
        Possui um sistema de rotas completo;
    </li>
    <li>
        Possibilita o tratamento de exceções dentro da aplicação;
    </li>
    <li>
        Permite a integração de vários sistemas de templates que facilitam a criação de páginas web para suas aplicações;
    </li>
    <li>
        Gerencia diferentes requisições HTTP com seus mais diversos verbos;
    </li>
    <li>
        Feito para a criação rápida de aplicações utilizando um conjunto pequeno de arquivos e pastas;
    </li>
</ul>

<h2> Iniciando o uso do Express </h2>

Para utilizar o módulo você precisa primeiramente instalar ele e depois requerer(importar) no seu arquivo principal Javascript.

```jsx
*npm i express*
```

```jsx
*const express = require(“express”);*
```

Depois disso, crie uma constante que irá receber todo o módulo express:

```jsx
*const app = express();*
```

Para você criar um servidor, basta escrever uma linha de código:

```jsx
app.listen(8081);
```

**OBS: essa linha de código deve ser a última da sua aplicação, ou seja, toda a aplicação deve ser escrita antes do .listen**

Só que aqui o servidor esta rodando infinitamente e não mostra nenhuma mensagem informando que ele está funcionando. Para isso, você incluirá uma função de callback:

```jsx
app.listen(8081, function(){
    console.log("Servidor foi inicializado na url: http://localhost:8081");
});
```

Só que ainda assim, quando você entra na url do servidor, ele informa *“cannot get /“*. 

Isso se dá pelo fato de que o seu servidor atualmente não está retornando nada quando o seu navegador faz o *“get request”*.

> **Get:** Usado quando o cliente deseja obter recursos do servidor
> 

> **Request:** Pedido que o cliente realiza no servidor. No navegador toda vez que você troca de página ou aperta enter na barra de endereço, uma nova request é feita. Independente se você está apenas pedindo a exibição de uma página, cadastrando um novo recurso, atualizando ou excluindo.
>

Não construiu ainda uma rota para o seu servidor, uma rota é como se fosse um caminho, é a página inicial.

Então você irá mudar isso, em cima do código app.listen, a gente vai escrever app.get. Que é um metodo que o Express nos permite especificar o que é para acontecer quando o navegador entra em contato com o seu servidor e faz um *“get request”*.

O primeiro parametro que ele pega é a localização do seu get request.

Que é a rota do seu servidor, representada pelo “/”.

```jsx
app.get("/")
```

Depois você terá uma callback function que informa ao seu servidor o que fazer quando receber esse request. 

Essa função recebe dois parâmetros, uma de request e uma de response.

Request é o que você está pedindo para o servidor fazer, nesse caso, carregar a página.

Response é o que ele irá fazer após carregar a página.

```jsx
app.get("/", function(req,res){
    res.send("<h3>Hello,world!</h1>");
});
```

Res.send para um arquivo HTML:

```jsx
res.sendFile(__dirname +"/index.html")
```

<h2> Post </h2>

Post request é quando o cliente envia ao servidor dados para armazenamento.

No caso de um formulário, por exemplo, no forms você colocará o method=”post”. Da seguinte maneira:

```jsx
<form method="post">
```

E no arquivo do servidor, você inserirá o código app.post, com uma callback function. Da seguinte maneira:

```jsx
app.post("/", function(req,res){
    res.send("Obrigado por inserir esses dados!");
});
```

<h2> Como armazenar Post Requests no servidor </h2>

Já aprendeu como que o servidor recebe os post requests dos clientes, mas ainda não sabe como que o servidor armazena esses dados. 

Para realizar isso, é necessário instalar outro pacote, chamado “Body Parser”.

Para instalar é bastante simples, basta digitar no CLI:

```jsx
npm i body-parser
```

Após instalar o pacote, você requerirá o Body Parser no seu arquivo js:

```jsx
const bodyParser = require("body-parser");
```

Para pegar dados de formulários, é utilizado o “urlencoded”:

```jsx
app.use(bodyParser.urlencoded({extended: true}));
```

E armazenando os dados em variáveis, utilizando o “req.body + nome do input”:

```jsx
let num1 = Number(req.body.num1);
let num2 = Number(req.body.num2);
let result = num1 + num2;
```


---

<h2> 😈 Nodemon 😈</h2>

<div align="center">
    <img height="400em" src="https://servidor-estaticos-xi-one.vercel.app/nodemon.png"/>
</div>


Para não ter que sair do servidor usando o “CTRL + C” toda vez que você faz alterações no seu código, você instalará o modulo chamado “nodemon”.

Basicamente ele observa o seu código e atualiza o seu servidor automaticamente.

Para realizar a instalação do nodemon, simplesmente abrá o Shell e execute o comando:

```jsx
npm i -g nodemon
```

Depois de instalar globalmente na sua máquina, você irá digitar “nodemon + nome do arquivo que contém o servidor”.

---

#####  O JavaScript é uma linguagem muito popular e nos últimos anos vimos nascer vários frameworks que a utilizam. Com o Node.js é possível usar todo o poder do JavaScript também no backend, além de chatbots, IoT, desenvolvimento de aplicações desktop e até mesmo IA. A documentação do Node está disponível no [site oficial](https://nodejs.org/pt-br).