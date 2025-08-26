# Curso de API REST con Javascript: Fundamentos

- **Qué es una API REST y cómo funciona con JavaScript**
    
    Aprender a consumir **API REST con JavaScript** te permite conectar aplicaciones web modernas de manera profesional. En el entorno web, JavaScript en el frontend cumple dos funciones principales: interactúa con el usuario y comunica el frontend con el backend. De este modo, se convierte en un puente indispensable para acceder a datos y responder eficazmente a las consultas de quienes usan la aplicación.
    
    ### **¿Cuáles son los requisitos clave para consumir API REST con JavaScript?**
    
    Antes de profundizar, necesitas dominar conceptos y tecnologías esenciales:
    
    - Conocimientos sólidos en **HTML y CSS** para manipular el DOM de forma efectiva.
    - Comprensión sobre cómo funciona el *JS Engine* (el motor interno de JavaScript), abordado en el curso específico de *JS Engine, V8 y el navegador*.
    - Dominio de **asincronismo en JavaScript**, incluyendo *callbacks*, *promesas*, *async/await*, y experiencia previa usando *XMLHttpRequest* y *Fetch* para hacer solicitudes asíncronas.
    
    Si tienes dudas sobre tu nivel de preparación, lo ideal es seguir la ruta de la escuela de desarrollo web y avanzar paso a paso hasta que se indique abordar consumo de API REST.
    
    ### **¿Qué es una API REST y para qué se usa en JavaScript?**
    
    **API** significa *Application Program Interface*, o sea, interfaz para interactuar con un sistema: en la web, las interfaces permiten que usuarios o robots se comuniquen fácilmente. Así como controlas funciones en un coche mediante una pantalla, en el frontend creamos interfaces que permiten a las personas comunicarse con robots (los programas) pulsando botones o enviando formularios sin necesidad de escribir código.
    
    Ahora bien, **API REST** es una interfaz enfocada no en la comunicación entre usuario y robot, sino en la de **robot con robot**: por ejemplo, entre el frontend y el backend, o incluso entre varios backends. REST significa *Representational State Transfer*, lo cual indica que la comunicación ocurre a través de HTTP (el mismo protocolo utilizado cuando navegas una página web).
    
    La diferencia clave frente a visitar una web tradicional es que con una API REST recibes respuestas directas en **formato JSON**, y no HTML. Así, el backend te entrega datos, y tú los muestras usando imágenes, formularios u otros elementos visuales según lo requiera la aplicación.
    
    ### **¿Qué protocolos existen y por qué usar REST y JSON?**
    
    Históricamente existieron otros protocolos de comunicación como **SOAP** (utilizaba XML), aún presente en aplicaciones antiguas. Sin embargo, REST y JSON han ganado protagonismo en el desarrollo moderno por su sencillez y flexibilidad.
    
    Para quienes inician, enfocarse en REST y JSON facilita el aprendizaje y la integración con la mayoría de servicios actuales, pues casi todas las aplicaciones nuevas adoptan estos estándares.
    
- **Flujo de comunicación entre front-end y back-end en aplicaciones web**
    
    Comprender **la interacción entre usuarios, front-end y back-end** es vital para desarrollar aplicaciones web modernas. El flujo de datos y el papel de tecnologías como JavaScript y APIs REST definen la experiencia del usuario y la eficiencia de la app.
    
    ### **¿Qué sucede cuando un usuario interactúa con una página web?**
    
    Cada vez que ingresas a una página como Platzi o YouTube, el proceso inicia en tu navegador (Google Chrome, Firefox, Safari, etc.). Escribes una URL (como platzi.com) y esto se transforma en una **solicitud dirigida al back-end**. El back-end, muchas veces invisible para el usuario, corresponde al servidor de la app, encargado de gestionar las peticiones.
    
    - El navegador actúa como intermediario entre el usuario y el servidor.
    - El usuario no recibe directamente la información, sino a través del flujo navegador-servidor-navegador.
    - La respuesta estándar del back-end suele ser en **HTML**, permitiendo visualizar imágenes y textos.
    
    ### **¿Qué es el server-side rendering y cómo influye en la experiencia de usuario?**
    
    El **server-side rendering** consiste en que cada vez que navegas entre páginas ( por ejemplo, de la página principal al blog), el navegador realiza otra petición al servidor, que responde con un nuevo HTML para cada vista.
    
    - Cada clic suele recargar la página completa desde cero.
    - Imágenes, CSS y otros recursos se cargan cada vez.
    - Este proceso puede hacer que la experiencia sea más lenta, especialmente en sitios grandes.
    
    ### **¿Por qué JavaScript y las single-page applications mejoran la navegación?**
    
    Gracias a **JavaScript**, surgieron las **single-page applications (SPA)**. JavaScript permite manipular el contenido visual (*DOM*) sin recargar todo desde el servidor.
    
    - JavaScript escucha acciones del usuario como clics, scroll o escritura en formularios.
    - Estas acciones pueden detonar solicitudes a **APIs** sin refrescar la página.
    - En vez de pedir un HTML completo, el navegador consulta la API (usando formatos como JSON) y actualiza solo la parte necesaria en la vista.
    - Esto hace que la aplicación *parezca* mucho más veloz al usuario.
    
    ### **¿Cómo se comunican el front-end y el back-end usando APIs?**
    
    En este modelo, el front-end (gracias a JavaScript) accede a **APIs del back-end** (por ejemplo api.platzi.com) para intercambiar información.
    
    - El usuario realiza una acción: JavaScript lo detecta.
    - JavaScript consulta la API REST del back-end.
    - El back-end responde, generalmente en formato **JSON**.
    - JavaScript actualiza el HTML para mostrar la nueva información, sin recargar la página completa.
    
    ### **¿Qué rol juegan las bases de datos en este flujo?**
    
    El **back-end** se apoya en **bases de datos** como MySQL, PostgreSQL o MongoDB para **persistir información**. De este modo:
    
    - Si un usuario crea o modifica contenido (comentarios, videos, etc.), esa información se guarda en la base de datos, no solo en el navegador.
    - Cuando se consulta información (como detalles de un curso), el back-end la extrae de la base de datos antes de devolverla al front-end.
    - Así, los cambios son accesibles para todos los usuarios presentes y futuros.
    
    ### **¿Por qué la comunicación entre usuario, front-end y back-end es más compleja de lo que parece?**
    
    La interacción no se limita a simples consultas y respuestas. El front-end traduce lo que hace el usuario en solicitudes precisas al back-end y, gracias a JavaScript y las APIs, solo se actualizan partes del contenido necesarias para la tarea en curso.
    
    ![](https://static.platzi.com/media/user_upload/flujo-ddef2aa7-0d4f-48b0-9da4-d90fcef9fa9d.jpg)
    
- **Consumo de APIs REST públicas con JavaScript y fetch**
    
    Aprender a consumir una **API REST** pública es una excelente práctica para quienes buscan dominar el desarrollo web moderno. Aquí verás cómo encontrar, elegir y consumir fácilmente una API gratuita desde GitHub, crear un pequeño proyecto de imágenes aleatorias de gatos y algunos consejos prácticos para manejar autenticación y evitar errores comunes como CORS.
    
    ### **¿Dónde encontrar APIs públicas gratuitas y seguras?**
    
    Para practicar el consumo de APIs, puedes buscar en *GitHub* el repositorio llamado *Public APIs*. Allí verás una colección de APIs organizadas por categorías (animales, arte, anime, blockchain y más). Estas APIs pueden ser utilizadas libremente, lo cual resulta perfecto para practicar y crear proyectos para tu portafolio.
    
    El repositorio muestra un índice donde cada API contiene información relevante como: - **CORS**: Indica si la API puede ser consumida fácilmente desde el navegador. Elige APIs sin CORS al empezar para evitar problemas de acceso. - **HTTPS**: Ofrece mayor seguridad en la transmisión de datos. Prioriza las APIs que lo incluyan. - **Método de autenticación**: Algunas APIs requieren *API key*, otras funcionan sin autenticación y algunas usan métodos avanzados como OAuth. Para comenzar, resulta más práctico elegir APIs que no usen OAuth.
    
    ### **¿Qué es la TheCat API y cómo se usa?**
    
    Entre las opciones para practicar, destaca *TheCat API*. Es gratuita hasta 10 000 solicitudes al mes y requiere solo una *API key*, permitiendo cargar imágenes de gatos aleatorios. Su documentación es clara e incluye rutas, ejemplos y descripciones para empezar rápido.
    
    En la sección de *quickstart*, la API ofrece una URL específica. Al hacer una petición a este endpoint, se recibe un array con un solo objeto que contiene, entre otras propiedades, la *url* de la imagen de un gato. Así puedes implementarla para mostrar imágenes aleatorias en tus proyectos.
    
    ### **¿Cómo integrar una API de imágenes en tu proyecto HTML y JavaScript?**
    
    1. **Estructura tu proyecto:**
    2. Crea una carpeta de trabajo, un archivo `index.html` y un archivo de JavaScript, por ejemplo `main.js`.
    3. Prepara HTML básico: incluye un título y un elemento `img` (con solo el atributo `alt`).
    4. **Conecta JavaScript:**
    5. Enlaza `main.js` dentro del HTML mediante una etiqueta `script` al final del body.
    6. Inicializa con un `console.log("Hello world!")` para comprobar la conexión.
    7. **Consulta a la API:**
    8. Define la URL del endpoint de *TheCat API*: `https://api.thecatapi.com/v1/images/search`.
    9. Usa `fetch` para realizar la petición; trabaja con promesas para transformar la respuesta usando `res.json()`.
    10. Accede a la propiedad `url` del primer elemento del array devuelto y asígnala como atributo `src` del elemento `img` en el DOM.
    
    ### **¿Cómo facilitar la lectura de respuestas JSON en el navegador?**
    
    Las respuestas de APIs REST suelen ser en formato JSON. Puedes instalar extensiones como *JSON Viewer* en navegadores como Google Chrome para visualizar mejor las estructuras, con tabulación, colores y encabezados que ordenan la información.
    
    Esto es útil, especialmente si necesitas explorar APIs con respuestas más extensas o complejas.
    
    ### **¿Qué retos prácticos ayudan a mejorar la integración de APIs?**
    
    Como parte del aprendizaje, se recomiendan dos retos basados en el ejemplo de imágenes de gatos: - **Reto 1:** Agrega un botón al HTML que permita cargar una nueva imagen aleatoria al hacer clic, sin recargar la página. Para ello, enlaza el evento del botón a la función que ejecuta el `fetch`. - **Reto 2:** Implementa la lógica usando *async/await* en vez de la sintaxis clásica de promesas con `then`, para practicar diferentes formas de manejar código asíncrono.
    
    ## Recursos
    
    https://github.com/public-apis/public-apis
    
    https://devhints.io/js-fetch
    
    https://developers.thecatapi.com/view-account/ylX4blBYT9FaoVd6OhvR?report=bOoHBz-8t
    
    https://github.com/platzi/consumo-api-rest-javascript/tree/6df9523904b7128bb58a0cddce4f4cea9bf08272
    
- **Endpoints y query parameters en APIs REST con JavaScript**
    
    Aprender a consumir APIs de forma eficiente es fundamental para cualquier persona interesada en el desarrollo web. Al comprender el uso de **endpoints** y **query parameters**, podemos acceder a datos exactos, optimizar el rendimiento de nuestras aplicaciones y brindar mejores experiencias. Aquí respondemos a las dudas más comunes sobre este proceso y mostramos cómo aplicar estos conceptos usando JavaScript moderno.
    
    ### **¿Qué son endpoints y por qué son importantes en una API?**
    
    Los **endpoints** son rutas o URLs específicas de una API. Cada endpoint nos permite acceder a diferentes recursos disponibles en el backend, evitando así solicitar toda la base de datos en cada llamada. De esta manera, una API puede segmentar su información, facilitando que solo obtengamos lo necesario; por ejemplo, categorías de razas o imágenes específicas de gatitos.
    
    - Permiten modularizar la información.
    - Ayudan a optimizar las solicitudes y el uso de recursos.
    - Cada recurso de la API suele tener su propio endpoint.
    
    Es fundamental consultar la **documentación** de la API para conocer las rutas disponibles y acceder solo a los datos relevantes para nuestro proyecto.
    
    ### **¿Cómo funcionan los query parameters para filtrar o limitar la información?**
    
    Los **query parameters** agregan información extra al endpoint para poder **filtrar o limitar** el contenido solicitado. Estos parámetros aparecen en la URL después de un símbolo de pregunta (`?`) y suelen tener la forma `clave=valor`. Podemos incluir varios parámetros separados por el símbolo `&`.
    
    - Permiten restringir resultados (por ejemplo, limitar el número de elementos mostrados).
    - Son útiles para filtrar datos según ciertos criterios (categoría, tipo de archivo, etc.).
    - Facilitan la paginación, evitando recibir demasiada información de una sola vez.
    
    Ejemplo práctico:
    
    ```jsx
    images/search?limit=3&page=2
    ```
    
    Esto solicita la segunda página de resultados, mostrando solo tres imágenes en total.
    
    ### **¿Cómo integrar endpoints y query parameters en proyectos JavaScript usando async/await?**
    
    Para aprovechar endpoints y query parameters desde JavaScript, se recomienda utilizar la sintaxis `async/await` para escribir código más claro y mantener la lógica controlada. Aquí el procedimiento, según el caso presentado:
    
    1. **Crear un botón** en HTML para recargar y mostrar una imagen aleatoria sin recargar toda la página:
    
    ```jsx
    <button onclick="reload()">Recargar</button>
    ```
    
    1. **Definir la función asíncrona** en JavaScript y renombrar correctamente las URLs para mayor claridad:
    
    ```jsx
    const API_URL = 'https://api.example.com/images/search?limit=3';
    async function reload() {
      const res = await fetch(API_URL);
      const data = await res.json();
      // Lógica para mostrar imágenes
    }
    ```
    
    1. **Llamar a la función** tanto al cargar el archivo JavaScript como al hacer clic en el botón para garantizar que siempre se muestren imágenes iniciales.
    2. **Modificar el tamaño de las imágenes** estableciendo un ancho fijo en las etiquetas `<img width="150">`.
    3. **Usar los IDs correctos** para cada imagen y actualizar el atributo `src`:
    
    ```jsx
    document.getElementById('imagen1').src = data[0].url;
    document.getElementById('imagen2').src = data[1].url;
    document.getElementById('imagen3').src = data[2].url;
    ```
    
    ### **¿Por qué es clave revisar la documentación de una API?**
    
    La **documentación** explica los endpoints disponibles y los query parameters soportados. Además, advierte sobre las necesidades de autenticación usando *API keys* y muestra ejemplos claros para consumir correctamente los recursos. Siempre es recomendable revisarla antes de programar para evitar errores y aprovechar al máximo las funcionalidades de la API.
    
- **¿Qué son los HTTP Status Codes?**
    
    ### **¿Qué son los HTTP Status Codes y por qué son importantes?**
    
    Los HTTP Status Codes son cruciales en el ciclo de vida de una solicitud en la web. Actúan como indicadores que nos proporcionan información sobre el estado de nuestra solicitud al servidor. Es fundamental entenderlos para reaccionar adecuadamente ante posibles errores y comunicar eficientemente a los usuarios qué está ocurriendo con sus peticiones.
    
    Los HTTP Status Codes se estructuran en rangos que indican el tipo de respuesta que se está recibiendo.
    
    ### **¿Qué significan los códigos de estado HTTP en la centena de los 200?**
    
    Los códigos HTTP en la centena de los 200 significan que todo está funcionando correctamente entre el frontend y el backend.
    
    - **200 (OK):** La solicitud se ha completado con éxito.
    - **201 (Created):** Se ha creado un recurso nuevo correctamente.
    - **202 (Accepted):** La solicitud ha sido aceptada para procesamiento, pero aún no se ha completado.
    
    Estos códigos proporcionan especificidad sobre el tipo de éxito obtenido, lo cual es esencial para una comunicación efectiva entre el cliente y el servidor.
    
    ### **¿Qué indican los códigos de estado HTTP en la centena de los 300?**
    
    Estos códigos están relacionados con el redireccionamiento. Nos indican que la solicitud actual no es la definitiva y que el backend sugiere una ruta diferente.
    
    - **307 (Temporary Redirect):** La ruta de redirección es temporal. Puede cambiar en el futuro.
    - **308 (Permanent Redirect):** La redirección es permanente. La URL a la que intentas acceder se ha movido permanentemente a otra dirección.
    
    Estas notificaciones son esenciales para la gestión de rutas y el acceso correcto a los recursos.
    
    ### **¿Qué sucede cuando encontramos códigos de estado HTTP en la centena de los 400?**
    
    Los códigos en el rango de los 400 indican errores causados por el frontend o por la solicitud enviada al servidor.
    
    - **400 (Bad Request):** Hay un error en la solicitud, como un typo o una sintaxis incorrecta.
    - **401 (Unauthorized):** Se requiere autenticación para acceder a la ruta solicitada.
    - **402 (Payment Required):** Es necesario realizar un pago para poder acceder a un recurso.
    - **404 (Not Found):** La ruta o recurso solicitado no existe.
    
    Entender estos códigos ayuda a depurar errores y a guiar mejor al usuario a corregir sus acciones.
    
    ### **¿Qué implican los códigos de estado HTTP en la centena de los 500?**
    
    Este rango de códigos indica errores del servidor, donde el backend ha tenido un fallo interno.
    
    - **500 (Internal Server Error):** Error genérico del backend, sin especificaciones.
    
    Los errores 500 frecuentemente requieren que el backend sea revisado por los desarrolladores, ya que el frontend no tiene la capacidad de resolverlos.
    
    ### **¿Por qué es importante conocer tanto el frontend como el backend?**
    
    Es crítico para los desarrolladores conocer cómo funcionan ambos aspectos del desarrollo web para mejorar la comunicación y la integración entre ellos.
    
    - **Desarrolladores Frontend:** Deberían tener un conocimiento básico del backend para comprender cómo se entrega la información a la interfaz de usuario.
    - **Desarrolladores Backend:** Necesitan entender cómo su trabajo impacta en la experiencia del usuario para crear soluciones más eficientes.
    
    El conocimiento integral del ciclo de solicitud-respuesta ayuda a proporcionar una experiencia de usuario más fluida y efectiva. Además, conocer los fundamentos del otro terreno facilita una mejor resolución de problemas y optimización.
    
    https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status
    
    https://httpstatusdogs.com/
    
- **Diferencia entre autenticación y autorización con API keys**
    
    La autenticación y la autorización son dos pilares fundamentales para la **seguridad y gestión de accesos en aplicaciones web**. Existen términos y procesos que muchas veces se confunden, pero entender su diferencia es clave para proteger información y garantizar un desarrollo profesional. Aquí encontrarás detalles esenciales y prácticos aplicados al trabajo con *API keys* en el backend.
    
    ### **¿Qué diferencia hay entre autenticación y autorización en la seguridad de una API?**
    
    La **autenticación** se ocupa de identificar quién realiza una solicitud al sistema. Por ejemplo, si alguien se presenta como "fulano", la autenticación sólo verifica si realmente lo es, pero no determina lo que puede hacer.
    
    Por su parte, la **autorización** analiza los permisos: decide si ese usuario que ya fue autenticado puede acceder a información específica, ejecutar acciones o modificar recursos. Así, aunque "fulano" esté identificado, no necesariamente podrá ver o modificar elementos como las fotos privadas de otra persona.
    
    Estas dos funciones trabajan juntas constantemente para proteger datos y restringir el acceso a recursos sensibles o limitados.
    
    ### **¿Cómo ayudan las API keys al backend a identificar solicitudes y proteger datos?**
    
    Las **API keys** son una de las herramientas que utiliza el backend para conocer quién está enviando cada petición. Así protege recursos y, además, puede limitar el número de solicitudes mensuales por usuario o aplicación.
    
    Por ejemplo, una API puede fijar un límite de diez mil solicitudes al mes. Si se excede, el sistema impide nuevas peticiones, alentando a cambiar de plan si se requiere más capacidad.
    
    Cada proyecto o usuario tiene su propia API key, lo que facilita rastrear cuántas solicitudes provienen de cada uno y restringe el acceso a rutas protegidas por la API.
    
    ### **¿Cuáles son las formas recomendadas de enviar una API key al backend?**
    
    Existen varias formas prácticas para enviar la **API key** en una solicitud:
    
    - Mediante un *query parameter*, agregando por ejemplo `?api_key=TU_API_KEY` a la URL.
    - A través de un *authorization header*, un método más cómodo y seguro que será abordado en módulos posteriores.
    
    El uso de *query parameters* resulta útil y sencillo para experimentar, aunque para entornos de producción se prefieren los *headers*.
    
    ### **¿Cuáles son otros métodos modernos de autenticación y autorización en aplicaciones?**
    
    Además de las API keys, existen métodos como:
    
    - *Authorization Basic*
    - *Bearer Token*
    - *OAuth 2.0*, reconocida por su mayor seguridad y complejidad
    - Combinación de *access key* y *secret key*
    
    Frameworks como Firebase gestionan procesos sofisticados para combinar autenticación y permisos, útil si tu aplicación maneja tanto autenticación basada en la aplicación como autenticación basada en usuarios.
    
    ### **¿Cómo obtener tu API key para comenzar a autenticar solicitudes?**
    
    Para probar la autenticación **application-based**:
    
    1. Accede a la sección de autenticación en la documentación de la API.
    2. Localiza las instrucciones para solicitar tu API key.
    3. Completa el formulario con un email válido y una breve descripción de tu proyecto.
    4. Confirma tu correo electrónico mediante el enlace recibido.
    5. Obtén y copia tu API key.
    
    Coloca la API key en cada petición (por ejemplo, como `?api_key=TU_API_KEY`). Así la API reconocerá tu identidad y permitirá el número de solicitudes correspondiente a tu cuenta.
    
    ### **¿Por qué considerar una autenticación combinada para frontend y usuarios?**
    
    Algunas aplicaciones deben identificar tanto al frontend (la aplicación) como a usuarios finales individuales. En estos casos se requiere una combinación de **application-based authentication** y **user-based authentication**, lo cual agrega seguridad y flexibilidad pero también complejidad al manejo de accesos y permisos.
    
- **Estructura HTML para mostrar gatos aleatorios y favoritos**
    
    Preparar una estructura HTML clara es esencial cuando trabajas con una API como *The Cat API*. Una base organizada permite aprovechar todas las opciones de interacción: mostrar gatos aleatorios, gestionar favoritos y subir tus propias fotos. Aquí aprenderás cómo planificar y organizar tu HTML para hacer tu proyecto funcional y listo para futuras mejoras.
    
    ### **¿Cómo crear secciones HTML para imágenes aleatorias y favoritos?**
    
    Separar el contenido en secciones visibles trae orden y claridad. Primero, se sugiere crear una sección específica para mostrar imágenes aleatorias de gatos, con un título que identifique la funcionalidad (por ejemplo, *random michis*). Utilizar IDs en los elementos (como imágenes o botones) te facilita conectar la lógica de JavaScript más adelante.
    
    Luego, se construye una segunda sección dedicada a los favoritos. Aquí se pueden reutilizar estructuras similares para mostrar imágenes seleccionadas por el usuario. Es importante que esta sección empiece vacía y solo se llene cuando existan favoritos almacenados. Además, puedes nombrar títulos o secciones en español o inglés, confirmando términos como *favorites* para una mejor organización y consistencia internacional.
    
    ### **¿Cómo debe estructurarse cada elemento de imagen y sus botones?**
    
    Cada imagen se recomienda incluirla dentro de un *article* (o un *div*, dependiendo de tus preferencias o necesidades de accesibilidad). Dentro de cada *article*, añade la imagen de gato y un botón que permita guardar o quitar de favoritos según la ubicación. Los botones deben tener un texto claro (como "guardar michi en favoritos" o "sacar al michi de favoritos"). Darles IDs diferentes a las imágenes y, si es necesario, a los botones, facilita su manipulación más adelante.
    
    Por practicidad, puedes replicar la estructura HTML de un *article* varias veces y solo cambiar los IDs asociados, asegurando que el código JavaScript pueda trabajar sin problemas al identificar los elementos por su ID. La estructura base no debe afectar la lógica, siempre y cuando los nombres coincidan.
    
    ### **¿Cuáles son los detalles prácticos para visualizar y personalizar la estructura?**
    
    Al terminar de organizar secciones y títulos con claridad (por ejemplo, usando *michis app*, *gatitos aleatorios*, y *favoritos*), recargar en el navegador debe mostrar la diferencia entre cada zona. Si deseas, personalizar el proyecto con CSS es una gran opción, sobre todo si piensas sumarlo a tu portafolio, ya que este tipo de API, aunque sencilla, muestra buenas prácticas profesionales.
    
    No olvides que la estructura de favoritos debe comenzar vacía y llenarse dinámicamente según la información recibida de la API. El HTML inicial refleja estados por defecto, y se ajustará al integrar funcionalidad de JavaScript en futuras etapas, como cuando aclares los métodos HTTP y cómo afectan la creación, edición y eliminación de fotos.
    
- **¿Qué son los Métodos HTTP?**
    
    ### **¿Cuáles son los métodos HTTP más importantes?**
    
    Los métodos HTTP son herramientas cruciales en el entorno web que permiten al frontend comunicar al backend el tipo de acción o solicitud que se quiere realizar. Vamos a desglosar los cinco métodos HTTP más importantes y su rol fundamental en la interacción entre cliente y servidor.
    
    ### ¿Qué es el método GET?
    
    El método **GET** es el más común y se usa principalmente para obtener datos del servidor. Cuando hacemos una solicitud de tipo GET, estamos indicando al backend que deseamos leer o consumir información sin alterarla.
    
    - **Usos comunes**: Obtener páginas web, cargar imágenes o recibir datos de API.
    - **Comportamiento por defecto**: Al utilizar herramientas como `fetch`, el método GET es el predeterminado, lo que nos permite hacer solicitudes de lectura con facilidad.
    
    ### ¿Cómo funciona el método POST?
    
    El método **POST** es esencial cuando queremos crear nuevos recursos en el servidor. Es el equivalente a dar vida a nuevas entidades dentro de una aplicación.
    
    - **Usos comunes**:
        - Crear nuevos usuarios en una base de datos.
        - Registrar nuevas entradas en un formulario.
        - Enviar datos para ser procesados por el servidor.
    
    Con POST, le estamos "spoileando" al backend que deseamos crear algo nuevo y que debe prepararse para recibir y almacenar dicha información.
    
    ### ¿Para qué se usan los métodos PUT y PATCH?
    
    Tanto el **PUT** como el **PATCH** se emplean para modificar recursos existentes, pero la forma en que lo hacen varía.
    
    - **PUT**:
        - **Propósito**: Actualizar completamente un recurso.
        - **Uso típico**: Modificar todos los detalles de un usuario en un sistema.
    - **PATCH**:
        - **Propósito**: Realizar cambios parciales en un recurso.
        - **Uso típico**: Cambiar solo un atributo, como el correo electrónico de un usuario.
    
    Estos métodos permiten a las aplicaciones mantener la información actualizada y adaptarse a las necesidades de los usuarios.
    
    ### ¿Qué hace el método DELETE?
    
    Como su nombre lo indica, el método **DELETE** se utiliza para eliminar recursos del servidor. Es crucial para el manejo adecuado de los datos, permitiendo la eliminación cuando ya no son necesarios.
    
    - **Usos comunes**:
        - Borrar cuentas de usuarios.
        - Eliminar entradas o registros incorrectos.
    
    Cuando el frontend recibe una solicitud para borrar algo, traduce esta acción a una solicitud DELETE para que el backend pueda procesarla adecuadamente.
    
    ### Reflexión final
    
    Estas herramientas no solo facilitan la comunicación entre el frontend y el backend, sino que también aseguran que las acciones realizadas en una aplicación web se gestionen de manera ordenada y eficiente. Aunque existen más métodos HTTP, estos cinco son los más fundamentales y versátiles, permitiendo cubrir una amplia gama de necesidades en el desarrollo diario de aplicaciones. Te animo a explorar estos métodos en tus propios proyectos para consolidar lo aprendido y avanzar en tus habilidades de desarrollo web.
    
- **Manejo de errores HTTP en peticiones GET con JavaScript**
    
    Gestionar peticiones HTTP y manejar errores correctamente en tu aplicación es clave para trabajar con APIs de manera profesional. En este resumen aprenderás cómo mejorar tu proyecto de imágenes de gatos random y favoritos usando la API de DecadAPI, incluyendo buenas prácticas para mostrar mensajes de error claros a los usuarios.
    
    ### **¿Cómo estructurar tus funciones para cargar imágenes aleatorias y favoritos en una API?**
    
    Crear funciones claras y separadas ayuda a mantener el código legible y fácil de mantener. Por ejemplo, en lugar de mezclar la carga de gatos aleatorios y favoritos en una sola función, es mejor definir funciones independientes:
    
    - **loadRandomMichis** se encarga de cargar imágenes aleatorias, utilizando el endpoint correspondiente de la API.
    - **loadFavoriteMichis** maneja la carga de los gatos que han sido marcados como favoritos, usando un endpoint distinto que requiere autenticación (API Key).
    
    Separar las funciones permite mayor flexibilidad y hace más fácil agregar lógica específica a cada una. Así, puedes definir diferentes constantes como `API_URL_RANDOM` o `API_URL_FAVORITES` para tener endpoints bien identificados.
    
    ### **¿Por qué algunos endpoints requieren API Key y cómo indicar errores de autenticación?**
    
    La API de DecadAPI diferencia entre endpoints públicos y privados. Por ejemplo:
    
    - El endpoint *images/search* para gatos aleatorios no necesita autenticación.
    - El endpoint *favorites* requiere obligatoriamente una API Key.
    
    Cuando olvidas enviar la API Key, el servidor responde con un **Status Code 401** indicando error de autenticación. Es recomendable mostrar este error al usuario utilizando un elemento HTML (como un `span`), para comunicarle de forma clara qué ocurrió y que pueda tomar acción (por ejemplo, volver a intentarlo luego).
    
    ### **¿Cómo informar al usuario sobre errores inesperados (status 400, 401, 500)?**
    
    Utilizar los status code HTTP correctamente puede ayudarte a entender y explicar por qué falló una solicitud.
    
    - Si el código de respuesta no es 200 (éxito), se debe mostrar un mensaje de error en un `span` visible para el usuario.
    - Puedes concatenar el `status` y el mensaje proporcionado por la API (`data.message`) para brindar más contexto.
    - Si el error es genérico, por ejemplo un 500, es útil indicar que algo falló y sugerir al usuario intentarlo más tarde.
    
    Este manejo proactivo mejora la experiencia y reduce la frustración de los usuarios.
    
    ### **¿Cuáles son las recomendaciones prácticas para optimizar la interfaz y el manejo de errores?**
    
    - Reduce el exceso de imágenes simultáneas si ocupan demasiado espacio en pantalla.
    - Utiliza nombres de funciones y variables descriptivas, como *loadRandomMichis* o *API_URL_FAVORITES*.
    - Limpia el código borrando partes no necesarias, como saludos de prueba o artículos HTML no usados.
    - Centraliza la comunicación de errores en un solo elemento visual.
    - Valida el status code de cada respuesta antes de mostrar datos al usuario.
    - Explora crear un objeto con posibles errores para mostrar mensajes personalizados y amigables según cada situación.
- **Configuración de peticiones POST con fetch en JavaScript para APIs**
    
    Aprende paso a paso a **enviar peticiones POST con JavaScript** utilizando el método fetch, configurando correctamente los headers y el body para trabajar con APIs y guardar elementos como favoritos, un conocimiento esencial para cualquier desarrollador frontend que trabaja con datos dinámicos y bases de datos remotas.
    
    ### **¿Cómo se crea una función asíncrona para guardar favoritos con fetch y POST?**
    
    Primero, se prepara una función asíncrona llamada `saveFavoriteMichis` para gestionar favoritos. El proceso implica llamar al método *fetch* desde JavaScript y establecer el endpoint correcto de la API. Es importante diferenciar entre inglés estadounidense y británico para nombrar rutas; en este ejemplo, se debe respetar la convención británica, usando "favourites".
    
    - El nombre de la función puede variar, pero debe dejar claro que guarda favoritos.
    - El endpoint debe coincidir con la ruta especificada en la documentación de la API.
    - El método por defecto de *fetch* es GET, pero aquí se utiliza POST para agregar favoritos.
    
    Cuando se llama a la función tras pulsar un botón en la interfaz, el usuario decide qué elemento guardar. Hay que asignar *onClick* a los botones y pasar el id relevante de cada imagen que será marcada como favorita.
    
    ### **¿Qué propiedades y argumentos se deben pasar a fetch para un POST exitoso?**
    
    Para enviar correctamente una petición POST, se debe agregar un segundo argumento a fetch, el cual es un objeto con propiedades específicas:
    
    - **method**: Se establece en "POST" para indicar el tipo de solicitud.
    - **headers**: Obligatorio cuando la API lo requiere; se establece el tipo de contenido, por ejemplo: `{"Content-Type": "application/json"}`.
    - **body**: Aquí se indica la información que será enviada. El backend espera los datos como string, no como objeto JavaScript.
    - Usar `JSON.stringify` para convertir el objeto JavaScript en string.
    
    Si se omite alguno de estos requisitos, la API devolverá un error tipo 400 (Bad Request). Los errores y mensajes suelen estar presentes en la respuesta y pueden capturarse transformando el resultado con `await res.json()` más un condicional que verifique el status para mostrar detalles útiles al usuario.
    
    ### **¿Cómo se debuguean errores comunes al enviar datos a una API?**
    
    Durante la depuración, pueden surgir varios errores. Algunos ejemplos del proceso práctico:
    
    - Si falta la propiedad "headers" (usando "header" en singular por error), la API podría «no entender» la petición y responder con error 400.
    - Si el atributo `image_id` no es tipo string, y se envía como número, el backend también genera error 400. Es esencial usar el valor id correcto como string y que exista en la base de datos.
    - Para detectar errores más fácilmente, se captura el mensaje concreto de error devolviendo el resultado en formato JSON y mostrándolo en pantalla.
    
    Cada cambio en la petición permite ver un progreso (por ejemplo, recibir un error distinto indica que el paso realizado fue efectivo aunque falta pulir detalles).
    
    ### **¿Cómo se integran los favoritos guardados en la interfaz y se verifica su persistencia?**
    
    Tras una petición POST exitosa, se puede comprobar que la imagen fue efectivamente guardada revisando la funcionalidad de carga de favoritos (GET a la misma API). Se recarga la página y se observa que la sección de favoritos presenta el elemento recién agregado.
    
    - Visualmente, se revisa el listado de imágenes favoritas y se verifica el id correcto.
    - El proceso puede repetirse para múltiples imágenes, demostrando así el control sobre los datos que persisten vía la API.
- **Manipulación dinámica del DOM con datos de API REST**
    
    La manipulación dinámica del DOM con datos provenientes de una API REST es una habilidad fundamental para quienes buscan construir aplicaciones web interactivas y personalizadas. Aquí verás cómo implementar este proceso, manejar métodos HTTP como GET y POST, y adaptar tu código para gestionar favoritos de manera eficiente en JavaScript.
    
    ### **¿Qué es una API REST y cómo se consumen datos con métodos HTTP?**
    
    Para recibir y mostrar información dinámicamente en una web, primero necesitas consumir una **API REST** utilizando métodos HTTP, como GET y POST.
    
    - El método GET se utiliza por defecto con *fetch* para solicitar datos.
    - Otros métodos importantes son POST, PUT, PATCH y DELETE.
    - Al usar POST, debes enviar un *body* (cuerpo) en formato JSON, lo que requiere emplear *JSON.stringify* para que el backend y frontend se comuniquen correctamente.
    - Además, debes especificar en los *headers* que el contenido es de tipo JSON para una correcta interpretación.
    
    ### **¿Cómo manipular el DOM dinámicamente con base en respuestas de la API?**
    
    El reto es mostrar en el HTML los datos que devuelve la API. Aquí, la clave es crear elementos HTML de manera dinámica según la información de cada respuesta:
    
    - Utiliza *document.createElement* para generar nodos como `article`, `img` y `button` por cada elemento recibido (por ejemplo, cada gato favorito).
    - Asigna las propiedades y contenido necesarios a estos nodos, como la URL de la imagen o el texto del botón.
    - Emplea *appendChild* para insertar los nuevos elementos en el contenedor correspondiente del DOM.
    - Si ocurre un error durante el request a la API, muestra el mensaje de error dinámicamente usando elementos de HTML ya seleccionados.
    - Ajusta propiedades visuales como el *width* de las imágenes directamente desde JavaScript para mantener la presentación bajo control temporalmente.
    
    ### **¿Cómo gestionar favoritos en la aplicación y actualizar interactivamente?**
    
    Para que los usuarios puedan agregar distintos favoritos y verlos reflejados de inmediato:
    
    - Cambia la función que guarda favoritos para que acepte un ID como argumento y así guardar cada imagen individualmente, evitando duplicar el mismo favorito.
    - Asigna dinámicamente el evento *onClick* a cada botón mediante JavaScript, asegurando que cada uno guarde el favorito correcto utilizando la función y el ID del gato seleccionado.
    - Utiliza una *arrow function* para enlazar el evento sin ejecutar la función antes de tiempo.
    - Cuando se agregan favoritos, refresca visualmente la sección de favoritos en el DOM para mostrar el nuevo contenido.
    - Si necesitas limpiar elementos o corregir errores como IDs inválidos, revisa cuidadosamente la correspondencia entre los selectores y elementos reales en tu HTML.
    - Puedes limitar el tamaño de las imágenes manipulando atributos como *width*.
- **Eliminación dinámica de favoritos con API usando método DELETE**
    
    La gestión dinámica de favoritos es esencial al construir interfaces interactivas con APIs. Aquí te explicamos, paso a paso y con gran claridad, cómo implementar la eliminación de elementos favoritos en una lista, asegurando que el usuario disfrute de una experiencia ágil y comprendida.
    
    ### **¿Cómo se implementa el método DELETE para eliminar elementos favoritos?**
    
    Eliminar elementos de favoritos desde el HTML implica no solo modificar el DOM local, sino también interactuar con la API usando correctamente el método *DELETE*.
    
    - **Primero**: Construye una función asíncrona responsable de esta acción; el nombre recomendado es `deleteFavoriteMichis`.
    - **Segundo**: Adapta el *endpoint* usando la sintaxis de template literals de ECMAScript para enviar dinámicamente el ID correcto en la URL.
    - **Tercero**: Asegúrate de que el *endpoint* reciba el ID del elemento que deseas eliminar, no el `imageID` sino el `ID` simple asignado por la API.
    - **Cuarto**: Ajusta la configuración del *fetch* usando el método *DELETE*. No envíes body ni headers extras, solo tu API key si es requerida.
    - **Quinto**: Luego de una respuesta exitosa, registra mensajes claros en la consola para confirmar el éxito de la operación.
    
    ### **¿Qué errores comunes pueden aparecer al eliminar favoritos y cómo solucionarlos?**
    
    Durante el proceso surgen desafíos frecuentes al usar las APIs:
    
    - **Confusión de IDs**: Es común intentar usar el `imageID` en vez del `ID` propio del favorito. Si recibes un error como "Invalid Account", revisa que estés enviando el ID correcto.
    - **Actualización visual incompleta**: Si tras eliminar un favorito este no desaparece del HTML, probablemente hace falta refrescar el listado llamando a la función que carga los favoritos después de borrar.
    - **Duplicación de elementos**: Es importante limpiar la sección del HTML antes de renderizar los favoritos actualizados para evitar duplicados.
    
    ### **¿Cómo se refresca el contenido sin recargar la página?**
    
    Mejorar la experiencia del usuario depende de mantener sincronizado el estado visual con la información real.
    
    - Llama a la función que carga favoritos inmediatamente después de guardar o eliminar un michi.
    - Antes de cargar nuevos elementos, elimina todos los existentes en la sección, incluidos títulos si es necesario, y vuelve a crearlos dinámicamente.
    - Utiliza métodos como `section.innerHTML = ''` y luego añade de nuevo el título y los artículos con los michis favoritos actualizados.
    
    Estas prácticas aseguran una interacción eficiente y evitan la necesidad de que el usuario recargue la página manualmente tras cualquier acción.
    
- **Función y uso de headers HTTP en solicitudes web**
    
    Los **headers en HTTP** cumplen un rol esencial en la comunicación entre los navegadores y los servidores backend. Entender su función y cómo usarlos puede mejorar ampliamente el desarrollo de aplicaciones web y la interacción con APIs.
    
    ### **¿Cuál es la función de los headers en HTTP según el estándar web?**
    
    Al enviar solicitudes HTTP, muchas veces no basta con especificar la ruta o el endpoint de la API. Los headers agregan **metainformación clave** sobre cómo se debe interpretar el contenido enviado a través del body, o incluso ayudan a indicar el formato en el que se quiere recibir la respuesta.
    
    - En el mundo HTML, el head contiene instrucciones como la codificación de caracteres (*meta charset*), que permiten mostrar caracteres especiales correctamente en el body de la página.
    - De manera similar, en una solicitud HTTP, los headers pueden indicar el *content-type* para definir el formato del contenido del body.
    
    Así, los headers facilitan que tanto el cliente como el servidor "se entiendan" y logren una comunicación eficiente.
    
    ### **¿En qué se diferencian body y headers en las solicitudes HTTP?**
    
    El **body** en una solicitud HTTP contiene la información principal que deseamos enviar al servidor, como datos para crear un nuevo producto o guardar favoritos. Sin embargo, para que el servidor interprete correctamente esa información, los **headers** le indican detalles como el tipo y formato del contenido, o condiciones especiales para la entrega y el procesamiento.
    
    Ejemplos de analogías:
    
    - El contenido del body es como la información principal de una carta, mientras que los headers son las instrucciones a la oficina postal de cómo manejar y entregar esa carta.
    - Si el body fuera un vaso de vidrio, el header sería la etiqueta de "frágil" para indicar el cuidado necesario.
    
    ### **¿Cuáles son los headers HTTP más comunes y para qué se utilizan?**
    
    En solicitudes HTTP existen múltiples tipos de headers útiles según la necesidad:
    
    - **content-type:** Especifica qué tipo de dato se envía en el body, como *application/json*.
    - **Authorization:** Permite enviar credenciales seguras, como API keys, dejando de usar query parameters para mayor comodidad y seguridad.
    - Headers para gestión de cookies, localización y otros controles adicionales.
    
    Ya se utilizó *content-type* previamente al hacer solicitudes POST. El siguiente paso será implementar el uso del header *Authorization* para transmisiones de credenciales, mejorando así el flujo de trabajo en las integraciones con APIs.
    
    https://apipheny.io/api-headers/
    
    https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers
    
- **Configuración del header x-api-key para autenticación en APIs**
    
    La autenticación utilizando **headers** y **API keys** es fundamental cuando consumes APIs modernas con JavaScript. Este tema es recurrente en entornos de desarrollo actuales porque garantiza mejores prácticas y fomenta hábitos seguros, incluso si el recurso solicitado no es altamente privado. Aprender los detalles de cómo configurar estos headers te permite construir proyectos robustos, entendiendo cuándo tu código es claro y cómo proteger tus datos ante eventuales riesgos.
    
    ### **¿Por qué usar headers para enviar API keys al consumir APIs?**
    
    La principal diferencia entre enviar tu **API key** como *query parameter* o como header radica en la presentación y en la experiencia del desarrollador. Al usar headers, tu código es más limpio; no expones el token en la URL, y es más fácil de mantener. El resultado no cambia para el backend: seguirá identificando al usuario, validando límites de solicitudes y comprobando tu autenticidad.
    
    - El header suele llamarse `x-api-key`, según la documentación de la API.
    - Si prefieres, puedes seguir usando *query parameters*, pero usar headers es visualmente más estético.
    - Los cambios realizados en el código afectan solo la forma de envío; la funcionalidad permanece igual.
    
    ### **¿Cómo configurar el header x-api-key en una solicitud fetch de JavaScript?**
    
    En JavaScript, puedes agregar tantos headers como desees en el segundo argumento de la función *fetch*. Esto hace que tus solicitudes sean flexibles y adaptables según lo que la API requiera.
    
    1. Elimina la API key de la URL y colócala dentro del objeto `headers`.
    2. Ejemplo sencillo para solicitud GET:
    
    ```jsx
    fetch('https://api.example.com/michis', {
      method: 'GET',
      headers: {
        'x-api-key': 'TU_API_KEY_AQUí'
      }
    })
    ```
    
    - El método puede especificarse aunque GET sea el valor por defecto.
    - Puedes agregar el header `x-api-key` y otros headers necesarios.
    
    Si omites este header y la API lo requiere, obtendrás un error 401, lo que indica que la autenticación es obligatoria.
    
    ### **¿Es más seguro usar un header que un query parameter para la API key?**
    
    Existe el mito de que enviar la API key por header es mucho más seguro. Si bien así evitas exponer la clave en el historial del navegador, los headers no son completamente seguros ante un atacante determinado. Los headers siguen siendo visibles y, si alguien intercepta la petición, podría obtener la API key.
    
    - No elimina el riesgo de acceso no autorizado si otros vectores de ataque están presentes.
    - El uso de headers es ligeramente más seguro en contextos donde el historial del navegador debe protegerse.
    - Para proteger datos realmente críticos, considera métodos más avanzados como OAuth 2.0.
    
    Muchos proyectos principiantes usan APIs abiertas o con API keys simples porque los datos no son altamente confidenciales; estos mecanismos solo limitan la cantidad de solicitudes a realizar.
    
- **Content-Type en APIs: comunicación entre frontend y backend**
    
    Entender a fondo el uso del header **Content-Type** asegura una comunicación eficaz entre frontend y backend en cualquier desarrollo web moderno. Este elemento en las solicitudes HTTP determina cómo se envía y recibe la información, y puede ser el motivo principal de errores inesperados si frontend y backend no hablan el mismo "idioma".
    
    ### **¿Por qué el Content-Type es relevante para integraciones API?**
    
    El **Content-Type** define el formato de datos en el que el frontend envía información al backend o viceversa. Si los formatos no coinciden, es muy probable recibir errores, como vimos en peticiones previas. - Por ejemplo, si tu API solo acepta *application/json* pero envías *text/plain*, recibes un error y tu backend responderá que no entiende la información. - Es fundamental revisar la documentación de la API o consultar con tu equipo de backend para saber qué formatos acepta.
    
    ### **¿Cuáles son los formatos Content-Type más comunes y para qué sirven?**
    
    Aunque *application/json* es el formato más habitual, existen otros usos relevantes: - **application/xml** y **text/xml**: Usados para compartir datos estructurados en XML. - **application/zip**: Para subir archivos comprimidos. - **application/x-www-form-urlencoded**: Común en formularios HTML tradicionales donde los datos se envían de manera codificada en la URL. - **multipart/form-data**: Esencial para subir archivos como imágenes, audio, videos o documentos de Office. - **text/plain**: Para enviar texto simple, aunque no todas las APIs lo soportan.
    
    Quizá uses formatos poco habituales, como archivos de Word si el cliente lo solicita, aunque es raro. Muchos errores surgen por elegir un Content-Type que el backend no acepta; siempre conviene validar antes de enviar la solicitud.
    
    ### **¿Qué sucede cuando hay un Content-Type incompatible entre cliente y servidor?**
    
    En los ejemplos prácticos, cambiar el header a *text/plain* cuando la API espera *application/json* genera respuestas de error porque el backend no interpreta los datos (por ejemplo, *image id is required* al intentar guardar un favorito). - Es esencial que ambos extremos "hablen el mismo idioma". - Si envías un objeto JavaScript sin *stringifiar* a JSON, también ocurren fallos, como el error *Unexpected token O in JSON at position uno*. - La función *JSON.stringify* permite que JavaScript convierta objetos a texto JSON comprensible tanto para frontend como para backend. - Esto es clave, sobre todo si el backend está escrito en otro lenguaje como PHP, Python o Go.
    
    ### **¿Cómo facilita FormData el envío de formularios y archivos?**
    
    El uso de **FormData** ahorra trabajo, ya que agrupa inputs del formulario sin tener que obtener valor por valor manualmente. Es práctico para enviar imágenes, audio y varios tipos de archivos, haciendo más eficiente el código y reduciendo errores.
    
    https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/MIME_types/Common_types
    
- **Subida de archivos con FormData en JavaScript**
    
    Trabajar con archivos en formularios HTML puede sonar complicado, pero JavaScript ofrece soluciones simples y potentes. El objeto **FormData** te permite capturar y enviar información de formularios, incluidos archivos, de una forma profesional y efectiva. Este resumen explora sus usos principales, su relación con las APIs y resuelve errores comunes al subir imágenes.
    
    ### **¿Qué es FormData y para qué sirve en formularios HTML?**
    
    **FormData** es una interfaz nativa de JavaScript que simplifica obtener todos los valores directamente de los formularios HTML. Permite manejar archivos como imágenes, sin necesidad de extraer cada valor manualmente. Además, puedes agregar o consultar datos usando los métodos `set`, `get` y `append`.
    
    - FormData facilita el manejo de archivos en formularios, como imágenes o documentos.
    - Sus métodos permiten guardar, recuperar y listar múltiples valores asociados a una misma llave en el formulario.
    - Es útil para automatizar la recolección de datos al enviar peticiones a APIs.
    
    ### **¿Cómo crear y manipular FormData con JavaScript?**
    
    Es recomendable tener un formulario con su respectivo ID. Por ejemplo:
    
    ```jsx
    <section id="uploading">
      <h2>Sube la foto de tu michi</h2>
      <form id="uploadingForm">
        <input id="file" name="file" type="file"/>
        <button type="button" onclick="uploadMichiPhoto()">Subir foto de michi</button>
      </form>
    </section>
    ```
    
    Para utilizar FormData con este HTML:
    
    ```jsx
    const form = document.getElementById('uploadingForm');
    const formData = new FormData(form);
    ```
    
    **Funciones claves de FormData:** - `set(clave, valor)`: Agrega o reemplaza un valor. - `get(clave)`: Recupera el valor de una llave específica. - `append(clave, valor)`: Suma un valor sin eliminar los anteriores (útil para varios archivos o valores). - `getAll(clave)`: Trae todos los valores asociados a una misma llave.
    
    Ejemplo con `append` y `getAll`:
    
    ```jsx
    formData.append('pruebaMichi', 'michi rigoberto');
    formData.append('pruebaMichi', 'michi patricia');
    console.log(formData.getAll('pruebaMichi')); // ['michi rigoberto', 'michi patricia']
    ```
    
    ### **¿Qué cuidados tomar al enviar archivos a una API?**
    
    Cuando envías una imagen a una API (como *The Cat API*), debes usar el método adecuado. En este caso, se utiliza *POST* al endpoint `/images/upload`. Detalles importantes:
    
    - El formulario debe tener un input `name="file"`, tal como lo necesita la API.
    - No asignes el header `Content-Type` manualmente si usas FormData. El método `fetch` lo gestiona y agrega el boundary necesario automáticamente, la información técnica que separa las partes de los datos.
    - El body de la petición debe ser la instancia de FormData, no un objeto convertido con `JSON.stringify`.
    
    **Código de ejemplo para envío:**
    
    ```jsx
    const response = await fetch(API_URL_UPLOAD, {
      method: 'POST',
      headers: {
        'x-api-key': API_KEY // NO incluir Content-Type aquí
      },
      body: formData
    });
    ```
    
    - Si asignas `Content-Type` manualmente, puedes provocar errores 500 en el servidor porque falta el boundary necesario para procesar archivos.
    
    ### **¿Por qué ocurre el error 500 al subir imágenes y cómo evitarlo?**
    
    Si asignas manualmente `Content-Type: multipart/form-data`, el servidor puede rechazar la solicitud porque necesita un parámetro de *boundary* único. Este boundary separa las distintas partes del formulario, igual que el símbolo `&` en los query parameters. Cuando usas **fetch** y envías FormData, el navegador agrega el boundary automáticamente. Deja que fetch maneje este detalle y evitarás problemas.
    
    - Usa siempre FormData y deja que fetch configure los headers relacionados al tipo de contenido.
    - Consulta la documentación de la API para validar que los nombres de los campos coincidan con lo esperado.
    
    ### **¿Qué retos prácticos puedes intentar para mejorar la experiencia?**
    
    Puedes agregar una vista previa de la imagen seleccionada antes de enviarla. Esto permite que los usuarios verifiquen la foto elegida, mejorando la confianza en el formulario. Si experimentas, comparte tus soluciones y aprendizajes en la sección de comentarios y ayuda a otros estudiantes a crecer.
    
    https://muffinman.io/blog/uploading-files-using-fetch-multipart-form-data/
    
    https://developer.mozilla.org/es/docs/Web/API/FormData
    
- **Instancia de Axios con configuración base para solicitudes HTTP**
    
    Axios sigue siendo una de las herramientas favoritas para hacer **solicitudes HTTP** en entornos de desarrollo moderno, facilitando el consumo de *API REST* tanto en navegadores como en Node.js. Aquí te comparto las mejores prácticas y detalles relevantes que destacan a Axios por encima de otras alternativas del ecosistema JavaScript.
    
    ### **¿Por qué Axios es tan popular para consumir APIs en JavaScript?**
    
    Axios destaca por su **experiencia de desarrollo simple y minimalista** comparada con métodos tradicionales como *XMLHttpRequest* o incluso el propio *fetch*. Desde encuestas como State of JS y ejemplos en repositorios de GitHub hasta la preferencia en cursos especializados, Axios se posiciona como una de las bibliotecas más empleadas. - **Facilita la configuración de solicitudes complejas** en menos pasos. - Permite trabajar tanto en el navegador como en Node.js. - Ofrece una sintaxis limpia para manejar métodos como GET, POST, PUT, entre otros.
    
    ### **¿Qué herramientas similares existen para hacer solicitudes HTTP?**
    
    Además de Axios, existen opciones como *Trae.js*, una herramienta minimalista influenciada por la comunidad argentina, y alternativas como *Node-Fetch* o *Request* para integrar Fetch en Node.js cuando no se disponía de soporte nativo. - Node.js ya anunció soporte nativo para *fetch*, por lo que el uso de algunas de estas herramientas puede disminuir con el tiempo.
    
    ### **¿Cómo se instala y configura Axios en el proyecto?**
    
    La instalación de Axios es flexible: - Puede agregarse mediante *npm*, script en HTML, *Yarn* o *Bower*. - Una vez incluido, Axios permite crear "instancias" usando `axios.create`, ideal para establecer configuraciones comunes.
    
    **Ejemplo básico de instancia y configuración:**
    
    ```jsx
    const api = axios.create({
      BASE_URL: 'http://api.dicatepi.com/v1/'
    });
    api.defaults.headers['x-api-key'] = 'TU_TOKEN_AQUI';
    ```
    
    - Así, todas las requests de esta instancia tendrán la misma base URL y headers.
    
    ### **¿Qué ventajas ofrece Axios sobre fetch y otras librerías?**
    
    **Axios realiza muchas tareas de forma automática:** - No requiere separar la URL o la configuración en distintos argumentos. - Al enviar datos con métodos POST, no es necesario hacer manualmente `JSON.stringify`. - No hay que parsear la respuesta con `.json()`, pues el resultado ya incluye la propiedad `data` con la información lista para usar. - Permite acceder fácilmente al `status` de la respuesta.
    
    **Fragmento de código usando Axios para una solicitud POST:**
    
    ```jsx
    const response = await api.post('favorites', { image_id: id });
    const data = response.data;
    const status = response.status;
    ```
    
    - No hace falta stringificar el cuerpo ni parsear la respuesta. Todo está listo en `response.data` y `response.status`.
    
    ### **¿Qué errores comunes puedes evitar usando Axios?**
    
    **Axios minimiza los errores tipográficos y de configuración:** - Al centralizar la configuración, como el header de autorización, se evita duplicar código y cometer errores al definir la API key en cada llamada. - Permite detectar rápidamente errores en los nombres de propiedades (`status` vs. `staus`), ya que el editor y la consola lo muestran claramente.
    
- **Propiedades avanzadas de Fetch: mode, cache y redirect**
    
    La correcta gestión de las propiedades avanzadas de **Fetch** puede marcar la diferencia entre un desarrollo web eficiente y uno plagado de complicaciones. Comprender cómo funcionan *mode*, *cache* y *redirect* dará mayor control, seguridad y flexibilidad en la interacción con APIs, especialmente en aplicaciones modernas donde la comunicación entre frontend y backend es clave.
    
    ### **¿Qué es la opción mode en Fetch y cómo afecta a CORS?**
    
    El parámetro **mode** de Fetch define cómo se gestionan las políticas de origen en las solicitudes HTTP. Esta opción es esencial para controlar con quién intercambiamos información, abordando de raíz los frecuentes errores de **CORS** (*Cross-Origin Resource Sharing*). Por ejemplo:
    
    - Si el backend emplea *same-origin*, solo las solicitudes desde el mismo origen serán aceptadas.
    - En APIs públicas, esta restricción suele eliminarse para facilitar el acceso de diversos clientes.
    - En el frontend también se puede usar *mode* para limitar cuándo una solicitud puede enviarse a otro servidor.
    - Por defecto, el valor es *no-cors*, permitiendo que Fetch intente comunicarse más libremente, aunque la respuesta final depende de la política del backend.
    
    Esta configuración resulta fundamental para evitar sorpresas, sobre todo al integrar sistemas con políticas de seguridad estrictas.
    
    ### **¿Cuáles son las claves del uso de la propiedad cache en Fetch?**
    
    La propiedad **cache** controla cómo se guardan y reutilizan los resultados de las solicitudes:
    
    - Permite que el navegador conserve información descargada previamente, útil para acelerar futuras peticiones o manejar la ausencia de internet.
    - La decisión de cuándo y cómo usar la caché debe tomarse con cuidado para evitar mostrar datos desactualizados.
    - Se puede forzar el uso de caché, ignorarla por completo o pedir siempre una nueva solicitud.
    - La lógica interna de Fetch gestiona por defecto estas operaciones, por lo que rara vez es necesario intervenir, salvo casos muy específicos.
    
    Conocer estos detalles ayuda tanto para responder entrevistas técnicas como para actuar ante comportamientos inesperados en aplicaciones web.
    
    ### **¿Qué opciones existen para el manejo de redirect en Fetch?**
    
    Con la opción **redirect** se decide cómo manejar las redirecciones HTTP (códigos de estado 300, 307, 308):
    
    - Se puede elegir que Fetch siga automáticamente las redirecciones con la opción *follow*.
    - O impedir el seguimiento de redirecciones por seguridad, evitando que Fetch acceda a fuentes no confiables.
    - En escenarios avanzados, como el uso de *service workers*, es posible gestionar manualmente cada redirección, aunque este trabajo normalmente solo se justifica en contextos muy concretos.
    
    Ajustar la política de redirección permite asegurar que los datos sensibles no sean enviados o recibidos por destinos no intencionados.
    
    ### **¿Cómo funciona internamente Fetch y cuál es el reto propuesto?**
    
    Fetch no implementa toda la lógica de las solicitudes HTTP por sí sola, sino que se apoya en los prototipos internos de *Request*, *Headers* y *Response*:
    
    - El código principal de Fetch reside en estos prototipos, cada uno encargado de aspectos específicos.
    - Examinar su código fuente es un excelente ejercicio para entender la arquitectura detrás del funcionamiento de Fetch.
    - El desafío planteado es analizar a fondo cómo estás escritas estas piezas, desglosar el código, y luego intentar construir tu propia versión de Fetch.
    
    Si has trabajado con Axios o similar, aplicar estos conceptos en tu propia función customizada te permitirá mejorar la experiencia al consumir APIs y añadir características exclusivas, como instancias personalizadas.
    
    https://developer.mozilla.org/en-US/docs/Web/API/Request/cache
    
    https://developer.mozilla.org/en-US/docs/Web/API/Window/fetch
    
    https://developer.mozilla.org/en-US/docs/Web/API/Request
    
    https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Caching#freshness
    
    https://developer.mozilla.org/en-US/docs/Web/API/Headers
    
    https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Caching#actualizaci%C3%B3n
    
    https://developer.mozilla.org/en-US/docs/Web/API/Response
    
- **Alternativas modernas a REST: GraphQL, WebSockets y Web 3.0**
    
    Hoy, el desarrollo web va mucho más allá del clásico modelo REST. Existen herramientas y protocolos modernos pensados para optimizar la interacción entre clientes y servidores, impulsar nuevas arquitecturas como las aplicaciones descentralizadas y mejorar la experiencia del usuario desde el frontend hasta el almacenamiento de datos. ¡Aquí te mostramos por qué conocer estas alternativas hará que tu perfil como desarrollador destaque!
    
    ### **¿Qué alternativas modernas existen a REST para transferir datos por HTTP?**
    
    REST dejó de ser la única opción para crear aplicaciones web efectivas. Ahora, encontramos soluciones como SendBeacon, GraphQL y Websockets, que optimizan escenarios específicos y necesidades técnicas.
    
    - **SendBeacon** es una herramienta reciente, ideal cuando solo necesitas enviar datos (como eventos de analítica) sin requerir respuesta del servidor.
    - *Ejemplo*: Su uso en herramientas como Google Analytics permite que si el paquete de datos no llega, simplemente se pierde la métrica, sin afectar la experiencia de usuario ni la carga de la web.
    - **GraphQL** rompe la lógica tradicional de múltiples endpoints REST; en vez de recibir datos genéricos o innecesarios, el frontend define exactamente qué información obtiene del backend, evitando respuestas innecesarias.
    - **Websockets** potencian la comunicación bidireccional y persistente, simulando una llamada telefónica que permanece abierta entre cliente y servidor para intercambiar información de manera eficiente y en tiempo real.
    
    ### **¿Cómo funcionan GraphQL y Websockets en la estructuración del frontend y backend?**
    
    Estas tecnologías ofrecen flexibilidad y eficiencia en la arquitectura de aplicaciones modernas:
    
    - En **GraphQL**, realizas "queries" para obtener solo los datos requeridos o "mutaciones" para modificar el estado, siempre a través de un único endpoint y con la estructura definida por el cliente.
    - *Ejemplo*: Puedes pedir solo el `ID` y la `URL` de un gatito específico, en vez de un objeto completo.
    - El "empowered client" representa al frontend como quien elige qué información le interesa realmente, optimizando el consumo de recursos.
    - En **Websockets**, utilizando librerías como SocketIO, se mantienen conexiones abiertas entre cliente y servidor, facilitando eventos y respuestas inmediatas sin la sobrecarga de establecer nuevas conexiones por cada petición.
    - *Ejemplo*: Cuando se produce un evento como un mensaje, ambos extremos pueden reaccionar instantáneamente sin demoras por reconexión.
    
    ### **¿Qué caracteriza a la web 2.0 y cuál es el enfoque de la web 3.0?**
    
    La web ha evolucionado de sitios estáticos a experiencias interactivas y ahora busca la descentralización:
    
    - **Web 1.0** permitía solo leer información estática, sin interacción.
    - **Web 2.0** (actual):
    - Los usuarios pueden crear contenido (comentarios, publicaciones) usando tecnologías como JavaScript, frameworks y APIs REST.
    - Las aplicaciones siguen una arquitectura en tres capas: cliente (frontend), lógica de negocios (backend) y persistencia (base de datos).
    - El frontend es un puente entre el usuario y la lógica de la aplicación, utilizando herramientas como React, Angular o Vue.
    - El backend se construye con lenguajes variados (Node.js, Python, Go) y se conecta con bases de datos (MongoDB, servicios en la nube, etc.).
    - **Web 3.0**:
    - Busca que los usuarios sean dueños de su contenido, gracias a tecnologías descentralizadas.
    - Mantiene la estructura de tres capas, pero cambia las tecnologías clave:
        - El cliente integra librerías especializadas como WJS o E3JS para conectar con lógica de negocio basada en blockchain.
        - La lógica de negocio se programa con lenguajes como Solidity, conectándose a soluciones de persistencia descentralizada (Ethereum, IFPS, Polygon).
        - Se usan protocolos como JSON-RPC y dominios ENS, diferenciándose de los tradicionales API REST y DNS.
    - Las aplicaciones descentralizadas (dApps) dependen de blockchain y smart contracts para garantizar la propiedad y transmisión segura de información.
    
    ### **¿Qué herramientas debes dominar para avanzar hacia aplicaciones descentralizadas?**
    
    - Comprender cómo consumir una API REST tradicional con JavaScript es esencial antes de trabajar con tecnologías de la web 3.0.
    - Si quieres especializarte en dApps, estudia herramientas como WJS, E3JS, JSON-RPC, ENS, y aprende sobre sistemas de persistencia en blockchain (como IFPS y Ethereum).
    - Explora cursos sobre criptomonedas, blockchain y desarrollo de smart contracts para ampliar tu perfil como desarrollador.
    
    https://platzi.com/blog/introduccion-a-graphql/
    
    https://platzi.com/blog/rest-o-graphql/
    
    https://platzi.com/cursos/nodejs-graphql/
    
    https://platzi.com/blog/websockets-en-nodejs/
    
    https://platzi.com/cursos/intro-dapps/
    
    https://platzi.com/blog/el-rey-ha-muerto-larga-vida-a-graphql/
    
    https://platzi.com/cursos/frontend-dapps/
    
    https://platzi.com/cursos/socket-io/
    
- **Consumo de API Rest con JavaScript para front-end developers**
    
    Aprender a consumir una API Rest con JavaScript es esencial para quienes buscan oportunidades como front-end developer. Dominar este proceso te permite construir aplicaciones web dinámicas, eficientes y preparadas para interactuar con servicios globales. Aquí te mostramos los puntos clave sobre APIs Rest, basados en lo aprendido, y te motivamos a avanzar hacia proyectos prácticos.
    
    ### **¿Qué es una API Rest y por qué es relevante para el desarrollo front-end?**
    
    Una **API Rest** es una interfaz que permite la comunicación entre diferentes sistemas a través de la web. Utiliza métodos como *GET*, *POST* y *DELETE*, lo que facilita obtener, enviar o eliminar datos. Es fundamental porque permite a las aplicaciones web consumir recursos externos y brindar mejores experiencias al usuario.
    
    ### ¿Cómo usar JavaScript para consumir una API Rest?
    
    Durante el aprendizaje usaste *fetch*, que por defecto realiza peticiones *GET*, pero también se puede configurar para otros métodos como *POST* y *DELETE*. Este proceso se aplicó directamente con la API de *The Cat API*, logrando solicitudes reales y manejo de diferentes códigos de estado HTTP.
    
    - Probaste *fetch* para obtener datos y explorar endpoints de la API.
    - Aprendiste a subir imágenes de gatos, almacenándolas en la nube con una URL pública.
    - La práctica incluyó agregar estilos personalizados usando CSS, mejorando el aspecto para portafolio.
    
    ### **¿Por qué personalizar tu proyecto y cómo presentarlo en tu portafolio?**
    
    Personalizar tu proyecto, como añadir imágenes propias y estilizar con CSS, muestra tus habilidades como front-end developer. Incluir estos trabajos en tu portafolio es clave para demostrar tu experiencia profesional.
    
    - Subiste imágenes propias, permitiendo compartirlas en línea.
    - Integraste funcionalidades interactivas, haciendo tu proyecto más atractivo y funcional.
    
    ### **¿Qué sigue después de dominar el consumo básico de APIs Rest en JavaScript?**
    
    El próximo paso es aplicar lo aprendido en un proyecto más ambicioso. Se propone trabajar con una API famosa de películas, enfocándose en construir una experiencia de usuario avanzada y un portafolio robusto.
    
    - El objetivo es crear una aplicación que interactúe de forma fluida con los usuarios.
    - Cada interacción generará solicitudes HTTP, acercándote a un nivel profesional en front-end.