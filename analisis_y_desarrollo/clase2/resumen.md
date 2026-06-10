# Componentes Esenciales de la Ingeniería de Requerimientos

## 1. El Concepto y su Entorno

### Definición Técnica
Un requerimiento no es simplemente un deseo o una idea suelta de lo que el sistema debería hacer. Según el estándar IEEE 830, se trata de una característica o restricción debidamente documentada que permite resolver un problema real. Para que una petición sea considerada un requerimiento formal, debe cumplir obligatoriamente con dos condiciones: poder registrarse por escrito y poder comprobarse mediante pruebas.

### El Proceso de Traducción (Abstracción)
El analista actúa como un puente entre el lenguaje cotidiano y el lenguaje de desarrollo, moviéndose en tres niveles:
* **La Necesidad:** Expresada por el usuario de forma común y directa (por ejemplo, querer saber qué van a servir de almuerzo para decidir si hacer la fila).
* **El Requerimiento:** El analista lo formaliza (el sistema debe publicar el menú diario para los usuarios registrados).
* **La Especificación:** Se transforma en instrucciones de software precisas (diseñar un endpoint que devuelva la información del menú en un formato específico y bajo ciertos parámetros de tiempo).

### Origen de la Información
Las peticiones provienen de diferentes actores con intereses particulares en el proyecto: los usuarios que operan el sistema a diario, los clientes que financian el desarrollo, el marco legal que regula el manejo de datos y los sistemas externos con los que se debe conectar la plataforma.

### Condiciones de un Requerimiento Profesional
Para que el desarrollo sea viable, cada requerimiento debe ser claro y poseer las siguientes características: ser indispensable para el negocio, admitir una única interpretación, poder evaluarse con claridad, no entrar en contradicción con otras reglas, incluir todos los detalles necesarios, abordar una sola función a la vez y permitir el rastreo de su origen.

---

## 2. Requerimientos Funcionales

Representan los componentes operativos del sistema; es decir, describen de manera explícita las tareas y acciones que el software ejecutará ante determinados estímulos.

* **Detección:** Se identifican mediante verbos orientados a la acción, reglas de control y la definición de roles específicos para cada tipo de usuario.
* **Estructura de Redacción:** Se utiliza una base clara: "El sistema deberá + [acción a realizar] + [entidad u objeto afectado] + [condiciones límites]".

### Clasificación Operativa
* **Gestión de Acceso:** Control de ingresos, registros de cuenta y validación de permisos.
* **Procesamiento de Datos:** Cálculos internos y operaciones lógicas o numéricas.
* **Almacenamiento (CRUD):** Registro, modificación, lectura y eliminación de datos en la base del sistema.
* **Flujos de Comunicación:** Envío de mensajes automatizados, alertas o correos.
* **Salidas de Información:** Creación de reportes y exportación de archivos en formatos estándar.
* **Reglas de Validación:** Filtros de control para garantizar la calidad de la información ingresada.

---

## 3. Requerimientos No Funcionales

Determinan los criterios de calidad y el comportamiento general del entorno técnico. No detallan lo que el sistema hace, sino las condiciones operativas bajo las cuales trabaja. Un requerimiento de este tipo que no incluya una forma de medirse se considera únicamente una expectativa, no una regla de diseño.

### Criterios de Rendimiento y Comportamiento
* **Eficiencia:** Tiempos máximos de espera y procesamiento de datos.
* **Protección:** Mecanismos de cifrado de credenciales y resguardo de la información.
* **Experiencia:** Facilidad de aprendizaje y nivel de esfuerzo requerido por el usuario.
* **Disponibilidad:** Capacidad del sistema para mantenerse operativo sin caídas inesperadas.
* **Crecimiento:** Tolerancia al incremento simultáneo de tráfico o volumen de información.
* **Código Limpio:** Viabilidad técnica para aplicar futuras mejoras o correcciones al software.
* **Compatibilidad:** Capacidad de operar correctamente en distintos navegadores o sistemas operativos.
* **Cumplimiento:** Adaptación a las normativas legales de la región geográfica correspondiente.

*Nota del Analista:* El diseño requiere equilibrar los compromisos técnicos. Aumentar las capas de protección informática suele incrementar los pasos para el usuario, del mismo modo que diseñar una infraestructura para soportar millones de consultas en tiempo real eleva significativamente los costos de mantenimiento.

---

## 4. Atributos de Calidad (Norma ISO/IEC 25010)

Son los pilares teóricos globales que miden el valor técnico de un producto de software. Los requerimientos no funcionales son la aplicación práctica de estos atributos.

1.  **Idoneidad Funcional:** Grado en que las funciones cubren las necesidades reales planteadas.
2.  **Eficiencia de Desempeño:** Optimización de recursos de hardware y velocidad de respuesta.
3.  **Compatibilidad:** Capacidad de interactuar y compartir datos con otras aplicaciones.
4.  **Usabilidad:** Facilidad de uso y accesibilidad para todo tipo de personas.
5.  **Fiabilidad:** Consistencia del sistema ante fallos bajo condiciones específicas.
6.  **Seguridad:** Resguardo de la confidencialidad e integridad de la información del negocio.
7.  **Mantenibilidad:** Facilidad para probar, modificar y evolucionar el código fuente.
8.  **Portabilidad:** Capacidad de traslado de la aplicación de un entorno de ejecución a otro.

---

## 5. Caso Práctico: Aplicación Escolar "SchoolEats"

### Contexto del Problema
La cafetería de una institución educativa presenta inconvenientes logísticos: tiempos excesivos de espera en las horas de almuerzo, falta de previsión en la cantidad de porciones a cocinar, incertidumbre sobre los platos disponibles e inconvenientes asociados al manejo de dinero en efectivo.

### Estrategia de Investigación
Para levantar la información se dividen las acciones según el volumen del público: se aplican formularios digitales masivos para estudiantes y padres, observación directa y entrevistas breves con el personal de cocina, y sesiones de planeación estructuradas con la dirección del colegio.

### Definición del Entorno del Sistema
* **Componentes Funcionales prioritarios:** Visualización del menú diario, reserva digital de almuerzos con débito de saldo interno y emisión de balances de consumo en formato digital.
* **Componentes No Funcionales obligatorios:** Garantizar estabilidad total durante la jornada de descanso escolar, compatibilidad con plataformas móviles y respuestas del servidor en lapsos mínimos de tiempo.
* **Atributos Esenciales:** Para este modelo de negocio, los factores clave son la estabilidad operativa (evitar que el sistema falle cuando todos intentan comprar), la usabilidad (diseño ágil para menores) y la seguridad informática (control de saldos de dinero).

---

## 6. Historias de Usuario

Metodología ágil para documentar el alcance del proyecto desde la perspectiva del beneficio real que recibe la persona.

### Estructura Base
* **Como:** [Definición del rol de usuario]
* **Quiero:** [Descripción de la funcionalidad solicitada]
* **Para:** [Propósito o valor que aporta al día a día]

### El Criterio de Calidad INVEST
Las historias deben procurar ser independientes entre sí, abiertas a la negociación con el equipo, valiosas para el usuario final, posibles de estimar en tiempo, con un alcance pequeño que quepa en un ciclo corto de trabajo y totalmente verificables.

### Aplicación Práctica con Reglas de Aceptación
**Caso de uso:** Visualización de opciones de comida desde el dispositivo móvil.
* **Escenario de visualización estándar:** Dado que el estudiante ha iniciado sesión, cuando accede a la sección principal, el sistema muestra el menú del día con su respectiva información visual, nombre del plato y costo.
* **Escenario de producto agotado:** Dado que un menú se ha quedado sin existencias en la cocina, cuando el usuario refresca la aplicación, la opción se muestra deshabilitada con una etiqueta de advertencia.
* **Escenario de contingencia de red:** Dado que el teléfono pierde la conexión de datos, cuando se intenta consultar la información, la aplicación despliega el último registro almacenado de forma local junto con un aviso informativo.