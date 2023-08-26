# CSS Inicial - Nem tudo são Pixels

Nesse curso vamos aprender como funcionam as unidades de medidas e valores no CSS, como tipos numéricos, unidades comuns, distâncias absolutas e relativas entre os elementos, porcentagens e muito mais.

* Nem tudo são pixels - 8 aulas - 22:54  
1 - Abertura - 00:19  
2 - Introdução - 02:51  
3 - Tipos numéricos e unidades comuns - 02:52  
4 - Distâncias absolutas e relativas - 05:45  
5 - Porcentagens - 03:23  
6 - Position - 02:39  
7 - Funções - 04:01  
8 - Strings e identificadores - 01:04  

Nessa aula vamos falar sobre valores e unidades de medidas no CSS e como podemos usar a documentação do MDN para aprender mais.

## Valores e unidades de medidas

* Cada propriedade possui valores `property: value`  
* Estudo constante a fim de entender as propriedades e seus valores

## Na prática

* Como conhecer e estudar os valores na documentação?
`<color> <length>`

* Os termos podem variar `values` ou `data types`
Documentação MDN: <https://developer.mozilla.org/en-US/>

## Tipos numéricos

* `<integer>`   Número inteiro como -10 ou 223  
* `<number>`  Número decimal como -2.4, 64 ou 0.234  
* `<dimension>` É um `<number>` com uma unidade junto: 90deg, 2s, 8px  
* `<percentage>` Representa uma fração de outro número: 50%  

## Unidades comuns

* `<length>` Representa um valor de distância: px, em, vw
* `<angle>` Representa um ângulo: deg, rad, turn
* `<time>` Representa um tempo: s, ms
* `<resolution>` Representa resoluções para dispositivos: dpi

## Distâncias absolutas e relativas

Distâncias absolutas `<length>`  
São fixas e não alteram seu valor.

| Unidade  | Nome                | Equivalência         |
|----------|---------------------|----------------------|
| cm       | Centímetros         | 1cm = 96px/2.54      | 
| in       | Inches (polegadas)  | 1in = 2.54cm = 96px  | 
| px       | Pixels              | 1px = 1/96th of 1in  |

* o mais comum e mais utilizado é o **px**  
* não é recomendado usar cm

## Distâncias relativas

São relativas a um outro valor, pode ser o elemento pai, ou root, ou o tamanho da tela.  

Benefício: Maior adaptação aos diferentes tipos de tela.  

| Unidade  | Relativo a                                    |
|----------|-----------------------------------------------|
| em       | Tamanho da font do elemento pai               |
| rem      | Tamanho da font do elemento raiz (root/html)  | 
| vw       | 1% da viewport wid                            |  
| vh       | 1% da viewport height                         |

Normalmente o tamanho da font padrão do navegador é de 16px e para mudar esse valor temos que fazer a alteração no root ou no elemento html.  

```css
:root {
  font-size: 18px;
}

/* OU */

html {
  font-size: 18px;
}
```

O viewport é a parte da tela que está sendo exibida. No caso dos navegadores web, é o que é exibido na janela/tela do documento. Conteúdos que estão fora do viewport só serão exibidos quando feito um scroll da área de visualização.  

## Porcentagens %

* Em muitos casos é tratado da mesma maneira que as distâncias `<length>`
* Sempre será relativo a algum valor

## Posições

`<position>`

Representa um conjunto de coordenadas 2D:
-- top, right, bottom, left e center

* Usado para alguns tipos de propriedades  
* Não confundir com a propriedade `position`

## Funções

Em programação, funções são reconhecidas por causar um reaproveitamento de código.  

* rgb()
* hsl()
* url()
* calc()

## Strings e identificadores

* Strings: Texto envolto em aspas  
  
```css
.box::after {
  content: "Isso é uma string"
}
```

* Identificadores: red, black, gold
