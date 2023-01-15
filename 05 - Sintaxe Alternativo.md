## Sintaxe Alternativo

A maioria das pessoas que usa o Markdown descobrirá que os elementos de sintaxe básicos e estendidos atendem às suas necessidades. Mas é provável que, se você usar o Markdown por tempo suficiente, inevitavelmente descobrirá que ele não suporta algo de que você precisa. Esta página fornece dicas e truques para contornar as limitações do Markdown.

Não é garantido que esses hacks funcionem em seu aplicativo Markdown. Se você precisar usar esses hacks com frequência, considere escrever usando algo diferente do Markdown.

## Sublinhado

O texto sublinhado não é algo que você normalmente vê na escrita na web, provavelmente porque o texto sublinhado é quase sinônimo de links. No entanto, se você estiver escrevendo um artigo ou relatório, talvez precise sublinhar palavras e frases. Alguns aplicativos, como [Bear](https://www.markdownguide.org/tools/bear/) e [Simplenote](https://www.markdownguide.org/tools/simplenote/), fornecem suporte para sublinhar texto, mas o Markdown não oferece suporte nativo ao sublinhado. Se o seu processador Markdown oferecer suporte a HTML, você poderá usar a tag HTML `<ins>` para sublinhar o texto em seu documento.

```html
Some of these words <ins>will be underlined</ins>.
```

Vai ficar:

Some of these words <ins>will be underlined</ins>.

## Identação (TAB)

Tabs e espaço em branco têm um significado especial no Markdown. Você pode usar espaços em branco à direita para criar quebras de linha e pode usar tabulações para criar blocos de código. Mas e se você precisar recuar um parágrafo à moda antiga, usando a tecla tab? Markdown não fornece uma maneira fácil de fazer isso.

Sua melhor aposta pode ser usar um editor Markdown que suporte recuo. Isso é comum em aplicativos mais voltados para editoração eletrônica. Por exemplo, o [iA Writer](https://www.markdownguide.org/tools/ia-writer/) permite personalizar as configurações de recuo do editor nas preferências do aplicativo. Ele também fornece opções de personalização de modelo para que você possa fazer com que o documento renderizado tenha a aparência que você espera, recuo e tudo.

Outra opção, se o seu processador Markdown for compatível com HTML, é usar a entidade HTML para espaço ininterrupto (`&nbsp;`). Esta provavelmente deve ser sua opção de último recurso, pois pode ficar estranho. Basicamente, cada `&nbsp;` em sua fonte Markdown será substituído por um espaço na saída renderizada. Portanto, se você inserir quatro instâncias de `&nbsp;` antes de um parágrafo, o parágrafo parecerá recuado quatro espaços.

```html
&nbsp;&nbsp;&nbsp;&nbsp;This is the first sentence of my indented paragraph.
```

Vai ficar:

&nbsp;&nbsp;&nbsp;&nbsp;This is the first sentence of my indented paragraph.

## Centralizar

Ter a capacidade de centralizar o texto é uma necessidade ao escrever um artigo ou relatório. Infelizmente, o Markdown não possui nenhum conceito de alinhamento de texto (uma possível exceção é ao usar tabelas). A boa notícia é que existe uma tag HTML que você pode usar: `<center>`. Se o seu processador Markdown oferecer suporte a HTML, você poderá colocar essas tags em torno de qualquer texto que deseja alinhar ao centro.

```html
<center>This text is centered.</center>
```

Vai ficar:

<center>This text is centered.</center>

A tag HTML `<center>` é tecnicamente suportada, mas oficialmente obsoleta, o que significa que funciona por enquanto, mas você não deveria usá-la. Infelizmente, não há outra alternativa HTML pura. Você pode tentar usar uma das alternativas CSS. Nem todos os aplicativos Markdown fornecem suporte a CSS, mas se o que você está usando oferece, aqui está uma alternativa para a tag `<center>`:

```html
<p style="text-align:center">Center this text</p>
```

Vai ficar:

<p style="text-align:center">Center this text</p>

## Cores

O Markdown não permite que você altere a cor do texto, mas se o seu processador Markdown suportar HTML, você pode usar a tag HTML `<font>`. O atributo color permite especificar a cor da fonte usando o nome de uma cor ou o código hexadecimal #RRGGBB.

```html
<font color="red">This text is red!</font>
```

Vai ficar:

<font color="red">This text is red!</font>

A tag HTML `<font>` é tecnicamente suportada, mas oficialmente obsoleta, o que significa que funciona por enquanto, mas você não deveria usá-la. Infelizmente, não há outra alternativa HTML pura. Você pode tentar usar uma das alternativas CSS. Nem todos os aplicativos Markdown fornecem suporte a CSS, mas se o que você está usando oferece, aqui está uma alternativa para a tag `<font>`:

```html
<p style="color:blue">Make this text blue.</p>
```

Vai ficar:

<p style="color:blue">Make this text blue.</p>

## Comentários

Algumas pessoas precisam da capacidade de escrever frases em seus arquivos Markdown que não aparecerão na saída renderizada. Esses comentários são essencialmente texto oculto. O texto pode ser visualizado pelo autor do documento, mas não é impresso na página da Web ou PDF. O Markdown não oferece suporte nativo a comentários, mas vários indivíduos empreendedores criaram uma solução.

Para adicionar um comentário, coloque o texto entre colchetes seguido de dois pontos, um espaço e um sinal de libra (por exemplo, [comentário]: #). Você deve colocar linhas em branco antes e depois de um comentário.

```
Here's a paragraph that will be visible.

[This is a comment that will be hidden.]: #

And here's another paragraph that's visible.
```

Vai parecer:

Here's a paragraph that will be visible.

[this is a comment that will be hidden.]: #

And here's another paragraph that's visible.

## Advertências

Advertências são freqüentemente usadas em documentação para chamar a atenção para advertências, notas e dicas. O Markdown não fornece sintaxe especial para advertências, e a maioria dos aplicativos Markdown não oferece suporte para advertências (uma exceção é o [MkDocs](https://www.markdownguide.org/tools/mkdocs/)).

No entanto, se você precisar adicionar advertências, poderá usar aspas com emoji e ênfase para criar algo semelhante às advertências que você vê em outros sites.

No entanto, se você precisar adicionar advertências, poderá usar aspas com emoji e ênfase para criar algo semelhante às advertências que você vê em outros sites.

```
> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.
```

Vai ficar:

> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.

## Tamanhos da imagem

A sintaxe Markdown para imagens não permite que você especifique a largura e a altura das imagens. Se você precisar redimensionar uma imagem e seu processador Markdown suportar HTML, você pode usar a tag HTML `img` com os atributos de largura e altura para definir as dimensões de uma imagem em pixels.

```html
<img src="image.png" width="200" height="100" />
```

A saída renderizada conterá a imagem redimensionada para as dimensões especificadas.

## Legenda para imagens

Markdown não oferece suporte nativo a legendas de imagens, mas há duas soluções possíveis. Se seu aplicativo Markdown oferecer suporte a HTML, você poderá usar as tags HTML figure e figcaption para adicionar uma legenda à sua imagem.

```html
<figure>
  <img src="/assets/images/albuquerque.jpg" alt="Albuquerque, New Mexico" />
  <figcaption>A single track trail outside of Albuquerque, New Mexico.</figcaption>
</figure>
```

Vai parecer:

<figure>
    <img src="images/albuquerque.jpg"
         alt="Albuquerque, New Mexico">
    <figcaption>A single track trail outside of Albuquerque, New Mexico.</figcaption>
</figure>

Se o seu aplicativo Markdown não oferece suporte a HTML, você pode tentar colocar a legenda diretamente abaixo da imagem e usar ênfase.

```
![Albuquerque, New Mexico](/assets/images/albuquerque.jpg)
*A single track trail outside of Albuquerque, New Mexico.*
```

Vai parecer:

![Albuquerque, New Mexico](images/albuquerque.jpg)
_A single track trail outside of Albuquerque, New Mexico._

## Alvos de links

Algumas pessoas gostam de criar links que abrem em novas abas ou janelas. A sintaxe Markdown para links não permite que você especifique o atributo de destino, mas se seu processador Markdown suportar HTML, você pode usar HTML para criar esses links.

```
<a href="https://www.markdownguide.org" target="_blank">Learn Markdown!</a>
```

Vai parecer:

<a href="https://www.markdownguide.org" target="_blank">Learn Markdown!</a>

## Símbolos

Markdown não fornece sintaxe especial para símbolos. No entanto, na maioria dos casos, você pode copiar e colar qualquer símbolo que deseja usar em seu documento Markdown. Por exemplo, se você precisar exibir Pi (π), basta encontrar o símbolo em uma página da Web e copiá-lo e colá-lo em seu documento. O símbolo deve aparecer como esperado na saída renderizada.

Como alternativa, se seu aplicativo Markdown oferecer suporte a HTML, você poderá usar a entidade HTML para qualquer símbolo que desejar. Por exemplo, se você deseja exibir o sinal de direitos autorais (©), pode copiar e colar a entidade HTML para direitos autorais (&copy;) em seu documento Markdown.

Lista de símbolos:

- Copyright (©) — &copy;
- Registered trademark (®) — &reg;
- Trademark (™) — &trade;
- Euro (€) — &euro;
- Left arrow (←) — &larr;
- Up arrow (↑) — &uarr;
- Right arrow (→) — &rarr;
- Down arrow (↓) — &darr;
- Degree (°) — &#176;
- Pi (π) — &#960;

Para obter uma lista completa de entidades HTML disponíveis, consulte a [página da Wikipédia sobre entidades HTML](https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references).

## Formatação de tabelas

Tabelas de remarcação são notoriamente meticulosas. Você não pode usar muitos elementos de sintaxe Markdown para formatar o texto nas células da tabela. Mas há soluções alternativas para pelo menos dois problemas comuns de tabela: quebras de linha e listas.

### Quebra de linhas nas células

Você pode separar parágrafos em uma célula de tabela usando uma ou mais tags `<br>` HTML.

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title |
| Paragraph   | First paragraph. <br><br> Second paragraph. |
```

Vai aparecer como:

| Syntax    | Description                                 |
| --------- | ------------------------------------------- |
| Header    | Title                                       |
| Paragraph | First paragraph. <br><br> Second paragraph. |

### Listas dentro das células

Você pode adicionar uma lista dentro de uma célula da tabela usando tags HTML.

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title |
| List        | Here's a list! <ul><li>Item one.</li><li>Item two.</li></ul> |
```

Vai parecer como:

| Syntax | Description                                                  |
| ------ | ------------------------------------------------------------ |
| Header | Title                                                        |
| List   | Here's a list! <ul><li>Item one.</li><li>Item two.</li></ul> |

## Índice

Alguns aplicativos Markdown, como o [Markdeep](https://www.markdownguide.org/tools/markdeep/), podem gerar automaticamente um sumário (também conhecido como sumário) a partir de seus cabeçalhos, mas esse não é um recurso fornecido por todos os aplicativos Markdown. No entanto, se seu aplicativo Markdown oferecer suporte a IDs de título, você poderá criar um sumário para seu arquivo Markdown usando uma lista e alguns links.

```
#### Table of Contents

- [Underline](#underline)
- [Indent](#indent)
- [Center](#center)
- [Color](#color)
```

Vai parecer como:

#### Table of Contents

- [Underline](#underline)
- [Indent](#indent)
- [Center](#center)
- [Color](#color)

## Vídeos

Se seu aplicativo Markdown oferecer suporte a HTML, você poderá incorporar um vídeo em seu arquivo Markdown copiando e colando o código HTML fornecido por um site de vídeo como YouTube ou Vimeo. Se o seu aplicativo Markdown não oferece suporte a HTML, você não pode incorporar um vídeo, mas pode chegar perto adicionando uma imagem e um link para o vídeo. Você pode fazer isso com praticamente qualquer vídeo em qualquer serviço de vídeo.

Como o YouTube facilita isso, vamos usá-los como exemplo. Veja este vídeo, por exemplo: https://www.youtube.com/watch?v=8q2IjQOzVpE. A última parte da URL (8q2IjQOzVpE) é o ID do vídeo. Podemos pegar esse ID e colocá-lo no seguinte modelo:

```
[![Image alt text](https://img.youtube.com/vi/YOUTUBE-ID/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE-ID)
```

O YouTube gera automaticamente uma imagem para cada vídeo (https://img.youtube.com/vi/YOUTUBE-ID/0.jpg), para que possamos usar isso e vincular a imagem ao vídeo no YouTube. Após substituirmos o texto alternativo da imagem e adicionarmos o ID do vídeo, nosso exemplo fica assim:

```
[![Less Than Jake — Scott Farcas Takes It On The Chin](https://img.youtube.com/vi/PYCxct2e0zI/0.jpg)](https://www.youtube.com/watch?v=PYCxct2e0zI)
```

A saída será:

[![Less Than Jake — Scott Farcas Takes It On The Chin](https://img.youtube.com/vi/PYCxct2e0zI/0.jpg)](https://www.youtube.com/watch?v=PYCxct2e0zI)
