# Factorio

Hola soy el ingeniero de la planta Factorio donde extraemos hierro y carbón. Necesito un sistema que me ayude a planificar distintas formas de organizar nuestro circuito de producción. En la fábrica contamos con dos extractores, uno de carbón y otro de hierro, dos cintas transportadoras (dato de color…una es roja y la otra azul) y una caja donde almacenamos las menas de carbón y hierro producidas. El circuito que tenemos hoy en la fábrica es el siguiente:

![alt text](https://github.com/algoritmos-iii/ejercicios-poo-soluciones/blob/master/circuito.png?raw=true)

Ahora necesito poder hacer funcionar este circuito. Pero pronto necesitaremos poder conectar los componentes de otra forma.

Ahh...me olvidé de contarles cómo funciona esto. El circuito tiene un ciclo de producción, hoy tenemos configurado para que ese ciclo sea el siguiente: funciona una vez el extractor de carbón, deposita la mena de carbón extraída en su cinta, luego funciona el extractor de hierro, dejando la mena de hierro en su cinta, luego funciona la cinta conectada al extractor de hierro, y luego la otra cinta, dejando las dos menas en la caja contenedora.

Tienen que modelar con nuestros queridos objetos el funcionamiento del circuito del ingeniero de Factorio. 

Sugerencia: simplifiquen el problema. Por ejemplo, no interesa cómo el extractor de hierro produce hierro. Les recomendamos descomponer la problemática en los siguientes escenarios:

Escenario 1: simplifiquemos el circuito, quiero conectar el extractor de carbón a una caja contenedora. Hago andar el extractor y veo que en la caja hay una mena de carbón. Por ejemplo si hago andar el extractor dos veces entonces en el contenedor hay dos menas de carbón.

Escenario 2: un escenario más avanzado ahora sería conectar el extractor de carbón a la cinta y la cinta a la caja. Si hago andar al extractor, entonces veo que hay una mena de carbón en la cinta. Luego si hago andarla cinta, veo que el contenedor tiene la mena de carbón que estaba en la cinta.

Escenario 3: circuito completo de la fábrica.
Tips: en el ambiente tienen colecciones ordenadas.

**¿Cómo crear una colección ordenada?**
unaColeccion := OrderedCollection new.

** ¿Cómo agregarle un objeto a una colección?**
unaColeccion add: ‘Hola’

**¿Cómo agregar todos los elementos de una colección a otra colección?**
otraColeccion := OrderedCollection new.
otraColeccion addAll: unaColeccion


**¿Cómo contar la cantidad de elementos que cumplen con cierta condición? Por ejemplo la cantidad de unos que tenemos.**
unaColeccion count: [ :cadaElemento | cadaElemento = 1 ]
