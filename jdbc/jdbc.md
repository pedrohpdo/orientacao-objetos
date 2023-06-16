# Java Data Base Connectivity
Ou como é conhecido por JDBC, é um conjunto de Funcionalidades/Interfaces/Classes comuns que ajudam o programador a manipular algum banco de dados relacional de forma mais otimizada. Funciona como uma ponte entre a aplicação Java e o banco de dados em questão, realizando a interpretação e a conversão dos comandos do banco, de acordo com as características de cada um.

Tendo isso em vista, podemos fragmentar o JDBC em duas camadas distintas, a <strong>API JDBC</strong> e os <strong>DRIVERS JDBC</strong>

## JDBC API
Se tratam do conjunto de interfaces e métodos que são fornecidos para o usuário interagir dentro do banco de dados. Estamos tratando de
```
    Métodos
    Classes
    Interfaces
    Conexões com o Banco de Dados
    Consultas
```

## JDBC Drivers
Software específico para um determinando banco de dados. É responsável por fornecer a comunicação de dados entre a aplicação Java e o banco de dados, tendo a responsabilidade de traduzir os comandos passados pela API JDBC para comandos e protocolos nativos do banco de dados utizado.
Cada banco de dados requer um driver específico para fazer funcionar.
<hr>

Elaborando uma linha compreensiva de eventos, podemos mapear a interação dessa forma:

<p>
    <img src="assets/jdbc.png" alt="img-fluxo">
</p>