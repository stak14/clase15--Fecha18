# Proyecto de Registro y Modal Estilo Matrix (.DARKWEB)

Este proyecto es una página web que presenta un formulario de registro estilizado con una temática "Matrix" y una ventana modal interactiva. La página incluye un fondo animado de "lluvia de código" característico de Matrix.

## ✨ Características

* **Formulario de Registro Interactivo:**
    * Campos para Nombre (First Name), Apellido (Last Name), Nombre de Usuario (Username), Contraseña (Password), Confirmación de Contraseña (Confirm Password) y Fecha de Nacimiento (Birthday).
    * Validación en tiempo real para los campos del formulario:
        * Nombre y Apellido: Solo letras y espacios.
        * Nombre de Usuario: Mínimo 4 caracteres.
        * Contraseña: Mínimo 8 caracteres, incluyendo al menos una letra mayúscula, un número y un símbolo especial (!@#$%^&*).
        * Confirmación de Contraseña: Debe coincidir con la contraseña ingresada.
        * Fecha de Nacimiento: Campo obligatorio. Se valida que el usuario sea mayor de edad (en el script actual, está configurado para mayores de 13 años, aunque el mensaje de error indica 21 años, lo cual es una inconsistencia a revisar en el código).
    * Opción para suscribirse a un boletín (checkbox).
    * Mensajes de error dinámicos debajo de cada campo si la validación falla.
    * Alerta de confirmación al enviar el formulario exitosamente.
* **Modal Interactivo:**
    * Un botón "Abrir Modal" para mostrar una ventana emergente.
    * El modal presenta un mensaje de "Alerta en Matrix" con opciones para "Salir de la Matrix" o "Quedarse".
    * Botones de acción en el modal que disparan alertas de JavaScript.
    * Se puede cerrar el modal haciendo clic en el botón de cierre (X) o fuera del contenido del modal.
* **Estilo Visual "Matrix":**
    * **Fondo Animado "Matrix Rain":** Un `<canvas>` renderiza una animación de caracteres cayendo, simulando el efecto icónico de Matrix.
    * **Diseño Oscuro y Neón:** Uso de colores oscuros para el fondo y colores neón (azul y verde) para textos, bordes y brillos, creando una atmósfera cyberpunk.
    * **Tipografía Monospace:** Se utiliza la fuente 'Share Tech Mono' para reforzar la estética hacker/tech.
    * **Animaciones Sutiles:**
        * Efecto `fadeInGlow` para la aparición del contenedor del formulario y el modal.
        * Efecto `flicker` para los mensajes de error.
        * Transiciones y sombras en botones e inputs al interactuar (hover, focus).
* **Estructura y Tecnologías:**
    * HTML semántico para la estructura del contenido.
    * CSS3 para el diseño, la tematización y las animaciones, utilizando variables CSS para una fácil personalización de los colores.
    * JavaScript puro (Vanilla JS) para:
        * La lógica de validación del formulario.
        * El control de la interactividad del modal.
        * La generación y animación del efecto "Matrix Rain" en el canvas.

## 🚀 Cómo Empezar

1.  Clona este repositorio o descarga los archivos.
2.  Abre el archivo `Ejemplo1y2.html` en tu navegador web preferido.

No se requieren pasos de compilación ni dependencias externas más allá de la conexión a Google Fonts para la tipografía 'Share Tech Mono'.

## 🛠️ Tecnologías Utilizadas

* **HTML5**
* **CSS3** (con variables CSS para theming)
* **JavaScript (ES6+)**
* **Google Fonts** (para la fuente 'Share Tech Mono')

## 🎨 Estructura del CSS y Tematización

El archivo utiliza variables CSS (custom properties) definidas en el `:root` para gestionar la paleta de colores y facilitar la personalización del tema neón.

Principales variables de color:
* `--neon-blue: #00ffff;`
* `--neon-green: #00ff00;`
* `--dark-bg: #1a1a1a;`
* `--form-bg: #2a2a2a;`
* `--text-color: #e0e0e0;`
* `--error-color: #ff3366;`

## 💡 Posibles Mejoras / Puntos a Notar

* **Consistencia en la Validación de Edad:** El script valida una edad mínima de 13 años pero el mensaje de error indica "Debes tener al menos 21 años para registrarte". Esto debería unificarse.
* **Seguridad de Contraseña:** Aunque hay validación en el frontend, la seguridad real de las contraseñas requiere manejo en el backend y hashing. Este es un ejemplo de frontend únicamente.
* **Accesibilidad (A11y):** Se podrían revisar y mejorar aspectos de accesibilidad, como el contraste de colores para usuarios con baja visión y el uso de atributos ARIA donde sea apropiado.
* **Modularización del JavaScript:** Para proyectos más grandes, el código JavaScript podría dividirse en módulos para una mejor organización.
* **Optimización del Canvas:** Para animaciones de canvas más complejas o de mayor duración, se podrían explorar técnicas de optimización adicionales.

---

Este README provee una visión general del proyecto "Registro y Modal | .DARKWEB".
