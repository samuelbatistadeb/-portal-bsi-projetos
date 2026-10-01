# Portal da Turma — Página de Projetos

Página desenvolvida para a disciplina de Programação Web I, do 4º período de Sistemas de Informação.

O objetivo é apresentar os projetos da turma, as tecnologias utilizadas, uma linha do tempo dos conteúdos estudados e informações complementares.

Este documento explica a estrutura HTML, os principais recursos de CSS e o motivo das escolhas.

## 1. O que a página apresenta

- Cabeçalho com o nome do portal.
- Menu com links para as seis páginas.
- Introdução sobre os trabalhos da turma.
- Cards com informações dos projetos.
- Linha do tempo com os conteúdos estudados.
- Área de destaques com informações complementares.

## 2. Tecnologias utilizadas

| Tecnologia | Função | Exemplo no projeto |
| --- | --- | --- |
| HTML | Organizar o conteúdo e indicar o significado de cada elemento. | Criar títulos, parágrafos, links e imagens. |
| CSS | Definir a aparência e a organização visual. | Aplicar cores, espaçamentos e colunas. |

O trecho apresentado não utiliza JavaScript. Os links e a rolagem dos projetos funcionam com recursos do navegador e CSS.

**Explicação simples:** o HTML organiza as informações. O CSS define como elas aparecem na tela.

## 3. Como abrir a página

1. Salve o HTML da página, por exemplo, como `projetos.html`.
2. Mantenha o arquivo `style.css` na mesma pasta, caso utilize o caminho abaixo.
3. Dentro do `<head>`, adicione:

```html
<link rel="stylesheet" href="style.css">
```

4. Coloque as imagens na pasta indicada pelo atributo `src`.
5. Abra o HTML no navegador.

Se o CSS estiver dentro de uma pasta chamada `css`, o caminho deve ser:

```html
<link rel="stylesheet" href="css/style.css">
```

Os links para outras páginas dependem da existência dos arquivos correspondentes.

A fonte do Google Fonts depende de acesso à internet. O CSS também define fontes alternativas.

## 4. Principais tags HTML

Tags são marcações que identificam os elementos da página. Muitas possuem abertura e fechamento:

```html
<p>Este é um parágrafo.</p>
```

| Tag | Função | Uso no projeto |
| --- | --- | --- |
| `<html>` | Envolve o documento HTML. | Contém toda a página. |
| `<head>` | Reúne configurações e referências. | Codificação, título da aba, fonte e CSS. |
| `<meta>` | Define informações sobre o documento. | Codificação e configuração da área de visualização. |
| `<title>` | Define o título da aba do navegador. | Identifica a página na aba. |
| `<link>` | Referencia um recurso externo. | Conecta a fonte e a folha de estilos. |
| `<body>` | Contém o conteúdo da página. | Cabeçalho, projetos, linha do tempo e destaques. |
| `<header>` | Identifica um cabeçalho. | Nome do portal e menu. |
| `<nav>` | Identifica uma área de navegação. | Menu principal e links numerados dos projetos. |
| `<section>` | Agrupa um conteúdo por tema. | Introdução e área de projetos. |
| `<article>` | Representa um conteúdo individual. | Cada projeto tem seu próprio artigo. |
| `<aside>` | Identifica conteúdo complementar. | Informações de destaque sobre os projetos. |
| `<h1>`, `<h2>` e `<h3>` | Indicam níveis de títulos. | Títulos da página, das seções e dos projetos. |
| `<p>` | Define um parágrafo. | Descrições e informações dos destaques. |
| `<strong>` | Indica importância no texto. | Rótulos como “Próximos passos”. |
| `<a>` | Cria um link. | Páginas, repositórios e destinos dentro da página. |
| `<img>` | Insere uma imagem. | Capturas de tela dos projetos. |
| `<ul>` | Cria uma lista sem ordem numérica. | Menu e tecnologias utilizadas. |
| `<li>` | Representa um item de lista. | Cada link do menu ou tecnologia. |
| `<div>` | Agrupa elementos sem um significado temático específico. | Contêiner do carrossel e eventos. |
| `<span>` | Agrupa pequenos trechos de conteúdo. | Meses e bolinhas da linha do tempo. |
| `<table>` | Representa uma tabela. | Estrutura atual da linha do tempo. |
| `<tr>` | Representa uma linha da tabela. | Agrupa as células dos eventos. |
| `<td>` | Representa uma célula da tabela. | Contém um evento da linha do tempo. |

### Por que usar tags com significado?

Elas ajudam a identificar a função de cada parte da página.

Por exemplo:

- `<nav>` informa que aquele conjunto serve para navegação.
- `<article>` identifica o conteúdo de um projeto.
- `<aside>` identifica informações complementares.

**Importante:** `<aside>` não significa “colocar na lateral”. A posição do elemento depende do CSS.

Da mesma forma, diminuir um `<h1>` pelo CSS não transforma esse elemento em `<h3>`. A tag continua indicando o mesmo nível de título.

## 5. Atributos HTML

Atributos são informações adicionadas às tags.

```html
<article class="card-projeto" id="projeto1">
    <h3>Portal da Turma</h3>
</article>

<a href="#projeto1">1</a>
```

| Atributo | Explicação |
| --- | --- |
| `class="card-projeto"` | Permite aplicar o mesmo estilo a vários cards. |
| `id="projeto1"` | Identifica um elemento específico e deve ser único na página. |
| `href="#projeto1"` | Leva ao elemento com esse ID dentro da própria página. |
| `src="img/projeto1.png"` | Indica o caminho do arquivo da imagem. |
| `alt="Print do Portal da Turma"` | Fornece uma descrição textual da imagem. |
| `lang="pt-BR"` | Identifica o idioma como português do Brasil. |

### Diferença entre classe e ID

Uma classe pode aparecer em vários elementos:

```html
<article class="card-projeto"></article>
<article class="card-projeto"></article>
```

Um ID identifica um elemento específico:

```html
<article id="projeto1"></article>
<article id="projeto2"></article>
```

**Motivo da escolha:** as classes permitem reaproveitar estilos. Os IDs permitem apontar para projetos específicos.

## 6. Como ler uma regra CSS

```css
aside.destaques strong {
    display: block;
    margin-bottom: 6px;
    color: var(--azul);
    font-weight: 600;
}
```

Uma regra CSS possui:

- **Seletor:** indica quais elementos recebem o estilo.
- **Propriedade:** indica o que será alterado.
- **Valor:** define como a propriedade será aplicada.

Nesse exemplo:

| Parte | Significado |
| --- | --- |
| `aside.destaques strong` | Seleciona os elementos `<strong>` dentro do aside com a classe `destaques`. |
| `display: block` | Faz o rótulo ocupar uma linha própria. |
| `margin-bottom: 6px` | Adiciona espaço abaixo do rótulo. |
| `color: var(--azul)` | Aplica a cor azul definida na variável. |
| `font-weight: 600` | Define o peso da fonte. |

### Seletores usados no projeto

| Seletor | O que seleciona |
| --- | --- |
| `*` | Todos os elementos. |
| `body` | O elemento `<body>`. |
| `.card-projeto` | Elementos com a classe `card-projeto`. |
| `#cabecalho` | O elemento com o ID `cabecalho`. |
| `.card-projeto img` | Imagens dentro dos cards. |
| `.card-projeto > a` | Links que são filhos diretos do card. |
| `aside.destaques p + p` | Um parágrafo imediatamente depois de outro parágrafo no aside. |

Quando várias regras atingem o mesmo elemento, o navegador usa a **cascata** para determinar o resultado. Essa decisão considera fatores como prioridade, especificidade e ordem das regras.

Por isso, a versão revisada substitui o CSS anterior, evitando regras antigas duplicadas.

## 7. Paleta de cores e tipografia

As cores seguem a identidade visual compartilhada da atividade.

| Variável | Cor | Uso principal |
| --- | --- | --- |
| `--azul` | `#1A3A5C` | Cabeçalho e títulos. |
| `--azul2` | `#2563A8` | Links e estados de interação. |
| `--azul3` | `#5B9BD5` | Bordas dos cards e bolinhas. |
| `--dourado` | `#C8922A` | Detalhes de destaque e foco. |
| `--fundo` | `#F5F7FA` | Fundo da página. |
| `--tinta` | `#1A1A2E` | Texto principal. |
| `--cinza` | `#5A6270` | Texto secundário. |
| `--linha` | `#D0D7E3` | Bordas e separadores. |
| `--branco` | `#FFFFFF` | Cards e texto do cabeçalho. |

### Variáveis CSS

As variáveis ficam em `:root`, que seleciona o elemento raiz do documento.

Exemplo reduzido:

```css
:root {
    --azul: #1A3A5C;
    --dourado: #C8922A;
    --branco: #FFFFFF;
}
```

A função `var()` usa o valor de uma variável:

```css
color: var(--azul);
```

**Motivo da escolha:** reutilizar as cores e facilitar alterações. Se uma variável mudar, as regras que usam essa variável acompanham a mudança.

### Fonte e leitura

```css
body {
    font-family: "Inter", Arial, sans-serif;
    font-size: 16px;
    line-height: 1.6;
    color: var(--tinta);
    background-color: var(--fundo);
}
```

- `font-family` define a fonte e suas alternativas.
- `font-size` define o tamanho básico do texto.
- `line-height` define a altura das linhas.
- `color` define a cor do texto.
- `background-color` define a cor de fundo.

**Motivo da escolha:** seguir a tipografia exigida pela atividade e manter uma leitura confortável.

## 8. Espaçamentos e medidas

| Propriedade | Explicação simples | Motivo do uso |
| --- | --- | --- |
| `padding` | Espaço entre o conteúdo e a borda. | Evitar texto colado às bordas. |
| `margin` | Espaço externo ao elemento. | Separar as áreas da página. |
| `gap` | Distância entre itens de Flexbox ou Grid. | Manter separação uniforme. |
| `max-width` | Define uma largura máxima. | Evitar conteúdo muito espalhado em telas grandes. |
| `border-radius` | Arredonda os cantos. | Dar acabamento discreto aos cards. |
| `box-sizing: border-box` | Inclui padding e borda na largura e altura definidas. | Tornar as medidas mais previsíveis. |

### Centralização

```css
max-width: 1140px;
margin: 0 auto;
```

A largura máxima limita o conteúdo. As margens laterais automáticas centralizam o bloco quando existe espaço disponível.

### Valores de espaçamento

```css
padding: 3rem 2rem;
```

- `3rem`: espaço superior e inferior.
- `2rem`: espaço nas laterais.

A unidade `rem` depende do tamanho da fonte do elemento raiz.

### Reset básico

```css
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
```

O reset remove margens e preenchimentos padrão para que o CSS do projeto defina os espaçamentos.

## 9. Cabeçalho e menu

O cabeçalho usa fundo azul e uma borda dourada.

O menu utiliza Flexbox:

```css
display: flex;
align-items: center;
justify-content: space-between;
flex-wrap: wrap;
gap: 18px;
```

| Propriedade | Função |
| --- | --- |
| `display: flex` | Organiza os elementos em um layout flexível. |
| `align-items: center` | Centraliza os itens no eixo transversal. |
| `justify-content: space-between` | Distribui o espaço entre os itens no eixo principal. |
| `flex-wrap: wrap` | Permite que os itens quebrem para outra linha. |
| `gap: 18px` | Define a distância entre os itens. |

Neste menu, o eixo principal é horizontal. Isso ajuda a organizar o nome do portal e os links lado a lado.

A propriedade `list-style: none` remove os marcadores visuais da lista, mantendo sua estrutura HTML.

**Motivo da escolha:** organizar a navegação e permitir que ela se adapte à largura disponível.

## 10. Cards e carrossel

```css
.carrossel {
    display: flex;
    gap: 24px;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    scroll-behavior: smooth;
    padding-bottom: 16px;
}
```

### Como funciona

- `display: flex` coloca os cards em sequência.
- `gap` separa os cards.
- `overflow-x: auto` permite rolagem horizontal quando o conteúdo não cabe.
- `scroll-snap-type` ajuda a alinhar os cards ao final da rolagem.
- `scroll-behavior: smooth` suaviza a rolagem por âncoras quando o navegador aplica esse comportamento.

Cada card também usa:

```css
scroll-snap-align: start;
```

Isso define o início do card como ponto de alinhamento.

O carrossel não troca os projetos automaticamente. O usuário acessa os demais projetos pela rolagem ou pelos links numerados.

### Largura dos cards

Em telas grandes:

```css
flex: 0 0 calc((100% - 48px) / 3);
```

- O primeiro `0` impede o crescimento pelo Flexbox.
- O segundo `0` impede a redução pelo Flexbox.
- O cálculo define a largura inicial de cada card.
- Os `48px` correspondem a dois espaços de `24px`.
- A divisão por três permite mostrar três cards por vez.

A função `calc()` realiza esse cálculo dentro do CSS.

### Organização interna

Dentro de cada card:

```css
display: flex;
flex-direction: column;
```

Isso organiza imagem, título, descrição, tecnologias e link verticalmente.

No link:

```css
margin-top: auto;
```

Essa margem usa o espaço livre acima do link, ajudando a mantê-lo na parte inferior do card.

**Motivo da escolha:** organizar os projetos de forma consistente e permitir acessar os demais sem JavaScript.

### Imagens dos projetos

```css
.card-projeto img {
    display: block;
    width: 100%;
    height: 180px;
    object-fit: contain;
    background-color: var(--fundo);
    border-radius: 5px;
    margin-bottom: 18px;
}
```

- `width: 100%` utiliza a largura interna disponível.
- `height: 180px` reserva uma área uniforme.
- `object-fit: contain` mostra a imagem inteira sem distorção.

O uso de `contain` pode deixar espaços vazios, mas evita cortar partes dos prints.

**Motivo da escolha:** preservar as informações das capturas de tela.

O CSS não corrige imagens ausentes ou caminhos errados.

## 11. Linha do tempo

A estrutura atual utiliza uma tabela. Cada célula contém:

- O mês.
- Uma bolinha.
- O nome do conteúdo estudado.

| Recurso | Função |
| --- | --- |
| `position: relative` na célula | Cria a referência para posicionar o segmento da linha. |
| `::after` | Cria o segmento visual pelo CSS. |
| `content: ""` | Permite exibir o pseudo-elemento sem texto. |
| `position: absolute` | Posiciona o segmento em relação à célula. |
| `:not(:last-child)` | Evita um segmento depois do último evento. |
| `border-radius: 50%` | Transforma o quadrado da bolinha em um círculo. |
| `z-index: 1` | Ajuda a manter a bolinha sobre o segmento. |

**Motivo do ajuste visual:** alinhar os eventos e utilizar as cores da turma.

**Limitação:** uma lista ordenada seria mais adequada para representar essa sequência cronológica. A revisão do CSS manteve a tabela existente.

## 12. Área de destaques: o aside

O aside reúne informações complementares sobre os projetos.

Um dos seus parágrafos é:

```html
<p>
    <strong>Próximos passos:</strong>
    Aprender JavaScript e desenvolver novos projetos.
</p>
```

- `<p>` organiza a informação como um parágrafo.
- `<strong>` indica a importância do rótulo.
- O CSS coloca o rótulo em uma linha própria.

### Organização com Grid

```css
aside.destaques {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 16px 24px;
    margin-top: 32px;
    padding: 24px;
    background-color: var(--branco);
    border: 1px solid var(--linha);
    border-left: 4px solid var(--dourado);
    border-radius: 8px;
}
```

### Explicação das principais regras

| Regra | Explicação |
| --- | --- |
| `display: grid` | Organiza o conteúdo em linhas e colunas. |
| `repeat(3, ...)` | Repete a definição de coluna três vezes. |
| `1fr` | Representa uma parte do espaço disponível. |
| `minmax(0, 1fr)` | Permite que a coluna diminua sem uma largura mínima imposta pelo conteúdo. |
| `gap: 16px 24px` | Separa linhas em 16px e colunas em 24px. |
| `border-left` | Cria o detalhe dourado à esquerda. |

Como as três colunas usam `1fr`, elas dividem igualmente o espaço disponível.

### Título ocupando toda a largura

```css
aside.destaques h3 {
    grid-column: 1 / -1;
    color: var(--azul);
    font-size: 21px;
}
```

`grid-column: 1 / -1` faz o título ocupar desde a primeira até a última linha da grade.

Assim, o título fica acima e os três parágrafos aparecem abaixo, um em cada coluna.

**Motivo da escolha:** aproveitar a largura disponível e separar visualmente as três informações.

O aside não recebe efeito de clique porque apresenta informações, sem funcionar como botão ou link.

## 13. Adaptação a telas menores

O CSS utiliza `@media` para aplicar regras conforme a largura da área de visualização.

| Largura | Cards visíveis por vez | Destaques |
| --- | --- | --- |
| Acima de 850px | Três. | Três colunas. |
| Acima de 600px e até 850px | Dois. | Três colunas. |
| Até 600px | Um. | Uma coluna. |

Exemplo:

```css
@media (max-width: 600px) {
    aside.destaques {
        grid-template-columns: 1fr;
        padding: 20px;
    }

    .card-projeto {
        flex-basis: 100%;
    }
}
```

Quando a largura é de até 600px:

- Os destaques ficam um abaixo do outro.
- Cada card ocupa a largura disponível.
- Os espaçamentos são reduzidos.
- A linha do tempo permite rolagem horizontal dentro do próprio componente.

O menu também pode quebrar para outra linha.

**Motivo da escolha:** manter o conteúdo legível em telas pequenas.

A regra considera a largura disponível, não o modelo do aparelho.

## 14. Interação e acessibilidade

| Recurso | Função |
| --- | --- |
| `:hover` | Altera a aparência quando o ponteiro passa sobre o elemento. |
| `:focus-visible` | Destaca o elemento em foco, especialmente na navegação por teclado. |
| `alt` | Fornece uma descrição textual da imagem. |
| `prefers-reduced-motion` | Permite respeitar a preferência por menos movimento. |
| `overflow-wrap: anywhere` | Permite quebrar textos longos para reduzir transbordamentos. |

### Foco de teclado

```css
a:focus-visible {
    outline: 3px solid var(--dourado);
    outline-offset: 4px;
}
```

O contorno ajuda o usuário a identificar qual link está selecionado ao navegar com o teclado.

### Preferência por menos movimento

```css
@media (prefers-reduced-motion: reduce) {
    .carrossel {
        scroll-behavior: auto;
    }
}
```

Essa regra desativa a rolagem suave quando o usuário indica preferência por movimento reduzido.

Esses recursos ajudam no uso da página, mas não representam uma verificação completa de acessibilidade.

## 15. Correções e melhorias pendentes

### Correções tratadas nesta revisão

- Inclusão da referência ao CSS no HTML.
- Remoção do `*/` solto antes da regra de `body`.
- Alteração da largura das imagens de `110%` para `100%`.
- Padronização das cores conforme a paleta exigida.
- Organização dos espaçamentos, cards e destaques.
- Adaptação do layout para telas menores.

O `*/` solto invalidava a regra do `body`, mas não necessariamente as regras seguintes.

### Pontos que ainda precisam ser revisados no HTML enviado

- Trocar `lang="en"` por `lang="pt-BR"`.
- Usar um título de aba descritivo.
- Revisar a hierarquia de `<h1>`, `<h2>` e `<h3>`.
- Usar um título curto e um parágrafo na introdução.
- Considerar `<main>` para identificar o conteúdo principal.
- Avaliar a troca da tabela da linha do tempo por uma lista ordenada.
- Completar nomes, descrições e links provisórios.
- Conferir a existência das imagens.
- Melhorar textos alternativos genéricos.
- Conferir os requisitos de seções e rodapé da atividade.

O ajuste visual não realiza automaticamente essas correções de conteúdo e semântica.

## 16. Roteiro simples para apresentar

### Objetivo

“A página reúne os projetos e os conteúdos estudados pela turma.”

### HTML

“As tags identificam o menu, os projetos e as informações complementares. Cada tag ajuda a organizar o significado do conteúdo.”

### CSS

“Os estilos organizam cores, tamanhos e espaçamentos, seguindo a identidade visual exigida pela atividade.”

### Cards

“Usamos Flexbox e rolagem horizontal para mostrar os projetos sem JavaScript.”

### Aside

“O aside contém informações complementares. Usamos Grid para separar os três destaques em colunas. No celular, eles ficam um abaixo do outro.”

### Pontos pendentes

“Ainda precisamos revisar os conteúdos provisórios e alguns pontos da estrutura HTML.”

## 17. Perguntas para treinar

### Por que usar `<aside>`?

Porque os destaques complementam o conteúdo principal. A tag não obriga o bloco a ficar na lateral.

### Por que usar Flexbox e Grid no mesmo projeto?

Flexbox organiza a sequência dos cards. Grid permite definir as colunas dos destaques.

Essa foi uma escolha de organização, não a única solução possível.

### O carrossel é automático?

Não. Ele usa rolagem horizontal e links que apontam para os projetos.

### `var()`, `calc()` e `repeat()` são JavaScript?

Não. São funções do CSS:

- `var()` utiliza o valor de uma variável.
- `calc()` calcula medidas.
- `repeat()` repete definições de linhas ou colunas.

### Qual é a diferença entre classe e ID?

Uma classe pode aparecer em vários elementos. Um ID identifica um elemento e deve ser único na página.

### Por que o CSS fica em um arquivo separado?

Para facilitar a manutenção e permitir compartilhar estilos entre páginas.

Alterações globais precisam ser conferidas nas outras páginas que utilizam o mesmo arquivo.

### Diminuir um `<h1>` pelo CSS transforma ele em `<h3>`?

Não. O CSS muda a aparência. O nível do título continua definido pela tag no HTML.

### Por que usar variáveis de cores?

Para reutilizar a paleta e facilitar alterações, mantendo a identidade visual do portal.

### Qual é a diferença entre `margin` e `padding`?

`margin` é o espaço externo ao elemento. `padding` é o espaço entre seu conteúdo e sua borda.

### O CSS corrige uma imagem que não carrega?

Não. É necessário conferir o caminho no atributo `src` e a existência do arquivo.
