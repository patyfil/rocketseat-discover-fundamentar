# Uma caixa dentro da outra

Box-Model - 7 aulas - 33:12  
01 - Abertura - 00:20  
02 - Introdução - 02:07  
03 - Box Sizing - 05:22  
04 - Display-block-inline - 06:43  
05 - Margin - 08:44  
06 - Padding - 03:02  
07 - Border-outline - 06:54  

## Box Model

* Fundamental para fazer layouts para a web
* Maior facilidade para aplicar o CSS

## O que é?

Uma caixa retangular.
Essa caixa possui propriedades de uma caixa (2D)

* Tamanho (largura x altura)          width | height  
* Conteúdo → content                  content  
* Bordas → border                     border  
* Preenchimento interno → padding     padding  
* Espaços fora da caixa → margin      margin  

*Cada elemento na sua página, será considerado uma caixa.*

<img src="box-model.png" width=250px>

## box-sizing

Como será calculado o tamanho total da caixa?

- content-box|border-box
  
```css
div {
  box-sizing: border-box;
}
```

### Exemplo:

#### HTML

```html
<div>
  css é incrível!
</div>
```
___

#### CSS

```css
div {
  width: 100px;
  height: 100px;
  border: 1px solid red;
  margin: 10%;
}
```

<img src="./css-incrivel.jpg">

___

#### CSS

```css
div {
  width: 100px;
  height: 100px;
  border: 1px solid red;
  margin: 10%;
  padding: 0 20px;
}
```

<img src="./css-padding.jpg">

___

#### CSS

```css
div {
  width: 100px;
  height: 100px;
  border: 1px solid red;
  margin: 10%;
  padding: 0 20px;
  box-sizing: border-box;
}
```

<img src="./css-box-sizing.jpg">

