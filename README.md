# CSS.__GB__
# stilo basico

```css
  *,*::before,*::after{
    margin:0;
    padding:0;
    box-sizing: border-box;
  }
  body{
    background-color: var(--background);
}
 ```
 # root basico
 ```css
 :root{
  --black:#0000
  --grey:somebody;
  --backgound:algunbackground
  etcetc
 }
 ```
## ligando el html al css
```http
  <link rel="stylesheet" href="../css/styles.css">
 ```
 ## Selectores simples
 ### selectores elementales
 selector universsal
 ```http
  *{}
 ```
 selectores de tipo o etiqueta
 ```http
  nombre de la etiqueta html
  h1{}
 ```
 ### selectores de atributos
 id(no es recomendable dar estilos con id)
 ```http
  #nombredelaid{}
 ```
 class (recomendable cuando se le quiere dar estilos a diferente grupos
 ```http
  .nombredelaclass{}
 ```
 otros
 ```css
  [nombredelatributo]{propiedad:valor;}
  [nombredelatributo+valorUrl]{propiedad:valor;}
  [nombredelatributo+^palabraquecoomienzalaUrl]{propiedad:valor;}
  [nombredelatributo+*algunapalabradelaUrl]{propiedad:valor;}
  [nombredelatributo+$palabraqueterminalaUrl]{propiedad:valor;}
  [nombredelatributo+|idioma]{propiedad:valor;}
 ```
 ## Selectores compuestos
 
 ### selectores agrupados
 ```bash
  .class,.class2,.class3.etc4{propiedad:valor;}
 ```
 ### selectores combinados
 desendientes
 ```bash
  div .class{propiedad:valor;}
 ```
 selector de hermano siguiente
 ```bash
  .class + tag{prop:value;}
 ```
 selector de hermanos siguientes
 seleccionas todos los hermanos que coincidan con la selecion
 ```bash
  .class ~ tag{prop:value;}
 ```
 ### pseudoclases-pseudoelementos
 
 ```http
  null
 ```
 ## Espacificidadb (cascada y herencia)
 -Etiquetas y pseudoelementos 001
 -clases, atributos y pseudoclases 010
 -Ids 100
 -Estilos en linea 1000
 -!important GANA A TODO y no se usa nunca
 
 ### Herencia 
 inherit fuerza la herencia de los link o lo que se te ocurra
 ```bash
  .Link{color:inherit;}
 ```
 initial fuerza a que el elemento no herede
 ```bash
  .class{color:initial;}
 ```
 ### Herramientas en inspeccionar/styles o computed se ve bien
 # color
 ## backgroun color
 ### background linear-gradient 
 ```bash
  background: linear-gradient(to right top,color,color)
 
 ```
 # Box model
 ## Taman:o
 ```http
  width:0px
  height:0px
 ```
 padding nos separa el contenido del borde y margin nos separa la caja de otras cajas
  ```http
  los elementos de lina tienen disponibles los margenes horizontales
  margin: right/left
  los de bloque todos
  margin: top/right/botton/left
  margin-left:auto a la izquierda
  margin-right:auto a la derecha 
  juntos de centran?
 ```
 ## centrar
 ```http
  margin-left:auto a la izquierda
  margin-right:auto a la derecha 
 ```
 para centrar elementos de linea usar display:block / text-aling:center
 las imgagenes vienen en inli-block para centrarlas tenemos que usar display:block / margin-left:auto;margin-right:auto
 ## border
 border modifica el taman:o de la caja
 ```http
   border-width: ancho del border
   border-style: style del border
   border-color: color del border
   border: 1px solid red
   border-right-color:blue
   border-style:none
   border-style:hidden
   border-style:dotted
   border-style: dashed
   border-style:double
   border-style:groove //3d
   border-style:ridge  //3d
   border-style: ridge //3d
   boeder-style:inset //3d
   boeder-style:outset //3d
 ```
 ## border outline
no modifica el taman:o de la caja
 ```http
  outline: 10px solid red //esto lo que hace es nos crea un border menos invacivo que el clasic
 ```
 outline-offset podemos jugar un poco con la posicion del border
 ```http
  outline-offset: -10px 
 ```
 ## box-sizing // sizing de la caja
 ```http
  box-sizing:border-box; //calcula la cantidad que tiene que restar para que el ancho quede igual
 ```
 ## border redondeados radius
 ```http
  border-radius:50px //esto dibuja 4 circulos 
  border-top-right-radius:50px
  border-top-left-radius:50px
  border-bottom-right-radius:50px
  border-botton-left-radius:50px
  border-radius: 50px 100px 150px 200px
  border-radius: 50px/50px //elipse
 ```
 ## desbordamientos
 ### overflow
 ```http
  overflow-y:auto;
  overflow-y:scroll;
  overflow-y:hidden // oculta el contenido que se desborda de las cajas de adentro
 ```
 ## colapsado de margenes
 los margenes verticales colapsan // para esto no hay solucion solo queda darle 
 
 ## Display
 hace que el elemento no se muestre pero sigue cargandoce
 ```http
  display:none
 ```
 hace que el elemento sea de bloque
 ```http
  display:bloque
 ```
 hace que el elemento sea de linea 
 ```http
  display:inline
 ```
 hace que el elemento sea de linea pero admite medidas y margenes verticales
 ```http
  display:inline-block
 ```
 ## text aling alinear texto
 podemos alinear el contenido siempre que no tenga valores puestos
 ```http
  text-aling:right; //centra al al derecha
  text-aling:left; //isquierda
  text-aling:center; //centro
  text-aling:justify //tratar de evitar portque centra raro
 ```
 # BOX SHADOW
  ```http
  box-shadow: inset(para dibujar la sombra por dentro) 5px 5px 10px(desenfoque) ,(agrega otra caja) 10px 10px blue
 ```
 # Posicionamiento (position)
 position tambien les da a los elementos de linaea la capacidad de botton top width right
 relative si lo movemos lo hara usando si posicion en el html como punto de referencia y el espacio que ocupaba sigue siendo su referencia
 ```http
  position:relative
 ```
 position absolute = el elemento usa el contenedor como referencia si no lo tiene usara el elemento html de referencia
 ```http
  position:absolute
  
 ```
 fixed pierde su espacio reservado y sus medidas se quedara fijo en esa posicion auque agamos scroll siempre toma como punto de ref el html
 hay un truco interezante que me gustaria probar con esto
 ```http
  position:fixed
 ```
 position sticky este se comporta de una manera interezante cuando le agregamos top:0; la propiedad overflow no tiene que estar declarada
 
```http
  position:sticky
 ```
 z-index modifica su contecto de apilamiento es decir le dice al browser que caja va arrida de otra
 ```http
  z-index:1
 ```
 el orden del stacking context es :  (de delante a atras)
 elementos posicionados con un z-index de 1 a mas
 elementos sin z-index declarados
 elementos no posicionados
 elementos con index negativos
 
 # Ordenar las propiedades es importante 
 ```http
  1 propiedades de posicionamiento
  2 propiedados de box model
  3 propiedades de texto
  4 propiedades visuales
  5 el resto
 
 ```
 `body {
 ------POSITION----------
      position:relative;
      top:0;
      left:0;
 ------BOX MODEL -------
      display:block;
      width:300px;
      height:300px;
      padding:10px
      margin:10px;
      overflow:hidden;
 -----PROPIEDADES DE TEXTO---
      font-size:16px;
      text-aling:center;
 -----VISUALES-------
      color:blue;
      border:2px solid red
      border-radius:50px
 -----EL RESTO-----
      opacity:1;
      
 }`
 
 ## Medidas em y rem
 rem corresponde a la medida de la raiz del documento(el estandar del tamanio de la fuente en la raiz del documento es 16px)
 em corresponde al contexto endonde nos encontramos(tanto rem como em se calcula en base a la propiedad font-size)
 
 # Viewport width hace referencia al ancho de viewport (anco de la pantalla cualquiera)
 ```http
  height:100vh
  width:100hv;
 ```
 vmax no los entendi
 vmin no los entendi
 
# Hacer un triangulo en css
```http
  border-top:500px solid red
  border-left:250px solid transparent
  border-right:250px solid transparent
 ```
 
 #
