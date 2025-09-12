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


})

<video controls>
  <source src="video-aula.mp4" type="video/mp4">
  <track src="legenda.vtt" kind="subtitles" srclang="pt" label="Português">
  Seu navegador não suporta vídeos.
</video>

<button onclick="toggleContraste()">Ativar/Desativar Alto Contraste</button>

<script>
  function toggleContraste() {
    document.body.classList.toggle("alto-contraste");
  }
</script>

<style>
  .alto-contraste {
    background-color: black;
    color: yellow;
  }
  .alto-contraste a {
    color: cyan;
  }
</style>

<nav aria-label="Menu principal">
  <ul>
    <li><a href="#home">Início</a></li>
    <li><a href="#sobre">Sobre</a></li>
    <li><a href="#contato">Contato</a></li>
  </ul>
</nav>

<button aria-label="Abrir menu de navegação">☰</button>

<button onclick="toggleDark()">🌙 Alternar modo escuro</button>

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
</style>
