<script>
    // Importa os dados dos lançamentos da pasta lib
    import { livrosl } from '$lib/livroslancamentos.js';
  </script>
  
  <div class="arrivals">
    <h1><b>Lançamentos</b></h1>
    <div class="arrivals_box">
      {#each livrosl as livro}
      <div class="arrivals-card">
        <div class="arrivals_image">
          <img src="{livro.img}" alt="{livro.titulo}">
        </div>
        <div class="arrivals_tag">
          <p>{livro.titulo}</p>
          <div class="arrivals_icon">
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-regular fa-star-half-stroke"></i>
          </div>
          <a href="https://www.amazon.com.br/Livros/b?ie=UTF8&node=6740748011" class="arrivals_btn">Saiba Mais</a>
        </div>
      </div>
      {/each}
    </div>
  </div>


<style>
    .arrivals{
    width: 100%;
    height: 100vh;
    margin-bottom: 35px;
}

.arrivals h1{
    font-size: 60px;
    text-align: center;
    margin-bottom: 35px;
}

.arrivals .arrivals_box{
    width: 96%;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
    grid-gap: 25px 0;
}

.arrivals .arrivals_box .arrivals-card{
    width: 250px;
    height: 350px;
    text-align: center;
    padding: 5px;
    border: 1px solid #919191;
    margin: auto 20px;
}

.arrivals .arrivals_box .arrivals-card:hover{
    box-shadow: 0 0 5px rgb(38, 52, 119);
}

.arrivals .arrivals_box .arrivals-card .arrivals_image{
    width: 150px;
    height: 220px;
    margin: 0 auto;
    cursor: pointer;
    box-shadow: 0 0 8px rgba(0, 0, 0,0.5);
    overflow: hidden;
}

.arrivals .arrivals_box .arrivals-card .arrivals_image img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    transition: 0.3s;
}

.arrivals .arrivals_box .arrivals-card:hover .arrivals_image img{
    transform: scale(1.1);
}

.arrivals .arrivals_box .arrivals-card .arrivals_tag p{
    font-family: queen of camelot;
    font-size: 20px;
    margin: 8px 0;
}

.arrivals .arrivals_box .arrivals-card .arrivals_tag .arrivals_icon{
    color: rgb(38, 52, 119);
    margin-bottom: 18px;
}

.arrivals .arrivals_box .arrivals-card .arrivals_tag .arrivals_btn{
    padding: 8px 20px;
    border: 2px solid rgb(38, 52, 119);
    text-decoration: none;
    color: #000;
    border-radius: 10px;
}
</style>