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

# Preparando o ambiente
Nesse contexto, vamos trabalhar com o MySQL, e como vimos antes, cada banco de dados implica em um Driver diferente, então vamos precisar baixar o driver para incorpora-lo ao nosso projeto.

### Baixando Driver
Você pode encontrar o driver clicando <a href="https://dev.mysql.com/downloads/connector/j/?os=26" rel="external" target="_blank">aqui</a>. Lembre-se de baixar o arquivo com a extensão ".zip" e o extraia assim que baixar.

Após isso, procure o arquivo com extensão .jar, deve ser algo parecido com isso aqui (mysql-connector-java-{número da versão})

<p>
    <img src="assets/driverarchive.png" alt="img-fluxo">
</p>

### Adicionando Driver ao Ambiente
Agora vamos incorporar o Driver no seu projeto. Na sua IDE (Estou usando o eclipse de referência) crie uma pasta a parte e a nomeie com a sua preferência. Geralmente uso "libs para questão de leitura"

<p>
    <img src="assets/jdbcarchive.png" alt="img-fluxo">
</p>

Agora adicione o driver que acabamos de baixar dentro dessa pasta criada. Você pode tanto fazer pelo explorador de arquivos dentro do sistema, como você pode copiar e colocar direto para o eclipse.