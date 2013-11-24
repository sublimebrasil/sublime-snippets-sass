# Sass Snippets para Sublime

> Agradecemos ao [@mrmartineau](https://github.com/mrmartineau) por ter gentilmente cedido a reposição deste plugin e ao [@FichteFoll](https://github.com/FichteFoll) pelo suporte.

## Instalação

Para instalar através do [Package Control](http://wbond.net/sublime_packages/package_control), procure por **Sassy Snippets**.

Entretanto, você pode fazer o download e colocá-lo manualmente no diretório `Packages`. Lembre-se de que o plugin vai funcionar, porém não serão realizadas as atualizações.

> Note: recomendamos o uso do plugin ["Syntax Highlighting for Sass"](https://github.com/P233/Syntax-highlighting-for-Sass) plugin para destacar a sintaxe do Sass.

## Lista de Snippets

* [Directives](#directives)
* [Flags](#flags)
* [Functions](#functions)
* [CSS Extensions](#cssextensions)


### Directives

##### [content] @content

```sass
@content
```

##### [debug] @debug

```sass
@debug $0;
```

##### [each] @each

```sass
@each ${1:var} in ${2:item1, item2, item3} {
	.#{$1}$3 {
		$4
	}
}$0
```

##### [extend] @extend

```sass
@extend $0;
```

##### [for] @for

```sass
@for $i from ${1:1} through ${2:10} {
	$3
}$0
```

##### [function] @function

```sass
@function $1($3) {
	$4
	@return $5;
}$0
```

##### [if] @if @else @if

```sass
@if ${1:something} ${2:==} ${3:true/false} {
	$4
} @else if {
	$5
}${6: @else {
	$7
\}}$0
```
**or**

```sass
@if ${1:something} ${2:==} ${3:true/false} {
	$4
} @else {
	$5
}$0
```

**or**

```sass
@if ${1:something} ${2:==} ${3:true/false} {
	$4
}$0
```

##### [import] @import

```sass
@import "$0";
```

##### [include] @include

```sass
@include $0;
```

**with Sass syntax**

```sass
+$0;
```

##### [mixin] @mixin

```sass
@mixin $1($2) {
	$3
}$0
```

**with Sass syntax**

```sass
=$0;
```

##### [return] @return

```sass
@return $0;
```

##### [warn] @warn

```sass
@warn $0;
```

##### [while] @while

```sass
$i: ${1};
@while $i > ${2} {
	.#{$i} $3 {
		$4
	}
}$0
```

##### [font] @font-face

```sass
@font-face {
	font-family:$1;
	src:url($2);$0
}
```


### Flags

##### [default] !default

```sass
!default
```

##### [optional] !optional

```sass
!optional
```

### Functions

#### Color

##### [rgb] rgb()

```sass
rgb(${1:$red}, ${2:$green}, ${3:$blue})
```

##### [rgba] rgba()

```sass
rgba(${1:$red}, ${2:$green}, ${3:$blue}, ${3:$alpha})
```

##### [rgba-short] rgba()

```sass
rgba(${1:$color}, ${3:$alpha})
```

##### [red] red()

```sass
red(${1:$color})
```

##### [green] green()
```sass
green(${1:$color})
```

##### [blue] blue()
```sass
blue(${1:$color})
```

##### [mix] mix()

```sass
mix(${1:$color1}, ${2:$color2}, ${3:$weight:50%})
```

##### [hsl] hsl()

```sass
hsl(${1:$hue}, ${2:$saturation}, ${3:$lightness})
```

##### [hsla] hsla()

```sass
hsla(${1:$hue}, ${2:$saturation}, ${3:$lightness}, ${4:$alpha})
```

##### [hue] hue()

```sass
hue(${1:$color})
```

##### [saturation] saturation()

```sass
saturation(${1:$color})
```

##### [lightness] lightness()

```sass
lightness(${1:$color})
```

##### [adjust-hue] adjust-hue()

```sass
adjust-hue(${1:$color}, ${2:$degrees})
```

##### [lighten] lighten()

```sass
lighten(${1:$color}, ${2:$amount})
```

##### [darken] darken()

```sass
darken(${1:$color}, ${2:$amount})
```

##### [saturate] saturate()

```sass
saturate(${1:$color}, ${2:$amount})
```

##### [desaturate] desaturate()

```sass
desaturate(${1:$color}, ${2:$amount})
```

##### [grayscale] grayscale()

```sass
grayscale(${1:$color})
```

##### [complement] complement()

```sass
complement(${1:$color})
```

##### [invert] invert()

```sass
invert(${1:$color})
```

##### [opacity] opacity() / [alpha] alpha()

```sass
alpha(${1:$color})
```

**or**

```sass
opacity(${1:$color})
```

##### [opacify] opacify() / [fade-in] fade-in()

```sass
opacify(${1:$color}, ${2:$amount})
```

**or**

```sass
fade-in(${1:$color}, ${2:$amount})
```

##### [transparentize] transparentize() / [fade-out] fade-out()

```sass
transparentize(${1:$color}, ${2:$amount})
```

**or**

```sass
fade-out(${1:$color}, ${2:$amount})
```

##### [adjust-color] adjust-color()

```sass
adjust-color(${1:$color}, ${2:[$red]}, ${3:[$green]}, ${4:[$blue]}, ${5:[$hue]}, ${6:[$saturation]}, ${7:[$lightness]}, ${7:[$alpha]})
```

##### [scale-color] scale-color()

```sass
scale-color(${1:$color}, ${2:[$red]}, ${3:[$green]}, ${4:[$blue]}, ${6:[$saturation]}, ${7:[$lightness]}, ${7:[$alpha]})
```

##### [change-color] change-color()

```sass
change-color(${1:$color}, ${2:[$red]}, ${3:[$green]}, ${4:[$blue]}, ${5:[$hue]}, ${6:[$saturation]}, ${7:[$lightness]}, ${7:[$alpha]})
```

##### [ie-hex-str] ie-hex-str()

```sass
ie-hex-str(${1:$color})
```

#### Number

##### [abs] abs()

```sass
abs(${1:$value})
```

##### [ceil] ceil()

```sass
ceil(${1:$value})
```

##### [floor] floor()

```sass
floor(${1:$value})
```

##### [max] max()

```sass
max(${1:$numbers...})
```

##### [min] min()

```sass
min(${1:$numbers...})
```

##### [percentage] percentage()

```sass
percentage(${1:$value})
```

##### [round] round()

```sass
round(${1:$value})
```

#### String

##### [quote] quote()

```sass
quote(${1:string})
```

##### [unquote] unquote()

```sass
unquote(${1:string})
```

#### List

##### [append] append()

```sass
append(${1:$list}, ${2:$value}, ${3:[auto/comma/space]})
```

##### [index] index()

```sass
index(${1:$list}, ${2:$value})
```

##### [join] join()

```sass
join(${1:$list1}, ${2:$list2}, ${3:[auto/comma/space]})
```

##### [length] length()

```sass
length(${1:$list})
```

##### [nth] nth()

```sass
nth(${1:$list}, ${2:$n})
```

##### [zip] zip()

```sass
zip(${1:$lists...})
```

#### Introspection

##### [comparable] comparable()

```sass
comparable(${1:$number1}, ${2:$number2})
```

##### [type-of] type-of()

```sass
comparable(${1:$number1}, ${2:$number2})
```

##### [unit] unit()

```sass
unit(${1:$number})
```

##### [unitless] unitless()

```sass
unitless(${1:$number})
```

#### Miscellaneous

##### [if] if()

```sass
if(${1:$condition}, ${2:$if-true}, ${3:$if-false})
```

#### Legacy

##### [counter] counter()

```sass
counter(${1:$args...})
```

##### [counters] counters()

```sass
counters(${1:$args...})
```

### CSS Extensions

##### [placeholder] @placeholder

```sass
%$1 {
	$2
}$0
```

## Contribuindo

1. Faça o `fork`!
2. Crie um `branch` para o novo recurso: `git checkout -b my-new-feature`
3. Faça o `commit` das suas mudanças: `git commit -m 'Add some feature'`
4. Faça o `push` para o branch: `git push origin my-new-feature`
5. Faça o `pull request`


## Licença

[MIT License](http://sublimebrasil.mit-license.org/) © Sublime Brasil
