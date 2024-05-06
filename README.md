# capacitacion-SIG
Material de apoyo para capacitación en SIG con QGis

# Introduccion a los SIG

## Representaciones - Tipos de Datos

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/37c92320-461d-429c-911c-51f6ba7725db)

Los datos pueden tener tres formatos, Raster, Vectorial y Tabular;

El formato vectorial a la vez admite tres posibilidades: puntos, líneas o polígonos.

* Los puntos representan ubicaciones del tipo ciudades, personas, sucursales, avistamiento, incidente, toma de muestra, etc.
* Las líneas representan recorridos, como los ríos, las rutas, trillos o un caño de agua, etc.
* Los polígonos, por su parte representan áreas como parcelas, provincias, o zonas de distribución de un individuo, ANP, etc.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/5d20e959-dd21-461e-ba5a-8a01fd588306)

Cualquiera de estos objetos que llamamos "vectoriales" se compone de 2 partes la Geográfica y Descriptiva

* Geográfica: Son pares de coordenadas que la ubican en el territorio.
* Descriptiva: Son sus atributos (campos de valores) que le dan un sentido lógico a ese objeto representado.

La relación de los elementos en su aspecto lógico y geográfico es de 1 a 1, es decir que, a cada registro en una tabla se le corresponde un objeto en el mapa y viceversa. 

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/c6def464-ef0f-4bc8-977e-2b2f80804cb9)

Raster son set de datos continuos (a diferencia de los vectores que son discretos) están conformados por pequeños espacios uno a continuación del otro y cada uno con un valor determinado. Nuevamente con el concepto de parte geográfica y lógica.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/b4383c9d-a76b-462c-a6c7-9a73168b787a)

Imagenes Visibles

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/c5552715-5e78-492e-a869-56abbd5acdf9)

Tabular refiere simplemente al conjunto de información o datos ordenada en campos para distintos objetos, pero que carecen del componenete geográfico. Situación que salvamos o que igualmente la aprovechamos llevandola al territorio identificando un valor o dato indice o lo que llamamos como identificador clave. (PK en bases de datos)(Puede ser único)

## Trabajo con capas y atributos

En escencia vamos a utilizar una herramienta para administrar, procesar, almacenar, etc los datos de nuestro interes transformandolos en capas que representen algo significativo en nuestro ámbito de estudio.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/9c52e2a4-d7e1-49fc-a007-01d375027ca9)


## Sistemas de posicionamiento y coordenadas

Componente geográfica son pares de coordenadas.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/a803d3e2-a3fe-4aee-a70d-d94e689fd6c2)

Ejemplos de presentación de estas coordenadas:
Las coordenadas geográficas se expresan tradicionalmente en el sistema sexagesimal: grados (°) minutos (’) segundos (’’)
Dependiendo del signo puede aparecer una letra que indica el hemisferio N, S o E, O(W)
- 27° 2' 31" S, 55° 14' 4" O  ó  -27° 2' 31", -55° 14' 4"
- -27.04182432, -55.23433301

Menos usadas:
- 27° 2.5095' S, 55° 14.0600' W
- 270231S, 0551404W

Con este tipo de representación (esférica) es complejo realizar ciertos análisis como por ejemplo de superficies o distancias, para solucionar (en parte) esto existen las proyecciones cartográficas, que utilizan modelos matemáticos para representar la tierra y luego asignar coordenadas en X e Y (generalmente en metros) a estos planos teóricos

- 7009101.30, 7377526.17  - Proyección POSGAR 98 / Argentina 7

Propiedades
- Unidades: metros
- Statica (depende de un datum(modelo) fijo a un plano)
- Cuerpo que representa: Tierra
- Método: Transverse Mercator

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/74a49139-2b39-42f4-9611-12f374b854f7)

Deformaciones

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/b6dd12c3-8650-4989-874a-2390a35d241c)

Primer Vistazo!!

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/d9232513-b9cf-445c-8459-ccd11816ed04)


# Métodos de creación de datos

Partiendo de lo que charlamos la vez anterior respecto a que los SIG necesitan datos y nos ayudan a administrarlos vamos a ver que existen muchos set de datos disponibles (lo vamos a ver en detalle más adelante), sin embargo, a medida que nuestro campo de trabajo ó proyecto es más específico vamos a tener que crear nuestros propios datos, ni hablar si estamos haciendo un relevamiento.

## Fotointerpretación

Con una imagen de base (raster) digitalizamos lo que podemos ver sobre la misma, para ello con anterioridad necesitamos detenernos y decidir que capa vamos a construir para optar por un lado puntos, lineas o poligonos (no se pueden mezclar dentro de una capa) y por otro lado sus atributos decidiendo para cada uno de ellos el tipo de dato.

Cuadro de diálogo de Creación de Capas
Antes de poder añadir nuevos datos vectoriales, necesitas un conjunto de datos vectoriales al que añadirlos. En este ejmplo, empezarás creando nuevos datos por completo, en lugar de editar un conjunto de datos existente. Además, necesitarás definir de antemano tu propio conjunto de datos nuevo.

*	Navega y haz clic en la entrada del menú Capa ‣Crear Capa‣ Nueva capa de archivo shape.
 
![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/fc364b5e-f122-4d9d-9c94-3d9a3b6d3a3d)

Se presentará el siguiente cuadro de diálogo:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/16fcabfb-28cb-4e05-b6d5-abb73d6194f4)

Haz clic en el botón “…” (puntos suspensivos) al final de “Nombre de archivo” y navega al directorio del proyecto o donde lo desees almacenar en el disco y dale un nombre representativo. Con esto listo, haz clic en Guardar.


Es importante decidir qué tipo de conjunto de datos quieres en este punto. Cada tipo de capa vectorialesta “construido de forma diferente” en sus bases, así que una vez hayas creado la capa, no puedescambiar su tipo.


Para el ejemplo, crearemos nuevas características para describir áreas. Para estas características, necesitarás crear un conjunto de datos poligonal.
*	Haz clic en Tipo de Geometría y elegiremos la opción Polígono
El siguiente campo te permite especificar el Sistema de Referencia de Coordenadas, o SRC. (Un SRC especifica la descripción de un punto en la Tierra en términos de coordenadas, y como hay muchas formas de hacer esto, hay muchos SRC diferentes. Para el SRC de este proyecto de ejemplo usemos el más general que es WGS84, así que es el correcto por defecto.)

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/b116c06c-2ad3-4ea1-a4ae-0af99fdbf40e)

A continuación hay una colección de campos agrupados en Nuevo atributo. Por defecto una capa tiene solo un atributo, el campo id (que deberías ver en Lista de atributos) inferior. Sin embargo, para que los datos que crees sean útiles, necesitas decir algo sobre las características que crearás en la nueva capa. Para tus propósitos actuales, será suficiente añadir un campo llamado nombre.

Replica la configuración siguiente, luego haz clic en el botón Añadir a la lista de atributos.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/7a8665aa-ba83-4017-ab81-5a1cce2a27b8)

De este modo puedes agregar los atributos que creas necesarios que tenga esta nueva capa y luego al ir insertando objetos se deberán completar con información.
Nota: Existen ciertas restricciones específicas para las tablas de atributos de los archivos Shape file: Los nombres de los campos no pueden tener más de 10 caracteres, y no pueden comenzar con un número o espacio vacío. Solo se pueden elegir entre los Tipos de dato: Entero o Integer, Decimal o Double, Fecha o Date y Datos de texto / Cadena de texto o String, donde para este último la longitud máxima es de 255 caracteres. 

Haz clic en Aceptar. Y la nueva capa quedará agregada al proyecto, pero aún sin objetos.

### EDICIÓN

Para empezar a digitalizar, necesitarás introducir modo de edición. Los softwares SIG normalmente lo requieren para prevenir que edites o borres accidentalmente datos importantes. El modo edición se activa o desactiva individualmente para cada capa.
Para introducir el modo edición para la capa nueva (o la que se desee):
*	Haz clic en la capa en la Lista de capas para seleccionarla (Asegúrate que seleccionas la capa correcta, ¡de lo contrario editarás la capa incorrecta!).
*	Haz clic en el botón Conmutar edición (Lápiz)  

Si no puedes encontrar ese botón, comprueba que la barra de herramientas Digitalización está activada. Debería haber un marcador junto a la entrada del menú Ver ‣ Barras de herramientas ‣ Digitalización

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/6b06937b-70af-4e22-82b1-50d1f959b350)

Tan pronto como estés en el modo edición, verás que las herramientas de digitalización están ahora activadas (dependiendo del tipo de geometría):

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/22b175ff-ac95-46c5-8e1d-a8f209b32d63)

Otros cuatro botones relevantes todavía están desactivados, pero se activarán cuando empecemos a interactuar con nuestros nuevos datos:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/589a7023-4d4f-4b4d-8fe6-1db75995b297)

En la barra de herramientas, están:
•	Guardar cambios de la capa: Guarda cambios hechos en la capa.
•	Añadir objeto espacial: Comienza a digitalizar un nuevo elemento.
•	Mover objeto(s) espacial(es): Mueve un elemento completo
•	Herramienta de nodos: Mueve solo una parte de un elemento
•	Borrar lo seleccionado: Borra el elemento seleccionado.
•	Cortar objetos espaciales: Corta el elemento seleccionado.
•	Copiar objetos espaciales: Copia el elemento seleccionado.
•	Pegar objetos espaciales: Pega de nuevo un elemento cortado o copiado en el mapa.

Para añadir un elemento nuevo:
1.	Haz clic en el botón Añadir objeto espacial para empezar a digitalizar en la capa o el Shape que hayas activado el modo edición y que este seleccionado en el Panel de Capas.
2.	Notarás que el cursor del ratón se ha convertido en una cruz. Esto te permite situar de forma precisa los puntos que digitalizarás. Recuerda que incluso si estas usando la herramienta de digitalización, puedes ampliar o disminuir el zoom en tu mapa con la rueda de tu ratón, y puedes desplazarte manteniendo pulsada la rueda del ratón y arrastrando el mapa.
3.	Empieza a digitalizar clicando en un punto en el mapa.
4.	En el caso de tipo líneas o polígonos sitúa más puntos clicando puntos adicionales en el mapa, hasta que la forma que estés dibujando cubra completamente la forma que busca.
5.	Después de situar el último punto, clic derecho para acabar de dibujar el polígono o línea. Esto finalizará el elemento y te mostrará el cuadro de diálogo Atributos.
6.	Completa los valores para cada atributo de la tabla.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/09e2d8ac-bcf7-485e-83b5-bc83eb7310e4)

Veremos 

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/a061353f-82cb-4919-9873-d997a28463ea)

Al completar y Aceptar

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/a1e55ad6-e3f1-4574-8d95-f7db359ebea7)

Para finalizar volvemos a clicar en el lapiz para conmutar la edición y no nos olvidemos de grabar!!!.

## Relevamiento con equipos GPS

Con todos los dispositivos GPS especificos y similares, como por ejemplo, celulares con aplicaciones como OSMAnd, podemos generara esta información directamente en terreno, claramente poniendo mayor enfasis y foco en la componente geográfica con menor fuerza en los atributos pero esto lo supliremos en gabinete.

El QGis levanta los archivos GPX generados con estos dispositivos un app's 

OSMAnd - PlayStore

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/4849caed-90fd-4a0e-a483-598d89ac1e38)

Captura de datos

![Screenshot_20240422-175501](https://github.com/russorl/capacitacion-SIG/assets/6954564/02674a7a-c5c0-433c-93d4-6f6f53c46020)

Bajar o compartir archivos GPX - Veamos ejemplos.

## Relevamiento x otros métodos 

El relevamiento más simple que podriamos hacer con móviles es tomar fotografías con la ubicación activada: de este modo podemos copiar las fotos de terreno al equipo y generar la capa de ubicación automáticamente a partir de las coordenadas enbebidas.

Buscamos entre las herramientas el proceso de "Importar fotos geoetiquetadas"

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/38908bae-c69b-49f8-bee7-bccec78a4b1e)

En la ventana 

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/002ccefe-5da2-43c7-bc2b-e7a7699f6d79)

* Especificaremos la carpeta donde tenemos las fotos clicando en "..." (tres puntos) 
*  o especificar donde queremos q (también podemos dejar dejar así y crear como capas temporales)
*  Por último algunas configuraciones extra para aprovechar las fotos y ya!!! Veamos ejemplos.

  Otros conocidos:
  * Epicollect5: Tipo formularios de encuesta, se pueden configurar por proyecto y también tiene una app de recoleccion que funciona con o sin conectividad.
  * KoboToolBox: Tipo formularios (pero más complejo de configurar y con más tipos de datos), se pueden configurar por proyecto y también tiene una app de recoleccion.
  * GoogleMaps: Permite generar capas para descargar en KML (puede ser engorroso el manejo de atributos y problemas de precision al marcar puntos)
  * QField: App desarrollada para compatibilidad con QGis, uso sin conectividad, no es tan simple de manejar en terreno y menos en dispositivos de pantalla pequeña.
  * SMART Conservation Software - Herramienta de seguimiento espacial y elaboración de informes (smartconservationtools.org) - (Por Investigar aún)
  * iNaturalist - Podra servir como herramienta de recolección de datos ?? 

### VISUALIZACIÓN

## Utilizando etiquetas

Antes de ser capaz de acceder a la herramienta de Etiquetas, necesitarás asegurarte de que está activada.

*	Ves al elemento del menú "Ver" ‣ "Barra de Herramientas".
*	Asegúrate de que el elemento "Etiqueta" está marcado. Si no lo está, haz clic en el elemento "Etiqueta" y se activará.
*	Haz clic en la capa LOCALIDADES_COMPLETAS en la Lista de capas, para que quede resaltado.
*	Haga clic en el siguiente botón de la barra de herramientas:  ![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/0322b6a0-ade3-40dc-b6e7-49645eb77ec1)
Esto te abrirá el cuadro de diálogo "Configuración del etiquetado de la capa".
*	Debemos elegir el la lista desplegable "Etiqueta sencilla".
Necesitarás elegir el campo de atributos que será utilizado en las etiquetas. En este caso elige el campo "NOMBRES".
*	Selecciona "NOMBRES" de la lista:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/7bb86c11-7e4e-4415-9895-a8df36ba956a)

* Clic en Aceptar.
* El mapa debería tener ahora etiquetas como éstas:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/15e16185-0b5d-4ac5-9bf4-22bc2d1657ce)

## Cambiando opciones de etiquetado
Dependiendo de los estilos que elegiste para tu mapa en las lecciones anteriores, puede que encuentres que las etiquetas no tienen el formato apropiado y se solapan o están demasiado lejos de sus puntos marcadores.
*	Abre la Herramienta de etiquetado de nuevo haciendo clic en su botón como antes.
*	Asegúrese de que "Texto" está seleccionado en la lista de opciones del lado izquierdo, después, actualice las opciones de formato de texto para que coincida con lo que se muestra aquí:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/ebb97d0a-b597-4ecb-8dad-0084467664ff)

¡El problema de fuente está resuelto! Ahora nos dirigimos al problema con las etiquetas solapadas con los puntos, pero antes de hacer esto, echemos un vistazo a la opción Margen.

*	Abre el cuadro de diálogo "Herramienta de etiquetado".
*	Selecciona "Buffer" de la lista de opciones de la izquierda.
*	Seleccione la casilla de verificación junto a Dibujar buffer de texto, después elija las opciones para que coincida con los que se muestran aquí:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/830ca352-6653-4f82-b230-77db81bd6d3c)

*	Haz clic en Aplicar.

Ahora podemos situar la posición de las etiquetas en relación con sus puntos marcadores.

*	En el cuadro de diálogo Herramienta de etiquetado, ve a la pestaña "Ubicación".
*	Cambie el valor de "Distancia a 2mm" y cerciórese que "Alrededor del punto" este seleccionado

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/90cca6fc-4bbc-4cff-9a14-992e1a2a67a4)

## Clasificación
La simbología nos permite representar los atributos de una capa de una forma sencilla de entender. También permite a los que visualicen el mapa entender el significado de las características, utilizando atributos relevantes que hemos escogido. Dependiendo del problema al que te enfrentes, aplicarás diferentes técnicas de clasificación para resolverlos:

### Clasificación de Datos. Símbolo único
*	Agregar la capa LIMITES_MUNICIPIOS_MISIONES
*	Abrir el cuadro de diálogo Propiedades de la Capa para la capa LIMITES_MUNICIPIOS_MISIONES
*	Ir a la pestaña Simbología.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/002a11f0-6a95-4bb7-81b0-cb2a54c27572)

### Clasificación de Datos. Categorizado

Haga clic sobre la lista desplegable que dice Categorizado: y configurar, el valor (poner nombre del campo por el cual quiero que se me categorice). En rampa de colores elegir cual quiero y mejor represente el valor del campo elegido

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/a098aadc-bd18-458a-b008-9d5316523be1)

Hacer clic en "Clasificar" y vemos como el mapa ha adquirido, la simbología configurada.
Cualquier atributo que no quiero que salga representado en el mapa, lo puedo eliminar, seleccionándolo y eliminándolo desde el signo "menos". Igualmente si quiero agregar uno, clic en el signo "más" y si quiero borrar toda la clasificación darle clic en "borrar todo".

### Clasificación de Datos. Graduado
La simbolización graduada de una capa, generalmente se desarrolla a partir de sus atributos numéricos.

Es la representación de una variable continua que permite agrupar los elementos de una capa en intervalos o rangos numéricos y representar gráficamente cada rango de forma diferente (icono, tamaño, color, borde, entre otros).

Se calcula a partir de los valores contenidos en una columna de atributos numérica.

El estilo graduado puede calcularse a partir de los siguientes métodos estadísticos:

* Intervalos iguales, para la capa LIMITES MUNICIPIOS_MNES: divide el conjunto de valores entre el número de clases deseadas.
* Valor: TOT_POBLAC
* Rampa de color: elegir el que mejor represente los atributos del campo.
* Modo: Intervalo igual 
* Clases: probar con 5, 10 o más.
* Dar clic en clasificar.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/db206713-66c7-48c1-a256-ee8d4b05ec49)

Se pueden cambiar varios métodos estadísticos o también se puede setear de forma particular, haciendo click en los valores:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/637027f5-bb16-42b3-b6ad-1db847e78b8e)

### Clasificación de Datos. Puntos
La simbolización en los objetos tipo punto cuenta con algunos estilos especificos para clasificar como ser graduación de tamaño y el mapa de calor.

### Graduación de tamaño
En las propiedades de Simbología de una capa de puntos podemos utilizar el tamaño como caracteristica de representacion de los valores de sus atributos. Para ello:

* Abrimos las Propiedades de la capa con clic derecho sobre ella o doble clic sobre la misma.
* Seleccionamos la propiedad "Simbología"
* Tipo de clasificación "Graduado"
* en Valor elegimos el atributo a representar
* Método "Tamaño"
* Clasificar

  ![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/6afe15be-6078-4705-853c-2d31b6e69c70)

deberiamos ver algo así:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/a65aaafd-81c7-4754-9a44-12ac819f1a85)

### Mapa de Calor
Otra representación muy conocida son los Mapas de Calor, los que ayudan a evidenciar la distribución de la información sobre el territorio. Para ello:

* Abrimos las Propiedades de la capa con clic derecho sobre ella o doble clic sobre la misma.
* Seleccionamos la propiedad "Simbología"
* Tipo de clasificación "Mapa de calor"
* Podemos elegir una "Rampa de color" y Valor de Radio si es significativo según el comportammiento de nuestros datos.
* en Ponderar puntos podemos elegimos el atributo que va a dar valor a cada objeto sobre los demás
* Aceptar

  ![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/96b2841a-cd86-48a6-812d-86dc1336f019)

deberiamos ver algo así:

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/86767a31-1857-4640-8240-d837a60ec3f3)

# Complementos

continuará....



  











