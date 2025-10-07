# Fundamentos de CSS

Aprende CSS con un enfoque práctico y actual: comprenderás el modelo de caja, construirás interfaces 100 % *responsive* centradas en *mobile*, usarás variables para mantener estilos consistentes y dominarás herencia, especificidad, *Flexbox* y *Grid*. Con la guía de Diego de Granda, profesional con más de quince años en desarrollo de software y experiencia reciente en inteligencia artificial, terminarás con un portafolio listo para mostrar y lanzar al mercado.

## **¿Qué aprenderás para crear sitios responsive y orientados a mobile?**

La ruta de aprendizaje se enfoca en bases sólidas y herramientas modernas para resolver proyectos reales sin complicarte.

### **¿Qué cubre el modelo de caja en CSS?**

- Entender cómo se define y controla el tamaño de los elementos.
- Ajustar espaciados internos y externos con precisión.
- Lograr interfaces coherentes al alinear componentes.

### **¿Cómo se construyen layouts adaptables?**

- Usar **layouts** con *Flexbox* para distribuir y alinear elementos con flexibilidad.
- Emplear **Grid** para estructuras más complejas y responsivas.
- Diseñar **proyectos 100 % responsive** pensados desde *mobile*.

## **¿Cómo funcionan variables, herencia y especificidad en CSS?**

Estas herramientas evitan conflictos, reducen la repetición y mantienen el código claro y escalable.

### **¿Para qué sirven las variables en CSS?**

- Centralizar colores, tamaños y tipografías.
- Evitar repetir estilos en múltiples archivos.
- Cambiar un valor y actualizar toda la interfaz de forma consistente.

### **¿Qué aportan la herencia y la especificidad?**

- La **herencia** permite que estilos del contenedor padre afecten a los hijos de forma controlada.
- La **especificidad** ayuda a priorizar reglas y evitar “pisar” estilos por error.
- Combinar ambas permite un CSS más predecible y mantenible.

## **¿Qué resultados obtendrás y quién es tu profesor?**

El objetivo es que salgas con un entregable profesional y listo para uso real.

### **¿Qué tendrás al final?**

- Un **portafolio 100 % responsive** listo para agregar tus proyectos.
- Material preparado para **lanzarlo al mercado**.

### **¿Quién te acompaña en el proceso?**

- Diego de Granda, con **más de quince años** de experiencia en desarrollo de software.
- En los **últimos dos, tres años**, ha trabajado construyendo productos con **inteligencia artificial**.
- Acompañamiento directo para aplicar cada concepto a un proyecto práctico.

## **CSS: qué es y formas de aplicar estilos en HTML**

Aprende qué es CSS, cómo opera la **cascada** y cuáles son las tres formas de aplicar estilos en *HTML*. Aquí verás cuándo usar el atributo *style*, la etiqueta *style* en el *head* y una **hoja de estilos externa** con *link*, destacando ventajas de mantenimiento y consistencia.

## **¿Qué es CSS y cómo funciona la cascada?**

CSS significa *Cascade Style Sheets* y describe la **hoja de estilos en cascada**. La cascada implica que los estilos se aplican de arriba hacia abajo: los **últimos estilos** que afectan a un elemento son los que prevalecen. Si defines un color y luego, más abajo, vuelves a definir otro para el mismo elemento, el último gana.

- Los estilos posteriores sobrescriben a los anteriores, si apuntan al mismo elemento.
- Cambios finales pueden “romper” expectativas si no se entiende la cascada.
- Es clave planear cómo y dónde aplicar reglas para evitar conflictos.

## **¿Cuáles son las tres formas de agregar estilos en HTML?**

Existen tres formas de aplicar estilos: 1) como atributo *inline* en la propia etiqueta, 2) dentro de la etiqueta *style* en el *head*, 3) mediante una **hoja de estilos externa** enlazada con *link*. La recomendación práctica es trabajar con un archivo externo.

### **¿Cómo se usa el atributo style en línea?**

Agrega el estilo directamente sobre la etiqueta. Es la forma más antigua y la menos mantenible en proyectos grandes.

```jsx
<p style="color: blue;">Texto con color en línea.p>
```

- Ventaja: cambio inmediato y localizado.
- Desventaja: difícil de mantener cuando el proyecto crece.

### **¿Cómo funciona la etiqueta style en el head?**

Define reglas en el documento, dentro de *head*, apuntando a etiquetas como *H1* o *H2*.

```jsx
<head>
  <style>
    h1 { color: blue; }
    h2 { color: green; }
  style>
```

- Ventaja: centraliza estilos del documento.
- Desventaja: sigue siendo poco escalable en equipos y proyectos grandes.

### **¿Por qué conviene una hoja de estilos externa?**

Crea un archivo, por ejemplo styles.css, y enlázalo con *link* en el *head*. Es la **buena práctica** para mantener, versionar y escalar estilos.

```jsx
<head>
  <link rel="stylesheet" href="styles.css" />
```

```jsx
/* styles.css */
h1 { color: blue; }
h2 { color: green; }
```

- Ventaja: separación clara entre estructura y presentación.
- Ventaja: reutilización y cambios globales más simples.

## **¿Qué efectos verás al aplicar estilos por etiqueta?**

Si seleccionas una etiqueta como *p*, la regla afectará a **todas las etiquetas p** del documento. Sin embargo, un estilo en línea en una etiqueta específica puede prevalecer por la cascada y la **especificidad**.

```jsx
/* styles.css */
p { color: #5795D3; }
```

```jsx
<p style="color: blue;">Este párrafo mantiene su azul por estilo en línea.p>

<p>Este párrafo usa el color #5795D3 de la hoja externa.p>
```

- Seleccionar por etiqueta aplica el cambio a múltiples elementos a la vez.
- Un estilo en línea puede sobrescribir la regla general de la hoja externa.
- Aparecen retos de **especificidad** que conviene planear para evitar conflictos futuros.

## **2. Selectores y Especificidad**

Domina cómo aplicar estilos con precisión en *CSS* usando elementos, **clases**, **ID**, **pseudoclases**, **especificidad** y **herencia**. Aprende a evitar estilos repetidos, a inspeccionar el *HTML* en el navegador y a controlar cambios de estado como el *hover* con reglas claras y reutilizables.

## **¿Cómo seleccionar en CSS: elementos, clases e ID?**

Trabajar con selectores es la base. Un selector de etiqueta aplica estilos a todas las etiquetas del mismo tipo. Las clases son reutilizables en múltiples elementos. Los **ID son únicos** y deben usarse para casos puntuales, especialmente cuando más adelante se interactúe con *JavaScript*.

- Usa el inspector del navegador: clic derecho y abrir inspector para ver *HTML* y estilos aplicados.
- Selector de etiqueta: afecta todas las etiquetas del mismo nombre.
- Selector de clase: se invoca con punto y puede repetirse en varios elementos.
- Selector de ID: se invoca con numeral y solo debe existir una vez.
- Evita estilos en línea como práctica habitual: tienen demasiado peso y complican el mantenimiento.

Ejemplos.

```jsx
/* Selector de etiqueta: se replica en todos los elementos */
p {
  margin-bottom: 30px;
}

/* Clase reutilizable */
.rojo {
  color: red;
}

/* ID único */
#unico {
  background: yellow;
}

```

## **¿Cómo ser más específico: selectores descendientes y contenedores?**

Cuando no conviene crear más clases, los **selectores descendientes** permiten aplicar estilos solo a elementos dentro de un contenedor con clase. Esto evita “pisarse” entre estilos y mejora el control.

- Contenedor con clase: agrupa elementos relacionados.
- Selector descendiente: se escribe con un espacio entre el contenedor y el elemento objetivo.
- Solo afecta a los hijos dentro del contenedor indicado.

Ejemplos.

```jsx
/* Estilo del contenedor */
.contenedor {
  border: 2px solid blue;
}

/* Solodentro de .contenedor */
.contenedor p {
  color: blue;
}

```

## **¿Cómo usar pseudoclases y manejar especificidad y herencia?**

Las **pseudoclases** cambian estilos según el estado de un elemento. Útiles para indicar interacción visual como el *hover* en enlaces y botones. Además, conocer la **especificidad** y la **herencia** evita conflictos al crecer el proyecto.

### **¿Qué hacen las pseudoclases hover, link y visits?**

- *hover*: aplica estilos cuando el puntero pasa encima.
- *link*: aplica a enlaces no visitados.
- *visits*: aplica a enlaces ya visitados.

Ejemplos.

```jsx
/* Estado de interacción en botón */
button:hover {
  background: lightblue;
  cursor: pointer;
}

/* Enlace no visitado */
a:link {
  color: green;
}

/* Enlace visitado */
a:visited {
  color: yellow;
}
```

### **¿Cómo funciona la especificidad en CSS?**

Piensa la especificidad como un sistema de puntos que define qué regla gana.

- Elementos/etiquetas: 1 punto.
- Clases: 10 puntos.
- ID: 100 puntos.
- Estilos *inline*: 1000 puntos.
- *importance*: sobrescribe casi cualquier regla.

Claves prácticas.

- Los **ID** reescriben clases y etiquetas.
- Los estilos *inline* y *importance* deben usarse con cuidado.
- A mayor especificidad, más control, pero también más riesgo de conflictos.

### **¿Qué se hereda y qué no en CSS?**

La **herencia** transmite estilos desde el contenedor padre a sus hijos cuando aplica a propiedades de texto.

- Se heredan: color, familia tipográfica, tamaño de fuente, alineación de texto y estilos de fuente.
- No se heredan: margin, padding, border, background, width, height, position.

Ejemplo de herencia.

```jsx
/* El color se hereda a los hijos, comodentro de .contenedor */
.contenedor {
  color: blue;
}
```

## **3.Pseudo-clases y Elementos**

Aprende a aplicar **pseudoclases** y **pseudoelementos** en **CSS** con ejemplos directos. Verás cómo estilizar estados con **:focus**, seleccionar elementos específicos con **:first-child**, **:last-child** y **:nth-child(even)**, y cómo generar comillas con **::before** y **::after** sin tocar el **HTML**.

## **¿Cómo estilizar estados con pseudoclases de CSS?**

Las pseudoclases permiten apuntar a estados específicos del **DOM**. Un caso típico es el estado **:focus** en un *input*: cuando recibe clic o foco del teclado, puedes cambiar su estilo sin crear clases adicionales.

### **¿Qué hace :focus y cómo aplicarlo?**

- **:focus** estiliza el elemento enfocado.
- Útil para alinear el diseño con la guía visual del producto.
- Combina **outline** y **background-color** para dar feedback inmediato.

```jsx
input:focus {
  outline: 2px solid #3498DB;
  background-color: #E8F4F8;
}
```

- Se aplica a todos los *input* cuando están en **focus**.
- **outline** no altera el layout y destaca el elemento activo.

## **¿Cómo seleccionar elementos específicos en listas y tablas?**

Cuando necesitas estilos solo en el primer o último elemento de una lista, o alternar filas en una tabla, las pseudoclases evitan crear clases manuales. Esto hace los selectores más **específicos** y mantenibles.

### **¿Cómo aplicar :first-child y :last-child en listas?**

- Apunta al primer y último hijo de una lista.
- Evita clases extra por elemento.

```jsx
li:first-child {
  color: green;
  font-weight: bold;
}

li:last-child {
  color: red;
  font-weight: bold;
}
```

### **¿Para qué sirve :nth-child(even) en tablas?**

- Alterna estilos por posición en filas de *tabla*.
- Escala a muchas filas sin añadir clases.

```jsx
tr:nth-child(even) {
  background-color: gray;
}
```

- Puedes ajustar la regla a pares o a otras expresiones según necesidad.
- Útil cuando hay 4, 10 o 100 filas: la selección sigue siendo declarativa.

## **¿Cómo crear contenido con pseudoelementos sin tocar el HTML?**

Los **pseudoelementos** generan contenido que no existe en el **HTML**. Con **::before** y **::after** puedes añadir comillas u otros detalles visuales directamente desde **CSS** usando la propiedad **content**.

### **¿Cómo usar ::before y ::after con content?**

- **::before** y **::after** se escriben con doble dos puntos.
- **content** inserta el texto (por ejemplo, comillas) al inicio o al final.
- El estilo del contenido se controla como cualquier nodo: color, tamaño, etc.

```jsx
.quotes::before {
  content: '"';
  color: blue;
  font-size: 24px;
}

.quotes::after {
  content: '"';
  color: blue;
  font-size: 24px;
}
```

- La clase *.quotes* envuelve el texto citado.
- En el inspector verás **::before** y **::after** como nodos generados por **CSS**, no como texto real en el **HTML**.

## **4. Box Model**

Domina el **modelo de caja** en **CSS** para evitar sorpresas en el layout: entender cómo se combinan contenido, **padding**, **borde** y **margin**, y cuándo usar *box-sizing* te da control real de las dimensiones. Aquí verás, con enfoque práctico, cómo inspeccionar elementos, interpretar medidas y aplicar un *reset* que mantenga tu diseño consistente.

## **¿Qué es el box model en CSS?**

CSS trata a todos los elementos como **cajas**. Incluso el texto ocupa un rectángulo visible en el flujo. Con el inspector de elementos se puede ver el diagrama del modelo: **contenido** en azul, **padding** en verde, **borde** delineando el contenedor y **margin** como el espacio externo.

- **Contenido**: el área real del elemento, visible en azul. Define lo que se muestra.
- **Padding**: espacio interno entre contenedor y contenido. Al quitarlo, el contenido se pega al borde.
- **Borde**: línea que rodea el contenedor y ocupa píxeles. Útil para visualizar dimensiones y posición.
- **Margin**: espacio externo para separar contenedores. Un margin de 20 píxeles separa bloques que, sin esto, quedan encimados.

### **¿Cómo verlo en el inspector de elementos?**

- Selecciona el elemento en el inspector.
- Observa el diagrama del modelo de caja y sus medidas.
- Activa o desactiva **padding**, **borde** y **margin** para entender su efecto.

## **¿Cómo afectan padding, borde y margin el tamaño?**

Cuando defines un width, el cálculo del ancho total cambia según *box-sizing*. Con *content-box*, el **width** aplica solo al contenido y se suman **padding** y **borde** laterales al total. Con *border-box*, el **width** incluye padding y borde, así que el elemento respeta la medida establecida.

- Con *content-box*: ancho total = width + padding izquierdo y derecho + borde izquierdo y derecho.
- Ejemplo claro: width 200 píxeles + padding 20 y 20 + borde 5 y 5 = 250 píxeles. En la práctica se vio aproximadamente 249,33 píxeles.
- Con *border-box*: el elemento mantiene los 200 píxeles de ancho aunque agregues padding y borde.

### **¿Qué box-sizing conviene usar?**

- La buena práctica recomendada: resetear a *box-sizing: border-box* desde el inicio del proyecto.
- Beneficio clave: **control total del tamaño** sin cálculos adicionales ni desbordes inesperados.

## **¿Por qué hacer un reset de estilos del navegador?**

Los navegadores aplican estilos por defecto que pueden alterar tu diseño. Al quitar un *reset*, se notan saltos porque algunos elementos traen **margin** y **padding** predefinidos por el agente del navegador. Usar un selector que aplique a todos los elementos para hacer *reset* garantiza que los espacios sean exactamente los que defines tú.

- Quita márgenes y paddings por defecto que deforman el layout.
- Evita que estilos del navegador rompan tus decisiones de diseño.
- Facilita un control consistente junto con *box-sizing: border-box*.

### **¿Qué habilidades consolidarás?**

- Inspeccionar elementos y leer el diagrama del **modelo de caja**.
- Diferenciar **contenido**, **padding**, **borde** y **margin** y cuándo usar cada uno.
- Ajustar separación entre contenedores con **margin** y separación interna con **padding**.
- Configurar *box-sizing* para controlar dimensiones reales del layout.
- Verificar medidas como **width** y **height** directamente en el inspector y corregir discrepancias.

## **5. Position CSS**

Aprende a usar la propiedad **position** en CSS con confianza. Aquí verás cómo aplicar relative, absolute, fixed, sticky y z-index con patrones prácticos que mejoran la maquetación, el control del *scroll* y el orden visual de tus elementos.

## **¿Qué es position en CSS y cómo se aplica?**

La propiedad **position** define cómo un elemento se sitúa en la página y cómo responde a *top*, *right*, *bottom* y *left*. Además, **z-index** controla qué elemento queda por encima cuando se superponen.

Para facilitar el ejercicio, se configuraron estilos base y selección múltiple con comas para reutilizar reglas en varios contenedores.

```jsx
/* Estilos base para varios contenedores */
.contenedor,
.contenedor-padre,
.contenedor-scroll,
.contenedor-z-index {
  border: 2px solid black;
  margin: 20px 0;
  padding: 10px;
}

/* Estilos base para cajas internas */
.caja,
.hijo-absolute,
.boton-fixed,
.elemento-sticky,
.capa {
  border: 1px solid red;
  padding: 10px;
}
```

- **Propiedad clave**: position controla el flujo y el desplazamiento con *top/right/bottom/left*.
- **z-index**: no es un tipo de position, pero define el orden de apilado.
- **Selectores con comas**: una regla aplica a varias clases a la vez.

## **¿Cómo funcionan relative, absolute y fixed en CSS?**

Estos tres modos cambian el flujo del documento y la interacción con sus hermanos y su contenedor. Entender sus diferencias evita saltos inesperados de diseño.

### **¿Cuándo usar position relative con top, right, bottom, left?**

Con **relative**, mueves el elemento desde su lugar original sin afectar el espacio que ocupaba: sus hermanos lo siguen “respetando”.

```jsx
.caja-relative {
  position: relative;
  top: 20px;
  left: 30px;
}
```

- Desplaza desde su posición original.
- Sus hermanos mantienen el hueco original.
- Usa *top/left/right/bottom* para ajustes finos.

### **¿Qué hace position absolute dentro de un contenedor padre?**

Con **absolute**, el elemento sale del flujo y no reserva espacio. Se posiciona respecto al primer ancestro con position configurado (comúnmente relative en el padre).

```jsx
.contenedor-padre {
  position: relative;
  height: 100px;
}

.hijo-absolute {
  position: absolute;
  top: 10px;
  right: 10px;
}
```

- Requiere que el padre tenga position (relative, fixed o sticky).
- Sus hermanos no “guardan” su espacio.
- Se mueve libremente dentro del padre posicionado.

### **¿Cómo fijar un elemento con position fixed en la pantalla?**

**Fixed** ignora el contenedor y se ancla a la pantalla. Permite botones persistentes durante el *scroll*.

```jsx
.boton-fixed {
  position: fixed;
  bottom: 30px;
  right: 30px;
}
```

- Permanece visible aunque haya *scroll*.
- No depende del position del padre.
- Ideal para acciones persistentes, como chat o “subir”.

## **¿Cómo se comporta sticky y cómo ordenar con z-index?**

Sticky combina lo mejor de relative y fixed según el *scroll*. Por su parte, z-index resuelve qué capa se ve al frente cuando varias se superponen.

### **¿Cómo lograr un encabezado con position sticky y overflow?**

Primero, crea un contenedor con *scroll* propio y luego fija el elemento cuando toque el borde indicado.

```jsx
.contenedor-scroll {
  height: 150px;
  overflow-y: auto;
}

.elemento-sticky {
  position: sticky;
  top: 0;
}
```

- Se comporta como relative hasta alcanzar top: 0.
- Al llegar al borde indicado, actúa como fixed.
- Vuelve a relative al “liberarse” del borde al invertir el *scroll*.

### **¿Cómo controlar el orden visual con z-index y capas?**

Define un contexto posicionado en el contenedor y usa **z-index** en elementos absolute para controlar qué queda delante.

```jsx
.contenedor-z-index {
  position: relative;
  height: 150px;
}

.capa {
  position: absolute;
  width: 80px;
  height: 80px;
}

.capa-1 { top: 20px; left: 20px; background: blue;  z-index: 1; }
.capa-2 { top: 40px; left: 40px; background: red;   z-index: 2; }
.capa-3 { top: 60px; left: 60px; background: green; z-index: 3; }
```

- A mayor **z-index**, más adelante aparece la capa.
- Sin z-index, el orden depende del flujo y del apilado por defecto.
- El contenedor con position crea el contexto para apilar con control.

## 6. **Organización BEM**

BEM en CSS te permite **escalar estilos sin conflictos** al nombrar clases con una estructura clara. Con bloques, elementos y modificadores bien definidos, los estilos dejan de “pisarse” y el código se vuelve predecible, mantenible y fácil de leer.

## **¿Qué es BEM y cómo evita conflictos en CSS?**

BEM significa *block*, *element* y *modifier*. La idea central: **cada clase indica su rol y alcance**. Un bloque agrupa una pieza independiente de interfaz; un elemento es una parte del bloque; un modificador expresa un estado o variante.

- Bloque: representa un componente como una tarjeta, por ejemplo, `card`.
- Elemento: se nombra con doble guion bajo: `card__title`, `card__price`, `card__button`, `card__badge`.
- Modificador: se nombra con doble guion: `card--feature`, `card__button--disable`.

Así se evita que estilos globales se mezclen: **cada selector apunta a un contexto específico**.

### **¿Cómo se estructura un bloque, elemento y modificador?**

- Bloque independiente: `card` agrupa borde, *padding* y tamaño máximo.
- Elementos internos: `card__title`, `card__price`, `card__button` y `card__badge` heredan el contexto de `card`.
- Modificadores: `-feature` para destacar la tarjeta y `-disable` para estados del botón.

## **¿Cómo nombrar clases con BEM en una tarjeta card?**

La tarjeta funciona como **bloque principal**. Dentro, se definen elementos para el título, el precio, los botones y un *badge*. Luego se aplican modificadores para estados específicos.

### **¿Cómo estilizar el bloque card?**

Se trabaja primero el contenedor para visualizarlo con claridad: borde, espaciados y ancho máximo.

```jsx
.card {
  border: 2px solid #333;
  padding: 20px;
  margin-bottom: 20px;
  max-width: 300px;
}
```

- Borde visible para distinguir componentes.
- *Padding* interno uniforme.
- *Margin-bottom* para separar tarjetas.
- *Max-width* para controlar el crecimiento.

### **¿Cómo estilizar los elementos title, price y button?**

Se aplican estilos puntuales a cada elemento, sin afectar otros bloques.

```jsx
.card__title {
  color: #333;
  margin-bottom: 50px; /* se ajustó para que se note la separación */
}

.card__price {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 25px;
}

.card__button {
  padding: 10px 20px;
  color: white;
  border: none;
  cursor: pointer;
  margin-right: 5px;
}
```

- Título con color y separación perceptible.
- Precio con *font-size* grande y *font-weight* en negrita.
- Botón con *padding* cómodo, sin borde, color de texto blanco y *cursor* tipo *pointer*.

### **¿Cómo aplicar un badge dentro del bloque?**

Un distintivo como oferta se modela también como elemento.

```jsx
.card__badge {
  background: red;
  color: white;
  padding: 3px 8px;
  font-size: 12px;
}
```

- Señal visual clara con contraste.
- Tamaño compacto y legible.

## **¿Cómo usar modificadores para estados como feature y disable?**

Los modificadores expresan variaciones: uno para el bloque completo (*feature*) y otro para el botón deshabilitado (*disable*). Separar estado de estructura mantiene el CSS limpio y predecible.

### **¿Cómo diferenciar el bloque con card--feature?**

Se ajusta el borde para destacar el componente sin duplicar reglas del bloque base.

```jsx
.card--feature {
  border-color: gold;
  border-width: 3px;
}
```

- Visual más prominente sin romper la consistencia.
- Reutilización del bloque con mínimos cambios.

### **¿Cómo comunicar un botón deshabilitado con card__button--disable?**

El estado de “no permitido” se refleja en color y *cursor*.

```jsx
.card__button--disable {
  background: grey;
  cursor: not-allowed;
}
```

- Fondo gris para comunicar estado inactivo.
- *Cursor* not-allowed para retroalimentación inmediata.

### **¿Qué habilidades y keywords refuerzas?**

- Estructuración con **BEM**: *block*, *element*, *modifier*.
- Nomenclatura: `__` para elementos y `-` para modificadores.
- Encapsulamiento de estilos: evitar que “se pisen”.
- Propiedades clave: *border*, *padding*, *margin-bottom*, *max-width*, *color*, *font-size*, *font-weight*, *background*, *cursor*.
- Estados UI: *feature* para el bloque y *disable* para el botón.

## **7. Unidades de medida**

Elegir la unidad correcta en CSS es clave para lograr un diseño responsive, accesible y controlado. Aquí se explica, con ejemplos claros, cuándo usar **px**, **%**, **rem**, **em**, **vw** y **vh**, sus ventajas y sus límites en contenedores y texto. Además, verás por qué **rem** mejora la accesibilidad y cómo **vw/vh** simplifican ocupar toda la pantalla.

## **¿Por qué los pixels pueden limitar el diseño responsive?**

Los *pixels* son una unidad fija: si defines un contenedor de 200px, se mantendrá así sin importar el tamaño de pantalla. Esto puede obligar a hacer scroll si el contenido es más ancho que el *viewport*. Es útil en casos puntuales, pero no siempre para definir el *width* de contenedores.

- Los *pixels* no se adaptan al tamaño de pantalla.
- Si el *viewport* es menor, aparece scroll.
- Siguen siendo válidos según el caso de uso.

Ejemplo:

```jsx
.box-pixel {
  border: 1px solid red;
  padding: 16px;
  width: 200px;
}
```

Tip práctico: con el inspector de elementos verás cómo todo cambia salvo el primer bloque fijo en 200px cuando reduces la pantalla.

## **¿Cómo usar porcentajes para contenedores flexibles?**

El porcentaje se calcula con base en el contenedor padre. Si ese padre tiene dimensiones, tu caja puede adaptarse. Por ejemplo, 50% tomará la mitad del ancho disponible del padre, y se mantendrá proporcional al redimensionar la ventana.

- Depende del tamaño del contenedor padre.
- Permite contenedores flexibles y relativos.
- Requiere que el padre tenga dimensiones definidas.

Ejemplo:

```jsx
.box-percent {
  border: 1px solid red;
  padding: 16px;
  width: 50%;
}
```

## **¿Qué diferencias hay entre rem, em, vw y vh?**

Estas unidades relativas resuelven necesidades distintas. **rem** y **em** se basan en el *font-size*; **vw** y **vh** usan el tamaño del *viewport*. Elegir bien evita comportamientos inesperados y mejora la accesibilidad.

### **¿Qué es rem y por qué mejora accesibilidad?**

Un **rem** equivale siempre al *font-size* del documento base (*HTML*), que por defecto es **16 píxeles**. No cambia, aunque alteres el *font-size* de contenedores internos. Es ideal para texto y también útil para dimensiones consistentes.

- 1rem = 16px por defecto en *HTML*.
- No se ve afectado por *font-size* de contenedores internos.
- Mejora la accesibilidad: si el usuario cambia el tamaño de fuente del dispositivo, el contenido en rem se ajusta.

Ejemplo:

```jsx
.box-rem {
  border: 1px solid red;
  padding: 16px;
  width: 15rem; /* 15 x 16px = 240px por defecto */
}
```

### **¿Qué es em y por qué puede acumularse?**

Un **em** toma como referencia el *font-size* del contenedor padre inmediato. Si no hay uno definido, hereda el de *HTML* (16px). El problema: es acumulativo. Cambiar *font-size* en distintos niveles altera el valor efectivo de 1em, y puede dificultar llegar a valores exactos.

- 1em = *font-size* del padre.
- Si el padre es 20px: 1em = 20px.
- Con anidaciones, los cálculos se acumulan y pueden redondearse.

Ejemplo con acumulación:

```jsx
.container {
  font-size: 20px; /* aquí 1em = 20px */
}
.container .inner {
  font-size: 24px; /* cambia la base dentro de .inner */
}
.box-em {
  border: 1px solid red;
  padding: 16px;
  width: 1em; /* vale 16px, 20px o más, según el padre */
}
```

Consecuencia: para medidas de contenedor, **rem** suele ser más predecible que **em**.

### **¿Qué son vw y vh y cómo ocupan pantalla?**

**vw** (view width) y **vh** (view height) miden en función del *viewport*: 1vw es 1% del ancho de la pantalla; 1vh es 1% de la altura. Son precisos para ajustar bloques a la pantalla y facilitan patrones comunes como secciones a pantalla completa.

- 30vw: ocupa el 30% del ancho del *viewport*.
- 20vh: ocupa el 20% de la altura del *viewport*.
- Útiles para resolver alturas relativas antes complejas en *CSS*.

Ejemplos:

```jsx
.box-vw {
  border: 1px solid red;
  padding: 16px;
  width: 30vw;
}

.box-vh {
  border: 1px solid red;
  padding: 16px;
  height: 20vh;
}

/* Sección tipo *hero* a pantalla completa */
.hero {
  width: 100vw;
  height: 100vh;
}
```

Habilidades que practicas aquí: - Definir dimensiones con *px*, *%*, *rem*, *em*, *vw* y *vh* según el objetivo. - Usar el inspector para verificar comportamientos en diferentes tamaños de pantalla. - Priorizar **rem** para tipografías y medidas previsibles; evitar acumulación indeseada de **em**. - Aplicar *vw/vh* para bloques adaptados al *viewport*, como un *hero* a pantalla completa.

## 8.**Fuentes Web**

Elegir y configurar fuentes web en CSS define la legibilidad y el estilo de una interfaz. Aquí aprenderás a usar familias tipográficas del navegador, crear un **font stack** con *fallback* confiable y cargar tipografías de **Google Fonts** como Poppins e Inter, con pesos y variaciones bien seleccionados para títulos y textos.

## **¿Qué familias tipográficas existen y cómo impactan la legibilidad?**

Las tipografías se agrupan en cinco familias que todo navegador reconoce por defecto. Elegir la correcta mejora la claridad del contenido y el tono visual del sitio.

- **Serif**: con “decoraciones” al final de los trazos. Ejemplo típico: Times New Roman. Da un aire clásico y editorial.
- **Sans-serif**: sin decoraciones. Ejemplos comunes: Arial, Helvetica. Se percibe más limpia y moderna.
- **Monospace**: ancho fijo en cada carácter. Ideal para mostrar código.
- **Cursive**: simula escritura a mano.
- **Fantasy**: más decorativa y expresiva.

### **¿Qué diferencias hay entre serif, sans-serif y monospace?**

- Serif: termina en “piquitos” o remates, útiles para dar formalidad.
- Sans-serif: elimina remates, mejora la lectura en pantallas y se ve más neutral.
- Monospace: todos los caracteres ocupan el mismo ancho, facilita alinear símbolos y leer código.

### **¿Cuándo usar monospace para código?**

- Para resaltar funciones, variables y fragmentos de programación.
- Para mejorar la lectura de ejemplos técnicos.
- Para diferenciar texto técnico con fondo claro y padding.

## **¿Cómo definir font-family, tamaños y estilos en CSS?**

Empieza por apuntar a las familias genéricas del navegador con un **font-size** claro. Luego añade estilo visual cuando lo necesites.

```jsx
.serif {
  font-family: serif;
  font-size: 20px;
}

.sans {
  font-family: sans-serif;
  font-size: 20px;
}

.monospace {
  font-family: monospace;
  font-size: 20px;
  background: #f0f0f0;
  padding: 5px;
}
```

- Usa **font-family** para elegir la familia tipográfica.
- Define **font-size** consistente para jerarquía y lectura.
- Para destacar monospace: fondo claro y **padding** breve.

### **¿Qué errores típicos debes evitar al estilizar fuentes?**

- Olvidar el “#” en colores hexadecimales: el navegador no lo interpreta.
- Escribir “font” en lugar de **font-size**: no aplicará el tamaño.
- No verificar en el inspector: confirma qué fuente se está renderizando.

## **¿Cómo crear un font stack y cargar Google Fonts con fallback?**

Un **font stack** es la lista ordenada de fuentes en **font-family**. El navegador intenta la primera; si no existe en el sistema, usa la siguiente. Cierra siempre con una familia genérica como **serif**, **sans-serif** o **monospace** para asegurar un *fallback* universal.

```jsx
/* Ejemplo de font stack con genérica al final */
.code-label {
  font-family: "Courier New", Courier, monospace;
}
```

Cargar de terceros con **Google Fonts** permite controlar pesos y variaciones como *Roman* o *itálica* para casos específicos (por ejemplo, títulos en **bold 700**). Embeber con la etiqueta HTML de *link* es directo.

```jsx
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Inter:wght@400;600&display=swap" rel="stylesheet">
```

Luego, define tus clases con comillas y agrega la familia genérica como *fallback*.

```jsx
.google-title {
  font-family: "Poppins", sans-serif; /* títulos */
}

.google-text {
  font-family: "Inter", sans-serif; /* párrafos */
}
```

- **Buena práctica**: termina el *stack* con una familia genérica. Garantiza renderizado consistente si falla la fuente primaria.
- **Compatibilidad**: algunas fuentes existen solo en ciertos sistemas (Mac OS o iOS) y no en Windows. El *fallback* evita inconsistencias.
- **Confiabilidad**: si se cae el servicio de fuentes, el *fallback* entra sin romper el diseño.

### **¿Qué considerar al combinar fuentes del sistema y de terceros?**

- Prioriza la fuente de marca, pero planea un *fallback* coherente.
- Selecciona solo los pesos necesarios para rendimiento.
- Alinea usos: títulos con **700**, textos con **400/600** según necesidad.

## 9. **Propiedades Tipográficas**

Mejora la legibilidad y accesibilidad dominando las propiedades tipográficas de CSS: *font-size* con *rem*, *font-weight*, *line-height* y *font-style*. Con pequeños ajustes, el texto se vuelve más claro, cómodo y consistente en distintos dispositivos. Aquí verás cómo aplicar estos cambios con clases simples como normal, light, bold, compact, space e italic.

## **¿Cómo ajustar el tamaño de fuente con rem para mejorar la accesibilidad?**

Usar *rem* en *font-size* garantiza un tamaño proporcional a la configuración del dispositivo. **1rem equivale a 16 píxeles**, y se adapta si la persona sube el tamaño de fuente en su sistema. **Es recomendable utilizar rem** para no perder legibilidad cuando el usuario necesita ampliar la tipografía.

```jsx
.normal {
  font-size: 1rem;
}
```

- 1rem: 16 px por defecto del navegador.
- Escala flexible según ajustes del usuario.
- Cambia el valor según necesidad: 1, 1.2, 2, etc.
- Mejora la visibilidad sin recalcular píxeles.

## **¿Qué es font-weight y cómo elegir el peso adecuado?**

El **peso de la fuente** define qué tan delgada o gruesa se ve. Con *font-weight* puedes ir de 100 a 900, pero **no todas las fuentes incluyen todos los pesos**. En fuentes por defecto, 300 y 400 pueden verse casi iguales; desde 600 se nota más diferencia. **900 se percibe como muy negrita**, similar a *bold*.

```jsx
.light {
  font-weight: 300;
}

.bold {
  font-weight: 900;
}
```

- Rango típico: 100 a 900.
- Variación visible: aumenta desde 600.
- Depende de la familia tipográfica disponible.
- Úsalo según el contenido: ligero para textos largos, pesado para énfasis.

## **¿Cómo usar line-height y font-style para mejorar la legibilidad?**

El **interlineado con *line-height*** añade “aire” entre líneas. En un párrafo con varias líneas (incluso separadas con *break line*), un valor bajo compacta el texto y uno alto facilita la lectura. **No uses unidades**: se declara con número.

```jsx
.compact {
  line-height: 1;
}

.space {
  line-height: 2;
}
```

- 1: texto compacto, menos separación.
- 2: mucho “aire”, lectura relajada.
- Intermedios útiles: 1.5 o 1.2 según el bloque.
- Ajusta según la longitud del texto y el contexto.

El **estilo de la fuente** se maneja con *font-style*. Hay tres opciones: **normal (también llamado “*roman*”)**, **italic** y **oblique**. *Oblique* inclina el texto de forma artificial cuando no existe una versión cursiva nativa.

```jsx
.italic {
  font-style: italic;
}

.oblique {
  font-style: oblique;
}

.normal {
  font-style: normal; /* valor por defecto */
}
```

- normal: estilo por defecto de la familia.
- italic: variante cursiva cuando existe.
- oblique: inclinación artificial cuando no hay cursiva.

## 10.**Control de Texto**

Controla tu tipografía con precisión usando **propiedades clave de CSS** para alinear, transformar, decorar e indentar texto. Aquí verás cómo aplicar *text-align*, *text-transform*, *text-decoration* y *text-indent* de forma clara, con ejemplos prácticos y consideraciones de maquetación.

## **¿Cómo alinear texto con CSS sin complicaciones?**

La alineación define la posición del contenido dentro de su contenedor. Por defecto, los párrafos se alinean a la izquierda y ocupan el **100 % del *width*** disponible. Con **la propiedad** *text-align* puedes usar valores como *left*, *center*, *right* y *justify* para lograr el resultado deseado. El centrado funciona mientras el contenedor tenga espacio; si no, necesitarás otras técnicas de maquetación.

```jsx
.left { text-align: left; }
.center { text-align: center; }
.right { text-align: right; }
.justify { text-align: justify; }
```

- **Left**: alineación por defecto a la izquierda.
- **Center**: centra el texto dentro del ancho disponible.
- **Right**: empuja el texto hacia la derecha.
- **Justify**: distribuye espacios para ocupar el ancho completo en cada línea.

Nota: *justify* ajusta los espacios entre palabras en líneas con suficiente contenido. Si una línea tiene pocas palabras, no forzará espacios excesivos.

## **¿Qué transformaciones de texto mejoran la legibilidad?**

Cuando el contenido llega en un formato y necesitas mostrarlo en otro, usa **la propiedad** *text-transform*. Puedes convertir a mayúsculas, minúsculas o capitalizar cada palabra sin cambiar el contenido original.

```jsx
.uppercase { text-transform: uppercase; }
.lowercase { text-transform: lowercase; }
.capitalize { text-transform: capitalize; }
```

- **Uppercase**: convierte todo a mayúsculas.
- **Lowercase**: transforma a minúsculas.
- **Capitalize**: pone en mayúscula la letra inicial de cada palabra.

Estas opciones ayudan a mantener consistencia tipográfica según el tono o la formalidad del contenido.

## **¿Cómo decorar e indentar texto de forma efectiva?**

Las decoraciones resaltan estados o estilos visuales. Las etiquetas de ancla traen subrayado por defecto, pero con **la propiedad** *text-decoration* puedes controlar la línea, y con *color* ajustar el color del texto.

```jsx
.underline { text-decoration: underline; }
.through { text-decoration: line-through; }
.no-underline { text-decoration: none; color: red; }
```

- **Underline**: añade una línea inferior a cualquier elemento, no solo enlaces.
- **Line-through**: tacha el texto; útil para estados como tareas completadas.
- **None**: elimina el subrayado en enlaces; combina con *color* para cambiar el azul por defecto.

Para maquetación editorial, **la propiedad** *text-indent* permite una sangría en la primera línea del párrafo, logrando un estilo de lectura más clásico.

```jsx
.indent { text-indent: 2rem; }
```

- **Text-indent**: aplica la sangría solo en la primera línea.
- **Unidades**: usar *rem* asegura consistencia relativa al tamaño base de fuente.

## 11. **Sistemas de Color**

Domina cómo aplicar color en CSS con **hexadecimal**, **RGB**, **HSL**, **alfa (RGBA)** y **nombres de color**. Verás cómo estos sistemas controlan el *background-color*, el texto y los bordes, con ejemplos claros para evitar dudas comunes y lograr tonos exactos.

## **¿Qué formatos de color usar en CSS?**

Estos son los formatos más usados para estilos consistentes. Cada uno controla **rojo, verde y azul** con una lógica distinta, pero todos sirven para definir el mismo resultado: un color en pantalla.

- **Hexadecimal (#RRGGBB)**: valores 0–9 y A–F. Dos dígitos por canal. Empieza con numeral. 000000 es negro. FFFFFF es blanco.
- **RGB (rgb(r, g, b))**: tres valores del 0 al 255 por canal. 0 apaga el canal, 255 lo lleva al máximo.
- **HSL (hsl(h, s%, l%))**: tono en grados 0–360, saturación 0–100 %, luminosidad 0–100 %.
- **Alfa (rgba)**: cuarto valor 0–1 para transparencia. 1 es sólido; 0, totalmente transparente.
- **Nombres de color**: palabras como green o gold. Lista amplia y práctica para ajustes rápidos.

## **¿Cómo aplicar cada sistema con ejemplos en código?**

Cada sistema tiene su sintaxis y rango. La clave es entender cómo se combinan los canales y qué hace cada número en el resultado visual.

### **¿Cómo funciona el color hexadecimal en CSS?**

El formato **#RRGGBB** combina rojo, verde y azul en **alfanumérico 0–9 y A–F**. Los dos primeros dígitos son rojo, los dos siguientes verde y los últimos azul.

```jsx
/* Blanco y negro. */
.box-blanco { background-color: #FFFFFF; }
.box-negro  { background-color: #000000; }

/* Rojo con combinación alta en R y valores menores en G y B. */
.box-rojo   { background-color: #FF5733; }
```

Claves prácticas: - Empieza con **#**. Siempre seis dígitos. - **FF** es el máximo del canal. **00** es el mínimo.

### **¿Qué hacen rgb y rgba con el color y la transparencia?**

En **rgb(r, g, b)** cada canal va de **0 a 255**. Es muy directo para ajustar intensidad por canal y es como se **renderizan** las imágenes en el navegador: píxel a píxel combinando RGB.

```jsx
/* Primarios. */
.box-negro  { background-color: rgb(0, 0, 0); }
.box-rojo   { background-color: rgb(255, 0, 0); }
.box-verde  { background-color: rgb(0, 255, 0); }
.box-azul   { background-color: rgb(0, 0, 255); }

/* Azul verdoso medio tenue. */
.box-azul-tenue { background-color: rgb(52, 152, 219); }
```

Con **rgba(r, g, b, a)** agregas el **alfa** para transparencia del 0 al 1.

```jsx
/* Sólido. */
.box-solida { background-color: rgba(231, 76, 60, 1); }
/* Media transparencia. */
.box-media  { background-color: rgba(231, 76, 60, 0.5); }
/* Más tenue. */
.box-tenue  { background-color: rgba(231, 76, 60, 0.25); }
```

Pautas rápidas: - Alfa en 1: color **100 % sólido**. - Alfa en 0.5: **semítransparente**. - Alfa en 0.25: **muy tenue**.

### **¿Cómo leer y ajustar hsl con tono, saturación y luminosidad?**

En **hsl(h, s%, l%)**: - **h** es el tono en **grados 0–360**. Se recorre por los principales: del 0 hacia rangos cercanos se perciben rojos; más adelante verdes; después azules. - **s** es saturación en **%**: 0 % da grises, 100 % da color puro. - **l** es luminosidad en **%**: 0 % es negro, 50 % color “normal”, 100 % blanco.

```jsx
/* Rojo con saturación media y luminosidad media. */
.box-hsl { background-color: hsl(0, 50%, 50%); }
```

Nota sobre nombres de color: también puedes declarar colores por nombre cuando necesitas rapidez en *background-color* o color de texto.

```jsx
.titulo { color: green; }
.destacado { background-color: gold; }
```

## **¿Qué habilidades y conceptos clave practicar?**

Potencia tu dominio con estas prácticas. Te darán control fino del color según el contexto de diseño y accesibilidad.

- Identificar canales: **rojo, verde y azul** en hex, rgb y rgba.
- Usar **rangos** correctos: 0–9 y A–F en hex; 0–255 en rgb; 0–360/0–100 %/0–100 % en hsl.
- Ajustar **saturación** para pasar de gris a color puro.
- Controlar **luminosidad** para moverte de negro a blanco.
- Aplicar **alfa** para superposiciones y fondos con transparencia.
- Cambiar color en propiedades: *background-color*, *color* (texto), *border*.
- Elegir formato según necesidad: hex para compactar, rgb para precisión por canal, hsl para manipular tono, rgba para transparencia, nombres para rapidez.

## **12. Variables CSS**

Las variables de CSS son la forma más simple y robusta de asegurar consistencia visual, acelerar cambios globales y evitar repetir código. Con el pseudoselector *:root* y la función *var()* puedes centralizar colores, espacios y tipografías, y escalar sin dolor proyectos con decenas de botones o tarjetas.

## **¿Por qué usar variables CSS para escalar proyectos?**

Las variables permiten definir un valor una sola vez y reutilizarlo en todo el CSS. Así evitas copiar y pegar, mantienes una **línea visual coherente** y haces **cambios globales en segundos**. Si diseño cambia la paleta, editas la variable y todo se actualiza de forma automática.

- Reducen repetición de estilos y errores humanos.
- Mantienen colores y fuentes consistentes.
- Hacen cambios globales desde un solo lugar.
- Mejoran el mantenimiento y tu salud mental.

### **¿Qué problemas resuelven las variables CSS?**

- Botones repetidos con el mismo *background*, *padding* y *margin*.
- Discrepancias por recordar mal un color o una fuente.
- Dificultad para actualizar paletas o espacios en muchos componentes.

## **¿Cómo declarar y usar variables con :root y var?**

El pseudoselector *:root* actúa como un contenedor global con mayor especificidad que *html*. Define ahí variables para que todo el documento pueda usarlas. La sintaxis: dos guiones, nombre y valor; luego consume con *var()*.

### **¿Cómo se declaran variables globales en :root?**

```jsx
:root {
  --color-primary: #3498db;
  --color-secondary: #2ecc71;
  --color-danger: #e74c3c;
  --color-dark: #2c3e50;
  --color-light: #ecf0f1;
  --space: 20px;
}
```

### **¿Cómo se aplican en botones y tarjetas reutilizables?**

Define estilos base del *button* y luego variantes que solo cambian el color de fondo con *var()*.

```jsx
button {
  padding: 10px 20px;
  margin: 5px;
  border: none;
  cursor: pointer;
}

.button-primary { background: var(--color-primary); }
.button-secondary { background: var(--color-secondary); }
.button-danger   { background: var(--color-danger); }

.card {
  background: var(--color-light);
  color: var(--color-dark);
  padding: var(--space);
  margin: 10px 0;
  border-radius: 5px;
}
```

Claves prácticas: - Usa *:root* para variables globales. - Nombra claro: por ejemplo, --color-primary, --space. - Centraliza cambios: cambia el valor en la variable y listo. - Extiende con variaciones ligeras, como *hover* si lo necesitas.

## **¿Cómo reescribir variables por componente sin romper estilos globales?**

Cuando un elemento necesita una variante específica, no dupliques reglas. Mantén la clase base y agrega una segunda clase que **reescriba el valor de la variable** solo en ese contexto. Así cambias el estilo local sin tocar el valor global.

### **¿Cómo sobreescribir variables en una clase compuesta?**

En el HTML se usa algo como class="card card-dark". La clase *card* define el estilo general y *card-dark* solo ajusta variables.

```jsx
/* card base usa var(--color-light) como fondo y var(--color-dark) como texto */
.card {
  background: var(--color-light);
  color: var(--color-dark);
}

/* esta variante reescribe los valores para esta tarjeta en particular */
.card.card-dark {
  --color-light: blue;  /* fondo localmente azul */
  --color-dark: white;  /* texto localmente blanco */
}
```

Beneficios de esta técnica: - Evita duplicar reglas de *background* y *color*. - Cambia solo ese componente sin afectar a los demás. - Mantiene las clases reutilizables y fáciles de mantener.

## 13.**Degradados**

Aprende a crear **backgrounds con degradados en CSS** de forma clara y rápida. Desde la preparación del contenedor hasta *linear-gradient* y *radial-gradient* con dirección, posición y múltiples colores. Todo con ejemplos prácticos y listos para copiar.

## **¿Cómo preparar los contenedores con CSS para degradados?**

Para que los degradados se aprecien bien, primero se definen estilos comunes en los contenedores *div*. La idea: usar el *background* del elemento como lienzo del degradado y asegurar buena legibilidad del texto.

- **Tamaño base**: *width* 200px y *height* 100px.
- **Espaciado**: *margin* 10px y *padding* 20px.
- **Legibilidad**: *color* blanco.
- **Distribución**: *display* en *inline-block* para que se ubiquen en línea con propiedades de bloque.
- **Alineación**: *text-align* center y *line-height* 60px para centrar el texto.

```jsx
.demo {
  width: 200px;
  height: 100px;
  margin: 10px;
  padding: 20px;
  color: #fff;
  display: inline-block; /* en línea, con propiedades de bloque */
  text-align: center;
  line-height: 60px;
}
```

Claves prácticas: - **inline-block** coloca elementos en línea y respeta ancho/alto. - Si no hay espacio, los elementos bajan de línea de forma natural.

## **¿Cómo crear degradados linear con dirección y diagonal?**

Un **degradado lineal** fusiona colores en una línea. Por defecto, *linear-gradient* va de arriba hacia abajo y acepta más de dos colores, aunque aquí se trabaja con dos para claridad.

### **¿Qué es un linear-gradient simple?**

- Por defecto, dirección vertical (arriba a abajo).
- Colores: azul #3498DB hacia morado #9B59B6.

```jsx
.linear-simple {
  background: linear-gradient(#3498DB, #9B59B6);
}
```

### **¿Cómo cambiar la dirección a la derecha?**

- Se define la dirección con palabras clave.
- Dirección: *to right*.
- Colores: rojo #E74C3C hacia amarillo/naranja #F39C12.

```jsx
.linear-direction {
  background: linear-gradient(to right, #E74C3C, #F39C12);
}
```

### **¿Cómo trazar un degradado diagonal?**

- Dirección diagonal: *to bottom right*.
- Colores: verde claro #2ECC71 hacia azul #3498DB.

```jsx
.linear-diagonal {
  background: linear-gradient(to bottom right, #2ECC71, #3498DB);
}
```

Puntos clave: - **Dirección controlada** con palabras como *to right* o *to bottom right*. - **Fusión suave** entre colores con resultados limpios.

## **¿Cómo usar radial-gradient y múltiples colores?**

Un **degradado radial** crea transiciones circulares desde un punto. Se puede definir la forma del círculo y su posición inicial. Además, los degradados admiten **múltiples colores** para efectos como arcoíris.

### **¿Cómo crear un radial-gradient simple?**

- Forma: *circle*.
- Colores: del amarillo/naranja #F39C12 al rojo #E74C3C desde el centro.

```jsx
.radial-simple {
  background: radial-gradient(circle, #F39C12, #E74C3C);
}
```

### **¿Cómo posicionar el centro del gradiente radial?**

- Posición del centro con *at*.
- Posición: *at top left*.
- Colores: rojo #E74C3C hacia azul #3498DB.

```jsx
.radial-position {
  background: radial-gradient(circle at top left, #E74C3C, #3498DB);
}
```

### **¿Cómo aplicar múltiples colores en un degradado lineal?**

- Dirección: *to right*.
- Colores: red, orange, yellow, green, blue.

```jsx
.multiple {
  background: linear-gradient(to right, red, orange, yellow, green, blue);
}
```

Buenas prácticas y usos: - **Backgrounds** de secciones como heroes o contenedores. - **Contraste**: texto blanco para máxima legibilidad. - **Escalabilidad**: combinar dirección y posición según el diseño.

## 14.**Sombras y Bordes**

Domina sombras y bordes en CSS con una guía clara y práctica. Aprenderás a combinar box-shadow, text-shadow y border-radius para crear contenedores y textos más atractivos, con trucos útiles como usar el inspector del navegador y evitar errores comunes en la sintaxis.

## **¿Cómo preparar estilos base para contenedores en CSS?**

Antes de aplicar sombras y bordes, conviene definir estilos consistentes para los elementos que usarás. Aquí se trabaja con div y la etiqueta p para que se comporten como tarjetas simples.

- Usa **display: inline-block** para que, si hay espacio, se coloquen en línea.
- Define **padding** y **margin** para separar contenido y elementos.
- Fija **background: white** para evitar transparencias indeseadas.
- Limita el encogimiento con **min-width: 100px**.
- Centra el texto con **text-align: center**.

```jsx
div, p {
  display: inline-block;
  padding: 20px;
  margin: 10px;
  background: #fff;
  min-width: 100px;
  text-align: center;
}
```

### **¿Qué conceptos clave aplicas aquí?**

- *display: inline-block*: coloca cajas en línea respetando dimensiones.
- *padding* y *margin*: espaciado interno y externo.
- *background*: buena práctica para visibilidad consistente del contenedor.
- *min-width*: evita que el contenido colapse más allá de un mínimo.
- *text-align: center*: alinea el texto al centro del contenedor.

## **¿Cómo aplicar y ajustar box-shadow e inset?**

La sombra de caja agrega profundidad a contenedores. Se compone de desplazamiento horizontal, desplazamiento vertical, difuminado (*blur*), expansión (*spread*) y color. Un error común: **no se usan comas** entre valores de box-shadow.

- Define primero una sombra simple con desplazamientos y color.
- Usa el inspector del navegador para **debuggear** y ajustar en vivo.
- Ajusta **blur** para difuminar y **spread** para expandir la sombra.
- Aplica **inset** si deseas una sombra interna.

```jsx
/* Sombra externa simple */
.shadow-simple {
  box-shadow: 5px 5px gray;
}
```

- Si necesitas una sombra interna, antepone **inset** y agrega el difuminado.

```jsx
/* Sombra interna (inset) con difuminado */
.shadow-inset {
  box-shadow: inset 0 0 10px gray;
}
```

### **¿Qué ajustes hacer con el inspector del navegador?**

- Arrastra el *widget* de sombras para explorar X e Y.
- Incrementa *blur* para una sombra más realista.
- Modera *spread* para evitar bordes exagerados.
- Copia los valores finales y pégalos en tu CSS.

## **¿Cómo crear sombras de texto y bordes redondeados efectivos?**

El texto también puede beneficiarse de una sombra sutil. Y con bordes redondeados, tus contenedores se sienten más amables y modernos, ideales para “tarjetas”.

### **¿Qué ajustes mejoran una text-shadow legible?**

- Usa desplazamientos moderados para no perder legibilidad.
- Aplica un *blur* equilibrado para suavizar sin deformar.
- Mantén un color **gris tenue** para no competir con el contenido.

```jsx
/* Sombra de texto sutil */
.text-shadow {
  text-shadow: 2px 2px 5px gray;
}
```

### **¿Cómo redondear bordes con border-radius?**

- Define un borde discreto y redondea esquinas.
- Combina **border-radius** con **box-shadow** para un efecto de tarjeta.

```jsx
/* Tarjeta con borde y esquinas suaves */
.radius-small {
  border: 2px solid #333;
  border-radius: 5px;
}
```

- Para lograr un **círculo** (ideal para avatares), usa **border-radius: 50%** y define ancho y alto iguales.

```jsx
/* Convertir en círculo */
.radius-small {
  width: 100px;
  height: 100px;
  border-radius: 50%;
}
```

- Si prefieres esquinas más marcadas, cambia el radio a 15px.

```jsx
/* Esquinas más redondeadas */
.radius-small {
  border-radius: 15px;
}
```

## 16.**Introducción Flexbox**

La alineación en *CSS* dejó de ser un dolor de cabeza con *Flexbox*. Aquí verás cómo activar el modelo flex, cuándo usarlo y qué propiedades aplican para centrar y distribuir elementos sin trucos. Todo con ejemplos claros y concisos, tal como se trabajó en el código.

## **¿Qué problema resuelve flexbox y cómo activarlo?**

Flexbox simplifica la tarea de **posicionar contenido dentro de contenedores**. Antes, centrar o reacomodar elementos era complejo y frágil. Con un solo cambio de *display*, el contenedor adopta el **modelo de layout flexible**, y puedes alinear y distribuir sus elementos con control total.

- Define un contenedor principal (*container*).
- Cambia su *display* a **flex** para activar *Flexbox*.
- Los elementos internos se vuelven **items flex** y responden al eje principal y transversal.

Ejemplo aplicado al contenedor principal con estilos base:

```jsx
.container {
  display: flex; /* Activa el modelo de Flexbox */
  background: #f0f0f0; /* background gris claro */
  padding: 10px; /* espacio interno */
  margin-bottom: 20px; /* separación entre contenedores */
  min-height: 100px; /* altura mínima del contenedor */
}
```

Idea clave: al pasar de *display: block* a *display: flex*, el layout cambia y puedes **usar propiedades flex** para alinear y distribuir con precisión.

## **¿Cómo se estiliza el contenedor y los items con CSS?**

Se distinguen el contenedor y los elementos internos para visualizar mejor el comportamiento. Así se entiende dónde actúa cada propiedad.

- Los elementos internos son **items** (por ejemplo, *divs* con números).
- Se usa un *background* visible y separación entre elementos.
- El texto se centra con *text-align* y se mejora la legibilidad con *padding*.

Ejemplo para los items:

```jsx
.item {
  background: #3498db; /* azul para diferenciar */
  color: white; /* contraste del texto */
  margin: 5px; /* separación entre items */
  text-align: center; /* centra el texto en el item */
  padding: 20px; /* espacio interno del item */
}
```

Habilidades que desarrollas: reconocer el **rol del contenedor** frente a los **items**, aplicar *padding*, *margin*, *min-height* y colores para **inspeccionar y depurar** el layout.

## **¿Cómo funcionan flex-direction, justify-content y align-items?**

Con *display: flex* activo, el siguiente paso es controlar la **dirección**, la **distribución** y la **alineación**. Estas tres propiedades cubren la mayoría de casos cotidianos de alineación en *CSS*.

### **¿Qué hace flex-direction en el eje principal?**

Define la dirección del **eje principal** del contenedor flex.

```jsx
.column {
  display: flex;
  flex-direction: column; /* apila los items en columna */
}
```

- Cambia de fila (por defecto) a columna con `column`.
- Útil cuando quieres que los items ocupen el 100% a lo largo del eje vertical.
- Permite pensar en **eje principal** (horizontal o vertical) y **eje transversal**.

### **¿Cómo centrar con justify-content en el eje principal?**

Controla la alineación y distribución a lo largo del eje principal del contenedor.

```jsx
.center {
  display: flex;
  justify-content: center; /* centra los items en el eje principal */
}
```

- Centra horizontalmente si el eje principal es una fila.
- Centra verticalmente si usas `flex-direction: column`.
- Palabras clave frecuentes: `flex-start`, `center`, `flex-end`, `space-between`, `space-around`.

### **¿Cómo alinear con align-items en el eje transversal?**

Alinea los items en el **eje transversal** del contenedor.

```jsx
.align {
  display: flex;
  align-items: center; /* centra los items en el eje transversal */
}
```

- Centra de arriba a abajo cuando el eje principal es horizontal.
- Responde al tamaño del contenedor padre (por ejemplo, `min-height: 100px`).
- Antes era complejo; ahora basta **una línea** con *Flexbox*.

Conceptos que dominas al practicar: - **Contenedor vs items**: dónde aplicar cada propiedad. - **Eje principal y eje transversal**: base mental de *Flexbox*. - **Centrado real** con `justify-content` y `align-items` sin hacks.

## 17.**Flexbox Avanzado**

Aprende a dominar **Flexbox** con ejemplos prácticos: configura el contenedor con **display: flex**, centra el contenido, controla el crecimiento con **flex-grow** y el atajo **flex**, y alinea elementos con **align-self**. Todo enfocado en un *workflow* claro y listo para aplicar en tus componentes en CSS.

## **¿Cómo configurar el contenedor y los items en Flexbox?**

Para activar el modelo de **Flexbox**, el primer paso es convertir el contenedor en un contexto flexible con **display: flex**. Así se habilitan las propiedades que permiten distribuir y alinear los elementos internos de forma eficiente. También se aplica **min-height: 100px** para asegurar una altura mínima, y se usa **margin-bottom** y **padding** para separar y dar aire visual.

```jsx
.container {
  display: flex;
  min-height: 100px;
  /* margin-bottom: ...; */
  /* padding: ...; */
  /* background: ... (gris utilizado previamente) */
}
```

### **¿Cómo se centra el texto dentro del item?**

Cada elemento dentro del contenedor es un **item**. Para centrar su contenido horizontalmente se usa **text-align: center**. Además, se aplica **padding** para generar espacio interno, **margin** para separación entre tarjetas, un **background** azul y **color: white** para contraste.

```jsx
.item {
  text-align: center;
  padding: 20px;
  margin: 5px;
  background: #3498db;
  color: white;
}
```

- Activar contexto flexible con *display: flex*.
- Asegurar altura mínima con *min-height: 100px*.
- Separar bloques con *margin-bottom* y dar aire con *padding*.
- Centrar texto con *text-align: center*.

## **¿Cómo hacer que los elementos crezcan con flex-grow y flex?**

Cuando hay espacio libre en el contenedor, **flex-grow** permite que los items crezcan para ocuparlo. Así controlas la proporción de crecimiento entre elementos vecinos de forma simple.

### **¿Qué hace flex-grow 0, 1 y 2?**

- 0: no crece para ocupar espacio extra.
- 1: crece proporcionalmente al resto que también tiene 1.
- 2: crece el doble respecto a los que tienen 1.

```jsx
.grow { /* aplicado al elemento con clase correspondiente */
  flex-grow: 1;
}
```

Ejemplo de uso: si un item tiene `.grow` con **flex-grow: 1**, ocupará espacio libre; si otro tiene valor 2, crecerá el doble que el de 1.

### **¿Cuándo usar el shorthand flex?**

El atajo **flex** agrupa varias configuraciones en una sola línea. En el ejemplo, **flex: 1** se comporta como el crecimiento proporcional visto con **flex-grow**.

```jsx
.flex.uno { /* elemento con clases: flex y uno */
  flex: 1;
}

.flex.dos { /* elemento con clases: flex y dos */
  flex: 2;
}
```

- *flex: 1* hace que el item crezca para ocupar el espacio disponible.
- *flex: 2* crece el doble que los que tienen *flex: 1*.
- Útil cuando quieres definir crecimiento de manera breve y consistente.

## **¿Cómo alinear contenido con align-self?**

Para alinear items de forma independiente, **align-self** permite posicionarlos en el eje cruzado. Con **flex-start** se sitúan arriba y con **flex-end** abajo. El alto visible se adapta al contenido y al **padding** aplicado.

```jsx
.self.start { /* elemento con clases: self y start */
  align-self: flex-start;
}

.self.end { /* elemento con clases: self y end */
  align-self: flex-end;
}
```

- *align-self: flex-start*: alinea el item en la parte superior.
- *align-self: flex-end*: alinea el item en la parte inferior.
- El espacio visible depende del contenido y del *padding* del item.

## **18.Grid Básico**

Con CSS Grid puedes **posicionar contenido en dos ejes a la vez** de forma clara y escalable. Activa el modelo con *display: grid*, define columnas con *grid-template-columns* usando fracciones *fr*, automatiza con la función *repeat()* y controla el espacio interno con *gap*. Verás un **grid 2×2**, cómo repartir **1fr 2fr 1fr**, y cuándo preferir *gap* en lugar de *margin*.

## **¿Qué diferencia a grid de flexbox?**

CSS Grid organiza elementos en **columnas y filas simultáneamente**, mientras que *flexbox* trabaja en **un eje a la vez** (horizontal o vertical). La clave es el **contenedor padre**: al aplicar *display: grid*, se activa el modelo de layout y los hijos se distribuyen en celdas.

- Contenedor padre con *display: grid* activado.
- Ejes doble: columnas y filas al mismo tiempo.
- Control directo de proporciones con la unidad **fr**.

**Idea fuerza:** si buscas estructuras bidimensionales (p. ej., 2 columnas por varias filas), usa **grid**; si solo necesitas un eje, usa **flexbox**.

## **¿Cómo crear columnas con grid-template-columns y fracciones fr?**

La unidad **fr** es exclusiva de Grid: representa una **fracción del espacio disponible** del contenedor. Con *grid-template-columns* defines cuántas columnas y qué proporción ocupa cada una. Por ejemplo, `1fr 1fr` reparte el espacio en dos partes iguales; al añadir una tercera `1fr`, tendrás tres columnas. Con cuatro elementos, se forma un **grid dos por dos** automáticamente.

### **¿Cómo definir un grid dos por dos?**

```jsx
.grid.simple {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.item {
  background: #3498db;      /* azul del ejemplo */
  color: white;
  padding: 20px;
  text-align: center;
  margin: 3px;               /* visible, aunque con grid conviene usar gap */
}
```

- `1fr 1fr`: dos columnas del mismo tamaño.
- Cuatro `.item` generan dos filas, formando el 2×2.

### **¿Cómo ajustar proporciones con 1fr, 2fr y 1fr?**

```jsx
.grid.fraccion {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}
```

- La columna central ocupa el doble que las laterales.
- Si cambias `2fr` por `1fr`, tendrás tres columnas iguales.

## **¿Cómo manejar el espacio con gap y la función repeat?**

Para evitar repetir valores, la función *repeat()* simplifica la definición de columnas: `repeat(3, 1fr)` crea **tres columnas iguales**. Además, *gap* establece el **espacio entre columnas y filas** del grid sin modificar el tamaño interior de los elementos, a diferencia de *margin*.

```jsx
.grid.gap {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;  /* espacio entre columnas y filas */
}
```

- `repeat(3, 1fr)`: código más limpio y fácil de mantener.
- `gap: 20px`: separación clara entre celdas del grid.
- Recomendación práctica: si ya usas *grid*, preferir **gap** sobre *margin* para separar elementos.

## 19.**Grid Avanzado**

Aprende a dominar CSS Grid con tres técnicas clave que simplifican la maquetación: **grid areas**, **span** y **grid lines**. Con estos patrones podrás definir un *layout* completo, extender elementos por columnas o filas y posicionarlos con precisión, todo desde CSS, de forma clara y escalable.

## **¿Cómo crear un layout con grid areas en CSS?**

Con **grid-template-areas** defines un *template* visual del *layout* y con **grid-area** enlazas cada elemento. Así posicionas *header*, *sidebar*, *content* y *footer* sin cálculos complejos.

- **display: grid** activa el modelo de cuadrícula.
- **grid-template-areas** dibuja el *layout* con nombres de áreas.
- **grid-template-columns** define anchos (ej: 200px y 1fr).
- **gap** y **margin-bottom** mejoran la separación visual.
- **grid-area** enlaza cada bloque con su área del *template*.

### **¿Cómo declarar el template de áreas?**

```jsx
.grid-areas {
  display: grid;
  grid-template-areas:
    "header header"
    "sidebar content"
    "footer footer";
  grid-template-columns: 200px 1fr;
  gap: 10px;
  margin-bottom: 20px;
}

/* Estilos base compartidos */
header, .sidebar, .content, footer {
  padding: 20px;
  text-align: center;
  color: white;
}
```

### **¿Cómo linkear elementos con grid area?**

```jsx
header { grid-area: header; background: #2ECC71; }
.sidebar { grid-area: sidebar; background: #E74C3C; }
.content { grid-area: content; background: #3498DB; }
footer { grid-area: footer; background: purple; }
```

- **header** ocupa el 100% del ancho al repetirse en la fila: "header header".
- **sidebar** queda a la izquierda y **content** a la derecha.
- **footer** también ocupa el 100% con "footer footer".
- Verifica que los nombres de clases coincidan (ej: `.sidebar` y no `.bar`).

## **¿Cuándo usar span para extender columnas en grid?**

Cuando quieres que un ítem se extienda a través de varias columnas o filas consecutivas sin recalcular fracciones, usa **span**. Es directo y legible.

```jsx
.grid-span {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  margin-bottom: 20px;
}

/* Extender un elemento por 2 columnas */
.item--span-2 { grid-column: span 2; }
```

- **grid-column: span 2** extiende el elemento por dos columnas.
- Alternativa más simple que ajustar muchas fracciones con 1fr.
- Escalable para diseños con muchos elementos.

## **¿Qué son las grid lines y cómo posicionar por líneas?**

Las **grid lines** son las líneas delimitadoras de columnas y filas. En lugar de pensar en fracciones o *span*, defines desde qué línea hasta cuál colocar el elemento, tanto en columnas como en filas.

```jsx
.grid-lines {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  margin-bottom: 20px;
}

/* Posicionar por columnas: de la línea 1 a la 3 */
.box-1 {
  grid-column: 1 / 3;
  background: red;
}

/* Posicionar por filas: de la línea 1 a la 3 */
.box-2 {
  grid-row: 1 / 3;
  background: green;
}
```

- Las líneas se cuentan desde el borde izquierdo/arriba hacia la derecha/abajo.
- **grid-column: 1 / 3** ocupa desde la línea 1 hasta la 3 (dos columnas de ancho).
- **grid-row: 1 / 3** ocupa desde la línea 1 hasta la 3 (dos filas de alto).
- Útil cuando necesitas posiciones precisas sin depender de nombres de áreas o *span*.

## 20.**Media Queries**

Diseña interfaces que se ven bien en cualquier pantalla con **responsive design** en CSS. A partir de un enfoque **mobile first**, aprenderás a priorizar contenido, usar **flexbox** y configurar **media queries** con puntos de quiebre claros para tablet y desktop. Además, verás cómo ajustar tipografías con **rem** y controlar la visibilidad por dispositivo sin perder accesibilidad.

## **¿Qué es responsive design y por qué empezar con mobile first?**

El objetivo es evitar experiencias pobres: texto diminuto, necesidad de hacer zoom o scroll lateral y navegación confusa. **Mobile first** obliga a priorizar lo esencial en pantallas pequeñas y luego “crecer” el diseño conforme aumenta el espacio.

- **Responsive design**: adaptar la UI al dispositivo para una buena lectura y navegación.
- **Mobile first**: definir primero estilos base para móvil y escalar a tablet/desktop.
- **Viewport**: ancho visible que guía cuándo activar cambios con **media queries**.
- **Accesibilidad** con **rem**: tipografías que respetan ajustes del usuario.
- **Habilidades** trabajadas: configurar **flexbox**, definir puntos de quiebre con **min-width**, gestionar visibilidad con **display**, depurar con el inspector del navegador.

## **¿Cómo aplicar media queries con flexbox paso a paso?**

La estrategia es clara: estilos base para móvil y, con **media queries**, reacomodar layout y visibilidad según el tamaño del **viewport**. Se usan puntos de quiebre en 768 px para tablet y 1024 px para desktop.

### **¿Qué estilos base definen el modo mobile?**

- Contenedor en columna con separación y márgenes.
- Tarjetas con color de fondo, contraste y **padding**.
- Navegación vertical pensada para menú tipo hamburguesa.
- Secciones de visibilidad: mostrar “mobile” y ocultar “tablet” y “desktop”.
- Tipografías en **rem**: título y texto escalables.

```jsx
/* Base: mobile first */
.container {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
}

.box {
  background: #3498DB;
  color: white;
  padding: 20px;
  text-align: center;
}

.nav {
  background: #2c3e50;
  margin-bottom: 20px;
}

.nav-list {
  list-style: none;
  display: flex;
  flex-direction: column;
}

.nav-list a {
  display: block;
  color: white;
  padding: 10px;
  text-decoration: none;
}

/* Visibilidad por dispositivo */
.visibility { margin-bottom: 20px; }
.mobile { background: red; color: white; padding: 10px; }
.tablet { display: none; }
.desktop { display: none; }

/* Tipografía base */
.responsive.title { font-size: 1.5rem; }
.responsive.text { font-size: 1rem; }
```

### **¿Qué cambia en tablet con min-width: 768px?**

- Reacomodo a fila con **flex-direction: row**.
- Tarjetas que crecen con **flex: 1**.
- Menú horizontal para aprovechar el ancho.
- Mostrar contenedor “tablet” y ocultar “mobile”.
- Título más grande con **2rem**.

```jsx
@media (min-width: 768px) {
  .container { flex-direction: row; }
  .box { flex: 1; }
  .nav-list { flex-direction: row; }

  .mobile { display: none; }
  .tablet {
    display: block;
    background: #F39C12;
    color: white;
    padding: 10px;
  }

  .responsive.title { font-size: 2rem; }
}
```

### **¿Qué cambia en desktop con min-width: 1024px?**

- Ocultar “tablet” y mostrar “desktop”.
- Ajustar jerarquía tipográfica: título a **3rem** y texto a **1.2rem**.

```jsx
@media (min-width: 1024px) {
  .tablet { display: none; }
  .desktop {
    display: block;
    background: green;
    color: white;
    padding: 10px;
  }

  .responsive.title { font-size: 3rem; }
  .responsive.text { font-size: 1.2rem; }
}
```

## **¿Qué ajustes de tipografía y visibilidad mejoran la experiencia?**

El uso de **rem** permite que los tamaños de fuente se adapten al dispositivo y a las preferencias del usuario. Se definen escalas claras: **1.5rem** en móvil, **2rem** en tablet y **3rem** en desktop para el título; el texto pasa de **1rem** a **1.2rem** en desktop. La visibilidad se controla con **display: none/block** para mostrar solo el bloque pertinente a cada tamaño.

- **Tipografía responsive** con **rem** para accesibilidad.
- **Visibilidad** por dispositivo: .mobile, .tablet, .desktop.
- **Flexbox** para alternar entre columna y fila según espacio disponible.
- **Media queries** con **min-width** en 768 px y 1024 px.
- Prueba práctica: usar el inspector y observar el número del **viewport** al redimensionar.
- Depuración común: verificar clases si un estilo no aplica por un error tipográfico.

## 21.**Diseño Fluido**

El diseño fluido en CSS potencia el responsive design al hacer que el layout se adapte entre breakpoints. Con unidades relativas y funciones como porcentajes, *vw*, *vh*, *rem* y *clamp*, tu interfaz se mantiene flexible sin depender solo de media queries. Aquí verás cómo aplicar contenedores fluidos, *grid* adaptable, imágenes flexibles y tipografía responsiva.

## **¿Qué es diseño fluido y cómo complementa responsive design?**

El enfoque fluido asegura que el layout se ajuste continuamente mientras se acerca a un breakpoint. No todas las pantallas se resuelven con media queries. Por eso, se usan medidas relativas para que el contenido se **adapte al ancho y alto disponibles**.

- **Porcentajes**: ajustan tamaños según el contenedor padre.
- **Unidades de viewport**: *vw* para ancho, *vh* para alto. Ocupan un porcentaje de la pantalla.
- **rem**: escala con el tamaño de fuente base del documento.
- **Breakpoints**: cambian estilos en puntos clave, pero el fluido suaviza la transición.

La combinación de estas unidades con *flex* y *grid* permite que el contenido **fluya** y mantenga legibilidad en móviles, tablets y desktop.

## **¿Cómo crear un contenedor fluido con width, max-width y min-width?**

Un contenedor fluido usa porcentajes, límites mínimo y máximo, y centrado automático. Así controlas el crecimiento sin perder flexibilidad.

- **width: 90%**: ocupa el 90% del padre.
- **max-width: 1000px**: no crece más de 1000 px.
- **min-width: 320px**: no se hace menor que 320 px (ancho móvil pequeño).
- **margin: 0 auto**: centra el bloque cuando hay espacio sobrante.
- **padding** y **color de fondo**: mejoran la lectura.

```jsx
.fluid-container {
  width: 90%;
  max-width: 1000px;
  min-width: 320px;
  margin: 0 auto;
  padding: 20px;
  background: blue;
  color: white;
}
```

Claves prácticas: - Si el viewport baja de 320 px, aparece scroll horizontal. - Al superar 1000 px, el contenido queda centrado gracias a *margin: 0 auto*. - Entre 320 y 1000 px, el bloque usa siempre el **90% del contenedor padre**.

## **¿Cómo aplicar grid, imágenes y texto fluido con clamp?**

Para un layout flexible sin media queries, *grid* ofrece patrones adaptables y las imágenes y fuentes requieren reglas específicas para mantener foco y legibilidad.

### **¿Qué patrón de grid usar con repeat, auto-fit y minmax?**

Con *grid-template-columns* y *repeat(auto-fit, minmax())* logras columnas que se reacomodan según el espacio. El mínimo asegura legibilidad; el máximo reparte el espacio disponible con *1fr*.

```jsx
.fluids-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-bottom: 20px;
}
```

- **auto-fit**: ajusta el número de columnas según el ancho disponible.
- **minmax(250px, 1fr)**: cada tarjeta mide mínimo 250 px y crece equitativamente.
- **gap**: separa elementos y mejora el ritmo visual.

### **¿Cómo hacer una imagen flexible dentro de su contenedor?**

Primero, limita el contenedor con *max-width* y céntralo. Luego, haz que la caja de imagen ocupe el 100% del ancho y define una altura para que sea visible.

```jsx
.image-contained {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
}

.image-box {
  width: 100%;
  height: 200px;
  background: red;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

Buenas prácticas: - Define altura para evitar colapsos visuales. - Considera el encuadre: en headers, prioriza la **zona visible** relevante. - Si luego usas imágenes reales, combina con *object-fit* y *object-position* según el caso.

### **¿Cómo escalar tipografía con la función clamp?**

La función **clamp()** define un mínimo, un valor ideal relativo y un máximo. Así el texto crece suave con el viewport y se detiene donde conviene.

```jsx
.fluid-title {
  font-size: clamp(1.5rem, 4vw, 3rem);
  margin-bottom: 10px;
}
```

- Mínimo: 1.5rem para móviles.
- Ideal relativo: 4vw para crecer con el ancho.
- Máximo: 3rem para desktop grandes.

Ventajas clave: - **Legibilidad constante** sin saltos bruscos. - Una sola regla cubre móviles, tablets y desktop.

## 22.**Mobile First**

Diseñar sitios responsive exige decisiones claras: optimiza el performance desde mobile, prioriza el objetivo del usuario y ajusta el layout con CSS para una experiencia fluida en cualquier tamaño de pantalla. Aquí encontrarás prácticas concretas para mejorar usabilidad, navegación y legibilidad sin cargar de más.

## **¿Cómo optimizar el performance y el contenido prioritario en responsive?**

Empezar por mobile ayuda a no sobrecargar. Los dispositivos móviles no tienen la misma potencia de cómputo que *desktop*, así que conviene cargar solo lo esencial y sumar elementos conforme crece el espacio hacia tablet y *desktop*.

- Cargar solo lo esencial en *mobile*. Enfócate en lo que el usuario necesita ver y hacer primero.
- Priorizar el contenido. Define el objetivo clave y muéstralo sin distracciones.
- Aplicar mejoras progresivas. Agrega características según las capacidades reales de los dispositivos de tus usuarios.
- Ajustar por dispositivo. Comprende qué usan tus usuarios y adapta características que puedan soportar.

## **¿Qué patrones de navegación y hero mejoran la experiencia mobile?**

Cuando el espacio se compromete, la navegación debe simplificarse. La idea es reducir ruido visual y permitir acceso rápido a lo importante. Lo mismo ocurre con secciones visuales como el *hero*.

### **¿Cómo manejar la navegación progresiva?**

- Usar icono de hamburguesa cuando el espacio se reduce.
- Alternar visibilidad con CSS y *JavaScript*: `display: none` / `display: block`.
- Quitar “basura” visual en pantallas pequeñas y dejar solo lo necesario para interactuar.

### **¿Cómo adaptar el hero por tamaño de pantalla?**

- Cambiar el layout con *grid* o *flex* según el espacio disponible.
- Si en *mobile* la imagen del *hero* no aporta al objetivo, se puede omitir.
- Mantener siempre visible el contenido clave con el que el usuario interactúa.

## **¿Cómo adaptar cartas y formularios con CSS flexible?**

El contenido debe fluir y reacomodarse según el ancho. Las cartas y los formularios son grandes candidatos para layouts que cambian cuando hay espacio suficiente.

- Hacer contenido flexible. Reacomoda cartas según el tamaño y cambia el layout cuando el ancho lo permita.
- Formularios adaptables. En pantallas amplias pueden ir campos lado a lado; en *mobile*, conviene columna para evitar toques fallidos.
- Cuidar el espacio entre inputs. Aumenta márgenes y separaciones para mejorar la interacción táctil.

### **¿Qué tamaños y espaciados *touch* garantizan buena usabilidad?**

- Touch targets: área mínima de **44 x 44 px** para botones y elementos interactivos.
- Fuentes: mínimo de **6 px (1 rem)** para asegurar legibilidad.
- Saltos de línea: **1.6** de interlineado para lectura cómoda en bloques de texto extensos.

## 23.**Transformaciones**

Domina las transformaciones CSS con ejemplos claros y prácticos. Aprende a mover, rotar y escalar elementos con **translate**, **rotate** y **scale**, usando **hover** como *trigger* y **transition** para suavizar el cambio. Además, configura un layout flexible con **flexbox** para visualizar tus cajas en columnas con buen espaciado.

## **¿Cómo preparar el contenedor y los elementos con flex y estilos base?**

Antes de animar, conviene definir una base visual clara. Un *container* con *display: flex* permite alinear y separar elementos de forma sencilla. Cada *box* tendrá tamaño fijo, color de fondo y centrado de texto.

### **¿Qué propiedades dan estructura y espaciado?**

- Usa **display: flex** para organizar en columnas o filas.
- Aplica **gap: 30px** para separar elementos.
- Añade **margin-bottom: 40px** y **padding: 20px** para respirar.
- Define **background: #f0f0f0** para contraste suave.
- Crea *box* de **100px x 100px** con **background: #3498DD** y texto blanco.
- Centra contenido con **align-items: center** y **justify-content: center**.

```jsx
.container {
  display: flex;
  gap: 30px;
  margin-bottom: 40px;
  padding: 20px;
  background: #f0f0f0;
}

.box {
  width: 100px;
  height: 100px;
  background: #3498DD;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### **¿Cómo suavizar cambios con transition en transform?**

- Añade **transition: transform 0.3s** para evitar saltos bruscos.
- Mejora la percepción del movimiento y la interacción.

```jsx
.box {
  /* ...estilos previos... */
  transition: transform 0.3s;
}
```

## **¿Cómo mover elementos con translateX, translateY y en diagonal?**

**translate** desplaza un elemento desde su posición original sin afectar al resto del layout. El *trigger* será **:hover** para visualizar el movimiento al pasar el cursor.

### **¿Qué hace translateX y translateY en hover?**

- **translateX(30px)** mueve 30 píxeles en horizontal.
- **translateY(-30px)** mueve 30 píxeles hacia arriba con valor negativo.

```jsx
.translate-x:hover { transform: translateX(30px); }
.translate-y:hover { transform: translateY(-30px); }
```

- Con **transition**, el desplazamiento se ve **sutil** y fluido.
- Útil cuando quieres indicar interactividad sin reflow del documento.

### **¿Cómo mover en diagonal con translate?**

- Pasa dos valores: **x, y**.
- Un ejemplo común: **translate(20px, 20px)** para ir a la derecha y abajo.

```jsx
.translate-xy:hover { transform: translate(20px, 20px); }
```

- Recuerda: el *trigger* es **hover**, pero puedes usar otros según la interacción deseada.

## **¿Cómo rotar y escalar con rotate y scale?**

**rotate** gira el elemento desde su centro por defecto (puedes cambiarlo con *transform-origin*). **scale** modifica el tamaño relativo sin romper el flujo.

### **¿Cómo rotar desde el centro con rotate?**

- Define el ángulo en grados: **45deg**, **90deg**, **180deg**.

```jsx
.rotate-45:hover { transform: rotate(45deg); }
.rotate-90:hover { transform: rotate(90deg); }
.rotate-180:hover { transform: rotate(180deg); }
```

- El giro sucede sobre el centro si no especificas otro punto.
- Ideal para expresar estados o direcciones de forma visual.

### **¿Cómo reducir o ampliar con scale?**

- **scale(0.5)** reduce a la mitad.
- **scale(1.5)** aumenta 1.5 veces.
- **scale(2)** duplica el tamaño.

```jsx
.scale-small:hover { transform: scale(0.5); }
.scale-medium:hover { transform: scale(1.5); }
.scale-2x:hover { transform: scale(2); }
```

- Usa **transition: transform 0.3s** para evitar cambios bruscos.
- Aplica valores según el objetivo visual del diseño.

## 24.**Transiciones**

Las transiciones en CSS mejoran la experiencia visual: suavizan cambios de color, tamaño y posición sin brusquedades. Aquí verás cómo aplicar *transition* a botones y cajas, cómo combinar cambios con *transform* y cómo controlar la velocidad con *linear*, *ease* y *ease-in-out*. Además, se muestra un caso de depuración frecuente con la cascada y múltiples *transform*.

## **¿Por qué usar transiciones en CSS?**

Las transiciones hacen que los cambios se sientan **suaves y naturales**. Evitan saltos abruptos al pasar el *hover* y aportan claridad visual.

- **Suavizar color de fondo** con *background-color* en 0.3s.
- **Escalar elementos** con *transform: scale* para dar feedback.
- **Mover en el eje X** con *translateX* y controlar el tiempo.
- **Acompañar el movimiento** con *box-shadow* para dar profundidad.

### **¿Qué estilos base necesitas en los botones?**

Primero se definen estilos base para separación y legibilidad. Usa *display: flex*, *gap* y *margin-bottom*.

```jsx
/* Contenedor de botones */
.buttons {
  display: flex;
  gap: 12px;
  margin-bottom: 40px;
}

/* Botón base */
.button {
  padding: 12px 24px;
  font-size: 16px; /* o 1rem */
  cursor: pointer;
  background: #3498DB;
  color: #fff;
  border: 0;
}
```

## **¿Cómo aplicar transiciones en botones con hover?**

La clave está en declarar la propiedad a animar, la duración y la función de aceleración. Así, el cambio no se ve brusco.

### **¿Cómo suavizar el cambio de color?**

Para que el color de fondo cambie de forma fluida con *hover*, anima *background-color*.

```jsx
/* Transición del color de fondo */
.button-color {
  transition: background-color 0.3s ease;
}
.button-color:hover {
  background-color: #E74C3C; /* rojo suave */
}
```

### **¿Cómo hacer que el botón crezca?**

Si buscas un efecto de crecimiento, anima *transform* con *scale*.

```jsx
/* Transición de tamaño */
.button-size {
  transition: transform 0.3s ease;
}
.button-size:hover {
  transform: scale(1.1);
}
```

### **¿Cómo combinar color, sombra y escala en un botón?**

Cuando un mismo elemento cambia varias propiedades, puedes usar `all` para cubrirlas. Evita declarar múltiples *transform* separados.

```jsx
/* Botón con varios cambios al hover */
.button-all {
  transition: all 0.3s ease;
}
.button-all:hover {
  background-color: #2ECC71; /* verde */
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
  transform: scale(1.1); /* se decidió escalar y no trasladar */
}
```

### **¿Cómo depurar conflictos con transform y la cascada?**

- No declares dos reglas de *transform* en el mismo selector al mismo tiempo: una pisará a la otra.
- Si necesitas combinar, usa un solo *transform*: por ejemplo, `transform: translateY(-5px) scale(1.1);`.
- Usa las herramientas del navegador: fuerza el *hover* en el inspector y revisa qué reglas están activas.

## **¿Cómo controlar el timing con linear, ease y ease-in-out?**

El tiempo y la aceleración definen la sensación del movimiento. Con *transform* y *transition* puedes mover una caja 200px a la derecha y ver cómo varía la velocidad según *linear*, *ease* y *ease-in-out*.

```jsx
/* Contenedor de ejemplos de timing */
.timing-container {
  display: flex;
  gap: 20px;
  margin-bottom: 40px;
}

/* Caja base */
.box {
  width: 100px;
  height: 100px;
  background: #9B59B6; /* morado */
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

/* Variantes de timing */
.timing-linear { transition: transform 1s linear; }
.timing-ease { transition: transform 1s ease; }
.timing-ease-in-out { transition: transform 1s ease-in-out; }

/* Disparador común */
.box:hover { transform: translateX(200px); }
```

- *linear*: velocidad uniforme todo el tiempo.
- *ease*: aceleración natural, empieza lento y acelera.
- *ease-in-out*: suave al inicio y al final, rápido en medio.

Consejos rápidos: - Define claramente la propiedad: *background-color* o *transform*, según el efecto. - Ajusta la duración: 0.3s para *hover* en UI se siente fluido. - Usa *box-shadow* para reforzar la sensación de elevación. - Evita conflictos: un único *transform* por selector al final de la cascada.

## 25.**Transiciones aplicadas**

Aplicar transiciones en CSS a una card puede cambiar por completo la experiencia: con *hover*, *transform* y *box-shadow* bien configurados, logras microinteracciones limpias, rápidas y consistentes. Aquí verás cómo se definen los estilos base, cómo se anima la tarjeta y cómo el contenido responde con un pequeño *delay* para reforzar la jerarquía visual.

## **¿Cómo crear una card con transiciones CSS consistentes?**

Para una base sólida se define un contenedor con ancho fijo, espaciado interno y bordes suaves. Lo clave: una **transición uniforme** para todas las propiedades que cambiarán, manteniendo la misma duración y *timing function* para que se sienta natural.

```jsx
.card {
  width: 300px;
  padding: 30px;
  background: white;
  border: 2px solid #ecf0f1; /* gris claro */
  border-radius: 10px;
  cursor: pointer;
  transition: transform .3s ease, box-shadow .3s ease, border-color .3s ease;
}
```

- **width: 300px** para controlar la composición.
- **padding: 30px** para espacio interno legible.
- **border: 2px** y **border-radius: 10px** para un contorno suave.
- **transition de .3s** en *transform*, *box-shadow* y *border-color* para coherencia.

### **¿Qué conceptos aplicas al definir la base?**

- Uso de *cursor: pointer* para indicar interactividad.
- Transición con *ease* para un movimiento suave.
- Separación de propiedades en la *transition* para claridad y control.

## **¿Qué efectos aplicar con hover para mejorar la interacción?**

Al pasar el puntero, la tarjeta se **eleva** con *translate*, gana **profundidad** con *box-shadow* y refuerza el foco con el cambio de **color del borde** a azul. Todo a la misma velocidad para evitar desajustes visuales.

```jsx
.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, .2);
  border-color: #3498db;
}
```

- *transform: translateY(-10px)* para elevar la tarjeta.
- *box-shadow: 0 10px 30px rgba(0,0,0,.2)* para profundidad.
- *border-color* azul para contraste y foco.

### **¿Por qué mantener la misma duración en transition?**

- Asegura una **percepción fluida** del cambio.
- Evita saltos entre propiedades que distraen.
- Refuerza la **consistencia** del movimiento.

## **¿Cómo estilizar el contenido: títulos y párrafos con transición?**

El contenido interno también comunica. El título cambia de color al *hover* y el párrafo se desplaza con un **pequeño delay** para entrar en escena después de la tarjeta.

```jsx
.card h3 {
  color: #2c3e50; /* gris oscuro */
  margin-bottom: 10px;
  transition: color .3s ease;
}

.card h3:hover {
  color: #3498db;
}

.card p {
  color: #7f8c8d; /* gris */
  transition: transform .3s ease .1s; /* delay de 0.1s */
}

.card:hover p {
  transform: translateX(10px);
}
```

- **H3** con color #2c3e50 y margen inferior de 10px para separación.
- *transition: color .3s ease* en el título para un cambio suave.
- Párrafo con *transition* en *transform* y **delay de 0.1s** para entrar después.
- *translateX(10px)* en el texto al *hover* de la card, no del párrafo: se activa desde el contenedor.

### **¿Qué habilidades y keywords refuerzas aquí?**

- Manejo de **transiciones CSS**: *transition*, duración y *timing function*.
- **Transformaciones** con *translate* en ejes X/Y.
- **Sombras** con *box-shadow* y opacidad *RGBA*.
- **Estados interactivos** con *hover* en contenedor y en elementos internos.
- **Jerarquía temporal** con *delay* para escalonar animaciones.

## 26.**Animaciones**

Las animaciones en *CSS* permiten mover, escalar y rotar elementos sin depender de un *trigger* como *hover*. Aquí verás cómo programarlas con *keyframes*, aplicar *transform* y controlar duración, curva de tiempo y repetición, incluyendo un *spinner* de *loading* listo para usar.

## **¿Cómo funcionan las animaciones en CSS y en qué se diferencian de las transiciones?**

A diferencia de las transiciones, que necesitan un *trigger* (por ejemplo, *hover*), las animaciones se ejecutan por sí mismas al declararlas con *keyframes* y aplicarlas con la propiedad *animation*. No hay eventos adicionales: el ciclo inicia y se repite según lo configurado.

- **@keyframes** define estados en 0 %, intermedios y 100 %.
- **animation** controla nombre, duración, curva de tiempo y repetición.
- **transform** aplica efectos como **scale**, **rotate** y **translateY**.
- **Timing functions**: *ease-in-out* suaviza inicio y final; *linear* mantiene velocidad constante.
- **Repetición**: *infinite* mantiene la animación corriendo sin parar.
- Asegúrate de escribir **keyframes en plural**: evita errores de sintaxis.

## **¿Cómo implementar animaciones pulse, rotate y bounce con keyframes?**

Antes de animar, se define un estilo base del contenedor .box: tamaño, color y centrado del contenido con *flex* para ver claramente los efectos.

```jsx
.box {
  width: 100px;
  height: 100px;
  background: #3498DB;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 20px;
  border-radius: 10px;
}
```

### **¿Cómo crear un efecto pulse con transform: scale?**

El elemento crece al 50 % del tiempo y vuelve a su tamaño original.

```jsx
@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.2); }
  100% { transform: scale(1); }
}

.box.pulse {
  animation: pulse 2s ease-in-out infinite;
}
```

- **scale(1.2)**: aumento aproximado del 20 % del tamaño.
- **ease-in-out**: entrada y salida suaves.
- **infinite**: se repite continuamente.

### **¿Cómo rotar con rotate en una animación continua?**

Gira 360 grados y repite sin fin con una velocidad constante.

```jsx
@keyframes rotate {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

.box.rotate {
  animation: rotate 3s linear infinite;
}
```

- **linear**: velocidad uniforme durante todo el ciclo.
- **360deg**: vuelta completa.

### **¿Cómo simular un rebote con translateY?**

Usa varios *frames* para subir y bajar en pasos decrecientes.

```jsx
@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  25% { transform: translateY(-30px); }
  50% { transform: translateY(-15px); }
  75% { transform: translateY(-5px); }
}

.box.bounce {
  animation: bounce 2s ease infinite;
}
```

- Secuencia con 0 %, 25 %, 50 %, 75 % y 100 %.
- **translateY negativo**: simula la subida del salto.
- **Pasos decrecientes**: sensación de amortiguación.

## **¿Cómo crear un spinner de loading solo con CSS?**

Un anillo con borde superior coloreado que rota de forma continua. Ideal para indicar carga hasta que con *JavaScript* ocultes el *spinner* y muestres el contenido.

```jsx
.spinner {
  width: 50px;
  height: 50px;
  border: 5px solid #f3f3f3;
  border-top: 5px solid #3498DB;
  border-radius: 50%;
  margin: 20px;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

- **border-top** coloreado: crea el efecto de giro visible.
- **1s linear infinite**: giro constante y fluido.
- **50% de border-radius**: círculo perfecto.