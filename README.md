I don't know much English, so I used AI for the following text:

# Grammar Checker
Grammar Checker es una extensión de Chrome diseñada para revisar y mejorar la gramática y ortografía en múltiples idiomas utilizando la API de OpenAI.
Características

# Requisitos

API de OpenAI: Necesitarás una clave de API para que la extensión funcione. Puedes registrarte en OpenAI y obtener una clave en su sitio web.
Navegador Chrome: La extensión fue desarrollada y probada en Google Chrome.

# Corrección de Gramática y Ortografía: Revisa textos en múltiples idiomas y proporciona sugerencias de corrección.
Soporte Multi-Idioma: La extensión admite los siguientes idiomas:

Español
Inglés
Francés
Alemán
Italiano
Portugués
Indonesio
Polaco
Vietnamita
Javanés
Turco


Resaltado de Errores Sin Modificar el Texto Original: La extensión identifica errores en el texto y los resalta sin modificar el contenido original. Los errores se subrayan con una línea punteada y al pasar el cursor sobre ellos se muestra una sugerencia de corrección.
Detección Automática de Idioma: La extensión detecta automáticamente el idioma del texto.
Interfaz Amigable: Proporciona una interfaz simple donde puedes ingresar texto, ver errores resaltados y copiar el resultado.
Personalización de API: Permite ingresar y guardar tu clave de API de OpenAI en la configuración.
Soporte para Textos Largos: Puede revisar textos de hasta 2500 palabras.

# Instalación

Clona o descarga este repositorio.
Abre Chrome y ve a chrome://extensions/.
Activa el Modo Desarrollador en la esquina superior derecha.
Haz clic en "Cargar extensión sin empaquetar" y selecciona la carpeta donde descargaste este repositorio.

# Configuración

Haz clic en el ícono de la extensión en la barra de herramientas de Chrome.
Ingresa tu clave de API de OpenAI en el campo correspondiente y haz clic en "Guardar API".
Puedes obtener una clave de API en OpenAI API Keys.
La clave de API se almacena de forma segura en el almacenamiento de Chrome.

# Uso

Abre la extensión haciendo clic en el ícono de Grammar Checker.
Ingresa el texto que deseas revisar en el campo de entrada (hasta 2500 palabras).
Haz clic en "Revisar Gramática" para recibir sugerencias de corrección.
Las palabras con errores se resaltarán con un subrayado punteado. Al pasar el cursor sobre ellas se mostrará una sugerencia de corrección.
Puedes copiar el texto original (sin modificaciones) haciendo clic en "Copiar texto corregido".

# Archivos Principales

background.js: Gestiona eventos de instalación, configuración y permisos de la extensión.
manifest.json: Define la configuración y permisos de la extensión.
popup.html: Contiene la interfaz de usuario para ingresar y revisar texto.
popup.js: Controla la lógica de corrección gramatical, detección de idioma, resaltado de errores y comunicación con la API de OpenAI.
styles.css: Define el diseño y estilo de la interfaz, incluyendo el resaltado de errores.
content.js: Maneja la selección de texto y comunicación con la página web.
options.html y options.js: Permiten a los usuarios configurar la clave de API de OpenAI y el modelo.

# Notas Importantes

Límite de Palabras: La extensión permite revisar textos de hasta 2500 palabras.
Privacidad: Todo el texto procesado se envía a la API de OpenAI para correcciones. Evita incluir información sensible en el texto enviado.
Resaltado de Errores Sin Modificar el Texto Original: La extensión resalta errores gramaticales y ortográficos sin modificar el texto original, permitiendo a los usuarios ver los errores sin afectar el contenido.

# Contribución
Si deseas contribuir al proyecto, por favor haz un fork del repositorio, crea una nueva rama para tus cambios y envía un pull request.
Licencia
Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.
