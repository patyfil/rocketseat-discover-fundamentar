# CSS Inicial - Cores e Background

Agora sim, cores

## Cores

8 aulas - 12:21  

01 - Abertura - 00:19  
02 - Introdução - 01:55  
03 - Keyword named values - 01:51  
04 - Hexadecimal - 01:49  
05 - RGB - 01:18  
06 - HSL - 02:45  
07 - Global values - 01:08  
08 - Conclusão - 01:16  

## Background

11 aulas - 16:20

01 - Introdução - 00:41
02 - Background-color - 01:42
03 - Background-image-repeat - 01:27
04 - Background-position - 01:08
05 - Background-size - 01:27
06 - Background-origin-clip - 02:07
07 - Background-attachment - 01:20
08 - Shorthand - 02:45
09 - Gradient - 01:58
10 - Múltiplos valores - 01:04
11 - Experimentar - 00:41

## Cores - Introdução

Usamos CSS para alterar cores do nosso documento.  

### Tipos

* background-color (para caixas)  
* color (para textos)  
* border-color (para caixas)  
* outros...  

### Valores

Podemos definir valores por:  

* palavra-chave (blue, transparent)  
* hexadecimal (#990011)  
* funções: rgb, rgba, hsl, hsla  

## Keyword named values

A keyword é uma palavra reservada que pode ser usada como um valor de propriedade em CSS.

```css
  color: currentcolor;  /* currentcolor = cor atual */
```

## Hexadecimal

Hexadecimais são números baseados no sistema decimal, mas com cada dígito representando apenas seis posições diferentes.

```css
/*<hex-color> values 0-9 e A-F*/
color: #090; /* RED, GREEN, BLUE */
color: #009900;
color: #090a;
color: #009900aa;
```

## RGB

RGB → Red, Green e Blue  
O alpha representa a transparência da cor  

```css
/*<rgb()> values */
color: rgb(34, 12, 64, 0.6) /* 0-255 */
color: rgba(34, 12, 64, 0.6)
```

## HSL

HSL → Hue - Saturation - Lightness

```css
color: hsl(180, 100%, 50%, 60%)
color: hsla(180, 100%, 50%, 60%)
```

```css
element {
  /* Keyword values */
  color: currentcolor;  /* currentcolor = cor atual */

  /* <named-color> values */
  color: red;
  color: orange;
  color: tan;
  color: rebeccaapurple;

  /* <hex-color> values 0-F */
  /* O alpha representa a transparência da cor */
  color: #090; /* 0:RED, 9:GREEN, 0:BLUE */
  color: #009900; /* 00:RED, 99:GREEN, 00:BLUE */
  color: #090a; /* RGB ALFA */
  color: #009900aa;

  /* <rgb()> values */
  color: rgb(34, 12, 64, 0.6); /* 0-255 */
  color: rgba(34, 12, 64, 0.6);
  color: rgb(34 12 64 / 0.6);
  color: rgba(34 12 64 / 0.3);
  color: rgb(34.0 12 64 / 60%);
  color: rgba(34.6 12 64 / 30%);

  /* <hsl()> values */
  color: hsl(30, 100%, 50%, 0.6); /* Hue - Saturation - Lumiance */
  color: hsla(30, 100%, 50%, 0.6);
  color: hsl(30 100% 50% / 0.6);
  color: hsla(30 100% 50% / 0.6);
  color: hsl(30.0 100% 50% / 60%);
  color: hsla(30.2 100% 50% / 60%);

  /* Global values */
  color: inherit; /* Herança */
  color: initial;
  color: unset;
}
```

Referência
<https://developer.mozilla.org/en-US/docs/Web/CSS/color_value>

## Background

* Define um fundo para nosso elemento  
* Sua área de atuação é a caixa toda  
* Por padrão, é transparente  

### Exemplos

* Usar cores solidas  
* Usar imagens  
* Controlar  
  * a posição das imagens  
  * se elas se repetem ou não  
  * o tamanho delas na caixa  
* Usar cor e imagem juntas  
* Usar cor gradiente  

## Background-color

A propriedade background-color define a cor de fundo do elemento selecionado.

HTML

```html
<header>

</header>
<main>
    <h1>Evolua rápido com a tecnologia</h1>
    <p>Junte-se a milhares de devs e acelere
    na direção dos seus objetivos</p>
</main>
```

CSS

```css
* {
    margin: 0;
}

header {
    height: 100px;
    border: 7px dashed red;
    background-color: rgb(55, 100, 50);
}
```

## Background-image-repeat

Para adicionar uma imagem como background podemos usar a propriedade `background-image`  
Por padrão a imagem vai se repetir e podemos modificar essa opção usando a propriedade `background-repeat`    

```css
/* Values */
background-repeat: repeat-x;
background-repeat: repeat-y;
background-repeat: repeat;
background-repeat: space;
background-repeat: round;
background-repeat: no-repeat;

/* Podedmos usar 2 valores: horizontal | vertical */
background-repeat: repeat space;
background-repeat: repeat repeat;
background-repeat: round space;
background-repeat: no-repeat round;
```

## Background-position

Com a propriedade `background-position` podemos mudar a posição da imagem do background.  

```css
/* Pricipais valores */
background-position: top;
background-position: bottom;
background-position: left;
background-position: right;
background-position: center;
```

## Background-size

Para mudar o tamanho da imagem do background usamos a propriedade `background-size`.

```css
/* Values */
background-size: cover;
background-size: contain;

/* Podemos usar 2 valores, o primeiro é para a largura da imagem e o segundo é para a altura */
background-size: 40% auto;
background-size: 2em 25%;
background-size: auto 8px;
background-size: auto auto;
```

## Background-origin-clip

A propriedade `background-origin` é quem define o ponto de origem de uma imagem específica.

```css
/* Principais valores */
background-origin: border-box;
background-origin: padding-box;
background-origin: content-box;
```

O `background-clip` define se a cor ou imagem do background iniciam debaixo de sua área de borda, preenchimento ou conteúdo.

```css
/* Principais valores */
background-clip: border-box;
background-clip: padding-box;
background-clip: content-box;
background-clip: text;
```

## Background-attachment

A propriedade `background-attachment` determina se a posição da imagem vai ser fixa ou se vai rolar junto com o conteúdo.

```css
/* Principais valores */
background-attachment: scroll;
background-attachment: fixed;
background-attachment: local;
```

## Shorthand

Podemos usar o shorthand `background` para definir todos os valores do background

## Gradient

`linear-gradient()` é a função usada para criar gradient linear com o CSS.  

```css
background: linear-gradient(45deg, red, yellow)
```  

`radial-gradient()` é a função usada para criar gradient circular.  

```css
background: radial-gradient(green, red, yellow)
background: radial-gradient(rgba(255, 255, 255, 0), rgba(255, 0, 0, 0.2))
```

## Múltiplos valores

Podemos aplicar múltiplos backgrounds em um mesmo elemento, podendo ter cor sólida, gradiente ou imagem. Para isso basta separar por vírgula cada background.
