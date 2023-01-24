## Sintaxe Básico

Quase todos os aplicativos Markdown suportam a sintaxe básica descrita no documento de design original do Markdown. Existem pequenas variações e discrepâncias entre os processadores Markdown que serão descritas superficialmente.

## Cabeçalhos

Para criar um título, adicione um _hashtag_ (#) na frente de uma palavra ou frase. O número de _hashtags_ que você usa deve corresponder ao nível do título. Por exemplo, para criar um título de nível três (`<h3>`), use três _hashtags_ (por exemplo, `### My Header`).

| Markdown               | HTML                       | Saída                    |
| ---------------------- | -------------------------- | ------------------------ |
| # Heading level 1      | `<h1>Heading level 1</h1>` | <h1>Heading level 1</h1> |
| ## Heading level 2     | `<h2>Heading level 2</h2>` | <h2>Heading level 2</h2> |
| ### Heading level 3    | `<h3>Heading level 3</h3>` | <h3>Heading level 3</h3> |
| #### Heading level 4   | `<h4>Heading level 4</h4>` | <h4>Heading level 4</h4> |
| ##### Heading level 5  | `<h5>Heading level 5</h5>` | <h5>Heading level 5</h5> |
| ###### Heading level 6 | `<h6>Heading level 6</h6>` | <h6>Heading level 6</h6> |

### Sintaxe alternativo

Como alternativa, na linha abaixo do texto, adicione qualquer número de caracteres == para o nível 1 do título ou caracteres -- para o nível 2 do título.

| Markdown                              | HTML                       | Saída                    |
| ------------------------------------- | -------------------------- | ------------------------ |
| Heading level 1 <br>==========        | `<h1>Heading level 1</h1>` | <h1>Heading level 1</h1> |
| Heading level 2 <br>----------------- | `<h2>Heading level 2</h2>` | <h2>Heading level 2</h2> |

### Melhores práticas

Os aplicativos Markdown não concordam em como lidar com um espaço ausente entre os _hashtags_ (#) e o texto do cabeçalho. Para compatibilidade, sempre coloque um espaço entre os _hashtags_ e o texto do cabeçalho.

| ✅ Faça assim      | ❌Não faça assim  |
| ------------------ | ----------------- |
| # Here's a Heading | #Here's a Heading |

Você também deve colocar linhas em branco antes e depois de um cabeçalho para questões de compatibilidade.

| ✅ Faça assim                                                                                 | ❌Não faça assim                                                                |
| --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Coloque uma linha em branco antes...<br/><br/># Heading<br/><br/>...e uma depois do cabeçalho | Sem linhas em branco, pode aparecer desformatado.<br/># Heading. Não faça assim |

## Parágrafos

Para criar parágrafos, use uma linha em branco para separar uma ou mais linhas de texto.

| Markdown                                                             | HTML                                                                          | Saída                                                                |
| -------------------------------------------------------------------- | ----------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Eu gosto de usar Markdown                                            | `<p>Eu gosto de usar Markdown</p>`                                            | Eu gosto de usar Markdown                                            |
| Acho que vou formatar<br/>todos os meus documentos a partir de agora | `<p>Acho que vou formatar<br/>todos os meus documentos a partir de agora</p>` | Acho que vou formatar<br/>todos os meus documentos a partir de agora |

### Melhores práticas

A menos que o parágrafo esteja em uma lista, não indente os parágrafos com espaços ou tabulações.

| ✅ Faça assim                                         | ❌Não faça assim                                   |
| ----------------------------------------------------- | -------------------------------------------------- |
| Don't put tabs or spaces in front of your paragraphs. | This can result in unexpected formatting problems. |
| Keep lines left-aligned like this.                    | Don't add tabs or spaces in front of paragraphs.   |

## Quebra de linhas

Para criar uma quebra de linha ou nova linha (`<br>`), finalize uma linha com dois ou mais espaços e adicione um return.

| Markdown                                                             | HTML                                                                 | Saída                                                     |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | --------------------------------------------------------- |
| This is the first line.&nbsp;&nbsp; <br>And this is the second line. | `<p>`This is the first line.`<br>`And this is the second line.`</p>` | This is the first line.<br/> And this is the second line. |

### Melhores práticas

Você pode usar dois ou mais espaços (comumente chamados de “espaço em branco à direita”) para quebras de linha em quase todos os aplicativos Markdown, mas isso é controverso. É difícil ver espaços em branco à direita em um editor, e muitas pessoas acidentalmente ou intencionalmente colocam dois espaços após cada frase. Por esse motivo, você pode querer usar algo diferente de espaços em branco à direita para quebras de linha. Se seu aplicativo Markdown oferecer suporte a HTML, você poderá usar a tag HTML `<br>`.

Para compatibilidade, use espaço em branco à direita ou a tag HTML `<br>` no final da linha.

Existem duas outras opções que não é recomendado usar. CommonMark e algumas outras linguagens de marcação leves permitem que você digite uma barra invertida (`\`) no final da linha, mas nem todos os aplicativos Markdown oferecem suporte a isso, portanto, não é a melhor opção do ponto de vista da compatibilidade. E pelo menos algumas linguagens de marcação leves não exigem nada no final da linha - basta digitar return e elas criarão uma quebra de linha.

| ✅ Faça assim                                                       | ❌Não faça assim                                          |
| ------------------------------------------------------------------- | --------------------------------------------------------- |
| First line with two spaces after.&nbsp;&nbsp;<br>And the next line. | First line with a backslash after.\<br>And the next line. |
| First line with the HTML tag after.`<br>`<br>And the next line.     | First line with nothing after.<br/>And the next line.     |

## Formatação

Você pode adicionar formatação colocando o texto em negrito ou itálico.

### Negrito

Para texto em negrito, adicione dois asteriscos ou sublinhados antes e depois de uma palavra ou frase. Para dar ênfase ao meio de uma palavra, adicione dois asteriscos sem espaços ao redor das letras.

| Markdown                     | HTML                                        | Saída                      |
| ---------------------------- | ------------------------------------------- | -------------------------- |
| I just love `**bold text**`. | I just love `<strong>`bold text`</strong>`. | I just love **bold** text. |
| I just love `__bold text__`. | I just love `<strong>`bold text`</strong>`. | I just love **bold** text. |
| Love`**is**`bold.            | Love`<strong>`is`</strong>`bold.            | Love**is**bold.            |

#### Melhores práticas

Os aplicativos Markdown não concordam sobre como lidar com sublinhados no meio de uma palavra. Para compatibilidade, use asteriscos em negrito no meio de uma palavra para dar ênfase.

| ✅ Faça assim    | ❌Não faça assim |
| ---------------- | ---------------- |
| Love`**is**`bold | Love`__is__`bold |

### Itálico

Para colocar o texto em itálico, adicione um asterisco ou sublinhado antes e depois de uma palavra ou frase. Para colocar em itálico o meio de uma palavra para dar ênfase, adicione um asterisco sem espaços ao redor das letras.

| Markdown                               | HTML                                            | Saída                                       |
| -------------------------------------- | ----------------------------------------------- | ------------------------------------------- |
| Italicized text is the `*cat's meow*`. | Italicized text is the `<em>`cat's meow`</em>`. | Italicized text is the <em>cat’s meow</em>. |
| Italicized text is the `_cat's meow_`. | Italicized text is the `<em>`cat's meow`</em>`. | Italicized text is the <em>cat’s meow</em>. |
| A`*cat*meow`.                          | A`<em>cat</em>meow`.                            | A<em>cat</em>meow.                          |

#### Melhores práticas

Os aplicativos Markdown não concordam sobre como lidar com sublinhados no meio de uma palavra. Para compatibilidade, use asteriscos para colocar em itálico o meio de uma palavra para dar ênfase.

| ✅ Faça assim | ❌Não faça assim |
| ------------- | ---------------- |
| A`*cat*`meow  | A`_cat_`meow     |

### Negrito e itálico

Para enfatizar o texto com negrito e itálico ao mesmo tempo, adicione três asteriscos ou sublinhados antes e depois de uma palavra ou frase. Para colocar negrito e itálico no meio de uma palavra para dar ênfase, adicione três asteriscos sem espaços ao redor das letras.

| Markdown                                  | HTML                                                            | Saída                                   |
| ----------------------------------------- | --------------------------------------------------------------- | --------------------------------------- |
| This text is `***really important***`.    | This text is `<em><strong>`really important`</strong></em>`.    | This text is **_really important_**.    |
| This text is `___really important___`.    | This text is `<em><strong>`really important`</strong></em>`.    | This text is **_really important_**.    |
| This text is `**_really important_**`.    | This text is `<em><strong>`really important`</strong></em>`.    | This text is **_really important_**.    |
| This text is `*__really important__*`.    | This text is `<em><strong>`really important`</strong></em>`.    | This text is **_really important_**.    |
| This is really`***very***`important text. | This is really`<em><strong>`very`</strong></em>`important text. | This is really**_very_**important text. |

#### Melhores práticas

Os aplicativos Markdown não concordam sobre como lidar com sublinhados no meio de uma palavra. Para compatibilidade, use asteriscos para negrito e itálico no meio de uma palavra para dar ênfase.

| ✅ Faça assim    | ❌Não faça assim |
| ---------------- | ---------------- |
| A`***cat***`meow | A`___cat___`meow |

## Citações

Para criar um blockquote, adicione um > na frente de um parágrafo.

```
> A maior glória de viver não está em nunca cair, mas em nos levantar toda vez que caímos.
```

A saída será algo parecido com:

> A maior glória de viver não está em nunca cair, mas em nos levantar toda vez que caímos.

### Multiplos parágrafos

Citações podem conter vários parágrafos. Adicione um > nas linhas em branco entre os parágrafos.

```
> Dorothy a seguiu por muitos dos belos aposentos de seu castelo.
>
> A Bruxa ordenou que ela limpasse as panelas e chaleiras e varresse o chão e mantivesse o fogo alimentado com lenha.
```

A saída será algo do tipo:

> Dorothy a seguiu por muitos dos belos aposentos de seu castelo.
>
> A Bruxa ordenou que ela limpasse as panelas e chaleiras e varresse o chão e mantivesse o fogo alimentado com lenha.

### Citações aninhadas

Citações podem ser aninhadas. Adicione um >> na frente do parágrafo que deseja aninhar.

```
> Dorothy a seguiu por muitos dos belos aposentos de seu castelo.
>
>> A Bruxa ordenou que ela limpasse as panelas e chaleiras e varresse o chão e mantivesse o fogo alimentado com lenha.
```

A saída será algo do tipo:

> Dorothy a seguiu por muitos dos belos aposentos de seu castelo.
>
> > A Bruxa ordenou que ela limpasse as panelas e chaleiras e varresse o chão e mantivesse o fogo alimentado com lenha.

### Citações com outros elementos

Citações podem conter outros elementos usando a formatação Markdown. Nem todos os elementos podem ser usados - você precisará experimentar para ver quais funcionam.

```
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

A saída será algo parecido com isso:

> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>   _Everything_ is going according to **plan**.

### Melhores práticas

| ✅ Faça assim                                                                                     | ❌Não faça assim                                                                            |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Try to put a blank line before...<br><br>> This is a blockquote<br><br>...and after a blockquote. | Without blank lines, this might not look right.<br>> This is a blockquote<br>Don't do this! |

## Listas

Você pode organizar itens em listas ordenadas e não ordenadas.

### Listas ordenadas

Para criar uma lista ordenada, adicione itens de linha com números seguidos de pontos. Os números não precisam estar em ordem numérica, mas a lista deve começar com o número um.

| Markdown                                                                                                                                                   | HTML                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Saída                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item                                                                                         | `<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ol>`                                                                                                                                                                                                                                                                                                                                                          | 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item                                                                                         |
| 1. First item<br>1. Second item<br>1. Third item<br>1. Fourth item                                                                                         | `<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ol>`                                                                                                                                                                                                                                                                                                                                                          | 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item                                                                                         |
| 1. First item<br>8. Second item<br>3. Third item<br>5. Fourth item                                                                                         | `<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ol>`                                                                                                                                                                                                                                                                                                                                                          | 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item                                                                                         |
| 1. First item<br>2. Second item<br>3. Third item<br>&nbsp;&nbsp;&nbsp;&nbsp;1. Indented item<br>&nbsp;&nbsp;&nbsp;&nbsp;2. Indented item<br>4. Fourth item | `<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Indented item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Indented Item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`</ol>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ol>` | 1. First item<br>2. Second item<br>3. Third item<br>&nbsp;&nbsp;&nbsp;&nbsp;1. Indented item<br>&nbsp;&nbsp;&nbsp;&nbsp;2. Indented item<br>4. Fourth item |

#### Melhores práticas

CommonMark e algumas outras linguagens de marcação leves permitem que você use um parêntese (`)`) como um delimitador (por exemplo, `1) Primeiro item`), mas nem todos os aplicativos Markdown oferecem suporte a isso, portanto, não é uma boa prática do ponto de vista da compatibilidade. Para compatibilidade, use apenas pontos.

| ✅ Faça assim                       | ❌Não faça assim                    |
| ----------------------------------- | ----------------------------------- |
| 1. Primeiro item<br>2. Segundo item | 1) Primeiro item<br>2) Segundo item |

### Listas não ordenadas

o crie uma lista não ordenada, adicione traços (-), asteriscos (\*) ou sinais de mais (+) na frente dos itens de linha. Recue um ou mais itens para criar uma lista aninhada.

| Markdown                                                                                                                                             | HTML                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Saída                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| - First item<br>- Second item<br>- Third item<br>- Fourth item                                                                                       | `<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ul>`                                                                                                                                                                                                                                                                                                                                                          | <li> First item<br><li> Second item<br><li> Third item<br><li> Fourth item                                                                         |
| _ First item<br>_ Second item<br>_ Third item<br>_ Fourth item                                                                                       | `<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ul>`                                                                                                                                                                                                                                                                                                                                                          | <li> First item<br><li> Second item<br><li> Third item<br><li> Fourth item                                                                         |
| + First item<br>+ Second item<br>+ Third item<br>+ Fourth item                                                                                       | `<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ul>`                                                                                                                                                                                                                                                                                                                                                          | <li> First item<br><li> Second item<br><li> Third item<br><li> Fourth item                                                                         |
| - First item<br>- Second item<br>- Third item<br>&nbsp;&nbsp;&nbsp;&nbsp;- Indented item<br>&nbsp;&nbsp;&nbsp;&nbsp;- Indented item<br>- Fourth item | `<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`First item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Second item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Third item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Indented item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Indented Item`</li>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`</ul>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<li>`Fourth item`</li>`<br>`</ul>` | <ul><li> First item</li><li> Second item</li><li> Third item</li><ul><li> Indented item</li><li> Indented item</li></ul><li> Fourth item</li></ul> |

#### Iniciando listas não ordenadas com números

Se você precisar iniciar um item de lista não ordenada com um número seguido por um ponto, poderá usar uma barra invertida (`\`) para escapar o ponto.

| Markdown                                                    | HTML                                                                                                | Saída                                                                       |
| ----------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| - 1968`\`. A great year!<br>- I think 1969 was second best. | `<ul>`<br>`<li>`1968. A great year!`</li>`<br>`<li>`I think 1969 was second best.`</li>`<br>`</ul>` | <ul><li>1968. A great year!</li><li>I think 1969 was second best.</li></ul> |

#### Melhores práticas

Os aplicativos Markdown não concordam em como lidar com diferentes delimitadores na mesma lista. Para compatibilidade, não misture e combine delimitadores na mesma lista - escolha um e fique com ele.

| ✅ Faça assim                                                         | ❌Não faça assim                                                       |
| --------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| - Primeiro item<br>- Segundo item<br>- Terceiro item<br>- Quarto item | - Primeiro item<br>\* Segundo item<br>- Terceiro item<br>+ Quarto item |

### Adicionando elementos nas listas

Para adicionar outro elemento em uma lista preservando a continuidade da lista, recue o elemento quatro espaços ou uma tabulação, conforme mostrado nos exemplos a seguir.

#### Parágrafos

```
* This is the first list item.
* Here's the second list item.

    I need to add another paragraph below the second list item.

* And here's the third list item.
```

A saída será algo tipo:

- This is the first list item.
- Here's the second list item.

  I need to add another paragraph below the second list item.

- And here's the third list item.

#### Citações

```
* This is the first list item.
* Here's the second list item.

    > A blockquote would look great below the second list item.

* And here's the third list item.
```

A saída será alto tipo:

- This is the first list item.
- Here's the second list item.

  > A blockquote would look great below the second list item.

- And here's the third list item.

#### Blocos de código

Os blocos de código são normalmente recuados com quatro espaços ou uma tabulação. Quando estiverem em uma lista, recue oito espaços ou duas tabulações.

```
1. Open the file.
2. Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3. Update the title to match the name of your website.
```

A saída será algo tipo:

1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.

#### Imagens

```
1. Open the file containing the Linux mascot.
2. Marvel at its beauty.

    ![Tux, the Linux mascot](/assets/images/tux.png)

3. Close the file.
```

A saída será algo parecido com:

1. Open the file containing the Linux mascot.
2. Marvel at its beauty.

   ![Tux, the Linux mascot](images/tux.jpg)

3. Close the file.

#### Listas

Você pode aninhar uma lista não ordenada em uma lista ordenada ou vice-versa.

```
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item
```

A saída será algo parecido com:

1. First item
2. Second item
3. Third item
   - Indented item
   - Indented item
4. Fourth item

## Código-fonte

Para denotar uma palavra ou frase como código, coloque-a entre acentos graves (`).

| Markdown                              | HTML                                               | Saída                                          |
| ------------------------------------- | -------------------------------------------------- | ---------------------------------------------- |
| At the command prompt, type \`nano\`. | At the command prompt, type `<code>`nano`</code>`. | At the command prompt, type <code>nano</code>. |

### Escapando os acentos graves

Se a palavra ou frase que deseja denotar como código incluir um ou mais acentos graves, você pode escapá-la colocando a palavra ou frase entre acentos graves duplos (``).

| Markdown                                | HTML                                                 | Saída                                            |
| --------------------------------------- | ---------------------------------------------------- | ------------------------------------------------ |
| `` Use `code` in your Markdown file. `` | `<code>`Use \`code\` in your Markdown file.`</code>` | <code>Use \`code\` in your Markdown file.</code> |

## Blocos de código-fonte

Para criar blocos de código, recue cada linha do bloco em pelo menos quatro espaços ou uma tabulação.

```
    <html>
      <head>
      </head>
    </html>
```

A saída será algo tipo:

```
<html>
    <head>
    </head>
</html>
```

## Linhas horizontais

Para criar uma régua horizontal, use três ou mais asteriscos (\*\*\*), hífens (---) ou sublinhados (\_\_\_) sozinhos em uma linha.

```
***

---

_________________
```

A saída será algo tipo:

---

### Melhores práticas

Para compatibilidade, coloque linhas em branco antes e depois das linhas horizontais.

| ✅ Faça assim                                                                       | ❌Não faça assim                                                       |
| ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Try to put a blank line before...<br><br>---<br><br>...and after a horizontal rule. | Without blank lines, this would be a heading.<br>---<br>Don't do this! |

## Links

Para criar um link, coloque o texto do link entre colchetes (por exemplo, [Duck Duck Go]) e siga-o imediatamente com o URL entre parênteses (por exemplo, (https://duckduckgo.com)).

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com).
```

A saída será algo parecido com:

My favorite search engine is [Duck Duck Go](https://duckduckgo.com).

### Adicionando títulos

Opcionalmente, você pode adicionar um título para um link. Isso aparecerá como uma dica de ferramenta quando o usuário passar o mouse sobre o link. Para adicionar um título, coloque-o entre aspas após o URL.

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").
```

A sapida será algo parecido com:

My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").

### URLs e e-mails

Para transformar rapidamente um URL ou endereço de e-mail em um link, coloque-o entre colchetes angulares.

```
<https://www.markdownguide.org>
<fake@example.com>
```

A saída será algo parecido com:

<https://www.markdownguide.org>  
<fake@example.com>

### Formatando links

Para enfatizar os links, adicione asteriscos antes e depois dos colchetes e parênteses. Para denotar links como código, adicione acentos graves entre colchetes.

```
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).
```

A saída será algo parecido com:

I love supporting the **[EFF](https://eff.org)**.  
This is the _[Markdown Guide](https://www.markdownguide.org)_.  
See the section on [`code`](#code).

### Links de referência

Os links de estilo de referência são um tipo especial de link que torna os URLs mais fáceis de exibir e ler no Markdown. Os links de estilo de referência são construídos em duas partes: a parte que você mantém alinhada com o seu texto e a parte que você armazena em outro lugar no arquivo para manter o texto fácil de ler.

#### Formatando a primeira parte do link

A primeira parte de um link de estilo de referência é formatada com dois conjuntos de colchetes. O primeiro conjunto de colchetes envolve o texto que deve aparecer vinculado. O segundo conjunto de colchetes exibe um rótulo usado para apontar para o link que você está armazenando em outro lugar do documento.

Embora não seja obrigatório, você pode incluir um espaço entre o primeiro e o segundo conjunto de colchetes. O rótulo no segundo conjunto de colchetes não diferencia maiúsculas de minúsculas e pode incluir letras, números, espaços ou pontuação.

Isso significa que os seguintes formatos de exemplo são aproximadamente equivalentes para a primeira parte do link:

- [hobbit-hole][1]
- [hobbit-hole] [1]

#### Formatando a segunda parte do link

A segunda parte de um link de estilo de referência é formatada com os seguintes atributos:

1. O rótulo, etre colchetes, seguido imediatamente por dois pontos e pelo menos um espaço (por exemplo, [rótulo]: ).
2. A URL do link, que você pode opcionalmente colocar entre colchetes angulares.
3. O título opcional do link, que pode ser colocado entre aspas duplas, aspas simples ou parênteses.

Isso significa que os seguintes formatos de exemplo são aproximadamente equivalentes para a segunda parte do link:

```
- [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle
- [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
- [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
- [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
- [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
- [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
- [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
```

Você pode colocar esta segunda parte do link em qualquer lugar do documento Markdown. Algumas pessoas os colocam imediatamente após o parágrafo em que aparecem, enquanto outras pessoas os colocam no final do documento (como notas de fim ou notas de rodapé).

#### Exemplo juntando as duas partes

Digamos que você adicione um URL como um link de URL padrão a um parágrafo e fique assim no Markdown:

```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.
```

Embora possa apontar para informações adicionais interessantes, o URL exibido realmente não acrescenta muito ao texto bruto existente, além de torná-lo mais difícil de ler. Para corrigir isso, você pode formatar o URL assim:

```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole][1], and that means comfort.

[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
```

Em ambas as instâncias acima, a saída renderizada seria idêntica:

> In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
> of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
> eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.

e a saída HTML seria:

```
<a href="https://en.wikipedia.org/wiki/Hobbit#Lifestyle" title="Hobbit lifestyles">hobbit-hole</a>
```

#### Melhores práticas

Os aplicativos Markdown não concordam sobre como lidar com espaços no meio de uma URL. Para compatibilidade, tente codificar o URL de todos os espaços com %20. Como alternativa, se seu aplicativo Markdown oferecer suporte a HTML, você poderá usar a tag HTML.

| ✅ Faça assim                                                                                                         | ❌Não faça assim                                |
| --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| `[link](https://www.example.com/my%20great%20page)`<br><br>`<a href="https://www.example.com/my great page">link</a>` | `[link](https://www.example.com/my great page)` |

## Imagens

Para adicionar uma imagem, adicione um ponto de exclamação (!), seguido de um texto alternativo entre colchetes e o caminho ou URL para o recurso de imagem entre parênteses. Opcionalmente, você pode adicionar um título entre aspas após o caminho ou URL.

```
![The San Juan Mountains are beautiful!](/assets/images/san-juan-mountains.jpg "San Juan Mountains")
```

A saída será:

![The San Juan Mountains are beautiful!](./images/san-juan-mountains.jpg "San Juan Mountains")

### Links para imagens

Para adicionar um link a uma imagem, coloque o Markdown da imagem entre colchetes e adicione o link entre parênteses.

```
[![An old rock in the desert](/assets/images/shiprock.jpg "Shiprock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)
```

A saída será:

[![An old rock in the desert](images/shiprock.jpg "Shiprock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)

## Caracteres de escape

Para exibir um caractere literal que seria usado para formatar texto em um documento Markdown, adicione uma barra invertida (\\) na frente do caractere.

```
\* Without the backslash, this would be a bullet in an unordered list.
```

A saída será:

\* Without the backslash, this would be a bullet in an unordered list.

### Caracteres que podem ser escapados

Você pode usar uma barra invertida para escapar dos seguintes caracteres.

| Caracter | Nome                   |
| -------- | ---------------------- |
| \        | contra-barra           |
| `        | agudo                  |
| \*       | asterisco              |
| \_       | sublinhado             |
| { }      | chaves                 |
| [ ]      | colchetes              |
| < >      | sinal maior menor      |
| ( )      | parênteses             |
| #        | hashtag                |
| +        | sinal de mais          |
| -        | sinal de menos (hífen) |
| .        | ponto                  |
| !        | exclamação             |
| \|       | barra vertical         |

## HTML

Muitos aplicativos Markdown permitem que você use tags HTML em texto formatado em Markdown. Isso é útil se você preferir determinadas tags HTML à sintaxe Markdown. Por exemplo, algumas pessoas acham mais fácil usar tags HTML para imagens. Usar HTML também é útil quando você precisa alterar os atributos de um elemento, como especificar a cor do texto ou alterar a largura de uma imagem.

Para usar HTML, coloque as tags no texto do seu arquivo formatado em Markdown.

```
This **word** is bold. This <em>word</em> is italic.
```

A saída será:

This **word** is bold. This <em>word</em> is italic.

### Melhores práticas

Por motivos de segurança, nem todos os aplicativos Markdown oferecem suporte a HTML em documentos Markdown. Em caso de dúvida, verifique a documentação do seu aplicativo Markdown. Alguns aplicativos suportam apenas um subconjunto de tags HTML.

Use linhas em branco para separar os elementos HTML em nível de bloco como `<div>`, `<table>`, `<pre>` e `<p>` do conteúdo ao redor. Tente não indentar as tags com tabulações ou espaços - isso pode interferir na formatação.

Você não pode usar a sintaxe Markdown dentro de tags HTML em nível de bloco. Por exemplo, `<p>itálico e **negrito**</p>` não funcionarão.
