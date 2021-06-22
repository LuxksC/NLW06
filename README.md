# NLW06

This repository was created for the development of Next Level Week 06 Origins Project

## Observações iniciais

Ao fazer uma modificação em qualquer arquivo o VSCode irá deixar uma bolinha branca ao lado do nome do arquivo, indicando que ele não foi salvo.

## HTML

HTML -> Hyper text markup language

- Fomato de uma tag no HTML:

  - <tag attribute="attribute_value">text</tag>

- Emmet

  - Ao digitar ! e dar Enter, ele atribui um cabeçalho ao seu código HTML;
  - Nesse cabeçalho, é possível mudar a linguagem do seu cógio em <html lang="linguagem">

- Tags:

  - A tag <html> éuma tag do tipo root=raíz, apartir dela teremos outras tags filhas como <head> e <body>
  - Na tag <head> teremos configurações da página como fontes e links com outros arquivos;
  - A tag <body> terá todo o conteúdo da página. Ou seja, o que está da URL para baixo;
  - <!--comentário--> Essa tag define um comentário no HTML;
  - Tags <meta>:
    - <meta charset="UTF-8"> Serve para ajustar a formatação do seu código a todos os navegadores, sem ela essaformatação pode dar errado.
    - <meta name="viewport" content="width=device-width, initial-scale=1.0"> Define que a largura da sua área visível é igual a largura do dispositvo em que seu site está sendo visualizado. Jáo initial-scale define que a escala da usa viewport será igual a 1, evitando distorções.

- Estrutura HTML:

  - Você deveolhar para os elementos de design e identificar a qual tag cada um deles pertence;
  - Exemplos:
    - <h1> = título
    - <p> = parágrafo
    - <img src="link" alt="">
      - Essa tag não tem fechamento, apenas tag de início
      - Alt --> Descrição da imagem em texto para pessoas que precisam deleitura de tela. Usar letra maiúscula apenas na primeira palavra para o leitor não interpretar como uma sigla.
    - <a> = link
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
    - <header>
    - <main>
      - <section>
      - Também podemos escrever section*n e o Emmet irá criar n tags section.
    - <footer>
  - Elas ajudam a se organizar no que você está fazendo e também nos SEOs (motores de busca), ou seja,irá ajudar sua página a aparecer na busca do Google;
  - Um SEO bem desenvolvido pode te ajudar a aparecer nas primeiras páginas do Google;
  - Também ajuda as pessoas com deficiência a navegar pela página;

- Dicas:
  - unsplash.com --> site com imagens gratuítas, buscar em inglês;
    - Nesse site,podemos apenas copiar o endereço da imagem e colar no atríbuto src;

## CSS

CSS --> Cascating Style Sheets

- Sintaxe:

  - seletor{
    propriedade:#value;
    }
  - seletor = h1/main/header/section...

- Estrutura em cascata:

  - No CSS ocódigo é montado em cascara, ou seja, teremos vários seletores ou classes uma embaixo da outra;
  - Essaestrutura da prioridade para os elementos que estão mais abaixo na ordem,caso tenham o mesmo nome;
    -Specificity:
    - Regra capaz de mudar a ordem depriorização da cascata, ou seja, muda o fato do que está mais embaixo valer mais;
      <img src="https://devopedia.org/images/article/291/7219.1602765579.svg" alt="Ordem de especificidade do CSS" />

- Reset:
  - O Navegador já vem com uma formatação padrão então para garantir que estamos partindo do zero em qualquer navegador, adicionamos a primeira linha do Código CSS o comando /_ RESET _/

## Integrações entre linguagens

- CSS+HTML
  - Para adicionar linkaro arquivo CSS com o HTML, basta inserir a tag link:css atravésdo Emmet.
  - <link rel="tipo de relação" href="nome do arquivo.css">

## Comandos VSCode

- Comandos Teclado

  - Ctrl+Shift+E --> Aparece a barra lateral com arquivos;
  - Ctrl+B --> Fecha e abre a lateral com os arquivos;

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
