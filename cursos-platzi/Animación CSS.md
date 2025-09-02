# Animación CSS

- **Principios de Animación CSS: Keyframes y Animation en Acción**
    
    ### ¿Qué es una animación? 🎭
    
    Una animación podría ser descrita como un **conjunto de fotogramas que cuenten con un estado inicial y final**, compuesto de distintos puntos medios que conforman la misma. Además, desde pequeños nuestros ojos 👀 han sido entrenados de forma involuntario al momento de ver las caricaturas a través del televisor.
    
    ### Principios de animación para la web 💻
    
    Actualmente, en el desarrollo web, podemos contar con diversas animaciones realizadas en su mayoría con CSS. Para ello, **existen principios a seguir, que se crearon con el fin de optimizar y aprovechar al máximo esta función**. Estos principios describen cómo se puede utilizar la animación para sumergir a los espectadores en un mundo creíble 👓. Un dato interesante, es que dichos principios fueron utilizados como metodología de trabajo para las animaciones que Disney diseñaba en aquellos tiempos.
    
    **Entre ellos tenemos** (estarán mencionados en su lengua original):
    
    - Squash and stretch
    - Anticipation
    - Staging
    - Straight-Ahead Action and Pose-to-Pose
    - Follow Through and Overlapping Action
    - Slow In and Slow Out
    - Arc
    - Secondary Action
    - Timing
    - Exaggeration
    - Solid drawing
    - Appeal
    
    Páginas
    
    https://static.platzi.com/media/public/uploads/12_principles_of_animation_14a18c8a-cc2c-492d-af3b-fae713c4fda6.gif
    
- **Maquetación de Juegos con CSS y Animaciones Interactivas**
    
    En esta clase, se presentará el reto a realizar.
    
    **El juego consiste en seleccionar la mayor cantidad de conejos**
    
    que puedas para acumular puntos en el contador que se encuentra en la parte superior.
    
    ![Resultado final del juego](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-05%20at%206.45.02%20PM%20%281%29.jpeg)
    
    Aprenderemos no solo a maquetar, sino a darle las animaciones correspondientes junto con su funcionalidad solo con CSS.
    
    ---
    
    ### Maquetación I - Realizando el contador 🎲
    
    Para ello, empezaremos con nuestro editor de código favorito, en este caso utilizaré Visual Studio Code, Colocaremos la estructura básica en un archivo llamado **contador.html**, en la etiqueta **\\** colocaremos una lista desordenada y dentro por cada elemento de lista, colocaremos un input de tipo checkbox y un div, así como veremos a continuación 👀.
    
    ![Estructura al realizar el contador](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-05%20at%208.46.25%20PM%20%281%29.jpeg)
    
    Y dentro del mismo archivo dentro de las etiquetas **\\**, abriremos las etiquetas **\**. Una vez realizado los pasos, haremos una pausa ⏳ para explicar el funcionamiento de usar **Counter en CSS**.
    
    ### Counter en CSS 🧮
    
    Los contadores de CSS, **nos permite numerar automáticamente la apariencia de un contenido**, cuyo valor puede tanto disminuir como aumentar, como una variable, mediante reglas CSS que capturan cuántas veces se usa.
    
    Entre sus propiedades tenemos:
    
    - **counter-reset:** Crea o reinicia un contador.
    - **counter-increment:** Incrementa un valor del contador.
    - **content:** Inserta el contenido generado (debe usarse con un pseudoelemento).
    - **counter()**: Función que agrega el valor de un contador a un elemento.
    
    Una vez explicado ello, dentro de la etiqueta **\**, colocaremos el siguiente código.
    
    ![Utilizando la propiedad count](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-05%20at%208.50.53%20PM%20%281%29.jpeg)
    
    Explicando cada una de las líneas, dentro de body creamos un contador con la propiedad **counter-reset** con el valor de **game**, posteriormente dentro del input cuando esté activo ✅, colocaremos la propiedad **counter-increment** indicando como valor **game**, dado que ese contador será el que se incrementará ➕. Por último, llamamos a la clase **.total-count::after** creando un contenido e indicando como propuedad a **counter(game)** ya que esto indica dónde se mostrará el indicador cada que un checkbox esté activo ✅.
    
    Una vez realices los pasos mencionados, obtendrás el siguiente resultado:
    
    ![Resultado de usar un contador en CSS](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-05%20at%208.59.40%20PM%20%281%29.jpeg)
    
    :::(Info) (Remember:) Cada que selecciones un checkbox , el contador aumentará en uno. En este caso, dado que se encuentran activos solo 3 casilleros, el contador es igual a 3️⃣. :::
    
- **Capas y posicionamiento en CSS: Uso del Z-Index en maquetación web**
    
    n este artículo, veremos en primer lugar, la definición de apilamiento, ya que esta herramienta nos será de utilidad para seguir con el juego.
    
    ## **¿Qué es el apilamiento? 🧱**
    
    El apilamiento es entendido como la **sobreposición de varios elementos** formando una pila. Tenemos varias definiciones de cada diferente rama como en la construcción, redes, entre otros.
    
    ### Contexto de apilamiento en CSS 🍰
    
    El contexto de apilamiento es la **conceptualización tridimensional de los elementos HTML a lo largo de un eje-Z** imaginario relativo al usuario en la página web. Los elementos HTML ocupan este espacio por orden de prioridad basado en sus atributos. Es decir, vendría a ser un apilamiento de forma horizontal con dirección a nosotros.
    
    ![Contexto de apilamiento](https://static.platzi.com/media/articlases/Images/colorful-g5a3b4b3e5_640%20%281%29.jpg)
    
    Una vez dicho ello, seguiremos en la creación de nuestro juego. Si analizamos la vista de cómo quedaría nuestro juego, tendríamos que identificar la cantidad de capas con las que contamos de acuerdo a su orden de apilamiento. Si visualizamos la siguiente imagen, visto desde otra perspectiva, podremos entender mejor el funcionamiento del contexto de apilamiento.
    
    ![Ejemplo de contexto de apilamiento en nuestro juego](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%2011.47.51%20AM%20%281%29.jpeg)
    
    ### ¿Y para qué nos sirve? 🤔
    
    Es una buena pregunta, pero no te dejes engañar ya que a pesar de ser un concepto sencillo, aporta con un valor enorme a nuestro juego. Además, como observamos, nos brinda una **sensación de profundidad** dándole un toque mágico de realismo a nuestra página. A diferencia de usar un fondo estático y no tengamos dónde esconder a nuestros conejitos 🐰, conocer y usar este tipo de estrategias nos ayuda a construir una página más completa y destacada ✨.
    
    ---
    
    ## **Poniendo en práctica lo aprendido 🐱‍🏍**
    
    Una vez tengamos claro el concepto, crearemos un archivo html y colocaremos la estructura básica como ya sabemos. En la etiqueta **<body>**, crearemos un contenedor div de clase **phone**, y dentro crearemos 10 contenedores div con las clases **layer** y **layer-(número de orden)**, si nos ayudamos de las abreviaciones emmet, solo colocamos esto dentro de nuestra etiqueta **<body>**, le damos a **ctrl + space** y al final cuando nos salgan opciones (por lo general una) solo le damos **enter**.
    
    ```
      .phone>(.layer.layer-$)*10
    
    ```
    
    Nos quedaría algo como esto:
    
    ![Resultado de colocar la abreviación Emmet](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%2012.23.45%20PM%20%281%29.jpeg)
    
    Luego de conseguir el siguiente resultado, nos dirigimos a nuestra etiqueta **<head>** y agregamos la etiqueta **<style>**, dentro colocaremos el siguiente código, que convertirá la posición del contenedor de clase **.phone** en absolute y la posición de los contenedores hijos de clase **.layer** en relative. Tendrás el resultado de cómo quedaría en su editor preferido 💻.
    
    ![Modificando la posición de los elementos](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%2012.46.09%20PM.jpeg)
    
    ---
    
    ### Maquetando la apariencia de teléfono 📱
    
    Luego de realizar todo lo mencionado, procederemos a agregar las siguientes propiedades dentro de la etiqueta **<style>**, modificando a **body** y el contenedor de clase **.phone**. Quedando como en la siguiente imagen, te explicaré lo que significa cada una de las propiedades más adelante 🤓.
    
    ![Resultado al maquetar la apariencia del télefono](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%2012.52.39%20PM%20%281%29.jpeg)
    
    Como podemos visualizar, hemos modificado a **body**, quitándole el margen que viene por defecto, definiendo un alto y ancho de toda la pantalla, y modificando su propiedad **display**, para poder colocar al centro todos los elementos hijos directos de body, en este caso al contenedor de clase **phone**, esto se logró con la propiedad que contiene grid que es **place-items** ingresando el valor de center 🎊.
    
    Siguiendo con la explicación, dentro del contenedor de clase **.phone**, hemos agregado un border de color negro y redondeado para dar la apariencia del contorno del teléfono 📱. Además, hemos definido un alto y ancho en píxeles, y por último un color de fondo de pantalla junto con una sombra.
    
    Si has seguido los pasos correctamente, obtendrás el siguiente resultado en el navegador ✅.
    
    ![Resultado en el navegador al maquetar el teléfono](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%2012.58.57%20PM%20%281%29.jpeg)
    
    ---
    
    ### Posicionando los elementos ⚙
    
    Una vez ya tengamos la apariencia del teléfono, lo que haremos será modificar uno por uno, los contenedores de clase **.layer**. Para ello, agregaremos cada uno de los contenedores de clase **.layer-(número de orden)** y agregaremos la propiedad **z-index** dándole como valor su número de orden, te debería quedar algo como esto 🧩.
    
    ![Resultado de colocar los z-index a los hijos](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%201.14.32%20PM.jpeg)
    
    :::(Info) (Aviso)
    
    Los escribí de esa forma para que puedas apreciar la estructura de cada uno y la captura no sea extensa, no hay problema si los escribes con su estructura normal.
    
    :::
    
    ---
    
    ### Modificando cada uno de los layers
    
    Empezaremos de forma ordenada por el **.layer-1** que vendría a ser un conejito 🐰, agregando un color, posición y tamaño. Con las propiedades **position**, **background**, **height**, entre otras. Así como podrás visualizar en la siguiente imagen 🎉.
    
    ![Modificando el layer-1 en CSS](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%201.21.44%20PM.jpeg)
    
    Si todo está correcto ✨, tendrías el siguiente resultado en el navegador.
    
    ![Resultado de modificar el layer-1](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%201.24.26%20PM%20%281%29.jpeg)
    
    En cuanto lo hayas conseguido, podremos pasar al **layer-2**, que sería el segundo conejito 🐰. También modificaremos su color, posición y tamaño ingresando casi las mismas propiedades que hicimos con el layer anterior.
    
    ![Modificando el layer-2 en CSS](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%201.28.29%20PM.jpeg)
    
    Si todo está correcto con el segundo layer ✨, tendrías el siguiente resultado en el navegador.
    
    ![Resultado de modificar el layer-2](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%201.29.38%20PM%20%281%29.jpeg)
    
    Poco a poco, todo va tomando forma, ahora pasaremos a modificar el contenedor de clase **layer-3**, que tendría a ser la plataforma 🎍 desde donde se esconden los dos primeros conejitos 🐰. Para ello, también definiremos tamaño, posición y colores. Ingresaremos las siguientes propiedades.
    
    ![Modificando el layer-3 en CSS](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%201.35.05%20PM.jpeg)
    
    Explicando lo que significan cada una de las propiedades, podremos verificar que cuenta con un alto y ancho gracias a las propiedades **height** y **width**, respectivamente. Además definimos un color con ayuda de **background** y como nuestra posición es absolute podemos ayudarnos de **bottom**, **left**, **right** y **top** para conseguir la posición deseada. Y así es como obtendremos el siguiente resultado en el navegador.
    
    ![Resultado de modificar el layer-3](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-06%20at%201.38.42%20PM%20%281%29%20%281%29.jpeg)
    
    **¡Felicidades!** 🎉
    
    Esto ha sido todo por este artículo. Si por alguna razón, no conseguiste realizarlo correctamente, no te desanimes. No todos lo logramos hacer a la primera. Recuerda que cualquier pregunta o duda puedes realizarla desde nuestra plataforma. Si has estado atento, te habrás dado cuenta que algunas propiedades son redundantes. Pero no te preocupes, lo solucionaremos en los próximos artículos 💎.
    
- **Dibujo de Conejitos con CSS: Estructura y Estilización**
    
    Para este artículo, ya debemos tener la siguiente vista lista. Una vez hayas llegado a esta vista, comenzamos con los conejitos 🐰.
    
    ![Foto del diseño avanzado.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%201.50.03%20PM%20%281%29.jpeg)
    
    ## **Empezando a maquetar nuestro primer conejito 🐇**
    
    Empezamos con el primer layer, con clase **layer-1**. Primero, cambiaremos el color de su fondo, por uno diferente a blanco ⬜, para que podamos visualizar los cambios que realizaremos con un mayor contraste. Y dentro de la etiqueta, colocaremos las siguientes etiquetas `\<div>` para las partes del cuerpo. Así como en la siguiente imagen.
    
    ![Maquetando nuestro primer conejo.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%202.08.37%20PM%20%281%29.jpeg)
    
    ### Estilando a nuestro primer conejito 🎈
    
    ### Estilando la oreja izquierda 🎊
    
    Dentro de nuestra etiqueta `\<style>`, colocaremos el estilo de las clases agregadas hace un momento. En este caso, usaremos las etiquetas `\<div>` con clases **left-ear--outer** y **left-ear--inner**. Ingresando las siguientes propiedades.
    
    ![Propiedades de CSS para la oreja izquierda.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%202.18.31%20PM.jpeg)
    
    Para **left-ear--outer**, le damos un fondo blanco, un border redondeado, un ancho y altura, le cambiamos su posición a **absolute** para poder indicarle la propiedad **left**.
    
    Si todo ha salido bien, conseguiremos el siguiente resultado ✨.
    
    ![Resultado de maquetar la oreja izquierda.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%202.19.34%20PM%20%281%29.jpeg)
    
    Una vez hayas conseguido lo mismo, te reto a hacer la oreja derecha por tu cuenta. De igual forma, podrás compararlo con nuestro resultado, pero intenta realizarlo por tu cuenta primero. ¡Confío en ti! 💚
    
    ### Estilando la oreja derecha 🎊
    
    Debajo de las clases dónde estilamos la oreja izquierda, colocamos el siguiente código, que sería muy parecido a excepción de algunos puntos. Como en lugar de la propiedad **left**, colocamos **right**.
    
    ![Propiedades para la oreja derecha.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%202.40.31%20PM.jpeg)
    
    Con las siguientes propiedades, conseguiremos formar la oreja derecha. Así tendríamos las dos orejas como se muestra a continuación 🎉.
    
    ![Resultado de maquetar la oreja derecha.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%202.41.51%20PM%20%281%29.jpeg)
    
    ### Estilando la cabeza 🐰
    
    En cuanto hayamos conseguido realizar las orejas satisfactoriamente. Lo que haremos, será estilar la etiqueta `\<div>` con clase **head**, con las siguiente propiedades. En donde la daremos un color de fondo, un borde redondeado, un ancho y alto, un margen para colocarlo al centro y las propiedades **left**, **right** y **top** con ayuda de la propiedades **position** con valor en **absolute**.
    
    ![Propiedades para la cabeza.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%202.46.57%20PM.jpeg)
    
    Con dichas propiedades, conseguiremos lo siguiente mostrado en el navegador 🎊.
    
    ![Resultado de maquetar la cabeza.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%206.44.15%20PM%20%281%29.jpeg)
    
    ### Estilando los ojos 👀
    
    Para los ojos, lo que haremos será modificar las etiquetas `\<div>` con las clases **head__eye**, **head__eye--left** y **head__eye--right**.
    
    Empezaremos modificando la clase **head__eye** 🎨. Colocaremos propiedades para definir el color de fondo, borde redondeado, un ancho y alto, y la posición en **absolute**.
    
    ![Maquetando código de los ojos.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%206.50.27%20PM.jpeg)
    
    Ahora, verás un solo punto dentro del conejo 🐰. Esto se debe a que tenemos dos ojos, pero uno está encima de otro, por eso tenemos el efecto de que solo hay uno. Así que nos faltaría modificar ahora las clases **head__eye--left** y **head__eye--right** para poder posicionar ambos ojos.
    
    ![Maquetando código de los ojos.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%206.54.55%20PM.jpeg)
    
    Con ello, estaríamos logrando visualizar correctamente ambos ojos de nuestro primer conejo, como lo muestra la siguiente imagen ✨.
    
    ![Resultado de modificar los ojos.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-20%20at%207.18.00%20PM%20%281%29.jpeg)
    
    ### Idea como realizar el efecto de zigzag 📍
    
    Si queremos lograr un efecto de zigzag para el fondo o los bloques, podemos guiarnos del siguiente link haciendo click [aquí](https://dev.to/cchana/explained-creating-a-zigzag-pattern-with-just-css-13g1){target="_blank"}.
    
    En dónde, el artículo nos explica cómo entender la lógica para el mismo, dividiendo desde pequeñas cuadrículas para que una vez unidas logremos el efecto.
    
- **Propiedades CSS para Animaciones y Keyframes**
    
    En este artículo, tratará sobre las animaciones 📍. Para trabajar con ellos, es necesario saber qué propiedades existen, y a partir de ello, saber con cuáles trabajaremos.
    
    En el siguiente enlace dando clic [aquí](https://static.platzi.com/media/public/uploads/animations_cheat_sheet_8394d34c-11b6-4150-ad63-cbad114e8f3a.pdf), veremos una visión general de las animaciones con CSS 🧩.
    
    Si bien no están todas, se encuentran las propiedades más recurrentes junto con su definición y sintaxis, increíble, ¿no? 👌
    
    ## **Propiedad animation-name 🤓**
    
    Animation puede tener solo un valor, o varios.
    
    Con estas propiedades, le colocamos un nombre a la fracción de código que queremos animar, para que el **keyframe** sepa a quién debemos animar. ¿Keyframes?, este extraño nombre tiene una función indispensable en la creación de animaciones, así que veremos una breve definición a continuación 🤯.
    
    ## **Keyframes 🎯**
    
    Básicamente el uso de la directiva **@keyframes** te permite definir el comportamiento de tu animación punto por punto, y cualquier elemento puede usar esta animación por medio de la regla animation-name.
    
    Dentro de @keyframes especificamos cada punto de nuestra animación por medio de porcentajes 💎. Podríamos tener un @keyframes de esta forma:
    
    ```
    @keyframes jump {
    
        /* Punto A */
        0% {
        }
    
        /* Punto B */
        40% {
        }
    
        /* Punto C */
        60% {
        }
    
        /* Punto D */
        90% {
        }
    
    }
    
    ```
    
    Los porcentajes pueden ser los que tú quieras, pero lo más importante a tener en cuenta es que mientras más cerca esté un porcentaje de otro más rápido será la transición de un punto a otro 😄.
    
    ## **¡Vamos al código! ✨**
    
    ### Principios para animar los ojos 👀
    
    Una vez nos encontremos dentro de nuestro editor, nos dirigiremos a la etiqueta **\style** y dentro de la clase **.head__eye**, ingresaremos la propiedad **animation-name** y la daremos como valor **blink**, así como en el siguiente ejemplo 👇.
    
    ![Ejemplo de propiedad animation-name](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-25%20at%208.48.39%20PM.jpeg)
    
    Una vez le hayamos dado dicha propiedad, procederemos a escribir el **@keyframe**, para empezar a modelar la animación que queremos con el conejito. Seguido del valor que le dimos a la propiedad **animation-name** hace un momento y sus llaves **{}**.
    
    Una vez dentro, escribiremos los porcetanjes, que significan en que tiempo de la animación queremos que surjan los cambios, también podemos colocar **from** o **to**, para indicar que se modifique ni bien inicio o finalice nuestra animación 🎊. Así como en el siguiente ejemplo:
    
    ![Resultado de agregar los keyframes](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-25%20at%208.55.56%20PM.jpeg)
    
    Hemos visto, como agregarle nombre a nuestras animaciones y saber como agregar keyframes. Nos vemos en el siguiente artículo para hablar de **Animation duration**.
    
- **Animaciones CSS: Control de Duración e Iteración**
    
    Felicidades por conseguir hacer parpadear los ojitos de nuestro conejito en el artículo anterior ✨. Además, hemos aprendido acerca de una propiedad que le asocia un nombre a nuestra animación. Ahora debemos conocer una propiedad que le indica la duración, para saber cuanto tiempo debe parpadear nuestro conejito o simplemente dejarlo en infinito ♾.
    
    ¿Y qué esperas?, acompáñanos en esta aventura 🐱‍🏍.
    
    ---
    
    ## **Propiedades para la duración de la animación ⌚**
    
    En este artículo veremos dos propiedades, las cuales su definición es la siguiente:
    
    ### Propiedad animation-duration ⌛
    
    Nos indica cuanto durará nuestra animación, solo recibe un valor que sería el tiempo, puede estar en segundos, milisegundos, etc. Los cuales serían: :::(Info) **animation-duration:** time | initial | inherit; :::
    
    ### Propiedad animation-iteration-count ⌛
    
    Nos indica cuantas veces se repetirá nuestra animación, también recibe solo un valor, y pueden ser los siguientes: :::(Info) animation-timing-function: linear | ease | ease-in | ease-out | ease-in-out | step-start | step-end | steps(int, start | end) | cubicbezier(n, n, n, n) | initial | inherit; :::
    
    ---
    
    ## **Vamos al código 💻**
    
    Dentro de la animación de nuestros ojitos, colocaremos ambas propiedades, la primera le indicará la duración que será de 2 segundos. Para la segunda propiedad, le daremos el valor de infinito para que nuestra animación se repita siempre. Así nos quedaría el siguiente fragmento dentro de la clase **head__eye**.
    
    ![Resultado de agregar las propiedades](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-27%20at%2010.45.52%20AM.jpeg)
    
    Una vez agregadas las dos propiedades, nos iremos a los keyframes para realizar los cambios que deseamos que contengan nuestra animación. En este caso, la propiedad que alteraremos de **head__eye** será **height** ya que haremos más pequeño el ojito para que de la impresión de que lo cierra 👀. Colocaremos que empiece su alto en 4px como ya lo estaba, luego cuando llegue al 5% de la animación su alto bajo a 1px y luego en el 10% de la animación este vuelvo a su tamaño normal. Y así nos quedaría el siguiente fragmento 👇.
    
    ![Resultado de modificar los keyframes](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-27%20at%2010.50.10%20AM.jpeg)
    
    Listo, una vez lo hayas modificado, nos dirigiremos a nuestro navegador a visualizar los cambios. Y quedaría así, colocaré los fotogramas de los porcentajes que modificamos:
    
    ![Conejito con los ojitos con altura en 4px](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-27%20at%2010.52.31%20AM%20%281%29.jpeg)
    
    Conejito con los ojitos con altura en 4px **en el 0% de la animación**
    
    ![Conejito con los ojitos con altura en 1px](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-27%20at%2010.52.31%20AM.jpeg)
    
    Conejito con los ojitos con altura en 1px **en el 5% de la animación**
    
    ![Conejito con los ojitos con altura en 4px](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-27%20at%2010.52.31%20AM%20%281%29.jpeg)
    
    Conejito con los ojitos con altura en 4px **en el 10% de la animación**
    
    ### Seamos detallistas 🎨
    
    Si lograron observar, podemos ver que el efecto funciona, pero al disminuir la altura, los ojitos suben en lugar de quedarse en el centro. Así que para solucionar ello de manera sencilla, le agregaremos la propiedad **transform** con el valor de **translate**.
    
    Cuando nos encontramos en el tiempo de la animación donde los ojitos disminuyen su tamaño (es decir en 5%), lo que haremos será agregar la propiedad para que pueda bajar 2px y permanecer en el medio 🎇.
    
    Pero si hacemos esto, cada que se repita la animación nuestros ojitos bajarán 2px de su posición actual y no queremos eso, ¿verdad? 🤨
    
    Para ello, agregaremos en el tiempo de la animación donde los ojitos regresan a su tamaño normal (es decir en 10%), que nuestros ojitos 👀 suban 2px, así su posición original no se verá afectada. Quedando nuestro código de la siguiente forma.
    
    ![Código donde se modifican los keyframes](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-04-27%20at%2011.00.54%20AM.jpeg)
    
- **Propiedades de Animación CSS: Timing Function y Delay**
    
    En este artículo, veremos dos propiedades muy importantes en el tema de la aceleración 🏃‍♀️. Las cuales son **animation timing function** y **animation delay**.
    
    ## **Propiedades 🎇**
    
    ### Animation timing function ⌚
    
    Básicamente es la aceleración con la cual correrá nuestra animación.
    
    ### Animation delay ⏰
    
    Es el tiempo que nuestra animación tardará en empezar.
    
    ### Animation Iteration Count 📒
    
    Es el número de veces que se repetirán nuestra animación.
    
    Una vez explicado esto, nos vamos al código para un mejor entendimiento.
    
    ## **Vamos al código 💻**
    
    Para empezar, y tener un contador cada que pulsemos a nuestro conejito, la agregaremos un input de tipo **checkbox**, de la siguiente manera.
    
    ![Agregamos input en el html](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-05-10%20at%203.10.15%20PM%20%281%29.jpeg)
    
    Dentro de nuestra etiqueta **style**, nos dirigiremos dentro del bloque donde se modifica la clase **layer-1**, e ingresaremos un nombre para la animación, una duración, el tipo de la velocidad y que sea en un bucle de manera infinita ♾, nos quedaría de la siguiente forma.
    
    ![Agregamos los valores para la animación](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-05-10%20at%203.27.23%20PM.jpeg)
    
    ### Seguimos con los Keyframes 🎯
    
    Una vez que nuestro **layer-1** tenga la propiedad **animation-name**, significa que ya le hemos dado un nombre para la animación, así que nos ayudaremos de ello para empezar con el keyframe. Así como la siguiente imagen. Además, agregamos la clase **.layer-1 input[type=checkbox]** para insertar estilos, pero lo dejaremos allí por un momento.
    
    ![Agregando los keyframes.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-06-12%20at%202.07.22%20PM%20%281%29.jpeg)
    
    Abrimos nuestro proyecto en el navegador, con ayuda de nuestro inspector vemos la posición de nuestro elemento **input** que hemos agregado 👇.
    
    ![Nuestro proyecto en el navegador).jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-06-12%20at%202.10.51%20PM%20%281%29.jpeg)
    
    Como podemos apreciar, nuestro **input** se posiciona de acuerdo a nuestro conejito 🐰.
    
    https://cubic-bezier.com/#.17,.67,.83,.67
    
- **Propiedades CSS para Animaciones: Dirección, Relleno y Estado de Reproducción**
    
    En esta clase, hablaremos de 3️⃣ propiedades que nos hacen falta para el tema de las animaciones que son:
    
    📍 Animation direction 📍 Animation fill mode 📍 Animation play state
    
    Las cuales veremos en un instante.
    
    ## **Propiedades 🎯**
    
    ### Animation Direction 🗽
    
    Dirección de la animación.
    
    - **Normal**: La animación se reproduce hacia delante en cada ciclo. Por defecto.
    - **Reverse**: La animación se reproduce hacia atrás en cada ciclo.
    - **Alternate**: La animación se invierte en cada ciclo, y la primera iteración se reproduce hacia adelante.
    - **Alternate-reverse**: La animación invierte la dirección en cada ciclo, y la primera iteración se reproduce hacia atrás.
    
    ### Animation Fill Mode 📢
    
    Estado de cierta animación. Al inicio o final.
    
    ### Animation Play State ⏯
    
    Define si la animación se reproduce o es pausada. (running or paused)
    
    Una vez tengamos aplicada estas últimas propiedades, tendríamos listo nuestro proyecto, el cual podrás verlo [aquí](https://static.platzi.com/media/public/uploads/animationland_f068b78d-e81c-4b6e-adeb-efb866eb630f.html){target="_blank"}.
    
    Hemos visto en este módulo, muchísimas propiadades para terminar nuestra animación. Falta muy poco para terminar 🎊.
    
    Solo nos faltaría un última detalle que sería el tema del **rendimiento**.
    
- **Optimización del Renderizado Web: Layout, Paint y Composite**
    
    En esta articlase, hablaremos de todo el trabajo de renderizado de la web. Que sería básicamente unos procesos, como lo vemos a continuación:
    
    🐱‍🏍 JavaScript 🐱‍🏍Style 🐱‍🏍 Layout 🐱‍🏍 Paint 🐱‍🏍 Composite
    
    El día de hoy, hablaremos de estas últimas tres, estos son los procesos que tienen que hacer algunas de nuestras propiedades para poder renderizarse en la web 💻. Sucede en cuestión de milisegundos.
    
    - **Composite**: Ordena las partes de la página. Propiedades como opacity y transform.
    - **Paint**: Rellena píxeles. Implica colores, imágenes, textos, sombras, etc.
    - **Layout**: Diseño de la página. Ancho, margin, padding, border, etc.
    
    Si nos dirigimos a [csstriggers.com](https://csstriggers.com/){target="_blank"}, podremos ver todas las propiedades de CSS que utilizamos y cómo actúan en los diferentes navegadores y motores. A continuación veremos una vista previa 👇.
    
    ![Página csstriggers.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-06-12%20at%202.45.28%20PM%20%281%29.jpeg)
    
    ## **Resumen de la articlase 🎯**
    
    Existen algunas propiedades en css que hacen que las paginas tarden mas en cargar. Esto se debe a que tienen que pasar por ciertas “capas” de renderizado hasta que se pinten en la pantalla.
    
    En pocas palabras, las propiedades que tengan relacion con una gran cantidad de pixeles nos van a afectar en el performance de la pagina web. Por eso el background afecta al desempeño de la pagina web ⌛.
    
    https://web.dev/articles/lcp?hl=es-419
    
    https://web.dev/articles/cls?hl=es-419
    
    https://csstriggers.com/
    
- **Debugging y uso de DevTools para optimizar animaciones web**
    
    En esta herramienta podemos encontrar diferentes tipos de herramientas para trabajar en paralelo con nuestro código de una manera muy eficiente.
    
    Algunas características en la cual nos puede servir son:
    
    - Accesibilidad web
    - Performance
    - Renderizare
    
    Para hacer uso de este servicio, deberemos abrir nuestro inspector.
    
    ```
    Darle en los tres puntos > More Tools > Rendering > Frame Rendering Stats
    
    ```
    
    Una vez hayamos seguido la ruta, nos aparecerá una pequeña ventana para poder ver la cantidad de frames que pasan en un solo segundo, también nos indica el tema de la memoria y la GPU 📢.
    
    ![Ver cantidad de frames.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-06-12%20at%202.55.14%20PM%20%281%29.jpeg)
    
    Ahora, si nos vamos a la pestaña que dice **Performance** 🎯, nos permitirá grabar nuestra animación para poder analizarla, con 10 seg estaría perfecto, nos mostraría la siguiente ventana.
    
    ![Performance.jpeg](https://static.platzi.com/media/articlases/Images/WhatsApp%20Image%202022-06-12%20at%203.41.42%20PM%20%281%29.jpeg)
    
    Con ello, podremos analizar, gracias a un diagrama al final, las distintas capas por las que pasa el renderizado explicado en la articlase anterior. También podremos analizarlo de acuerdo a fracciones de tiempo de nuestra animación grabada ✨.