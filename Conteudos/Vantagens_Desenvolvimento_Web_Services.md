## O que são Web Services (WS)

* São soluções para aplicações **se comunicarem independente de linguagem**, softwares e hardwares utilizados
* Inicialmente Serviços Web foram criados para troca de mensagens utilizando a linguagem XML (Extensible Markup Language) sobre o protocolo HTTP sendo identificado por URI (Uniform Resource Identifier)

* Podemos dizer que **Serviços Web são API's** que se comunicam por meio de **redes sobre o protocolo HTTP.**



#### Vantagens de usar um WS

* Linguagem Comum: Pois são muitas linguagens de programação e cada banco de dados de empresa possui a sua, com a WS isso irá facilitar a integração.
* Integração : Ganho de velocidade na integração
* Reutilização de implementação: Uma vez que o retorno é sempre o mesmo
* Segurança: O WS irar tratar tudo, a própria empresa irá tratar o que irá devolver de dado ou não para o WS.
* Custos: Fica muito mais barato fazer as integrações, é uma solução única para todo mundo.



#### Principais Tecnologias

* SOAP
* REST
* XML
* JSON





## Estrutura SOAP

###  	SOAP

* SOAP - **Simple Object Acess Protocol**
* É um protocolo baseado em XML para cessar serviços web principalmente por HTTP;
* Pode-se dizer que o SOAP é uma definição de como serviços web se comunicam;
* Foi desenvolvido para facilitar integrações entre aplicações



### Vantagens

* Permite integrações entre aplicações, independente de linguagem, pois usa como linguagem comum o XML;
* É independente de plataforma e software;
* Meio de transporte genérico, ou seja, pode ser usado por outros protocolos além do HTTP



### XML

* XML - Extensible Markup Language
* É uma linguagem de marcação criada na década de 90 da W3C
* Facilita a separação de conteúdo
* Não tem limitação de criação de tags
* Linguagem comum para integrações entre aplicações



* O "SOAP Message" possui uma estrutura única que deve sempre ser seguida.

* SOAP Envelope é o primeiro elemento do documento e é usado para encapsular toda a mensagem SOAP.

* SOAP Header é o elemento onde possui informações de atributos e metadados da requisição

* SOAP Body é o elemento que contém os detalhes da mensagem


### Estruturas do SOAP

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133868797-956ca006-ef2e-4242-98d8-ec71dce08159.png" width="500px" />
</div>


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133868842-7aaf00fb-fd95-40ab-9cba-6125c2a2715b.png" width="500px" />
</div>




## Entendendo o que é WSDL e XSD

### WSDL

* WSDL - **Web Services Description Language**
* Usado para descrever Web Services, funciona como **um contrato de serviço**
* A descrição é feito em um **documento XML**, onde é descrito o **serviço, especificações de acesso, operações e métodos**

### XSD

* XSD - **XML Schema Definition**
* É um schema no formado **XML** usado para **definir a estrutura de dados que será validada pelo XML**
* O XSD funciona como **uma documentação de como deve ser montado** o SOAP Message (XML) que será enviado através de Web Service



## Aprenda o que são REST, API e JSON

### REST

* REST - **Representation State Transfer**
* É um **estilo de arquitetura de software** que **define a implementação de um serviço web**
* Podem trabalhar com os fomatos XML, JSON  ou outros.



### Vantagens do REST

* Permite **integrações entre aplicações e também entre cliente e servidor **em **páginas web e aplicações**

* Utiliza dos **métodos HTTP ** para **definir a operação que está sendo efetuada**

* Arquitetura de **fácil compreensão** 

  

### Estrutura do REST

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133868858-c2be7197-3f9b-43ee-a8c0-ece19a6e4db3.png" width="500px" />
</div>



### API

* API - **Application Programming Interface**
* São **conjuntos de rotinas documentados e disponibilizados por uma aplicação** para que **outras aplicações possam consumir suas funcionalidades**
* Ficou popular com o aumento dos serviços web
* As maiores plataformas de tecnologia disponibilizam APIs para acessos de suas funcionalidades, algumas delas são: Facebook, Twitter, Telegram, Whatsapp, GitHub...



### Principais Métodos HTTP

* GET - Solicita a representação de um recurso
* POST - Solicita a criação de um recurso
* DELETE - Solicita a exclusão de um recurso
* PUT - Solicita a atualização de um recurso



### JSON

* JSON - **JavaScript Object Notation**
* **Formatação leve utilizada para troca de mensagens entre sistemas**
* Usa-se de uma **estrutura de chave e valor** e também de **listas ordenadas**
* Um dos formatos mais populares e mais utilizados para troca de mensagens entre sistemas

### Estrutura do JSON

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133868870-453f44ca-8372-41d2-ad69-acb798edadf6.png" width="500px" />
</div>





## Veja sobre integração com REST e métodos HTTP na prática

### Código de Estado

* Usado pelo servidor para avisar o cliente sobre o estado da operação solicitada
* **1xx** - Informativo (foi recebido, mas não há uma resposta para lhe dar o processamento)

* **2xx** - Sucesso (foi recebida e processada com sucesso)

* **3xx** - Redirecionamento (Usado para quando o usuário precisa fazer uma outra ação além daquela )

* **4xx** - Erro do cliente (Quem está fazendo a requisição colocou uma informação incorreta, URI inválida ou API inexistente)

* **5xx** - Erro do servidor (URI existe, mas ocorre um erro de processamento no servidor)



#### Informações a mais sobre os códigos  e referencias

https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status

https://docs.python-requests.org/en/latest/

https://developer.twitter.com/en/docs/api-reference-index



