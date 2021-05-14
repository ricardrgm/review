# REVIEW DEL CURSO DE FRONT-END WEB DEVELOPER

## Día 1- 22 ABR

Páginas Web: Contenido de distinto tipo; imágenes, texto, vídeo, sonido, ... mostrado a través de un **navegador**.
Las páginas web para ser visualizadas de forma pública tienen que estar alojadas en un **servidor web**

Las webs son **texto** están desarrolladas en un lenguaje de marcas: **HTML**

```html
  <!DOCTYPE html>
  <html>
    <head>INFORMACION QUE NO SE VISUALIZA EN LA PAGINA</head>
    <body></body>
  </html>
```

Imagen: `<img>`
Titulo: `<h1>`
Lista desordenada: `<ul><li>`
Lista ordenada: `<ol><li>`
Hipervínculo: `<a></a>`
Texto: `<p>`

[página del curso](https://bcncodes-academy.web.app)

[MDN: La biblia del desarrollo web](mdn.com)

## Día 2 - 23 Abril

Elementos de bloque vs en linea

Elementos de bloque: div, p, h1, h2, main, header, footer,...
Elementos de línea: img, a, span, strong, i, em,...

Elementos semánticos:
header: contenido es la cabecera de la página
footer: contenido que va al pie de página
nav: barra navegación

strong, ul, table, ...

Comenzamos el ejercicio del [blog Anden27](http://anden-27.blogspot.com/2018/03/museo-de-los-vikingos-en-oslo.html)

## Día 3 - 26 Abril

Inicio CSS:
formato de una regla CSS
concepto de herencia de estilos
selectores de id y de clase

Ejercicio con selectores de clase
Recepta de la iaia. EJercicio entregable

## Día 4 - 27 Abril

Selectores avanzados: Según la posición en el árbol podemos seleccionarlos
Ej.: 

```css
selección de descendientes:
header a{ }
body nav{ }
selección hijos directos:
body > nav { }
header > nav { }
selección por agrupación:
p, h2{ }
selección por un atributo: img[src="gatito.jpg"]{ }
selección por pseudoelementos: div::before{ }
selección por pseudoclases: a:hover{ }
```
BOX-MODEL || MODELO DE CAJA

elemento de bloque: estructura de caja: contenido | padding | border | margin
medidas de una caja: ancho de una caja por defecto se refiere al contenido. Se puede cambiar con la propiedad:
    `box-sizing` y valor `border-box`
    
## Día 5 - 28 Abril

Posicionamiento - Positioning: 
1. propiedad positioning;
2. display: flex;
3. display: grid;

1. Positioning
  - `position: static`, posición por defecto, el elemento no se puede mover de su lugar,
  - `position: relative`, elemento se mueve si se alteran los valores de las props: top, left, right or bottom. El elemnto se desplaza el hueco no se rellena.
  - `position: absolute`, el se mueve igual que el relative, pero su espacio se ocupa por el siguiente elemento. Las coordenadas se fijan respecto al elemento superior posicionado como relative, y si no hay ninguno respecto al body.
  - `position: fixed`: 0 que absolute pero el el no se mueve con scroll.
  - `position: sticky`:  0 que fixed pero hace scroll hasta que el scroll llega a las coordenadas del elemento.

---

JS
codeCombat
como se asignan valores a variables y se imprimen por pantalla.

## Día 6 - 29 Abril

JS

Cómo se declaran variables: 
```js
let nom_variable = valor;
const nom_constante = valor;
```

Tipos de variable:
```js
let nombre = "Pepe"; // nombre es una variable de tipo string
let num = 3; // num es una variable de tipo number
let bandera = true; // bandera es de tipo boolean
```

Una variable sin valor devuelve `undefined`

Operadores:
+ --> se utiliza para sumar number o para concatenar strings.
"-", "/","*","%", "**"

Sumar numero number + string = concatenar strings

---

CSS

pseudo-elementos: elementos que no pertenecen a la página pero se generan sobre elementos que ya existen.




```css
p::before{
  content="":
}

after, first-letter, first-line, selection, etc.
```

## Día 7 - 30 de Abril

Pseudo-classes: Diferentes estados que puede tener un elemento. Ej.: `:hover`, `:visited`, `:link`, etc.

Flexbox: librería que se ocupa de posicionar elementos html.
  - Necesita un elemento contenedor al que se aplica el flex: `display:flex` para modificar el comportamiento de los hijos
  - Propiedades del contenedor: `flex-flow: column wrap`, `justify-content: center`, `align-items: center`
  - Propiedades de los hijos: `order: 1`, `align-self`

## Día 8 - 3 Mayo

Repaso de semánticos HTML,

Media queries: `@media()`
  - Diseño Adaptativo: adaptamos nuestra web al ancho del dispositivo.
  - Mobile first: el diseño de reglas para el móvil son el por defecto, van fuera de los `@media()`
  
  ```css
  p{
  font-family: ...;
  display: none;
  }
  
  @media(min-width:480px){
    p{
      display:block;
    }
  }
  
  ``` 

### D-ia 9 - 4 Mayo

JS
Condiciones:
Modificadores del flujo de programación: if(_condicion_){instrucciones} else {instrucciones}
  - if(_condicion1_){}else if(_condicion2_)...

CSS
propiedades: `overflow: hidden | scroll | auto` 
             `z-index:1` posicionar elementos en el eje z. 

### Día 10 - 5 Mayo

Transformaciones, transiciones y animaciones:

```css
@keyframes movimiento {
0%{transform:translate(0px); background-color: red;}
25%{transform: translate(25px); background-color:black;}
...
100%{transform: translate(100px)}
}
transform: translate(), rotate(), scale(), skew(), matrix()
transition: all 1.5s   //animación disparada por un evento, que cesa con el evento
animate: movimiento 1.5s 0s infinite alternate
```

### Día 11 - 6 Mayo

JS
**función**
Agrupación de código con el propósito de ser reutilizado

```js
function sayHello(){
  console.log('Hello');
}

function sayHello(nombre){
console.log(`Hello ${nombre}`);
}
``` 

### Día 12 - 7 Mayo


### Día 13 - 10 Mayo

GRIDCSS

- Igual que flex, se aplica al contenedor para posicionar los elementos hijos.
- Tiene dos partes:
-   Definición de la cuadrícula (grid)
-   Se posicionan los elementos en la cuadrícula

```css
.padre{
  display: grid;
  /*Opción 1 */
  grid-template-areas: "header header header header"
                       "main   main   main   aside"
                       "footer footer footer footer"
 /*Opción 2 */                      
 grid-template-areas: "header  header"
                       "main   aside"
                       "footer footer"                       
  grid-template-columns: 3fr 1fr;
  grid-template-rows: 1fr 8fr 1fr;
                         
}

header{ grid-area:header; }
main {grid-area: main; }
aside {grid-area: aside; }
footer{ grid-area: footer; }

---
.hijo1{
  grid-column: 1;
  grid-rows: 1 /span 2;
}
```
### Día 14 - 11 Mayo

JS - arrays
-----------

Colecciones ordenadas de elementos. 

```js
let miArray = [1,2,3,4,5];
let miArrayStrings = ['Hola','que','hase'];

La posición que ocupa el elemento en el array comienza con la posición 0.

miArray.length: núm. elementos que tiene
miArray.splice(i,j);: función que elimina o sustituye elementos del array.

for(let i=0; i<miArray.length; i++){
  console.log(miArray[i]);
}
```
### Dia 15 - 12 Mayo

Repaso de maquetación html-css: code-along  YUM-YUM

1. Estructuración con semánticos
2. Preparación de los assets: imágenes, fuentes,...
3. Dar estilos: 
  1. Linkar las hojas de estilo.
  2. Dimensionamos cajas principales
  3. Posicionamos cajas principales
  4. Empezamos a dimensionar y posicionar elementos hijos. Comenzando por el elemento superior. (RECOMENDADO Comentarios en el css para indicar secciones del documento)
  5. Detalles:
    1. Tamaño fuentes
    2. Ajuste fino de espacios: padding y margin
    3. Colores
**Recomendaciones**:
  - imágenes si tienen contenido semántico son `<img>`. Si son estéticas son background.
  - Utilizar herramientas para: selección colores (color-pickers), generación de gradientes, conversión de colores a filtros, buscador de fuentes (what-a-font, fontis,...)
  - Utilizar validadores del HTML y CSS: w3validator o similares
  - Imprescindible tener abierto el inspector del navegador. 
  - Antes de utilizar una propiedad que no conocemos comprobar su sintaxis en MDN o W3SCHOOL.
  - No piquéis. Utilizad las recomendaciones del vscode.
  - Instalar extensiones de vscode de productividad: cssgenerator, browsersync, html y css snippets,...
  - PACIENCIA

### Día 16 - 13 Mayo

Cómo escribir funciones en ES6:
  `() => { }` -- Función flecha ó arrow function 
  
  Son funciones anónimas. Una función flecha debe estar asignada a una variable.
  El equivalente de `function(){...}`
  
  `let miFuncion = (params) => {... contenido de la función}`
  No tienen contexto.

---
Métodos Avanzados de Arrays:

- Funciones iteradoras. 
- Funciones que reciben por parámetro otra función. La función que se pasa por parámetro se llama **callback**
```js
let saludar = (e)=>console.log(`hola ${e}`);

let array = ['Vilma','Pedro','Pablo','Betty'];
//funciones de callback
array.forEach(saludar);


array.sort();

console.log(array);
console.log(array.find(elemento => elemento.includes('V')))

arrayNums = [123,3423,55,3,0];

let nuevoArray = arrayNums.map(numero =>
numero * 2 )

console.log(nuevoArray);

let acumulado = array.reduce((ac,el)=> ac +='-'+ el)

console.log(acumulado);
```



