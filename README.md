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
