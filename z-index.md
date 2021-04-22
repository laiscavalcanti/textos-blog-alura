---
title: "Reset CSS: o que é?"
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

Neste artigo iremos desmestificar a propriedade `z-index` do CSS e aprender como usá-la da melhor forma.  O que no primeiro momento pode parecer complicado, essa propriedade especifica a ordem de sopreposição dos elementos na tela.

Quando pensamos de posicionamento de elementos, a primeira coisa que vem a nossa cabeça é os eixos X e Y - o eixo X é referente à coordenada horizontal e o eixo y referente a coordenada vertical. Já o eixo z é responsável pelo cálculo e posicionamento da profundidade de um determinado elemento em relação à tela, se estará mais afastado ou mais próximo.

E para que essa propriedade tenha efeito, o elemento precisa ter a proprideade `posisition` definida diferente de `static`, que é a o valor de posicionamento padrão. Ou seja, definida como `fixed`, `sticky`, `relative` ou `absolute` .

# A sobreposição de elementos sem o z-index:

Sem a propriedade `z-index`, o posicionamento