# microservices-suport
Microservices Register Suport  - Eureka RMI.


![Macro](https://cloud.githubusercontent.com/assets/1268884/9224928/7cec593e-40dc-11e5-8b63-6ff15eceffe0.png)

#Ordem de execução dos projetos:

Microservices-support ServiceRegistrationServer

Cep-microservices 

Endereco-microservices 

#Arquitetura

A ideia arquitetural é de compor os sistemas através de [microservices] (http://martinfowler.com/articles/microservices.html)

A principal utilização desse projeto é que quando temos vários processos trabalhando em um conjunto precisamos achar um ou outro.
Esse pequeno projeto serve como o "Descobridor" de todos os serviços startados. 

Ele faz uso da biblioteca Spring Cloud e principalmente do recurso disponibilizado pela Netflix 
chamado "Eureka". 

a classe principal é:[ServiceRegistrationServer!](/src/main/java/br/com/netboots/microservices/suport/ServiceRegistrationServer.java)  

#Algumas explicações

@SpringBootApplication - Define que a aplicação é um "Springboot", faz uma porção de configurações como procurar por
beans, components, além de startar um tomcat embedded.

@EnableEurekaServer - Startar um servidor de registros de serviços. 


As principais configurações de port, name, host estão no arquivo: [registration-server.yml](src/main/resources/registration-server.yml) 

o dashboard do eureka será startado em localhost:1111



