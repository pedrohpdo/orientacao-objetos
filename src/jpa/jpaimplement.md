# Implementação JPA
Usando JPA com Hibernate, precisaremos baixar os JAR's no site do [Hibernate](www.hibernate.org), o site oficial você encontra clicando [aqui](www.hibernate.org).

Com o arquivo .zip baixado, precisaremos de todos os arquivos .jar obrigatórios(required). Para utilziar o Hibernate, é necessário adicionar todos esses Jar's ao Classpath da sua aplicação.

## JBDC
Não se esqueça que o Hibernet utiliza o JDBC por baixo dos panos, então você também vai precisar arquivo .jar que corresponde ao driver jdbc do seu banco. Caso não saiba do que se trata, [clique aqui para acessar entender sobre JDBC e ter acesso aos drivers](https://github.com/pedrohpdo/aulas-java/blob/main/src/jdbc/jdbc.md).

## Configurar o jpa com as propriedades da Database

Qual banco vamos persistir dados? Qual o acesso? Login? Senha? O JPA precisa dessas informações, e para isso crie um arquivo chamado persistence.xml.

Alguns dados desse arquivo tem uma maior complexidade, então vamos configurar esse arquivo da seguinte forma:

````xml
  <persistence xmlns="http://java.sun.com/xml/ns/persistence"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://java.sun.com/xml/ns/persistence
      http://java.sun.com/xml/ns/persistence/persistence_2_0.xsd"
      version="2.0">

    <persistence-unit name="tarefas">

      <!-- provedor/implementacao do JPA -->
      <provider>org.hibernate.jpa.HibernatePersistenceProvider</provider>

      <!-- entidade mapeada -->
      <class>br.com.caelum.tarefas.modelo.Tarefa</class>

      <properties>
        <!-- dados da conexao -->
        <property name="javax.persistence.jdbc.driver"
            value="com.mysql.jdbc.Driver" />
        <property name="javax.persistence.jdbc.url"
            value="jdbc:mysql://localhost/fj21" />
        <property name="javax.persistence.jdbc.user"
            value="root" />
        <property name="javax.persistence.jdbc.password"
            value="<SENHA DO BANCO AQUI>" />

        <!--  propriedades do hibernate -->
        <property name="hibernate.dialect"
            value="org.hibernate.dialect.MySQL8Dialect" />
        <property name="hibernate.show_sql" value="true" />
        <property name="hibernate.format_sql" value="true" />

        <!--  atualiza o banco, gera as tabelas se for preciso -->
        <property name="hibernate.hbm2ddl.auto" value="update" />
      </properties>
    </persistence-unit>
  </persistence>
````
Depois disso aqui, vamos mapear uma entidade dentro da base.

## Mapeando uma Entidade
Mapeando uma entidade/class Tarefa, utilizando anotações. LEMBRANDO QUE TODAS AS ANOTAÇÕES SÃO IMPORTADADAS DO PACOTE <strong>jakarta.persistence</strong>

````java
@Entity
public class Tarefa {
    @Id
    @GeneratedValue
    private long id;

    @Column(name = "descricao")
    private String descri;
    private boolean finalizado;
    private Date finalizado;
}
````

Exemplo simples, mas podemos entender como algumas anotações funcionam dentro do Jpa:

### Entity
A mais importante das anotações, ela quem indica que os objetos dessa classe será persistida dentro do banco de dados.

### Id
Indica que determinado atributo será utilizado como chave primária da tabela.

### GeneratedValue
Anotação que faz referência ao @id, onde diz que queremos que o próprio banco de dados seja populada pelo banco, seja ele uma chave "auto_increment" ou "sequence", a depender da base.
