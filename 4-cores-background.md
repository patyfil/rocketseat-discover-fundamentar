# Cores e Background

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

