## O que é Markdown?

- linguagem de marcação para adicionar formatação
- documento de texto puro
- criado em 2004 por John Gruber

## Por que usar Markdown?

- permite criar qualquer documento desde livros à documentação técnica
- é portável podendo ser aberto em praticamente qualquer aplicação
- independente de plataforma e sistema operacional

## Sintaxe básica

- Quase todos os aplicativos Markdown suportam a sintaxe básica
- Existem pequenas variações e discrepâncias

### Cabeçalhos

- usar _hashtag_ mais um espaço em branco na frente da palavra ou frase
- número de _hashtags_ indica o nível do cabeçalho indo de 1 a 6
- usar uma linha antes e depois dos cabeçalhos

| Markdown                 | HTML                         | Saída                      |
| ------------------------ | ---------------------------- | -------------------------- |
| # Cabeçalho nível 1      | `<h1>Cabeçalho nível 1</h1>` | <h1>Cabeçalho nível 1</h1> |
| ## Cabeçalho nível 2     | `<h2>Cabeçalho nível 2</h2>` | <h2>Cabeçalho nível 2</h2> |
| ### Cabeçalho nível 3    | `<h3>Cabeçalho nível 3</h3>` | <h3>Cabeçalho nível 3</h3> |
| #### Cabeçalho nível 4   | `<h4>Cabeçalho nível 4</h4>` | <h4>Cabeçalho nível 4</h4> |
| ##### Cabeçalho nível 5  | `<h5>Cabeçalho nível 5</h5>` | <h5>Cabeçalho nível 5</h5> |
| ###### Cabeçalho nível 6 | `<h6>Cabeçalho nível 6</h6>` | <h6>Cabeçalho nível 6</h6> |

### Parágrafos

- usar uma linha em branco para separar uma ou mais linhas de texto

| Markdown                  | HTML                               | Saída                     |
| ------------------------- | ---------------------------------- | ------------------------- |
| Eu gosto de usar Markdown | `<p>Eu gosto de usar Markdown</p>` | Eu gosto de usar Markdown |

### Quebra de linhas

- finalizar a linha com dois ou mais espaços e depois ENTER...
- ...ou usar a tag `<br>` se o seu aplicativo Markdown suportar

### Formatação: Negrito

- adicionar dois asteriscos antes e depois de uma palavra ou frase

| Markdown                     | HTML                                        | Saída                      |
| ---------------------------- | ------------------------------------------- | -------------------------- |
| I just love `**bold text**`. | I just love `<strong>`bold text`</strong>`. | I just love **bold** text. |
| Love`**is**`bold.            | Love`<strong>`is`</strong>`bold.            | Love**is**bold.            |

### Formatação: Itálico

- adicionar um asterisco antes e depois de uma palavra ou frase

| Markdown                               | HTML                                            | Saída                                       |
| -------------------------------------- | ----------------------------------------------- | ------------------------------------------- |
| Italicized text is the `*cat's meow*`. | Italicized text is the `<em>`cat's meow`</em>`. | Italicized text is the <em>cat’s meow</em>. |
| A`*cat*meow`.                          | A`<em>cat</em>meow`.                            | A<em>cat</em>meow.                          |

### Formatação Negrito + Itálico

- adicionar três asterisco antes e depois de uma palavra ou frase

| Markdown                                  | HTML                                                            | Saída                                   |
| ----------------------------------------- | --------------------------------------------------------------- | --------------------------------------- |
| This text is `***really important***`.    | This text is `<em><strong>`really important`</strong></em>`.    | This text is **_really important_**.    |
| This is really`***very***`important text. | This is really`<em><strong>`very`</strong></em>`important text. | This is really**_very_**important text. |

### Citações

- adicionar um sinal de maior que (>) na frente de um parágrafo

```
> A maior glória de viver não está em nunca cair, mas em nos levantar toda vez que caímos.
```

- citações com múltiplos parágrafos adicionar um sinal de maior que (>) nas linhas em branco entre os parágrafos

```
> Dorothy a seguiu por muitos dos belos aposentos de seu castelo.
>
> A Bruxa ordenou que ela limpasse as panelas e chaleiras e varresse o chão e mantivesse o fogo alimentado com lenha.
```

- citações aninhadas adicionar dois sinais de maior que (>>) na frente do parágrafo que deseja aninhar

```
> Dorothy a seguiu por muitos dos belos aposentos de seu castelo.
>
>> A Bruxa ordenou que ela limpasse as panelas e chaleiras e varresse o chão e mantivesse o fogo alimentado com lenha.
```

- alguns elementos de formatação Markdown podem ser usados dentro de citações

```
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

### Listas Ordenadas

- colocar números seguidos de pontos começando pelo número 1 mais um espaço em branco antes da palavra ou frase

| Markdown                                                                                                                                                   | HTML                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Saída                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item                                                                                         | `<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ol>`                                                                                                                                                                                                                                                                                                                                                          | 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item                                                                                         |
| 1. First item<br>1. Second item<br>1. Third item<br>1. Fourth item                                                                                         | `<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ol>`                                                                                                                                                                                                                                                                                                                                                          | 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item                                                                                         |
| 1. First item<br>8. Second item<br>3. Third item<br>5. Fourth item                                                                                         | `<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ol>`                                                                                                                                                                                                                                                                                                                                                          | 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item                                                                                         |
| 1. First item<br>2. Second item<br>3. Third item<br>&nbsp;&nbsp;&nbsp;&nbsp;1. Indented item<br>&nbsp;&nbsp;&nbsp;&nbsp;2. Indented item<br>4. Fourth item | `<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Indented item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Indented Item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`</ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ol>` | 1. First item<br>2. Second item<br>3. Third item<br>&nbsp;&nbsp;&nbsp;&nbsp;1. Indented item<br>&nbsp;&nbsp;&nbsp;&nbsp;2. Indented item<br>4. Fourth item |

### Lista Não Ordenadas

- colocar um traço (-) mais um espaço em branco antes da palavra ou frase

| Markdown                                                                                                                                             | HTML                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Saída                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| - First item<br>- Second item<br>- Third item<br>- Fourth item                                                                                       | `<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ul>`                                                                                                                                                                                                                                                                                                                                                          | <li> First item<br><li> Second item<br><li> Third item<br><li> Fourth item                                                                         |
| _ First item<br>_ Second item<br>_ Third item<br>_ Fourth item                                                                                       | `<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ul>`                                                                                                                                                                                                                                                                                                                                                          | <li> First item<br><li> Second item<br><li> Third item<br><li> Fourth item                                                                         |
| + First item<br>+ Second item<br>+ Third item<br>+ Fourth item                                                                                       | `<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ul>`                                                                                                                                                                                                                                                                                                                                                          | <li> First item<br><li> Second item<br><li> Third item<br><li> Fourth item                                                                         |
| - First item<br>- Second item<br>- Third item<br>&nbsp;&nbsp;&nbsp;&nbsp;- Indented item<br>&nbsp;&nbsp;&nbsp;&nbsp;- Indented item<br>- Fourth item | `<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Indented item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Indented Item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`</ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ul>` | <ul><li> First item</li><li> Second item</li><li> Third item</li><ul><li> Indented item</li><li> Indented item</li></ul><li> Fourth item</li></ul> |

### Código fonte

- Para denotar uma palavra ou frase como código, coloque-a entre acentos graves (`)

| Markdown                              | HTML                                               | Saída                                          |
| ------------------------------------- | -------------------------------------------------- | ---------------------------------------------- |
| At the command prompt, type \`nano\`. | At the command prompt, type `<code>`nano`</code>`. | At the command prompt, type <code>nano</code>. |

### Linhas Horizontais

- use três ou mais asteriscos (\*\*\*)
- colocar linhas em branco antes e depois das linhas horizontais

### Links

- colocar o texto do link entre colchetes e siga-o imediatamente com a URL entre parênteses

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com).
```

### Imagens

- adicionar um ponto de exclamação (!), seguido de um texto alternativo entre colchetes e o caminho ou URL para o recurso de imagem entre parênteses.

```
![The San Juan Mountains are beautiful!](/assets/images/san-juan-mountains.jpg "San Juan Mountains")
```

### Caracteres de Escape

- adicionar uma barra invertida (\\) na frente do caractere.

| Character | Name                                           |
| --------- | ---------------------------------------------- |
| \         | backslash                                      |
| `         | backtick (see also escaping backticks in code) |
| \*        | asterisk                                       |
| \_        | underscore                                     |
| { }       | curly braces                                   |
| [ ]       | brackets                                       |
| < >       | angle brackets                                 |
| ( )       | parentheses                                    |
| #         | pound sign                                     |
| +         | plus sign                                      |
| -         | minus sign (hyphen)                            |
| .         | dot                                            |
| !         | exclamation mark                               |
| \|        | pipe (see also escaping pipe in tables)        |

### HTML

- se seu aplicativo suportar, colocar as tags no texto do seu arquivo formatado em Markdown

```
This **word** is bold. This <em>word</em> is italic.
```
