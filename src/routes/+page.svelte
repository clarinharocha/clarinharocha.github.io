<script>
    let livros = [
      { titulo: "A Rainha Vermelha", autor: "Victoria Aveyard", preco: "30,99", precoAntigo: "34,99", genero: "Romance, Ficção Juvenil", imagem: "a rainha vermelha.jpg" },
      { titulo: "Harry Potter", autor: "J.K. Rowling", preco: "60,99", precoAntigo: "69,90", genero: "Aventura, Fantasia", imagem: "prisioneiro de azkaban.jpg" },
      { titulo: "O Pequeno Príncipe", autor: "Antoine de Saint-Exupéry", preco: "13,50", precoAntigo: "15,60", genero: "Literatura Infantil, Fábula", imagem: "pequeno principe.jpg" },
      { titulo: "Amor e Gelato", autor: "Jenna Evans Welch", preco: "42,67", precoAntigo: "46,67", genero: "Ficção", imagem: "amor e gelato.jpg" },
      { titulo: "Como Eu Era Antes de Você", autor: "Jojo Moyes", preco: "43,50", precoAntigo: "47,92", genero: "Romance de Amor, Ficção", imagem: "como eu era antes de voce.jpg" }
    ];
</script>

<section>
  <main>    
    <div class="main">
                  
        <div class="main-tag">
          <h1><b>Seja Bem Vindo à<br><span>Leia Mais</span></b></h1>
          <p>
            A melhor livraria do país. Aqui você encontra diversos títulos que<br>irão te surpreender, 
            com preços ótimos e de qualidade altissíma!
          </p>
      </div>
     </div>
</section>

    <section class="container py-5">
        <div class="featured_boks">
          <h1><b>Livros em Destaque</b></h1>
          <div class="featured_books_box">
            {#each livros as livro}
            <div class="features-books_card">
              <div class="featured_books_img">
                <img src="{livro.imagem}" alt="Imagem do Livro">
              </div>
              <div class="featured_books_tag">
                <h2>{livro.titulo}</h2>
                <p class="writer">{livro.autor}</p>
                <div class="categories">{livro.genero}</div>
                <p class="book_price">{livro.preco}<sub><del>{livro.precoAntigo}</del></sub></p>
                <a href="https://www.amazon.com.br/Livros/b?ie=UTF8&node=6740748011" class="f_btn">Saiba Mais</a>
              </div>
            </div>
            {/each}
          </div>
        </div>
      </section>


  <footer class="bg-primary text-white py-4">
    <div class="container d-flex justify-content-between">
      <div>
        <h5>Leia Mais</h5>
        <p>O sonho de levar sorrisos a cada história!</p>
      </div>
      <div>
        <h5>Links</h5>
        <ul class="list-unstyled">
          <li><a href="/" class="text-white">Início</a></li>
          <li><a href="/lancamentos" class="text-white">Lançamentos</a></li>
          <li><a href="/sobre-a-marca" class="text-white">Sobre a Marca</a></li>
        </ul>
      </div>
      <div>
        <h5>Contatos</h5>
        <p>+55 (18) 4002-8922</p>
        <p>+55 (18) 5478-3214</p>
        <p>leiamais@gmail.com</p>
      </div>
      <div>
        <h5>Redes Sociais</h5>
        <p>Facebook: @LeiaMais</p>
        <p>Instagram: @LeiaMais</p>
        <p>Twitter: @LeiaMais</p>
      </div>
    </div>
  </footer>

<style>
section .main{
    display: flex;
    align-items: center;
    justify-content: space-around;
    position: relative;
    top: 10%;
}

section .main h1{
    position: relative;
    font-size: 70px;
    top: 20px;
    left:25px;
}

section .main h1 span{
    color: rgb(38, 52, 119);    
}

section .main p{
    width: 650px;
    text-align: justify;
    line-height: 22px;
    position: relative;
    top: 20px;
    left: 25px;
}

::-webkit-scrollbar{
    width: 10px;
    height: 5px;
}

::-webkit-scrollbar-track{
   box-shadow: inset 0 0 8px rgba(0, 0, 0,0.2);
}

::-webkit-scrollbar-thumb{
    background: rgb(38, 52, 119);
    border-radius: 5px;
}

.featured_boks .featured_books_box {
    width: 100%;
    height: 500px; /* Definindo uma altura fixa para todos os cards */
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(5, 1fr); /* Ajustando o número de colunas */
    gap: 20px; /* Espaço entre os cards */
    justify-items: center;
    padding: 10px;
    overflow-x: auto; /* Habilitando a rolagem horizontal */
    scroll-behavior: smooth; /* Animação suave ao rolar horizontalmente */
}

.featured_boks .featured_books_box .features-books_card {
    width: 250px; /* Largura fixa para todos os cards */
    height: 100%; /* Faz com que os cards preencham toda a altura definida */
    text-align: center;
    padding: 15px 10px; /* Aumentei o padding para dar mais espaço entre os elementos */
    border: 1px solid #919191;
    display: flex;
    flex-direction: column;
    justify-content: space-between; /* Distribuindo o conteúdo dentro do card */
    margin: 0 10px; /* Adicionando margem para garantir espaçamento horizontal */
}

.featured_boks .featured_books_box .features-books_card .featured_books_img img {
    width: 100%;
    height: auto;
    max-height: 250px; /* Garantindo que a imagem não ultrapasse a altura do card */
    object-fit: contain; /* A imagem se ajusta sem distorção */
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag h2 {
    margin: 12px 0;
    font-size: 18px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .writer {
    color: #919191;
    font-size: 14px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .categories {
    color: rgb(38, 52, 119);
    margin-top: 8px;
    font-size: 14px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .book_price {
    margin-top: 8px;
    font-weight: bold;
    margin-bottom: 15px;
    font-size: 16px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .book_price sub {
    font-weight: 100;
    padding: 0 5px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .f_btn {
    padding: 8px 20px;
    border: 2px solid rgb(38, 52, 119);
    text-decoration: none;
    color: #000;
    border-radius: 10px;
    margin-top: 15px; /* Espaçamento adequado antes do botão */
    align-self: flex-end; /* Alinha o botão ao final do card */
}
</style>