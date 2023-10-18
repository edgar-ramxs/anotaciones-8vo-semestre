# Sistema de recomendacion

- Usuario

  - Nombre
  - Apellido
  - rut
  - correo
  - contraseña
  - carrera
  - semestre / materias interesadas
  -

- Documentacion oficial

- Ejercicio
  - Nombre
  - Tema o Clasificacion
  - Nivel
  - Descripcion
  - Lenguaje
  - Meta:
    - fecha
    - version
    - patron
    - ranking

## [Sistemas de Recomendación - Machine Learning - Clase 11 - Parte 1](https://www.youtube.com/watch?v=9KWVIZJfm8Q)

### Notas

- Definicion (SR) son tecnicas para sugerir items apropiados a un usuario
- Se aplican en contextos donde un usuario por si mismo no puede evaluar correctamente ue consumir (que se puede consumir es un item )
  - gran mayoria de oferta
  - muchos elementos sin reconocimineto para el usuario
- Sugerencia personalizadas
- items mas populares o caracteristica uqe definan un cojunto de elementos
- preferecias de un usuario minimo a maximo
- naturaleza de los datos (explicitos o implicitos)

  - exp: puntaje o likes del usuario
  - imp: infieren las preferencias (clicks, mover el mouse sobre un items, consumo de series, matrones de busqueda)

- Proceso aquitectura

  - recoleccion de los datos
  - modelo de recomendaciones
  - post procesamiento de la recomendacion
    - en este punto se suelen incluir ciertas reglas para mejorar las sugerencias y evitar las sugerencias inutiles.
  - Modelos online: Operar en tiempo real, cuando ingrese el usuario se tiene que recomendar algun tipo de ejercicio.
    - procesamiento en tiempo real
    - costo de los algoritmos para el analisis del modelo (requerimiento de computo optimizados)
  - interfaz de usuario

- Enfoques
  - Basados en popularidad (Estadisticas)
  - Collaborative Filtering (Filtrado colaborativo)
    - comportamiento de usuarios similares
  - Content-based Filterin (Filtado basdo en el contenido)
    - contenido del ejercicio en si
  - Hibridos ( Combinacion de dos o mas enfoques )

> Algebra lineal, tecnicas heuristicas, deep learning o redes neuronales. Factorizacion de matrices

#### Filtrado colaborativo

- usuarios dan rating a un elemento
- patrones de los usuarios
- caracteristicas con elementos o usuarios similares
- crear relaciones entre individuos
- datos historicos (co relacion linear, similitud de coseno)
- tecnicas de DL o ML para predecir los raiting como clasificador

Filtrado colaborativo basado en Memoria:

> User-item filtering : De un usuario se buscan patrones que los identifique con otros usuarios, ya que se le puede recomendar elementos que los otros usuarios les han gustado.
> item-item filtering : Matriz de usuarios y elementos. Similitudes entre elementos que hayan sido rankeados

Similitud coseno

Modelos basados en contenido

- Caracteristicas: genero, año, texto, titulo, descripcion, tablas de contenido con las que se pueden usuar un NLP.
- keywords
- Ventajas y desventajas [42:00]
- extraccion de features: TF_IDF

filtrado colaborativo basado en modelos [52:00]

## [UWE en Sistema de Recomendación de Objetos de Aprendizaje. Aplicando Ingeniería Web: Un Método en Caso de Estudio](http://40.71.171.92/bitstream/handle/123456789/667/relais-v2-n3-137-143.pdf?sequence=1&isAllowed=y)

- UWE (UML Web Engineering), UML, Estereotipo, AGORA, Objetos de Aprendizaje.

Introduccion

> La aplicación Web sugiere a los usuarios una colección de recursos educativos que pueden resultar útiles para la creación de un Objeto de Aprendizaje compuesto.

APLICACIÓN DEL MÉTODO EN CASO DE ESTUDIO

> La gestión de los Objetos de Aprendizaje involucra factores como el objetivo educativo, el estilo de aprendizaje, el grado de interacción, el diseño de la interfaz de usuario, las estructuras de almacenamiento, los descriptores, etc. Además, incluye varios procesos como la catalogación, la búsqueda y recuperación, la generación y composición de objetos, etc.

```TXT
Para ello, se considera el uso de diversas tecnologías y
aspectos informáticos relacionados con la Ingeniería de
Software, el Soft-Computing, la Ingeniería del Conocimiento,
la Web semántica, la Minería de datos y otras herramientas,
con el fin de establecer modelos, técnicas e instrumentos que
faciliten el desarrollo, la explotación y evaluación de todos tipo
de recursos orientados a la instrucción y el aprendizaje.
```

```TXT
El usuario interesado en realizar la creación de un objeto de
aprendizaje compuesto deberá iniciar sesión en la aplicación y
si es la primera vez, deberá registrarse previamente, llenando
un formulario que corresponde a su perfil. Esta información
permitirá que la aplicación personalice las recomendaciones a
dicho usuario.
```

## [EmoRemSys: Sistema de recomendación de recursos educativos basado en detección de emociones](https://pdfs.semanticscholar.org/0575/6ea8c9995e49cd20e120612d9e1d620fdbbf.pdf)

> uno de los problemas que se les presentan a los estudiantes al hacer búsquedas específicas de recursos en diferentes repositorios es que se encuentran con un gran número de resultados y en ocasiones pierden demasiado tiempo para seleccionar un recurso o no encuentran lo que necesitan.

- EmoRemSys
- PBRecS
- SocConnect

```TXT
En (Poy & Gonzales-Aguilar, 2014) se presentó un estudio y análisis de
los MOOC (Cursos online abiertos y masivos), una de las herramientas que ha surgido
de la combinación de e-learning y modelos de redes sociales, la cual se ha integrado
en muchos programas educativos transformando las organizaciones e-learning a nivel
mundial. A partir de los estudios previos, se identificaron en el análisis cuatro factores
críticos que son (1)el diseño de software educativo, (2)las tasas de abandono, (3)el alcance
de la universalización, y (4)la estrategia de negocio subyacente a esta oferta educativa.
```

- Apache Mahout
- arquitectura (pag 5)

_Se quita los procesos de analizacion de sentimientos y obtencion de imagen_

```TXT
Se desarrollaron un contjunto de
componentes necesarios para el correcto funcionamiento de este sistema, entre los
cuáles están: el desarrollo del servició Web encargado de realizar las recomendaciones
mediante el filtrado colaborativo con la API de Apache Mahout, los componentes
de análisis sentimental en donde se usa la API de SkyBiometry para la detección del
sentimiento del estudiante, el analizador de peticiones que sirve como puerta de enlace
a la petición que realiza el usuario al momento de ceder o no las funcionalidades de
su cámara Web, así como también el uso de diversas tecnologías para complementar
el sistema como el uso de CSS3 para los estilos de la página, JQuery para el uso de
la cámara Web y las fotografías automáticas del estudiante, Ajax para la funcionalidad
de almacenar la fotografía automáticamente en el servidor sin necesidad de salir de la
página, el uso de Flash Player para la visualización de los recursos educativos de tipo
video en formato.flv para el correcto funcionamiento en los diferentes browser que hay
en la actualidad, el uso de Google Docs para la visualización de los recursos educativos
que están en formato office, HTML5 para ocupar los formatos en imagen y audio de los
recursos.
```

Desfasado en el tiempo. _27/03/2016_

## [Realidad aumentada y sistemas de recomendación grupales: Una nueva perspectiva en sistemas de destinos turísticos](http://www.scielo.org.ar/scielo.php?pid=S1851-17322014000100003&script=sci_arttext&tlng=pt)

> Se presenta en este trabajo un enfoque de sistema de realidad aumentada aplicada al turismo basada en el contexto que utiliza técnicas de recomendación para visitas en grupo en un sistema integrado de gestión de destinos (SIGD).

> Un caso especial son los sistemas de recomendación basados en casos en los que cada uno que se recupera representa una recomendación anterior de un producto similar al que el usuario desea. Estos sistemas cuentan con una base de casos que se compone de problemas resueltos anteriormente junto con la solución tomada. De este modo los nuevos problemas se resuelven adaptando soluciones anteriores encontradas para resolver problemas similares.

## [Personalización de Sistemas de Recomendación](https://www.researchgate.net/profile/Francisco-Garcia-Penalvo/publication/268344600_Personalizacion_de_Sistemas_de_Recomendacion/links/54d0ab3e0cf20323c21888ad/Personalizacion-de-Sistemas-de-Recomendacion.pdf)

```TXT
Este documento describe un sistema de recomendación basado en agentes
adaptativos, actualmente en desarrollo, que integra la personalizacion de las
recomendaciones al usuario a la vez que la estrategia comercial del sitio. El sistema
de recomendación implementa una arquitectura propia de comercio electrónico
denominada e-CoUSAL [4], pero perfectamente trasladable a cualquier sector de
oferta de servicios en Internet.
```


