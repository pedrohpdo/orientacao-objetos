# Abstração
Se tratando dessse pilar, ele não é, necessariamente uma implementação, ou uma palavra reservada ou algo que vamos escrever dentro dos nossos blocos de código. Apesar disso, vamos e precisamos entender um pouco melhor do que realmente se faz em uma modelagem orientada a objetos.

# Abstração = Simplificação
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

Agora vamos entender usar a gigantesca AMAZON para fazer um contraponto. Pense no seu contexto, pense em como milhares de produtos são entregues e em quais dados devem ser necessários para isso acontecer. Vamos tentar representar isso aqui

````java
    public class Produto {
        String nomeProduto;
        double precoCompra;
        double precoVenda;
        int quantidadeEstoque;

        String nomeVendedor;
        String cpfVendedor;

        Date dataCadastro;
        Date dataVenda;

        Location localizacao;
        Category CategoriaProduto;

        double imposto1;
        double imposto2;
    } 
````
E tenho certeza que essa implementação de ser algo próximo da realidade. Mas percebe como a mesma entidade demanda umas abstração diferente

# Nem toda abstração tem um correspondente
Exatamente. Mesmo que a premissa da Orientação a Objetos seja olhar para o mundo real e trazer isso para dentro do seu software, eventualmente você vai se deparar com uma implementação que só faz sentido dentro do contexto do seu software.

## Mudando de Exemplo,
Vamos tentar representar uma faculdade:
<p>
    <img alt="example1" src="assets/abstracao1.png">
</p>
A ideia é entender que, o conceito do "Aluno Bolsista" só é conveniente dentro do escopo de uma faculdade, e essa especificidade ainda sim demanda uma implementação mais robusta, como novos atributos (Valor da bolsa, o seu desconto ou até mesmo qual a natureza da sua bolsa).