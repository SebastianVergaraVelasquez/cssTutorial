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