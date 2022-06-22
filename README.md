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

- **inline**: Exibe um elemento embutido, em linha (como <span>);
- **block**: Exibe um elemento em bloco, começa em uma nova linha e ocupa toda a largura (como <p>);
- **contents**: Faz com que os filhos de um elemento apareçam como se fossem filhos diretos do pai, ignorando o próprio elemento (pode ser útil quando um wrapper deve ser ignorado ao usar CSS grid ou técnicas de layout semelhantes);
- **grid**: Exibe um elemento como um grid container em nível de bloco (divide o layout em partes).
- **inline-block**: Exibe um elemento como um block container de nível embutido. O próprio elemento é formatado como um elemento embutido, mas podemos aplicar valores de altura(height) e largura(width);
- **inline-flex**: Exibe um elemento como um flex container de nível embutido;
- **inline-grid**: Exibe um elemento como um grid container de nível embutido;
- **inline-table**: Exibe o elemento como uma tabela de nível embutido;
- **list-item**: O elemento se comporta como um elemento <li>;
- **run-in**: Exibe um elemento como bloco ou embutido, dependendo do contexto;
- **table**: O elemento se comporta como um elemento <table>;
- **table-caption**: O elemento se comporta como um elemento <caption>;
- **table-column-group**: O elemento se comporta como um elemento <colgroup>;
- **table-header-group**: O elemento se comporta como um elemento <theade>;
- **table-footer-group**: O elemento se comporta como um elemento >tfoot>;
- **table-row-group**: O elemento se comporta como um elemento <tbody>;
- **table-cell**: O elemento se comporta como um elemento <td>;
- **table-column**: O elemento se comporta como um elemento <col>;
- **table-row**: O elemento se comporta como um elemento <tr>;
- **none**: o elemento é completamente removido;
- **initial**: Herda esta propriedade de se elemento pai;
- **flex**: Exibe um elemento como um flex container e nível de bloco;
