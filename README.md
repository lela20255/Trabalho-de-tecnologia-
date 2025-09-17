document.addEventListener('DOMContentLoaded', function () {  
    const botaoDeAcessibilidade = document.getElementById('botao-acessibilidade')
    const opcoesDeAcessibilidade = document.getElementById('opcoes-acessibilidade')

    botaoDeAcessibilidade.addEventListener('click', function () {
        botaoDeAcessibilidade.classList.toggle('rotacao-botao');
        opcoesDeAcessibilidade.classList.toggle('apresenta-lista')

    })

    const aumentaFonteBotao = document.getElementById('aumentar-fonte');
    const diminuiFonteBotao = document.getElementById('diminuir-fonte');

    const alternaContraste = document.getElementById('alterna-contraste')

    let tamanhoAtualFonte = 1;

    aumentaFonteBotao.addEventListener('click', function () {
        tamanhoAtualFonte += 0.1;
        document.body.style.fontSize = `${tamanhoAtualFonte}rem`

    })

    diminuiFonteBotao.addEventListener('click', function () {
        tamanhoAtualFonte -= 0.1;
        document.body.style.fontSize = `${tamanhoAtualFonte}rem`

    })

    alternaContraste.addEventListener('click', function () {
        document.body.classList.toggle('alto-contraste')
    })


})<button onclick="toggleDark()">🌙 Alternar modo escuro</button>

<script>
  function toggleDark() {
    document.body.classList.toggle("dark");
  }
</script>

<style>
  .dark {
    background: #121212;
    color: #eee;
  }
</style><a href="#conteudo" class="skip-link">Pular para o conteúdo principal</a>

<style>
  .skip-link {
    position: absolute;
    left: -999px;
    top: auto;
    background: #000;
    color: #fff;
    padding: 8px;
  }
  .skip-link:focus {
    left: 10px;
    top: 10px;
  }
</style>

<main id="conteudo">
  <h1>Bem-vindo ao site acessível</h1>
</main>
<button onclick="mostrarAviso()">Mostrar aviso</button>
<p id="aviso" role="alert"></p>

<script>
  function mostrarAviso() {
    const aviso = document.getElementById("aviso");
    aviso.textContent = "Sua sessão vai expirar em 2 minutos!";
    let audio = new Audio("aviso.mp3");
    audio.play();
  }
</script><video controls>
  <source src="video-aula.mp4" type="video/mp4">
  <track src="legendas.vtt" kind="subtitles" srclang="pt" label="Português">
  Seu navegador não suporta o elemento de vídeo.
</video>

<p><a href="transcricao-video.html">Acesse a transcrição completa do vídeo</a></p>

<form>
  <label for="nome">Nome:</label>
  <input type="text" id="nome" aria-required="true">

  <label for="email">E-mail:</label>
  <input type="email" id="email" aria-required="true">

  <button type="submit">Enviar</button>
</form>
