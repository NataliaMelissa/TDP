# TDP
Trabajos del curso de Taller de Desempeño Profesional. El curso se divide en 5 sprints, donde en cada sprint eres asignado para ayudar en un proyecto de los alumnos de tesis (Taller de proyecto 1 y taller de proyecto 2). Por eso las carpetas están divididas según el sprint.

## Sprint 2:
Fuí asignada para ayudar en un chatbot desarrollado en aws. La función se creó utilizando los servicios de Amazon Lambda en AWS. Las intenciones que tiene el chatbot son de dar la bienvenida a la persona, darle motivación y/o ayudarle con sus cursos. El chatbot fue realizado utilizando Amazon Lex V2 y el lambda fue realizado en Amazon Lambda con los formatos de respuesta para amazon v2.

Para este sprint el desarrollo del chatbot se realizó sola ya que fuí el único recurso asignado al proyecto. 

**Intenciones del Bot:** son como el objetivo que va a cumplir el chatbot, 1 intención = 1 objetivo.
- Bienvenida: Recibe a la persona, les pregunta su nombre y las deriva a las intenciones correspondientes según lo que necesiten.
- AyudaCurso: la persona necesita ayuda con los cursos, el chatbot le envía información para que le ayude a repasar los cursos.
- Motivación: la persona necesita un poco de motivación/ayuda porque está muy estresada, cansada, etc.

**Slots del Bot:** slots son el input que recibe el chatbot y tienen un tipo de dato, son como las variables.
- Slots intención Bienvenida:
  - Usuario: es de tipo alphanumérica y recibe el nombre de usuario de la persona hablando con el Bot.
  
- Slots de la intención AyudaCurso:
  - NivelComprension: contiene cuál es el nivel de comprensión de la persona en general, el rango de valores es del 1-5 y el tipo de dato es numérico.
  - NombreCurso: contiene el nombre del curso y su tipo de dato es la ranura creada NombreCurso
  - TipoEstudio: contiene la información sobre si la persona prefiere estudiar en grupo o sola (esos son sus posibles valores) y su tipo de dato es la ranura creada TipoEstudio.
  - TipoComprension: contiene la información sobre si la persona prefiere repasar con un podcast, video y contenido visual (posibles valores: contenido visual, video o podcast y las permutaciones para cada valor) y el tipo de dato es la ranura creada TipoComprension.

- Slots de la intención Motivacion:
  - SentimientoEmocional: contiene el nivel emocional de la persona para saber qué tan calmada/tranquila está, su valor es del 1-5 (1 = muy estresada, 5 = calmada), el tipo de dato es numérico.
  - UtilidadVideo: contiene si el video recibido fue útil o no, sus posibles valores son sí o no (y las permutaciones de estos), el tipo de dato es una ranura creada llamada SiNo
  - CoachPsicologo: contiene si la persona prefiere ser ayudada por un coach o un psicólogo, sus posibles valores son: coach o psicólogo (y las permutaciones de estas), el tipo de dato es una ranura llamada CoachPsicologo.

## Sprint 3:
Fuí asignada para apoyar al mismo chatbot que en el sprint 2, por lo que se tuvo que desarrollar en aws utilizando amazon Lex v1 y amazon Lambda. Se tuvo que volver a crear el chatbot que estaba en Amazon lex v2 (versión 2 de amazon) a Amazon Lex V1 (versión 1 de amazon). El lambda se encarga de controlar la conversación: redirige a las intenciones necesarias, valida los valores de los slots, etc. Los archivos en la carpeta Sprint 3 son: index, motivation, helpCourse, Welcome y utils. Index es el archivo principal que controla todo y llama a los otros archivos para jalar la lógica que necesita. El archivo helpCourse contiene toda la lógica para realizar las validaciones, respuestas, etc. de la intención AyudaCurso. El archivo motivation contiene toda la lógica para realizar las validaciones, respuestas, etc. de la intención Motivacion. El archivo welcome contiene la lógica de la intención Bienvenida. El archivo utils, contiene los formatos de respuesta en de aws lambda v1 necesarios. 

Para este sprint, el desarrollo del chatbot y los lambda se tuvo ayuda de Marco (otro recurso) quienes fuímos asignados para apoyar. El Lambda fue realizado por ambos, pero Marco realizó sólo los archivos de Utils, Welcome y gran parte del archivo de helpCourse, la mitad del archivo index. Yo me encargué de realizar el archivo de Motivacion, terminar el archivo de helpCourse (agregar la opción de videos del slot TipoComprension), terminar index (poner los comandos necesarios para que funcione la intención motivación). 

**Intenciones del Bot:** son como el objetivo que va a cumplir el chatbot, 1 intención = 1 objetivo.
- Bienvenida: Recibe a la persona, les pregunta su nombre y las deriva a las intenciones correspondientes según lo que necesiten.
- AyudaCurso: la persona necesita ayuda con los cursos, el chatbot le envía información para que le ayude a repasar los cursos.
- Motivación: la persona necesita un poco de motivación/ayuda porque está muy estresada, cansada, etc.

**Slots del Bot:** slots son el input que recibe el chatbot y tienen un tipo de dato, son como las variables.
- Slots intención Bienvenida:
  - Usuario: es de tipo alphanumérica y recibe el nombre de usuario de la persona hablando con el Bot.
  
- Slots de la intención AyudaCurso:
  - NivelComprension: contiene cuál es el nivel de comprensión de la persona en general, el rango de valores es del 1-5 y el tipo de dato es numérico.
  - NombreCurso: contiene el nombre del curso y su tipo de dato es la ranura creada NombreCurso
  - TipoEstudio: contiene la información sobre si la persona prefiere estudiar en grupo o sola (esos son sus posibles valores) y su tipo de dato es la ranura creada TipoEstudio.
  - TipoComprension: contiene la información sobre si la persona prefiere repasar con un podcast, video y contenido visual (posibles valores: contenido visual, video o podcast y las permutaciones para cada valor) y el tipo de dato es la ranura creada TipoComprension.

- Slots de la intención Motivacion:
  - SentimientoEmocional: contiene el nivel emocional de la persona para saber qué tan calmada/tranquila está, su valor es del 1-5 (1 = muy estresada, 5 = calmada), el tipo de dato es numérico.
  - UtilidadVideo: contiene si el video recibido fue útil o no, sus posibles valores son sí o no (y las permutaciones de estos), el tipo de dato es una ranura creada llamada SiNo
  - CoachPsicologo: contiene si la persona prefiere ser ayudada por un coach o un psicólogo, sus posibles valores son: coach o psicólogo (y las permutaciones de estas), el tipo de dato es una ranura llamada CoachPsicologo.
