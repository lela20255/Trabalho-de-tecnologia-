<button id="botao-acessibilidade">♿ Acessibilidade</button>

<div id="opcoes-acessibilidade" class="lista-acessibilidade">
  <button id="aumentar-fonte">Aumentar Fonte</button>
  <button id="diminuir-fonte">Diminuir Fonte</button>
  <button id="resetar-fonte">Fonte Padrão</button>
  <button id="alterna-contraste">Ativar/Desativar Alto Contraste</button>
  <button id="toggle-dark">Alternar Modo Escuro</button>
  <button id="modo-leitura">Modo Leitura</button>
  <button id="toggle-animacoes">Ativar/Desativar Animações</button>
  <button id="espacamento">Alternar Espaçamento</button>
</div>

<script>
document.addEventListener('DOMContentLoaded', function () {
  const botaoDeAcessibilidade = document.getElementById('botao-acessibilidade');
  const opcoesDeAcessibilidade = document.getElementById('opcoes-acessibilidade');

  botaoDeAcessibilidade.addEventListener('click', function () {
    botaoDeAcessibilidade.classList.toggle('rotacao-botao');
    opcoesDeAcessibilidade.classList.toggle('apresenta-lista');
  });

  const aumentaFonteBotao = document.getElementById('aumentar-fonte');
  const diminuiFonteBotao = document.getElementById('diminuir-fonte');
  const resetarFonteBotao = document.getElementById('resetar-fonte');
  const alternaContraste = document.getElementById('alterna-contraste');
  const toggleDark = document.getElementById('toggle-dark');
  const modoLeitura = document.getElementById('modo-leitura');
  const toggleAnimacoes = document.getElementById('toggle-animacoes');
  const espacamento = document.getElementById('espacamento');

  let tamanhoAtualFonte = 1;
  let espacamentoAtivo = false;
  let leituraAtiva = false;

  aumentaFonteBotao.addEventListener('click', function () {
    tamanhoAtualFonte += 0.1;
    document.body.style.fontSize = `${tamanhoAtualFonte}rem`;
  });

  diminuiFonteBotao.addEventListener('click', function () {
    tamanhoAtualFonte -= 0.1;
    document.body.style.fontSize = `${tamanhoAtualFonte}rem`;
  });

  resetarFonteBotao.addEventListener('click', function () {
    tamanhoAtualFonte = 1;
    document.body.style.fontSize = "1rem";
  });

  alternaContraste.addEventListener('click', function () {
    document.body.classList.toggle('alto-contraste');
  });

  toggleDark.addEventListener('click', function () {
    document.body.classList.toggle('dark');
  });

  modoLeitura.addEventListener('click', function () {
    leituraAtiva = !leituraAtiva;
    if (leituraAtiva) {
      document.body.classList.add('modo-leitura');
    } else {
      document.body.classList.remove('modo-leitura');
    }
  });

  toggleAnimacoes.addEventListener('click', function () {
    document.body.classList.toggle('sem-animacoes');
  });

  espacamento.addEventListener('click', function () {
    espacamentoAtivo = !espacamentoAtivo;
    if (espacamentoAtivo) {
      document.body.classList.add('espacamento');
    } else {
      document.body.classList.remove('espacamento');
    }
  });
});
</script>

<style>
/* Alto contraste */
.alto-contraste {
  background-color: black !important;
  color: yellow !important;
}
.alto-contraste a { color: cyan !important; }

/* Dark mode */
.dark {
  background: #121212 !important;
  color: #eee !important;
}

/* Modo leitura */
.modo-leitura {
  max-width: 800px;
  margin: auto;
  font-size: 1.2rem;
  line-height: 1.8;
  background: #fdfdfd;
  color: #111;
}

/* Desativar animações */
.sem-animacoes * {
  animation: none !important;
  transition: none !important;
}

/* Espaçamento extra */
.espacamento {
  line-height: 2 !important;
}
</style>
