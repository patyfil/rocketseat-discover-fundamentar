# Rocketseat - Discover - Trilha Fundamentar

## Guia Estelar de CSS – Cascading Style Sheet  

1 - Abertura - 00:35
2 - Conhecendo o CSS - 02:01
3 - Comentários - 01:57
4 - Anatomia - 04:34
5 - Seletores - 04:16
6 - Box model - 05:22
7 - Origem do CSS - 07:09
8 - A Cascata - 05:27
9 - Especificidade - 06:18
10 - Regra important - 02:28
11 - At rules - 01:30
12 - Shorthand - 03:25
13 - Funções - 02:04
14 - DevTools - 02:49
15 - Cuidados com a escrita - 02:18
16 - Vendor prefixes - 02:10

### Introdução

### O que significa CSS?

* Cascading Style Sheet
* Código para criar estilos no HTML
* HTML é a estrutura, e o CSS é a beleza
* Não é uma linguagem de programação;
* É uma linguagem style sheet.

### Comentários

Os comentários abrem com `/*` e terminam com `*/`.
```css
/* Comentário */
```

### Anatomia do CSS

**Selectors (Seletores):** Nesse caso o h1, que vai buscar no HTML a tag h1 e aplicar as mudanças.
**Declaration (Declaração):** As chaves e tudo dentro delas.
**Properties (Propriedades):** As coisas a serem alteradas.
**Property values (Valores de propriedades):** Os novos valores que estamos atribuindo a tais propriedades.

<img src="/CSS%20ANATOMIA.jpg" width= "300px">

### Selectors

Conecta um elemento HTML com o CSS.

#### Tipos

* Global Selector `*`
* Element/Type Selector `h1`
* ID Selector `#box, #container`
* Class Selector `.red, .m-4`
* Attribute selector, Pseudo-class, Pseudo-element, e outros.

### Box model
É uma caixa retangular. Essa caixa possui as mesmas propriedades de uma caixa 2D, e tem como propriedades:

**Tamanho (largura x altura):** width e height, respectivamente
**Conteúdo:** o content
**Bordas:** o border
**Preenchimento interno:** o padding
**Espaços fora da caixa:** a margin

Quase todo elemento de uma página é considerado uma caixa: Posicionamentos, tamanhos, espaçamentos, bordas, cores, então, em suma, elementos HTML são caixas, assim como quase tudo no CSS.

### Origem do CSS  

#### 1 - inline

* Atributo `style`
  
```css
<h1 style="color: blue;">Título <strong style="color: red;">alo</strong></h1>
```  

#### 2 - interno `<style>`

* Dentro do head ou no body
* tag html que irá conter o css

```css
<style>
  h1 {
    color: blue;
  }
  strong {
    color: red;
  }
</style>
```

#### 3a - externo (Usado dentro do HTML) - `<link>`

* A forma mais comum
* arquivo css externo
  
```css
<link rel="stylesheet" href="style.css">
```

#### 3b - externo (Usado dentro do CSS) - `@import`

* arquivos css externo

```css
@import 'https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap'
```

`@import` é uma regra do CSS, portanto, deve ser usada dentro do css, ao invés de dentro do HTML, como as duas primeiras formas.
Não é recomendado seu uso, pois leva um pouco mais de tempo do que através da tag link, fazendo a página ficar menos responsiva, demorando mais para o carregamento da mesma.

### A Cascata (cascading)

A escolha do browser de qual regra aplicar, caso haja muitas regras para o mesmo elemento.

* Seu estilo é lido de cima para baixo, ou seja, caso haja algum selector com informações conflitantes, o mais embaixo é o que será atribuído.  

* São levados em consideração 3 fatores:

1. A origem do estilo;
2. A especificidade;
3. A importância;

### A origem do estilo

`Inline > tag style > tag link`

`Inline` é mais forte que `tag style` e `tag style` é mais forte que `tag link`

### Especificidade

É um cálculo matemático, onde, cada tipo de seletor e origem do estilo, possuem valores a serem considerados.  

`0`     Universal selector, combinators e negation pseudo-class (:not())  
`1`     Element type selector e pseudo-elements (::before, ::after)  
`10`    Classes e atribute selectors ([type=”radio”])  
`100`   ID Selector  
`1000`  Inline  

### A regra !important

* cuidado, evite o uso
* não é considerado uma boa prática
* quebra o fluxo natural da cascata

### At-rules

* Está relacionado ao comportamento do CSS
* Começa com o sinal de `@` seguido do identificador e valor

São as seguintes:

* `@import`    /*inclui um CSS externo*/
* `@media`     /*regras condicionais para vários dispositivos*/
* `@font-face`  /*para colocar fontes externas*/
* `@keyframes`  /*serve para as animations do CSS*/

```css
@import url(http://local.com/styles.css);

@media {min-width: 500px) {
  /* rules here */
}

@font-face {
  /* rules here */
}

@keyframes nameofanimation {
  /* rules here */
}
```

### Shorthand

* Junção de propriedades
* resumido
* legível
É basicamente a ideia de junção de propriedades, para que fiquem de forma resumida e legível.

```css
{
    /* background properties */
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;

    /* background shorthand*/
    background: #000 url(images/bg.gif) no-repeat left top;

    /* font properties */
    font-style: italic;
    font-weight: bold;
    font-size: .8em;
    line-height: 1.2;
    font-family: Arial, sans-serif;

    /* font shorthand */ 
    font: bold italic .8em/1.2 Arial, sans-serif;
```

### Algumas das características do shorthand

* Não irá considerar propriedades anteriores, ou seja, caso faça um shorthand, apenas ele será considerado, quaisquer propriedades anteriores serão substituídas pelas do shorthand.
* Os valores que não forem especificados irão assumir o valor padrão.
* Por fim, geralmente, a ordem descrita não importa, mas, caso haja muitas propriedades com valores semelhantes, poderemos encontrar problemas.

### Propriedades que aceitam shorthand

animation, background, border, border-bottom, border-color, border-left, border-radius, border-right, border-style, border-top, border-width, column-rule, columns, flex, flex-flow, font, grid, gri-area, grid-column, grid-row, grid-template, list-style, margin, offset, outline, overflow, padding, place-content, place-items, place-self, text-decoration, transition.

**<https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties>**

### Funções

* Nome seguido de abre e fecha parêntesis
* recebe argumentos

#### Exemplos

```css
@import url(“http://urlaqui.com/sytle.css”);
{
  color: rgb(255, 0, 100);
  width: calc(100% - 10px);
}
```

### DevTools

#### Descrição

Uma das ferramentas mais importantes para o desenvolvedor CSS é o DevTools (do inglês, Ferramentas de Desenvolvedor), é recomendado que você estude e faça uso da mesma, pois será muito utilizada.

### Vendor Prefixes

São coisas que permitem que browsers adicionem `features` a fim de colocar em uso alguma novidade que vemos no CSS.

#### Exemplo

```css
p {
  -webkit-background-clip: text;  /*Chrome, Safari, iOS e Android*/
  -moz-background-clip: text;   /* Mozilla (Firefox) */
  -ms-background-clip: text;   /* Internet Explorer ou Edge*/
  -o-background-clip: text;   /* Opera */
}
```

### Consultas

Você também pode consultar se a feature pode ser utilizada através dos sites:

<https://ireade.github.io/which-vendor-prefix>

<https://caniuse.com>
