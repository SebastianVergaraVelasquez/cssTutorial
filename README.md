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