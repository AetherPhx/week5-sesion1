# Conceptos Importantes CSS

## Selectores
Los selectores existen de diversos tipos.
### Etiqueta.
    <tag>
### Clase
    .class
### ID
    #id
### Inline
    <tag style="color: red;">
    <!-- ! Esta se aplica en el html usando el atributo style. -->

## Herencia
Los valores de las propiedades de un selector pueden heredarse a sus descendientes.
En el caso de que no se haga y se desee tomar algún valor del selector contenedor/padre, se puede usar el valor 'inherit'.
### Ejemplo:
    ```html
    <p class="padre">
        <span class="hijo"></span>
    </p>
```
    ```css
    .padre{ color: red; }
    .hijo{ color: inherit;}
    }
```
La propiedad 'color' de 'hijo' tendrá el valor heredado de la propiedad 'color' de 'padre' gracias al valor 'inherit'.


## Cascada
Los estilos se aplicarán dependiendo de qué tan abajo del .css se encuentren.
### Ejemplo:
    ```css
        p{ color: red; }
        p{ color: blue; }
    ```
    <!--! Se aplicará el color blue porque es el último en el .css -->

## Especificidad
Los selectores cuentan con un valor que determina qué es más importante y por lo tanto, cuál se aplicará en el caso de haber conflicto.
### Tabla de Especificidad
    Etiqueta     1
    Clase        10
    ID           100
    Inline       1000
    !important   Infinito

### Ejemplo
    ```css
        .parrafo{ color: red; }
        p{ color: blue; }
    ```
    <!--! Se aplicará el color red porque las clases tienen mayor especificidad. -->

## Familias Tipográficas
Se pueden aplicar de diferentes formas fuentes de texto.
Por ejemplo, en google fonts (https://fonts.google.com) puedes encontrar fuentes de texto gratuitas que permiten usarlas en tu proyecto mediante 3 métodos:
### link
    ```html
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap" rel="stylesheet">
    ```

### @import
    ```css
    @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
    ```

### Download
Se descarga y carga la fuente directamente al proyecto.
De esta forma no es necesario el link o @import y no habrá la posibilidad que no se use la fuente porque se rompa el link.

## Tamaño de Fuentes
Existen muchas unidades para establecer el tamaño de la fuente, pero al final siempre se usará y mostrará en píxeles(px).
### px
Los pixeles que medirá y se mostarán en la pantalla del dispositivo.
### em
Esta medida es en base a la medida del elemento padre. (1em = 16px)
### rem
Esta medida es en base a la medida del elemento raiz. (1rem = 16px)
### vw(Viewport Width) y vh(Viewport Height)
Estas medidas son en base a la dimensión correspondiente de la pantalla del dispositivo.
(1vw = 1% del ancho de la pantalla)
(1vh = 1% del alto de la pantalla)

## Propiedades de Fuente o Texto
### text-transform
Permite convertir el texto según el valor/formato escogido.
capitalize: Todos los caracteres en mayúscula
uppercase: Primera letra mayúscula
lowercase: Todo minúsucula
### text-align
Permite alinear el texto en el elemento.
left: Izquierda <!--Por defecto>
right: Derecha
center: Centrado
justify: Justificado
### font-weight
Define el grosor de la fuente mediante palabras clave o valores.
<!--! Los valores son dependiente de los que tenga disponible la fuente en la que se usan -->
light: ligero
normal: normal
bold: negrita
### text-decoration
Define la decoración del texto.
none: Ninguna
underline: Subrayado
overline: Sobrrelleno
line-through: Tachado
### font-style
Define el estilo de la fuente.
normal: normal
italic: cursiva