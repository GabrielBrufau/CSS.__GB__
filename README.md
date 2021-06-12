# CSS.__GB__
# nivel basico
(w3.org)

```http
  
 ```
## ligando el html al css
```http
  <link rel="stylesheet" href="../css/styles.css">
 ```
 ## Selectores simples
 ### selectores elementales
 selector universsal
 ```http
  *{propiedad:valor;}
 ```
 selectores de tipo o etiqueta
 ```http
  nombre de la etiqueta html
  h1{propiedad:valor;}
 ```
 ### selectores de atributos
 id(no es recomendable dar estilos con id)
 ```http
  #nombredelaid{propiedad:valor;}
 ```
 class (recomendable cuando se le quiere dar estilos a diferente grupos
 ```http
  .nombredelaclass{propiedad:valor;}
 ```
 otros
 ```http
  [nombredelatributo]{propiedad:valor;}
  [nombredelatributo+valorUrl]{propiedad:valor;}
  [nombredelatributo+^palabraquecoomienzalaUrl]{propiedad:valor;}
  [nombredelatributo+*algunapalabradelaUrl]{propiedad:valor;}
  [nombredelatributo+$palabraqueterminalaUrl]{propiedad:valor;}
  [nombredelatributo+|idioma]{propiedad:valor;}
 ```
 ## Selectores compuestos
 
 ### selectores agrupados
 ```http
  .class,.class2,.class3.etc4{propiedad:valor;}
 ```
 ### selectores combinados
 desendientes
 ```http
  div .class{propiedad:valor;}
 ```
 selector de hermano siguiente
 ```http
  .class + tag{prop:value;}
 ```
 selector de hermanos siguientes
 seleccionas todos los hermanos que coincidan con la selecion
 ```http
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
 ```http
  .Link{color:inherit;}
 ```
 initial fuerza a que el elemento no herede
 ```http
  .class{color:initial;}
 ```
 ### Herramientas en inspeccionar/styles o computed se ve bien
 # Box model
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
 
 
 

 
