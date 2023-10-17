# Sistema de recomendacion


## [Sistemas de Recomendación - Machine Learning - Clase 11 - Parte 1](https://www.youtube.com/watch?v=9KWVIZJfm8Q)

### Notas
+ Definicion (SR) son tecnicas para sugerir items apropiados a un usuario
+ Se aplican en contextos donde un usuario por si mismo no puede evaluar correctamente ue consumir (que se puede consumir es un item )
    - gran mayoria de oferta
    - muchos elementos sin reconocimineto para el usuario
+ Sugerencia personalizadas
+ items mas populares o caracteristica uqe definan un cojunto de elementos 
+ preferecias de un usuario minimo a maximo
+ naturaleza de los datos (explicitos o implicitos)
    - exp: puntaje o likes del usuario
    - imp: infieren las preferencias (clicks, mover el mouse sobre un items, consumo de series, matrones de busqueda)

+ Proceso aquitectura
    - recoleccion de los datos
    - modelo de recomendaciones
    - post procesamiento de la recomendacion
      * en este punto se suelen incluir ciertas reglas para mejorar las sugerencias y evitar las sugerencias inutiles. 
    - Modelos online: Operar en tiempo real, cuando ingrese el usuario se tiene que recomendar algun tipo de ejercicio. 
      * procesamiento en tiempo real
      * costo de los algoritmos para el analisis del modelo (requerimiento de computo optimizados)
    - interfaz de usuario

+ Enfoques
  - Basados en popularidad (Estadisticas)
  - Collaborative Filtering (Filtrado colaborativo) 
    * comportamiento de usuarios similares
  - Content-based Filterin (Filtado basdo en el contenido)
    * contenido del ejercicio en si
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



