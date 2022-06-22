## CSS (Cascading Style Sheet)

Define os elementos apresentados em tela, bem como, aparência e formatação de documentos da Web, layout, cores e fontes.

### Seletores

- **.(ponto)** ⇒ De classe. Para estilizar um grupo de elementos;
- **\*(asterisco)** ⇒ Universal. Pode ser usado para selecionar todo e qualquer tipo de elemento em uma página HTML;
- **#(cardinal/jogo da velha)** ⇒ Por ID. Possui uma especificidade maio que o seletor de classe;
- **:visited** ⇒ Quando o link é visitado;
- **:active** ⇒ Quando ativamos o elemento. Ex.: quando clicamos em um link e não soltamos o botão do mouse;
- **:houver** ⇒ Quando passamos o mouse em cima do elemento;
- **:focus** ⇒ Quando clicamos em cima de um campo de texto para escrever, o elemento ganha foco (muito utilizado em textos);
- **:enabled** ⇒ Representa qualquer elemento ativado/selecionado/clicado/digitado e etc;
- **:disabled** ⇒ Representa qualquer elemento desativado, não pode ser ativado/selecionado/clicado/digitado etc;

### Display’s

- **inline**: Exibe um elemento embutido, em linha (como a tag "span");
- **block**: Exibe um elemento em bloco, começa em uma nova linha e ocupa toda a largura(como a tag "p");
- **contents**: Faz com que os filhos de um elemento apareçam como se fossem filhos diretos do pai, ignorando o próprio elemento (pode ser útil quando um wrapper deve ser ignorado ao usar CSS grid ou técnicas de layout semelhantes);
- **grid**: Exibe um elemento como um grid container em nível de bloco (divide o layout em partes).
- **inline-block**: Exibe um elemento como um block container de nível embutido. O próprio elemento é formatado como um elemento embutido, mas podemos aplicar valores de altura(height) e largura(width);
- **inline-flex**: Exibe um elemento como um flex container de nível embutido;
- **inline-grid**: Exibe um elemento como um grid container de nível embutido;
- **inline-table**: Exibe o elemento como uma tabela de nível embutido;
- **list-item**: O elemento se comporta como um elemento ( tag "li");
- **run-in**: Exibe um elemento como bloco ou embutido, dependendo do contexto;
- **table**: O elemento se comporta como um elemento "table";
- **table-caption**: O elemento se comporta como um elemento ( tag "caption");
- **table-column-group**: O elemento se comporta como um elemento ( tag "colgroup");
- **table-header-group**: O elemento se comporta como um elemento ( tag "theade");
- **table-footer-group**: O elemento se comporta como um elemento ( tag "tfoot");
- **table-row-group**: O elemento se comporta como um elemento ( tag "tbody");
- **table-cell**: O elemento se comporta como um elemento ( tag "td");
- **table-column**: O elemento se comporta como um elemento ( tag "col");
- **table-row**: O elemento se comporta como um elemento ( tag "tr");
- **none**: o elemento é completamente removido;
- **initial**: Herda esta propriedade de se elemento pai;
- **flex**: Exibe um elemento como um flex container e nível de bloco;

### COMENTÁRIOS

Os comentários são feitos da seguinte forma: abrem com /_ e terminam com _/ .

```bash
/* o que ficar aqui dentro será considerado comentário */
```

### ANATOMIA

**Selectors**: Nesse caso o h1, que vai buscar no HTML a tag h1 e aplicar as mudanças.

**Declaration**: As chaves e tudo dentro delas.

**Properties**: As coisas a serem alteradas.

**Property values**: Os novos valores que estamos atribuindo a tais propriedades.

### BOX MODEL

É uma caixa retangular. Essa caixa possui as mesmas propriedades de uma caixa 2D, e tem como propriedades:

- Tamanho (largura x altura **\*width** e **height\***);
- Conteúdo: o **\*content**;\*
- Bordas: o **\*border**;\*
- Preenchimento interno: o **\*padding**;\*
- Espaços fora da caixa: a **\*margin**;\*

Quase todo elemento de uma página é considerado uma caixa: Posicionamentos, tamanhos, espaçamentos, bordas, cores, então, em suma, elementos HTML são caixas, assim como quase tudo no CSS.

### MANEIRAS DE ESTILIZAÇÃO DO HTML

- Inline
  É feita por dentro do próprio HTML, através da tag _style_, utilizada da seguinte forma:

  ```
  <h1 style="color: blue;">Título
  	<strong style="color: red;">alo</strong>
  </h1>
  ```

  Ou dentro do _head_ do HTML, assim:

  ```
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  	<style>
  	h1 {
  			color: blue;
  			}

  	strong {
  			color: red;
  			}
  	</style>
  </head>
  ```

- Link
  A forma mais comum, é através da tag link, onde vamos linkar um documento CSS externo, um outro arquivo para nosso documento HTML, feito da seguinte forma:
  ```
  <link rel="stylesheet" href="style.css">
  ```
  Neste caso, o nosso documento CSS se chama _style.css_ e sua relação com o HTML é de _stylesheet_.
- @import
  Na verdade é uma regra do CSS, portanto, deve ser usada dentro do CSS, ao invés de dentro do HTML, como as duas primeiras formas, e seu uso é mostrado a seguir:
  ```
  @import 'https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap'
  ```
  Não é recomendado seu uso, pois leva um pouco mais de tempo do que através da tag link, fazendo a página ficar menos responsiva, demorando mais para o carregamento da mesma.

### CASCATA (Cascading)

Seu estilo é lido de cima para baixo, ou seja, caso haja algum selector com informações conflitantes, o mais embaixo é o que será atribuído.

São levados em consideração 3 fatores:

- A origem do estilo;
- A especificidade;
- A importância;

**ESPECIFICIDADE**

É um cálculo matemático, onde cada tipo de seletor e origem do estilo possuem valores a serem considerados.

Os mais fracos são universal selector, combinators e negation pseudo-class, com o valor de 0. Em seguida, com valor de 1, são os element type selector e pseudo-elements.

Também temos os classes e attribute selectors, com valor de 10, ou seja, são mais fortes que os anteriores.

O segundo mais forte, ID selector, com um valor de 100, vence todos os selectors anteriores.

Por fim, temos o inline, com o valor 1000, quaisquer desses selectors anteriormente citado

### AT RULES (@)

São regras relacionadas ao comportamento do CSS, começa com um sinal de @ seguido do identificador e do valor.

São as seguintes:

- @import serve para incluir um CSS externo.
- @media são regras condicionais para vários dispositivos.
- @font-face é para colocar fontes externas.
- @keyframes serve para as animations do CSS.

### SHORTHAND

Código simplificado

Exemplo:

```
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
}
```

### FUNÇÕES

Um tipo de valor existente no CSS, é estruturado com um nome seguido de abre e fecha parênteses, que recebe um argumento/valor, que são seus valores.

Um exemplo de função é:

```
color: rgb(255,0,100);
```

### VENDOR PREFIXES

São coisas que permitem que browsers adicionem _features_ a fim de colocar em uso alguma novidade que vemos no CSS.

Exemplos:

```
p {
	-webkit-background-clip: text; /*Chrome, Safari, iOS e Android*/
	-moz-background-clip: text; /* Mozilla (Firefox) */
	-ms-background-clip: text; /* Internet Explorer ou Edge*/
	-o-background-clip: text; /* Opera */
```

Você também pode consultar se a feature pode ser utilizada através dos sites:

**[https://ireade.github.io/which-vendor-prefix](http://ireade.github.io/which-vendor-prefix)**

**[https://caniuse.com](http://caniuse.com/)**
