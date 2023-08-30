# Java Peristence API
JPA é dita uma especificação que define como frameworks ORM devem persistir os dados da aplicação dentro de uma base relacional. Ou seja, para trabalhar com JPA, você deve utilizar um framework ORM que siga essas restrições.

# Surgimento pela necessidade
Seu surgimento vem da popularização do Java no mundo corporativo, o que levantou certos pontos dentro da comunidade, como o grande tempo gasto em criação, tanto de linguagem SQL como em scripts JDBC responsável por trabalhar com elas.
Além do mais, existe a questão da mudança de paradigmas. Bancos de Dados SQL utilizam-se do paradigma relacional, e POO, paradigma orientado a objetos (Meio óbvio).

## Paradigma Relacional
Aqui nós tratamos de tabelas e colunas, que possuem chaves primárias (Primary Key) e chaves estrangeiras (Foreing Key), encontradas em outras tabelas distintas.

## Paradigma Orientado a Objetos
Em uma aplicação Java, informações/entidades são representadas por meio de clases e atributos. Mas essas representações estão sujeitas a diversas peculiaridades. Herança, Enumerações, Polimorfismo, Composição para atributos, entre outros montes

Essa distinção entre paradigmas gerou um buraco em que, a todo momento devemos transformar Objetos em Registros e Vice-Versa.

