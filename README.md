# capacitacion-SIG
Material de apoyo para capacitación en SIG con QGis

# Introduccion a los SIG

## Representaciones - Tipos de Datos

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/37c92320-461d-429c-911c-51f6ba7725db)

Los datos pueden tener tres formatos, Raster, Vectorial y Tabular;

El formato vectorial a la vez admite tres posibilidades: puntos, líneas o polígonos.

* Los puntos representan ubicaciones del tipo ciudades, personas, sucursales, avistamiento, incidente, toma de muestra, etc.
* Las líneas representan recorridos, como los ríos, las rutas o un caño de agua, etc.
* Los polígonos, por su parte representan áreas como parcelas, provincias, o zonas de distribución de un individuo, ANP, etc.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/5d20e959-dd21-461e-ba5a-8a01fd588306)

Cualquiera de estos objetos que llamamos "vectoriales" se compone de 2 partes la Geográfica y Descriptiva

Geográfica: Son pares de coordenadas que la ubican en el territorio.
Descriptiva: Son sus atributos (campos de valores) que le dan un sentido lógico a ese objeto representado.

La relación de los elementos en su aspecto lógico y geográfico es de 1 a 1, es decir que, a cada registro en una tabla se le corresponde un objeto en el mapa y viceversa. 

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/c6def464-ef0f-4bc8-977e-2b2f80804cb9)

Raster son set de datos continuos (a diferencia de los vectores que son discretos) están conformados por pequeños espacios uno a continuación del otro y cada uno con un valor determinado. Nuevamente con el concepto de parte geográfica y lógica.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/b4383c9d-a76b-462c-a6c7-9a73168b787a)



![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/c5552715-5e78-492e-a869-56abbd5acdf9)

Tabular refiere simplemente al conjunto de información o datos ordenada en campos para distintos objetos, pero que carecen del componenete geográfico. Situación que salvamos o que igualmente la aprovechamos llevandola al territorio identificando un valor o dato indice o lo que llamamos como identificador clave. (PK en bases de datos)(Puede ser único)

## Trabajo con capas y atributos

En escencia vamos a utilizar una herramienta para administrar, procesar, almacenar, etc los datos de nuestro interes transformandolos en capas que representen algo significativo en nuestro ámbito de estudio.

![image](https://github.com/russorl/capacitacion-SIG/assets/6954564/9c52e2a4-d7e1-49fc-a007-01d375027ca9)


## Sistemas de posicionamiento y coordenadas

Componente geográfica son pares de coordenadas.



