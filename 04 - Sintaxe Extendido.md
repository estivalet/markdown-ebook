## Sintaxe Extendido

A sintaxe básica descrita no documento de design original do Markdown adicionou muitos dos elementos necessários no dia a dia, mas não foi suficiente para algumas pessoas. É aí que entra a sintaxe estendida.

Vários indivíduos e organizações assumiram a responsabilidade de estender a sintaxe básica adicionando elementos adicionais como tabelas, blocos de código, realce de sintaxe, link automático de URL e notas de rodapé. Esses elementos podem ser habilitados usando uma linguagem de marcação leve que se baseia na sintaxe básica do Markdown ou adicionando uma extensão a um processador Markdown compatível.

## Markdown languages

Nem todos os aplicativos Markdown oferecem suporte a elementos de sintaxe estendidos. Você precisará verificar se a linguagem de marcação leve que seu aplicativo está usando suporta ou não os elementos de sintaxe estendida que você deseja usar. Caso contrário, ainda pode ser possível habilitar extensões em seu processador Markdown.

Aqui estão várias linguagens de marcação leves que são superconjuntos de Markdown. Eles incluem sintaxe básica e se baseiam nela adicionando elementos adicionais como tabelas, blocos de código, realce de sintaxe, link automático de URL e notas de rodapé. Muitos dos aplicativos Markdown mais populares usam uma das seguintes linguagens de marcação leves:

- CommonMark
- GitHub Flavored Markdown (GFM)
- Markdown Extra
- MultiMarkdown
- R Markdown

Existem dezenas de processadores Markdown disponíveis. Muitos deles permitem que você adicione extensões que permitem elementos de sintaxe estendidos. Verifique a documentação do seu processador para obter mais informações.

## Tabelas

Para adicionar uma tabela, use três ou mais hífens (---) para criar o cabeçalho de cada coluna e use barras verticais (|) para separar cada coluna. Para compatibilidade, você também deve adicionar um tubo em cada extremidade da linha.

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```

Fica parecido com:

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

> Dica: Criar tabelas com hífens e barras verticais pode ser tedioso. Para acelerar o processo, tente usar o [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) ou [AnyWayData Markdown Export](https://anywaydata.com/). Crie uma tabela usando a interface gráfica e, em seguida, copie o texto formatado em Markdown gerado em seu arquivo.

### Alinhamento

Você pode alinhar o texto nas colunas à esquerda, à direita ou ao centro adicionando dois pontos (:) à esquerda, à direita ou em ambos os lados dos hífens na linha do cabeçalho.

```
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```

Vai ficar:

| Syntax    | Description |   Test Text |
| :-------- | :---------: | ----------: |
| Header    |    Title    | Here's this |
| Paragraph |    Text     |    And more |

## Blocos de código protegidos

A sintaxe básica do Markdown permite criar blocos de código recuando as linhas em quatro espaços ou uma tabulação. Se você achar isso inconveniente, tente usar blocos de código protegidos. Dependendo do seu processador ou editor Markdown, você usará três crases (```) ou três tis (~~~) nas linhas antes e depois do bloco de código. A melhor parte? Você não precisa recuar nenhuma linha!

````
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````

Vai se parecer com:

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

### Realce de sintaxe

Muitos processadores Markdown suportam realce de sintaxe para blocos de código protegidos. Esse recurso permite que você adicione realce de cor para qualquer idioma em que seu código foi escrito. Para adicionar realce de sintaxe, especifique um idioma próximo aos crases antes do bloco de código cercado.

````
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````

Vai se parecer com:

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## Notas de rodapé

As notas de rodapé permitem adicionar notas e referências sem sobrecarregar o corpo do documento. Quando você cria uma nota de rodapé, um número sobrescrito com um link aparece onde você adicionou a referência da nota de rodapé. Os leitores podem clicar no link para pular para o conteúdo da nota de rodapé na parte inferior da página.

Para criar uma referência de nota de rodapé, adicione um cursor e um identificador entre colchetes ([^1]). Os identificadores podem ser números ou palavras, mas não podem conter espaços ou tabulações. Os identificadores apenas correlacionam a referência da nota de rodapé com a própria nota de rodapé — na saída, as notas de rodapé são numeradas sequencialmente.

Adicione a nota de rodapé usando outro cursor e número entre colchetes com dois pontos e texto ([^1]: Minha nota de rodapé.). Você não precisa colocar notas de rodapé no final do documento. Você pode colocá-los em qualquer lugar, exceto dentro de outros elementos, como listas, citações de bloco e tabelas.

```
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.
```

Vai se parecer com: VERIFICAR!!!!!!!!!!!

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

## Cabeçalhos com IDs

Muitos processadores Markdown oferecem suporte a IDs personalizados para cabeçalhos - alguns processadores Markdown os adicionam automaticamente. Adicionar IDs personalizados permite vincular diretamente aos cabeçalhos e modificá-los com CSS. Para adicionar um ID de título personalizado, coloque o ID personalizado entre chaves na mesma linha do título.

```
### My Great Heading {#custom-id}
```

O HTML ficará assim:

```html
<h3 id="custom-id">My Great Heading</h3>
```

### Referenciando cabeçalhos com IDs

Você pode criar links para títulos com IDs personalizados no arquivo criando um link padrão com um sinal de hashtag (#) seguido pelo ID do título personalizado. Estes são comumente referidos como links de âncora.

| Markdown                      | HTML                                     | Saída                                  |
| ----------------------------- | ---------------------------------------- | -------------------------------------- |
| `[Heading IDs](#heading-ids)` | `<a href="#heading-ids">Heading IDs</a>` | <a href="#heading-ids">Heading IDs</a> |

Outros sites podem vincular ao título adicionando o ID do título personalizado ao URL completo da página da Web (por exemplo, `[IDs do título](https://www.markdownguide.org/extended-syntax#heading-ids))`.

## Listas de definição

Alguns processadores Markdown permitem que você crie listas de definição de termos e suas definições correspondentes. Para criar uma lista de definições, digite o termo na primeira linha. Na próxima linha, digite dois pontos seguidos por um espaço e a definição.

```
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```

O HTML será:

```html
<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term.</dd>
  <dd>This is another definition of the second term.</dd>
</dl>
```

E a saída será:

<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>

## Tachado

Você pode tachar palavras colocando uma linha horizontal no centro delas. O resultado se parece ~~com isso~~. Este recurso permite que você indique que certas palavras são um erro que não deve ser incluído no documento. Para tachar palavras, use dois símbolos de til (~~) antes e depois das palavras.

```
~~The world is flat.~~ We now know that the world is round.
```

A saída será:

~~The world is flat.~~ We now know that the world is round.

## Lista de Tarefas

As listas de tarefas permitem que você crie uma lista de itens com caixas de seleção. Em aplicativos Markdown que oferecem suporte a listas de tarefas, as caixas de seleção serão exibidas ao lado do conteúdo. Para criar uma lista de tarefas, adicione traços (-) e colchetes com um espaço ([ ]) na frente dos itens da lista de tarefas. Para marcar uma caixa de seleção, adicione um x entre os colchetes ([x]).

```
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```

A saída será:

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

## Emoji

Há duas maneiras de adicionar emoji aos arquivos Markdown: copiar e colar o emoji em seu texto formatado em Markdown ou digitar códigos de acesso de emoji.

### Copy/paste

Na maioria dos casos, você pode simplesmente copiar um emoji de uma fonte como a [Emojipedia](https://emojipedia.org/) e colá-lo em seu documento. Muitos aplicativos Markdown exibirão automaticamente o emoji no texto formatado em Markdown. Os arquivos HTML e PDF que você exporta de seu aplicativo Markdown devem exibir o emoji.

> Nota: Se você estiver usando um gerador de site estático, certifique-se de [codificar as páginas HTML como UTF-8](https://www.w3.org/International/tutorials/tutorial-char-enc/).

### Códigos de emoji

Alguns aplicativos Markdown permitem que você insira emoji digitando códigos de acesso emoji. Eles começam e terminam com dois pontos e incluem o nome de um emoji.

```
Gone camping! :tent: Be back soon.

That is so funny! :joy:
```

A saída será:

Gone camping! :tent: Be back soon.

That is so funny! :joy:

> Nota: Você pode usar esta [lista de códigos de acesso de emoji](https://gist.github.com/rxaviers/7360908), mas lembre-se de que os códigos de acesso de emoji variam de aplicativo para aplicativo. Consulte a documentação do aplicativo Markdown para obter mais informações.

## Realce

Isso não é comum, mas alguns processadores Markdown permitem que você destaque o texto. O resultado se parece <mark>com isso</mark>. Para destacar palavras, use dois sinais de igual (==) antes e depois das palavras.

```
I need to highlight these ==very important words==.
```

Vai se parecer com:

I need to highlight these <mark>very important words</mark>.

Como alternativa, se seu aplicativo Markdown oferecer suporte a HTML, você poderá usar a tag `mark` do HTML.

```html
I need to highlight these <mark>very important words</mark>.
```

## Subscrito

Isso não é comum, mas alguns processadores Markdown permitem que você use o subscrito para posicionar um ou mais caracteres um pouco abaixo da linha normal do tipo. Para criar um subscrito, use um símbolo de til (~) antes e depois dos caracteres.

```
H~2~O
```

A saída será:

H<sub>2</sub>O

> Nota: Certifique-se de testar isso em seu aplicativo Markdown antes de usá-lo. Alguns aplicativos Markdown usam um símbolo de til antes e depois das palavras não para subscrito, mas para tachado.

De forma alternativa podemos usar a tag `<sub>` do HTML.

```html
H<sub>2</sub>O
```

## Sobrescrito

Isso não é comum, mas alguns processadores Markdown permitem que você use o sobrescrito para posicionar um ou mais caracteres um pouco acima da linha normal do tipo. Para criar um sobrescrito, use um símbolo de circunflexo (^) antes e depois dos caracteres.

```
X^2^
```

A saída será:

X<sup>2</sup>

De forma alternativa podemos usar a tag `<sup>` do HTML.

```html
X<sup>2</sup>
```

## Link de URL automático

Muitos processadores Markdown transformam URLs em links automaticamente. Isso significa que, se você digitar http://www.example.com, seu processador Markdown o transformará automaticamente em um link, mesmo que você não tenha usado colchetes.

```
http://www.example.com
```

A saída será:

http://www.example.com

## Desabilitando Link de URL automático

Se você não deseja que um URL seja vinculado automaticamente, pode remover o link denotando o URL como código com backticks.

```
`http://www.example.com`
```

A saída será:

`http://www.example.com`
