## Conceito da Internet das Coisas (Part. I)

Coisas que não são pessoas, começam a usar dessa rede mundial  e a partir daí trocar dados. No qual é o objetivo maior além de conhecer pessoas.



#### Porque conectar as coisas?

- Embutir sensores em objetos do dia a dia
- Coletar dados dos sensores
- Usar o dado para tomar decisão



#### Conceitos básicos de IoT

* Things: Onde queremos colocar os nossos sensores (onde queremos coletar dados)
* Cloud: Onde queremos processar e armazenar esses dados
* Inteligência: Saber utilizar esses dados gerados de forma inteligente para resolver problemas, otimizar processos e ter vantagem competitiva.



#### Smart Buildings

É a capacidade de coletar esses dados, armazena-lós e utilizá-los de forma inteligente para melhorar os sistemas de prevenção de incêndio. Ou garantir acesso a determinadas áreas a certas pessoas.



#### Smart Home

Monitoramento de diversos sensores: Alarme, Temperatura, Impacto.

Tem com o objetivo coletar os dados do morador, para assim atender a necessidade daquele morador. Exemplo: Estou voltando da rua, após uma corrida matinal, suei bastante e assim que eu chego em casa, um sensor de temperatura irá medir e interpretar a minha necessidade de já colocar a casa em um ambiente o mais adequado para mim, ligando o ar-condicionado.



#### Wearables

São componentes vestíveis, no qual irá coletando os dados da nossa saúde, dos locais em que frequento.



#### Agriculture

É possível implantar um sensor em determinada área do solo (se está mais umida ou seca), e assim, atender a necessidade da plantação de irrigar determinado solo.



#### Smart Transportation

Tesla: Carros autônomos 



#### Energy Efficiency

Com IoT, é possível coletar dados, tanto de fontes geradoras de energia, quando de fontes consumidoras, criando assim uma rede de informações importantes para tomada de decisão, sempre buscando a eficiência energética. 



#### Computação Ubíqua


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133865891-802f8b09-6e31-42a2-a1d7-90db2815a356.png" width="500px" />
</div>



#### Desafio da IoT

* **Privacidade e Segurança:** Muitas empresas lancaram produtos sem se preocupar com a privacidade e segurança. Ex.: Uma empresa chinesa começou a produzir uma câmera residencial em larga escala, só que ela não se preocupou com a privacidade e segurança, e os hackers começaram a invadir essas câmeras para acessar a imagem e o som.

* **Quantidade exponencial de dispositivos conectadas na rede:** Cada vez mais dispositivos iram se conectar nessa rede. Então para isso é preciso saber coletar esses dados, armazená-los e o mais importante usa-lós de forma inteligente. 
* Gerar valor a partir dos dados coletados: As empresas e as pessoas que tentam utilizar IoT, já procuram olhar o dado como valor, antes mesmo de criar uma solução.



## Arquitetura da Internet das Coisas (Part. II)

#### Como conectar as coisas?

Existe uma grande quantidade de opções de conectar os seus dispositivos (residenciais e industriais). Alexa, Google, Lâmpadas inteligentes e Tomadas

#### Considere esses atributos na escolha

* Baixo consumo de energia: O sensor e dispositivo irá se hospedar da energia de bateria de lítio (para coletar dados de objetos remotos)
* Rede de dados limitado: eles podem está em uma rede 3g ou 4g, sem wi-fi (Limitação de disponibilidade da rede).
* Resiliência: O device precisa ser projetado para lhe dar com a falta de rede. Lidando através de um buffet, armazenando os dados localmente e assim que houver uma disponibilidade de rede favorável, transmitir esses dados armazenados.
* Segurança: Quem poderá acessar? Quais as camadas de segurança que deverei me preocupar?
* Customização: Sensor de temperatura, ele irá atuar em diferentes ambientes e diferentes tipos de fornecedor. É preciso sempre pensar nessa customização para atender determinada necessidade.

* Baixo Custo: Uma vez que o intuito é conectar bilhões de dispositivos nos próximos anos, deveremos pensar no baixo custo de implementar essa tecnologia.



#### Arduino

Placa única com um único microcontrolador

Plataforma de prototipagem

Entradas/Saidas

Desenvolvedor escreve em C/C++

Interface serial ou USB

Shields



#### Embarcados (MCUs)

Microcontrolador de chip único

Sistema operacional real time

Embarcado

Uso industrial, médico, militar, transporte



#### Minicomputadores (Raspberry Pi)

Computador completo

Hardware integrado em uma única placa

Roda SO Linux ou Windows

Uso doméstico e comercial



#### O protocolo de comunicação - Estudo de Caso

* **Gps tracker** (para veículos no qual será exigido um nível maior de confiabilidade): É uma **solução embarcada**, terá mais controle, pois **ficará ligado diretamente no sistema elétrico do veículo**, assim que o motorista der partida no carro, a coleta de informações já passará para a nuvem.

* **Gps tracker** + **App** (Hybrid): Para veículos que não precisem de um nível tão grande de confiabilidade



* App (Smartphone): Para aqueles veículos que sejam para coletar informações em determinados momentos.



#### MQTT

É importante que todos se comuniquem na mesma língua. E o MQTT fará isso!


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866481-a2b79a74-ffbc-481a-b1f9-f023c50af344.png" width="500px" />
</div>




- Base na pilha do TCP/IP

- Protocolo e mensagem assíncrona **(M2M)** -> Machine to Machine
- Criado pela **IBM** para **conectar sensores de pipeline de petróleo a satélites**
- **Padrão OASIS**  suportado pelas linguagens de programação mais populares



#### Modelo Cliente Servidor


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866591-c94ac0d3-d51a-4e64-a397-8ec2dd8b6b57.png" width="500px" />
</div>




* Endereço de site (quando eu digito esse endereço, eu sou o client)

* O servidor processar o conteúdo em HTML e devolve para o client
* Esse modelo é síncrono



#### Modelo Publish/Subscribe


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866672-db672e53-d885-427a-a306-07c18b8d5129.png" width="500px" />
</div>




MQTT Broker é um **roteador de mensagens** para os clients que estão inscritos para receberem aquelas mensagens.

Esse modelo tem uma capacidade de lhe dar com escalabilidade de dados muito superior ao modelo cliente servidor. 

Um dispositivo publicando mensagem pode alimentar muitos softwares dispositivos que tem interesse de ouvir aquela mensagem.



#### Publish


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866702-32665c9b-2dfb-4f7d-9084-1d3fe38625f9.png" width="500px" />
</div>




## Flexibillidade dos Tópicos e Cloud

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866722-4b4759e5-63d3-44ba-98c3-02629f8a3e0e.png" width="500px" />
</div>



- Isso irá permitir modelar o sistema conforme a necessidade
  Cada veículo em determinado momento, assim que receber uma  posição geográfica do GPS (Tracker ou Android), assim que receber essa informação ele irá publicar no broker com seu ID específico.



#### Subscribe


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866736-3dfde5ab-ed18-4eb9-9f8e-d9432cb1258e.png" width="500px" />
</div>



Capacidade que um cliente, software ou device tem de se conectar ao broker e ouvir o broker.

#### Posições de usuário específico


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866755-f5aa6f9c-b8f2-41b5-b8f5-169a035837e2.png" width="500px" />
</div>


1) Descreve a posição do usuário
2) Descreve a velocidade do gps
3) Descreve as informações do acelerômetro do usuário e não do GPS
4) Para visualizar a posição de todos os usuários (+) -> Carácter coringa
5) De um usuário específico as informações de GPS
6) Ao usar o hashtag o broker irá entregar todas as mensagens dos tópicos da sequência (internos)



#### QoS 0

Níveis diferentes de qualidade de serviço
É o nível mais barato, mais otimista e de menor esforço. 

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866772-e7862fd2-a654-4de4-9d9a-5f997f1dbd1e.png" width="500px" />
</div>



#### QoS 1

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866782-e16d80c3-993d-481d-b7e4-75cd0e91b1c8.png" width="500px" />
</div>

É o mecanismo mais comum de protocolo MQTT



#### QoS 2

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866799-146d0b69-c1b1-421d-8dc3-f133ee92365f.png" width="500px" />
</div>

É o nível mais caro, pois há no mínimo dois pares de servidores para comunicação.





### Cloud

* Grande e cada vez maior número de devices conectados
* TBs ou PBs de informações
* Potencial de escala global
* As soluções de IoT possuem uma capacidade de escala global, e a nuvem é a melhor opção de armazenamento desses dados massivos gerados.
* É importante ter uma visão de como a nuvem funciona

--------------------------------------------------------------------------------------------------------------------

#### Para o estudo de caso

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866842-ab91a595-0890-458f-ab7f-78f93cd87212.png" width="500px" />
</div>

1) **Data Store:** Irá armazenar as infomações geográficas em uma base de dados onde elas irão permenecer por um tempo necessário no qual irei utilizá-lo em determinado momento para **gerar informações (insights)**
2) **Cache (Real Time Analytics):** Irá disponibilizar ao usuário a informação mais atualizada da posição de cada veículo. 

* Em ambos os casos, necessitará da figura do worker (minha aplicação / regra do negócio)

* O worker precisa fazer um subscribe do broker, se inscrevendo nos tópicos do broker onde os apps ou gps trackers irão publicar as informações
* O worker irá transmitir a informação final
* No segundo worker ele precisaria receber o dado mais atual para transmitir a informação real time 







<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866864-808c0499-2b9f-4ba2-9000-94c5922b6abb.png" width="500px" />
</div>



* O armazenamento da informação dentro da nuvem, **precisará ser bem pensada;**
* Sempre estaremos dando com informações geradas das mais diversas naturezas pelos dispositivos (olhar da IoT) e existe a possibilidade desses dispositivos escalarem significativamente;
* **PostgreSQL** ou **MySQL** para lidar com posição geográfica Lat e Long (Tabelas / Estruturadas);
* **É importante levar em consideração o volume**
* **Cassandra, MongoDB (NoSQL)**: Armazenamento de Clusters, eles dão **mais flexibilidade** pois poderá armazenar tanto **dados estruturados** quanto **não estruturados.** 

* É preciso **preparar a aplicação** para lhe dar com **dados que não tem velocidade** com **dado que tem velocidade**.



## Estudo de Caso (Part. III)

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866877-7a8debda-279e-4c3d-9767-fc8c9e786b1a.png" width="500px" />
</div>


* Coletar dados de uma frota de veículo
* Disponibilizar esses dados real time para o cliente
* Armazenar esses dados coletados para serem utilizados futuramente
* Arquitetura é uma questão de escolha



GPS (Device)

Broker (Mider)

Worker 

Data Store



### Arquitetura

### Prova de Conceito (Teste mais rápido de ponta a ponta)


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866890-a7806709-a46c-4638-bd0b-d94cdfbe007b.png" width="500px" />
</div>




### Mínimo Produto Viável (Mais robusta - empresarial)


<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866932-9f33f984-4054-46d4-bc96-2d793cb0fb55.png" width="500px" />
</div>


* Evolução para uma carga maior de dados escaláveis 
* HiveMQ (Broker bastante conhecida no meio corporativo)

* Akka Scala JVM: Para lhe dar com grande fluxo de dados
* Voltada para dados estruturados e não estruturados (SQL e NoSQL)





### Solução em Cloud (AWS)

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133866932-9f33f984-4054-46d4-bc96-2d793cb0fb55.png" width="500px" />
</div>


* IoT Core: Broker
* AWS Kinesis Firehose: DataStreaming (Fluxo constante de dados), através dele irá interpretar os dados do IoT Core e transmitir para a AWS S3
* AWS S3





### IoT na Prática (Interface Gráfica / Aplicação Web)

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133867000-b6ce2f67-00d9-419a-81e1-0be44b221b23.png" width="500px" />
</div>





### IoT na Prática (Cloud)

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133867030-cb5a403a-b04b-49d5-92d4-ede8216fbdcb.png" width="500px" />
</div>




* **AWS Lambda:** Uma função (unidade de código) pela Amazon, **ela dispararia sempre quando houver um dado novo da posição geográfica de determinado veículo (Lat e Long).** A função de execução é a alimentação de área de Cache (ElasticCache Redis).  Informando a chave (Id User) e o valor da chave (Lat; Long). A diferença é que **a Lambda sempre irá armazenar a última informação coletada do User**, ou seja, **a mais atual;**





<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133867047-a368cf72-241a-494d-8833-531f57f94b7c.png" width="500px" />
</div>



* Criar um back-end 
* AWS EC2 são máquinas virtuais (são servidores que rodam linux e windows)
* FeathersJS Backend: Framework que irá rodar dentro do EC2 e se comunicar pelo ElasticCache

