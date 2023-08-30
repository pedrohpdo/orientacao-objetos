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


### References
###### [Apostila - UMA INTRODUÇÃO PRÁTICA AO JPA COM HIBERNATE (Alura)](https://www.alura.com.br/apostila-java-web/uma-introducao-pratica-ao-jpa-com-hibernate)
###### [Introdução ao JPA (DevMedia)](https://www.devmedia.com.br/introducao-a-jpa-java-persistence-api/28173)
###### [Introdução JPA e Hibernate (Nélio Alves)](https://www.youtube.com/watch?v=CAP1IPgeJkw&t=413s)
