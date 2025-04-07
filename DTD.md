<!-- 
Nombre: Sergio Morales
Curso: ASIR1
Fecha: 06/04/2025
Ejercicio: XML DTD3
-->

<!ELEMENT cuento (personajes, trama, etiqueta*, precio?)>
<!ATTLIST cuento 
    cod CDATA #REQUIRED
    titulo CDATA #REQUIRED
    genero CDATA #IMPLIED
>

<!ELEMENT personajes (personaje+)>

<!ELEMENT personaje (nombre, genero, descripcion?, descripcion_fisica | imagen | url)>
<!ATTLIST personaje 
    id ID #REQUIRED
    tipo CDATA "principal"
>

<!ELEMENT nombre (#PCDATA)>
<!ELEMENT genero (#PCDATA)>
<!ELEMENT descripcion (#PCDATA)>
<!ELEMENT descripcion_fisica (#PCDATA)>
<!ELEMENT imagen (#PCDATA)>
<!ELEMENT url (#PCDATA)>

<!ELEMENT trama (#PCDATA)>

<!ELEMENT etiqueta EMPTY>
<!ATTLIST etiqueta 
    nombre CDATA #REQUIRED
>

<!ELEMENT precio (#PCDATA)>
<!ATTLIST precio 
    moneda CDATA "euro"
>
