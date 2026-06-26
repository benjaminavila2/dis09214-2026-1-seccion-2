# Repo Exámen

---

# *Información del Proyecto*

## *Nombre del proyecto*  
Desigualdad de Género en la Política Chilena

## *Autores*  
Benjamin Ávila y Sara Graadt

---

# *Descripción Objetiva*

### "regla del sistema":
Dos personajes tienen el mismo objetivo (llegar al poder), pero el algoritmo no les entrega las mismas condiciones para alcanzarlo. La desigualdad no está representada por el resultado final, sino por las reglas de interacción que gobiernan el sistema.

## *¿Qué es el proyecto?*

Es una visualización interactiva desarrollada en p5.js que representa de forma visual y dinámica la desigualdad de género en el acceso al poder político en Chile.

 En lugar de representar datos estadísticos de forma convencional, el proyecto transforma la información y el concepto de desigualdad en una experiencia interactiva. El usuario participa activamente manipulando a ambos personajes y observando cómo las reglas del sistema generan comportamientos diferentes para cada uno, haciendo evidente la desigualdad de oportunidades. 

Nuestro  proyecto busca evidenciar lo difícil y arduo que es para el género femenino llegar a cargos políticos en Chile, mostrando al mismo tiempo cómo los hombres logran llegar mucho más rápido al poder, representado de manera explícita una manera clara la desigualdad de género presente en instituciones políticas como lo son el Senado, la Cámara de Diputadas y Diputados, las alcaldías del país, hasta la mismísima presidencia.


---

## *¿Qué se ve en pantalla?*

El proyecto está dividido en tres momentos de navegación.

La primera pantalla corresponde al inicio del proyecto, donde se presenta el título y un botón que permite acceder a la experiencia.

La segunda pantalla entrega las instrucciones necesarias para comprender la interacción, explicando cómo se controla cada personaje y cómo funciona el indicador de presión social.

Finalmente, la tercera pantalla corresponde a la simulación principal. En ella aparecen dos personajes que representan a un hombre y una mujer intentando ascender dentro del sistema político. Ambos se desplazan verticalmente, pero utilizando mecanismos completamente distintos, generando una comparación inmediata entre sus posibilidades de alcanzar el poder.

A medida que ambos avanzan, el fondo cambia progresivamente desde el Congreso Nacional hacia el Palacio de La Moneda, simbolizando el recorrido político desde los espacios legislativos hasta el máximo nivel del poder ejecutivo.

---

## *¿Qué elementos visuales aparecen?*

La composición visual está construida mediante elementos simples que funcionan como símbolos.

Entre ellos aparecen:

- Un personaje masculino vestido formalmente que utiliza un jetpack para ascender rápidamente.
- Un personaje femenino vestida con traje ejecutivo que asciende únicamente mediante una escalera.
- Una escalera vertical que representa el esfuerzo constante y progresivo.
- Un jetpack que simboliza los privilegios o ventajas estructurales.
- Una transición entre imágenes del Congreso Nacional y el Palacio de La Moneda.
- Nubes en movimiento que aportan profundidad y dinamismo al escenario.
- Un indicador porcentual de presión social controlado por el movimiento horizontal del mouse.
- Botones de navegación, reinicio e instrucciones.
  
Cada uno de estos elementos tiene una función dentro del sistema y contribuye a construir la metáfora visual de la desigualdad.


-----

# *Descripción Conceptual*

## *Idea central del proyecto*

La idea principal del proyecto consiste en representar que el acceso al poder político no ocurre bajo las mismas condiciones para todas las personas.

Mientras históricamente los hombres han ocupado la mayor parte de los cargos de representación política y han contado con estructuras que favorecen su participación, las mujeres han debido enfrentar múltiples barreras sociales, culturales e institucionales para alcanzar esos mismos espacios.

Esta diferencia se traduce en el sistema mediante dos formas completamente distintas de movimiento.

El hombre posee un jetpack que le permite ascender continuamente mientras el usuario mantiene presionado el mouse o la barra espaciadora. Su progreso es rápido, fluido y prácticamente sin obstáculos.

La mujer, en cambio, solo puede subir un peldaño cada vez mediante acciones individuales del usuario. Cada avance requiere un esfuerzo adicional, representando el camino más complejo que históricamente han debido recorrer muchas mujeres para acceder a posiciones de liderazgo político.

De esta forma, el algoritmo deja de ser solamente una secuencia de instrucciones y pasa a transformarse en una representación simbólica de una realidad social.


---

## *Regla de oro del sistema*

La lógica principal puede resumirse en la siguiente regla:

> “Mientras más privilegios estructurales posee un personaje, más fácil y rápido resulta su ascenso hacia el poder.”

Esta regla se implementa mediante distintas operaciones del programa.

El hombre posee un movimiento continuo, mientras que la mujer solamente puede avanzar en intervalos fijos de un peldaño.

Además, existe una segunda regla visual:

> “A mayor progreso de los personajes, el escenario transiciona desde el Congreso Nacional hacia el Palacio de La Moneda.”

Esta transformación convierte el espacio político en una representación visual del recorrido hacia las posiciones de mayor poder dentro del Estado chileno.

---

## *¿Cómo se relaciona esta lógica con la problemática de género?*

La desigualdad de género no se representa mediante cifras o gráficos estadísticos, sino mediante diferencias en las reglas del propio sistema.

Los dos personajes persiguen exactamente el mismo objetivo: ascender.

Sin embargo, el programa no les entrega las mismas posibilidades para lograrlo.

Mientras uno puede avanzar constantemente con un solo gesto, la otra necesita repetir una acción varias veces para obtener un progreso equivalente.

Esta diferencia busca representar las barreras estructurales presentes en la política chilena, donde históricamente las mujeres han enfrentado mayores dificultades para acceder a cargos de representación, liderazgo y toma de decisiones.

Así, el código se convierte en una metáfora computacional de la desigualdad.


---

# *Input / Output y Sistema*

## *¿Qué datos entran? (INPUT)*

El sistema recibe información en tiempo real proveniente de la interacción del usuario y de variables internas del programa.

#### Interacción del usuario

- Clic del mouse (mousePressed)
- Posición horizontal del mouse (mouseX)
- Barra espaciadora (SPACE)
- Flecha hacia arriba (UP_ARROW)
- Flecha hacia abajo (DOWN_ARROW)
-Variables del sistema
- Estado de la aplicación (estado)
- Posición vertical del hombre (hombreY)
- Posición vertical de la mujer (mujerY)
- Estado del jetpack (jetpackFuego)
- Posición y velocidad de las nubes
- Tamaño de la ventana (windowWidth y windowHeight)


### *Datos utilizados*

| Elemento  | Representación |
|---|---|
| Congreso Nacional |Inicio del recorrido político y espacio legislativo.
| Palacio de La Moneda | Meta del ascenso y representación del máximo poder ejecutivo. |
| Hombre | Representa los privilegios históricos masculinos para acceder al poder político. |
| Mujer | Representa el mayor esfuerzo requerido para alcanzar espacios de representación política. |
| Escalera | Simboliza las barreras estructurales y el ascenso progresivo. |
| Jetpack | Simboliza las ventajas y facilidades históricas asociadas al género masculino. |

#### Referencias conceptuales
- Participación histórica de mujeres en la política chilena.
- Congreso Nacional de Chile.
- Palacio de La Moneda.
- Estudios sobre desigualdad de género y representación política.

---

## *¿Cómo se procesan y transforman?*

El programa transforma constantemente los datos ingresados mediante diversas funciones y reglas computacionales.

| Función | Transformación |
| --- | --- |
| mousePressed() | Cambia de pantalla, reinicia el sistema o hace avanzar a la mujer. |
| keyPressed() | Permite subir o bajar a la mujer exactamente un peldaño. |
| map() | Convierte la posición del mouse en un porcentaje de presión social. |
| map() | Calcula la transición entre Congreso y La Moneda según el progreso de ambos personajes. |
| constrain() | Limita el movimiento de ambos personajes dentro del escenario. |
| random() | Genera posiciones, tamaños y velocidades distintas para las nubes y el fuego del jetpack. |
| if | Determina qué pantalla mostrar y cómo responde cada personaje según la interacción del usuario. |


---

## *¿Qué respuesta visual producen? (OUTPUT)*

- Ascenso continuo del hombre mediante el jetpack.
- Ascenso escalonado de la mujer utilizando la escalera.
- Activación y animación del fuego del jetpack.
- Movimiento continuo de las nubes.
- Aparición progresiva del Palacio de La Moneda.
- Desaparición gradual del Congreso Nacional.
- Desplazamiento del fondo simulando avance hacia el poder.
- Actualización en tiempo real del indicador de presión social.
- Cambio entre pantallas (Inicio, Instrucciones e Interacción).
- Reinicio completo de la simulación.

---

# *Pensamiento Computacional*

## *Reglas que gobiernan el sistema*

| Elemento | Regla computacional |
| --- | --- |
| Hombre | Asciende continuamente mientras se mantiene presionado el mouse o la barra espaciadora. |
| Mujer | Solo avanza un peldaño (60 px) por cada acción del usuario. |
| Jetpack | Solo aparece cuando el hombre está ascendiendo. |
| Fondo | La opacidad del Congreso disminuye mientras aumenta la de La Moneda según el progreso promedio. |
| Nubes | Se desplazan constantemente hacia la izquierda y reaparecen al salir de pantalla. |
| Movimiento | constrain() impide que los personajes abandonen los límites del escenario. |
| Estados | La interfaz cambia entre Inicio, Instrucciones e Interacción mediante la variable estado. |

---

## *Explicación del sistema de interactividad*

La interacción está diseñada para que el usuario experimente directamente una desigualdad en las posibilidades de ascenso.

El personaje masculino responde a una interacción continua: basta con mantener presionado el mouse o la barra espaciadora para que ascienda de forma constante gracias al jetpack. Esta mecánica representa un acceso más directo y privilegiado hacia el poder político.

En contraste, el personaje femenino requiere una acción individual para avanzar cada peldaño de la escalera. Cada pulsación de la flecha superior o cada clic en la zona de la escalera produce un único avance, obligando al usuario a realizar un esfuerzo repetitivo para alcanzar la misma altura.

Finalmente, el progreso conjunto de ambos personajes modifica el escenario mediante una transición gradual entre el Congreso Nacional y el Palacio de La Moneda. De esta forma, el entorno también responde a la interacción del usuario, reforzando visualmente la idea de acercarse a los espacios de mayor poder político.


# *Referentes*

## *Referentes Visuales*

### *Barbara Kruger*
Artista visual feminista reconocida por utilizar tipografía, fotografía y mensajes políticos directos para cuestionar las estructuras de poder, el género y los medios de comunicación. Inspiró el uso de un contraste visual dentro del proyecto.

### Guerrilla Girls
Colectivo feminista de artistas fundado en 1985 que denuncia la desigualdad de género mediante afiches, estadísticas, humor y visualización de datos.

### *Lotty Rosenfeld*
Artista chilena perteneciente a la Escena de Avanzada. Utilizó intervenciones urbanas y símbolos visuales para cuestionar el poder político y las estructuras patriarcales en Chile durante la dictadura. Referente por el uso del espacio visual como denuncia política.

---

## *Referentes Teóricos*

### *Feminism for the 99%*  
Texto sobre desigualdad estructural de género en sistemas políticos y económicos.

### *Simone de Beauvoir*
Autora de “El segundo sexo”, obra fundamental para comprender la desigualdad histórica entre hombres y mujeres y la exclusión femenina en espacios de poder.

### Comisión Económica para América Latina y el Caribe
Organismo de Naciones Unidas que publica investigaciones sobre igualdad de género y participación política en América Latina.

### Ministerio de la Mujer y la Equidad de Género
Institución pública encargada de promover la igualdad entre hombres y mujeres en Chile.

---

## *Referentes Históricos*

### *Sufragio femenino en Chile (1949)*  
Contexto histórico fundamental para comprender la representación política femenina en Chile.

### Ley de Cuotas Electorales (2015)
Estableció un porcentaje mínimo de candidaturas femeninas para promover una mayor representación de mujeres en el Congreso.

## *Sufragistas chilenas*
Movimiento feminista que logró el derecho a voto femenino en elecciones presidenciales en Chile en 1949. Referente histórico clave para contextualizar la baja representación política femenina actual.

### *Revuelta feminista chilena de 2018*
Movimiento estudiantil y social que visibilizó masivamente desigualdades estructurales de género en Chile, utilizando performance, gráfica y activismo visual como herramientas de protesta. 

### Convención Constitucional (2021)
Fue el primer órgano constituyente del mundo elegido con paridad de género.


---
