# Estudos sobre FLEXBOX
Flexbox é destinado à criação de layout em uma dimensão, horizontal ou vertical, já o Grid layout à criação de layout em duas dimensões, linhas e colunas.
Flex container é um elemento de marcação contendo elementos filhos e destinado a criar um contexto de formatação flex para este elementos filhos.

Vamos utilizar a seguinte estrutura HTML para nossos exemplos:
```
<div class="container">
  <div class="item">item-1</div>
  <div class="item">item-2</div>
  <div class="item">item-3</div>
</div>
```

Nosso CSS base vai ser:
```
* {
  margin: 0;
  padding: 0;
}
/* Flex Container */
.container {
  max-width: 600px;
  margin: 20px auto;
/* esquemas flexbox */
}
/* Flex items*/
.item {padding: 10px 0;text-align: center;}
.container> :nth-child(1){
  background: cadetblue;
}
.container> :nth-child(2){
  background: red;
}
.container> :nth-child(3){
  background: yellowgreen;
}
```

#### Propriedade Display
A propriedade display foi criada em 1996 pela especificação para a CSS1 e só permitia os valores none, block, inline e list-item. Agora podemos usar o valor flex. 
Quando definimos um elemento pai com o display flex ele se torna um container Flex e todos os seus 'filhos' passam a ser denominados como flex itens. 
Utilização: display: flex;

Por padrão o display flex, definido no pai, tem seu flex-direction como row, ou seja, em linha.

#### Propriedade Direction
Destinado a definir o sentido e a direção do eixo principal. Podemos alterar essa direção indicando com as seguintes opções:
```
flex-direction: column; //deixa a direção do eixo em coluna
flex-direction: column-reverse; //deixa a direção do eixo em coluna reversa
flex-direction: row-reverse; //deixa a direção do eixo em linha reversa
flex-direction: row; //deixa a direção do eixo em linha
```

#### Propriedade Wrap
O flex-wrap é utilizado quando queremos que haja a quebra de linha dos flex itens. Isso serve para que eles não fiquem compactados além do limite do seu conteúdo. Nele temos as seguinte opções: 
```
flex-wrap: nowrap;//não deixa haver a quebra de linha
flex-wrap: wrap;//habilita a quebra de linha
flex-wrap: wrap-reverse;//habilita a quebra de linha reversa
```

#### Propriedade Flow
O flex-flow é um atalho para usar o flex-direction e flex-wrap. Nele temos as seguintes opções:
```
flex-flow: row nowrap; //define o flex-direction como inline e sem quebra de linha
flex-flow: row wrap; //define o flex-direction como inline e com quebra de linha
flex-flow: column nowrap; //define o flex-direction como em coluna e sem quebra de linha
```

#### Propriedade Justify-content
Justify-content é usado no flex container para alinhar os filhos em determinada direção para ocupar todo o conteúdo do seu container, isso se já não estiverem ocupando o espaço. Nele temos as seguintes opções:
```
justify-content: space-around; 
justify-content: space-between; 
justify-content: center; 
justify-content: flex-end; 
justify-content: flex-start;
```

#### Propriedade align-itens
Utilizamos o align-items para fazer um alinhamentos dos filhos em relação ao eixo do container pai. Nele temos as seguintes opções: 
```
align-items: baseline; 
align-items: center; 
align-items: flex-end; 
align-items: flex-start; 
align-items: stretch;
```

#### Propriedade align-content
Para utilizar o align-content precisamos que o container flex (pai) tenha um heigth definido e que esse valor tem que ser maior que a soma das linhas dos filhos. Use o wrap pelo amor de Deus.
