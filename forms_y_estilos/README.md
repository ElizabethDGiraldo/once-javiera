# 📝 Como realice la encuesta en html y css 

Este documento detalla la estructura y el diseño del código proporcionado, el cual está orientado a una interfaz de captura de datos con un enfoque en la experiencia de usuario (UX) y validación frontend.

---

### 1. 🏗️ Estructura HTML (Estructura de Datos)

El código HTML utiliza etiquetas semánticas para organizar la información de manera lógica y accesible:

*   **Encabezado (`<header>`):** Define el título de la sección con un enfoque directo ("Ingresa y tu información 😼").
*   **Contenedores de Control:**
    *   `fila-doble`: Agrupa los campos de **Nombre** y **Email** para optimizar el espacio horizontal.
    *   `optgroup`: Organiza las opciones del menú desplegable (`<select>`) en categorías lógicas como *Crecimiento personal* y *Laboral*.
*   **Atributos de Validación:**
    *   `required`: Obliga al usuario a completar el campo.
    *   `minlength` / `maxlength`: Restringe la longitud del texto (ej. mínimo 20 caracteres para el mensaje).
    *   `pattern`: Define una expresión regular para validar el formato del número telefónico.
*   **Inputs Especializados:** Utiliza tipos específicos (`email`, `tel`, `radio`, `checkbox`) para mejorar la entrada de datos en dispositivos móviles.

---

### 2. 🎨 Estética y Diseño (CSS Moderno)

El estilo CSS se basa en una metodología limpia y altamente adaptable:

*   **Variables de Entorno (`:root`):**
    > Permiten un mantenimiento centralizado de colores (`--primario`, `--fondo`) y bordes (`--radio`).
*   **Sistema de Rejilla (Grid & Flexbox):**
    *   `display: grid`: Utilizado en `.fila-doble` para crear columnas precisas.
    *   `display: flex`: Aplicado en el `body` para centrar todo el formulario en la pantalla y en las opciones de botones.
*   **Estados de Interacción:**
    *   `focus`: Cambia el color del borde y añade una sombra suave (`box-shadow`) cuando el usuario selecciona un campo.
    *   `valid` / `invalid`: Proporciona retroalimentación visual inmediata (verde para éxito, rojo para error) mediante el uso de la pseudo-clase `:not(:placeholder-shown)`.
*   **Tipografía de Alta Calidad:** 
    *   Implementa fuentes externas mediante Google Fonts: **Trispace** para un aire moderno y **IBM Plex Serif** para un toque de seriedad académica.

---

### 3. 📱 Adaptabilidad (Responsive Design)

El diseño está preparado para múltiples dispositivos mediante **Media Queries**:

*   **Punto de quiebre (520px):**
    *   La rejilla de dos columnas (`.fila-doble`) se transforma en una sola columna para evitar el apiñamiento de texto en smartphones.
    *   Se ajustan los rellenos (`padding`) para maximizar el área de visualización en pantallas pequeñas.

---

### 4. 🚀 Detalles Técnicos Destacados

| Característica | Implementación | Propósito |
| :--- | :--- | :--- |
| **Accesibilidad** | `label for="..."` | Vincula etiquetas con inputs para lectores de pantalla. |
| **Seguridad** | `novalidate` | Desactiva la validación nativa del navegador para permitir una lógica personalizada (o control total vía CSS). |
| **Limpieza** | `box-sizing: border-box` | Asegura que el padding no afecte el ancho total de los elementos. |
| **Interactividad** | `transition` | Crea animaciones suaves de 0.2s al interactuar con los botones e inputs. |