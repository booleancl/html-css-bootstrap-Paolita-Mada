# HTML CSS BOOTSTRAP

htm css y javascript son los pilares de toda app o sitio web.
Cualquie cosa que funcione dentro de un navegador web(chrome,mozilla o safari) utiliza estos pilares. y no solo eso, hoy tambien se pueden hacer aplicaciones"nativas" con estas tecnologias.

## HTML

Significa ** Hyper test Markup Languaje**, que en castellano seria algo como lenguake de mercado de hyper texto. Lenguaje de marcado es por la*Etiquetas*. Dependiendo de su etiqueta el navegador lo procesa de diferente forma. Y el hyper texto se refiere a que estos documentos estan enlazados por *Links*.

Con HTML crearemos *documentos estructurados* que el navegador puede interpretar

El documento principal de un sitio o app se debe llamar **indexhtml**. Todo junto y con minusculas.

Esta primera etiqueta indica al navegador la version de HTML. En este caso indica que es la version 5.
```html
 <!DOCTYPE html>
 ```

 Luego de eso viene la primera etiqueta que es parte del documento. la famosa etiquera **html**
 ```<html lang="es">
  ...
  </html>
  ```

  Del ejemplo anterior vemos que esta etiquera se compone de 2 partes principales.La etiquera de apertura `<html>` y la de cierre `</html>`.

  Entremedio de las etiquetas de apertura y cierre ira el contenido.

  Ademas vemos la etiqueta de apertura tiene el **atributo** `lang="es"`, lo que le indica al navegador en que idiona esta el contenido del documento.

  >**ATENCION**: Solo las etiquetas de apertura pueden tener atributos,las etiquetas de cierre no.

  ## head

  A continuacion viene etiqueta `head`.
  Esta etiqueta entrega informacion al**Navegador** sobre como visualizar el contenido que vendra en las siguientes secciones. Por ejemplo se indica mediante etiquetas `meta`el set de caracteres que tutilizara la pagina.
  Ejemplo:
  ```html
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hola Microsystem</title>
</head>
```
La tercera etiqueta `meta` que tiene el atributo `name="viewport"` permite que el contenido se cargue inicialmente considerando el tamaño de pantalla disponible, desde grandes a muy pequeños.

Ademas dentro del head se encuentra la etiqueta `title`, que es la encargada de mostrar el nombre del sitio en la pestaña del navegador.

Por otra parte dentro del `head` podemos cargar otros recursos que utilizara el documento como por ejemplo hojas de estilo CSS o archivos Javascript

### Estructuras Jerarquica

Algo que es muy importante notar y que no es tan evidente, es que los documentos HTML forman una estructura jerarquica bien definida del tipo arbol.
Donde la etiqueta raiz es la estiqueta `html`. Lo podemos visualizar de la siguente forma

```html
  <html>
    <head></head>
    <body></body>
  <html> 
```

Esto es muy importante de comprender ya que luego manejaremos las etiquetas pensando en su ubicacion relativa dentro del arbol. y pensaremos que las etiquetas son **nodos** que tienen **nodos padre**, **hermanos** y **nodos hijos**.

## Etiquetas principales

### Titulos

Las etiquetas para hacer titulos son las etiquetas **h** con numeros del 1 al 6. Ejemplos

```html
 <h1>Super titulo</h1>
 <h2>Super sub titulo</h2>
 <h3>Super sub sub titulo</h3>
 <h4>...</h4>
 <h5>...</h5>
 <h6>...</h6>
```
### links

Los links son el corazon de internet y los crearemos frecuentemente.Se componen de el atributo `href` que indica el destino del link y su contenido, que es lo que se muestra al usuario.

```html
 <a href="heading.html">Titulo</a>
```

### Imagenes

Las imagenes son una de las etiquetas que no requiere de cierre ya que la imagen que se despliega se indica mediante el atributo `src` y en caso de que la imagen no este disponible se despliega el texto indicado en el atributo `alt` conocido como texto alternativo.

### Listas

#### Ordenadas

```html
<ol>
        <li>Lunes</li>
        <li>Martes</li>
        <li>Miercoles</li>
        <li>Jueves</li>
        <li>Viernes</li>
    </ol>
```
### No ordenadas
```html
 <ul>Pilares de la web
        <li>HTML</li>
        <li>CSS</li>
        <li>Javascript</li>
    </ul>
    ```
    ### Tablas

    <table>
        <tr>
            <th>Italiano</th>
            <th>Chacarero</th>
        <tr>
        <tr>   
                <td>Tomate</td>
                <td>Lechuga</td>
        <tr>
        <tr>        
                <td>Palta</td>
                <td>Potoros</td>
        <tr>
        <tr>        
                <td>Mayo</td>
                <td>Aji</td>
        </tr>

### Etiquetas no semanticas
Estas etiquetas no tiene un significado propio y sirven como contenedor para agrupar otras etiquetas
## div
```html
<div>
  <p>Hola mundo</p>
</div>
```
## spam
La etiqueta span se puede usar dentro de un texto.
```html
<div>
  <p>Hola<span>mundo</span></p>
</div>
```
La idea detras de los elementos no sematicos es utilizar css para darles estilo.
Mas adelante, en este modulo veremos lo frecuente de su uso el marco de trabajo o framework bootstrap.

## Formularios
Contiene controles interectactivos para ingresar informacion

```html
<form action="/search" nethod="get">...

</form>
```

Cuando enviamos el formulario mediante el metodo get, los parametros ingresados quedan reflejados en la uri despues del signo 7 y separados por `&`.

## CSS

Hojas de estilo en cascada( Cascade Style Sheets) Css nos permite entregar al sitio el aspecto que queremos. Lo hace aplicando reglas de estilo sobre diferentes elementos del HTML.

Los navegadores tienen estilos predefiridos para mostrar las diferentes etiquetas.

Cuando el codigo CSS esta definido dentro del mismo archivo html,se denomina css-inline, pero no es la mejor forma de definir los estilos que se van a utilizar en varias paginas. para eso es mejor utilizar un archivo externo y vincularlo al html.

## sintaxis CSS
las reglas CSS parten con un selector,luego dentro de las llaves se ingresan las propiedades junto con su valor.
Ejemplo:

```css
h2{
  color: blue;
  font-size: 24px;
}
selector{  
  propiedad: valor;
  propiedad: valor;
}
p{
  color:red;
  text-aling: center;
}
```
### Selectores

en el ejemplo anterior el selector era la misma etiqueta, es decir, la regla de estilo aplica a **todos** las etiquetas de ese tipo, tenemos otros 2 selectores muy fecuentes.el selector por "id" y por "clase"

el id es un atributo de las etiquetas HTML. toda etiqueta puede tener el atributo "id" para diferenciar del resto. y podemos usar ese atributo como selector css usando la notacion "#"

ejemplo de selector por id
```css
#fname{
  border-radius: 6px;
}
```
CSS es muy flexibles y permite combinar selectores. Ej:

```css
/* Esta regla aplica a los parrafos con clase centered*/
p.centered {
  text-aling: center;
  color: purple;
}
```

Si tenemos reglas que se repiten. Ejemplo

```css

h1{
  text-align: center;
  color: blue
}

h2 {
  text-align: center;
  color: blue
}
```

Podemos refactorizarlo en una sola regla:

```css
h1, h2{
  text-align: center;
  color: blue
}
```
Selector | Ejemplo | Descripcion
---- | ---- | ----
#id | #some-id | Selecciona TODOS los elementos con `id="some-id"`
.class | .some-class | Selecciona TODOS los elementos con clase `class="some-class"`
element.class | p.intro Selecciona solo los `<p>` con clase `class="intro"`
element. element | div, p | Selcciona todos los elementos `<div>` y `<p>`

### Modelo de caja

En esencia cada elemento html esta inserto dentro de una caja que consiste de: Margen, Borde, Padding y contenido.

### Unidades de medida

En general, no solo en desarrollo, podemos clasificar las unidades de medida en dos grupos:

- Unidades Absolutas:Pixel(px)
- Unidades Relativas: Porcertaje%, rem , em, vh , vw

### rem 
Es una unidad de medida relativa al font-size del elemento raiz

### em
Es relativa al font-size del mismo elemento
### vh
Es relativo al 1% del alto de la pantalla (viewport)
### vw
Es relativo al 1% del ancho de la pantalla o viewport

### Tipos de diseños

- El diseño estatico: Sirve para un solo tamaño de pantalla
- El diseño fluido: Se basa en porcentanjes(%) dependiendo del tamaño de la pantalla.
- Diseño responsivo: Tiene puntos de quiebre (distintos tamaños)para aplicar diferentes estilos

### CSS MediaQueries

Utiliza la regla `@media` para incluir un bloque de propiedades CSS solo si la condicion es verdadera.Ejemplo:

```css
@media only screen and (max-width: 600px){body{
  background-color: green
  { 
}
```
Existen ciertos tamaños de pantalla mas o menos estandarizados y estas serian sus respectivas media queries:

```css
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...}
```
### Display

```css
/*si el tamaño de la pantalla es de 600px o menor, el color de fondo del body sera verde*/ 
@media only screen and (max-width: 600px){
  body {
    background-color: green
  }

  p{
    display: none
  }
}
```

el valor de la propiedad display modifica como el navegador posicionara la caja del elemento.

la caja puede ser de lado a lado, en en ese caso la propiedad display tendra el valor "block".
Tambien podemos establecer el valor como `inline` y en ese caso, la caja sera del menor tamaño posible. ejemplo:

.side-to-side{
  display:block;
  margin: solid
}
.narrow{
  display: inline;
  margin: solid
}

