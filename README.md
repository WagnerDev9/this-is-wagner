# This Is Wagner
Aqui você verá uma playlist pessoal minha em uma página web.
Playlist em que as faixas estão separadas por categoria. Essas são, Energy, Chill e Love. Cada categoria representa um sentimento ou situação em que eu escuto as músicas.

#Desenvolvimento da página
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

No footer no final da página você encontra links pessoais, onde você será redirecionado para meus perfis no Linked In, Git Hub e Instagram.
