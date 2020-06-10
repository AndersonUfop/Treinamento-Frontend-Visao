# HTML

## Sumário

- Primeiros passos
- !DOCTYPE
- Elemento <head>
- Elemento <body>
- Elementos Semânticos
    - section
    - article
    - header
    - footer
    - nav
    - aside
    - figure
- Cabeçalhos
- Estilos
    - Tag style
- Classes HTML
- IDs HTML
- Diferença entre classes e IDs
- Imagens
- Links
    - Imagens como links
- Listas
    - Listas não-ordenadas
    - Listas ordenadas
- Formulários
    - Form
    - Label e Inputs
    - Input type date
    - Input type number
    - Input type password
    - Input type file
    - Radio
    - Checkbox
    - TextArea
    - Select
    - Button
    - Submit
- Tabelas

# Primeiros passos

1. Abra uma IDE de sua preferência (recomendação: **VS Code**)
2. Crie uma pasta em um repositório de sua preferência.
3. Crie um arquivo com o nome de **"index.html"**.

    *O navegador sempre identifica a primeira página de um site como index.html.*

    *Tente digitar em uma página da Internet o seu endereço e colocar index.html, vai aparecer sempre a página principal do site.*

4. Voltando para ide, no arquivo index.html digite o seguinte comando:

    ```html
    <!DOCTYPE html>
    <html lang="pt-BR">

    <head>
        <meta charset="UTF-8">
        <title>Meu primeiro site</title>
    </head>

    <body>
        <p>Hello World!</p>
    </body>

    </html>
    ```

5. Agora abra o index.html no navegador de sua preferência.
6. Certo, agora vamos mudar o conteúdo escrito, mas no próprio navegador!
7. Com o botão direito vá em inspecionar elemento, ou aperte 
8. Substitua o texto pelo seu nome e veja o resultado.
9. Avançando, vamos colocar um ícone no titulo do site, por isso digite o seguinte comando:

 

```html
<link rel="icon" href="images/Logo-Flat-Versao-Clara.png" type="image/png" sizes="16x16">
```

10. Visualize os resultados no navegador.

## !DOCTYPE

Todos os documentos HTML devem começar com uma declaração *<!DOCTYPE>*.

Não é uma tag HTML e sim uma informação para o navegador  sobre o tipo de documento esperado.

## Elemento <head>

É um recipiente para todos os elementos da cabeça: *<title>, <style>, <meta>, <link>, <script>* e *<base>*.

São metadados (dados de dados) e são colocados entre o <*html>* e o *<body>*. Os metadados não são exibidos.

Definem conjuntos de elementos, titulo, conjunto de caracteres, os estilos, scripts e outras metainformações. 

## Elemento <body>

Contém todo conteúdo de um elemento HTML, como: títulos, parágrafos, tabelas, imagens, listas, links, etc.

## Elementos semânticos

Descreve um significado para o navegador e para o desenvolvedor.

![https://www.w3schools.com/html/img_sem_elements.gif](https://www.w3schools.com/html/img_sem_elements.gif)

**Exemplos de elementos não-semânticos:** *<div>* e *<span>* não conta nada sobre o seu conteúdo.

**Exemplos de elementos semânticos:**  *<form>***,** *<table>* ****e *****<article>* define o seu conteúdo claramente.

### O elemento <section>

Define uma seção em um documento.

De acordo com a documentação do HTML do W3C: "Uma seção é um agrupamento temático de conteúdo, geralmente com um cabeçalho".

Uma página inicial normalmente pode ser dividida em seções para introdução, conteúdo e informações de contato.

Exemplo:

```html
<section>
  <h1>Como fazer um plano de ação</h1>
  <p>Plano de ação é uma ferramenta que traça uma metodologia ...</p>
</section>
```

### O elemento <article>

Especifica um conteúdo independente.

Um artigo deve ser capaz de fazer sentido por si próprio e deve ser possível lê-lo independente do restante do site.

Exemplos onde um *<article>* pode ser usado:

- Postagem no fórum
- Postagem no blog
- Artigo de jornal

Exemplo:

```html
<article>
	<h1>Como fazer um plano de ação</h1>
	<p>Para aprender como fazer um plano de ação, é preciso se concentrar em cinco pilares 
	    fundamentais: a iniciação do projeto (traçando os principais objetivos e metas), 
	    o planejamento (estabelecendo as ações), a execução (tomando as medidas), o 
	    monitoramento (avaliando os resultados) e o encerramento (documentando o que foi feito).</p>
	</article>
```

⁉️ **Aninhando <article> na <section> ou vice-versa ?**

⁉️ **Podemos usar as definições para define como aninhar esses elementos ?**

**Não podemos!** 

Na Internet você encontrará páginas com *<section>* elementos que contém *<article>* elementos e *<article>* elementos que contém *<section>* elementos.

Você também encontrará páginas que contém *<section>* elementos que contém *<section>* elementos e *<article>* elementos que contém *<article>* elementos.

**Exemplo para um jornal:**

O esporte <article> na **seção** de esportes pode ter uma seção técnica em cada *<article>.*

### O elemento <header>

Especifica o cabeçalho de um elemento ou seção.

Deve ser usado com contêiner para conteúdo introdutório.

Você pode ter vários *<header>* em um elemento.

Exemplo:

```html
<section>
  <article>
      <header>
          <h1>Como fazer um plano de Ação ?</h1>
          <p>Como fazer um plano de ação simplesmente perfeito para a sua empresa?</p>
      </header>
      <p>Essa é uma dúvida importante, cuja resposta pode colocar o seu negócio em uma rota de crescimento.</p>
  </article>
</section>
```

❗**Fique Atento**

Não confunda *<header>* com *<head>*

O *<head>* é um elemento para todos os elementos da cabeça: *<title>, <style>, <meta>, <link>, <script>.*

O *<header>* é um cabeçalho de um elemento ou seção.

### O elemento <footer>

Especifica o rodapé para um elemento ou seção.

Um *<footer>* deve conter informações sobre o elemento que o contém.

Um rodapé normalmente contém: autor do documento, informações de direitos autorais, links para termos de uso, informações de contato, etc.

Você pode ter vários footer em um documento.

```html
<footer>
  <p>&copy; 2020, by I'm Kind of a Big Deal, LLC </p>
</footer>
```

### O elemento <nav>

Define um conjunto de links de navegação.

Nem todos os os links de um documento devem estar dentro do *<nav>.* O nav é destinado apenas para o bloco principal de links de navegação.

```html
<nav>
  <a href="departamentos.html">Departamentos</a>
  <a href="membros.html">Membros</a>
  <a href="ferramentas.html">Ferramentas</a>
</nav>
```

**DICA:**

Para automatizar o trabalho digite: "*nav>a*3".* 

*Funcionou no VS Code, não sei se funciona em outras IDEs.*

### O elemento <aside>

Define algum conteúdo além do conteúdo que é colocado (como uma barra lateral).

Deve estar relacionado ao conteúdo.

```html
<section>
  <article>
      <p>Minha família e eu visitamos o Epcot Center neste verão.</p>
  </article>
  <aside>
      <h4>O Epcot Center é um parque temático na Disney World, Flórida.</h4>
  </aside>
</section>
```

### O elemento <figure>

Uma imagem e uma legenda podem ser agrupadas em um *<figure>*.

O objetivo de uma legenda é adicionar uma explicação visual a uma imagem.

O *<img>* define a imagem, o *<figcaption>* define a legenda.

Exemplo:

```html
<figure>
  <img src="https://upload.wikimedia.org/wikipedia/commons/c/ca/1_epcot_spaceship_earth_2010a.JPG" alt="Epcot Center">
  <figcaption>Epcot Center na Disney World, Florida</figcaption>
</figure>
```

## Cabeçalhos

Cabeçalhos são títulos ou legendas que você pode exibir em uma página web.

1. No mesmo arquivo digite:

```html
		<body>
			<h1>Titulo</h1>
	    <h2>Subtitulo</h2>
	    <h3>Texto 3</h3>
	    <h4>Texto 4</h4>
	    <h5>Texto 5</h5>
	    <h6>Texto 6</h6>
		</body>
```

*Dica de SEO:  Sempre seguir a hierarquia do texto! O Google penaliza se não seguir estas regras.*

# Título da página

## Titulo do post

### Subtitulo do post

2. Digite o código abaixo:

```html
<body>
    <h1>Tecnologia</h1>
    <h2>Treinamento de HTML</h2>
    <h3>Aprenda html e se prepare para o mercado</h3>
    <p>Aprenda HTML como você nunca viu, domine tudo deste o básico até o avançado, 
		<strong>isto é possível</strong>.
    </br> Saia da sua zona de conforto e vamos codar!
    </p>
    <h4>Autor: Seu nome</h4>
</body>
```

## Estilos HTML

O elemento *style* é usado para adicionar estilos ao elemento com cor, tamanho, fonte e muito mais.

Exemplo:

```html
<body style="background-color:powderblue;">
```

## Tag <style>

É utilizada para aplicar um CSS em um documento HTML.

```html
<style>
  h1 {color:red;}
  p {color:blue;}
</style>
```

## Classes HTML

O elemento classe é usado para definir estilos iguais para elementos com o mesmo nome de classe.

Exemplo:

```html
<div class="cabecalho">
   <p>Minha família e eu visitamos o Epcot Center neste verão.</p>
</div>
<div class="subtitulo">
  <h4>O Epcot Center é um parque temático na Disney World, Flórida.</h4>
</div>
```

```html
<style>
  .cabecalho {
      font-size: 18pt;
      color: red;
  }
  .subtitulo {
      background-color: blue;
      font-family: Arial, Helvetica, sans-serif;
  }
    </style>
```

O atributo class pode ser usado em qualquer elemento HTML.

O elemento class diferencia maiúsculas e minúsculas!

Use (**.)** para selecionar elementos de uma classe específica.

Um elemento HTML  pode ter mais de uma classe, cada nome de classe é separado por um espaço.

TAGS diferentes podem compartilhar a mesma classe. 

## ID HTML

O id é um atributo usado para especificar um ID exclusivo de um elemento HTML (o valor deve ser exclusivo no documento HTML).

No CSS para selecionar um ID exclusivo, escreva um caractere de hash (#) seguido pelo ID do elemento.

Exemplo:

```html
<p id="subtitulo">Minha família e eu visitamos o Epcot Center neste verão.</p>
```

```html
#subtitulo {
  display: inline-block;
  font-style: italic;
}
```

### Diferença entre classe e ID

As classes permitem atribuir formatação a vários elementos de uma vez. 

As IDs são únicas para cada elemento.

DICA!

Para automatizar o trabalho, tem um método para digitar ID e classe mais rápido, define classe e ID ao mesmo tempo e também define os elementos que estarão aninhados, com classe e ID:

```html
div#lista.lista1>ul#item.elementos*5
```

## Imagens

Para adicionar imagens em um site use este comando:

```html
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
```

## Links

Os links permitem que os usuários vão para outras páginas.

```html
<a href="https://github.com/AndersonUfop" title="My Github" target="_blank">Link</a>
```

### Imagens como links

```html
<a href="https://www.infoescola.com/geologia/caverna/">
    <img src="https://www.infoescola.com/wp-content/uploads/2011/11/caverna1-450x450.jpg" alt="Imagem">
</a>
```

DICA!

*Linkar a foto da logo da empresa para a página principal.*

## Listas

As listas permitem agrupar um conjunto de coisas.

### Listas não-ordenadas

- Departamentos
- Membros
- Ferramentas

```html
<ul class="list-unstyled components">
        <li>Departamentos</li>
        <li>Membros</li>
        <li>Ferramentas</li>
</ul>
```

### Listas ordenadas

1. Departamentos
2. Membros
3. Ferramentas

```html
<ol>
        <li>Departamentos</li>
        <li>Membros</li>
        <li>Ferramentas</li>
    </ol>
```

DICA! 

*Para automatizar o trabalho você pode digitar o [**nome da tag*quantidade que você quer]***

Exemplo:

```html
 li*3
```

Resultado:

```html
		<li></li>
    <li></li>
    <li></li>
```

Funcionou no VS Code, não sei se funciona em outras IDEs.

## Formulários

### Form

```html
<form action="index.html" method="POST">
```

### Label e Inputs

```html
<form>
       <label for="inputNome">Nome completo:</label>
       <input type="text" id="nome" placeholder="Digite seu nome" required>
   </form>
```

### Input type number

```html
<label for="inputFilhos">Número de filhos:</label>
<input type="number" id="filhos" placeholder="1" min="0" max="7" required>
```

### Input type date

```html
<label for="inputdataNasc">Data de nascimento:</label>
<input type="date" id="dataNasc" min="1900-01-01" max="2030-12-31">
```

### Input type password

```html
<label for="inputSenha">Senha:</label>
<input type="password" id="senha" maxlength="10" placeholder="Digite sua senha" required>
```

### Input type file

```html
<label for="myFile">Adicione uma foto:</label>
<input type="file" id="imagem" accept="image/*">
```

### Radio

```html
<input type="radio" name="sexo" value="masculino" id="masculino">
<label>Masculino</label>
<input type="radio" name="sexo" value="feminino" id="feminino">
<label>Femino</label>
```

### Checkbox

```html
<input type="checkbox" id="check1">
<label for="check1">HTML</label>
<input type="checkbox" id="check2">
<label for="check2">CSS</label>
<input type="checkbox" id="check3">
<label for="check3">JavaScript</label>
<input type="checkbox" id="check4">
<label for="check4">PHP</label>
<input type="checkbox" id="check5">
<label for="check5">Laravel</label>
<input type="checkbox" id="check6">
<label for="check6">Node JS</label>
<input type="checkbox" id="check7">
<label for="check7">React JS</label>
```

### TextArea

```html
<label for="descricao">Descrição</label>
<textarea rows="5" cols="16" placeholder="Descrição" required id="descricao"></textarea>
```

### Select

```html
<label for="departamento" id="departamento">Departamento</label>
<select name="departamento" id="departamento">
    <option value="1">Presidência</option>
    <option value="2">Vice-presidência</option>
    <option value="3">Projetos</option>
    <option value="4" selected>Qualidade</option>
    <option value="5">Marketing</option>
    <option value="6">Gestão de Pessoas</option>
</select>
```

### Button

```html
<button type="button" class="close" onclick="fechar()">Fechar</button>
<button type="button" disabled>Cancelar</button>
```

### Submit

```html
<button type="submit" class="btn btn-dark" onclick="confirmacao()">Salvar</button>
```

## Tabelas

```html
<table class="table" id="table" width="80%">
    <thead>
        <tr>
            <th scope="col" id="col1">Departamento</th>
            <th scope="col" id="col2">Descrição</th>
            <th scope="col" id="col4"> </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Presidência</td>
            <td>O departamento é responsável por gerir uma <br>empresa júnior.</td>
            <td>
                <a href="editar.html">
                    <button type="button">Editar</button>
                </a>
                <button type="button">Excluir</button>
            </td>
        </tr>
        <tr>
            <td>Marketing</td>
            <td>O departamento éesponsável pela <br>comunicação interna e<br> externa.</td>
            <td>
                <a href="editar.html">
                    <button type="button">Editar</button>
                </a>
                <button type="button">Excluir</button>
            </td>
        </tr>
        <tr>
            <td>Gestão de Pessoas</td>
            <td>O departamento é responsável por promover<br> treinamentos, eventos<br> e resolver conflitos internos</td>
            <td>
                <a href="editar.html">
                    <button type="button" disabled>Editar</button>
                </a>

                <button type="button" disabled>Excluir</button>
            </td>
        </tr>
    </tbody>
</table>
```
