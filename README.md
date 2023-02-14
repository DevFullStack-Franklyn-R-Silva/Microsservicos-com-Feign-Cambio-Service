O que precisa para funcionar:

- Java 11+ [Clique aqui](https://www.oracle.com/java/technologies/javase/jdk19-archive-downloads.html)
- Maven 3.9.0+ [Clique aqui](https://maven.apache.org/download.cgi) 
- Colocar as variáveis de ambiente [Clique aqui](https://www.jdevtreinamento.com.br/variaveis-de-ambiente-configuracao/#:~:text=No%20menu%20%C3%A0%20esquerda%20clique,em%20%5BVARI%C3%81VEIS%20DE%20AMBIENTE%5D.)
- MySQL server Community [Clique aqui](https://dev.mysql.com/downloads/mysql/)
- MySQL Workbench [Clique aqui](https://dev.mysql.com/downloads/workbench/) ou HeidiSQL [Clique aqui](https://www.heidisql.com/download.php)
- Spring Tools 4 [Clique aqui](https://spring.io/blog/2021/06/21/spring-tools-4-11-0-released)
- Docker [Clique aqui](https://www.docker.com/)

# Microsservicos-com-Feign-Cambio-Service

## O que são microsserviços?
- Um estilo arquitetural.
- Uma alternativa às aplicações "monolíticas" tradicionais
- As aplicações são implementadas como um conjunto de
pequenos serviços, cada um dos quais sendo executado como
um processo independente e cada um dos quais se
comunicando com os outros por meio de algum tipo de
protocolo bem conhecido.
  - Microsserviços trazem vários benefícios e riscos que devem
ser considerados.

## Definições dos especialistas:

- _"Uma aplicação única, desenvolvida como um
conjunto de pequenos serviços, cada um executando
o seu próprio processo e se comunicando com
mecanismos leves, geralmente por API's REST
através do protocolo HTTP"._ – **Martin Fowler**

- _"Microsserviços são o bom e velho SOA otimizado"._ – **Adrian Cockcroft** – **Netflix**

> API – Application Programming Interface;  `   `   SOA – Service Oriented Architecture.

## Algumas definições

- São uma aplicação única, desenvolvida como um conjunto de pequenos
serviços
  - (em vez de um único aplicativo monolítico)
- ... cada um executando o seu próprio processo
  - (não apenas módulos / componentes dentro de um único executável)
- ... e se comunicando com mecanismos leves
  - (como HTTP e REST, ou mensagens AMQP etc)
- Escrito, implantado, dimensionado e mantido separadamente
  - (potencialmente em diferentes linguagens)
- São usados para encapsular funcionalidades ou regras de negócios
  - (em oposição ao encapsulamento natural da linguagem como pacotes, classes, jars etc)
- Podem ser substituídos e atualizados de forma independente


## O que precisa para rodar o projeto?

Java 17 [download](https://www.java.com/pt-BR/download/ie_manual.jsp?locale=pt_BR)

SpringToolSuite4 [Download](https://spring.io/tools) &nbsp;

Mysql [Download](https://www.mysql.com/downloads/) 
ou
HeidiSQL [Download](https://www.heidisql.com/download.php)

Ter o cambio service na máquina e o book service na máquina.
https://github.com/hadesfranklyn/Microsservicos-com-Feign-Book-Service/tree/main

## O que é o projeto?

Imagine o seguinte, a gente tem um cliente representado aqui pelo POSTMAN, mas pode ser uma outra aplicação, um outro serviço, qualquer tipo de cliente.
Abaixo tem esse endpoint http://localhost:8100/book-service/1/BRL, book service, esse book service tem acesso à base de dados também chamada de book_service,
nesse banco de dados tem autor, data de lançamento, preço e título do livro. O preço está em dolar. Imagine que tem que vender em diferentes mercados, evidentemente que nenhum sistema real cálculo de preço vai ser muito mais complexo do que isso, vai levar em conta a tributação na série e outras variáveis.

# Eureka Naming Server

O servidor de nomenclatura Eureka é um servidor baseado em REST usado nos serviços da Nuvem AWS para balanceamento de carga e failover de serviços de camada intermediária.

O servidor de nomes Eureka é um aplicativo que contém informações sobre todos os aplicativos de atendimento ao cliente. Cada microsserviço se registra no servidor de nomenclatura Eureka. O servidor de nomes registra os serviços do cliente com seus números de porta e endereços IP . Também é conhecido como Discovery Server.   O servidor de nomes Eureka vem com o pacote Spring Cloud. Ele é executado na porta padrão 8761 . Ele também vem com um componente cliente baseado em Java, o cliente eureka, que facilita muito as interações com o serviço.

https://www.javatpoint.com/eureka-naming-server


http://localhost:8765/book-service/14/BRL
http://localhost:8765/cambio-service/4/USD/BRL

API Gateway é um serviço gerenciado que permite que desenvolvedores criem, publiquem, mantenham, monitorem e protejam APIs em qualquer escala com facilidade. APIs agem como a “porta de entrada” para aplicativos acessarem dados, lógica de negócios ou funcionalidade de seus serviços de back-end.

# falta implementar: 
## circuit breaker microservices
Os disjuntores são um padrão de design para criar microsserviços resilientes, limitando o impacto de falhas e latências de serviço . O principal objetivo do padrão do disjuntor é evitar qualquer falha em cascata no sistema. Em um sistema de microsserviço, falhar rapidamente é crítico.

## Swagger OpenApi
O Swagger ajuda os usuários a criar, documentar, testar e consumir serviços da Web RESTful . Ele pode ser usado com uma abordagem de desenvolvimento de API de cima para baixo e de baixo para cima. No método top-down ou design-first, o Swagger pode ser usado para projetar uma API antes que qualquer código seja escrito.

## Referências

> https://nfvwiki.etsi.org/index.php?title=NFV_FAQ

> https://www.etsi.org/newsroom/press-releases/1673-2019-10-etsi-introduces-a-new-end-to-end-architectural-framework-for-network-and-service-automation

> https://www.etsy.com/

> https://en.wikipedia.org/wiki/Etsy

> https://martinfowler.com/bliki/MonolithFirst.html

> https://techbeacon.com/app-dev-testing/monolith-microservices-horror-stories-best-practices

> https://medium.com/a-technologists-pov/i-just-heard-that-monoliths-are-the-future-of-software-development-2190bf7f3c40

> https://www.youtube.com/watch?v=kow-sXTCg30

> https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html

> https://www.slideshare.net/spnewman/principles-of-microservices-velocity
