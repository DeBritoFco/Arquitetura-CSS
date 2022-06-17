# arquitetura-css
curso de arquitetura da Alura. 

Protótipo do site: https://www.figma.com/file/0gMF5BPgplPYqQA6Om1T1sk9/alura-bootstrap

Aqui temos o protótipo para que saibamos o que fazer durante o projeto, mas claro que algumas coisa podem ficar diferentes. Vamos também usar uma pasta que por padrão chamamos de assets, onde geralmente ficam todos os arquivos estáticos, como CSS, imagens, arquivos de JS e assim por diante.

Temos tmbém o arquivos index.html, que geralmente é o arquivo principal da aplicação. Esse é o código atual da nossa aplicação:

<!DOCTYPE html>
<html lang="pt-BR">
    <head>
        <link href="https://fonts.googleapis.com/css?family=Pacifico|Roboto:100,300,400,500,700,900" rel="stylesheet" />
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <meta http-equiv="X-UA-Compatible" content="ie=edge" />
        <title>Fruta & Fruto</title>
        <link href="./assets/css/normalize.css" rel="stylesheet" />
        <link href="./assets/css/reset.css" rel="stylesheet" />
    </head>
    <body></body>
</html>

Cabe destacar que o arquivo normalize.css é resposável por resetar estilos do nosso navegador. Já o arquivo reset.css é referente aos estilos que desejamos que sejam padrão em todos os navegadores, mas que não estão presentes no normalize.css. Por exemplo, usaremos na nossa aplicação a fonte padrão Roboto.

Geralmente a criação de um site começa de cima para baixo, ou seja, do cabeçalho até o rodapé. Para criarmos um cabeçalho no HTML, por exemplo, usamos a tag <header>; o logo é uma imagem, e carregamos imagens usando a tag <img>, que não precisa ser fechada; o menu de navegação é construído usando a tag <nav>; listas são construídas com a tag <ul>, de unordered list (lista não ordenada); itens de uma lista utilizam a tag <li>, de list item; e o link é expresso por uma tag <a>, de anchor (âncora).

<body>
    <header>
        <img>
        <nav>
            <ul>
                <li><a></a></li>
            </ul>
        </nav>
    </header>
</body>

Sempre importante lembrar que a tag <img> receberá um parâmetro alt que representa um texto a sere exibido quando o navegador não conseguir redenrizar a imagem.

## Estilizando o cabeçalho

Agora que temos toda a marcação HTML do cabeçalho pronta, passaremos para a estilização. Vamos criar uma novo arquivo CSS, dentro da pasta "assets" do nosso projeto. Para utilizarmos um seletor de tag no CSS, basta passarmos o seu nome seguido de chaves ({}).

header {
    Os códigos do projeto com todas suas especificações estão disponíveis e para ficar mais didático aqui vamos manter o foco na explicação do que está acontecendo no desenvolvimento.
}

Uma breve explicação do display flex é que ele torna o elemento um flez container automaticamente transformando todos os seus filhos diretos em flez itens, deixando um do lado do outro. Quem tiver curiosidade olha esse link que tem um exemplo bem bacana: https://origamid.com/projetos/flexbox-guia-completo/

Ainda no cabeçalho foi usado o justify-content: alinha os itens flex no container de acordo com a direção. A propriedade só funciona se os itens atuais não ocuparem todo o container

justify-content: center;  -> Alinha os itens ao centro do container.
justify-content: space-around; ->  Cria um espaçamento entre os elementos. Os espaçamentos do meio são duas vezes maiores que o inicial e final.
justify-content: space-between; -> Cria um espaçamento igual entre os elementos. Mantendo o primeiro grudado no início e o último no final.

No nosso usamos o esse último e caso tenham curiosidade vejam na prática a diferença entre eles. Vocês irão perceber como fica melhor de entender.

Lembrando que eu estou iniciando meus estudos e com certeza quem for mais experientes irá perceber isso, já que existem outras formas de fazer o que estou fazendo de uma maneira mais simplificada. Vou chegar lá com certeza mas por enquanto muita calma nessa hora.

Mais uma vez aparece o display flex para que os menus fiquem um do lado do outro

header nav ul {
    display: flex;
}

https://caelum-online-public.s3.amazonaws.com/1258-arquitetura-css/Transcricao/Imagens/cabecalho3.png

Dentro da lista vamos retirar as bolinhas usando o list-style: none. Depois, ainda no menu, vamos ajustar a cor, espaçamento entre os links e a cor do link "início" que é exibido com uma cor mais escura. Iremos elimiar a margem à direita do item "comunidade". Será adicionado um espaçamento dos itens da borda em relação ao layout e finalizando ativando a função hover nos itens quando o mouse for passado sobre eles.

Aqui tem uma explicação simples e direta do text-transform

https://satellasoft.com/artigo/css/conhecendo-a-propriedade-do-css-text-transform

## Simplificando os seletores

Começaremos, em index.html, adicionando a classe cabecalho ao <header> usando o parâmetro class. Em <img> adicionaremos a classe logo; ao <nav> a classe menu; ao <ul> a classe menu-lista; aos <li> a classe menu-item; e aos <a> a classe menu-link.

Foi criada uma nova pasta dentro do diretório "assets\css" referente ao menu e após isso as impostações com o caminho correto. Continuaremos com o mesmo resultado visual, mas agora a organização do nosso CSS está bem melhor. A ideia de criar um arquivo CSS para cada elemento da página tem um nome: Atomic Design, que consiste, basicamente, em um modelo de organizar os componentes, pastas e a estrutura do nosso CSS a partir do princípio de átomos, onde um átomo é toda tag HTML.


