# NLW06

# Aula 01

This repository was created for the development of Next Level Week 06 Origins Project

## Observações iniciais

Ao fazer uma modificação em qualquer arquivo o VSCode irá deixar uma bolinha branca ao lado do nome do arquivo, indicando que ele não foi salvo.

## HTML

HTML -> Hyper text markup language

- Fomato de uma tag no HTML:

  - `<tag attribute="attribute_value">text</tag>`

- Emmet

  - Ao digitar ! e dar Enter, ele atribui um cabeçalho ao seu código HTML;
  - Nesse cabeçalho, é possível mudar a linguagem do seu cógio em `<html lang="linguagem">`

- Tags:

  - A tag `<html>` éuma tag do tipo root=raíz, apartir dela teremos outras tags filhas como `<head>` e `<body>`
  - Na tag `<head>` teremos configurações da página como fontes e links com outros arquivos;
  - A tag `<body>` terá todo o conteúdo da página. Ou seja, o que está da URL para baixo;
  - `<!--comentário-->` Essa tag define um comentário no HTML;
  - Tags `<meta>`:
    - `<meta charset="UTF-8">` Serve para ajustar a formatação do seu código a todos os navegadores, sem ela essaformatação pode dar errado.
    - `<meta name="viewport" content="width=device-width, initial-scale=1.0">` Define que a largura da sua área visível é igual a largura do dispositvo em que seu site está sendo visualizado. Jáo initial-scale define que a escala da usa viewport será igual a 1, evitando distorções.

- Identificador único (ID):

  - Ele facilita a comunicação entre HTML e o CSS
  - Caso eu queira me referir a um elemento específico do código HTML dentro do CSS, eu posso criar um ID para ele;
  - Exemplo: `<header id="header">`
  - Nesse caso, o header em que for adicionado esse ID, poderá ser chamado no código CSS através da Hash: #header;

- Classe (class):

  - É um atributo com a mesma função do ID, porém uma classe pode ser atribída a várias tags, já um ID só será atribuído a uma única Tag.
  - A classe é chamada no CSS através de um ponto: .nomedaclasse

- Estrutura HTML:

  - Você deveolhar para os elementos de design e identificar a qual tag cada um deles pertence;
  - Exemplos:
    ```
    - <h1> = título
    - <p> = parágrafo
    - <img src="link" alt="">
      - Essa tag não tem fechamento, apenas tag de início
      - Alt --> Descrição da imagem em texto para pessoas que precisam deleitura de tela. Usar letra maiúscula apenas na primeira palavra para o leitor não interpretar como uma sigla.
    - <a> = link;
    - <nav> --> declara que dentro dessa tag irão existir elementos clicáveis (links);
    - <span> --> Cria uma separação entre elementos mas deixa um elemento dentro do outro;
    - <div> --> cria uma separação e por padrão deixa um elemento abaixo do outro.
    - <ul> --> lista não ordenada
    - <li> --> item da lista (list item)
    ```
  - Para que o código não fique uma zona, precisamos dividir ele em caixas:
    -A caixa superior em que geralmente ficam os menus, se chama header.
  - No caso do nosso arquivo ele está separado em:
    - Header
    - Início
    - Sobre
    - Serviços
    - Depoimentos
    - Contato
    - Footer

- Tags semânticas:

  - São Tags que possuem significado e ajudam a montar a estrutura da página.
  - Exemplos:

  ```
    - <header>
    - <main>
      - <section>
      - Também podemos escrever section*n e o Emmet irá criar n tags section.
    - <footer>
  - Elas ajudam a se organizar no que você está fazendo e também nos SEOs (motores de busca), ou seja,irá ajudar sua página a aparecer na busca do Google;
  - Um SEO bem desenvolvido pode te ajudar a aparecer nas primeiras páginas do Google;
  - Também ajuda as pessoas com deficiência a navegar pela página;

  ```

- Dicas:

  - unsplash.com --> site com imagens gratuítas, buscar em inglês;
    - Nesse site,podemos apenas copiar o endereço da imagem e colar no atríbuto src;

  ```

  ```

## CSS

```
CSS --> Cascating Style Sheets

- Sintaxe:

  - seletor{
    propriedade:#value;
    }
  - seletor = h1/main/header/section...
  - - = seletor universal

- Estrutura em cascata:

  - No CSS ocódigo é montado em cascara, ou seja, teremos vários seletores ou classes uma embaixo da outra;
  - Essaestrutura da prioridade para os elementos que estão mais abaixo na ordem,caso tenham o mesmo nome;
    -Specificity:
    - Regra capaz de mudar a ordem depriorização da cascata, ou seja, muda o fato do que está mais embaixo valer mais;
      <img src="https://devopedia.org/images/article/291/7219.1602765579.svg" alt="Ordem de especificidade do CSS" />
    - Podemos nos referenciar a um elemneto que está dentro de outro no CSS. Exemplo, se eu tenho um elemento no HTML do tipo <nav class="container">, posso me referenciar a esse elemento específico no CSS como nav.container{} ou se ele está dentro de um header com id="header", posso me referenciar a ele como #header nav {}

- Separação dasatribuições do CSS:

  - No caso do nosso código, classificamos as partes da nossa cascata em:
    - RESET
    - BASE
    - ?
    - LAYOUT
    - HOME

- Reset:

  - O Navegador já vem com uma formatação padrão então para garantir que estamos partindo do zero em qualquer navegador, separamos uma parte do CSS para as configurações gerais de formatação dos elementos.
```

- Propriedades de espaçamento no CSS:
  <img src="https://i.stack.imgur.com/tOwij.png" alt="imagem detalhando as propriedades de espaçamento do CSS">

```
- Propriedades:

  - Exemplos: margin, padding, border, etc.
  - boz-sizing --> Define a forma como o CSS irá interpretar o tamanho que é dado para uma caixa;
  - box-sizing: border-box --> Define que o tamanho dado em wideth e high será equivalente ao tamanho da borda e os demais tamanhos que serão dados como padding ou content serãodiminuidos desses valores;

- Unidades:

  - Unidade relativa: se ajusta conforme o dispositivo(rem);
  - Unidade fixa: não irá se ajustar, terá sempre o mesmo tamanho(px);
  - 1 rem = 16px --> Caso o font-size do seletor root estiver classificado como 100%, caso isso mude o tamanho de todo o resto irá mudar junto;

- Classe container

  - Quando todos os elementos da página seguem um espaçamento padrão, é normal definirmos uma classe chamada container para guardar os atributos de espaçamento dados a esses elementos.

- Propriedade Display com valor flex:

  - Aparentemente o que ela faz é posicionar os elementos filhos do seletor um do lado do outro
  - O uso dessa propriedade com esse valor possibilita usar outra propriedade chamada justify-content.
    - Essa propriedade aceita os seguintes valores:
      - Padrão, equivalente ao texto colado na esquerta;
      - Flex-end, texto colado na direita;
      - space-between, distribui os elementos igualmente dentro do espaço disponível;

- Text-Decoration

  - Essa propriedade pode ser usada no link como "text-decoration: none" para tirar a decoração automática qeu o HTML da para links.

- Definição de variáveis:

  - Uma variável no CSS pode ser definida da seguinte forma: "--nomedavariável: valor"
  - Se uma variável é definida no CSS em um elemento pai, ela poderá ser acessada por todos os elementos filhos;
  - Para que uma variável possa ser acessada por todos os elementos do código, é recomendado definirmos ela dentro do elemento ":root";
  - Ao mudar o valor de uma variável, você muda o valor de tudo que está atribuido a ela;

- Chamando as variáveis:

  - Para chamar uma variável, a sintaxe éa seguinte: "var(--nomedavariável)" esse texto deve ser inserido no lugar do valor ao qual a variável é equivalente;
  - Caso seja digitado apenas "--nomedavariavel" o Emmet irá completar;

- Webkit-font-smooting:

  - Propriedade que ajuda a suavizar o texto
  - Não são todos os navegadores que aceitam esse tipo de propriedade mas o Chrome aceita
  - Valores usados na aula para essa propriedade: auto e antialised (deixa a fonte mais fraca)

- Posição relativa:

- Elemento fantasma:
  - Isso foi usado no exemplo da seguinte forma: "#home .image::before{}"
  - Esse comando irá criar um elemento fantasma uma linha acima do elemento que está sendo referenciado, nesse caso seria o elemento com a classe image, dentro do elemento de id home.
```

## Integrações entre linguagens

```
- CSS+HTML
  - Para adicionar linkaro arquivo CSS com o HTML, basta inserir a tag link:css atravésdo Emmet.
  - <link rel="tipo de relação" href="nome do arquivo.css">
```

## Comandos VSCode

- Comandos Teclado

  - Ctrl+Shift+E --> Aparece a barra lateral com arquivos;
  - Ctrl+B --> Fecha e abre a lateral com os arquivos;
  - Alt+Seta para cima --> Pega o que está selecionado e move para dentro da caixa que está acima.

- Detalhes importantes:

  - Toda página precisa de um arquivo primério determinado index;
  - Emmet é uma função do VSCode que completa o código automaticamente. Exemplo: digite h1+Enter;
  - Para criar um arquivo html, basta que ele termine com .html;
  - É possível habilitar o auto save através do caminho File > AutoSave;

### Plugins usados

- Prittier

  - Ao salvar um código(Ctrl+S), o prittier entra em ação garantindo que ele estará corretamente formatado.

- MaterialIcon
  - Atribui o icone de cada linguagemao arquivo dessa linguagem;

-Dracula
-Apenas melhora o visualdo VSCode

-Live Server

- Permite acompanhar mudanças em tempo real no browser de acordo com o que é alterado no código;
- Para botá-lo em ação basta apertar com o botão direito em cima do arquivo index e depois em "Open With Live Server"

## Figma

- Comandos teclado:

  - Ctrl+\ --> Tira as barras laterias da visualização;

- Estrutura:
  - Para facilitar a codificação, no Figma é possível Fazer a separação dos designs em caixas como Header,Início, Footer, etc.

## Google Fonts

- Como importar fontes de lá para o código:

  - No caso do nosso projeto, apenas escolhemos as fontes no site, copiamos o link gerado pelo google fontes e colamos no cabeçalho da página.

- A adição da fonte a um determinado seletor, id ou classe pode ser feita através do CSS, com a propriedades "font" que recebe como valores a força da fonte, tamanho, nome da fonte e uma fonte substituta.

# Aula 02

## Hamburguer Menu

Para criar os items da lista, utilizamos as tags`<ul>, <li>, e <a>`. Para que ao clicar nesse item, o usuário seja direcionado a uma seção específica, adicionamos o ID da seção a qual ele deve ser direcionado como referência para o link.
