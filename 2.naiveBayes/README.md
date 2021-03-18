# Ejemplo - Naive Bayes

## Descripcion del contexto

La AGETIC realizó un estudio con el propósito de integrar tecnologías de software libre a los métodos de enseñanza-aprendizaje en Unidades Educativas Públicas. El objetivo de este estudio es obtener información inicial de información relevante sobre Tecnologías de Información y Comunicación TIC de las las Unidades Educativas Públicas.

## Descripción del dataset
|#|Nombre variable|Tipo|Pregunta de encuesta|
|-----|-------|------|------|
|#|parte_proyecto_inclusion| string| ¿Fue parte del proyecto Inclusión Digital?|
|#|sexo|	  string|¿Cuál es su sexo?|
|#|edad|  string| ¿Cuántos años tiene?|
|#|departamento|	  string|¿En qué departamento se encuentra la unidad educativa de la cual es profesor?   |
|#|ciudad|	  string| ¿En qué ciudad se encuentra la unidad educativa de la cual es profesor?   |
|#|unidad_educativa|	  string|¿Cuál es la Unidad Educativa donde imparte clases?|
|#|normalista|	 string| ¿Cuál es el nivel de instrucción adquirido? [Profesor Normalista]|
|#|tecnico|	 string| ¿Cuál es el nivel de instrucción adquirido? [Técnico]|
|#|licenciatura|	 string|¿Cuál es el nivel de instrucción adquirido? [Licenciatura]|
|#|especialidad|	 string|¿Cuál es el nivel de instrucción adquirido? [Especialidad]|
|#|maestria|	 string|¿Cuál es el nivel de instrucción adquirido? [Maestría]|
|#|doctorado|	 string|¿Cuál es el nivel de instrucción adquirido? [Doctorado]|
|#|otro|   string|¿Cuál es el nivel de instrucción adquirido? [Otro]|
|#|tiempo_ue_actual|	 string| ¿Cuánto tiempo es profesor de la Unidad Educativa que actualmente imparte clases?|
|#|tiempo_ue_actual_num|	 numeric| ¿Cuántos años es profesor de la Unidad Educativa que actualmente imparte clases?|
|#|area_imparte|	 string|¿Cúal es el área en la que imparte sus clases?|
|#|paso_curso_tec|	 string| ¿Pasó algún tipo de curso o capacitación respecto al uso de tecnologías en aula?|
|#|curso|	 string|  ¿Cuál es el curso o capacitación respecto a tecnologías en el aula?|
|#|pc_casa|	 string|¿Tienen computadora en su casa?|
|#|laptop_escritorio|	 string|¿Es una computadora de escritorio o una laptop?|
|#|num_pc|	 numeric|  ¿Cuántas computadoras (escritorio o portátil) tiene?|
|#|tablet|	 string|  ¿Tienen tabletas en su casa?|
|#|num_tablet|	 numeric| ¿Cuántas tabletas tiene en casa?|
|#|origen_pc|	 string|¿La computadora de donde fue obtenida?|
|#|pc_llenado|	 string| ¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Llenado de formularios y planillas (MINEDU)]|
|#|pc_juegos|	 string|¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Juegos]|
|#|pc_estudio|	 string|¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Estudio]|
|#|pc_musica|	 string|¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Música]|
|#|pc_redes|	 string|¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Redes Sociales]|
|#|pc_nada|	 string|¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Ningún uso]|
|#|pc_planificar|	 string|¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Planificar clases]|
|#|pc_clases|	 string| ¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Uso en clases]|
|#|pc_videos|	 string| ¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Vídeos]|
|#|pc_internet|	 string|¿Cuál es el uso que le da a la computadora de escritorio, portátil o tablet?  [Internet]|
|#|tiene_celular|	 string|¿Tiene Teléfono celular?|
|#|tiene_smartphone|	 string|¿El celular con el que cuenta es inteligente (smartphone)?|
|#|cel_llamadas|	 string| ¿Qué uso le da al celular?  [Llamadas]|
|#|cel_musica|	 string| ¿Qué uso le da al celular?  [Música]|
|#|cel_juegos|	 string| ¿Qué uso le da al celular?  [Juegos]|
|#|cel_fotos|	 string| ¿Qué uso le da al celular?  [Fotos]|
|#|cel_redes|	 string| ¿Qué uso le da al celular?  [Uso de Redes Sociales]|
|#|cel_text|	 string| ¿Qué uso le da al celular?  [Mensajes de texto]|
|#|cel_videos|	 string| ¿Qué uso le da al celular?  [Vídeos]|
|#|cel_internet|	 string| ¿Qué uso le da al celular?  [Internet]|
|#|internet_casa|	 string| ¿Tienes acceso a internet en tu casa?|
|#|internet_movil|	 string|¿Tiene acceso a internet en su celular móvil?|
|#|internet_colegio|	 string| ¿Tienes acceso a internet en el colegio?|
|#|usa_facebook|	 string|De las siguientes redes sociales ¿cuáles utiliza? [Facebook]|
|#|usa_youtube|	 string| De las siguientes redes sociales ¿cuáles utiliza? [You Tube]|
|#|usa_whatsapp|	 string|De las siguientes redes sociales ¿cuáles utiliza? [WhatsApp]|
|#|usa_messenger|	 string|De las siguientes redes sociales ¿cuáles utiliza? [Messenger]|
|#|usa_instagram|	 string|De las siguientes redes sociales ¿cuáles utiliza? [Instagram]|
|#|usa_twiter|	 string|De las siguientes redes sociales ¿cuáles utiliza? [Twitter]|
|#|usa_linkedin|	 string|De las siguientes redes sociales ¿cuáles utiliza? [LinkedIn]|
|#|usa_skype|	 string|De las siguientes redes sociales ¿cuáles utiliza? [Skype]|
|#|dias_uso_internet|	 numeric|¿Cuántos días a la semana utiliza internet?|
|#|so|	 string|¿Qué sistema operativo utilizas en tu computadora?|
|#|conoce_soft_libre|	 string| ¿Sabes que es el Software Libre?|
|#|existe_laboratorio|	 string| En su unidad educativa ¿Existe un aula específica equipada para el uso de computadoras?|
|#|sabe_inclusion_digital| string| ¿Sabe de lo que trata el proyecto Inclusión Digital?|

