---
title: " z-index: Como utilizar essa propriedade do CSS"
date: pode deixar vazio
draft: true
description: "z-index: Como utilizar essa propriedade do CSS"
author: "seu user da alura"
authorEmail: "lais.cavalcante@caelum.com.br"
main_guide: "formacao-front-end"
main_category: "front-end"
guides:
  - "formacao-front-end"
---

Neste artigo iremos desmistificar a propriedade `z-index` do CSS e aprender como usá-la da melhor forma. O que no primeiro momento pode parecer complicado, essa propriedade especifica a ordem de sobreposição dos elementos na tela.

Quando pensamos em posicionamento de elementos, a primeira coisa que vem à nossa cabeça são os eixos X e Y - o eixo X é referente à coordenada horizontal e o eixo y referente a coordenada vertical. Já o eixo z é responsável pelo cálculo e posicionamento da profundidade de um determinado elemento em relação à tela, se estará mais afastado ou mais próximo.

E para que essa propriedade tenha efeito, o elemento precisa ter a propriedade `posisition` definida diferente de `static`, que é a o valor de posicionamento padrão. Ou seja, definida como `fixed`, `sticky`, `relative` ou `absolute` .

# A sobreposição de elementos sem o z-index:

Sem a propriedade `z-index` definida, por padrão, os elementos recebem o valor automático que é `z-index: auto`
Ou seja, o posicionamento é sequencial, em ordem crescente - o `z-index` de menor valor é o elemento mais profundo enquanto o `z-index` de maior valor é o mais próximo da tela.
Assim, como está demonstrado na imagem abaixo:

![imagem que representa três quadrados em cores diferentes demonstrando como funciona o posicionamento sem a propriedade z-index](https://i.imgur.com/ECTjwn9.png)

A marcação referente a imagem:

```
<body>
    <div class="square1"> Quadrado 1 </div>
    <div class="square2"> Quadrado 2</div>
    <div class="square3"> Quadrado 3</div>
    </div>
</body>
```

Os estilos referentes a imagem:

```
div{
    width: 200px;
    height: 200px;
    position: fixed;
    border: 2px solid #000000;
    border-radius: 2px;
    padding: .5rem;
    font-family: 'Roboto', sans-serif;
}

.square1{
    background-color: blueviolet;
}
.square2{
    background-color: lightcoral;
    margin-left: 3rem;
    margin-top: 3rem;
}
.square3{
    background-color:  lightgreen;
    margin-left: 6rem;
    margin-top: 6rem;
}
```
## Sobreposição de elementos utilizando z-index

Mas e se quisermos que o quadrado rosa fique na frente dos demais? O nível de profundidade desse elemento precisa mudar e, para isso,
acrescentamos o valor de `z-index: 3` , que é o maior valor dentre os elementos, para o quadrado rosa. Assim, ele ficará na frente dos outros quadrados

![imagem que representa três quadrados em cores diferentes demonstrando como funciona o posicionamento sem a propriedade z-index:3](https://i.imgur.com/qGDL62S.png)

Segue os estilos referente à imagem acima:

```
.square1{
    background-color:blueviolet;
    z-index: 2;
}
.square2{
    background-color: lightcoral;
    margin-left: 3rem;
    margin-top: 3rem;
    z-index: 3;
}
.square3{
    background-color:  lightgreen;
    margin-left: 6rem;
    margin-top: 6rem;
    z-index: 1;
}
```
Então, o que temos na imagem é o quadrado rosa como menos profundidade, dado que a propriedade `z-index` tem o maior valor dentre os elementos.
Já o quadrado verde, cujo valor de `z-index: 1`, tem a maior profundidade, ele é o último na sequência dos elementos.

## Utilizando valores negativos com z-index

O  `z-index` permite setar valores negativos para posicionar um elemento na tela. Usamos valores negativos para quando precisamos posicionar que um desses elementos com menor prioridade entre os demais e fique em último na ordem de posicionamento da tela. Vamos ao exemplo:

```
.square1{
    background-color:blueviolet;
}
.square2{
    background-color: lightcoral;
    margin-left: 3rem;
    margin-top: 3rem;
    z-index: -1;
}
.square3{
    background-color:  lightgreen;
    margin-left: 6rem;
    margin-top: 6rem;   
}
```
![](https://i.imgur.com/SzlRazV.png?1)

O quadrado de cor rosa recebe um valor negativo para `z-index`, -1, assim, jogando esse elemento para uma maior profundidade na tela, ou seja, é o último desses elementos na sequência. Como os outros quadrados não estão definidos com nenhum valor para `z-index`, por padrão, eles terão valor `auto` e por isso, tem maior prioridade a um valor negativo.


##Agora é com você!

Utilize o código compartilhado aqui para testar outros valores para `z-index`, brincar com as diversas possibilidades dessa propriedade e, estudar com a nossa Formação de HTML e CSS e com os cursos de Front-end!


Bons estudos e até o próximo artigo :}