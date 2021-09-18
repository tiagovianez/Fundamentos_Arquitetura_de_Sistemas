

### Monolito

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133868182-8256d48b-629d-4a24-88e6-0da363f207b5.png" width="500px" />
</div>

* O mecanismo mais simples, as aplicações iniciam por ele. É um único codebase, aplicação única.

* Uma aplicação que terá 03 instâncias e conectadas em 1 ou mais banco de dados
* A ideia dele é uma aplicação, quando não há muita demanda. Caso haja um aumento da demanda, apenas um aplicação não será suficiente para rodar, por isso é necessário ter outras instâncias para dar conta e até mesmo caso haja algum erro em uma delas.



### Microserviços #1

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133868200-4f29d4f3-b8ee-4298-b05a-842d8dbe8844.png" width="500px" />
</div>


* Um serviço para cada operação
* Nodo 1 equivale a um monolito
* O serviço 3 é interno, que não possui uma camada http de comunicação
* Conforme a arquitetura irá crescendo, isso ficará mais difícil de manter e monitorar



### Microservicos #2

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133868228-e2336cc4-040d-450f-a9bd-c43372b3d4d1.png" width="500px" />
</div>


* Não há mais um canal de comunicação direta, ao invés disso, haverá um Message Broker
* A vantagem disso é que não haverá dependência de um serviço para outro, justamente pelo fato, de que todas informações irão passar por um Message Broker.
* Há uma flexibilização de troca de serviços, pelo fato da independência de comunicação entre eles.
* A grande questão é que a arquitetura ficará refém do Message Broker



### Microserviços #3

<div align="left">
<img src="https://user-images.githubusercontent.com/78626907/133868374-81a1b747-a8a6-4fb5-88e2-bf6d31a395f6.png" width="500px" />
</div>


* Gerenciador de Pipeline (Ex.: Kamuda, AWS..)
* A Request entra pelo Proxy, em seguida vai até o Gerenciador de Pipeline, através daquela request ele irá interpretar e transmitir para determinado serviço, até encerrar o Pipeline.
* O Gerenciador de Pipeline tem suas vantagens mas é preciso saber trabalhar, uma vez o gerenciador estiver fora do ar, toda a arquitetura ficará fora do ar.





## Comparativo entre os tipos de arquitetura

### Pros e Contras Monolito

#### Prós

* Baixa complexidade
* Monitoramento simplificado

#### Contra

* Stack única
* Compartilhamento de recursos
* Acoplamento
* Mais complexo e escalabilidade



### Prós e Contras Microserviços #1

#### Prós

* Stack dinâmica: Poderá trabalhar com diversas tecnologias
* Simples escalabilidade: Poderá consumir bem menos recursos da máquina que rodam aquele serviço

#### Contra

* Acoplamento: Um serviço **terá dependência um do outro**

* Monitoramento mais complexo: Várias aplicações rodando separadamente

* Provisionamento mais complexo: Por haver **mais serviços rodando**. Deverá haver um provisionador de nodes, serviços e containers (docker)



### Prós e Contras Microserviços #2

#### Prós

* Stack dinâmica
* Simples escalabilidade
* Desacoplamento: Por ter diferentes aplicações se **comunicando de forma assíncrona**

#### Contra

* Monitoramento mais complexo: Há um message brocker entre cada serviço.
* Provisionamento mais complexo: para prover um serviço, e para isso é preciso prever que aquele serviço não ficará offline.



### Prós e Contras Microserviços #3

#### Prós

* Stack dinâmica
* Simples escalabilidade
* Desacoplamento
* Menor complexidade: Não há mais comunicação assíncrona devido a pipeline

#### Contra

* Provisionamento mais complexo: Precisa prover uma **manutenção de monitoramento e escalabilidade desse gerenciador de pipeline**, pois ele **deverá se manter sempre online,** pois caso ele falhe, toda a arquitetura irá falhar.
* Plataforma inteira depende do gerenciador de pipeline: **Ele precisará gerenciar esse erro.**





## Gerenciamento de erros e volume de acesso

#### Onde é mais complexo:

* Processos assíncronos (Microserviços #2): 
* Pipeline



#### Solução:

* Dead letter queue
* Filas de re-tentativas

