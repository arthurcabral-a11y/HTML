# HTML
projetos-web/
   └── primeira-pagina-html5/
       ├── index.html
       └── imagens/
           ├── tecnologia-sociedade.svg
           └── robo-inteligencia-artificial.svg
   git config --global user.name "Seu Nome"
   git config --global user.email "seu-email@exemplo.com"
git init
git add .
git commit -m "Adiciona primeira página HTML5"
git branch -M main
git remote add origin https://github.com/seu-usuario/projetos-web.git
git push -u origin main
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu Primeiro Documento HTML</title>
</head>
<body>
  <h1>Olá, Mundo!</h1>
  <p>Este é o meu primeiro documento HTML.</p>
</body>
</html>
<h1>Este é um Cabeçalho de Nível 1</h1>
<h2>Este é um Cabeçalho de Nível 2</h2>
<p>Este é um parágrafo de texto.</p>
<ol>
  <li>Primeiro item</li>
  <li>Segundo item</li>
  <li>Terceiro item</li>
</ol>
<a href="https://www.example.com" target="_blank">Visite o Example</a>
<img src="imagem.jpg" alt="Descrição da imagem">
<a href="pagina.html">Link Interno</a>
<a href="https://www.example.com" target="_blank">Link Externo</a>
<h2 id="seção1">Seção 1</h2>
<a href="#seção1">Ir para a Seção 1</a>
<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Idade</th>
      <th>Cidade</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ana</td>
      <td>28</td>
      <td>São Paulo</td>
    </tr>
    <tr>
      <td>João</td>
      <td>35</td>
      <td>Rio de Janeiro</td>
    </tr>
  </tbody>
</table>
<table>
  <tr>
    <th rowspan="2">Nome</th>
    <th colspan="2">Informações</th>
  </tr>
  <tr>
    <th>Idade</th>
    <th>Cidade</th>
  </tr>
  <tr>
    <td>Ana</td>
    <td>28</td>
    <td>São Paulo</td>
  </tr>
  <tr>
    <td>João</td>
    <td>35</td>
    <td>Rio de Janeiro</td>
  </tr>
</table>
<form action="/submit" method="post">
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome">

  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <input type="submit" value="Enviar">
</form>
<form action="/submit" method="post">
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome">

  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <label for="idade">Idade:</label>
  <input type="number" id="idade" name="idade">

  <label for="senha">Senha:</label>
  <input type="password" id="senha" name="senha">

  <label for="nascimento">Data de Nascimento:</label>
  <input type="date" id="nascimento" name="nascimento">

  <label>
    <input type="checkbox" name="newsletter" checked>
    Inscrever-se na newsletter
  </label>

  <label>
    <input type="radio" name="genero" value="masculino">
    Masculino
  </label>
  <label>
    <input type="radio" name="genero" value="feminino">
    Feminino
  </label>

  <input type="submit" value="Enviar">
</form>
<form action="/submit" method="post">
  <!-- Campos obrigatórios -->
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome" required> 

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <!-- Campo numérico com restrição de idade -->
  <label for="idade">Idade:</label>
  <input type="number" id="idade" name="idade" min="18" max="99">

  <!-- Campo de senha com padrão de validação -->
  <label for="senha">Senha:</label>
  <input type="password" id="senha" name="senha" pattern="[a-zA-Z0-9]{8,}">

  <input type="submit" value="Enviar">
</form>
<h1 style="color: blue; font-size: 24px;">Este é um cabeçalho h1</h1>
<p style="color: red;">Este é um parágrafo de texto.</p>
<!DOCTYPE html>
<html>
<head>
  <title>Minha Página</title>
  <style>
    h1 {
      color: blue;
      font-size: 24px;
    }
  </style>
</head>

<body>
  <h1>Este é um cabeçalho h1</h1>
  <p>Este é um parágrafo de texto.</p>
</body>

</html>
<!DOCTYPE html>
<html>
<head>
  <title>Minha Página</title>
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <h1>Este é um cabeçalho h1</h1>
  <p>Este é um parágrafo de texto.</p>
</body>

</html>

<h1 class="titulo">Título Principal</h1>
<p id="paragrafo-principal">Este é um parágrafo principal.</p>
/* Seletor de Elemento */
h1 {
  color: blue;
}

/* Seletor de Classe */
.titulo {
  font-size: 24px;
}

/* Seletor de ID */
#paragrafo-principal {
  font-weight: bold;
}

p {
  color: #662214;
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.5;
}

body {
  background-color: #c2b280;
}

div {
  margin: 20px;
  padding: 10px;
  border: 2px solid #000;
}
.container {
  display: flex;
}
.container {
  display: flex;
  flex-direction: row; /* ou row-reverse, column, column-reverse */
}
.container {
  display: flex;
  justify-content: center; /* ou flex-start, flex-end, space-between, space-around */
}
container {
  display: flex;
  align-items: center; /* ou flex-start, flex-end, stretch, baseline */
}
.item1 {
  order: 2;
}

.item2 {
  order: 1;
}

.item3 {
  order: 3;
}
.item {
  flex-grow: 1;
}
.item {
  flex-shrink: 1;
}
.item {
  flex-basis: 200px;
}
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
}

.item {
  background-color: #f0f0f0;
  padding: 20px;
  margin: 10px;
  flex-grow: 1;
  text-align: center;
}
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto;
  gap: 10px;
}
.item1 {
  grid-column: 1 / 3; /* Ocupará da coluna 1 até antes da coluna 3 */
  grid-row: 1 / 2; /* Ocupará a linha 1 */
}

.item2 {
  grid-column: 3 / 4; /* Ocupará a coluna 3 */
  grid-row: 1 / 2; /* Ocupará a linha 1 */
}

.item3 {
  grid-column: 1 / 4; /* Ocupará da coluna 1 até antes da coluna 4 */
  grid-row: 2 / 3; /* Ocupará a linha 2 */
}

<div class="container">
  <div class="item item1">Item 1</div>
  <div class="item item2">Item 2</div>
  <div class="item item3">Item 3</div>
</div>
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: auto;
  gap: 10px;
}

.item {
  background-color: #f0f0f0;
  padding: 20px;
  text-align: center;
}
.relative-box {
  position: relative;
  top: 20px;
  left: 30px;
}

.absolute-box {
  position: absolute;
  top: 50px;
  right: 20px;
}
.box1 {
  position: absolute;
  z-index: 1;
}

.box2 {
  position: absolute;
  z-index: 2;
}
<meta name="viewport" content="width=device-width, initial-scale=1.0">
.container {
  width: 80%;
  height: 50vh;
}
/* Estilos para dispositivos com largura máxima de 600px */
@media (max-width: 600px) {
  .container {
    flex-direction: column;
  }
}

/* Estilos para dispositivos com largura mínima de 601px */
@media (min-width: 601px) {
  .container {
    flex-direction: row;
  }
}
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
.container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.item {
  flex: 1 1 100px;
  margin: 10px;
  background-color: #f0f0f0;
  padding: 20px;
}

@media (max-width: 600px) {
  .container {
    flex-direction: column;
  }
}
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu Currículo Online</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="sobre.html">Sobre</a></li>
        <li><a href="projetos.html">Projetos</a></li>
        <li><a href="contato.html">Contato</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section id="home">
      <h1>Bem-vindo ao Meu Currículo Online</h1>
      <p>Olá! Eu sou [Seu Nome], um(a) desenvolvedor(a) web com experiência em [suas especialidades].</p>
    </section>
  </main>
  <footer>
    <p>&copy; 2024 [Seu Nome]. Todos os direitos reservados.</p>
  </footer>
</body>
</html>
Vamos agora criar os outros arquivos HTML (sobre.html, projetos.html, contato.html) com estruturas semelhantes.

Arquivo sobre.html:

<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sobre Mim</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="sobre.html">Sobre</a></li>
        <li><a href="projetos.html">Projetos</a></li>
        <li><a href="contato.html">Contato</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section id="sobre">
      <h1>Sobre Mim</h1>
      <p>Eu sou [Seu Nome], um(a) desenvolvedor(a) web com [X] anos de experiência em [suas especialidades].</p>
    </section>
  </main>
  <footer>
    <p>&copy; 2024 [Seu Nome]. Todos os direitos reservados.</p>
  </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meus Projetos</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="sobre.html">Sobre</a></li>
        <li><a href="projetos.html">Projetos</a></li>
        <li><a href="contato.html">Contato</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section id="projetos">
      <h1>Meus Projetos</h1>
      <p>Aqui estão alguns dos projetos em que trabalhei:</p>
      <ul>
        <li><strong>Projeto 1:</strong> Descrição do projeto 1.</li>
        <li><strong>Projeto 2:</strong> Descrição do projeto 2.</li>
        <li><strong>Projeto 3:</strong> Descrição do projeto 3.</li>
      </ul>
    </section>
  </main>
  <footer>
    <p>&copy; 2024 [Seu Nome]. Todos os direitos reservados.</p>
  </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contato</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="sobre.html">Sobre</a></li>
        <li><a href="projetos.html">Projetos</a></li>
        <li><a href="contato.html">Contato</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section id="contato">
      <h1>Contato</h1>
      <p>Envie-me uma mensagem através do formulário abaixo:</p>
      <form action="https://wa.me/55[SEU_NUMERO]?text=" method="get" target="_blank">
        <label for="mensagem">Mensagem:</label>
        <textarea id="mensagem" name="text" rows="4" cols="50"></textarea>
        <br>
        <button type="submit">Enviar via WhatsApp</button>
      </form>
    </section>
  </main>
  <footer>
    <p>&copy; 2024 [Seu Nome]. Todos os direitos reservados.</p>
  </footer>
</body>
</html>
/* Estilos gerais */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f9f9f9;
}

header {
  background-color: #333;
  color: #fff;
  padding: 10px 0;
}

nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  text-align: center;
}

nav ul li {
  display: inline;
  margin: 0 15px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
}

main {
  padding: 20px;
  text-align: center;
}

footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 10px 0;
  position: fixed;
  bottom: 0;
  width: 100%;
}

form {
  display: inline-block;
  text-align: left;
}

form label {
  display: block;
  margin-top: 10px;
}

form textarea {
  width: 100%;
  max-width: 500px;
}
/* Estilos gerais */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f9f9f9;
}

header {
  background-color: #333;
  color: #fff;
  padding: 10px 0;
}

nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  text-align: center;
  display: flex;
  justify-content: center;
}

nav ul li {
  margin: 0 15px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
}

main {
  padding: 20px;
  text-align: center;
}

footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 10px 0;
  position: fixed;
  bottom: 0;
  width: 100%;
}

form {
  display: inline-block;
  text-align: left;
}

form label {
  display: block;
  margin-top: 10px;
}

form textarea {
  width: 100%;
  max-width: 500px;
}

/* Layouts de Seções */
section {
  margin: 20px 0;
}

.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.item {
  background-color: #f0f0f0;
  padding: 20px;
  margin: 10px;
  flex: 1 1 300px;
  text-align: center;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
<section id="home" class="container">
    <div class="item">
    <h1>Bem-vindo ao Meu Currículo Online</h1>
    <p>Olá! Eu sou [Seu Nome], um(a) desenvolvedor(a) web com experiência em [suas especialidades].</p>
    </div>
</section>
<section id="sobre" class="container">
    <div class="item">
    <h1>Sobre Mim</h1>
    <p>Eu sou [Seu Nome], um(a) desenvolvedor(a) web com [X] anos de experiência em [suas especialidades].</p>
    </div>
</section>
<section id="projetos" class="container">
    <div class="item">
    <h1>Meus Projetos</h1>
    <p>Aqui estão alguns dos projetos em que trabalhei:</p>
    <ul>
        <li><strong>Projeto 1:</strong> Descrição do projeto 1.</li>
        <li><strong>Projeto 2:</strong> Descrição do projeto 2.</li>
        <li><strong>Projeto 3:</strong> Descrição do projeto 3.</li>
    </ul>
    </div>
</section>
<section id="contato" class="container">
    <div class="item">
    <h1>Contato</h1>
    <p>Envie-me uma mensagem através do formulário abaixo:</p>
    <form action="https://wa.me/55[SEU_NUMERO]?text=" method="get" target="_blank">
        <label for="mensagem">Mensagem:</label>
        <textarea id="mensagem" name="text" rows="4" cols="50"></textarea>
        <br>
        <button type="submit">Enviar via WhatsApp</button>
    </form>
    </div>
</section>
<main>
  <section id="sobre" class="container">
    <div class="item">
      <h1>Sobre Mim</h1>
      <img src="sua-foto.jpg" alt="Foto de [Seu Nome]" style="width:150px;border-radius:50%;">
      <p>Eu sou [Seu Nome], um(a) desenvolvedor(a) web com [X] anos de experiência em [suas especialidades].</p>
    </div>
  </section>
</main>
<main>
  <section id="projetos" class="container">
    <div class="item">
      <h1>Meus Projetos</h1>
      <p>Aqui estão alguns dos projetos em que trabalhei:</p>
      <table id="table-projetos" border="1">
          <tr>
            <th>Nome do Projeto</th>
            <th>Descrição</th>
            <th>Ano</th>
          </tr>
          <tr>
            <td>Projeto 1</td>
            <td>Descrição do projeto 1.</td>
            <td>2022</td>
          </tr>
          <tr>
            <td>Projeto 2</td>
            <td>Descrição do projeto 2.</td>
            <td>2023</td>
          </tr>
          <tr>
            <td>Projeto 3</td>
            <td>Descrição do projeto 3.</td>
            <td>2024</td>
          </tr>
        </table>
    </div>
  </section>
</main>
#table-projetos {
  width:100%;
  text-align: center;
}
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<p>Uma fórmula inline: \(E = mc^2\)</p>
<p>Uma fórmula display:</p>
\[
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
\]
<div class="container">
  <div class="row">
    <div class="col-md-4">
      <h2>Título 1</h2>
      <p>Conteúdo da coluna 1.</p>
    </div>
    <div class="col-md-4">
      <h2>Título 2</h2>
      <p>Conteúdo da coluna 2.</p>
    </div>
    <div class="col-md-4">
      <h2>Título 3</h2>
      <p>Conteúdo da coluna 3.</p>
    </div>
  </div>
</div>
