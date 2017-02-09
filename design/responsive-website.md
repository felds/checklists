# Design de website responsivo

* [ ] Fontes
* [ ] [Favicons](#favicons)
* [ ] Imagens
* [ ] Iconografia
* [ ] Paleta de cores
* [ ] Menus
* [ ] Resoluções e orientações
* [ ] Títulos e descrições
* [ ] Estilos básicos de conteúdo
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



## Cards e descrições de compartilhamento<a name="social"></a>

**O site ou sistema deve funcionar nos tamanhos de dispositivos mais populares
e nas orientações vertical e horizontal (no caso de dispositivos móveis).**

Elementos como abas e conteúdos fixos (c/ paralax) podem não funcionar corretamente em dispositivos menores ou na horizontal, onde alguns dispositivos exibem apenas um parágrafo médio de texto.

Alguns elementos podem ser simplificados e outros até removidos caso estes não sejam extritamente necessários para o entendimento do conteúdo.

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
