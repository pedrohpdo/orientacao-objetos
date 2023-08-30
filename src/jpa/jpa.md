# Java Peristence API

JPA é dita uma especificação que define como frameworks ORM devem persistir os dados da aplicação dentro de uma base relacional. Ou seja, para trabalhar com JPA, você deve utilizar um framework ORM que siga essas restrições.

## Surgimento pela necessidade

Seu surgimento vem da popularização do Java no mundo corporativo, o que levantou certos pontos dentro da comunidade, como o grande tempo gasto em criação, tanto de linguagem SQL como em scripts JDBC responsável por trabalhar com elas.
Além do mais, existe a questão da mudança de paradigmas. Bancos de Dados SQL utilizam-se do paradigma relacional, e POO, paradigma orientado a objetos (Meio óbvio).

Em paradigmas relacionais tratamos de tabelas e colunas, que possuem chaves primárias (Primary Key) e chaves estrangeiras (Foreing Key), encontradas em outras tabelas distintas.

Já em uma aplicação orientada a objetos, informações/entidades são representadas por meio de clases e atributos. Mas essas representações estão sujeitas a diversas peculiaridades. Herança, Enumerações, Polimorfismo, Composição para atributos, entre outros montes

Essa distinção entre paradigmas gerou um buraco em que, a todo momento devemos transformar Objetos em Registros e Vice-Versa.

## Arquitetura de uma aplicação JPA

<img alt="fluxo-app-jpa" src="./assets/java-fluxo-app.png">

## Frameworks ORM: Hibernate
Talvez o framework que mais ande lado a lado com o JPA seja o Hibernate. Caso você não saiba o que isso mas saiba o que é o Spring Framework, fique ciente que é exatamente a mesma coisa acontecendo por debaixo dos panos e é bom você ter uma noção básica.

O Hibernate é uma ferramenta ORM open source, curiosamente nasceu sem o JPA mas hoje em dia é comum você acessar ele através da JPA, fazendo o caminho inverso. 

<strong>Seu maior trunfo</strong> é abstrair todo a camada SQL e JDBC, que agora será gerada em tempo de execução. E sendo ainda mais ousado, ele vai gerar o SQL que serve para um determinado banco de dados por conta própriam o que nos permite trocar a base sem ter que alterar scripts Java, já que isso é responsabilidade do Hibernate.

## Principais Inclusões
Dentre as principais inclusões com a implementação da JPA, temos:

- <strong>POJOS Persistentes:</strong> Agora objetos são POJO's(Plain Old Java Object), o que significa que objetos Java não dependem mais de interfaces ou frameworks externos para serem persistidos. Qualquer objeto pode ser persistido dentro de um ORM, onde todo o mapemaento pode ser feito através de anotações no seu código.

- <strong>Consultas em Objetos:</strong> Agora as consultas são realizadas pela JPQL, uma linguagem de consulta que é transformada posteriormente para SQL. Essas consultas usam um sistema interno que se baseia no modelo da entidade. Ou seja, o modelo da entidade é igual ao modelo da tabela no ela é armazenada (atributos = colunas). 

- <strong> Configurações Simples:</strong> Existe um grande número de características de persistência que a especificação oferece, todas são configuráveis através de anotações, XML ou uma combinação das duas. Anotações são simples de usar, convenientes para escrever e fácil de ler. Além disso, JPA oferece diversos valores defaults, então dependendo do escopo do seu projeto, você pode sair usando JPA sem medo de ser feliz.

## [Guia Rápido para Implementação](jpa.md)

### References/Materiais
###### [Apostila - UMA INTRODUÇÃO PRÁTICA AO JPA COM HIBERNATE (Alura)](https://www.alura.com.br/apostila-java-web/uma-introducao-pratica-ao-jpa-com-hibernate)
###### [Introdução ao JPA (DevMedia)](https://www.devmedia.com.br/introducao-a-jpa-java-persistence-api/28173)
###### [Introdução JPA e Hibernate (Nélio Alves)](https://www.youtube.com/watch?v=CAP1IPgeJkw&t=413s)
###### [Java Persistence API: Primeiros Passos (Dev Media)](https://www.devmedia.com.br/java-persistence-api-jpa-primeiros-passos/30511)
###### [User Guide (Hibernate ORM 6.2.7.final)](https://docs.jboss.org/hibernate/orm/6.2/userguide/html_single/Hibernate_User_Guide.html)

