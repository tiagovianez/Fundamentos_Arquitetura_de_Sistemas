Prof. Oswaldo Neto

CTO - Lady Driver


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



#### RFID Supply Chain

 



#### Energy Efficiency

Com IoT, é possível coletar dados, tanto de fontes geradoras de energia, quando de fontes consumidoras, criando assim uma rede de informações importantes para tomada de decisão, sempre buscando a eficiência energética. 



#### Computação Ubíqua


<div align="center">
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

![image-20210915001652755](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915001652755.png)

- Base na pilha do TCP/IP

- Protocolo e mensagem assíncrona **(M2M)** -> Machine to Machine
- Criado pela **IBM** para **conectar sensores de pipeline de petróleo a satélites**
- **Padrão OASIS**  suportado pelas linguagens de programação mais populares



#### Modelo Cliente Servidor

![image-20210915210518481](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915210518481.png)

* Endereço de site (quando eu digito esse endereço, eu sou o client)

* O servidor processar o conteúdo em HTML e devolve para o client
* Esse modelo é síncrono



#### Modelo Publish/Subscribe

![image-20210915210824812](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915210824812.png)



MQTT Broker é um **roteador de mensagens** para os clients que estão inscritos para receberem aquelas mensagens.

Esse modelo tem uma capacidade de lhe dar com escalabilidade de dados muito superior ao modelo cliente servidor. 

Um dispositivo publicando mensagem pode alimentar muitos softwares dispositivos que tem interesse de ouvir aquela mensagem.



#### Publish

![image-20210915211202231](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915211202231.png)



## Flexibillidade dos Tópicos e Cloud

![image-20210915211425827](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915211425827.png)

- Isso irá permitir modelar o sistema conforme a necessidade
  Cada veículo em determinado momento, assim que receber uma  posição geográfica do GPS (Tracker ou Android), assim que receber essa informação ele irá publicar no broker com seu ID específico.



#### Subscribe

![image-20210915211913761](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915211913761.png)

Capacidade que um cliente, software ou device tem de se conectar ao broker e ouvir o broker.

#### Posições de usuário específico

![image-20210915212048542](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915212048542.png)

1) Descreve a posição do usuário
2) Descreve a velocidade do gps
3) Descreve as informações do acelerômetro do usuário e não do GPS
4) Para visualizar a posição de todos os usuários (+) -> Carácter coringa
5) De um usuário específico as informações de GPS
6) Ao usar o hashtag o broker irá entregar todas as mensagens dos tópicos da sequência (internos)



#### QoS 0

Níveis diferentes de qualidade de serviço

![image-20210915212842521](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915212842521.png)

É o nível mais barato, mais otimista e de menor esforço. 



#### QoS 1

#### ![image-20210915213051664](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915213051664.png)

É o mecanismo mais comum de protocolo MQTT



#### QoS 2

![image-20210915213343431](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915213343431.png)

É o nível mais caro, pois há no mínimo dois pares de servidores para comunicação.





### Cloud

* Grande e cada vez maior número de devices conectados
* TBs ou PBs de informações
* Potencial de escala global
* As soluções de IoT possuem uma capacidade de escala global, e a nuvem é a melhor opção de armazenamento desses dados massivos gerados.
* É importante ter uma visão de como a nuvem funciona

--------------------------------------------------------------------------------------------------------------------

#### Para o estudo de caso

![image-20210915214105368](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915214105368.png)

1) **Data Store:** Irá armazenar as infomações geográficas em uma base de dados onde elas irão permenecer por um tempo necessário no qual irei utilizá-lo em determinado momento para **gerar informações (insights)**
2) **Cache (Real Time Analytics):** Irá disponibilizar ao usuário a informação mais atualizada da posição de cada veículo. 

* Em ambos os casos, necessitará da figura do worker (minha aplicação / regra do negócio)

* O worker precisa fazer um subscribe do broker, se inscrevendo nos tópicos do broker onde os apps ou gps trackers irão publicar as informações
* O worker irá transmitir a informação final
* No segundo worker ele precisaria receber o dado mais atual para transmitir a informação real time 







![image-20210915215511562](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915215511562.png)

* O armazenamento da informação dentro da nuvem, **precisará ser bem pensada;**
* Sempre estaremos dando com informações geradas das mais diversas naturezas pelos dispositivos (olhar da IoT) e existe a possibilidade desses dispositivos escalarem significativamente;
* **PostgreSQL** ou **MySQL** para lidar com posição geográfica Lat e Long (Tabelas / Estruturadas);
* **É importante levar em consideração o volume**
* **Cassandra, MongoDB (NoSQL)**: Armazenamento de Clusters, eles dão **mais flexibilidade** pois poderá armazenar tanto **dados estruturados** quanto **não estruturados.** 

* É preciso **preparar a aplicação** para lhe dar com **dados que não tem velocidade** com **dado que tem velocidade**.



## Estudo de Caso (Part. III)

![image-20210915224015082](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915224015082.png)

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

![image-20210915225116270](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915225116270.png)





### Mínimo Produto Viável (Mais robusta - empresarial)

![image-20210915225523787](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915225523787.png)

* Evolução para uma carga maior de dados escaláveis 
* HiveMQ (Broker bastante conhecida no meio corporativo)

* Akka Scala JVM: Para lhe dar com grande fluxo de dados
* Voltada para dados estruturados e não estruturados (SQL e NoSQL)





### Solução em Cloud (AWS)

![image-20210915225947199](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915225947199.png)

* IoT Core: Broker
* AWS Kinesis Firehose: DataStreaming (Fluxo constante de dados), através dele irá interpretar os dados do IoT Core e transmitir para a AWS S3
* AWS S3





### IoT na Prática (Interface Gráfica / Aplicação Web)

![image-20210915230427385](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915230427385.png)





### IoT na Prática (Cloud)

![image-20210915230517975](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915230517975.png)

* **AWS Lambda:** Uma função (unidade de código) pela Amazon, **ela dispararia sempre quando houver um dado novo da posição geográfica de determinado veículo (Lat e Long).** A função de execução é a alimentação de área de Cache (ElasticCache Redis).  Informando a chave (Id User) e o valor da chave (Lat; Long). A diferença é que **a Lambda sempre irá armazenar a última informação coletada do User**, ou seja, **a mais atual;**





![image-20210915232249668](C:\Users\Tiago\AppData\Roaming\Typora\typora-user-images\image-20210915232249668.png)

* Criar um back-end 
* AWS EC2 são máquinas virtuais (são servidores que rodam linux e windows)
* FeathersJS Backend: Framework que irá rodar dentro do EC2 e se comunicar pelo ElasticCache

