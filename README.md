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

## Good practices annotated
>
> - create variables for parameters (colors, default sizes, etcs)
> - Create mixin for code that repeat
> - Set meaningful name for code divisions
> - aninar os elementos filhos com seu pai com cuidado para evitar estruturas muito profundas causando lentidão no browser
> - usar o & para alinamento direto com o elemento pai
> - caso arquivo sejá scss não é necessário usar a extenção do arquivo no import
> - criar pastas para organização do projeto
> - concatenar arquivos scss é uma boa prática reduzindo o request ao servidor

cores - funções
lighten(cor, porcentagem) deixa a cor informada mais clara conforme porcentagem informada
darken(cor, porcentagem) deixa a cor informada mais escura conforme porcentagem informada
PARA MAIS FUNÇÕES DE CORES CONSULTAR A DOCUMENTAÇÃO DO SASS
http://sasslang.com/documentation/Sass/Script/Functions.html.
https://sass-lang.com/documentation/functions funções sass


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

Sass	minifique	seu	arquivo
sass	--watch	estilos.scss:/estilos.css	--style	compressed

LER NO SITE DO SASS (http://sass-lang.com),	dos	segui
Controladores	de	fluxo	(	@if	,		@else	)
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
