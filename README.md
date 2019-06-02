<div align="center">
  <h1>Course SASS - Learning pre css processors</h1>
  <p>
    Extracted annotations of the course sass-aprendendo-pre-processadores-css book.
  </p>
</div>

## Compilations
Sass Files (scss)
```rb
sass filename.scss:filename.css
```

Keep the compiler active for  new code build automatic
```rb
sass --watch filename.scss:filename.css
```

## Commenting in code Sass

**This way, it does not appear in the code compiled**
``` css
// comment
```

**This way, it appear in the code compiled**
``` css
/** comment **/
```

## Variables Sass

**defining**
``` css
$nome_variavel = blue;
```

**using**
``` css
div {
  cor: $nome_variavel
}
```

## Good practices annotated {#cust-id}
>
> - Create variables for parameters (colors, default sizes, etcs)
> - Create mixin for code that repeat
> - Set meaningful name for code divisions
> - To nest the children elements with your father, careful to avoid too deep structures causing slowness browser
> - Use the '&' to align directly with the parent element
> - If file type is 'scss', so isn't not necessary typing the extension in the his import
> - Create folder for to organize of project
> - Concatenating 'scss' files is a good practice to reduce the request to the server


My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").

<https://www.markdownguide.org>

imagem 
![Philadelphia's Magic Gardens. This place was so cool!](/assets/images/philly-magic-gardens.jpg "Philadelphia's Magic Gardens")
imagem link
[![An old rock in the desert](/assets/images/shiprock.jpg "Shiprock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)

cores - funções
lighten(cor, porcentagem) deixa a cor informada mais clara conforme porcentagem informada
darken(cor, porcentagem) deixa a cor informada mais escura conforme porcentagem informada
PARA MAIS FUNÇÕES DE CORES CONSULTAR A DOCUMENTAÇÃO DO SASS **[SASS FUNCIONTION](http://sasslang.com/documentation/Sass/Script/Functions.html)** \| **[LINKS TWO](https://sass-lang.com/documentation/functions)**


INSTALANDO O COMPASS
gem	update	--system
gem	install	compass

criando o compass na raiz do projeto
compass create

manter o compass vigiando alterações para compilar automaticamente
compass	watch css/estilos.scss


MIXIN - cópia o código na onde é chamado (não performático)
@mixin nome {
	cor: red;
}
Usando MIXIN
.div {
	@include nome_mixin
}
Podemos passar parâmetros para os mixin 0 funções
---------------
EXTEND - deixando o código mais performático
extend permite compartilhar código entre várias regras css
criar   
    .nomeextend
usar
    @extend .nomeextend
---------------
USAR ESTA DECLARAÇÃO NO LUGAR DA DE CIMA
placeholder % retirar a classe gerada inultimente no código pelo extend
criar
    %nomeplaceholder
usar
    @extend %nomeplaceholder
---------------
podemos criar funções que retornan resultados

@function retorna-largura() {
	@return 1 *2;
}

função round para valore quebrados (18.58)

Sass	minifique	seu	arquivo [cust](#cust)
sass	--watch	estilos.scss:/estilos.css	--style	compressed


LER NO SITE DO SASS (http://sass-lang.com),	dos	segui
http://susy.oddbird.net)
http://sasslang.com/documentation/Sass/Script/Functions.html.
https://sass-lang.com/documentation/functions funções sass


TO SEE TOO
Controladores	de	fluxo	(	@if	,		@else	) I love supporting **[SASS-LANG](http://sass-lang.com)**.
Laços	de	repetição	(	@for	,		@while	)
Diretiva	para	debugar	o	código	(	@debug	)
Diretivas	erros	e	alertas
Source	map	(ajuda	a	debugar	no	Devtools)
Susy	(não	é	uma	feature,	mas	sim	um	framework	para
montar	grids	customizadas	-	http://susy.oddbird.net)

Sugiro	 que	 você	 faça	 testes	 em	 seus	 projetos	 para	 ver	 a
diferença	 entre	 eles.	 Recomendo	 esse	 post	 interessantíssimo	 à
respeito	 do	 tema	 que	 dá	 vitória	 para	 o	 mixin:
http://csswizardry.com/2016/02/mixins-better-for-performance.

Vamos	 abrir	 o	 arquivo	 HTML	 principal	 dessa	 página,	 o
	index.html	.	Esse	arquivo	e	o	 restante	do	projeto	 se	encontram
neste	 link:	 https://github.com/designernatan/livro-sass.	 Se
possível,	 dê	 uma	 estudada	 com	 carinho	 no	 código,	 tanto	 HTML
quanto	CSS,	para	se	situar	melhor	no	projeto,	como	se	você	tivesse
acabado	de	entrar	na	equipe	de	front-end	da	Apeperia.


TASK RUNNERS
As	ferramentas	mais	usadas	desse	tipo	atualmente	são	o	Gulp
(http://gulpjs.com)	e	o	Grunt	(http://gruntjs.com/).

http://blog.sass-lang.com	 —	 Blog	 da	 galera	 que
desenvolve	 o	 Sass.	 Sempre	 quando	 há	 novas
features,	eles	postam	a	respeito.
http://thesassway.com	 —	 Gosto	 bastante	 desse
por	 dividir	 seus	 posts	 em	níveis,	 do	iniciante	ao
avançado.

Fóruns:
http://www.guj.com.br
https://github.com/frontendbr
http://forum.tableless.com.br
http://forum.casadocodigo.com.br
Comunidades:
Meetup	CSS
Meetup	FrontUX
Femug
