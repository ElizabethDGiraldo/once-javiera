# Guía Completa de Ingeniería de Requerimientos: Conceptos, Elicitación, Documentación y Viabilidad

---

## 1. Profundización del Concepto de Requerimiento

### Definición Formal (IEEE 830)
Un requerimiento es una propiedad documentada que un sistema debe poseer para resolver un problema o lograr un objetivo. Se trata de una declaración verificable de una funcionalidad, restricción o característica de calidad.
* **El criterio fundamental:** Si una necesidad no se puede escribir de forma clara ni se puede comprobar una vez construida, entonces no constituye un requerimiento.

### Niveles de Abstracción
El proceso de ingeniería consiste en traducir las expectativas del usuario en especificaciones técnicas a través de tres niveles:
1. **Necesidad del Usuario (Nivel Informal/Emocional):** La manifestación inicial del problema. Ejemplo: "Quiero saber qué hay de comida para no perder el viaje a la cafetería".
2. **Requerimiento del Sistema (Nivel Formal/Traducido):** La traducción estructurada de la necesidad. Ejemplo: "El sistema debe mostrar el menú del día actualizado a todos los estudiantes autenticados".
3. **Especificación Técnica (Nivel de Detalle de Desarrollo):** La definición exacta para los programadores. Ejemplo: "La API `/menu/dia` debe retornar un JSON con los platos del día, en menos de 300 ms, usando HTTPS".

### Fuentes de Requerimientos (Stakeholders)
Los requerimientos provienen de diferentes actores con intereses específicos en el proyecto:
* **Usuarios Finales:** Operan el sistema diariamente y conocen los detalles prácticos.
* **Clientes y Patrocinadores:** Financian el proyecto y definen las metas del negocio.
* **Leyes y Normativas:** Regulaciones obligatorias del entorno (como la protección de datos).
* **Sistemas Externos:** Plataformas de software con las que el sistema debe integrarse.

### Las 7 Cualidades de un Buen Requerimiento
* **Necesario:** Si se elimina, el sistema deja de cumplir su propósito principal.
* **No ambiguo:** Admite una única interpretación posible.
* **Verificable:** Se puede diseñar una prueba para comprobar si se cumple o no.
* **Consistente:** No entra en contradicción con ningún otro requerimiento del proyecto.
* **Completo:** Contiene toda la información necesaria para su desarrollo.
* **Atómico:** Expresa una sola idea o función de forma independiente.
* **Trazable:** Permite rastrear su origen histórico y las partes del sistema que afecta.

---

## 2. Requerimientos Funcionales (RF)

### Definición
Un requerimiento funcional describe una acción concreta, tarea o cálculo que el sistema debe ejecutar como respuesta a una entrada específica. Define el comportamiento directo del software.

### Identificación en el Discurso
Para reconocerlos en documentos o entrevistas, se debe prestar atención a:
* **Verbos de acción:** Registrar, calcular, mostrar, enviar, validar, modificar.
* **Flujos de datos:** Entradas específicas que generan salidas determinadas.
* **Reglas de decisión:** Caminos lógicos condicionales ("si ocurre X, el sistema hace Y").

### Estructura Estándar de Redacción
Se recomienda seguir la siguiente plantilla formal:
`El sistema deberá + [acción/verbo] + [objeto] + [condiciones o restricciones].`

### Categorías Principales
* **Autenticación:** Gestión de accesos, contraseñas y permisos de usuarios.
* **Cálculo:** Operaciones matemáticas y estadísticas sobre los datos.
* **Persistencia (CRUD):** Almacenamiento, lectura, modificación y borrado de información.
* **Comunicación:** Envió de notificaciones, correos electrónicos o mensajes de texto.
* **Reporte:** Generación y exportación de documentos en formatos específicos.
* **Validación:** Comprobación de formatos, reglas del negocio y restricciones de datos.

---

## 3. Requerimientos No Funcionales (RNF)

### Definición
Un requerimiento no funcional especifica cómo debe comportarse el sistema y bajo qué restricciones de calidad. No determina qué tareas hace, sino la calidad con la que las ejecuta. Un sistema puede cumplir todas sus funciones pero ser un fracaso rotundo si sus requerimientos no funcionales fallan.

### Categorías de Calidad
* **Rendimiento:** Tiempos de respuesta y uso óptimo de recursos de cómputo.
* **Seguridad:** Protocolos de cifrado, políticas de acceso y resguardo de datos.
* **Usabilidad:** Facilidad de aprendizaje, accesibilidad y comodidad para el usuario.
* **Confiabilidad:** Nivel de disponibilidad del sistema y tolerancia ante fallos.
* **Escalabilidad:** Capacidad de soportar incrementos masivos de usuarios concurrentes.
* **Mantenibilidad:** Facilidad para corregir errores, actualizar el código y realizar pruebas.
* **Portabilidad:** Compatibilidad con diferentes sistemas operativos, navegadores y dispositivos.
* **Legales:** Cumplimiento de normativas vigentes (como la Ley 1581 de 2012 de protección de datos en Colombia).

### El Criterio de la Medición
Cualquier requerimiento no funcional que no incluya una métrica clara y un umbral aceptable se considera un simple deseo y no una especificación técnica utilizable. Todo debe poder medirse y verificarse.

### Conflictos de Interés (Trade-offs)
La mejora de un requerimiento no funcional suele perjudicar a otro. El analista debe balancear estas decisiones según las prioridades del negocio:
* **Seguridad vs. Usabilidad:** Añadir múltiples pasos de verificación hace al sistema más seguro pero menos cómodo para el usuario.
* **Rendimiento vs. Mantenibilidad:** Un código extremadamente optimizado para la velocidad puede volverse muy difícil de entender y modificar más adelante.
* **Escalabilidad vs. Costo:** Soportar millones de usuarios simultáneos requiere una infraestructura en la nube compleja y costosa.

---

## 4. Atributos de Calidad (Norma ISO/IEC 25010)

### Concepto General
Los atributos de calidad son los conceptos abstractos que definen la excelencia de un producto de software. La norma internacional ISO/IEC 25010 los clasifica en 8 categorías principales.



### Relación entre Atributos y RNF
* El **Atributo de Calidad** es el concepto conceptual (Ejemplo: Seguridad).
* El **Requerimiento No Funcional** es la aplicación concreta y medible de ese atributo en el proyecto (Ejemplo: "Las contraseñas se almacenarán cifradas con bcrypt factor 12").

### Los 8 Atributos de la Norma
1. **Adecuación Funcional:** Capacidad del software para cumplir con todas las tareas solicitadas de forma correcta.
2. **Eficiencia de Desempeño:** Optimización de tiempos de procesamiento y recursos de hardware.
3. **Compatibilidad:** Habilidad para coexistir e intercambiar información con otras aplicaciones.
4. **Usabilidad:** Facilidad con la que los usuarios comprenden y operan la interfaz.
5. **Confiabilidad:** Capacidad de mantener un nivel de operación continuo ante condiciones adversas.
6. **Seguridad:** Protección de la información contra accesos no autorizados y garantía de la identidad de los datos.
7. **Mantenibilidad:** Facilidad para modificar, corregir o evolucionar el código fuente.
8. **Portabilidad:** Capacidad de transferir el software de un entorno operativo a otro de manera efectiva.

---

## 5. El Arte de Elicitar Requerimientos

### Definición y Mentalidad
Elicitar significa descubrir de forma activa las necesidades reales de los usuarios, yendo más allá de lo que ellos expresan verbalmente. No es una recopilación pasiva de datos, sino un proceso de investigación donde el analista actúa como un detective. Los clientes suelen proponer soluciones basadas en lo que conocen en lugar de explicar el problema de raíz.

### Las 3 Técnicas Fundamentales
* **Entrevistas:** Conversaciones individuales profundas. Permiten explorar detalles a fondo, aunque requieren bastante tiempo.
* **Encuestas:** Cuestionarios cerrados distribuidos a grupos grandes. Proveen datos numéricos y estadísticos de forma rápida, pero carecen de profundidad.
* **Observación:** Análisis directo de los usuarios en su entorno de trabajo real. Permite descubrir procesos automatizados, costumbres y atajos que las personas olvidan mencionar en las entrevistas.

### El Fenómeno del Iceberg
* **Lo que se expresa:** Las peticiones explícitas de los clientes ("Quiero una pantalla azul con un botón").
* **Lo que se piensa en silencio:** Las motivaciones competitivas o comerciales latentes.
* **Lo inconsciente:** Los miedos al cambio tecnológico, las costumbres diarias instaladas y las rutinas organizacionales implícitas.

### Habilidades Esenciales
* **Escucha Activa:** Prestar atención total al usuario, sin interrumpir ni preparar respuestas mentales anticipadas.
* **Curiosidad Iterativa:** Indagar de forma constante el origen de cada respuesta para hallar el problema inicial.
* **Manejo del Silencio:** Tolerar las pausas en la conversación, las cuales suelen preceder a explicaciones clave.
* **Evitar Suposiciones:** No dar nada por sentado. Cada elemento obvio debe ser validado directamente con los interesados.

---

## 6. Ejecución de Entrevistas, Encuestas y Observación

### Tipos de Entrevistas
* **Estructurada:** Sigue una lista fija y cerrada de preguntas. Es útil para comparar respuestas de diferentes personas, pero no permite descubrir imprevistos.
* **No Estructurada:** Se desarrolla como una conversación libre. Sirve para fases iniciales de exploración, aunque su análisis posterior resulta complejo.
* **Semiestructurada:** Utiliza un guion guía pero otorga la libertad de profundizar en temas de valor que surjan durante la charla. Es el formato más balanceado.

### Las Etapas de la Entrevista
1. **Planificación:** Investigar el perfil del entrevistado, fijar los objetivos técnicos y redactar las preguntas clave.
2. **Desarrollo:** Crear un clima de confianza, plantear preguntas abiertas, registrar las respuestas y realizar resúmenes periódicos para validar la información.
3. **Consolidación:** Organizar y transcribir las notas en las primeras 24 horas para evitar la pérdida de detalles esenciales.

### Diseño Técnico de Encuestas
* **Extensión:** Limitar el cuestionario a un máximo de 10 o 15 preguntas para reducir la tasa de abandono.
* **Claridad:** Redactar preguntas directas centradas en una única idea a la vez, evitando el uso de tecnicismos informáticos.
* **Escala Likert:** Utilizar opciones graduadas del 1 al 5 para medir actitudes, opiniones y frecuencias de forma cuantitativa.

### Metodología de Observación y el Efecto Hawthorne
Al observar el entorno de trabajo, se deben registrar las herramientas utilizadas, las interacciones personales y los retrasos operativos en bitácoras estructuradas por horas.
* **Efecto Hawthorne:** Reacción psicológica por la cual las personas alteran temporalmente su comportamiento habitual al saberse observadas. Para contrarrestarlo, el analista debe prolongar sus sesiones de observación hasta que su presencia se vuelva parte de la rutina normal del lugar.

---

## 7. Análisis de Viabilidad

### Definición
Es la evaluación formal que realiza el analista para determinar si un requerimiento solicitado por el cliente puede cumplirse de manera realista en la práctica, actuando como un filtro ético y profesional.

### Las 5 Dimensiones de Análisis
1. **🛠️ Técnica:** Disponibilidad de la tecnología necesaria y nivel de capacitación del equipo de desarrollo.
2. **💰 Económica:** Evaluación de si el presupuesto asignado cubre el costo de infraestructura, licencias y horas de trabajo.
3. **👥 Operativa:** Grado de aceptación del software por parte de los usuarios y su alineación con los procesos de la organización.
4. **📜 Legal:** Cumplimiento estricto de leyes de privacidad, accesibilidad, derechos de autor y normativas del sector.
5. **⏱️ Temporal:** Factibilidad de completar el desarrollo dentro de los plazos solicitados por el cliente.

### Criterios de Decisión (Semáforo de Viabilidad)
* **Verde (Alta viabilidad):** El proyecto cuenta con las condiciones adecuadas para iniciar su desarrollo.
* **Amarillo (Viabilidad media):** Existen riesgos o limitaciones. Se requiere renegociar el alcance, extender los plazos o ajustar el presupuesto.
* **Rojo (Baja viabilidad):** El requerimiento infringe normativas legales o supera las capacidades económicas y temporales. No debe iniciarse en esas condiciones.

---

## 8. La Importancia de Documentar

### Mente vs. Papel
Confiar la definición de un sistema exclusivamente a la memoria del equipo genera riesgos graves. Los detalles técnicos se desvanecen en pocos días, la información se vuelve subjetiva y el conocimiento desaparece si algún miembro clave se retira del proyecto. Un documento escrito mantiene las especificaciones inalterables en el tiempo, unifica los criterios del equipo de desarrollo y funciona como un respaldo legal ante controversias.

### Funciones de la Documentación en el Proyecto
* **Pacto Contractual:** Actúa como un acuerdo formal entre el cliente y el equipo técnico sobre el alcance del producto.
* **Guía de Desarrollo:** Funciona como el mapa de ruta para los programadores, evitando ambigüedades en la implementación.
* **Criterio de Aceptación:** Provee la base técnica para que el equipo de control de calidad diseñe las pruebas del sistema.
* **Memoria Técnica:** Preserva el conocimiento del software frente a la rotación de personal.

---

## 9. El Estándar IEEE 830 para Documentos SRS

La Especificación de Requerimientos de Software (SRS) estructurada bajo el estándar IEEE 830 organiza la información del proyecto en cuatro secciones principales:

### Estructura del Documento Maestro
1. **Introducción:** Describe el propósito del documento, el alcance del sistema, glosarios de términos y referencias normativas o legales.
2. **Descripción General:** Presenta la perspectiva del producto, sus funciones principales, las características de los usuarios, las restricciones del entorno y las suposiciones iniciales.
3. **Requisitos Específicos:** El núcleo del documento. Contiene el listado numerado de todos los requerimientos funcionales y no funcionales, las interfaces con otros sistemas y los criterios de aceptación.
4. **Apéndices:** Incluye información complementaria como diagramas de arquitectura, bocetos de interfaz y matrices de trazabilidad.

---

## 10. Casos de Uso (CU)

### Concepto y Propósito
Un caso de uso es una descripción narrativa que detalla la secuencia ordenada de pasos en los que un actor interactúa con el sistema para cumplir un objetivo específico. Mientras el requerimiento define una obligación del software en una sola frase, el caso de uso narra detalladamente cómo se ejecuta dicha acción.

### Componentes de un Caso de Uso
* **Actor:** Cualquier entidad externa (persona, hardware o sistema de software) que interactúa con la aplicación de forma directa.
* **Sistema:** El límite del software que procesa las solicitudes y reacciona ante las acciones del actor.
* **Objetivo:** La meta concreta que el actor desea alcanzar al iniciar el proceso.
* **Escenario:** El conjunto de flujos de pasos ordenados que describen la interacción.

### Relaciones en Diagramas UML
* **Inclusión (`‹‹include››`):** Se utiliza cuando un caso de uso requiere obligatoriamente la ejecución de otro flujo para completar su tarea.
* **Extensión (`‹‹extend››`):** Se aplica para añadir pasos opcionales al flujo principal, los cuales se activan únicamente si se cumple una condición lógica específica.

---

## 11. Historias de Usuario (Enfoque Ágil)

### Concepto y Estructura
En las metodologías ágiles de desarrollo, las historias de usuario representan una forma conversacional de registrar requerimientos desde la perspectiva del usuario que percibe el valor de la función. Se estructuran bajo la siguiente sintaxis:
* **Como** `[tipo de usuario]`
* **Quiero** `[acción o funcionalidad]`
* **Para** `[beneficio u objetivo esperado]`

### El Criterio de Calidad INVEST
Para asegurar que una historia de usuario esté bien redactada, debe cumplir con las siguientes características del acrónimo INVEST:
* **I - Independiente:** Su valor se puede entender y desarrollar sin depender obligatoriamente de otras historias.
* **N - Negociable:** No funciona como un contrato cerrado, sino como un punto de partida para la discusión y el refinamiento en el equipo.
* **V - Valiosa:** Aporta un beneficio claro y explícito para el usuario o el negocio.
* **E - Estimable:** El equipo técnico posee la información suficiente para calcular el esfuerzo o tiempo necesario para su desarrollo.
* **S - Small (Pequeña):** Su alcance es lo suficientemente acotado como para completarse dentro de un ciclo de desarrollo corto o sprint.
* **T - Testable (Verificable):** Cuenta con criterios de aceptación claros que permiten comprobar si la función se implementó correctamente.

### Estructura de Criterios de Aceptación
Se redactan bajo el formato lógico **Given / When / Then** (Dado / Cuando / Entonces) para definir el comportamiento esperado ante diferentes escenarios:
* **Dado** `[contexto inicial o estado del sistema]`
* **Cuando** `[el usuario realiza una acción específica]`
* **Entonces** `[el sistema reacciona y produce un resultado determinado]`

---

## 12. Plantilla y Caso de Estudio Integrado: "SchoolEats" y "Biblioteca Escolar"

A continuación se presenta la aplicación práctica de los conceptos mediante un documento de especificación técnica adaptado para un sistema de biblioteca escolar.

### Especificación de Requerimientos de Software (SRS) - Caso: Sistema de Biblioteca

#### 1. Introducción
* **1.1 Propósito:** Este documento define las especificaciones para el desarrollo del Sistema de Gestión de Biblioteca Escolar (SGBE). Su objetivo es eliminar el registro en cuadernos físicos y automatizar el control de préstamos. Está dirigido al equipo de desarrollo y al personal administrativo del colegio.
* **1.2 Alcance:** El software abarcará la búsqueda de textos en línea, la reserva digital de ejemplares, el control de inventario de libros y la emisión de alertas de vencimiento. Quedan excluidos los procesos de compra de libros y la contabilidad financiera de la institución.
* **1.3 Referencias Legales:** Ley 1581 de 2012 (Régimen General de Protección de Datos Personales en Colombia).

#### 2. Descripción General
* **2.1 Restricciones del Proyecto:** El desarrollo cuenta con un presupuesto total de 15 millones de pesos y un plazo estricto de entrega de 4 meses. Debe operar de forma multiplataforma mediante entorno web y aplicación móvil nativa.
* **2.2 Perfiles de Usuario:** Estudiantes (800 usuarios con necesidades de consulta y reserva), Profesores (40 usuarios con permisos de solicitudes grupales) y Bibliotecarios (3 usuarios administrativos con control total del inventario).

#### 3. Requisitos Específicos

##### Requerimientos Funcionales (RF)
* **RF-001:** El sistema deberá permitir a los usuarios buscar textos en el catálogo ingresando el título, autor o categoría temática.
* **RF-002:** El sistema deberá permitir reservar un ejemplar en estado "disponible" por un tiempo máximo de 72 horas.
* **RF-003:** El sistema deberá registrar los préstamos vinculando el identificador del libro, el documento del usuario y las fechas límite de entrega.
* **RF-004:** El sistema deberá emitir reportes mensuales automáticos con el listado de los 20 libros más solicitados por los usuarios.

##### Requerimientos No Funcionales (RNF)
* **RNF-001 (Rendimiento):** El tiempo de procesamiento para las consultas en el catálogo no deberá superar los 2 segundos para el 95% de las peticiones.
* **RNF-002 (Confiabilidad):** La plataforma deberá garantizar una disponibilidad continua del 99.5% durante la jornada escolar activa (07:00 a 17:00).
* **RNF-003 (Seguridad):** Las contraseñas de acceso de todos los perfiles deberán guardarse en la base de datos cifradas mediante el algoritmo bcrypt factor 12.

---

### Modelo de Documentación de Caso de Uso

| Componente | Definición Aplicada |
| :--- | :--- |
| **Identificador** | CU-001 |
| **Nombre** | Reservar Libro |
| **Actor Principal** | Estudiante Autenticado |
| **Precondiciones** | El alumno no presenta multas vigentes ni supera el límite de 3 reservas activas. |
| **Flujo Principal** | 1. El estudiante selecciona el ejemplar en el catálogo.<br>2. El sistema valida el estado de disponibilidad.<br>3. El estudiante confirma el apartado del libro.<br>4. El sistema cambia el estado del libro a "Reservado" y emite un comprobante digital. |
| **Excepciones** | Si el libro no tiene copias disponibles, el sistema bloquea la acción y ofrece al usuario la opción de ingresar a una lista de espera. |
| **Reglas de Negocio**| Las reservas se cancelan de forma automática si el ejemplar no es retirado físicamente en un plazo de 72 horas. |

---

## 13. El Proceso de Revisión Cruzada

### Concepto y Dinámica de Control de Calidad
La revisión cruzada consiste en someter el documento SRS elaborado al análisis de otros miembros del equipo técnico antes de proceder a la fase de desarrollo o firma del contrato. Esta revisión busca identificar incoherencias o errores que el autor original ya no percibe debido al cansancio o a la familiaridad con el texto.

### Defectos Críticos a Mitigar
* **Uso de Lenguaje Subjetivo:** Expresiones ambiguas como "la interfaz debe ser moderna", "el sistema debe ser rápido" o "la aplicación debe ser segura". Deben eliminarse y sustituirse por rangos numéricos y métricas objetivas.
* **Mezcla de Conceptos (Falta de Atomicidad):** Agrupar diferentes tareas en un único enunciado (por ejemplo: "El sistema permitirá cancelar reservas, emitir reportes en Excel y enviar alertas por mensaje"). Cada función debe separarse con su propio identificador único para poder desarrollarse y probarse de manera independiente.
* **Introducción Prematura de Detalles de Diseño:** Incluir nombres específicos de tablas de bases de datos, rutas exactas de red o líneas de código técnico dentro de los requerimientos funcionales. Esos elementos pertenecen exclusivamente a la fase de arquitectura técnica y diseño de software, no a la especificación de las necesidades del usuario.