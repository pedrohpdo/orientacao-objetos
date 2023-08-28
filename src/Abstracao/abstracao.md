# Abstração
Se tratando dessse pilar, ele não é, necessariamente uma implementação, ou uma palavra reservada ou algo que vamos escrever dentro dos nossos blocos de código. Apesar disso, vamos e precisamos entender um pouco melhor do que realmente se faz em uma modelagem orientada a objetos.
Neste ponto da jornada, vamos observar o mundo real. A partir disso, vemos que o mundo real é complexo, e sua complexidade deve ser <strong>abstraída/simplificada</strong> para que nós, como desensolvedores possamos implementar um sistema que vá atender as necessidades do seu negócio.

## Nem tudo precisa ser abstraído
Nós entendemos que o conceito de Classes e Objetos dentro do mundo OO é justamente a leitura de algo do mundo real representado dentro do pequeno universo Java, por exemplo. Mas aí é o pulo do gato, nem tudo necessariamente precisa ser abstraído. Tudo de uma única coisa: a necessidade.

## Mesma entidade, duas representações
Vamos imaginar um mercado de bairro e vamos pegar um produto dele e tentar representa-lo, imaginando como ele seria usado dentro de um software (<strong>Lembrando, dentro de um mercado de bairro</strong>). Provavelmente ele chegaria perto disso aqui:

````java
    public class Produto {
        String nome;
        double precoCompra;
        double precoVenda;
        int quantidadeEstoque;
    } 
````

Bom, acho que dentro de um contexto simples como um mercadinho, isso poderia facilmente atender as necessidades desse tipo de software, já que essa modelagem tem apenas o que é necessario para seu software performar.

Agora vamos entender usar a gigantesca AMAZON para fazer um contraponto.
