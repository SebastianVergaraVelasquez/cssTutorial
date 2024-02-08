*Selectores CSS*

- Universal: *{}
- De tipo: Ejemplo: h1{}
- Clase: class="nombre-clase": .nombre-clase{}
- ID: id="id-nombre": #id-nombre{}
- Propiedad: ejemplo: active = True ; [active = True]{}
- Descendente: <h2><p></p></h2> ; h2 p {}
- Pseudoclase: .clase-cualquiera p:hover{}   (hover -> cuando el cursor esté sobre el elemento)

*Especificidad*

Jerarquía

important  ejemplo: color:grey !important
estilos en linea style=" color:grey"
identificadores
clases (estos 3 misma jerarquía)
pseudoclases
atributos
elemementos    (estos dos misma jerarquía)
pseudoelementos

*Modelado en cajas*

Elementos en bloque y en linea
-a los elementos en bloque se les puede dar width y height, a los que están en línea no. Display permite transformar el valor por defecto del elemento

*propiedades*

overflow: si un elemento supera las dimensiones de su contenedor, dependiendo del valor que se le de a overflow opera de manera distinta sobre el contenido sobrante.

    overflow: auto  genera barras de scroll en el eje donde el contenido sobresalga del contenedor
    overflow: scroll genera barras de scroll en ambos ejes
    overflow: hidden oculta el contenido que salga del contenedor
    overflow-y / overflow-x se pueden manejar los tres valores de overflow en cada eje por separado

float: El mejor uso que se puede dar es para que en un contenedor con texto y una imagen, al darle float a la imagen pareciera que el texto rodeara a la imagen.

object-fit: Acomoda la imagen dentro de un contenedor
    none: da la imagen del tamaño original
    cover: ajusta la imagen al contenedor
    contain: ajusta el contenedor al tamaño de la imagen

object-position: permite desplazar la imagen cierta medida respecto a cada eje

cursor: permite seleccionar el tipo de cursor al ubicarse sobre el elemento

*grid*

grid-template-columns
grid-template-rows

grid-template-columns: 100px repeat(4, 50px) 200px;
grid-template-rows: repeat(2, 1fr 2fr);

-minmax

Si establecemos un rango, por ejemplo, grid-template-column: minmax(200px, 500px), estaremos indicando que la celda de columna indicada, tendrá un tamaño de 500px, salvo que redimensionemos la ventana del navegador y la hagamos más pequeña, en cuyo caso, el tamaño de la celda podría ir disminuyendo hasta 200px, medida en la cuál se quedaría como mínimo.

-gap

Para especificar los huecos (espacio entre celdas) podemos utilizar las propiedades column-gap y/o row-gap. En ellas indicaremos el tamaño de dichos huecos:

grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));

justify-items	start | end | center | stretch	
align-items	start | end | center | stretch	
justify-content	start | end | center | stretch | space-around | space-between | space-evenly	
align-content	start | end | center | stretch | space-around | space-between | space-evenly

.container {
  display: grid;
  grid-template-areas: "head head"
                       "menu main"
                       "foot foot";

  grid-template-columns: 1fr 1fr;
  grid-template-rows: 100px 200px 100px;
}

grid-auto-flow: Define cómo se distribuyen los elementos que no tienen una ubicación especificada dentro del grid.

grid-auto-flow: row;: Coloca los elementos automáticamente en filas.
grid-auto-flow: column;: Coloca los elementos automáticamente en columnas.
grid-template-areas: Permite especificar áreas con nombres y asignar elementos a esas áreas.

grid-column-gap y grid-row-gap: Define el espacio entre las columnas y filas del grid, respectivamente.
Ejemplo: grid-column-gap: 20px; grid-row-gap: 10px;
grid-template: Es una abreviatura que combina grid-template-rows, grid-template-columns, y grid-template-areas en una sola declaración.
Ejemplo: grid-template: auto / 1fr 2fr;
grid-column-start, grid-column-end, grid-row-start, grid-row-end: Establecen el inicio y el fin de las líneas de grid en las que un elemento debe comenzar y terminar su posición.
Ejemplo: grid-column-start: 2; grid-column-end: 4;
grid-area: Es una abreviatura para especificar la ubicación del elemento dentro del grid.
Ejemplo: grid-area: 2 / 2 / 3 / 4;

transition: all 1s ease;

transition-property: Especifica qué propiedad o propiedades CSS deben ser animadas. Puedes definir múltiples propiedades separadas por comas.

Ejemplo: transition-property: width, height, color;
transition-duration: Define la duración de la transición en segundos o milisegundos.

Ejemplo: transition-duration: 0.5s;
transition-timing-function: Especifica cómo la transición debería cambiar con el tiempo. Hay varios valores predefinidos, como ease, linear, ease-in, ease-out, ease-in-out, entre otros.

Ejemplo: transition-timing-function: ease-in-out;
transition-delay: Indica un retraso antes de que comience la transición.

Ejemplo: transition-delay: 0.2s;

box-shadow: offset-x offset-y blur-radius spread-radius color;
4px 6px -2px rgba(0, 0, 0, 0.5)

<progress value="50" max="100">