# :memo: Notes
## CSS
- - -
### Resources
* [W3C CSS](https://www.w3.org/Style/CSS/)
* [The CSS validator](https://jigsaw.w3.org/css-validator/)
* [CSS: Cascading Style Sheets](https://developer.mozilla.org/en-US/docs/Web/CSS)
* [MDN web docs](https://developer.mozilla.org/en-US/)
* [CSS Reference](https://cssreference.io/)
* [CSS Cascading and Inheritance Level 5](https://www.w3.org/TR/css-cascade-5/)
* [Introducing the CSS Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)
* [Aspectos básicos del diseño web adaptable](https://developers.google.com/web/fundamentals/design-and-ui/responsive/?hl=es)
### Terms and concepts
* CSS or Cascading Style Sheets

* Syntax
	- Shorthand
* Indention
* Comments

* Rules
	- inline in element with attribute style
	- in block in element with tag style
	- link to external with css file
	- import a style sheet into another style sheet

* Selector
	* Element
		- Block
		- Inline
	* Declaration or block
		- Attribute
		- Value

* Selectors
	- Universal
	- Mark or Tag or Type
	- Class
	- Attribute / Attribute and value
	- Id

* Attributes
	- Typography
	- Container
	- Content

* Values and Units
	- Absolute (ej: px)
	- Relative (ej: %, em, rem)

* Cascade
	* Algorithm
		- Origin
		- Specificity
		- Order

* Origin
	1. Author
	2. User custom
	3. User Agent stylesheet / Browser

* Specificity
	1. !important keyword
	2. Inline
	3. Identifier
	4. Class and pseudo-class
	5. Type and pseudo-element

* Collision

*	Prioritize
	1. !important keyword
	2. Inline
	3. Identifier
	4. Class and pseudo-class
	5. Markor Tag or Type and pseudo-element
	6. Order
	7. Author
	8. User custom
	9. User Agent stylesheet / Browser

* Hierarchy
	- Descendant
	- Parent element
	- Sibling element
	- Child element
	- Automatic or default mode
	- Manually or force mode
	* CSS Combinators

* Pseudo-class :
	- State
	- Position
	- Relation
* Pseudo-element ::
	- Typographic
	- Content

* Color
	* Values
		- keywords
		- Hexadecimal
		- Hexadecimal with Alpha
	* Functions
		- RGB
		- RGBA
		- HSL
		- HSLA

* Fonts

* Media queries
	- Breakpoint
	- X-device first

* Custom properties or Variables

* Animations

* Reset styles

* CSS browser prefixes
	- -webkit-	Chrome, Safari, Android
	- -moz-		Firefox
	- -o-			Opera
	- -ms-		Internet Explorer
	- -khtml-		Konqueror

* CSS Methodlology
	- BEM
#### Examples
```
/* RESET STYLES MANUALLY */
html {
  height: 100%;
  font-size: 62.5%;
  box-sizing: border-box;
  scroll-behavior: smooth;
}
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
	border-width: 0;
  border-style: solid;
  border-color: #000;
}
body {
  height: 100%;
}
img,
svg,
video,
canvas,
audio,
iframe,
embed,
object {
	max-width: 100%;
  display: block;
  vertical-align: middle;
}
a {
  text-decoration: none;
  color: inherit;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-size: inherit;
  font-weight: inherit;
}
ol,
ul {
  list-style: none;
}
input,
button {
  font: inherit;
  color: inherit;
  border: none;
  background-color: transparent;
}
button:focus {
  outline: 1px dotted;
  outline: 5px auto -webkit-focus-ring-color;
}
i {
	font-size: 16px;
}
.google-map * {
  border-style: none;
}

/* SEUDOCLASES ":" de estado, de posición, de relación  */
ELEMENTO:SEUDOCLASE {}
a:link {}/* apariencia de enlaces no visitados */
a:visited {}/* enlaces ya visitados */
a:hover {}/* cuando el puntero del mouse esté sobre */
a:active {}/* cuando se selecciona, un click */
a:focus {}/* otro estado, cuando esté seleccionado */
p:first-line {}/* dar estilos a la primera línea del parrafo */
p:nth-child(número de la línea){}/* dar estilo a otras líneas del parrafo */
:not(elemento)/* dar estilos a los elementos que NO sean <elemento> */

/* SEUDOELEMENTOS "::" tipográficos, de contenido */
SELECTOR::SEUDOELEMENTO {}
SELECTOR::before{}/* seudoelemento */
SELECTOR::after{}/* seudoelemento */
p::first-letter {}/* dar estilo a la primera letra del parrafo */
p::first-line {}/* dar estilo a la primera línea del parrafo */
div::before {}/* agregar un elemento despues de nuestra caja */
div::after {}/* agregar un elemento antes de nuestra caja */
li::nth-of-type()/* hacer referencia a un elemento del tipo ...  */
elemento::selection {}/* dar estilo cuando lo seleccione */
#nombreIdentificador {}/* selector id, crear un id, no usar id para estilos, solo para javascript */
.nombreClase {}/* selector class, crear una clase */

/* COMBINAR SEUDOCLASES CON SEUDOELEMENTOS */
SELECTOR:SEUDOCLASE:SEUDOELEMENTO {}
div:hover::before {}
div:hover::after {}

/* CSS Combinators */
[atributo ~ ="valor"]/* ~ para apuntar a elementos que contengan una palabra especifica */
[atributo | ="valor"]/* | para apuntar a elementos que comiencen con una palabra especifica */
[atributo ^ ="valor"]/* signo paraguas para apuntar a elementos que comiencen con un valor especifico */
[atributo $ ="valor"]/* $ para apuntar a elementos que terminen con un valor especifico */
[atributo * ="valor"]/* * para apuntar a elementos que contengan un valor especifico */
selector + selector {}/* apuntar a elementos hermanos adyacentes */
selector ~ selector {}/* apuntar a elementos hermanos inmediatos (todos los hermanos) */

@font-face {}/* agregar fuentes */

/* MEDIAQUERIES */
/* MOBILE FIRST - consiste en codificar para dispositivos moviles y dar cambios a medida que crecen las pantallas */
/* cambios a partir de 480px en adelante */
@media screen and (min-width: 480px) {
	max-width: 420px;
}
/* cambios a partir de 768px en adelante */
@media screen and (min-width: 768px) {
	max-width: 720px;
}
/* cambios a partir de 992px en adelante */
@media screen and (min-width: 992px) {
	max-width: 960;
}

/* es clave trabajar con medidas porcentuales y no fijas */

/* crear animaciones */
@keyframes{}

/*  */
@-webkit-keyframes {
	from {}
	to {}
}

SELECTOR {
	/* ATRIBUTOS \ PROPIEDADES */
	width:;/* ancho */
	height:;/* alto */
	margin:;/* margen externo */
	padding:;/* margen interno */
	border:;/* borde */
	border-style:;/* estilo del borde */
	border-width:;/* ancho del borde */
	border-color:;/* color del borde */
	border-radius:;/* bordes redondeados, ovalos, circulos */
	border-collapse:;/* unificar bordes */
	border-spacing:;/* espaciado de los bordes */
	box-shadow:;/* dar sombra a las cajas */
	box-sizing:;/* incluir el padding a su tamaño, que el padding no sume a su tamaño -webkit- -moz- */
	cursor:;/* cambiar aspecto del cursor  */
	vertical-align:;/* alineción vertical, con el valor "top" quito espacios */
	display/* controlar la ubicación tipo bloque, tipo línea, flex */
	display: flex;/* con el valor "flex" habilitamos "flexbox", contenedor padre */
	opacity:;/* dar opacidad */
	color:;/* dar color */
	justify-content:;/*  */
	align:;/*  */
	align-items:;/*  */
	align-content:;/*  */
	order:;/*  */
	align-self:;/*  */
	visibility:;/* controlar la visivilidad, ocultar sin quitar */
	position:;/* controlar la posición, normal, relativo, absoluto, fijo, flotante */
	top:; right:; bottom:; left:;/* controlar la flotación, la ubicación de un elemento tipo bloque */
	float:;/* que el elemento flote a la derecha, izquierda,  */
	clear:;/* permite limpiar, resetear, corrige errores de float */
	content: "";/*  */
	overflow:;/* otra manera de corregir errores de float, más recomendada */
	overflow:;/* evitar que el contenido se desborde de su contenedor */
	overflow-x:;/* eliminar cualquier scroll horizontal */
	overflow-y:;/*  */
	overflow-wrap:;/*  */
	z-index/* establecer el nivel de capa, controlar sobreposición de cajas - SIEMPRE debe ir acompañado de "position"*/
	background:;/* fondo */
	background: url();/* imagen de fondo */
	background-image:;/* imagen de fondo */
	background-repeat:;/* repetición de la imagen de fondo */
	background-size:;/* tamaño del fondo */
	background-size:cover;/* tamaño imagen del fondo al 100% */
	background-attachment:;/* fijar el fondo o dejarlo scroll */
	background-position:;/* posición de la imagen */
	background-color:;/* color de fondo */
	font-size:;/* tamaño de la fuente */
	text-decoration:;/* decoración del texto */
	font-family:;/* fuente familia */
	font-style:;/* estilo del texto */
	font-weight:;/* ancho del texto */
	font-variant:;/* modificar el aspecto de la fuente, ej que las primeras sean mayusculas */
	font:;/* shorthand o método abreviado */
	text-align:;/* alinear texto */
	text-transform:;/* transformar todo el texto a mayusculas, minuscula, capital */
	text-shadow:;/* poner sombra al texto */
	text-overflow:;/*  */
	text-indent:;/* identar */
	text-decoration:;/* decorar */
	letter-spacing:;/* ajustar espaciado entre letras */
	word-spacing:;/* ajustar espaciado entre palabras */
	line-height:;/* ajustar espaciado de altura de línea de texto */
	list-style:;/* dar estilo a las listas */
	list-style-type:;/* dar estilo a las listas */
	list-style-image:;/* para poner una imagen */
	list-style-position:;/* dar estilo a las listas */
	empty-cells:;/* dar estilo a las tablas a las celdas vacias */
	cursor:;/* cambiar el puntero */
		transform:;/* hacer transformaciones,  animaciones -webkit- -moz- */
	transform:perspective()/* cambios en perspectiva visual */
	transform:translate();/* trasladar elemento */
	transform:scale();/* escalar elemento */
	transform:rotate();/* rotar elemento */
	transform:skew();/* sesgar elemento */
	transform-origin/*  */
	transition:nombre del elemento valores ease linear;/* transiciones */
	transition-property:;/* especificar aplicación por ejemplo cuando tengo varias tranciciones */
	transition-delay:;/* un retrazo en la transición */
	transition-duration:;/* especificar tiempo en la transición */
	transition-timing-function:;/* especificar tiempo en la transición en sus diferentes estados */
	animation-name:;/* manejar animaciones */
	animation-duration:;/* establecer duración de la animación */
	animation-iteration-count:;/* establecer cuanto tiempo durará la animación */
	animation-delay:;/*  */
	animation-timing-function:;/*  */
	@keyframes{}/* crear animaciones */
	/* FLEXBOX PADRE */
	display: flex;/* Habilitar, activar FLEXBOX, flex o inline-flex */
    flex-direction: row;/* row, row-reverse, column, column-reverse */
	flex-wrap: nowrap;/* nowrap, wrap */
    justify-content: flex-start;/* flex-start, flex-end, center, space-between, space-around - alineación de ítems sobre eje principal */
	align-items: stretch;/* stretch, flex-start, flex-end, center - alineación de ítems sobre el eje cruzado*/
	flex-flow:;/* combina "flex-direction" con "flex-wrap" */
	/* FLEXBOX HIJO */
	flex-shrink:;/* controla como se contrae */
	flex-grow:;/* añade espacio sobre eje principal */
	flex-basis: auto;/* define el tamaño de un ítem en términos del espacio que deja como espacio disponible */
	align-self:;/*  */
	flex:;/* combina "flex-shrink" "flex-grow" "flex-basis" */
	flex: initial;/* el ítem se restablece con los valores iniciales de Flexbox */flex: 0 1 auto;
	flex: auto;/* los ítems pueden crecer y llenar el contendor así como encoger si se requiere */flex:1 1 auto;
	flex: none;/* se crearán ítems flex totalmente inflexibles */flex: 0 0 auto;
	flex:; /* <positive-number>*/flex: x x x;
	flex: 0 0 calc(33.3% - 1rem);/* Ej. aquí el rem es como un padding */
	top: 80vh;
}
```
- - -
## Software Developer
[Javier Andrés Garzón Patarroyo](https://javierandresgp.com)
