# Resumen Completo: Fundamentos de la Ingeniería de Software

## 1. La Importancia del Análisis y Diseño
El desarrollo de software exitoso requiere planificación previa. Intentar programar sin entender el problema genera caos, retrasos y productos defectuosos.

* **Análisis:** Define el **QUÉ** se va a construir (entender el problema, usuarios, necesidades y restricciones).
* **Diseño:** Define el **CÓMO** se va a construir (planificar la solución, arquitectura, tecnologías e interfaz).
* **Programación:** Es únicamente el último paso del proceso.

> **La Estadística Clave:** El **66%** de los proyectos de software fracasan o presentan graves problemas (Standish Group). La causa principal no es la programación, sino los **requerimientos mal definidos**.

### La Regla del 1-10-100
Esta regla demuestra que corregir un error es exponencialmente más caro a medida que avanza el proyecto:
* **Análisis:** $1$
* **Diseño:** $10$
* **Programación:** $100$
* **Producción:** $1000+$

---

## 2. El Ciclo de Vida del Software
Es el conjunto de etapas por las que pasa un sistema desde su concepción hasta que se vuelve obsoleto. Aunque teóricamente son secuenciales, en la práctica moderna son **cíclicas**.



[Image of software development life cycle phases]


1. **Análisis de Requerimientos:** Conversación con clientes para documentar qué debe hacer el sistema. *Resultado: Especificación de Requerimientos.*
2. **Diseño:** Definición de la arquitectura, módulos, bases de datos e interfaces. *Resultado: Planos y prototipos.*
3. **Implementación (Programación):** Escritura del código fuente basado en los diseños. *Resultado: Software funcional (no probado).*
4. **Pruebas:** Verificación de errores y cumplimiento de requisitos. *Resultado: Reporte de errores corregidos.*
5. **Despliegue:** Entrega e instalación del software en el entorno real del cliente. *Resultado: Sistema en producción.*
6. **Mantenimiento:** Corrección de fallos emergentes y adición de nuevas funciones. *Resultado: Versiones mejoradas.*

---

## 3. Metodologías de Desarrollo

### A. Metodologías Estructuradas (Tradicionales)
Se basan en planificar todo al inicio y seguir el plan de forma estricta. Son ideales para proyectos con requerimientos estables y sistemas críticos.

* **Modelo Cascada (Waterfall):** Secuencial puro. Cada fase debe terminar por completo antes de iniciar la siguiente. No permite regresar.
* **Modelo en V:** Variante de la cascada donde cada fase de desarrollo tiene una fase de pruebas correspondiente (ej. Diseño de módulos $\rightarrow$ Pruebas unitarias).
* **Modelo Espiral:** Enfoque cíclico centrado en el análisis y reducción de riesgos en cada iteración.



[Image of waterfall versus agile software development methodology]


### B. Metodologías Ágiles
Nacidas del *Manifiesto Ágil (2001)*, priorizan el valor del software funcionando, la colaboración y la respuesta rápida al cambio sobre los procesos y la documentación extensa. Trabajan mediante **iteraciones** cortas (1-4 semanas).

* **Scrum:** Marco basado en *Sprints* (ciclos cortos), reuniones diarias (*Daily standups*) y roles definidos (*Product Owner*, *Scrum Master*, *Equipo de desarrollo*).
* **Kanban:** Tablero visual enfocado en el flujo de trabajo mediante columnas (Por hacer, Haciendo, Probando, Hecho). Su regla de oro es limitar el trabajo en curso (WIP).
* **XP (Extreme Programming):** Enfoque técnico que promueve la programación en pares, el desarrollo guiado por pruebas (TDD) y la refactorización constante.

### Tabla Comparativa

| Criterio | Estructuradas 📏 | Ágiles ⚡ |
| :--- | :--- | :--- |
| **Planificación** | Toda al inicio | Continua, en cada sprint |
| **Cambios** | Difíciles y costosos | Bienvenidos en cualquier momento |
| **Documentación** | Extensa y formal | La mínima necesaria |
| **Cliente** | Ve el producto al final | Participa constantemente |
| **Equipo ideal** | Grande, especializado | Pequeño, multifuncional |
| **Riesgo** | Alto si se detectan fallos tarde | Bajo, se detectan rápido |
| **Mejor para...** | Sistemas críticos, regulados (bancos, salud) | Productos comerciales, apps, startups |

---

## 4. Ingeniería de Requerimientos
Un requerimiento es la descripción de lo que el sistema debe hacer o una restricción que debe cumplir.

### Tipos de Requerimientos
* **Funcionales (QUÉ):** Acciones concretas que realiza el sistema. *Ejemplo: "El sistema debe permitir registrar usuarios".*
* **No Funcionales (CÓMO):** Características de calidad y restricciones del sistema. *Ejemplo: "La página debe cargar en menos de 3 segundos".*

### Cualidades de un Buen Requerimiento (SMART)
Para evitar ambigüedades, los requerimientos deben ser:
* **S**pecific (Específico).
* **M**easurable (Medible).
* **A**chievable (Alcanzable).
* **R**elevant (Relevante).
* **T**ime-bound (Con un plazo/límite).

### Técnicas de Elicitación (Obtención de información)
Los requerimientos se descubren utilizando:
* Entrevistas y encuestas.
* Observación directa del entorno de trabajo.
* Talleres con los interesados (*stakeholders*).
* Análisis de documentos y leyes.
* Construcción de prototipos rápidos.