index:

<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="https://fonts.googleapis.com/css2?family=Bai+Jamjuree&display=swap" rel="stylesheet" />
    <link rel="stylesheet" href="style.css" />
    <title>Flash Cards</title>
  </head>
  <body>
    <main>
      <article class="cartao">
        <div class="cartao__conteudo">
          <div class="frente">
            <h3>O que é Javascript?</h3>
            <p>O que é Javascript?</p>
          </div>
          <div class="verso">
            <p>Javascript é uma linguagem de programação voltada à web.</p>
          </div>
        </div>
      </article>

      <article class="cartao">
        <div class="cartao__conteudo">
          <div class="frente">
            <h3>O que é CSS?</h3>
            <p>O que é CSS?</p>
          </div>
          <div class="verso">
            <p>CSS é uma linguagem de marcação para estilização de páginas.</p>
          </div>
        </div>
      </article>

      <article class="cartao">
        <div class="cartao__conteudo">
          <div class="frente">
            <h3>O que é HTML?</h3>
            <p>O que é HTML?</p>
          </div>
          <div class="verso">
            <p>HTML é a linguagem de marcação usada para estruturar páginas na web.</p>
          </div>
        </div>
      </article>
    </main>

    <footer>
      <p>Projeto desenvolvido por Gabriel Marcelino - sem fins lucrativos</p>
    </footer>
  </body>
</html>


Stlye:

:root {
    --bg-color: #0e0e0e;
    --text-color: #ffffff;
    --border-color: #ffffff;
  }
  
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Bai Jamjuree', sans-serif;
  }
  
  body {
    background: url('bg-desktop.webp') no-repeat center center fixed;
    background-size: cover;
    color: var(--text-color);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  main {
    padding: 40px;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
  }
  
  .cartao {
    width: 250px;
    height: 200px;
    perspective: 1000px;
  }
  
  .cartao__conteudo {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transition: transform 0.8s;
  }
  
  .cartao:hover .cartao__conteudo {
    transform: rotateY(180deg);
  }
  
  .frente, .verso {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    background-color: rgba(0, 0, 0, 0.6);
    color: var(--text-color);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 2px solid var(--border-color);
    border-radius: 10px;
    padding: 10px;
    text-align: center;
  }
  
  .verso {
    transform: rotateY(180deg);
  }
  
  .cartao__conteudo h3 {
    font-size: 20px;
    margin-bottom: 10px;
  }
  
  .cartao__conteudo p {
    font-size: 16px;
    line-height: 1.4;
    padding: 0 10px;
  }
  
  footer {
    background-color: rgba(0, 0, 0, 0.8);
    text-align: center;
    padding: 10px;
    color: var(--text-color);
    border-top: 1px solid var(--border-color);
  }
  
