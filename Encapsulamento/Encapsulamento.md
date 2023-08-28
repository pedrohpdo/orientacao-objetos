# Encapsulamento
Tido como um dos pilares da Orientação a Objetos, o encapsulamento diz respeito a "guardar" determinadas informações dentro de cápsulas, afim de não mostrar essas informações para todo mundo, uma vez que, muitas vezes elas não são necessárias.

## Imagine
Um carro, ele é composto por uma série de mecanismos que estão diretamente ligados. A embreagem está ligada a marcha está ligada, que está ligada ao motor, que está ligada a num sei o que (Não tenho a menor ideia de carro). Perceba que são processos diretamente ligados mas você, como motorista, só tem acesso a funções específicas, como a marcha, os pedais ou o volante.

O processo da queima de combustível, quantas vezes a roda gira, quantos RPM o carro consegue fazer. Tudo isso isso está escondido ao seu uso. Trazendo para o java, podemos dizer que esses comportamentos estão **privados**.

## Da mesma forma
Funciona a visibilidade dentro do Java. Veremos que, ao interagir entre objetos, vamos nos preocupar apenas com o que é visível ou **público**. Da mesma forma que ao criarmos nossos códigos, devemos saber selecionar quais características e comportamentos (**Atributos e Métodos**) devem estar vísiveis para o restante das camadas do programa, e isso é muito importante no processo da programação.

# E porque raios atômicos encapsulamento é importante?
Quando você esconde uma implementação, maiores são as chances de melhorarmos o relacionamento entre objetos. Não entendeu? Veja só

Imagine duas classes que interagem entre si. Um método chama o outro, esse mesmo chama outro, e assim vai. Concorda que se eu fizer uma mísera alteração dentro do meu código, todo o restante pode sofrer efeitos colaterais? Uma pequena alteração dentro desse cenário pode ser catastrófico para o restante do programa.

Agora imagine que temos duas classes com apenas dois métodos vísiveis, que interagem entre si o restante é privado. Percebe que, agora o nível de encapsulmento é maior e consequentemente, o impacto gerado entre as classes deve ser bem menor.

<p>
    <img src="assets/example1.png.png">
</p>

Encapsular código determina que seu uso seja mais fácil, e que não seja necessário que determinadas entidades saibam o que acontece debaixo dos panos, melhorando a comunicação entre entidades. Quanto mais encapsulado seu programa for, menores são as chances de você ter problemas no relacionamento das entidades.

## E o que são cápsulas?

<p>
    <img src="assets/capsula.png.png">
</p>

O próprio objeto é a cápsula. Lembrando que o próprio objeto é um agrupador, onde nele estão agrupados uma série de atributos e métodos. E o fato de agruparmos essas informações nos gera a possibilidade de podermos encapsular dados desse objeto para que isso não seja acessível a nenhum outro local do seu sistema. Isso diz respeito ao nível de segurança do seu código.

### Exemplificando o Encapsulamento
Criando um exemplo tosco, vamos imaginar uma classe Pessoa e vamos tomar de referência a sua idade.
``` java
public class Pessoa {
    public String nome;
    public int idade;
    public float peso;
}
```

Por uma questão óbvia, não podemos ter uma idade negativa, então faz sentido nós abstrairmos mais o código e criarmos um método onde, apenas ele vai poder alterar esse valor. Algo desse tipo:
``` java
public class Pessoa {
    public String nome;
    private int idade;
    public float peso;

    public void atualizarIdade(int valorIdade){
        if(idade > 0) {
            this.idade = valorIdade;
        }
    }
}
```

# Modificadores de Acesso
A princípio, temos 4 modificadores de acesso em Java:

<p>
    <img src="assets/camadas.png.jpg">
</p>

## Public
Aqui é porteira aberta, qualquer lugar do seu sistema pode ter acesso a algum atributo ou método dentro da sua classe caso ela use a palavra public em sua assinatura

``` java
    public int idade;
    public void setIdade() {}
```

## Private
Sendo um dos mais usados, juntamente com o public, agora vamos no sentido oposto. Atributos e Métodos private não podem ser acessados em lugar NENHUM, a não ser dentro da própria classe. Aqui temos o maior nível de encapsulamento.

``` java
    private int idade;
    private void validarIdade() {}
```

## Package(Default)
Para quem caiu de paraquedas nesse assunto, saiba que você já usa isso sem saber. O nível de visibilidade default permite que nossos atributos e métodos possam ser acessados desde que estejam todos dentros do mesmo pacote.

``` java
    int idade;
    void validarIdade() {}
```

## Protected
Ele segue a mesma linha do Default: Atributos e métodos são acessados dentro do mesmo pacote, mas também podem ser transmitidos via herança

``` java
    protected int idade;
    protected validarIdade() {}
```