# O que é?
This Is Wagner é uma playlist pessoal minha em uma página web.
Playlist em que as faixas estão separadas por categoria. Essas são, Energy, Chill e Love. Cada categoria representa um sentimento ou situação em que eu escuto as músicas.

# Desenvolvimento da página
Para este projeto elaborei de forma simples e bonita a disposição dos elementos na tela. Todo o tempo nessa página estará sendo reproduzido um vídeo como background, para deixar ele no fundo e fixa-lo utilizei "z-index", para colocar por trás de todos os elementos, veja a seguir:
```css
video-bg {
position: fixed;
z-index: -1;
}
```
Implementei um meio de navegação prático, pois o usuário não precisa ficar rodando o scroll, ele navega nas sessões por botões(next/back), para avançar ou voltar para sessão anterior click por click. Além desse meio o usuário pode também navegar pela navbar que fica no header, nela estão as 3 categorias lado a lado, além disso, o logotipo é um botão que possibilita voltar para o início da página com um click. Para isso usei o "href", referenciando com o id de cada sessão.
```html
<a id="botaobackenergy" class="botaoback" href="#section2">↟</a>
<a id="botaonextlove" class="botaonext" href="#section4">↡</a>
```
Para exibição das fixas e com elas as letras utilizei um modal para cada uma, assim o usuário não precisa sair da página para acessar o conteúdo, praticidade para tornar a experiência confortável. Para o modal foi escrito linhas em Java Script, para mostrar e fechar ele. Para mostrar basta clicar em alguma faixa e o modal irá aparecer. Para fechar tem no canto superior direito bem no vértice da caixa um botão para fechar, ou, clicando em qualquer área fora do modal. Caso a música esteja tocando, ao fecha-lo o iframe reseta e a reprodução é encerrada no mesmo instante.
```javascript
function iniciaModal(modalID) {
    const modal = document.getElementById(modalID);
    iframe.classList.add('.iframe');
    modal.classList.add('mostrar');
    modal.addEventListener('click', (event) => {
        if (event.target.id == modalID || event.target.className == 'fechar') {
            modal.classList.remove('mostrar');
        }

    })
}

const a1 = document.querySelector('.a1');
a1.addEventListener('click', () => iniciaModal('modal1'));

$('#modal1.modal-container').on('click', function () {

    var video = $(".iframe1").attr("src");
    $(".iframe1").attr("src", "");
    $(".iframe1").attr("src", video);

});
```
```html
<div id="modal1" class="modal-container">
        <div id="modalbotao">
            <button class="fechar">✖</button>
            <iframe class="iframe1" width="530" height="300" src="https://www.youtube-nocookie.com/embed/aq_gGxMZ6tg"
                title="YouTube video player" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen></iframe>
        </div>
        <div class="modal">
            <div class="lyric">
                <h1>BE SOMEONE</h1>
                <h3><span class="white">KVSH, SCHILLIST, RAY X BEN</span> ϟ ENERGY</h3>
                <div class="linha-modal">
                    <hr class="linha-de-quebra-2">
                </div>

                <p class="lyrics">
                    lyrics
                </p>
            </div>
        </div>
    </div>

No footer no final da página você encontra links pessoais, onde você será redirecionado para meus perfis no Linked In, Git Hub e Instagram.
