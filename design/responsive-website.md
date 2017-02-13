# Design de website responsivo

* [ ] Fontes
* [ ] [Favicons](#favicons)
* [ ] Imagens
* [ ] Iconografia
* [ ] Paleta de cores
* [ ] Menus
* [ ] Resoluções e orientações
* [ ] Títulos e descrições
* [ ] [Estilos básicos de conteúdo](#estilos-básicos-de-conteúdo)
* [ ] [Cards e descrições de compartilhamento](#social)
* [ ] [Interações em diferentes dispositivos](#device-specific-interactions)
* [ ] [404](#404)



## Favicons<a name="favicons"></a>

**O site ou sistema deve ter os ícones compatíveis com os principais sistemas operacionais e navegadores.**

O navegador Safari, assim como o Windows mobile e desktop, exibe apenas a silhueta do ícone;  
O iOS não permite o uso de transparências;  
devido aos diversos tamanhos de tela e densidade de pixels, é bem difícil gerenciar tudo isso manualmente.


### Real Favicon Generator

O site http://realfavicongenerator.net/ consegue gerar um pacote de ícones compatíveis com todos os navegadores e SOs mais usados.

Além disso, ele também gera os temas para Android e customiza o ícone de aplicação no Windows.


## Estilos básicos de conteúdo

Como devem se parecer os seguintes elementos? Como eles devem se comportar em diferentes
resoluções de tela?

```html
<h1>Título principal (artigo)</h1>

<h2>Título secundário (seção do artigo)</h2>
<p>Cada tópico do conteúdo.</p>

<h3>Título terciário (detalhes ou sub-seções)</h3>
<p>Neste documento, é a descrição de alguma ferramenta ou processo.</p>

<ul>
  <li>Listas NÃO-ORDENADAS</li>
  <li>com conteúdos de diferentes tamanhos.</li>
  <li>palavras, frases, números e textos mais extensos...</li>
  <li>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
    non proident, sunt in culpa qui officia deserunt mollit anim id est
    laborum.
   </li>
</ul>

<ol>
  <li>Listas ORDENADAS (opcional)</li>
  <li>com conteúdos de diferentes tamanhos.</li>
  <li>palavras, frases, números e textos mais extensos...</li>
  <li>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
    non proident, sunt in culpa qui officia deserunt mollit anim id est
    laborum.
   </li>
</ol>

<p>
  <a href="#">Links</a>
  e
  <button type="button">Botões</button>
</p>
```

<!-- @TODO forms, images, deeper lists -->


## Cards e descrições de compartilhamento<a name="social"></a>

**O site ou sistema deve funcionar nos tamanhos de dispositivos mais populares
e nas orientações vertical e horizontal (no caso de dispositivos móveis).**

Elementos como abas e conteúdos fixos (c/ paralax) podem não funcionar
corretamente em dispositivos menores ou na horizontal, onde alguns dispositivos
exibem apenas um parágrafo médio de texto.

Alguns elementos podem ser simplificados e outros até removidos caso estes não
sejam extritamente necessários para o entendimento do conteúdo.

### Breakpoints mais comuns

Segue uma tabela com os 4 breakpoints máximos mais significantes usados em alguns sites:

| Site            | Celular P | Celular G | Tablet / Desktop P  | Desktop G |
|-----------------|-----------|-----------|---------------------|-----------|
| Apple.com       | 419       | 767       | 1023                | 1275      |
| YouTube         | 325       | 657       | 1080                | 1294      |
| G1              | 320       | 619       | 959                 | 1199      |
| Huffington Post | 480       | 767       | 995                 | 1190      |
| Twitter         | 325       | 520       | 880                 | 1094      |
| Bootstrap       | 576       | 768       | 992                 | 1200      |



## Interações em diferentes dispositivos<a name="device-specific-interactions"></a>

Como o conteúdo vai reagir a mouse, touch, ambos ou nenhum deles?

Não é recomendado, por exemplo, que algum conteúdo seja revelado apenas no `hover`,
já que esta interação não acontece em dispositivos com touch.



## 404

O que deve aparecer quando o usuário tentar acessar uma página que não existe?

É interessante informar o usuário do erro ao mesmo tempo que o direciona para algum lugar de interesse (ex: home, busca, tags/categorias/posts/páginas mais populares).
